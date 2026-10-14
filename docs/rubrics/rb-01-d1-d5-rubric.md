---
doc_id: "RB-01"
title_en: "The D1–D5 Assessment Rubric"
title_ar: "معيار التقييم د١–د٥"
family: "rubrics"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 3
depth: 5
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: true
last_reviewed: "2026-10-01"
domain_tags: ["rubrics", "assessment", "credentials", "review"]
route: "/credentials/review/rubric/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# RB-01 · The D1–D5 Assessment Rubric

**What this instrument is.** The five dimensions on which a candidate's submitted work is judged,
and the rule that makes the judgement checkable: **the rubric is frozen before the cohort opens.**

**Designated** as a Work of Foundational Character ([DL-1 row 6](../license/designation-list.md)),
because a rubric that can be altered after submission is not an assessment standard — it is an
opinion issued afterwards.

---

## 1. Position

Assessment is where a credential either means something or does not. Everything upstream — the
curriculum, the lesson architecture, the six rails — produces a claim that a person can do
something; the rubric is what tests it.

Its siblings are [RB-02 The Proof Ladder](rb-02-proof-ladder.md), which classes the *evidence* a
candidate supplies, and [MX-005](../corpus/mx-005-credentialing-and-assessment.md), which governs
the credential itself. Published at `/credentials/review/rubric/`, with a mirror at
`/method/assessment/rubric/` — **two routes, deliberately**: the Method route defines the
instrument, the Credentials route states how a candidate is judged by it, and
[SITE-01 §5.2](../site/route-manifest.md) requires each to open on a different section and cite the
other.

**The macro register.** Credentialing at scale has drifted toward two failure modes, and both are
about what is cheap to measure. Automated assessment measures what a machine can mark. Reputational
assessment measures who the assessor already knows. Under **HX‑05** (asymmetry of the record) both
concentrate the power to certify in whoever controls the instrument, and neither gives the
candidate a document they can argue with. A **published, frozen, dimensioned** rubric is the
cheapest available correction: it lets a candidate know before submitting exactly what will be
judged, and lets them contest a score against a text.

---

## 2. Definition — the five dimensions

Each scores **0–4**. Dimensions are **not summed** — see §4.

| Dim | Name | Asks |
|---|---|---|
| **D1** | **Correctness** | Does it work, and is what it claims about itself true? |
| **D2** | **Method** | Was the approach defensible, and is the reasoning recoverable from the artefact? |
| **D3** | **Limits** | Does the candidate state what their work does not do, and why? |
| **D4** | **Evidence** | Is the claim supported at the level [RB-02](rb-02-proof-ladder.md) requires? |
| **D5** | **Transmission** | Could a competent stranger reproduce or extend this from what is supplied? |

### 2.1 The scale, stated so a score can be wrong

`0` absent · `1` attempted, materially deficient · `2` adequate, meets the stated requirement ·
`3` strong, exceeds it in a specified way · `4` exemplary, usable as a teaching specimen.

**`2` is the pass point on every dimension**, and it is deliberately described as *adequate*
rather than *good*. A rubric whose midpoint reads as praise inflates within two cohorts.

### 2.2 D3 and D5 are the estate's additions, and the reason this rubric exists

D1, D2 and D4 appear in some form in most assessment schemes. The other two do not.

**D3 — Limits.** A candidate who cannot state what their work fails to do has not finished
thinking about it. This mirrors the estate's own requirement on itself:
[ST-24 §2.1](../standards/st-24-page-prose-standard.md) makes a Limits section mandatory on every
page and requires it to name a **class** — epistemic, technical, ethical, economic. A candidate
scoring 0 on D3 may still have working software; they do not yet have an assessable claim about it.

**D5 — Transmission.** Work that only its author can operate is not a contribution. Under **HX‑22**
(loss of transmissible skill) this is a structural matter rather than a courtesy: a body of
practice that cannot be handed on dies with its practitioners, and an academy that certifies
non-transmissible work is certifying the wrong property.

**Neither is scored on presentation quality.** A rough README that genuinely enables a stranger
scores higher on D5 than a polished document that does not.

---

## 3. Mechanism — the freeze

