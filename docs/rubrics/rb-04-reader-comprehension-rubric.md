---
doc_id: RB-04
title_en: Reader Comprehension Rubric
title_ar: مقياس فهم القارئ
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
domain_tags: [rubric, comprehension, reader, self-assessment, understanding]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. The rubric is designed to be run by a reader on themselves, because the estate has refused the means of running it on readers.
route: /rubrics/rb-04/
---

# RB-04 — Reader Comprehension Rubric

> **Authority.** `operative-form`, tier 5. A form for a reader to judge **their
> own** understanding. It grades nobody, records nothing, and is not used for any
> credential ([REG-05](../registries/reg-05-credential-registry.md)).

> **Disclosure first.** This rubric exists in an unusual shape because of a
> refusal. The estate cannot measure whether readers understand anything — that
> would require per-reader instrumentation, refused by
> [MX-023](../corpus/mx-023-attention-and-human-sovereignty.md) and recorded as
> a declined dataset at
> [REG-06 `DSET-R01`](../registries/reg-06-dataset-registry.md). So the rubric is
> handed to the reader instead. **The estate will never see your result**, which
> means this instrument is honest about comprehension and useless as evidence
> about it.

---

## 1. Position

The corpus rests on a premise stated in
[BK-01's thesis](../registries/reg-03-book-registry.md): *a reader owes themselves
comprehension before reliance.* Every eight-part page in this estate is built to
support that — Position, Definition, Mechanism, Worked instance, Failure modes,
Limits, Falsifier, Obligation, in that discipline, per
[ST-24](../standards/st-24-page-prose-standard.md).

But "understanding before use" is only a slogan unless a reader has a way to tell
whether they have understood. Most readers cannot, reliably: the feeling of having
understood a well-written page is nearly indistinguishable from having understood
it. This rubric exists to separate the two, and it does so by asking for
**productions**, not recognitions.

### 1.1 Recognition is not comprehension

| Feels like understanding | Actually tests understanding |
|---|---|
| The page was clear | You can state its obligation without looking |
| You agreed with it | You can state the strongest objection to it |
| You remember the structure | You can say what would falsify it |
| You could find it again | You can say what it does **not** cover |
| You could quote it | You can apply it to a case it does not mention |

The right column is what §2 scores. Each item requires the reader to **produce**
something; none can be satisfied by a feeling of fluency.

## 2. Definition

Five dimensions, each 0–4, each reported separately. **No total** — inherited from
[RB-01 §1.1](rb-01-d1-d5-rubric.md) and for the same reason: a composite would let
recall mask an inability to apply.

| Dim | Name | The production it demands |
|---|---|---|
| **C1** | **Obligation** | State what the instrument requires, and of whom, without re-reading |
| **C2** | **Boundary** | State two things it does **not** cover |
| **C3** | **Falsifier** | State what observation would show it wrong |
| **C4** | **Objection** | State the strongest argument against it, as its opponent would |
| **C5** | **Transfer** | Apply it to a case the instrument does not discuss, and say what follows |

### 2.1 The scale

| Score | Meaning |
|---|---|
| **0** | Cannot produce it |
| **1** | Can produce it only by re-reading and copying |
| **2** | Can produce it in substance, with a material error |
| **3** | Can produce it accurately from memory |
| **4** | Can produce it accurately **and** say why the instrument chose that way over an alternative |

The **1 is important**: copying from an open page is a real and low score. Most
readers who feel they have understood a governance document are at 1 on C1 and at
0 on C3–C5, and would report themselves as "understood it".

### 2.2 C4 is the discriminating dimension

Any attentive reader can reach 3 on C1. **C4 — stating the strongest objection as
its opponent would — is where comprehension is actually tested**, because it
requires holding the instrument's reasoning firmly enough to see where it gives
way.

It is also the dimension this corpus is best equipped to support, because
[ST-06](../standards/st-06-objections-standard.md) requires instruments to file
their own strongest objections as `open`, and several do:
[MX-005 §5](../corpus/mx-005-scope-and-boundaries.md),
[REG-06 §5.1](../registries/reg-06-dataset-registry.md),
[MX-011 §9.3](../corpus/mx-011-security-and-disclosure.md). A reader can check
their C4 answer against the estate's own published adverse case.

## 3. Mechanism

### 3.1 How to run it

```
read the instrument once, normally
CLOSE it
for C1..C5: write your answer, in your own words, on paper or in a file
NOW reopen the instrument
compare; score yourself 0..4 against §2.1
report NOTHING to anyone
```

The close-then-produce order is the whole method. Scoring with the page open
measures reading, not comprehension.

### 3.2 What to do with a low score

| Low dimension | What it usually means | What helps |
|---|---|---|
| **C1** | You read the reasoning and skipped §9 | Read the Obligation section first next time |
| **C2** | You absorbed the claims and not the limits | Read the Limits section; in this corpus it is always present and always adverse |
| **C3** | You treated the text as information, not as a claim | Read the Falsifier; every instrument here has one |
| **C4** | You agreed too early | Find the estate's own `open` objection ([ST-06](../standards/st-06-objections-standard.md)) |
| **C5** | You learned the instrument, not the principle | Try the instrument's own Worked instance on different facts |

### 3.3 The rubric is never used on a person by anyone else

Stated as a prohibition, not a preference:

- It produces **no credential** ([REG-05 §2.1](../registries/reg-05-credential-registry.md)
  refuses completion-without-demonstration and ranking).
- It generates **no record** the estate holds
  ([REG-06](../registries/reg-06-dataset-registry.md)).
- It must **never** be used to rank readers against each other — cohort ranking
  drives the stratum I harms in
  [HX-000](../harms/hx-000-the-fourteen-structural-harms.md).
- It must **never** be gamified into progress markers, streaks, or badges
  ([MX-023](../corpus/mx-023-attention-and-human-sovereignty.md)).

## 4. Worked instance

**A reader runs RB-04 on [MX-003 privacy notice](../corpus/mx-003-privacy-notice.md).**

They read it once, close it, and write:

| Dim | Their answer | Score | Why |
|---|---|---|---|
| **C1** Obligation | "The estate must not add analytics, and must audit its hosting layer and publish the result." | **3** | Accurate from memory; both limbs of §12 |
| **C2** Boundary | "It doesn't cover the hosting provider's own logs, and it doesn't promise the estate can notify you of corrections." | **4** | Both correct, and the second is the *adverse* one — §5's costliest admission |
| **C3** Falsifier | "If there were a cookie or a tracking script." | **2** | Correct but incomplete: they missed §10(e), third-party requests, which is the one the estate flags as most likely to fire |
| **C4** Objection | "Refusing analytics means they can't tell if anyone reads it." | **2** | This is the estate's own §5 admission, restated — **not** the strongest objection. The stronger one is in §5: *the refusal to hold an address list means a reader who relied on a corrected document can never be told*, which harms readers rather than the estate |
| **C5** Transfer | "If they added a newsletter, they'd have to open a dataset with a prior written question." | **3** | Correct transfer to a case MX-003 does not discuss, correctly routed through [REG-06 §3.1](../registries/reg-06-dataset-registry.md) |

**Profile: 3, 4, 2, 2, 3.** No total.

### 4.1 What the profile tells this reader

They understood the obligations and the boundary well, and **scored lowest exactly
where the instrument is most adverse to itself**. On C4 they produced the objection
that costs the *estate* something and missed the one that costs the *reader*
something — which is the more important of the two and is the one MX-003 goes out
of its way to publish.

That is a common and instructive pattern: readers of a self-critical document tend
to absorb the criticisms that flatter the author's honesty and skip the ones that
describe a cost to themselves. A reader with this profile should reread
[MX-003 §5](../corpus/mx-003-privacy-notice.md) before relying on anything in the
corpus, because the un-absorbed fact — *nobody will tell you when a document you
relied on is corrected* — bears directly on how they should use the estate.

That is the rubric doing its job: not grading a reader, but pointing at the one
paragraph their own answers show they skipped.

## 5. Failure modes

| # | Failure | Mechanism | Current state |
|---|---|---|---|
| F1 | **Scoring with the page open** | Convenience | Prevented only by the reader's honesty (§3.1) |
| F2 | **C4 answered with the author's own concession** | The corpus hands readers its objections | **Actual** — §4's reader did exactly this |
| F3 | **Rubric repurposed as assessment** | Demand for a measurable outcome | Prohibited by §3.3 |
| F4 | **Gamification** | Progress markers added to "help" | Prohibited by §3.3 |
| F5 | **Total computed** | Five numbers feel incomplete | Prohibited by §2 |
| F6 | **Estate never learns anything** | By design | **Actual and accepted** — §6 |
| F7 | **Fluency mistaken for comprehension** | The corpus is written to be clear | The entire reason for §1.1 |

F2 is subtle and worth stating. This corpus's practice of publishing its own
strongest objections ([ST-06](../standards/st-06-objections-standard.md)) makes C4
*easier to answer and harder to answer well*. A reader who repeats the estate's
filed objection has shown attentive reading, not independent judgement — that is a
2, not a 4. A 4 on C4 requires an objection the estate did **not** publish.

## 6. Limits

1. **The estate learns nothing from this rubric.** By construction. It cannot tell
   whether any reader has ever run it, whether the dimensions discriminate, or
   whether the anchors are usable. Every claim in §§1–3 is **E0** under
   [ST-07](../standards/st-07-evidence-and-verify.md).
2. **Self-scoring is unreliable** in the specific direction of overestimation, and
   this rubric has no correction for it. F1 has no control.
3. **No calibration, no inter-rater data** — there are no raters.
4. **C5 (transfer) is the hardest to self-score fairly**: a reader cannot easily
   tell whether their transfer is correct without the estate's confirmation, which
   they will not receive.
5. **Five dimensions are asserted**, not derived. A comprehension literature
   exists; the estate has not surveyed it, and this rubric is not grounded in it.
   That is a straightforward gap and not a principled position.
6. **No Arabic text**, while `prevailing_text: ar` — so a reader assessing their
   comprehension of an estate whose authoritative language is Arabic is doing so in
   the subordinate language, against instruments whose prevailing text does not
   exist ([MX-020](../corpus/mx-020-language-authority.md)).
7. **BK-01's thesis remains untested.** [REG-03 §5.1](../registries/reg-03-book-registry.md)
   records its falsifier — *if readers who comprehend a mechanism rely on it no
   differently from readers who do not, the thesis fails* — as **E0**. This rubric
   was the obvious instrument for testing it and, because of §6.1, cannot.

## 7. Falsifier

> **IF FALSE.** This rubric is falsified if:
>
> - **(a)** a reader scoring ≥ 3 on all five dimensions is shown to have a material
>   misunderstanding of the instrument — which would mean the five dimensions do not
>   cover comprehension;
> - **(b)** a reader scoring ≤ 1 on C1 is shown to apply the instrument correctly in
>   practice — which would mean the dimensions measure articulation, not
>   understanding;
> - **(c)** the rubric is used to produce any credential, ranking, or record held
>   by the estate (§3.3);
> - **(d)** a total score appears alongside RB-04 output;
> - **(e)** the estate is shown to hold any RB-04 result — which would mean §6.1's
>   refusal was breached.
>
> **(a) and (b) are the substantive tests and the estate cannot run either**, for
> exactly the reason in §6.1. They are runnable only by a reader who is willing to
> tell someone their result, which the estate does not ask for. This rubric
> therefore publishes a falsifier it has deliberately placed beyond its own reach,
> and a reader should weigh that honestly: it is either principled restraint or a
> convenient way to hold an untestable claim, and the estate's own
> [REG-06 §5.1](../registries/reg-06-dataset-registry.md) concedes the two can look
> identical.

## 8. Obligation

**On a reader (optional — this rubric binds nobody):**
- Close the page before answering (§3.1).
- Answer C4 with an objection the estate did **not** publish; otherwise score
  yourself 2 (F2).
- Report five numbers to yourself; compute no total.
- Act on the lowest dimension using §3.2.

**On the estate:**
- Never collect, request, or infer a reader's result (§3.3,
  [REG-06](../registries/reg-06-dataset-registry.md)).
