---
doc_id: BX-005
title_en: The Phase Audit Method
title_ar: منهج تدقيق المراحل
family: bcia
version: v2026.10.1
status: published
authority: operative-form
prevailing_text: ar
audience_tier: 3
depth: micro
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [bcia, audit, method, sixteen-questions, diagnostic]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000, class I-1, resting on gap 1. The method has been applied to four pages, all chosen by the system that wrote them.
route: /bcia/audit/
---

# BX-005 — The Phase Audit Method

> **This page will not resolve:** whether a phase audit predicts anything about
> real readers. It is a diagnostic for authors, validated against no reader
> ([§7.1](#7-limits)).

> **Authority.** `operative-form`, tier 5. Unlike
> [BX-001](bx-001-before-phase.md)–[BX-004](bx-004-after-phase.md), which are
> companions, this supplies a **form for judging**. It still creates no duty —
> phase obligations are discharged by the standards named in
> [BX-000 §4.2](bx-000-bcia-charter.md).

> **Disclosure first.** In four applications
> ([BX-001 §5](bx-001-before-phase.md)–[BX-004 §5](bx-004-after-phase.md)) this
> method produced **four findings, each naming a free remedy that had never been
> adopted**. That is a strong result and a suspicious one: a diagnostic applied by
> its own author to its own corpus, finding problems with cheap fixes, is exactly
> what motivated reasoning produces. §5 tests whether the findings survive a
> harder case.

---

## 1. Position

[BX-000](bx-000-bcia-charter.md) establishes four phases.
[BX-001](bx-001-before-phase.md)–[BX-004](bx-004-after-phase.md) describe each.
This instrument turns them into **sixteen questions** an author can run against a
page in under ten minutes.

Why a separate instrument rather than a section of the charter: the audit is the
only part of BCIA that **does** something, and burying an operative form inside a
descriptive charter is the error
[MX-004 §2.2](../corpus/mx-004-terms-of-top-levels.md)'s tie-break rules exist to
prevent — *duty beats description*.

### 1.1 What the audit is for

**Not** for scoring pages. [RB-03](../rubrics/rb-03-instrument-quality-rubric.md)
does that, on six dimensions, with its own anchors and thresholds.

The phase audit is **diagnostic**: it tells an author *which phase a page fails*,
so the right standard can be applied. A page scoring poorly on
[RB-03](../rubrics/rb-03-instrument-quality-rubric.md) Q3 (disclosure) might fail
at phase B (the disclosure is late) or phase A (the disclosure is unreachable
afterwards) — different remedies, same score.

## 2. The sixteen questions

Four per phase. Each answerable **yes / partly / no** by reading the page.

### Before

| # | Question |
|---|---|
| **B-i** | Can a reader tell in 30 seconds whether this is their page? |
| **B-ii** | Is the audience visible **in the rendered page**, not only in front matter? |
| **B-iii** | Is the authority class stated before any substance? |
| **B-iv** | Does the opening say what the page will **not** resolve? |

### Contact

| # | Question |
|---|---|
| **C-i** | Are all eight [ST-24](../standards/st-24-page-prose-standard.md) parts present? |
| **C-ii** | Does the worked instance **trace**, or merely illustrate? |
| **C-iii** | Are Failure modes and Limits **adverse**, or decorative? |
| **C-iv** | Is the terminal state **visually prominent** (tabulated or bolded)? |

### Internalisation

| # | Question |
|---|---|
| **I-i** | Is there a concrete case to attach the abstraction to? |
| **I-ii** | Is the boundary stated early enough to be reached? |
| **I-iii** | Does the page offer **one or two** relations for integration, or eight? |
| **I-iv** | Does the exit pair offer a **transfer**, or only a reference? |

### After

| # | Question |
|---|---|
| **A-i** | Is the obligation actionable without re-reading? |
| **A-ii** | Is the falsifier runnable by an outsider? |
| **A-iii** | Can currency be determined unaided (version + next review date)? |
| **A-iv** | Does the page link the defects filed against it? |

### 2.1 Four questions encode findings from the phase documents

| Question | Source finding |
|---|---|
| **B-iv** | [BX-001/1](bx-001-before-phase.md) — one line saying what the page will not resolve |
| **C-iv** | [BX-002/1](bx-002-contact-phase.md) — terminal state must be scan-visible |
| **I-iii** | [BX-003/1](bx-003-internalisation-phase.md) — two integrates, eight fragments |
| **A-iv** | [BX-004/1](bx-004-after-phase.md) — P1, instruments linking their own defects |

None of the four is required by any standard. All four are **free**. That
convergence is either the method working or the method being fitted to its own
findings, and §5 is written to distinguish them.

## 3. Mechanism

### 3.1 Running an audit

```
read the page ONCE, normally
for each of the 16: answer yes / partly / no
report FOUR profiles — one per phase. Never a total
the phase with the most 'no' answers names the remedy's home
```

**No total**, inherited from [RB-01 §1.1](../rubrics/rb-01-d1-d5-rubric.md): a
composite would let a strong Contact score conceal a failed Before, which is the
exact failure [BX-001 §5](bx-001-before-phase.md) traced.

### 3.2 Reading the result

| Pattern | Diagnosis |
|---|---|
| B weak, C/I/A strong | **Phase-blind page** — good content nobody can find their way into |
| C weak, others strong | Form failure — apply [ST-24](../standards/st-24-page-prose-standard.md) |
| I weak | Too many relations, or no concrete case |
| A weak | Unreachable after reading; usually A-iv |
| All weak | The page should probably not exist |

## 4. Worked instance — the easy case

**Auditing [BX-002](bx-002-contact-phase.md), which was written after the findings
existed.**

| Phase | i | ii | iii | iv | Profile |
|---|---|---|---|---|---|
| **B** | partly | no | yes | **yes** | 1 yes, 1 partly, 2 no |
| **C** | yes | yes | yes | **yes** | 4 yes |
| **I** | yes | partly | **no** (16 links) | yes | 2 yes |
| **A** | yes | yes | yes | **no** | 3 yes |

A page written by an author who knew the sixteen questions still answers **no** to
I-iii and A-iv — because both are governed by
[ST-18](../standards/st-18-related-blocks-and-exit-pairs.md)'s eight-link floor and
the omitted faults group, which the author complied with rather than overrode.

That is mildly reassuring: the audit is not simply confirming the author's
intentions.

## 5. Worked instance — the hard case

**Auditing an instrument written long before BCIA existed:
[ST-01 identifier and URL grammar](../standards/st-01-identifier-and-url-grammar.md).**

Chosen because [RB-03 §6](../rubrics/rb-03-instrument-quality-rubric.md) scored it
the corpus's **strongest** profile (4,3,3,4,4,3), and
[ST-17 §5.1](../standards/st-17-worked-instance-standard.md) recorded that its
worked instance **taught the author nothing**. If the phase audit is merely
motivated reasoning, it should find little here too.

| Phase | Question | Answer |
|---|---|---|
| **B** | B-i my page? | **partly** — title names the subject; opening is a precedence note |
| | B-ii audience visible? | **no** — front matter only |
| | B-iii authority stated? | **yes** |
| | B-iv what it won't resolve? | **no** |
| **C** | C-i eight parts? | **yes** |
| | C-ii traces? | **partly** — four rules applied cleanly; nothing stressed |
| | C-iii adverse limits? | **yes** — discloses that immortality freezes early mistakes |
| | C-iv terminal state prominent? | **no** — no blockage to make prominent |
| **I** | I-i concrete case? | **yes** |
| | I-ii boundary early? | **no** — Limits at §7 |
| | I-iii one or two relations? | **no** — eight |
| | I-iv transfer? | **partly** |
| **A** | A-i actionable? | **yes** |
| | A-ii outsider-runnable falsifier? | **yes** |
| | A-iii currency unaided? | **yes** |
| | A-iv links its defects? | **no** |

**Profiles: B 1/4 · C 2/4 · I 1/4 · A 3/4.**

**Terminal state: `result` — the corpus's strongest instrument scores 1 of 4 at
Before and 1 of 4 at Internalisation.**

### 5.1 The finding

[RB-03](../rubrics/rb-03-instrument-quality-rubric.md) rated ST-01 the best
instrument in the corpus. The phase audit rates it **weak at two of four phases**.

Both are right, and the divergence is the useful output.
[RB-03](../rubrics/rb-03-instrument-quality-rubric.md)'s six dimensions —
bindingness, falsifiability, disclosure, operability, traceability, proportion —
are **all properties of the text as an instrument**. Every one is a Contact-and-After
property. **RB-03 has no dimension that measures Before or Internalisation at all.**

So the corpus's quality rubric is **structurally blind to half the phases**, and
scored its best page highly while that page was failing at arrival and integration.

That is not a criticism of [RB-03](../rubrics/rb-03-instrument-quality-rubric.md) —
it measures what it claims to. It is a finding about the estate's assessment
coverage: **every quality instrument the estate owns measures the two phases the
eight-part recipe already serves, and none measures the two it does not.**

Filed per [ST-17 W6](../standards/st-17-worked-instance-standard.md):

> **Finding BX-005/1.** [RB-03](../rubrics/rb-03-instrument-quality-rubric.md)'s six
> dimensions measure phases C and A only. The estate has no quality measure for
> phases B and I, which is why
> [BX-000 §5.1](bx-000-bcia-charter.md)'s systemic phase B weakness went unnoticed
> across ~80 instruments despite a quality rubric being applied. Either RB-03
> should gain two dimensions, or the phase audit should be run alongside it as
> standard practice. Filed as a ratification question.

This answers §1's suspicion. The method was **not** merely fitted to its own
findings: applied to the page most likely to defeat it, it produced a result that
contradicts the estate's existing quality assessment and explains a documented
blind spot.

## 6. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Audit used as a score** | Prohibited by §3.1 — four profiles, no total |
| F2 | **Author audits own page** | **Actual ×5**; §5 chose a hostile case as partial mitigation |
| F3 | **Questions fitted to findings** | **Tested in §5** and survived |
| F4 | **Partly used to avoid a no** | Unguarded; the anchors are coarse |
| F5 | **Phase blind spot in the quality rubric** | **Actual** — §5.1 |
| F6 | **Audit never run by anyone else** | **Actual** |

## 7. Limits

1. **No reader has validated any phase claim.** The whole method is **E0**
   ([REG-06](../registries/reg-06-dataset-registry.md)).
2. **Five audits exist, all self-audits** — one per phase document plus §5.
3. **yes / partly / no is coarse** and "partly" absorbs disagreement (F4).
4. **Four questions per phase is arbitrary**, chosen for symmetry.
5. **Written by the system that wrote the pages being audited**
   ([MX-017 C1](../corpus/mx-017-conflicts-of-interest.md)).
6. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** an outside auditor differs from a published profile on **four or more**
>   of the sixteen questions — which would show the anchors unusable;
> - **(b)** a page auditing strongly across all four phases is shown to serve
>   readers badly;
> - **(c)** §5.1 is wrong — [RB-03](../rubrics/rb-03-instrument-quality-rubric.md)
>   is shown to have a dimension measuring Before or Internalisation. **Checkable in
>   two minutes** against RB-03 §2;
> - **(d)** a seventeenth question is identified that none of the sixteen covers;
> - **(e)** the four free remedies (B-iv, C-iv, I-iii, A-iv) are shown to require
>   permission or amendment — which would defeat §2.1's claim that they are free.
>
> **(c) is the sharpest and cheapest.** If RB-03 does measure those phases, §5.1's
> finding collapses and this instrument's main contribution with it.

## 9. Obligation

**On an author (form, not duty):**
- Run all sixteen; report **four profiles, never a total** (§3.1).
- Read the page once, normally, before answering (§3.1).
- Use the phase with the most `no` answers to locate the remedy (§3.2).
- Prefer a hostile case when auditing your own work (F2, §5).

**On the estate:**
- File **BX-005/1**: RB-03 measures phases C and A only (§5.1).
- Adopt the four free remedies — B-iv, C-iv, I-iii, A-iv — which no standard
  forbids (§2.1, §8e).
- Run falsifier §8(c) first; it takes two minutes and could invalidate §5.1.
- Have someone other than the author run one audit (F6).

---

### Related

**The phases this audits** — [BX-000](bx-000-bcia-charter.md) ·
[BX-001](bx-001-before-phase.md) · [BX-002](bx-002-contact-phase.md) ·
[BX-003](bx-003-internalisation-phase.md)

**Assessment instruments this sits beside** —
[RB-03](../rubrics/rb-03-instrument-quality-rubric.md) ·
[RB-04](../rubrics/rb-04-reader-comprehension-rubric.md) ·
[RB-01](../rubrics/rb-01-d1-d5-rubric.md) ·
[RB-05](../rubrics/rb-05-harm-review-gate.md)

**Standards the questions test** —
[ST-24](../standards/st-24-page-prose-standard.md) ·
[ST-17](../standards/st-17-worked-instance-standard.md) ·
[ST-18](../standards/st-18-related-blocks-and-exit-pairs.md) ·
[ST-16](../standards/st-16-audience-tier-standard.md)

**Where its faults are recorded** —
[defect register](../00-governance-map/defect-register.md) ·
[REG-07](../registries/reg-07-defect-classification-registry.md) ·
[open questions](../00-governance-map/open-questions-and-ratifications.md) ·
[BX-004](bx-004-after-phase.md)

### Exit pair

1. **Try to break §5.1 in two minutes.** Falsifier §8(c) — open
   [RB-03 §2](../rubrics/rb-03-instrument-quality-rubric.md) and look for a
   dimension measuring arrival or integration. If one exists, this page's main
   finding is wrong.
2. **Audit the corpus's best page yourself.**
   [ST-01](../standards/st-01-identifier-and-url-grammar.md) — §5 says it scores 1
   of 4 at Before. See whether you agree.

<!-- mx-pagestamp: BX-005 · v2026.10.1 · operative-form · tier 5 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; all five existing phase audits are self-audits -->
