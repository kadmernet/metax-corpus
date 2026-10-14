---
doc_id: "RB-06"
title_en: "Structural Review and Build Gates"
title_ar: "المراجعة البنيوية وبوابات البناء"
family: "rubrics"
version: "v2026.10.2"
status: "canonical"
authority: "operative-form"
prevailing_text: "en"
audience_tier: 4
depth: 4
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-25"
domain_tags: ["rubrics", "structural-review", "build-gates", "three-pass"]
derived_from: "THE METAX CORPUS MX-006 §§6.3, 6.4, 6.8; AG-002 SENTINEL; ST-13"
supersedes: ["Index allocation RB-03 'Structural Review and Build Gates' (refuge number; see GM-13)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "specification"
authorship_note: "Drafted by an AI system under AG-000. Gates G1–G4 are mechanical and unimplemented; G5–G7 need people who do not exist."
hreflang: "en, ar"
---

# RB-06 · Structural Review and Build Gates

> **Authority.** `operative-form`, tier 5. It enforces [MX-026](../corpus/mx-026-editorial-and-evidence.md)
> §§4, 5 and 9 through [ST-13](../standards/st-13-static-build-and-sentinel.md). The harm gate is
> [RB-05](rb-05-harm-review-gate.md); instrument quality is scored by [RB-03](rb-03-instrument-quality-rubric.md).

> **Disclosure first.** Nothing has passed or failed this review. The build does not run it, and
> no series exists to review.

---

## 1. Position

A structural review checks that an artefact has the **parts** that make it checkable. It does not
judge whether the content is true. The two questions are kept apart on purpose: a reviewer who
asks both at once tends to let good prose excuse a missing falsifier.

## 2. The seven gates, in order

| # | Gate | Type | Fails when |
|---|---|---|---|
| G1 | Front matter complete (ST-02) | Mechanical | Any required field is missing |
| G2 | Every claim card has a falsifier | Mechanical | A card has no `IF FALSE` field |
| G3 | The series has Limits (four classes) **immediately before** the Bridge | Mechanical | Either is missing, or they are in the wrong order |
| G4 | No typed counts and no unresolved placeholders | Mechanical | A number has no source, or a `[…]` bracket is rendered |
| G5 | **Language pass** | Human | Voice or style breaches ([ST-27](../standards/st-27-style-guide-en.md)) |
| G6 | **Science pass** | Human subject reviewer | An unsupported claim, or a banned comparison |
| G7 | **Ethics pass** | Human with veto | An exclusion is breached, or a harm is unassessed |

**The passes are never merged.** A reviewer who does G5 and G7 in one reading has done neither.

## 3. Outcomes

- `PASS`: all seven gates pass.
- `RETURNED`: any gate fails, with reasons given per gate.
- `BLOCKED`: G7 veto. There is no appeal to the Curator.

## 4. Worked instance (hypothetical)

*Hypothetical.* An S15 draft passes G1, G2 and G4. It fails G3 because the Limits module comes
after the Bridge lesson. The outcome is `RETURNED` with one reason. G5–G7 are not run, because a
structural failure is cheaper to fix before human review time is spent.

## 5. Failure modes

- Human gates done by the drafting agent.
- G3 checking only that a Limits module exists, not that it covers all four classes.
- `PASS` recorded when G6 and G7 were skipped because no reviewer was available.

## 6. Limits

A `PASS` means the parts are present and have been read by the right people. It does not mean the
content is correct.

## 7. Falsifier

This rubric is wrong if an artefact that passes all seven gates is later found to breach MX-026 in
a way that one of the gates names.

## 8. Obligation

Build G1–G4 into SENTINEL before G5–G7 are staffed. The mechanical gates are cheap and do not
need a second person.

## 9. Macro register

When review merges language, science and ethics, the result is polished text whose ethics were
checked for typos. **Ordering the passes is the cheapest structural protection an editorial
institution can buy.**

---

**Related:** [MX-026](../corpus/mx-026-editorial-and-evidence.md) · [ST-13](../standards/st-13-static-build-and-sentinel.md) ·
[ST-03](../standards/st-03-limits-and-bridge.md) · [ST-04](../standards/st-04-falsifiability-and-claim-cards.md) ·
[RB-05](rb-05-harm-review-gate.md) · [RB-03](rb-03-instrument-quality-rubric.md) ·
[ST-25](../standards/st-25-cognitive-arc.md) · [AG-019](../agents/ag-019-human-in-the-loop-gates.md)