- Never convert this into a credential, badge, streak, or ranking (§3.3).
- Keep publishing its own strongest objections, even though doing so makes C4
  easier to answer cheaply ([ST-06](../standards/st-06-objections-standard.md)).
- Keep the Obligation, Limits, and Falsifier sections present on every page —
  §3.2's remedies depend on them existing everywhere
  ([ST-24](../standards/st-24-page-prose-standard.md)).
- State plainly that BK-01's thesis remains untested and that this rubric cannot
  test it (§6.7).

---

### Related

**Sibling rubrics** — [RB-01](rb-01-d1-d5-rubric.md) ·
[RB-02](rb-02-proof-ladder.md) · [RB-03](rb-03-instrument-quality-rubric.md) ·
[RB-05](rb-05-harm-review-gate.md)

**What makes the rubric runnable** — [ST-24](../standards/st-24-page-prose-standard.md) ·
[ST-06](../standards/st-06-objections-standard.md) ·
[ST-04](../standards/st-04-falsifiability-and-claim-cards.md) ·
[SITE-02](../site/page-contract.md)

**The refusals behind its shape** — [MX-023](../corpus/mx-023-attention-and-human-sovereignty.md) ·
[REG-06](../registries/reg-06-dataset-registry.md) ·
[REG-05](../registries/reg-05-credential-registry.md) ·
[MX-003](../corpus/mx-003-privacy-notice.md)

**The untested thesis** — [REG-03](../registries/reg-03-book-registry.md) ·
[ST-07](../standards/st-07-evidence-and-verify.md) ·
[LEX-01](../lexicon/keyword-register.md) ·
[MX-001](../corpus/mx-001-about-metax.md)

### Exit pair

1. **Run it once, now.** Close this page and answer C1–C5 about **this rubric**.
   Your C4 must be an objection §6 does not already make.
2. **Read the paragraph readers skip.** [MX-003 §5](../corpus/mx-003-privacy-notice.md)
   — §4.1 predicts you missed it.

<!-- mx-pagestamp: RB-04 · v2026.10.1 · operative-form · tier 5 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; no comprehension result is collected, stored, or seen by the estate -->
