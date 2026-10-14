---
doc_id: ST-17
title_en: Worked Instance Standard
title_ar: معيار المثال المُعالَج
family: standards
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
domain_tags: [worked-instance, examples, method, falsifiability, standards]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. This standard was written after the practice it describes had already produced four discovered defects, listed in §5.
route: /standards/st-17/
---

# ST-17 — Worked Instance Standard

> **Authority.** `operative-form`, tier 5. Governs the fourth part of
> [ST-24](st-24-page-prose-standard.md)'s eight-part recipe — the **worked
> instance** — which is the part that most often decides whether a page is worth
> anything.

> **Disclosure first.** This standard codifies a practice that was already running
> and had already paid. Writing worked instances in this corpus has surfaced at
> least **four defects that design alone had missed** — a missing link check
> (ST-08 L6), an incomplete rule (ST-15 A1), an undesigned dependency between two
> standards (ST-16 U7 × ST-09), and a governing-instrument overclaim
> (MX-018 §6 → MX-005). §5 lists them. That record is the whole argument for this
> standard, and it is the argument that a purely deductive corpus cannot make.

---

## 1. Position

Eight parts make a page under [ST-24](st-24-page-prose-standard.md): Position,
Definition, Mechanism, Worked instance, Failure modes, Limits, Falsifier,
Obligation. Seven of them can be written from the author's intentions. **The
worked instance cannot.**

That asymmetry is the reason it earns its own standard. A definition can be
elegant and empty; a mechanism can be specified and inoperable. A worked instance
**runs the mechanism on a real case and reports where it stops** — and because the
case is real, it can refuse to cooperate.

> **The test of a worked instance: it must be capable of embarrassing the
> instrument that contains it.**

An example that could only ever confirm the rule is not a worked instance. It is
an illustration, and illustrations are decoration.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **worked instance** | An application of the instrument's mechanism to a specific case, traced to its end, including failure |
| **illustration** | An example chosen because it works — **not** a worked instance |
| **terminal state** | Where the trace stops: a result, or an identified blockage |
| **blockage** | A point where the mechanism cannot proceed with available resources |
| **counter-instance** | A second case chosen because it fails where the first succeeded |
| **discovered defect** | A fault in the instrument found by working the instance |

### 2.1 Illustration vs worked instance

| | Illustration | Worked instance |
|---|---|---|
| Case chosen | Because it works | Because it is representative, or because it is hard |
| Outcome | Known before writing | **Not** known before writing |
| Can it fail? | No | **Yes, and often does** |
| Value | Clarifies | **Tests** |
| Length | Short | As long as the trace requires |

A reader can tell the two apart by one question: *did the author learn anything?*
If the instance ends exactly where the mechanism predicted, with no residue, it is
probably an illustration.

## 3. The six requirements

Cumulative. A worked instance failing any one is non-compliant.

| # | Requirement | Why |
|---|---|---|
| **W1** | **Specific.** Named instrument, named provision, named facts. Never "suppose a user" with no user | Generality is how an example avoids testing anything |
| **W2** | **Traced to a terminal state.** Every step shown, including the one that fails | A trace that stops at the first success proves nothing about the rest |
| **W3** | **Tabulated where it has steps.** A step table with a status column per step | Makes the blockage visible rather than narrated away |
| **W4** | **Honest about the terminal state.** If it is a blockage, say so; if `indeterminate`, say so | [ST-07](st-07-evidence-and-verify.md) — an outcome stated more definitely than the trace supports is an overclaim |
| **W5** | **A counter-instance where the first case succeeds.** If the mechanism worked, show a case where it does not | Otherwise the instance is an illustration (§2.1) |
| **W6** | **Discovered defects filed, not fixed in place.** If working the instance exposes a fault, file it | [Charter §0.8](../corpus/mx-000-charter.md); a silent fix conceals the discovery |

### 3.1 W5 is the anti-illustration rule

When a mechanism works on the chosen case, the author has learned nothing and the
reader has been shown nothing. W5 requires a second case that fails.

[REG-01 §4](../registries/reg-01-series-registry.md) does this: the `S1` trace
works (two of nine items, arithmetic checkable), so a counter-instance follows —
`S3`, a series number burnt by a careless citation with no series behind it. The
second case carries the instructive content.

### 3.2 W6 and the discovery duty

A worked instance that exposes a fault presents a temptation: quietly repair the
instrument and publish a clean example. That is a silent edit of the worst kind,
because it also erases the evidence that the design was wrong.

W6 requires the opposite: **publish the instance that broke, state what it broke,
and file it.** [ST-15 §5](st-15-amendment-and-versioning-standard.md) does this —
the HX-000 trace exposed that rule A1 conflated version-suffixing with path
correction, and the standard states the clarification **and** records that it was
discovered in the writing, in the same act as first publication.

## 4. Mechanism

### 4.1 Writing one

