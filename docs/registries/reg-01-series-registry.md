---
doc_id: REG-01
title_en: Series Registry
title_ar: سجل السلاسل
family: registries
version: v2026.10.1
status: published
authority: record
prevailing_text: ar
audience_tier: 3
depth: meta
evidence_class: semi-durable
review_interval_months: 6
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [series, registry, identifiers, curriculum]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000; the register records no series that has completed a full review cycle.
route: /registries/series/
---

# REG-01 — Series Registry

> **Authority note.** This document is a **record** (`authority: record`). Under
> [GM-01 precedence](../00-governance-map/precedence-and-conflict-rules.md), records
> sit **outside** the precedence ladder entirely. Nothing on this page creates,
> modifies, or interprets an obligation. Where this register and a governing
> instrument disagree, the governing instrument is correct and this register is
> **defective** — and the defect is reportable under
> [MX-013 §4](../corpus/mx-013-records-and-versioning.md).

> **Disclosure first.** The register below holds **four** series entries. The
> corpus cites series identifiers in at least **eleven** places. The register is
> therefore known-incomplete at the moment of publication, and the incompleteness
> is not an accident of drafting but a true statement about the estate: most cited
> series have a name and no content. This is filed as
> [DEF-032](../00-governance-map/defect-register.md).

---

## 1. Position

REG-01 sits at **tier 6** of the precedence ladder in its *subject* (registries),
but as a **record** it is excluded from the ladder in its *authority*. The
distinction matters and is routinely collapsed by careless readers, so it is
stated flatly:

- The **existence** of a series is a fact. Facts are recorded here.
- The **rules** governing series are obligations. Obligations live in
  [ST-01 identifier grammar](../standards/st-01-identifier-and-url-grammar.md),
  [MX-013 records and versioning](../corpus/mx-013-records-and-versioning.md), and
  [RB-01 D1–D5](../rubrics/rb-01-d1-d5-rubric.md).

A reader who wants to know *whether the estate may open a new series* must not
read this page. A reader who wants to know *which series the estate has opened*
is in the right place.

## 2. Definition

