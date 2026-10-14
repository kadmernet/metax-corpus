---
doc_id: MX-003
title_en: Privacy Notice
title_ar: إشعار الخصوصية
family: corpus
version: v2026.10.1
status: published
authority: governing
prevailing_text: ar
audience_tier: 1
depth: micro
evidence_class: semi-durable
review_interval_months: 6
curator: Maher
license: ML-2.3
designated: yes
last_reviewed: 2026-09-16
domain_tags: [privacy, data, collection, refusals, sessions]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000 and not reviewed by counsel.
counsel_reviewed: no
provenance_of_purpose: Required since inception; absent until v2026.10.1. The site operated with no published privacy notice.
route: /privacy/
---

# MX-003 — Privacy Notice

> **Authority.** `governing`, tier 3. Subordinate to
> [ML-2.3](../license/the-maher-license.md),
> [HX-000](../harms/hx-000-the-fourteen-structural-harms.md) (tier 1a) and the
> [Charter](mx-000-charter.md). The refusals that make this notice short are set by
> [MX-023](mx-023-attention-and-human-sovereignty.md) and
> [MX-022](mx-022-identity-and-sessions.md).

> **The short version.** The estate collects **no personal data**, has **no
> accounts**, sets **no cookies**, runs **no analytics**, and holds **no dataset
> about any reader** ([REG-06](../registries/reg-06-dataset-registry.md)).
>
> **The honest qualification.** The estate has **not audited what its hosting
> layer logs by default**, and hosting layers log by default. Until that audit is
> done, the paragraph above describes the estate's *conduct*, not verified
> *system behaviour*. See [§7](#7-the-unaudited-layer) — it is the most important
> section on this page.

---

## 1. Position

Most privacy notices are long because they enumerate collection. This one is
short because there is little to enumerate, and it is **not** short because the
estate has declined to look.

Two sections carry the real content:

- **§5** — what the estate refuses to collect, and what those refusals cost it.
- **§7** — the one place the estate cannot currently vouch for its own claim.

A reader in a hurry should read §7 and ignore the rest, because §7 is where this
notice is weakest and therefore where a reader's own scepticism is most useful.

## 2. Definitions

| Term | Meaning | Source |
|---|---|---|
| **personal data** | Any record joinable to a person **by any party holding it** | [REG-06 §2.2](../registries/reg-06-dataset-registry.md) |
| **session** | One visit. Not an identity, not linked across visits | [MX-022](mx-022-identity-and-sessions.md) |
| **engagement metric** | Any per-reader measure of attention | [MX-023](mx-023-attention-and-human-sovereignty.md) |
| **collection** | Retention of a record, whether or not it is used | §3.2 |

### 2.1 The joinability test

The estate does **not** accept that data is non-personal because it does not
personally intend to identify anyone. If a record *could* be joined to a person by
anyone holding it, it is personal data. Under that test **IP addresses, request
timestamps, and user-agent strings are personal data**, and their presence in a
server log is collection.

This is stricter than many regimes require, and it is the reason §7 exists: under
a looser test the estate could claim a clean posture without auditing anything.

## 3. What the estate collects

### 3.1 By intention: nothing

| Category | Collected? |
|---|---|
| Name, email, or contact details | **No** — no forms exist |
| Account credentials | **No** — no accounts exist |
| Cookies or local storage | **No** |
| Analytics identifiers | **No** |
| Page views per reader | **No** |
| Time on page, scroll depth | **No** — forbidden fields |
| Referrer or campaign tokens | **No** — forbidden by [ST-23](../standards/st-23-affiliate-and-referral.md) |
| Inferred interests or segments | **No** — hard exclusion, [MX-014](mx-014-research-ethics-and-exclusions.md) |
| Payment data | **No** — no payment path is active ([MX-021](mx-021-payments-and-commerce.md)) |
| Location | **No** |

### 3.2 Collection is the event, not analysis

The estate treats **retention** as the collection event. A field the estate never
queries is still collected if it is stored. This follows the reasoning of
[HX stratum I](../harms/hx-000-the-fourteen-structural-harms.md): the availability
of a record changes what may be done with it later, by parties the reader never
dealt with. "We don't look at it" is not a privacy property.

### 3.3 Third parties

| Third party | Role | Data it may see |
|---|---|---|
| Hosting provider | Serves the static files | Whatever the transport reveals — see §7 |
| Web font provider | `FNT-001`, [REG-04](../registries/reg-04-media-registry.md) | **Potentially the reader's request** if served remotely |
| CDN | Asset delivery | Same class as hosting |
| Analytics vendor | **none** | — |
| Advertising network | **none** — forbidden, [MX-009](mx-009-advertising-and-commercial.md) | — |
| Affiliate network | **none** — forbidden, [ST-23](../standards/st-23-affiliate-and-referral.md) | — |

The font row is a real exposure and is named rather than buried. A remotely
served font means a reader's browser contacts a third party the reader did not
choose. The estate's own [REG-04 §5.1](../registries/reg-04-media-registry.md)
already records that the font's licence terms are unarchived; whether it is
self-hosted is a **separate** and currently unverified question. Both belong on
the same defect.

## 4. What the estate does with what it does not have

Nothing. There is no profiling, no personalisation, no recommendation, no A/B
testing, no email, and no retargeting — not because they are unimplemented but
because each is refused:

| Practice | Refused by |
|---|---|
| Personalisation of content | [MX-023 §2](mx-023-attention-and-human-sovereignty.md) — refusal 2 |
| Engagement optimisation | [MX-023 §2](mx-023-attention-and-human-sovereignty.md) |
| A/B testing on readers | [MX-014](mx-014-research-ethics-and-exclusions.md) — human-subjects exclusion |
| Email capture | No form; no legitimate prior question ([REG-06 §3.1](../registries/reg-06-dataset-registry.md)) |
| Progress tracking, streaks, badges | [MX-023](mx-023-attention-and-human-sovereignty.md); [REG-05 §5.2](../registries/reg-05-credential-registry.md) |

## 5. What the refusals cost

A refusal presented as free is a marketing claim. These are not free.

| Refusal | What the estate gives up |
|---|---|
| No analytics | Cannot say whether **any** page is read, or whether the 1200-word floor helps or harms. The question is legitimate and is refused at gate 3 ([REG-06 §4](../registries/reg-06-dataset-registry.md)) |
| No per-reader tracking across a notice | **Cannot test the central premise of its own licence** — that harm disclosure changes behaviour. That premise stays **E0** ([REG-06 §5.1](../registries/reg-06-dataset-registry.md)) |
| No accounts | Cannot offer private credential verification; verification must be public or not exist ([REG-05 §3.2](../registries/reg-05-credential-registry.md)) |
| No email | Cannot notify a reader of a correction to a document they relied on. The [changelog](../00-governance-map/changelog.md) is pull-only |
| No error telemetry | Client-side faults are invisible to the estate; a reader must report them |

The fourth is the one that most clearly harms readers rather than the estate. A
reader who relies on a document that is later corrected has **no way to be told**.
The estate's substitute is publication and version stamps, which requires the
reader to come back and check. That is a weaker protection than a notification,
and the estate has chosen the weaker one to avoid holding an address list.

A reader who thinks that trade is wrong has identified a genuine objection. It is
filed as `open` under [ST-06](../standards/st-06-objections-standard.md), not
rebutted.

## 6. Reader rights

Because the estate holds no personal data, the usual rights have unusual answers:

| Right | Answer |
|---|---|
| Access — *what do you hold about me?* | **Nothing**, subject to §7 |
| Rectification | Nothing to rectify |
| Erasure | Nothing to erase. **If §7's audit finds hosting logs, this answer changes** |
| Portability | Nothing to port |
| Objection to processing | No processing occurs |
| Withdraw consent | No consent was requested, because no basis was needed |

This table is only as true as §7. The estate states it plainly rather than
hedging every row, and places the hedge where it belongs — in its own section,
under its own heading, at the same prominence.

## 7. The unaudited layer

> **This is the section that matters.**

The estate asserts it collects nothing. That assertion covers **the estate's own
code and configuration**, which is small, static, and contains no collection.

It does **not** cover:

1. **Default hosting logs.** Static hosts commonly retain request logs containing
   IP address, timestamp, path, user-agent, and referrer. Under §2.1 every one of
   those is personal data. **The estate has not inspected its hosting
   configuration**, so it does not know whether such logs exist, what they retain,
   or for how long.
2. **CDN edge logs**, same class.
3. **Remote font or asset requests**, which would disclose a reader's request to a
   third party. See §3.3.

### 7.1 Status of the audit

| Item | State |
|---|---|
| Hosting default logging inspected | **No** |
| Retention period known | **No** |
| CDN logging inspected | **No** |
| Fonts confirmed self-hosted | **No** |
| Filed as | [REG-06 §7.1](../registries/reg-06-dataset-registry.md) limit; verification item [V-14+](../00-governance-map/verification-log.md) |

### 7.2 What the estate says in the meantime

It does not say "we collect nothing." It says:

> **The estate collects nothing by design and has not verified what its
> infrastructure collects by default. A reader should assume that ordinary web
> server logs may exist until the estate publishes the audit.**

That sentence is less attractive and is the only one the evidence supports. Under
[ST-07](../standards/st-07-evidence-and-verify.md) the unqualified claim would be
**E0 presented as E3** — an overclaim, class DC-3 in
[REG-07](../registries/reg-07-defect-classification-registry.md).

## 8. Worked instance

**A reader asks: "Do you know I was here?"**

| Layer | Answer | Confidence |
|---|---|---|
| Estate's own records | No. There is no database row, no file, no counter | **High** — the estate authored every file and there is no collection code |
| Estate's own analytics | No. None is installed | **High** — verifiable by viewing page source |
| Cookies / storage | No. None is set | **High** — verifiable by the reader in their own browser, in seconds |
| Hosting request log | **Unknown** | **None** — not inspected |
| CDN edge log | **Unknown** | **None** |
| Third-party font request | **Unknown** | **None** |

The useful feature of this table is that the reader can verify the three
high-confidence rows **themselves, immediately**, using their browser's developer
tools — no trust in the estate required. The three unknown rows cannot be verified
by the reader and are the estate's to answer.

That asymmetry is the correct shape for a privacy notice: the claims a reader can
check are stated crisply, and the claims only the operator can check are marked
unverified rather than asserted with borrowed confidence from the checkable ones.

## 9. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Clean-posture overclaim** — asserting zero collection without the audit | **Prevented** by §7, at the cost of a weaker headline |
| F2 | **Silent default collection** — host logging enabled and unknown | **Live and unquantified** |
| F3 | **Third-party asset leakage** — fonts or CDN disclosing requests | **Live**; `FNT-001` unverified |
| F4 | **Refusal erosion** — analytics added "temporarily" to answer a good question | Guarded by [REG-06](../registries/reg-06-dataset-registry.md)'s refused rows, which make reopening visible |
| F5 | **Rights table invalidated** — §6 becomes false if §7 finds logs | **Conditional**; §6 is explicitly subject to §7 |
| F6 | **Prevailing text absent** — Arabic governs, does not exist | **Systemic** |

## 10. Falsifier

> **IF FALSE.** This notice is falsified if:
>
> - **(a)** any cookie, local storage entry, or persistent identifier is set by the
>   service — **checkable by any reader in under a minute**;
> - **(b)** any analytics or tracking script is present in a served page —
>   checkable by viewing source;
> - **(c)** any retained record about a reader exists in estate-controlled storage;
> - **(d)** the hosting or CDN layer is shown to retain request logs — which would
>   **not** falsify §7 (which predicts this) but **would** falsify §6's rights
>   table;
> - **(e)** any request is made to a third-party domain the reader did not choose.
>
> (a), (b) and (e) are all checkable by the reader with developer tools open. The
> estate invites all three and has performed none of them as a recorded
> verification — which is itself the point of
> [GM-08](../00-governance-map/verification-log.md), where four checkable items sit
> unclosed.

## 11. Limits

1. **§7 is the whole limit.** The estate's privacy posture is a design commitment
   with an unverified infrastructure layer beneath it.
2. **No counsel review.** Whether this notice satisfies any legal regime is
   unknown. It was written to be *true*, not to be *compliant*, and the two are not
   the same document.
3. **No named data protection contact**, because there is one participant
   ([DEF-031](../00-governance-map/defect-register.md)). A rights request would be
   received and answered by the same person, with no independent review —
   [MX-016](mx-016-appeals-and-due-process.md) stage 2 is vacant.
4. **No Arabic text**, while `prevailing_text: ar`
   ([MX-020](mx-020-language-authority.md)).
5. **6-month review interval** is set deliberately short (`semi-durable`) because
   §7 is expected to change. If the audit is done, this notice must be re-issued
   immediately, not at the interval.

## 12. Obligation

**On the estate:**
- Perform the hosting and CDN audit and publish the result. This is the single
  outstanding act that would let §§3 and 6 be stated without qualification.
- Confirm fonts and assets are self-hosted, or disclose the third party at the
  point of use.
- Never add analytics or per-reader measurement, including to answer a good
  question ([REG-06 §4](../registries/reg-06-dataset-registry.md)).
- Keep collection = retention, not use (§3.2).
- Re-issue this notice on audit completion rather than waiting for the interval.
- Where a reader cannot be notified of a correction, say so rather than implying
  the changelog reaches them (§5).

**On a reader:**
- Verify (a), (b) and (e) in §10 yourself. This notice is more useful as an
  invitation to check than as a promise to believe.

---

### Related

**Refusals that shape this notice** — [MX-023](mx-023-attention-and-human-sovereignty.md) ·
[MX-022](mx-022-identity-and-sessions.md) ·
[MX-014](mx-014-research-ethics-and-exclusions.md) ·
[ST-23](../standards/st-23-affiliate-and-referral.md)

**Data holdings and storage** — [REG-06](../registries/reg-06-dataset-registry.md) ·
[ST-22](../standards/st-22-platform-and-persistence.md) ·
[MX-024](mx-024-infrastructure-and-migration.md) ·
[REG-04](../registries/reg-04-media-registry.md)

**User-facing companions** — [MX-002 terms](mx-002-terms-of-service.md) ·
[SITE-04 demo notice](../site/demo-notice.md) ·
[MX-016 appeals](mx-016-appeals-and-due-process.md) ·
[MX-012](mx-012-licensing-and-reuse.md)

**Where the gap is recorded** — [defect register](../00-governance-map/defect-register.md) ·
[GM-08 verification log](../00-governance-map/verification-log.md) ·
[REG-07](../registries/reg-07-defect-classification-registry.md) ·
[ST-07](../standards/st-07-evidence-and-verify.md)

### Exit pair

1. **Check it yourself.** Open developer tools, reload this page, and look at
   storage and network requests. Falsifier §10(a),(b),(e) are yours to run.
2. **Read the refusal that costs readers most.** [§5](#5-what-the-refusals-cost) —
   the estate cannot tell you when a document you relied on was corrected.

<!-- mx-pagestamp: MX-003 · v2026.10.1 · governing · tier 3 · reviewed 2026-09-16 · next review 2027-03-16 -->
<!-- mx-demo: the live site is a demonstration; the infrastructure layer described in §7 is unaudited -->
