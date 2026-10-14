---
doc_id: "GM-19"
title_en: "Continuity Register: Every Dependency on the Curator, as a Dated Defect"
title_ar: "سجل الاستمرارية [AR-DRAFT]"
family: "governance-map"
version: "v2026.10.3"
status: "draft"
authority: "record"
prevailing_text: "en"
audience_tier: 3
depth: 4
evidence_class: "perishable"
review_interval_months: 3
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-08"
domain_tags: ["governance", "continuity", "succession", "HX-28", "HX-23", "single-steward"]
route: "/about/continuity-register/"
human_read: "none"
conformance_state: "unmet"
derived_from: "MX-015; ML-OPS-2 / steward-succession.md; HX-000 v2027.1 §13 (HX-28); ML-2.4 §H.33; launch-blockers; GM-17 §2.1; Meta-Review route /about/continuity-register/"
authorship_note: "Compiled by an AI system under AG-000 to close GM-17 M-23. Each row is a fact already recorded elsewhere in the corpus. The register only gathers them so that the total is visible."
hreflang: "en, ar"
---

# GM-19 · Continuity Register

> **Authority.** A **record**. It lists every point at which the estate stops working, or stops being
> honest, if **one person** (the Curator, Maher) becomes unavailable. Each row is a defect with a
> date opened, and none is closed by being listed. This is the estate's own instance of **HX-28
> (steward dependence)** and **HX-23 (custody beyond the horizon)**.

> **Disclosure first.** Listing these dependencies does not remedy them. Under the source harm
> "disclosure as licence" (UH-02), an institution **may not cite this register as evidence of its
> integrity**. It shows how much rests on one person. It does not show that the estate is careful.

---

## 1. The test

For each row the question is: *if Maher were unavailable tomorrow, for good, what happens to this,
and who would know?* The answers are:
- `stops`: nothing further happens.
- `drifts`: things continue, unaccountably.
- `false`: a published claim becomes untrue.
- `held`: a successor mechanism exists.

## 2. Register

| CR | Dependency | Recorded at | If unavailable | Remedy (what closes it) | Opened | Remedy within the Curator's sole control? |
|---|---|---|---|---|---|---|
| CR-01 | **The only signer.** No key exists, so no successor can sign either | B-01, REG-12 §2, M-01 | `stops`: no instrument can ever be signed | Generate a key, publish the fingerprint, and lodge an escrowed recovery with the successor | 2026-08-30 | **yes** |
| CR-02 | **The only steward of ML-2.x, HX-000 and BX-018** | ML-2.3 §E.8; HX-28 | `drifts`: the instruments persist with no one able to amend them, admit a harm or answer a determination | Executed succession instrument with written acceptance (ML-2.4 §H.33(a)) | 2026-09-02 | no (needs a successor) |
| CR-03 | **The succession instrument is a form, not an act** | MX-015; steward-succession.md; AG-022; M-04 | `stops` | Name, trigger, acceptance, publication | 2026-09-02 | no |
| CR-04 | **The only prompter** of every agent | AG-013; AG-022 degraded mode | `stops` for generation (safe). `drifts` if a third party re-uses the kernel | Name a second prompter or declare agent work suspended on unavailability (AG-022) | 2026-09-25 | yes (declaration) |
| CR-05 | **The ethics veto is unheld**, so nobody but the Curator ever decides a bio-adjacent question | MX-000 §0.5.1; RAT-04; M-03 | `stops`: BCIA beyond status, audit and charter stays frozen. **That is the safe failure** | Name the holder | 2026-08-28 | no |
| CR-06 | **The only receiver of objections and comments** | DEF-053; CPF-1 §2 | `stops`: objections go nowhere, silently | An independent dissent receiver | 2026-09-30 | no |
| CR-07 | **The only person who can write the Arabic prevailing text** | MX-020; RAT-09; X-35 | `false`: files with `prevailing_text: ar` name a text that will never exist | Commission a translator, or set `prevailing_text: en` (X-35) | 2026-08-28 | yes (the setting) |
| CR-08 | **The only holder of the domain, hosting and processor accounts** | REG-12 | `stops` at the next renewal. The ad processors keep running until then | Documented custody of the accounts with the successor; a D1-style static export | 2026-09-02 | yes |
| CR-09 | **The only assessor and credential issuer** | MX-025; REG-05 | `false`: issued credentials cannot be verified once `verify.` lapses | Static, signed, self-verifying credential artefacts (MLT-06 position; ST-30) | 2026-09-02 | partly |
| CR-10 | **The only author with `human_read` standing.** Every instrument at `none` stays non-governing for ever | ST-02 v2027.1 fields; HX-17 (Family B "governance volume"); UH-03 | `false`: the corpus is permanently drafts calling themselves canonical | Read and record. A second reader | 2026-09-30 | yes |
| CR-11 | **The only source of Book 9 ch. 2–9** | BX-012; RAT-05; M-29 | `stops`: Gate 1 is unclosable for ever | Supply the text, or declare it lost | 2026-08-14 | yes |
| CR-12 | **The only maker of every pending ruling** (RAT-01…38, RAT-B-01…06) | GM-04 | `drifts`: refuge numbers become permanent by default (GM-13 §6) | Rulings, or a published default-on-lapse rule | 2026-08-28 | yes |
| CR-13 | **No wind-down cost is published** | Family B DT-4; HX-23 | `false`: commitments to learners have no stated horizon | Publish a horizon and the cost of an orderly cessation | 2026-09-30 | yes |
| CR-14 | **The premise register can only be founded by the Curator** | Bundle closing note; RAT-36; M-10 | `stops`: UH-10 stays unremedied | Write the first seven premises | 2026-09-30 | yes |

