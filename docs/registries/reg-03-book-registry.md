---
doc_id: REG-03
title_en: Book Registry
title_ar: سجل الكتب
family: registries
version: v2026.10.1
status: published
authority: record
prevailing_text: ar
audience_tier: 3
depth: meta
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [books, registry, long-form, publication]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. The register contains no completed book.
route: /registries/books/
---

# REG-03 — Book Registry

> **Authority note.** A **record**, outside the precedence ladder
> ([GM-01](../00-governance-map/precedence-and-conflict-rules.md)). Book *content*
> is licensed by [ML-2.3](../license/the-maher-license.md); book *form* is governed
> by [ST-24](../standards/st-24-page-prose-standard.md) and
> [SITE-02](../site/page-contract.md); book *addresses* by
> [SITE-03](../site/routing-law.md). This page records only what exists.

> **Disclosure first.** **The estate has published no book.** Two are in progress;
> one is announced and undrafted. A registry with no completed entries is still
> worth publishing, because the alternative — mentioning books in prose without a
> register — is how an estate accumulates implied works. Every book the corpus
> mentions is listed below with its true state.

---

## 1. Position

A book is the estate's **longest-form unit** and therefore the one where the gap
between announcement and delivery can grow largest without anyone noticing. Three
structural facts follow:

1. A book cannot be a stub. A stubbed page is honest; a stubbed book is a
   prospectus.
2. A book's obligations are **inherited, not special**. There is no relaxed
   standard for long work.
3. A book, being durable, sits at `review_interval_months: 12` — the longest
   interval in [ST-05](../standards/st-05-decay-and-review-intervals.md). Long
   intervals are dangerous for incomplete work, which is why §5 records a
   *drafting* state separately from a *review* date.

## 2. Definition

A **book** is a work satisfying all five:

1. **Single sustained argument** across ≥ 8 chapters, with a stated thesis.
2. **Declared completion state** at every moment of its public life — `announced`,
   `drafting`, `partial-public`, `complete`, or `abandoned`.
3. **Chapter-level addressing**: each chapter independently routable; the book's
   own route is a hub, not a monolith.
4. **A falsifier for the thesis** (ST-04). A book whose thesis cannot fail is a
   catalogue of opinions, and must be registered as something other than a book.
5. **An authorship statement** disclosing AI involvement per
   [MX-007](../corpus/mx-007-ai-use-and-disclosure.md).

### 2.1 Book vs series vs page

| Unit | Binding logic | Registered in | Can be open-ended? |
|---|---|---|---|
| **Page** | One topic, one address | [REG-02](reg-02-page-registry.md) | n/a |
| **Series** | Recurring editorial intent | [REG-01](reg-01-series-registry.md) | Yes, if declared |
| **Book** | One sustained argument | REG-03 (this) | **No** — must have an end |

The distinction is load-bearing. A series may be declared open-ended; a book may
not. An "open-ended book" is a series with pretensions, and registering it as a
book borrows the finality a book promises without accepting the duty to finish.

## 3. Mechanism

### 3.1 States and permitted transitions

```
announced ──► drafting ──► partial-public ──► complete
    │             │              │
    └─────────────┴──────────────┴──────────► abandoned
```

- `announced` — named publicly; no chapter drafted. **Must** carry a date.
- `drafting` — chapters exist, none public.
- `partial-public` — some chapters public, book incomplete. Every public chapter
  must show the book's completion fraction.
- `complete` — all declared chapters public and compliant.
- `abandoned` — terminal; requires a corrections-log entry naming the reason.

No transition is silent. Each requires a [changelog](../00-governance-map/changelog.md)
line. `announced → complete` without passing through the intermediate states is
impossible and, if it appears in the record, indicates a falsified history.

### 3.2 The announcement clock

An `announced` book with **no chapter public after 12 months** is automatically in
defect. This is the estate's only *automatic* defect trigger outside the licence,
and it exists because announcement is cheap and delivery is not. The remedy is
one of: publish a chapter, move to `drafting` with a dated plan, or move to
`abandoned`. "Still coming" is not a remedy.

### 3.3 Chapter compliance

Each chapter is a page and inherits every page duty: front matter, ST-24 eight
parts, SITE-02 furniture, the word floor. A book therefore cannot be compliant
while any chapter is not. The book's compliance is the **minimum** across its
chapters, never the average — the same anti-averaging principle as
[RB-01](../rubrics/rb-01-d1-d5-rubric.md).