```
1. choose a case: representative, or the hardest available
   — do NOT choose it because you know it works (§2.1)
2. list the mechanism's steps from the instrument's own §3/§4
3. trace each step; record status per step (W3)
4. reach a terminal state; name it honestly (W2, W4)
5. if the case succeeded → find a counter-instance (W5)
6. if the trace exposed a fault in the instrument → file it (W6)
7. state what the reader should take from it
```

Step 1 is where the standard is won or lost. Step 6 is where it pays.

### 4.2 The three terminal states

| Terminal state | Meaning | Must be labelled |
|---|---|---|
| **result** | The mechanism completed and produced an outcome | Yes |
| **blockage** | The mechanism stopped for want of a resource or a party | **Yes, with the resource named** |
| **indeterminate** | The mechanism completed and the outcome cannot be determined | **Yes, with the reason** |

`blockage` and `indeterminate` are the most common terminal states in this corpus
and the most useful. [MX-002 §8](../corpus/mx-002-terms-of-service.md) traces a
trainer's reuse question to `indeterminate` — because three Scale Gate thresholds
are unpublished — and names the estate as the cause. An instance that had returned
a confident permission would have contradicted the tier 1 instrument.

### 4.3 Where a blockage recurs

When several worked instances across different instruments hit the **same**
blockage, that is a structural finding, not a coincidence. The corpus has one:
instances in [REG-05](../registries/reg-05-credential-registry.md),
[RB-05](../rubrics/rb-05-harm-review-gate.md),
[MX-016](../corpus/mx-016-appeals-and-due-process.md) and
[MX-017](../corpus/mx-017-conflicts-of-interest.md) all terminate at the same
resource: **a second person**. That convergence is what produced
[DEF-031](../00-governance-map/defect-register.md), and it was visible only because
each instance was traced to its blockage rather than abandoned at the first
difficulty.

## 5. Worked instance

**This standard, applied to itself — with the corpus's discovery record as the
case.**

W1 requires specificity, so the case is: *did working instances in this corpus
actually discover defects that design missed?* Four candidates:

| # | Instrument | What the instance exposed | Terminal state | Filed? |
|---|---|---|---|---|
| 1 | [ST-08 §5](st-08-cross-reference-and-link-integrity.md) | L1 tests **existence**, not **identity**; the ML-2.3 §A.10 → HX-000 reference passes L1 while incorporating a mis-titled draft. Check **L6** did not exist | `blockage` → new check specified | Yes — L6 added in §5.1 |
| 2 | [ST-15 §5](st-15-amendment-and-versioning-standard.md) | Rule A1 conflated version-suffixed paths (forbidden) with correcting a path stating a false fact (required) | `result` + rule gap | Yes — A1 clarified in-text |
| 3 | [ST-16 §5](st-16-audience-tier-standard.md) | U7 cannot be discharged without [ST-09](st-09-summary-and-abstract-standard.md) S1–S5; two independently written standards are dependent | `result` + undesigned dependency | Yes — U7 completed in §5.1 |
| 4 | [MX-018 §6](../corpus/mx-018-third-party-dependencies.md) | [MX-005 §2](../corpus/mx-005-scope-and-boundaries.md) claims authorship as the estate's **capability**; it is a **service received from a dependency**. Class DC-3 overclaim on a governing instrument | `result` + governing-instrument defect | Yes — filed, not silently edited |

**Terminal state: result.** Four of four traced instances produced a discovered
defect. The practice pays.

### 5.1 The counter-instance W5 demands

The trace above succeeded, so W5 requires a case where working an instance
discovered **nothing**.

[ST-01 §4 as scored in RB-03](../rubrics/rb-03-instrument-quality-rubric.md) is
one. The identifier-grammar standard's worked instance applies four rules to a
straightforward case, they apply cleanly, and nothing is exposed. ST-01 scored 4,
3, 3, 4, 4, 3 — the corpus's strongest profile — and its instance taught the author
nothing.

**Why:** ST-01's obligations are discharged by authorship alone, and authorship is
the estate's one available act. Mechanisms that need only the author to act do not
blockage, so their instances cannot surprise. The productive instances are the ones
whose mechanisms need a **second party, a runner, or a published number** — exactly
the three things the estate lacks.

### 5.2 What follows, and what does not

**Follows:** the worked-instance requirement should be **most strictly enforced on
instruments whose mechanisms require resources the estate does not have**, because
that is where instances find things.

**Does not follow:** that the practice is validated generally. Four discoveries in
roughly eighty instruments is not a rate, the instances were written by the same
author as the instruments, and an author who writes an instance may notice a fault
they would have noticed on rereading anyway. The claim *"worked instances find
defects design misses"* is **E1** under
[ST-07](st-07-evidence-and-verify.md) — checkable in the record, not
experimentally established. No control condition exists and none can be
constructed by one author.

## 6. Failure modes

