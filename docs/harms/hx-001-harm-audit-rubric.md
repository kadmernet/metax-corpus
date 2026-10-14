---
doc_id: "HX-001"
title_en: "Harm Audit Rubric"
title_ar: "معيار تدقيق الأضرار"
family: "harms"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 5
depth: 5
evidence_class: "semi-durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["harms", "audit", "rubric", "measurement"]
route: "/license/harms/falsifiers/"
incorporated_by: "ML-2.3 §H.7 and §H.16"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# HX-001 · Harm Audit Rubric

**What this instrument is.** The scored procedure by which a deployment is assessed against
[HX-000](.), producing the dispositions that a [Part H Statement](../license/part-h-statement.md)
records. It carries the **counterproductivity test** required by
[ML-2.3 §H.7](../license/ml-2-3.md).

**What it is not.** It is not a certification, and it issues no pass. It produces a **disposition
per harm** and a record of what was examined — nothing more, because a rubric that concluded
"compliant" would be an instrument of the harm its own Stratum V names.

---

## 1. Position

The register states what the harms are. The Statement records what a deployer concluded. This
rubric is the procedure **between** them, and without it the Statement is an opinion with a
signature.

That gap is not hypothetical. A twenty-five-harm register invites exactly one failure mode: a
deployer reads the harm titles, forms an impression, and writes twenty-five plausible sentences.
The result satisfies §H.16's form and carries no information, because nothing was examined. This
rubric exists to make the difference between an examined and an unexamined disposition **visible
in the artefact** — which is why §5 requires the *method* to be recorded alongside the conclusion.

Its parent is [ML-2.3 §H.7](../license/ml-2-3.md); its published route is
`/license/harms/falsifiers/`; its consumers are deployers completing a Statement,
[RB-05](../rubrics/rb-05-harm-review-gate.md) reviewers, and any reader auditing a published
Statement against the procedure that should have produced it.

---

## 2. Definition — the five dimensions

Every harm is assessed on five dimensions. Each scores **0–3**. The dimensions are deliberately
not weighted into a single number; §4 explains why that refusal is the rubric's most important
design decision.

| Dim | Name | Asks |
|---|---|---|
| **A** | **Instantiation** | Is the harm's mechanism present in this system, specifically? |
| **B** | **Exposure** | How many are affected, and could they decline? |
| **C** | **Measurement** | Is the mechanism instrumented, or is the assessment an impression? |
| **D** | **Remedy** | What has been done, and does it address the mechanism or its symptom? |
| **E** | **Reversibility** | Can the deployment be withdrawn, and what would be lost? |

### 2.1 The scales, stated so a score can be wrong

**A — Instantiation.**
`0` mechanism structurally absent · `1` present only in a path few reach · `2` present in a normal
path · `3` present in the primary path, or constitutive of how the system works.

*A=0 is the only score permitting a `not engaged` disposition*, and it means **structurally
absent** — not small, not managed, not unintended. A system with an engagement metric cannot score
A=0 on HX‑01 whatever its intentions.

**B — Exposure.**
`0` no third-party users · `1` users who can decline at trivial cost · `2` users for whom
declining is costly · `3` users who cannot practically decline, or users in a formative capacity.

B tracks the Scale Gate's unavoidability test
([ML-S2 §3.3](../license/scale-gate.md)) rather than headcount, on the same reasoning: **consent
is the variable scale destroys.**

**C — Measurement.**
`0` not measured and not measurable · `1` not measured though measurable · `2` measured
indirectly · `3` measured directly, with the series retained.

**C=1 is the most informative score in the rubric** and the most uncomfortable to write. It says:
*this could be examined and we chose not to.* A deployer who scores C=1 across a stratum has
disclosed something no prose disposition would have revealed.

**D — Remedy.**
`0` none · `1` disclosure only · `2` addresses the symptom · `3` addresses the mechanism.

**Disclosure alone is D=1, never higher.** Telling a reader that a system extracts their attention
does not stop it extracting their attention. Disclosure is a floor, and the rubric refuses to let
it read as a remedy — the same position [SITE-04 §7](../site/demo-notice.md) takes about the
estate's own demo strip.

**E — Reversibility.**
`0` withdrawal impossible or catastrophic for users · `1` possible at severe cost · `2` possible
with notice · `3` designed for withdrawal, with an exit path published.