## 4. Worked instance

**How the clock would bite, traced on a real row.**

`BK-03` below is `announced`, dated 2026-08. Under §3.2 the clock expires
2027-08. Suppose nothing is drafted by then. The estate's options are three, and
each has a visible cost:

- **Publish one chapter.** Satisfies the clock, but a single chapter of a
  ten-chapter argument is `partial-public` at 1/10, and every public chapter must
  print that fraction. The reader sees 1/10.
- **Move to `drafting` with a dated plan.** Requires naming chapter titles and a
  date. The date then becomes falsifiable, and missing it is a further defect.
- **Move to `abandoned`.** Cheapest in effort, most expensive in credibility, and
  requires the corrections-log entry to say *why*.

There is no fourth option in which the announcement quietly persists. That is the
whole design: the clock converts silence from a free action into a recorded
defect.

A second instance, on the other side. `BK-01` is `drafting` with 4 of 11 chapters
written. Because no chapter is public, the reader currently sees **nothing** — not
a partial book, not a teaser. That is correct behaviour under §2(2): a book
becomes visible when it becomes `partial-public`, and until then its existence is
recorded only here, in a register, where it cannot be mistaken for a reading
experience.

## 5. The register

| ID | Title (EN) | Thesis (abridged) | Chapters declared | Chapters written | Public | State | Dated | Route |
|---|---|---|---|---|---|---|---|---|
| `BK-01` | Understanding Before Use | A reader owes themselves comprehension before reliance; systems owe readers the means of it | 11 | 4 | 0 | `drafting` | 2026-05 | `/books/bk-01/` |
| `BK-02` | The Harms Book | The twenty-five structural harms of ML-2.3, each with a worked instantiation and a falsifier | 25 + 3 | 2 | 0 | `drafting` | 2026-07 | `/books/bk-02/` |
| `BK-03` | Governing a Corpus | A document estate can be governed by instruments a single reader can check | 10 | 0 | 0 | `announced` | 2026-08 | `/books/bk-03/` |

### 5.1 Row notes

- **`BK-01`** — Thesis has a falsifier: *if readers who comprehend a mechanism
  rely on it no differently from readers who do not, the thesis fails.* No study
  supports or refutes this; the claim is therefore **E0** under
  [ST-07](../standards/st-07-evidence-and-verify.md) and is labelled as such
  inside the draft.
- **`BK-02`** — Depends entirely on **N-01**, the HX-000 re-version to 25 harms,
  which is the estate's largest outstanding item. `BK-02` cannot pass `drafting`
  until HX-000 exists, because a book about twenty-five harms cannot be written
  against a document that describes fourteen. This dependency is the reason the
  row shows 2 of 28.
- **`BK-03`** — Announced with zero chapters. Clock expires **2027-08**. Recorded
  here so the expiry is discoverable rather than forgotten.

### 5.2 Books mentioned in the corpus but **not** registered

A register's honesty is tested by what it admits it cannot place. The following
titles appear in prose across the estate and have **no** entry above, because no
chapter and no thesis exists for them:

| Mentioned as | Where | Disposition |
|---|---|---|
| "the forthcoming lexicon volume" | [LEX-01](../lexicon/keyword-register.md) intro | **Not a book.** Reclassified as a term set; no `BK-` number assigned |
| "the design compendium" | [DS-00](../design/ds-00-as-built-token-layer.md) | **Not a book.** It is the `DS-` family read in order |
| "the standards handbook" | README (earlier revision) | **Withdrawn phrase.** Logged to corrections |

Each of these is an instance of the same error: describing an existing *family* as
a forthcoming *book*, which promises an argument where only a filing category
exists. No `BK-` numbers were spent, which is the one piece of good news —
compare `S3` in [REG-01](reg-01-series-registry.md), where a careless citation did
burn a number permanently.

## 6. Failure modes