| # | Failure | Mechanism | Current state |
|---|---|---|---|
| F1 | **Illustration passed as instance** | Case chosen because it works | Guarded by W5; the commonest failure in technical writing |
| F2 | **Trace abandoned at first difficulty** | Blockage is unflattering | Guarded by W2; **the failure that would have hidden DEF-031** |
| F3 | **Terminal state overstated** | `indeterminate` reported as a result | Guarded by W4, [ST-07](st-07-evidence-and-verify.md) |
| F4 | **Discovered defect silently fixed** | Cleaner page | Prohibited by W6; **unverifiable from outside** |
| F5 | **Hypothetical facts** | "Suppose a user…" | Guarded by W1 |
| F6 | **Instance longer than the instrument** | Enthusiasm | Not prohibited; a long instance on a short rule is a signal the rule is under-specified |
| F7 | **Convergent blockage unnoticed** | Each instance read alone | Guarded by §4.3; noticed once |

F4 is the one a reader cannot check. A silently repaired instrument and a
well-designed one look identical. The only defence is the corpus's habit of
recording discoveries in-text, and that habit is self-administered
([MX-017](../corpus/mx-017-conflicts-of-interest.md)).

## 7. Limits

1. **The central claim is E1** (§5.2): the discovery record is real, the causal
   claim is not established.
2. **No control.** One author wrote both the instruments and the instances; the
   counterfactual — what design alone would have caught — is unavailable.
3. **F4 is unverifiable** from outside.
4. **W5 is unevenly applied.** Several instruments in this corpus have a successful
   instance and no counter-instance, and are therefore non-compliant with their own
   standard.
5. **Four discoveries are not a rate** over ~80 instruments; most instances
   discovered nothing, and §5.1 explains why without excusing it.
6. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** This standard is falsified if:
>
> - **(a)** a worked instance is shown to have been chosen because its outcome was
>   known — the definition of an illustration (§2.1);
> - **(b)** a trace stops before its terminal state (W2);
> - **(c)** a terminal state is labelled `result` where the trace supports only
>   `indeterminate` or `blockage` (W4);
> - **(d)** a fault discovered while working an instance was repaired without a
>   record (W6) — **unverifiable, and the estate says so**;
> - **(e)** an instrument's instance succeeds with no counter-instance (W5) —
>   **fires now**, in several places (§7.4);
> - **(f)** the four discoveries in §5 are shown to have been findable by rereading
>   alone — which would falsify §5.2's E1 claim and reduce this standard to a style
>   preference.
>
> **(f) is the honest test of the standard's value and cannot be run without a
> second author.** It is published as the thing that would defeat this instrument,
> rather than omitted because it is unanswerable.

## 9. Obligation

**On an author:**
- Choose the case **before** knowing whether it works (§4.1 step 1).
- Trace to a terminal state and **name** it: result, blockage, or indeterminate
  (W2, W4, §4.2).
- Tabulate steps with a per-step status (W3).
- Add a **counter-instance** whenever the first case succeeds (W5).
- **File** what the instance discovers; never repair silently (W6,
  [Charter §0.8](../corpus/mx-000-charter.md)).
- Name the resource when the terminal state is a blockage — convergent blockages
  are structural findings (§4.3).
- Write the instance most carefully on instruments whose mechanisms need
  resources the estate lacks (§5.2).

**On the estate:**
- Supply counter-instances to the instruments currently missing them (§7.4).
- Keep the central claim labelled **E1**; do not promote it (§5.2).
- Record convergent blockages as single structural defects rather than many small
  ones — as [DEF-031](../00-governance-map/defect-register.md) does.

---

### Related

**The recipe this part belongs to** — [ST-24](st-24-page-prose-standard.md) ·
[SITE-02](../site/page-contract.md) ·
[ST-16](st-16-audience-tier-standard.md) ·
[ST-09](st-09-summary-and-abstract-standard.md)

**Honesty about outcomes** — [ST-07](st-07-evidence-and-verify.md) ·
[ST-04](st-04-falsifiability-and-claim-cards.md) ·
[ST-06](st-06-objections-standard.md) ·
[ST-03 limits and bridge](st-03-limits-and-bridge.md)

**The four discoveries** — [ST-08](st-08-cross-reference-and-link-integrity.md) ·
[ST-15](st-15-amendment-and-versioning-standard.md) ·
[MX-018](../corpus/mx-018-third-party-dependencies.md) ·
[MX-005](../corpus/mx-005-scope-and-boundaries.md)

**Convergent blockage** — [DEF-031](../00-governance-map/defect-register.md) ·
[REG-08](../registries/reg-08-role-and-authority-registry.md) ·
[REG-05](../registries/reg-05-credential-registry.md) ·
[MX-016](../corpus/mx-016-appeals-and-due-process.md)

### Exit pair

1. **Find an illustration.** Pick any worked instance in this corpus and ask
   whether the author could have known the outcome first. Falsifier §8(a) is yours.
2. **Read a productive blockage.**
   [MX-002 §8](../corpus/mx-002-terms-of-service.md) — a reuse question traced to
   `indeterminate` because the estate withheld three numbers.

<!-- mx-pagestamp: ST-17 · v2026.10.1 · operative-form · tier 5 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; several instruments lack the counter-instance this standard requires -->
