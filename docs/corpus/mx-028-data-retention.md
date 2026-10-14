---
doc_id: "MX-028"
title_en: "Data Retention Schedule"
title_ar: "جدول الاحتفاظ بالبيانات"
family: "corpus"
version: "v2026.10.2"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 2
depth: 4
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-25"
domain_tags: ["corpus", "privacy", "retention", "records", "deletion"]
route: "/about/legal/retention/"
derived_from: "THE METAX CORPUS v2026.09.0 Part II MX-018; ST-22 persistence tiers"
supersedes: ["Index allocation MX-018 'Data Retention Schedule' (refuge number; see GM-13)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "specification"
authorship_note: "Drafted by an AI system under AG-000. Periods restate the source; statutory periods vary and are unreviewed by counsel."
counsel_reviewed: false
hreflang: "en, ar"
---

# MX-028 · Data Retention Schedule

> **Authority.** `governing`, tier 3. Collection is [MX-003](mx-003-privacy-notice.md); storage
> tiers are [ST-22](../standards/st-22-platform-and-persistence.md); holdings are recorded at
> [REG-06](../registries/reg-06-dataset-registry.md). [ST-19 I-4](../standards/st-19-two-plane-architecture.md)
> cites "MX-018" for retention — that text is here.

> **Disclosure first.** **The estate holds almost none of the data this schedule governs**: no
> accounts, no submissions, no applications exist ([REG-06](../registries/reg-06-dataset-registry.md)).
> The schedule is written before the data, which is the only time it can be written without an
> interest in keeping more.

---

## 1. Position

Retention is where privacy promises are actually kept or broken. A notice saying "we collect
little" is meaningless if what is collected is kept forever. Each period below is justified by
**the purpose that ends it** — when the purpose ends, the data goes.

## 2. The schedule

| Record | Period | Purpose that ends it |
|---|---|---|
| Edge server logs | **30 days** | Security and aggregate traffic |
| Account records | Life of account + **12 months** | Dispute window after closure |
| Credential submissions and evidence | **7 years** | Period in which validity may be challenged |
| ON REQUEST evidence | **24 months** after decision, then deleted | Appeal window, then none |
| Credential registry entries | **Permanent** | Records of fact |
| Academy applications — unsuccessful | **3 years** | Re-application context |
| Academy applications — successful | Life of academy + **7 years** | Audit trail |
| Audit reports | **Permanent** | Institutional record |
| Appeals correspondence | **7 years** | Matches submission period |
| Payment records | Statutory tax period `[VERIFY]` V-15 — varies by jurisdiction | Tax law |
| General correspondence | **3 years** | Follow-up |
| Published specimens | Until consent withdrawn | Consent |

## 3. Mechanism

- Deletion is **scheduled at write time**: every record carries its expiry date when stored
  ([ST-22](../standards/st-22-platform-and-persistence.md)).
- Deletion is logged by **count**, not content.
- **Erasure requests** override the schedule except for permanent records of fact (registry
  entries, audit findings), which is disclosed in [MX-003](mx-003-privacy-notice.md).

## 4. Worked instance

A candidate is rejected in 2027 and never resubmits. Their dossier deletes in 2034; their ON
REQUEST evidence in 2029; the registry holds **nothing** about them, because rejections are
counted, not listed.

## 5. Failure modes

Backups that outlive the schedule; "anonymised" copies that are re-identifiable; analytics
exports never scheduled.

## 6. Limits

A schedule cannot bind processors the estate does not audit ([MX-018](mx-018-third-party-dependencies.md) D1, D2).

## 7. Falsifier

Wrong if any record type the estate holds is absent from §2, or any held record is found past its
period.

## 8. Obligation

Counsel review of statutory periods per jurisdiction before the identity plane opens.

## 9. Macro register

Data kept indefinitely becomes an asset, and assets are sold. **Deleting on schedule is the only
reliable way to make sure a future owner cannot monetise a past promise.**

---

**Related:** [MX-003](mx-003-privacy-notice.md) · [ST-22](../standards/st-22-platform-and-persistence.md) ·
[REG-06](../registries/reg-06-dataset-registry.md) · [MX-022](mx-022-identity-and-sessions.md) ·
[MX-025](mx-025-credentialing-and-assessment.md) · [MX-011](mx-011-security-and-disclosure.md) ·
[ST-19](../standards/st-19-two-plane-architecture.md) · [MX-013](mx-013-records-and-versioning.md)