**The rubric applying to a cohort is fixed before that cohort opens and does not change until it
closes.** No mid-cohort amendment, no clarification that alters a threshold, no new dimension.

**Why absolute.** A rubric amendable during assessment lets the assessor change the test after
seeing the answers, which is not assessment. The candidate's protection is that the text they were
judged against is the text they read before starting — and that they can retrieve it afterwards.

**How an amendment happens.** Between cohorts, with a changelog line at
[`changelog.md`](../00-governance-map/changelog.md), a version increment, and the previous version
retained under [MX-013 Rule 4](../corpus/mx-013-records-and-versioning.md). A candidate judged
under `v2026.10.1` can retrieve `v2026.10.1` in 2031.

### 3.1 The reviewer's record

For each dimension:

```
D{n}  [0-4]
  Because:   [one sentence, citing the specific artefact or passage]
  Evidence:  [what the reviewer actually examined]
Reviewer: [natural person]   Date: [ ]   COI declared: [yes/no]
```

**`Evidence: what the reviewer actually examined`** is the field that makes review auditable.
"Reviewed the submission" and "ran the test suite on commit `a3f9`, read §§2–4 of the dossier" are
not the same review and produce the same scores. This is the identical mechanism
[HX-001 §5](../harms/hx-001-harm-audit-rubric.md) uses for harm audits, and for the same reason: a
score without a record of what was looked at cannot be contested.

---

## 4. Why there is no total score

The five dimensions are **never summed into a grade.** This is the rubric's most contested design
decision and it mirrors [HX-001 §4](../harms/hx-001-harm-audit-rubric.md) exactly.

**The dimensions are not commensurable.** D1=4 with D3=0 is working software from someone who
cannot say what it fails at. D1=2 with D5=4 is modest work that others can build on. Summing
implies an exchange rate between correctness and transmissibility, and none exists.

**A total invites optimisation of the total.** Once a number exists, the cheapest route to raising
it is found — and here it is **D4**, evidence, because assembling more documentation raises a score
without improving the work.

**A total permits an appeal about arithmetic instead of about judgement.** The estate would rather
contest *"D3 scored 1 and here is why that is wrong"* than *"the total should have been 14."* The
first is a conversation about the work; the second is about the scale.

**What is issued instead:** a **five-tuple** plus a determination — `pass`, `pass with specified
deficiency`, or `not yet`. The middle outcome is the useful one and the most used: it names exactly
which dimension failed and what would close it.

**`not yet` rather than `fail`** is deliberate and not euphemism. The credential ladder is
renewable and re-submittable; a determination that closes a door the estate does not intend to
close misdescribes its own process.

---

## 5. Worked instance — a Series Practitioner submission

A candidate submits a working retrieval-evaluation harness for S01.

**D1 Correctness — 3.** Runs, reproduces its reported numbers on a clean checkout. One documented
edge case fails, and the candidate says so — which is why this is 3 and not 2: the self-report is
*evidence about D1*, not a deduction from it.

**D2 Method — 2.** Approach defensible; the choice of baseline is unexplained. Adequate, not
strong. *Because:* dossier §3 states the baseline and not the reason for it.

**D3 Limits — 1.** The dossier lists features not yet built. That is a **roadmap, not limits.**
Nothing states what the harness *cannot determine* — that it measures retrieval quality and says
nothing about downstream task performance. Materially deficient.

**D4 Evidence — 3.** P2 under [RB-02](rb-02-proof-ladder.md): artefact plus reproducible run, short
of independent replication.

**D5 Transmission — 4.** A stranger cloned it and ran it in eleven minutes from the README alone.
Exemplary.

**Determination: `pass with specified deficiency` — D3.** The candidate is told precisely what
closes it: one paragraph naming the limit class of what the harness cannot determine.

**What a summed score would have produced.** 13 of 20, a pass, and **the D3 deficiency would have
disappeared into the total** — which is the exact outcome §4 exists to prevent. The most useful
thing this assessment produced is the one sentence a total would have averaged away.

---

## 6. Failure modes

**Score inflation across cohorts.** `2` drifts from *adequate* to *disappointing*. Detected only
by publishing the distribution, which `/credentials/review/statistics/` exists to do.

