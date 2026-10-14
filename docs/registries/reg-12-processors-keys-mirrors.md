---
doc_id: "REG-12"
title_en: "Processors, Keys and Mirrors Registry"
title_ar: "سجل المعالِجين والمفاتيح والمرايا"
family: "registries"
version: "v2026.10.2"
status: "canonical"
authority: "record"
prevailing_text: "en"
audience_tier: 3
depth: 2
evidence_class: "volatile"
review_interval_months: 3
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-25"
domain_tags: ["registries", "processors", "keys", "mirrors", "privacy", "continuity"]
route: "/license/machinery/processors/"
derived_from: "MX-028 Data Retention; ML-OPS-1 Registry and Mirrors; ST-29 Security Architecture"
supersedes: ["Index allocation REG-08 'Processors, Keys and Mirrors' (refuge number; see GM-13)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "record"
authorship_note: "Compiled by an AI system under AG-000. Processor facts are from the corpus's own statements. Jurisdictions and contract terms are unverified."
hreflang: "en, ar"
---

# REG-12 · Processors, Keys and Mirrors Registry

> **Authority.** A **record**. It lists every third party that touches visitor data, every signing
> key, and every mirror. What it records is governed by [MX-028](../corpus/mx-028-data-retention.md),
> [ML-OPS-1](../license/registry-and-mirrors.md) and [ST-29](../standards/st-29-security-architecture.md).
> Earlier drafts called this register "REG-08"; that number now belongs to Role and Authority ([GM-13](../00-governance-map/identifier-reallocation-record.md)).

> **Disclosure first.** Two of the listed processors are **non-compliant** with the corpus's own
> advertising and privacy rules (R-58b). **No signing key exists. No mirror exists.** Every
> jurisdiction below is marked **[VERIFY]**.

---

## 1. Processors

| P-id | Processor | Function | Data touched | Jurisdiction | State | Compliance |
|---|---|---|---|---|---|---|
| P-01 | Cloudflare Pages | Static hosting, CDN | IP address, request logs | [VERIFY] | active | Acceptable. Retention of logs [VERIFY] against MX-028 |
| P-02 | Google AdSense | Advertising | Cookies, device identifiers, behavioural profile | [VERIFY] | active per SITE sources | **Non-compliant.** Conflicts with MX-009 and MX-029 §6 (R-58b) |
| P-03 | Adsterra | Advertising | Cookies, device identifiers, redirects | [VERIFY] | active per SITE sources | **Non-compliant.** Same conflict. Redirect behaviour is also a security concern (ST-29 E3) |
| P-04 | FNT-001 (payment/fintech processor named in sources) | Payments | Payer identity, amounts | [VERIFY] | declared, not verified live | Pending: needs a DPA and a retention statement |
| P-05 | Binance Pay | Crypto payments | Wallet identifiers, amounts | [VERIFY] | proposed | **Blocked by RAT-13** (Curator ruling on crypto acceptance) |
| P-06… | Analytics, email, form handlers | — | — | — | **inactive / none** | None may be added without a row here first |

**Rule.** A processor that is live on the site but has no row here counts as a defect in class S1
([REG-07](reg-07-defect-classification-registry.md)).

## 2. Signing keys

| K-id | Purpose | Algorithm | Fingerprint | Holder | Created | Rotates | Revocation URL |
|---|---|---|---|---|---|---|---|
| *(none)* | Registry and credential signing (ST-30) | — | — | — | — | — | — |

Until K-01 exists, [ST-30](../standards/st-30-registry-and-verifier.md) verification cannot be
performed, and every credential claim remains **unverifiable** (V-17).

## 3. Mirrors

| M-id | Role | Host | Operator | Sync cadence | Last verified | State |
|---|---|---|---|---|---|---|
| M1 | Primary text mirror (ML-OPS-1 §2) | — | — | — | — | **empty** |
| M2 | Independent-operator mirror | — | — | — | — | **empty** |
| M3 | Cold archive (e.g., a deposit library) | — | — | — | — | **empty** |

ML-OPS-1 requires at least two mirrors before the scale gate ([scale-gate](../license/scale-gate.md)) can open.
**The gate is therefore closed on this ground alone.**

## 4. Rules

- Rows are appended and never deleted. A retired processor, key or mirror keeps its row, marked `retired` with a date.
- A key compromise is logged here within 24 hours, and the revocation is published before any replacement key.
- Changes are made only under the Curator's authority ([AG-018](../agents/ag-018-change-control.md)).

## 5. Falsifier

This register is wrong if any script, pixel, payment endpoint, key or mirror serving MetaX content is
missing from it, or if any row claims a state that a fetch of the live site contradicts.

---

**Related:** [MX-028](../corpus/mx-028-data-retention.md) · [ML-OPS-1](../license/registry-and-mirrors.md) ·
[ML-OPS-2](../license/steward-succession.md) · [ST-29](../standards/st-29-security-architecture.md) ·
[ST-30](../standards/st-30-registry-and-verifier.md) · [REG-11](reg-11-determinations-registry.md) ·
[Scale gate](../license/scale-gate.md) · [GM-13](../00-governance-map/identifier-reallocation-record.md) ·
[Open questions](../00-governance-map/open-questions-and-ratifications.md)