**Counts (computed from §2):** 14 rows · 7 `stops` (CR-01, 03, 05, 06, 08, 11, 14), 2 `drifts` (CR-02, 12), 4 `false` (CR-07, 09, 10, 13), 1 mixed (CR-04) · **9
remedies within the Curator's sole control** (CR-01, 04, 07, 08, 10, 11, 12, 13, 14) · **0 `held`**.

## 3. Age and survival (the UH-02 test)

The Family B harm "disclosure as licence" asks that every open item carry its age and the number of
review intervals it has survived. At a 3-month interval, measured to 2026-10-08:

| Opened | Rows | Age (days) | Intervals survived |
|---|---|---|---|
| 2026-08-14 | CR-11 | 55 | 0 |
| 2026-08-28 | CR-05, 07, 12 | 41 | 0 |
| 2026-08-30 | CR-01 | 39 | 0 |
| 2026-09-02 | CR-02, 03, 08, 09 | 36 | 0 |
| 2026-09-25 | CR-04 | 13 | 0 |
| 2026-09-30 | CR-06, 10, 13, 14 | 8 | 0 |

No row has yet survived an interval. **The first will do so on 2026-11-14 (CR-11).** Under the source's
rule, any item with a remedy in sole control that survives two intervals should be escalated to a
blocking condition or closed. That applies to CR-11 from **2027-02-14** and to CR-01 from **2027-02-28**.

## 4. Obligation

- **Curator:** close the nine sole-control rows, or state for each why it stays open.
- **Agents:** recompute §3 at every review. Never describe the estate as "resilient" while §2 has no `held` row.

## 5. Falsifier

This register is incomplete if there is any function of the estate that stops or becomes false on the
Curator's unavailability and is not a row here.

---

**Related:** [MX-015](../corpus/mx-015-succession-and-continuity.md) · [Steward succession](../license/steward-succession.md) · [HX-000 v2027.1 §13](../harms/hx-000-register-v2027-1.md) ·
[Launch Blockers](launch-blockers.md) · [Decision Record Register](../license/decision-record-register.md) · [GM-17](corpus-review-v2027.1.md)
