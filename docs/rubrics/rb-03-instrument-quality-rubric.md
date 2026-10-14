---
doc_id: RB-03
title_en: Instrument Quality Rubric
title_ar: مقياس جودة الأدوات
family: rubrics
version: v2026.10.1
status: published
authority: operative-form
prevailing_text: ar
audience_tier: 3
depth: meta
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [rubric, quality, instruments, scoring, self-assessment]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000, which then scored its own output with it; see §6.
route: /rubrics/rb-03/
---

# RB-03 — Instrument Quality Rubric

> **Authority.** `operative-form`, tier 5. It supplies a **form for judging**, not
> a governing duty. The duty to meet form is
> [ST-24](../standards/st-24-page-prose-standard.md) and
> [SITE-02](../site/page-contract.md); the duty to label evidence is
> [ST-07](../standards/st-07-evidence-and-verify.md). This rubric scores how well
> an instrument discharges those duties.

> **Disclosure first.** This rubric was applied, once, by its own author to its own
> corpus ([§6](#6-worked-instance)). The result was **not flattering and not
> independent** — a self-score is [MX-017 C1](../corpus/mx-017-conflicts-of-interest.md),
> an unrecusable conflict whose interest pulls toward a higher mark. A reader
> should treat every number in §6 as the interested party's own estimate and rerun
> the rubric themselves; that is what §8 asks for.

---

## 1. Position

Three rubrics exist and they judge different things:

| Rubric | Judges | Subject |
|---|---|---|
| [RB-01](rb-01-d1-d5-rubric.md) | Competence | A **person's** demonstrated work |
| [RB-02](rb-02-proof-ladder.md) | Strength of proof | A **claim's** evidential standing |
| **RB-03** (this) | Quality of an instrument | A **document** in this corpus |
| [RB-05](rb-05-harm-review-gate.md) | Harm handling | A **piece of work** before publication |

RB-03 fills the gap the others leave: an instrument can be perfectly formed under
ST-24, carry properly labelled E0 claims, and still be **bad** — vague where it
should bind, silent where it should refuse, unfalsifiable in the parts that
matter. Form compliance is necessary and nowhere near sufficient.

### 1.1 Inherited refusals

From [RB-01](rb-01-d1-d5-rubric.md), two rules carry over unchanged:

- **No total score.** Dimensions are reported individually. A composite lets a
  strong dimension hide a failing one, which is the specific failure mode a
  governance corpus can least afford.
- **Frozen per cohort.** The rubric version under which an instrument was scored
  is recorded with the score, permanently.

## 2. Definition

RB-03 scores an instrument on **six** dimensions, each 0–4, each independently
reported.

| Dim | Name | Asks |
|---|---|---|
| **Q1** | **Bindingness** | Does it state what is *required*, or only what is *desirable*? |
| **Q2** | **Falsifiability** | Can an outsider run its falsifier without the estate's cooperation? |
| **Q3** | **Disclosure** | Does it name its own gaps, and in the direction adverse to the author? |
| **Q4** | **Operability** | Can the processes it specifies actually be run by the parties that exist? |
| **Q5** | **Traceability** | Does every identifier and term link to its defining instrument? |
| **Q6** | **Proportion** | Is the length and register matched to the weight of the subject? |

### 2.1 The scale

| Score | Meaning |
|---|---|
| **0** | Absent. The dimension is not addressed at all |
| **1** | Asserted. Addressed in words with nothing behind it |
| **2** | Partial. Addressed, with material gaps the instrument does not acknowledge |
| **3** | Sound. Addressed, gaps acknowledged |
| **4** | Exemplary. Addressed, gaps acknowledged, and the acknowledgement is itself checkable |

The step from **2 to 3 is acknowledgement**, not completeness. This is deliberate
and is the rubric's central judgement: an instrument with a disclosed gap is more
useful than one with a concealed one, even though the second reads better. The
step from **3 to 4 is checkability** of the disclosure.

### 2.2 Q4 is where this corpus fails

Operability is scored against **the parties that exist**, not the parties a
well-run institution would have. An instrument specifying independent review
scores **1 on Q4** in an estate with one participant, however well the review is
described. [DEF-031](../00-governance-map/defect-register.md) is the general case.

This makes Q4 unusually harsh here, and the harshness is the point: a rubric that
scored specifications on their elegance would rate this corpus highly and tell a
reader nothing.

## 3. Mechanism

### 3.1 Scoring path

```
read the instrument in full            (no scoring from summaries — GM-01 §3)
for each dimension Q1..Q6:
    locate the evidence in the text
    assign 0..4 against §2.1
    record the LOCATION, not just the score
report six numbers + the rubric version
NEVER compute a total
```

Recording the **location** is mandatory. A score without a pointer is an opinion;
a score with a section reference is a claim another reader can check, which is the
only thing that makes a self-score worth publishing at all.

### 3.2 Outcomes

Unlike [RB-05](rb-05-harm-review-gate.md), RB-03 produces **no pass/fail**. It
produces a profile. The reason: an instrument's adequacy depends on its tier. A
`record` may legitimately score 1 on Q1 (bindingness) because records bind
nothing; a **tier 1 governing** instrument scoring 1 on Q1 is defective.

Interpretation by authority class:

| Authority | Dimensions that must be ≥ 3 | Tolerable low |
|---|---|---|
| `governing` | Q1, Q2, Q3, Q5 | Q4 (if the inoperability is disclosed), Q6 |
| `operative-form` | Q1, Q3, Q5 | Q2, Q4 |
| `companion` | Q3, Q5 | Q1, Q2, Q4 |
| `record` | Q3, Q5 | Q1, Q2, Q4, Q6 |

Note that **Q3 (disclosure) must be ≥ 3 for every authority class.** It is the one
non-negotiable dimension in the rubric, which follows directly from
[Charter §0.8](../corpus/mx-000-charter.md).

### 3.3 Who may score

Anyone. RB-03 requires no access, no role, and no cooperation — the entire input is
published text. This is the one rubric in the corpus that a stranger can apply as
authoritatively as the curator, and that property is the answer to
[MX-017](../corpus/mx-017-conflicts-of-interest.md)'s substitute **S4**.

## 4. Worked instance — scoring a strong instrument

**[ST-01 identifier and URL grammar](../standards/st-01-identifier-and-url-grammar.md).**

| Dim | Score | Location and reasoning |
|---|---|---|
| Q1 Bindingness | **4** | Four numbered rules, imperative. Rule 2 (numbers immortal) is unambiguous and consequential |
| Q2 Falsifiability | **3** | Falsifier is outsider-runnable against published identifiers; needs a listing, not estate cooperation |
| Q3 Disclosure | **3** | Discloses the immortality doctrine's cost — it freezes early mistakes, as [MX-004 §3.1](../corpus/mx-004-terms-of-top-levels.md) shows |
| Q4 Operability | **4** | Requires only that the curator assign numbers carefully. One person suffices |
| Q5 Traceability | **4** | Nineteen prefixes, each pointing to its family |
| Q6 Proportion | **3** | Appropriate length; arguably long for a four-rule instrument |

**Profile: 4, 3, 3, 4, 4, 3.** No total. Governing-class thresholds (Q1, Q2, Q3,
Q5 ≥ 3) are met.

Why ST-01 scores well on Q4 where most of the corpus scores 1: its obligations are
discharged by **authorship**, and authorship is the estate's one available act.
Every low Q4 in the corpus marks an instrument that asked for something other than
writing.

## 5. Failure modes

| # | Failure | Mechanism | Current state |
|---|---|---|---|
| F1 | **Self-scoring inflation** | Author scores own work | **Actual** — §6; the only scores that exist are self-scores |
| F2 | **Score without location** | Opinion presented as assessment | Prohibited by §3.1 |
| F3 | **Composite creep** | A total computed because six numbers are inconvenient | Prohibited by §1.1 |
| F4 | **Tier-blind reading** | A record judged as if governing | Guarded by §3.2's table |
| F5 | **Q3 gaming** | Disclosing trivial gaps to earn the non-negotiable dimension | **Live risk.** The 3→4 step (checkability) is the only guard |
| F6 | **Rubric never applied by an outsider** | Nobody reruns it | **Actual** — §3.3 invites it; no one has |

F5 deserves naming. Because Q3 must be ≥ 3 for every authority class, there is a
standing incentive to disclose **something** rather than the **most adverse**
thing. The estate's own instruments disclose heavily, and whether they disclose
the *worst* available fact in each case is precisely what an outside scorer should
test.

## 6. The self-score

Applied by the author to a sample of its own corpus. **Treat as the interested
party's estimate** ([MX-017 C1](../corpus/mx-017-conflicts-of-interest.md));
direction of interest is toward higher marks.

| Instrument | Authority | Q1 | Q2 | Q3 | Q4 | Q5 | Q6 | Thresholds met? |
|---|---|---|---|---|---|---|---|---|
| [ST-01](../standards/st-01-identifier-and-url-grammar.md) | operative-form | 4 | 3 | 3 | 4 | 4 | 3 | Yes |
| [MX-002 terms](../corpus/mx-002-terms-of-service.md) | governing | 3 | 3 | 4 | 2 | 4 | 3 | Yes (Q4 low, disclosed) |
| [MX-003 privacy](../corpus/mx-003-privacy-notice.md) | governing | 3 | 4 | 4 | 2 | 4 | 3 | Yes |
| [MX-016 appeals](../corpus/mx-016-appeals-and-due-process.md) | governing | 3 | 2 | 3 | **1** | 4 | 3 | **Q2 fails** |
| [MX-017 conflicts](../corpus/mx-017-conflicts-of-interest.md) | governing | 2 | 3 | 4 | **1** | 4 | 3 | **Q1 fails** |
| [SITE-01 route manifest](../site/route-manifest.md) | governing | 3 | 3 | **2** | 3 | 4 | 2 | **Q3 fails** |
| [REG-05 credentials](../registries/reg-05-credential-registry.md) | record | 1 | 4 | 4 | 1 | 4 | 3 | Yes |
| [enforceability table](../license/enforceability-two-track-table.md) | companion | 2 | **1** | 2 | 2 | 3 | 3 | **Q3 fails** |

### 6.1 What the self-score shows

Four of eight fail a threshold for their authority class, **by the author's own
scoring**.

- **[MX-016](../corpus/mx-016-appeals-and-due-process.md) Q2 = 2.** Its falsifier
  cannot be run by an outsider, because whether stage 2 *would* operate is
  untestable until someone appeals. A governing instrument with an unrunnable
  falsifier is exactly what [ST-04](../standards/st-04-falsifiability-and-claim-cards.md)
  warns against.
- **[MX-017](../corpus/mx-017-conflicts-of-interest.md) Q1 = 2.** It is a governing
  instrument that mostly *describes* and *discloses*. Its four substitutes are
  stated as owed, and its own §5.1 concedes two are applied weakly. Low
  bindingness is the accurate score for an instrument whose main verb is
  "disclose".
- **[SITE-01](../site/route-manifest.md) Q3 = 2.** It enumerates 321 routes.
  [REG-02](../registries/reg-02-page-registry.md) had to supply the disclosure that
  most correspond to no written page ([DEF-032](../00-governance-map/defect-register.md)).
  **An instrument should not need a sibling to make its own adverse disclosure** —
  that is the definition of a 2 rather than a 3 on Q3.
- **[enforceability table](../license/enforceability-two-track-table.md) Q2 = 1,
  Q3 = 2.** Its central claims are legal-effect claims it cannot test, and it says
  so only in §6 rather than at the head. This corroborates from a second direction
  what [MX-005 §5](../corpus/mx-005-scope-and-boundaries.md) already published
  against itself.

**The pattern across all four failures: disclosure placed too late or too far
away.** Three of the four would move from failing to passing by relocating an
admission the estate has *already made elsewhere* to the head of the instrument
that owes it. That is a cheap, concrete, non-governance fix, and it is the most
actionable finding this rubric has produced.

## 7. Limits

1. **Every existing score is a self-score** (F1, F6). The rubric's own §3.3 says a
   stranger can apply it as well as the curator; no stranger has.
2. **Eight instruments of ~80 scored.** A 10% sample chosen by the author.
3. **The 0–4 anchors are qualitative.** Two scorers will differ by a point;
   nothing calibrates them. No inter-rater agreement has been measured because
   there has only ever been one rater.
4. **Q6 (proportion) is the weakest dimension** and close to taste. It is retained
   because length inflation is a real fault in this corpus, and removed honesty
   would be worse than a soft dimension.
5. **No Arabic text**, while `prevailing_text: ar`.
6. **This rubric scored by this rubric** would take roughly Q1 3, Q2 4, Q3 3,
   Q4 4, Q5 4, Q6 3 — and that estimate has exactly the reliability §6's preamble
   warns of.

## 8. Falsifier

> **IF FALSE.** This rubric is falsified if:
>
> - **(a)** an outside scorer, applying §2 to any instrument in §6, differs from
>   the self-score by **two or more points on any dimension** — which would show
>   either the anchors are not usable or the self-score is inflated;
> - **(b)** an instrument is shown to be plainly good while scoring ≤ 1 on three
>   or more dimensions, or plainly bad while scoring ≥ 3 on all six;
> - **(c)** a total score appears anywhere in the corpus alongside RB-03 output;
> - **(d)** a score is published without a location (§3.1);
> - **(e)** Q3 ≥ 3 is awarded to an instrument that discloses only trivial gaps
>   while a material one is known (F5).
>
> **(a) is the test that matters and only a stranger can run it.** The estate has
> published its own marks specifically so that disagreement is possible; a rubric
> whose results were never published could never be contradicted.

## 9. Obligation

**On a scorer:**
- Read the instrument in full; never score from a summary
  ([GM-01 §3](../00-governance-map/precedence-and-conflict-rules.md)).
- Record a **location** with every score (§3.1).
- Report six numbers. **Never a total** (§1.1).
- Judge Q4 against the parties that exist, not ideal ones (§2.2).
- Read thresholds by authority class, not uniformly (§3.2).

**On the estate:**
- Publish its self-scores including the failures (§6 does).
- **Relocate late disclosures to the head of the instruments that owe them** —
  the §6.1 finding, and the cheapest quality improvement available.
- Invite and publish outside scores unchanged, including scores worse than its own.
- Never award Q3 ≥ 3 to itself for disclosing the easy gap (F5).

---

### Related

**Sibling rubrics** — [RB-01](rb-01-d1-d5-rubric.md) ·
[RB-02](rb-02-proof-ladder.md) · [RB-04](rb-04-reader-comprehension-rubric.md) ·
[RB-05](rb-05-harm-review-gate.md)

**What is being scored against** — [ST-24](../standards/st-24-page-prose-standard.md) ·
[SITE-02](../site/page-contract.md) · [ST-04](../standards/st-04-falsifiability-and-claim-cards.md) ·
[ST-07](../standards/st-07-evidence-and-verify.md)

**Why Q4 scores low** — [DEF-031](../00-governance-map/defect-register.md) ·
[REG-08](../registries/reg-08-role-and-authority-registry.md) ·
[MX-016](../corpus/mx-016-appeals-and-due-process.md) ·
[MX-005 Annex A](../corpus/mx-005-scope-and-boundaries.md)

**The conflict in self-scoring** — [MX-017](../corpus/mx-017-conflicts-of-interest.md) ·
[ST-06](../standards/st-06-objections-standard.md) ·
[REG-07](../registries/reg-07-defect-classification-registry.md) ·
[GM-08 verification log](../00-governance-map/verification-log.md)

### Exit pair

1. **Disagree with a number.** Pick one row of [§6](#6-the-self-score), read the
   instrument, and score it yourself. Falsifier §8(a) needs a stranger and the
   estate cannot run it.
2. **Fix the cheap thing.** [§6.1](#61-what-the-self-score-shows) — three of four
   failures resolve by moving an existing admission to the top of the page.

<!-- mx-pagestamp: RB-03 · v2026.10.1 · operative-form · tier 5 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; all scores recorded here are self-scores -->