| # | Failure | Why it happens | Current state |
|---|---|---|---|
| F1 | **Prospectus drift** — announced books accumulate | Announcement is free | Controlled by the §3.2 clock; **one clock live** (`BK-03`) |
| F2 | **Family-as-book** — a filing category described as a forthcoming work | Prose written before registry existed | **Occurred ×3**, all caught in §5.2 |
| F3 | **Average compliance** — a strong chapter masking a failing one | Temptation to report a mean | Prevented by the minimum rule (§3.3) |
| F4 | **Thesis without falsifier** — a book of assertions | Long form invites accumulation over argument | `BK-01` and `BK-03` theses are E0; labelled, not hidden |
| F5 | **Dependency deadlock** — a book blocked on an absent instrument | `BK-02` on HX-000 | **Live and unresolved** |
| F6 | **Open-ended book** — book status claimed for a series | Books confer finality | Prevented by §2.1; not observed |
| F7 | **Chapter orphaning** — chapter public, book row stale | Manual maintenance | Possible; nothing public yet, so latent |

## 7. Limits

1. **No completed book exists.** Every general claim in §§2–3 about how books
   behave in this estate is therefore **untested**. The mechanism is specified and
   has never run to completion once.
2. **The clock has never fired.** Its first possible firing is 2027-08. Until then
   §3.2 is a promise about future conduct by a single person
   ([DEF-031](../00-governance-map/defect-register.md)).
3. **No Arabic book, no Arabic chapter, no Arabic title in this register** — while
   `prevailing_text: ar`. The prevailing text of every row is absent.
4. **`BK-02` is structurally blocked** and will remain so until N-01 is discharged.
   Listing it as `drafting` is accurate but flattering; `blocked` would be a truer
   word, and the state vocabulary of §3.1 does not contain it. That is a defect in
   the vocabulary, not in the row — filed with **RAT-24** as a companion question.

## 8. Falsifier

> **IF FALSE.** This register is falsified if:
>
> - **(a)** any book chapter is publicly reachable while its row shows `Public: 0`;
> - **(b)** a `BK-` identifier appears anywhere in the corpus and is absent here;
> - **(c)** `BK-03`'s clock passes 2027-08 with no state change and no defect entry;
> - **(d)** any row's "chapters written" count is shown to be overstated.
>
> (b) is checkable by search in one minute. (c) is checkable by a calendar and
> requires no access to anything. The estate invites (c) specifically, because a
> commitment whose breach is easy to detect is the only kind worth publishing.

## 9. Obligation

None arises here — this is a record. The bearing duties:

- Every chapter meets [ST-24](../standards/st-24-page-prose-standard.md) and
  [SITE-02](../site/page-contract.md) in full; length grants no relief.
- State changes are logged in the
  [changelog](../00-governance-map/changelog.md); abandonment additionally in the
  [corrections log](../00-governance-map/corrections-log.md).
- Theses carry falsifiers per [ST-04](../standards/st-04-falsifiability-and-claim-cards.md);
  unsupported theses are labelled **E0**, not left unlabelled.
- AI involvement is disclosed per [MX-007](../corpus/mx-007-ai-use-and-disclosure.md).
  Every row above was drafted with AI assistance.
- Reuse of any book content is governed by
  [ML-2.3](../license/the-maher-license.md) — not by this page and not by
  [MX-012](../corpus/mx-012-licensing-and-reuse.md), which only summarises.

---

### Related

**Form and length** — [ST-24](../standards/st-24-page-prose-standard.md) ·
[SITE-02](../site/page-contract.md) · [ST-04](../standards/st-04-falsifiability-and-claim-cards.md) ·
[ST-07](../standards/st-07-evidence-and-verify.md)

**Dependencies** — [HX-000 draft](../harms/hx-000-the-fourteen-structural-harms.md) ·
[HX-002](../harms/hx-002-harm-instrument-map.md) ·
[ML-2.3](../license/the-maher-license.md) ·
[task ledger](../00-governance-map/task-ledger.md)

**Records** — [REG-01](reg-01-series-registry.md) ·
[REG-02](reg-02-page-registry.md) ·
[GM-02](../00-governance-map/document-index.md) ·
[corrections log](../00-governance-map/corrections-log.md)

**Adjacent registries** — [REG-04](reg-04-media-registry.md) ·
[REG-05](reg-05-credential-registry.md) · [REG-06](reg-06-dataset-registry.md)

### Exit pair

1. **Set a reminder for 2027-08.** If `BK-03` has not moved, the estate has broken
   a rule it wrote against itself, and §8(c) tells you so.
2. **Unblock the real bottleneck.** Read the
   [HX-000 draft](../harms/hx-000-the-fourteen-structural-harms.md); `BK-02` waits
   on it.

<!-- mx-pagestamp: REG-03 · v2026.10.1 · record · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; no book chapter is publicly reachable -->