E exists because [§H.27](../license/ml-2-3.md) makes reversibility a duty, and because an
irreversible deployment converts every other dimension into a permanent condition. A system
scoring E=0 has removed its own remedy.

---

## 3. Mechanism — the counterproductivity test (§H.7)

Applied to every harm scoring **D≥2**. It is the rubric's sharpest instrument and the one most
likely to be skipped.

> **Has the remedy made the harm worse, or moved it onto someone who did not choose it?**

Four questions, each answered in writing:

**1. Displacement.** Did the remedy move the harm rather than reduce it? *Worked case:* removing
ad slots and replacing them with a subscription reduces HX‑01 and may raise **HX‑07** —
the harm moves from attention to access, and lands on those who cannot pay.

**2. Substitution.** Did it replace a human activity that was itself the good? *Worked case:*
automating assessment feedback reduces reviewer burden and engages **§H.29** and possibly
**§H.3(a)(vii)** — the feedback was the formative activity.

**3. Certification.** Does the remedy now certify the harm as handled? *Worked case:* a cookie
banner converts unconsented tracking into consented tracking without changing what is collected.
This is **HX‑15** and it is the most common instance in practice.

**4. Metric capture.** Is the remedy's success measured by an indicator the remedy itself
produces? *Worked case:* "harm reduced because complaints fell" — after the complaint route was
replaced by a satisfaction survey.

**A remedy failing any of the four scores D=1 regardless of its ambition**, and the failure is
recorded, not just the score. A rubric that let a counterproductive remedy score highly would be
worse than no rubric, because it would launder the failure into a credential.

---

## 4. Why there is no total score

The five dimensions are **never summed.** This is the rubric's central design decision and it is
contested, so the reasoning is given in full.

A single number would be immediately useful. It would rank deployments, support a threshold, and
let a deployer report improvement. It would also be the mechanism by which this rubric became an
instrument of **HX‑15** and **HX‑16 (metric capture)** — the harms its own register names.

Three reasons, in ascending order of seriousness.

**The dimensions are not commensurable.** A=3 (constitutive of the system) and E=3 (designed for
withdrawal) do not offset. Summing implies a rate of exchange between "this harm is how the system
works" and "we could turn it off," and no such rate exists.

**A total invites optimisation of the total.** Once a number exists, the cheapest route to
improving it is found — and it is always **C**, measurement, because instrumenting a mechanism
raises the score without changing the mechanism. A deployer optimising this rubric would instrument
enthusiastically and remediate nothing, and their number would improve.

**A total permits a passing grade.** The moment a threshold exists, the rubric's output becomes
"compliant / non-compliant," and §H.16.3's presumption — that an all-clear return is evidence of
theatre — is defeated by arithmetic. The register cannot both hold that clean returns are
suspicious and issue a scale on which a clean return is available.

**What is produced instead:** a **five-tuple per harm** (`A,B,C,D,E`), a disposition, and the
counterproductivity findings. Twenty-five tuples are harder to read than one number, and that is
the point — they cannot be improved without saying which dimension moved and why.

---

## 5. The record

For each harm, the audit records:

```
HX-nn  [harm title]
  A instantiation  [0-3]  because: [one sentence]
  B exposure       [0-3]  because: [one sentence]
  C measurement    [0-3]  method:  [what is measured, how often, by whom]
  D remedy         [0-3]  what:    [and mechanism-or-symptom]
  E reversibility  [0-3]  exit:    [notice period, what is lost]
  §H.7 counterproductivity: [displacement / substitution / certification /
                             metric capture — findings, or "none found and why"]
  DISPOSITION: [remedied | partially remedied | unremedied | not engaged]
  Review: [date]
  Examined by: [natural person]  On: [date]  Evidence: [what was looked at]
```

**`Evidence: what was looked at` is the field that makes the rubric auditable.** "Reviewed the
codebase" and "read the product description" produce the same dispositions and are not the same
audit. A reader comparing two Statements can tell which was examined, and that comparison is the
only external check this instrument has.

**Mapping tuples to dispositions**, as guidance and not as arithmetic:

