---
doc_id: "RB-02"
title_en: "The Proof Ladder P0–P3"
title_ar: "سلّم الإثبات ب٠–ب٣"
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
domain_tags: ["rubrics", "evidence", "credentials", "proof"]
route: "/credentials/evidence/proof-ladder/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# RB-02 · The Proof Ladder P0–P3

**What this instrument is.** The four levels at which a candidate may prove a claim about their own
work, and the rule that the **credential names the level** rather than concealing it.

**Designated** as a Work of Foundational Character ([DL-1 row 10](../license/designation-list.md)).

---

## 1. Position

[RB-01](rb-01-d1-d5-rubric.md) judges the work across five dimensions. Its **D4** asks whether the
claim is supported at the level this ladder requires — so RB-02 is the instrument D4 defers to, and
the two are useless apart.

The distinction they enforce is one most credentialing systems collapse: **what a candidate built**
versus **what a candidate has shown**. A person can build something excellent and prove nothing
about it; a person can prove a great deal about something modest. A credential that does not
separate these asserts a competence it has not tested.

Published at `/credentials/evidence/proof-ladder/`. Its estate-side analogue is
[ST-07](../standards/st-07-evidence-and-verify.md)'s E0–E4 classes — the same idea applied to the
corpus's own claims rather than to a candidate's, and §2.1 explains why the two scales differ.

**The macro register.** Under **HX‑02** (epistemic dependency) a credential is a **transfer of
trust**: a reader who cannot assess a practitioner's work relies on the issuer's assessment
instead. The whole apparatus therefore rests on whether the issuer's evidence standard is
published and whether it fires. A credentialing system with no stated proof level asks the world
to defer to a judgement it will not describe, which is the harm rather than a bureaucratic
shortfall.

---

## 2. Definition — the four levels

| Level | Means | Verified by |
|---|---|---|
| **P0** | **Assertion.** The candidate says they did it | Nobody. **Never sufficient for a credential** |
| **P1** | **Artefact.** The work exists and can be inspected | A reviewer reads it |
| **P2** | **Reproduction.** A reviewer independently ran it and obtained the reported result | A reviewer executes it |
| **P3** | **Independent replication.** A party unconnected to the candidate obtained it | A third party, named |

**The ladder is about who checked, not about how impressive the work is.** A trivial script at P3
is better proven than a substantial system at P1 — and the credential says so, which is the point.

### 2.1 Why four levels rather than ST-07's five

[ST-07](../standards/st-07-evidence-and-verify.md) grades the **estate's own claims** on E0–E4,
where E4 is independent replication *or* a retrievable primary source. A candidate cannot cite a
primary source *for their own work* — there is nothing to retrieve except the work — so the
"retrievable source" rung has no analogue here and the ladder is four rungs, not five.

The parallel that does hold is the bottom rung. **E0 is unpublishable; P0 is uncreditable.** In
both cases the floor is *an assertion with nothing behind it*, and in both cases the correct
response is to obtain evidence or withdraw the claim.

### 2.2 P2 is the working level, and P3 is rarer than it sounds

**Most credentials in this estate are earned at P2.** A reviewer clones the artefact, runs it,
obtains the reported result. That is a genuine check and it is affordable.

**P3 requires a party unconnected to the candidate**, named in the record. That is expensive, and
the estate does not pretend otherwise: P3 is expected for `Master-Fellow` and
`MetaX Contributor` and **not** for `Series Practitioner`. A ladder demanding P3 everywhere would
produce a credential nobody can earn, which is a different failure from one anybody can.

**What "unconnected" excludes:** a co-author, a colleague at the same organisation, a person the
candidate proposed as a replicator, and any reviewer with an undeclared conflict under
`/credentials/review/conflicts/`.

---

## 3. Mechanism — the submission pack

A candidate supplies, per claim:

```
CLAIM        [what the work does, one sentence]
LEVEL SOUGHT [P1 | P2 | P3]
ARTEFACT     [location, commit or version identifier]
REPRODUCTION [exact steps; expected output]
ENVIRONMENT  [what it needs to run]
NOT CLAIMED  [what this evidence does not establish]
```

### 3.1 `NOT CLAIMED` is the field that does the work

It is the [RB-01](rb-01-d1-d5-rubric.md) **D3** requirement arriving at the evidence layer, and it
is the field candidates most often leave empty.

A reproduction establishes *that the reported result was obtained under the stated conditions*. It
does not establish that the approach is optimal, that it generalises, or that it works at another
scale. A candidate who states this precisely has demonstrated something a passing run cannot show:
that they understand the limits of their own evidence.

**A `NOT CLAIMED` field left blank is itself assessable** — under D3, and usually adversely.

### 3.2 The level is recorded on the credential

The issued credential names the proof level per claim. A verifier at
`/credentials/verify/lookup/` returns it, and `/credentials/verify/limits/` — *"What It Does Not
Prove"* — states in prose what a P2 credential does and does not establish.

**This is the estate's central anti-inflation mechanism.** A credential that concealed its
evidentiary basis would let P1 and P3 look identical to an employer, and every incentive would then
push toward the cheaper one.

---

## 4. Worked instance — one claim at three levels

*"This harness measures retrieval quality on the S01 benchmark and reports nDCG@10 of 0.71."*