A **series** (`S` prefix, per ST-01's closed prefix set) is a numbered sequence of
works published under a single pedagogical or editorial intent, where:

1. the intent is stated in writing **before** the first item is published;
2. items are numbered from `S1` upward with no gaps and no reuse;
3. the series has a **named** terminal condition — a stated point at which it is
   complete, or an explicit declaration that it is open-ended;
4. every item in the series is separately addressable under
   [SITE-03 routing law](../site/routing-law.md); and
5. the series is entered in this register **at the moment of the first
   publication**, not retroactively.

A sequence of works lacking any of (1)–(5) is **not a series**. It is a pile. The
estate contains piles, and calling a pile a series in order to inherit the
series's credibility is a species of the counterfeiting described in
[ST-04 §3](../standards/st-04-falsifiability-and-claim-cards.md).

### 2.1 What a series is not

| Not a series | Why | Correct term |
|---|---|---|
| All documents in one family (`ST-`, `MX-`) | Family membership is a filing fact, not an editorial intent | family |
| A tag or topic cluster | Membership is post-hoc and revisable | domain tag |
| A book's chapters | Internal structure of one work | chapters, see [REG-03](reg-03-book-registry.md) |
| Everything published in one month | Chronology is not intent | changelog range |
| A numbered course of study with no terminal condition | Fails limb (3) unless open-endedness is declared | candidate series |

## 3. Mechanism

### 3.1 Opening a series

| Step | Actor | Artefact produced | Reversible? |
|---|---|---|---|
| 1. Draft the intent statement | Curator | Prose, ≤ 400 words | Yes |
| 2. Assign the next free `S` number | Curator | Number, permanent | **No** — ST-01 Rule 2 |
| 3. Declare terminal condition | Curator | One sentence | Yes, by amendment with record |
| 4. Enter row in §5 below | Curator | Register row | Append-only |
| 5. Publish item 1 | Curator | Page under SITE-02 contract | Yes (withdrawal leaves a stub) |

Step 2 is the irreversible step. Under **ST-01 Rule 2 (numbers are immortal from
first assignment)** an `S` number, once written down anywhere a reader could have
seen it, is spent. A series that is opened and abandoned does not free its number;
it occupies it forever with the word `abandoned`.

### 3.2 Closing a series

A series closes in exactly one of four ways, and the register must say which:

- **`complete`** — the terminal condition declared at opening was met.
- **`abandoned`** — the curator states in writing that no further items will be
  published and the terminal condition was **not** met. Requires a corrections-log
  entry.
- **`superseded`** — a later series covers the same ground. The later series must
  name the earlier in its own intent statement.
- **`withdrawn`** — the series is removed from publication for a reason under
  [MX-008 §2 red lines](../corpus/mx-008-moderation-and-enforcement.md). The row
  stays; the content does not.

There is no fifth way, and in particular there is **no silent lapse**. A series
with no new item for twelve months and no closure entry is in a defect state, not
in a state of rest.

### 3.3 Numbering

`S` numbers are integers, unpadded, assigned in order of **opening**, not in order
of subject. `S1` is not necessarily introductory. Readers who infer difficulty
order from series number are inferring something the grammar does not encode; the
difficulty signal lives in [RB-02 proof ladder](../rubrics/rb-02-proof-ladder.md)
levels printed on each item.

## 4. Worked instance

**The estate's own first series, traced end to end.**

`S1` was opened to carry the *Understanding Before Use* sequence: short works each
of which explains one mechanism the reader is about to be asked to rely on. The
intent statement is reproduced in the row. The terminal condition was declared as
*"complete when every mechanism named in MX-000 §3 has one item."* MX-000 §3 names
nine mechanisms. Two items exist.

So `S1`'s register row reads `open`, its completion reads `2/9`, and its honest
description is *behind*. That is the whole value of the register: it converts an
optimistic impression ("we have a series") into an arithmetic statement ("two of
nine"). The arithmetic is checkable by any reader in under a minute, which is the
test [ST-07 §2](../standards/st-07-evidence-and-verify.md) sets for a claim of
class E1.

A second instance, less flattering. `S3` appears in the corpus in a cross-reference
written before the series existed. The reference was written; the number is
therefore spent under ST-01 Rule 2; no item was ever published. `S3`'s row reads
`reserved-by-citation`, which is a status the estate did not want to need and
cannot avoid having.

## 5. The register

Status vocabulary: `open` · `complete` · `abandoned` · `superseded` · `withdrawn` ·
`reserved-by-citation`.

| ID | Title (EN) | Intent (abridged) | Terminal condition | Items published | Status | Opened | Route |
|---|---|---|---|---|---|---|---|
| `S1` | Understanding Before Use | One short work per mechanism the reader is asked to rely on | Every mechanism in MX-000 §3 has one item | 2 of 9 | `open` | 2026-06 | `/series/s1/` |
| `S2` | Reading the Corpus | How to read a governing instrument without mistaking a summary for it | Open-ended (declared) | 1 | `open` | 2026-08 | `/series/s2/` |
| `S3` | *(untitled)* | — none recorded — | — none recorded — | 0 | `reserved-by-citation` | — | *(none)* |
| `S4` | Harms in Practice | One worked instantiation per harm stratum in ML-2.3 | Six strata each have one item | 0 of 6 | `open` | 2026-09 | `/series/s4/` |

### 5.1 Notes on each row

- **`S1`** — Two of nine. The seven absent items are not drafted. The series is
  cited by [MX-001](../corpus/mx-001-about-metax.md) in a way that implies
  completeness; that implication is wrong and is logged as a reconciliation item.
- **`S2`** — Declared open-ended at opening, which satisfies limb (3) of §2. An
  open-ended series can never be `complete`; its only closures are `abandoned`,
  `superseded`, or `withdrawn`.
- **`S3`** — The number is burnt. No intent statement exists, so under §2 this is
  not a series at all; the row exists to stop `S3` being reassigned.
- **`S4`** — Opened 2026-09 with zero items. Opening a series before drafting its
  first item is permitted by §3.1 but is poor practice, because it converts an
  intention into a public commitment with no evidence behind it. Recorded here as
  a self-criticism rather than removed.

## 6. Failure modes

| # | Failure | How it shows | Detection | Current state |
|---|---|---|---|---|
| F1 | **Retroactive series** — a pile renamed a series after the fact | Intent statement postdates item 1 | Compare dates in §5 to page stamps | Not observed |
| F2 | **Number reuse** — an abandoned number reassigned | Two intents, one `S` number | ST-13 SENTINEL check S3 | **Undetectable** — SENTINEL does not run ([DEF-001](../00-governance-map/defect-register.md)) |
| F3 | **Silent lapse** — no items, no closure | Register says `open`, changelog silent for 12 months | Manual review at 6-month interval | **Live risk** for `S4` |
| F4 | **Completion inflation** — "series" cited as complete when partial | Prose elsewhere implies coverage | Cross-read citations against §5 | **Occurring** — MX-001 vs `S1` |
| F5 | **Orphan items** — a page belongs to a series with no register row | Page stamp names a series absent from §5 | Route manifest diff | Not observed |
| F6 | **Terminal condition drift** — condition quietly widened so the series can be called complete | Condition text differs from opening text | No opening text is archived for `S1` | **Unverifiable** — see §7 |

## 7. Limits

1. **No archived opening texts.** For `S1` and `S2` the intent statements in §5 are
   *reconstructions*, not the originals, because the originals were not separately
   archived. F6 is therefore not merely undetected but undetectable for those two
   rows. This is a real failure of
   [GM-12 archive register](../00-governance-map/archive-register.md) Class B.
2. **The register is manually maintained.** Every consistency property claimed
   here depends on the curator performing a comparison no machine performs. There
   is one curator ([DEF-031](../00-governance-map/defect-register.md)).
3. **No Arabic titles for series.** `prevailing_text: ar` and no row carries an
   Arabic title. Under [MX-020 §2](../corpus/mx-020-language-authority.md) the
   prevailing text of a record is the Arabic text; there is none; therefore the
   prevailing text of this register **does not exist**. This is not a translation
   backlog — it is a structural defect in the record's own authority claim.
4. **`reserved-by-citation` is unbounded.** Nothing prevents a careless
   cross-reference from burning `S5`, `S6`, `S7` tomorrow. The only control is
   authorial care, which is not a control.

## 8. Falsifier

> **IF FALSE.** This register is falsified if any one of the following is shown:
>
> - **(a)** a series exists in published form whose identifier is absent from §5;
> - **(b)** any `S` number in §5 is shown to have carried a different intent at an
>   earlier date than the one recorded;
> - **(c)** a row's "items published" count differs from the number of pages
>   actually reachable under its route;
> - **(d)** an `S` number is shown to have been reassigned after abandonment.
>
> Each of (a)–(d) is checkable by a reader with no special access. (c) is
> checkable in **under five minutes** against
> [SITE-01 route manifest](../site/route-manifest.md). No such check has been
> performed and recorded; that omission is itself the content of
> [V-14](../00-governance-map/verification-log.md).

## 9. Obligation

This record imposes no obligation, because records cannot. The obligations that
*bear on* it live elsewhere and are restated here for navigation only:

- Assign identifiers per [ST-01](../standards/st-01-identifier-and-url-grammar.md);
  numbers are immortal.
- Keep the record append-only and publish corrections per
  [MX-013 §3](../corpus/mx-013-records-and-versioning.md).
- Do not describe a partial series as complete — [ST-04](../standards/st-04-falsifiability-and-claim-cards.md)
  treats coverage overstatement as a counterfeit claim.
- Nothing here licenses use of series content; use is governed by
  [ML-2.3](../license/the-maher-license.md) and summarised, without authority, by
  [MX-012](../corpus/mx-012-licensing-and-reuse.md).

---

### Related

**Grammar and form** — [ST-01](../standards/st-01-identifier-and-url-grammar.md) ·
[ST-02](../standards/st-02-front-matter-schema.md) ·
[ST-24](../standards/st-24-page-prose-standard.md) ·
[SITE-02](../site/page-contract.md)

**Records and permanence** — [MX-013](../corpus/mx-013-records-and-versioning.md) ·
[GM-12](../00-governance-map/archive-register.md) ·
[GM-02](../00-governance-map/document-index.md) ·
[changelog](../00-governance-map/changelog.md)

**Sibling registries** — [REG-02](reg-02-page-registry.md) ·
[REG-03](reg-03-book-registry.md) · [REG-04](reg-04-media-registry.md) ·
[REG-05](reg-05-credential-registry.md)

**Defects touching this page** — [DEF-001](../00-governance-map/defect-register.md) ·
[DEF-031](../00-governance-map/defect-register.md) ·
[DEF-032](../00-governance-map/defect-register.md) ·
[V-14](../00-governance-map/verification-log.md)

### Exit pair

1. **Check a row.** Open [SITE-01](../site/route-manifest.md) and count the pages
   under `/series/s1/`. If the count is not 2, file a defect.
2. **Read the governing instrument instead.** [ST-01](../standards/st-01-identifier-and-url-grammar.md)
   states the rules this register merely reports.

<!-- mx-pagestamp: REG-01 · v2026.10.1 · record · reviewed 2026-09-16 · next review 2027-03-16 -->
<!-- mx-demo: the published site is a demonstration; routes listed here may not resolve -->