**D3 answered with a roadmap.** §5's live instance. Future features are not limits, and the
confusion is near-universal on first submission.

**D5 scored on polish.** A well-written README that does not enable a stranger is a D5 failure
dressed as a success. The test is whether someone *did* reproduce it, not whether the documentation
looks thorough.

**The reviewer who knows the candidate.** COI declaration is mandatory and published at
`/credentials/review/conflicts/`. An estate this small cannot always avoid the conflict, so it
**declares** it rather than pretending otherwise — the same treatment
[RB-05 §5](rb-05-harm-review-gate.md) applies to its own gate-holder problem.

**Mid-cohort clarification.** *"To clarify, D4 requires…"* issued during assessment. That is an
amendment, however phrased, and §3 forbids it.

---

## 7. Limits

**Class: technical.** Nothing here is automatable. Every dimension requires a competent reader,
which bounds throughput and makes the rubric's quality dependent on reviewer quality.

**Class: epistemic.** **Inter-rater reliability is unmeasured.** Two reviewers scoring the same
submission may diverge, and the estate does not know by how much. The two-auditor test specified
for [HX-001 §8](../harms/hx-001-harm-audit-rubric.md) applies here identically and has not been
run — which makes §2.1's scale a specification rather than a validated instrument.

**Class: practical.** **No credential has ever been issued.** No submission has been assessed, no
reviewer has used this rubric, and the appeals route at
[MX-016](../corpus/mx-016-appeals-and-due-process.md) has never been exercised. Everything above is
untested.

**Class: governance.** The rubric cannot make a reviewer honest. Its protections are procedural —
publication, freezing, the `Evidence` field, COI declaration — and each raises the cost of a bad
review without preventing one.

---

## 8. Falsifier

1. **Two competent reviewers, same submission, materially different tuples.** Directly testable,
   never run, and the likeliest to fire. It would falsify §2.1's scale as a procedure rather than
   the dimensions as a set.
2. **A candidate scoring ≥2 on all five whose work is nonetheless not worth certifying** —
   under-inclusive dimensions, remediable only by a sixth dimension, not by raising thresholds.
3. **A candidate scoring 0–1 on a dimension whose work is clearly certifiable**, showing that
   dimension a formality. **D3 is the candidate**: if capable practitioners routinely fail it while
   producing excellent work, D3 is measuring documentation habits rather than understanding.
4. **`pass with specified deficiency` proving unused** — either everyone passes clean or nobody
   does, which would show the middle determination decorative.

---

## 9. Obligation

**For the reviewer:** score every dimension, write the `Because` and the `Evidence`, name yourself,
declare conflicts. Never sum. Issue one of three determinations.

**For the candidate:** the rubric is published before you start and frozen while you are assessed.
If you are scored against a text that changed, that is a breach of §3 and grounds for appeal under
[MX-016](../corpus/mx-016-appeals-and-due-process.md).

**For the estate:** run the inter-rater test (§8.1) before issuing a single credential. Publish the
score distribution per cohort at `/credentials/review/statistics/`, including the dimension most
often failed — which the estate expects to be D3 and should verify rather than assume.

**Under ML-2.3:** §H.05 (asymmetry of the record — the candidate must be able to contest against a
text), §H.16.3 by analogy (an assessment regime where nothing ever fails is presumptively not
assessing), §H.19 (authorship of record — the named reviewer), §H.22 (language parity — the rubric
must be assessed identically in both language trees).

---

**Related:** [RB-02 The Proof Ladder](rb-02-proof-ladder.md) ·
[RB-05 Harm Review Gate](rb-05-harm-review-gate.md) ·
[MX-005 Credentialing and Assessment](../corpus/mx-005-credentialing-and-assessment.md) ·
[MX-016 Appeals and Due Process](../corpus/mx-016-appeals-and-due-process.md) ·
[HX-001 Harm Audit Rubric §4](../harms/hx-001-harm-audit-rubric.md) ·
[ST-24 Page Prose Standard](../standards/st-24-page-prose-standard.md) ·
[SITE-01 Route Manifest §5.2](../site/route-manifest.md)

*Curated by Maher. Five dimensions, no total score, three determinations — and zero credentials
ever issued, which makes every claim in this instrument a specification rather than a result.*
