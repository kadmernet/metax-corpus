---
doc_id: "RB-05"
title_en: "The Harm Review Gate"
title_ar: "بوابة مراجعة الأضرار"
family: "rubrics"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 4
depth: 4
evidence_class: "semi-durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["rubrics", "harms", "build-gates", "review"]
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# RB-05 · The Harm Review Gate

**What this instrument is.** The gate that stops something shipping until its harm assessment has
been done. [HX-001](../harms/hx-001-harm-audit-rubric.md) is the *procedure* for assessing a
deployment; RB-05 is the **point in a workflow where the procedure is enforced** and the record of
what happens when it fails.

**The distinction that makes it a separate document.** A rubric with no gate is a suggestion. The
estate has learned this about itself the expensive way: it holds a falsifiability standard, an
evidence standard, a decay standard and a front-matter schema, and **none of them is enforced**,
because the build that would enforce them does not run
([DEF-001](../00-governance-map/defect-register.md#def-001)). RB-05 exists so that the harms
register does not join that list.

---

## 1. Position

This gate sits in three workflows, and its placement in each is the substance of the instrument.

**In the estate's own build**, between "the artefact is complete" and "the artefact is published."
**In an academy's chartering path**, at Requirement 11 (`/academies/requirements/r11-part-h/`).
**In a licensee's deployment**, at the tier threshold crossing that triggers
[ML-2.3 §H.16](../license/ml-2-3.md)'s ninety-day window.

Its parent instruments are [RB-03 Structural Review and Build Gates](rb-03-structural-review.md),
which establishes the estate's gate vocabulary, and HX-001, which supplies the assessment. Its
consumers are whoever holds the publish decision.

**The macro register, because a gate is a political object.** A gate is where an institution
decides what it will refuse to ship. Most technology organisations have gates for security, for
legal exposure and for brand risk — and none for harm to the people affected, because harm to
affected parties has no internal claimant. RB-05 is an attempt to manufacture that claimant
procedurally. Whether a manufactured claimant survives contact with a deadline is the open
question, and §7 says so.

---

## 2. Definition — what the gate examines

The gate does **not** re-run HX-001. It examines whether HX-001 was run properly, which is a
different and cheaper question. Six checks:

| # | Check | Fails when |
|---:|---|---|
| **1** | **Completeness** | Any of the twenty-five harms has no five-tuple |
| **2** | **Warrant for `not engaged`** | A `not engaged` disposition without `A=0`, or with A=0 justified as "small" or "managed" rather than structurally absent |
| **3** | **Counterproductivity applied** | Any harm scoring `D≥2` with no §H.7 finding recorded, including "none found and why" |
| **4** | **Evidence recorded** | Any harm whose `Evidence: what was looked at` field is absent or generic |
| **5** | **Reflexive stratum examined** | HX‑15…HX‑19 scored `A=0` across all five, or dispositions in Strata V and VI with no `Evidence` |
| **6** | **Named person** | No natural person under §H.16.4, or a department in that field |

**Check 5 is the one this gate exists for.** Strata V and VI — reflexive and successor harms — are
the two a deployer will skip, because they are about the *act of governing* and about *people who
cannot object*, and neither has a complainant in the room. A five-tuple set that marks all of
HX‑15…HX‑19 structurally absent is almost certainly an assessment that was not attempted, and the
gate treats it as a failure rather than as a clean result.

---

## 3. Mechanism — the three outcomes

The gate returns one of three states. There is deliberately no "pass."

| Outcome | Meaning | Effect |
|---|---|---|
| **CLEARED** | The assessment was performed to procedure | Publication proceeds. **Not** a finding that the artefact is harmless |
| **RETURNED** | The assessment is incomplete or unwarranted | Publication blocked. The specific failed checks are named |
| **ESCALATED** | The assessment is complete and discloses an absolute engaged, or a Tier 3 deployment with an unremedied Stratum I harm | Publication blocked. Goes to the Curator. **No editor may clear it** |

### 3.1 Why "CLEARED" and not "PASSED"

The vocabulary is load-bearing. A gate that issues a **pass** has certified the artefact, and a
certification is what an organisation cites later: *"it passed harm review."* That sentence is
[HX‑17](../harms/hx-002-harm-instrument-map.md) — the audit that certifies itself — and it would
be created by this gate's own output.

**CLEARED** states only that the procedure was followed. It makes no claim about the artefact,
which means it cannot be cited as one. An artefact can be CLEARED while carrying four unremedied
harms, and that is correct: the gate's job is to ensure the harms were *found and published*, not
to decide whether they are acceptable. That decision belongs to a person, on the record.

### 3.2 The escalation triggers, and why they are narrow

Only two things escalate, and the narrowness is deliberate — a gate that escalates everything is a
gate that is routed around.

**An absolute engaged (§H.3(a)(i)–(viii)).** Not a judgement call. If the assessment discloses an
absolute, the grant has already terminated under §F.4 and the question is not whether to ship but
what has already happened. Note that **(vii) developmental substitution is disjunctive** — any
single limb suffices — which makes it the trigger most likely to fire and the one most likely to
be misread as cumulative.

**A Tier 3 deployment with an unremedied Stratum I harm.** Tier 3 means users who cannot
practically decline ([Scale Gate §3.3](../license/scale-gate.md)). An unremedied cognitive harm
imposed on people with no exit is the specific configuration §H.21 (proportionate imposition)
addresses, and it is not an editorial decision.

### 3.3 What the gate does not do

**It does not weigh harm against benefit.** No benefit column exists, here or in HX-001, because a
benefit column becomes the place every harm is justified. The gate therefore cannot tell anyone
whether to ship — only whether they know what they are shipping.

**It does not score.** It returns three states and a list of failed checks. Any attempt to derive
a metric from gate outcomes — clearance rates, time-to-clear — recreates
[HX‑16](../harms/hx-002-harm-instrument-map.md) (metric capture) and is prohibited by §5.

**It does not expire an assessment silently.** An assessment past its review date does not lapse
into RETURNED; it lapses into **nothing**, and the artefact's published Statement becomes stale
with dates a reader can check. The gate governs publication, not the passage of time.

---

## 4. Worked instance — this estate, run against its own gate

The most useful test of a gate is its author's own artefact, so: **MetaX.Academy, at v2026.10.1.**

**Check 1, completeness — FAILS.** HX-000 exists at eleven of twenty-five harms
([DEF-021](../00-governance-map/defect-register.md#def-021)). Fourteen harms have no register text,
so no five-tuple can be scored against them.

**Check 3, counterproductivity — not reached.** No tuples, so no `D≥2` to test.

**Check 4, evidence — partially satisfiable.** The estate has unusually good evidence for its
content-plane claims: it fetched its own live site and read `css/style.css`, `index.html`,
`components.js` and `site.js`, which produced nine corrections. But that evidence carries a defect
of its own — none of it recorded **provenance of purpose**, so nine claims describe a *demo* while
reading as claims about the estate
([DEF-024](../00-governance-map/defect-register.md#def-024)).

**Check 5, reflexive stratum — FAILS in the informative direction.**
[HX-002 §7](../harms/hx-002-harm-instrument-map.md) marks HX‑21 and HX‑24 `unexamined`, which is a
worse state than a named failure and is recorded as such. But the estate did *not* mark Strata V
and VI structurally absent — it marked HX‑15 as **FAILS** against itself, which is the behaviour
check 5 was written to require.

**Check 6, named person — FAILS.** No natural person is named, because
[ML-2.1 still carries `[STEWARD NAME]` unfilled and is unsigned](../license/version-history.md#5-what-this-history-does-not-contain)
([B-01](../00-governance-map/launch-blockers.md)).

**Outcome: RETURNED**, on checks 1, 5 and 6.

**What this demonstrates about the gate, which is why the instance is worth including.** The
estate cannot clear its own harm review gate, and the gate is not thereby wrong — it is
*operating*. Three of the failures are sequencing (the register is incomplete, the licence is
unsigned) and one is substantive (two successor harms unexamined). A gate whose author cleared it
on the first attempt would tell a reader that the gate was calibrated to the author. This one was
not, and the RETURNED result is published rather than deferred until it would read better.

---

## 5. Prohibited uses of this gate

Four, each of which would convert the gate into an instrument of the harms it enforces.

**No clearance metric.** Clearance rates, mean time-to-clear, quarterly clearance counts. Any such
metric makes clearing the objective, and the cheapest route to clearing is a thinner assessment.
This is HX‑16 and it is prohibited outright.

**No clearance as a marketing claim.** "Harm-reviewed" or "cleared under RB-05" may not appear in
promotional material by the estate or any licensee. CLEARED means the procedure was followed and
nothing else; advertising it converts §3.1's careful vocabulary back into a certification.

**No pre-clearance.** A gate applied to a plan rather than to a built artefact assesses an
intention. Assessments run against specifications must be re-run against what shipped.

**No delegation to the party assessed.** The gate holder may not be the person who completed
HX-001. Where an estate is small enough that this is impossible — as it is here — the conflict must
be **declared in the record** rather than resolved by pretending otherwise. This document is
subject to that declaration: it was drafted by the same agent that drafted HX-001 and HX-002, and
§4's RETURNED result was produced by that agent against its own estate. A reader should weight it
accordingly.

---

## 6. Limits

**Class: technical.** Nothing here is automatable except checks 1 and 6. Checks 2, 3, 4 and 5 all
require reading an assessment and judging whether it was serious, and no build step can do that.

**Class: institutional, and this is the binding one.** A gate is only as strong as the
organisation's willingness to be blocked by it. RB-05 has **no enforcement mechanism** beyond the
Curator's own commitment, and the estate's history is not reassuring: it holds four standards with
gates that do not run. This gate's honest status is *"specified, never exercised in anger."*

**Class: epistemic.** The gate examines whether an assessment was performed to procedure. It cannot
detect an assessment that is thorough, well-evidenced, procedurally perfect and **wrong** about
what the system does.

**Class: ethical.** By refusing a benefit column the gate refuses to be a decision procedure. Some
readers will find that evasive — the hard question is always whether a harm is worth its benefit,
and this instrument declines it. The refusal is deliberate and it has a cost: the gate can block
publication and cannot justify shipping.

---

## 7. Falsifier

This gate is wrong if any of the following is observed:

1. **An artefact CLEARED that plainly instantiates several harms undisclosed in its Statement** —
   showing the six checks to be satisfiable without examination.
2. **An artefact RETURNED whose assessment was in fact thorough** — showing a check to be a
   formality rather than a test. Check 5 is the candidate: a genuinely static document with no
   governance apparatus might honestly score `A=0` across Stratum V.
3. **The gate routed around under deadline pressure, without the routing being recorded.** This is
   the likeliest failure of all and it falsifies §6's institutional limit rather than the
   procedure — a gate with no enforcement is a gate that documents its own bypass or is silent
   about it.
4. **A clearance metric appearing anywhere in the estate**, which would show §5's prohibitions to
   be unenforceable by prose.

---

## 8. Obligation

**For the gate holder:** run the six checks, return one of three states, name the failed checks.
Never issue a pass. Never clear an ESCALATED artefact, whatever the deadline.

**For the estate:** the standing obligation is check 1 — complete HX-000, without which this gate
returns RETURNED on every artefact including its own. Then examine HX‑21 and HX‑24. Then sign the
licence, so that check 6 can be satisfied by anyone at all.

**Record every bypass.** If the gate is routed around, that fact belongs in the
[Defect Register](../00-governance-map/defect-register.md) as a governance defect with a named
decision-maker. An unrecorded bypass is worse than no gate, because it produces the *appearance*
of a gate — which is HX‑15, committed by the instrument built to catch it.

**Under ML-2.3:** §H.7 (counterproductivity, check 3), §H.16 (the Statement this gates), §H.16.3
(why no pass is issued), §H.17 (non-theatre), §H.19 (check 6), §H.21 (escalation trigger 2),
§H.25 (agent constraint, which §5's fourth prohibition and this document's own authorship
declaration engage directly).

---

**Related:** [HX-001 Harm Audit Rubric](../harms/hx-001-harm-audit-rubric.md) ·
[HX-002 Harm → Instrument Map](../harms/hx-002-harm-instrument-map.md) ·
[Part H Statement](../license/part-h-statement.md) ·
[Scale Gate](../license/scale-gate.md) ·
[RB-03 Structural Review](rb-03-structural-review.md) ·
[Defect Register](../00-governance-map/defect-register.md) · [ML-2.3](../license/ml-2-3.md)

*Curated by Maher. Six checks, three outcomes, no pass — and its author's own estate returns
RETURNED on three of the six, published rather than deferred until it would read better.*