**At P1.** The reviewer reads the code and the results file. Establishes: code exists, is coherent,
reports 0.71. **Does not establish** that running it produces 0.71 — the file could be stale,
hand-edited, or from different parameters. P1 is *the work exists and is not obviously wrong*.

**At P2.** The reviewer clones at commit `a3f9`, runs the documented command, obtains 0.71 ±0.002.
Establishes reproducibility under the stated conditions. **Does not establish** that the benchmark
measures what the candidate says, nor that another environment gives the same figure.

**At P3.** An unconnected researcher, named, obtains 0.709 on different hardware. Establishes
environment-independence. **Still does not establish** that nDCG@10 is the right metric — a
question of judgement, assessed under D2, not of proof.

**What the instance shows.** The same true claim occupies three evidentiary positions, and the
difference between them is entirely **who checked and under what independence**. Note also that
what remains unestablished at P3 — whether the metric is the right one — is *never* reachable by
this ladder. Proof levels measure verification, not judgement, and a credentialing system that
conflates them will issue confident credentials for well-verified bad ideas.

---

## 5. Failure modes

**P0 laundered as P1.** A screenshot, a description, a link to a private repository. If a reviewer
cannot inspect the artefact, the level is P0 and the claim is uncreditable.

**P2 claimed without execution.** A reviewer reading a CI badge rather than running the code. The
`Evidence: what the reviewer actually examined` field of
[RB-01 §3.1](rb-01-d1-d5-rubric.md) is the control.

**"Independent" replication that is not.** A colleague, a co-author, a replicator the candidate
nominated. §2.2's exclusions exist because this is the commonest way P3 becomes P2 with extra
paperwork.

**Level inflation across cohorts.** P2 granted for partial reproduction, then for a successful
build, then for a passing test suite. Detected only by publishing the distribution of levels per
cohort.

**`NOT CLAIMED` left blank.** §3.1. The estate expects this to be the most frequently deficient
field on first submission.

**Proof level mistaken for quality.** A P3 credential on trivial work outranking a P1 credential on
substantial work, **in a reader's mind**. The ladder cannot prevent this; `/credentials/verify/limits/`
exists to say so plainly, and RB-01's D1 and D2 are where substance is judged.

---

## 6. Limits

**Class: practical, and it dominates.** **No credential has ever been issued and no submission has
ever been assessed.** Every level, threshold and exclusion here is a specification. The estate does
not know what fraction of submissions will reach P2, nor whether P3 is achievable at all for an
unfunded candidate.

**Class: economic.** P3 requires a named, unconnected party to spend real time. The estate has no
mechanism to compensate them, so P3 currently depends on goodwill — which is not a foundation for
the top two credential tiers and is stated here rather than discovered later.

**Class: epistemic.** The ladder measures **verification**, not **judgement**. §4's worked instance
shows the boundary: no proof level establishes that a metric is the right metric.

**Class: technical.** Reproduction depends on the candidate's environment documentation. A
reviewer who cannot reproduce may be facing a broken claim or a missing dependency, and the ladder
does not distinguish them — the reviewer must, in the `Because` field.

---

## 7. Falsifier

1. **A claim whose proof does not fit the four levels** — under-inclusive. Candidate: work whose
   artefact **cannot be shared** for legitimate reasons, where P1 is unreachable and the claim may
   still be true. The estate currently has no answer and does not pretend to.
2. **P2 proving indistinguishable from P1 in practice**, because reviewers do not in fact execute.
   Measurable once reviews exist.
3. **P3 never achieved by any candidate in a year**, showing the top rung aspirational and the two
   senior credentials therefore unearnable as specified. **The likeliest to fire.**
4. **Credentials at different levels treated identically by employers**, falsifying §3.2's premise
   that recording the level prevents inflation.

---

## 8. Obligation

**For the candidate:** state the level you seek and complete `NOT CLAIMED` honestly. Claiming P3
and delivering P2 is not judged as a stronger P2 — it is a misdescription of your own evidence and
is assessed as such.

**For the reviewer:** execute what you claim to have executed. Record it. Where reproduction fails,
say whether the claim failed or the environment did.

**For the estate:** publish the distribution of levels per cohort at
`/credentials/review/statistics/`, and solve P3's compensation problem before offering
`Master-Fellow` — an unearnable top tier is worse than a missing one.

**For a reader of a credential:** the level is on the record and
`/credentials/verify/limits/` states what it does not prove. A P2 credential is a claim about
reproduction under stated conditions, and nothing more.

**Under ML-2.3:** §H.02 (epistemic dependency — the transfer of trust a credential performs),
§H.05 (asymmetry of the record), §H.19 (authorship of record — the named replicator at P3), §H.16.3
by analogy (an evidence regime in which nothing ever falls short is not testing anything).

---

**Related:** [RB-01 The D1–D5 Rubric](rb-01-d1-d5-rubric.md) ·
[RB-05 Harm Review Gate](rb-05-harm-review-gate.md) ·
[ST-07 Evidence and VERIFY](../standards/st-07-evidence-and-verify.md) ·
[MX-005 Credentialing and Assessment](../corpus/mx-005-credentialing-and-assessment.md) ·
[SITE-01 §5.6](../site/route-manifest.md) ·
[MX-016 Appeals and Due Process](../corpus/mx-016-appeals-and-due-process.md)

*Curated by Maher. Four rungs, one uncreditable floor, and a top rung that currently depends on
somebody's goodwill — which the estate states here rather than discovering when the first
Master-Fellow applies.*