| Pattern | Disposition |
|---|---|
| A=0 | `not engaged` — the only warrant for it |
| A≥1, D=3, §H.7 clean | `remedied` |
| A≥1, D=1–2, or §H.7 finding | `partially remedied` |
| A≥1, D=0 | `unremedied` |
| A≥1, C≤1, D claimed ≥2 | `partially remedied` — **an unmeasured remedy cannot be certified** |

The last row is the one that will be resisted. A deployer who has genuinely fixed something but
never measured it must still write *partially remedied*, and that is correct: the claim may be
true, and it is unsupported.

---

## 6. Failure modes

**The impression audit.** Twenty-five plausible sentences, no `Evidence` field, no tuples. §5's
record format exists to make this visible rather than to prevent it.

**Skipping §H.7 where it bites hardest.** The test applies to D≥2 — exactly the harms a deployer
feels good about. It is the section most likely to be treated as a formality by someone acting in
good faith.

**Measurement as remedy.** Scoring C=3 and reading it as progress. Instrumentation is not
remediation; it is the precondition for knowing whether remediation worked.

**Disposition drift.** A prior audit's dispositions carried forward with a new date. The
`Examined by / On / Evidence` fields must be re-completed or the audit is a copy.

**Stratum V and VI under-scored systematically.** The reflexive and successor harms are the
hardest to instantiate against one's own system, because they are about *the act of governing* and
*people who cannot object*. A deployment scoring A=0 across all eleven of HX‑15…HX‑25 has almost
certainly not looked; the estate's own audit should be checked against this first.

---

## 7. Limits

**Class: epistemic.** The rubric cannot detect a harm HX-000 does not name. Its coverage is the
register's coverage, and the register is nine days old and has never had an entry withdrawn.

**Class: technical.** Nothing here is automatable. Every dimension requires judgement about a
specific system, which means the rubric's output quality is bounded by the honesty of the person
completing it — and its only defence is that dishonesty must be written down in the `because` and
`Evidence` fields, where a reader can find it.

**Class: ethical.** It scores harms and does not weigh them against benefits. That omission is
deliberate — a benefit column would immediately become the place every harm is justified — but it
means the rubric is **not a decision procedure.** It tells a deployer what their system does. It
does not tell them whether to ship.

**Class: incomplete by dependency.** HX-000 exists at eleven of twenty-five harms
([DEF-021](../00-governance-map/defect-register.md#def-021)). Until the register is complete, an
audit run against it is an audit of eleven harms wearing a twenty-five-harm form, and any Statement
produced now must say so.

---

## 8. Falsifier

This rubric is wrong if either holds:

1. **A system scoring high on D and E across all twenty-five harms is nonetheless plainly
   harmful** — showing the five dimensions to be under-inclusive, remediable only by a sixth
   dimension and not by rescaling.
2. **Two competent auditors, examining the same system with the same evidence, produce materially
   different tuples** — showing the scales to be too vague to be a procedure. This is the likelier
   failure and it is testable directly: two auditors, one system, sealed results. The estate has
   not run that test and should, before requiring the rubric of anyone else.

---

## 9. Obligation

**For the deployer:** complete §5 for every harm, including the eleven of Strata V and VI that
concern your governance rather than your product. Apply §H.7 to every D≥2. Name a natural person
under §H.16.4. Record what you looked at.

**For the estate:** run the two-auditor test of §8.2 before requiring this rubric of any licensee;
complete HX-000 so an audit against it is an audit of the full register; and publish the estate's
own tuples alongside its [Part H Statement](../license/part-h-statement.md) rather than only the
dispositions — a rubric whose author publishes conclusions without tuples has published exactly
the impression audit §6 names.

**Under ML-2.3:** §H.7 (counterproductivity), §H.4 (optimisation disclosure), §H.16 (the
Statement), §H.16.3 (the all-clear presumption), §H.19 (authorship of record), §H.27
(reversibility).

---

**Related:** [HX-000 The Register](.) ·
[HX-002 Harm → Instrument Map](hx-002-harm-instrument-map.md) ·
[Part H Statement](../license/part-h-statement.md) ·
[Scale Gate](../license/scale-gate.md) ·
[RB-05 Harm Review Gate](../rubrics/rb-05-harm-review-gate.md) · [ML-2.3](../license/ml-2-3.md)

*Curated by Maher. Five dimensions, twenty-five tuples, no total score — because the moment a
total exists, the cheapest way to improve it is to measure more and remediate nothing.*
