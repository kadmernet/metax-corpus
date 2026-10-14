---
doc_id: "ST-20"
title_en: "Payment Integration and Webhook Trust"
title_ar: "تكامل المدفوعات وثقة الويب هوك"
family: "standard"
version: "v2026.09.2"
status: "canonical · ratification pending"
authority: "governing"
prevailing_text: "en"
audience_tier: 4
evidence_class: "semi-durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.1"
derived_from: ["MX-DESIGN-001 Part 5"]
last_reviewed: "2026-08-30"
domain_tags: ["security", "commerce", "architecture"]
ai_disclosure_url: "../corpus/mx-007-ai-use-and-disclosure.md"
hreflang: "en, ar"
---

# ST-20 — Payment Integration and Webhook Trust

**Governs:** the technical contract between `pay.metax.academy`, the payment processor, and the
entitlement store. Policy is at [MX-021](../corpus/mx-021-payments-and-commerce.md).

> **Blocked.** No part of this standard may be implemented before
> [B-11](../00-governance-map/launch-blockers.md#b-11--the-instruments-the-new-plane-requires-do-not-exist--hard-blocker),
> [B-12](../00-governance-map/launch-blockers.md#b-12--riba-structure-and-payment-rails-are-unreviewed--hard-blocker)
> and [B-13](../00-governance-map/launch-blockers.md#b-13--single-payment-rail--hard-blocker) close.

---

## §1 The trust model, in one rule

> **The return URL is a hint. The signed webhook is the truth.**

Everything in this standard follows from that. A return URL is constructed by the processor and
traversed by the user's browser, which means it is **attacker-reachable**: a user can type it,
replay it, share it, or arrive at it having abandoned payment entirely. Any system that grants
entitlement on a return URL grants entitlement to anyone who can guess a URL shape.

| Signal | Trust | Permitted effect |
|---|---|---|
| Return URL `GET /return/{intent}` | **None** | Display only. May show "checking…" |
| Signed webhook | **Authoritative** | Writes the entitlement record |
| Client-side JS | **None** | Never a source of payment state |

---

## §2 Intent lifecycle

| State | Set by | Meaning |
|---|---|---|
| `created` | `pay.` | Intent exists; quote captured; nothing charged |
| `redirected` | `pay.` | User sent to processor |
| `returned` | Return URL | **Hint only.** Not a state change with effects |
| `confirmed` | **Webhook** | Payment settled. Entitlement written |
| `failed` | Webhook | Plain diagnosis available at `/failed/{intent}` |
| `expired` | `pay.` | Quote window elapsed without settlement |
| `refunded` | Webhook | Entitlement adjusted per [MX-021](../corpus/mx-021-payments-and-commerce.md) |

**Only `confirmed` grants entitlement, and only a verified webhook may set it.**

### §2.1 Retry reuses the intent

`/failed/{intent}` offers a retry that **reuses the intent** rather than creating a new one. A
retry that mints a fresh intent produces orphaned records, double-charge risk, and a reconciliation
problem that surfaces weeks later in an accounting mismatch.

---

## §3 Webhook verification — all five, or reject

A webhook is processed only if **every** condition holds:

1. **Signature valid** against the processor's published key.
2. **Timestamp within tolerance** — 300 s. Outside it, reject as replay.
3. **Intent exists** and is in a state from which the transition is legal.
4. **Amount and asset match** the intent's captured quote.
5. **Event id not previously processed** — idempotency key persisted.

Condition 5 is what makes redelivery safe. Processors redeliver by design, and a handler that is
not idempotent will grant an entitlement twice or refund twice — and the second one will be
discovered by the customer, not by MetaX.

**A webhook failing any condition is logged as a security event**
([MX-011](../corpus/mx-011-security-and-disclosure.md)) and never partially applied. There is no
"probably fine" path.

---

## §4 The processing screen

`/processing/{intent}` polls with an honest message and states explicitly:

> **"You may close this page; your receipt will be emailed."**

**No countdown, no spinner implying imminence, no "do not close this window."** A processing
screen that implies the user must wait is a designed anxiety, and settlement timing is not under
the user's control. Also forbidden: any upsell on this screen, per
[MX-021 §21.1.1](../corpus/mx-021-payments-and-commerce.md#2111-dark-patterns-forbidden-by-name).

---

## §5 Quote, settlement and the receipt

Prices are declared in **one fiat display currency**; settlement is the crypto amount quoted at
intent creation, with the **validity window stated on screen**.

The receipt records **both**:

| Field | Why |
|---|---|
| Fiat display figure | What the buyer agreed to pay |
| Settled amount **and asset** | What actually moved |
| Quote timestamp and window | Makes the conversion auditable |

*A receipt that records only the crypto amount is useless for accounting a year later*, when the
asset's value bears no relation to what was charged.

`/receipt/{id}` is **permanent, static, individually addressable and printable** — the one
identity-plane route with content-plane permanence properties, because a receipt that cannot be
retrieved later is not a receipt.

---

## §6 Method-agnosticism as a build requirement

Binance Pay is the only method today. The integration layer is therefore built so that a second
processor is **configuration, not redesign** — which is what makes
[B-13](../00-governance-map/launch-blockers.md#b-13--single-payment-rail--hard-blocker) closable
rather than a rewrite.

Requirements: no processor name in any route, template or entitlement schema; one adapter interface
(`createIntent`, `verifyWebhook`, `refund`, `quote`); processor identity stored as data on the
intent, never inferred from code paths.

---

## §7 What is forbidden

| Forbidden | Reason |
|---|---|
| Granting entitlement on a return URL | §1 |
| Card or wallet data touching MetaX infrastructure | MetaX is never in the card data path |
| Storing any payment instrument | Nothing to breach |
| Interest, financing, percentage late fees, BNPL | [Charter §0.4.2](../corpus/mx-000-charter.md#2-core-riba-instruments) |
| Split payment totalling more than single payment | [MX-021 §21.2.2](../corpus/mx-021-payments-and-commerce.md#2122-permitted) |
| Any third-party tag on `pay.` | [DS-06 §6.5](../design/ds-06-error-and-empty-states.md#65-analytics-posture) |
| **Any agent write to a payment intent, entitlement or refund** | [AG-009 §2](../agents/ag-009-prohibited-actions.md) — absolute, even under a valid Curator prompt |

---

## §8 Conformance

| Rule | Enforced by | Failure |
|---|---|---|
| Entitlement writes originate only from a verified webhook | Code-path audit + integration test | Build failure |
| All five §3 conditions enforced | Adversarial test suite: bad signature, stale timestamp, replayed id, amount mismatch, illegal transition | Build failure |
| Idempotency under redelivery | Duplicate-delivery test | Build failure |
| No processor name in routes or schema | Static analysis | Build failure |
| Receipt carries both figures | Template gate | Build failure |
| Split-payment equality displayed on the pricing page | Content gate | Build failure |

The §3 adversarial suite is a launch condition under
[B-15](../00-governance-map/launch-blockers.md#b-15--auth-is-unaudited--hard-blocker): the five
conditions must be shown to *reject*, not merely to exist in the code.

---

**Related:** [MX-021 Payments and Commerce](../corpus/mx-021-payments-and-commerce.md) ·
[MX-022 Identity and Sessions](../corpus/mx-022-identity-and-sessions.md) ·
[ST-16 Security Architecture](st-16-security-architecture.md) ·
[ST-19 Two-Plane Architecture](st-19-two-plane-architecture.md) ·
[MX-011 Security and Disclosure](../corpus/mx-011-security-and-disclosure.md)

*Curated by Maher. One rule carries this standard: the return URL is a hint and the webhook is the
truth. Every failure this standard prevents is a failure of trusting the browser.*
