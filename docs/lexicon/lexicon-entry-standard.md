---
doc_id: LEX-02
title_en: Lexicon Entry Standard
title_ar: معيار مدخل المعجم
family: lexicon
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
domain_tags: [lexicon, entry, form, arabic, terminology]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. The standard requires an Arabic term on every entry; no entry in the lexicon has one.
route: /lexicon/entry-standard/
---

# LEX-02 — Lexicon Entry Standard

> **Authority.** `operative-form`, tier 5. Governs the **form of a lexicon entry**.
> The rules about *which* terms are defined and *where* are
> [ST-10](../standards/st-10-terminology-and-definition-standard.md); the register
> itself is [LEX-01](keyword-register.md); Arabic mechanics are
> [ST-11](../standards/st-11-arabic-authoring.md).

> **Disclosure first.** This standard requires field 2 of every entry to be the
> **Arabic term**. [LEX-01](keyword-register.md) contains **twenty entries and no
> Arabic**. So every existing entry is non-compliant with this standard at its
> second field, in a corpus whose prevailing text is Arabic
> ([MX-020](../corpus/mx-020-language-authority.md)). The standard is published in
> that state rather than weakened to match.

---

## 1. Position

A lexicon in this corpus is not a glossary. A glossary helps a reader with a word;
a **lexicon entry states where a term's meaning is fixed and what it excludes.**

Three duties from [ST-10](../standards/st-10-terminology-and-definition-standard.md)
land here as form:

- **T1** one term, one defining instrument → the entry must name **exactly one**.
- **T5** confusable pairs declared → the entry must carry its pair.
- **T6** imported terms flagged with divergence → the entry must state it.

So an entry is a **pointer with guards**, not a definition. The definition lives in
the defining instrument. An entry that restates the definition has become a local
definition, which T3 prohibits.

### 1.1 The entry never defines

Stated as a prohibition because it is the natural drafting instinct:

> An entry gives the **shortest possible orientation** — enough to confirm the
> reader has the right term — and then **sends them to the defining instrument**.
> It never states the operative meaning.

A reader who can act on an entry without opening the defining instrument has been
given a summary, and summaries owe
[ST-09](../standards/st-09-summary-and-abstract-standard.md)'s five elements.
Keeping entries orientational avoids that burden entirely.

## 2. The nine fields

Every entry carries nine fields in this order. Fields 1–5 are **mandatory**; 6–9
are **conditional** and must be present when applicable.

| # | Field | Content | Mandatory |
|---|---|---|---|
| 1 | **Term (EN)** | The English term, in the form used in the corpus | Yes |
| 2 | **Term (AR)** | The Arabic term. **The authoritative form** | **Yes** |
| 3 | **Defining instrument** | Exactly one, linked, with the section | Yes |
| 4 | **Orientation** | ≤ 25 words. Enough to confirm the right term; never the operative meaning | Yes |
| 5 | **Not** | What the term does **not** mean, or is confused with | Yes |
| 6 | **Confusable pair** | The paired term and the one-line distinction | If T5 applies |
| 7 | **Imported from** | The field, plus narrower / wider / **uncertain** | If T6 applies |
| 8 | **First use** | The instrument where the term first appeared in the corpus | If earlier than field 3 |
| 9 | **Superseded sense** | A former meaning, retained per [ST-15 A3](../standards/st-15-amendment-and-versioning-standard.md) | If the meaning has changed |

### 2.1 Field 5 is the discriminating field

"Not" is where an entry earns its place. A term's boundary is more useful than its
centre, because readers err at edges.

| Term | Weak entry | Field 5 doing work |
|---|---|---|
| **record** | "A kind of document" | **Not** a governing instrument; a `record` sits **outside** the precedence ladder and creates no obligation |
| **notice** | "A communication" | **Not** a page banner. Sense 2 ("demo notice") is a *disclosure*; only sense 1 starts a cure clock |
| **session** | "A visit" | **Not** an identity. Nothing links two sessions |
| **designated** | "Marked under the licence" | **Not** the same as the front matter field; see field 6 |

Each of these boundaries corresponds to a real conflation risk named in
[ST-10 §6.1](../standards/st-10-terminology-and-definition-standard.md).

### 2.2 Field 2 and the authority inversion

Field 2 is mandatory and **is the authoritative form**, because
[MX-020](../corpus/mx-020-language-authority.md) makes Arabic the prevailing text
of every instrument.

The consequence is stark and worth stating rather than absorbing: **the corpus's
terms have no authoritative form.** Field 1 is the subordinate language; field 2
does not exist anywhere. A dispute about what a term means could not be resolved
by consulting the prevailing text, because there is none to consult.

This is not a translation backlog. It means [LEX-01](keyword-register.md) is a
register of subordinate-language approximations of terms whose real definitions have
never been written — which is a stronger statement than
[ST-10 §7.2](../standards/st-10-terminology-and-definition-standard.md) makes, and
it follows directly from requiring field 2.

## 3. The rules

| # | Rule | Rationale |
|---|---|---|
| **X1** | Nine fields, in order; 1–5 always present | Machine readability ([ST-14](../standards/st-14-machine-surfaces-and-json-schemas.md)) |
| **X2** | Field 3 names **exactly one** instrument | [ST-10 T1](../standards/st-10-terminology-and-definition-standard.md) |
| **X3** | Field 4 is ≤ 25 words and **states no obligation** | §1.1; otherwise it is a summary |
| **X4** | Field 5 is never empty. "No common confusion" is not acceptable — find the edge | §2.1 |
| **X5** | Field 7 records **`uncertain`** where divergence is unknown; never guesses | No counsel ([REG-08](../registries/reg-08-role-and-authority-registry.md)) |
| **X6** | An entry is **not** amended to reflect a changed meaning — field 9 records the former sense | [ST-15](../standards/st-15-amendment-and-versioning-standard.md) A3 |
| **X7** | Alphabetical by field 1 **and** by field 2 when Arabic exists; the two orders are published separately | Arabic and English collation differ ([ST-11](../standards/st-11-arabic-authoring.md)) |

### 3.1 X7 and the two orders

An Arabic–English lexicon cannot have one canonical order. Arabic collation is by
root in scholarly practice and by letter in modern practice, and neither maps to
English alphabetical order.

[ST-11](../standards/st-11-arabic-authoring.md) records that Arabic metrics and
collation are **explicitly unverified** in this corpus. So X7 requires two
published orders and the estate can currently produce **one**, which makes the
Arabic-ordered index one of the absent lexicon artefacts alongside the roots index.

## 4. Worked instance

**Writing one compliant entry, then finding what it cannot do.**

Term: **record**. One of the four T1 breaches in
[ST-10 §6.1](../standards/st-10-terminology-and-definition-standard.md).

| # | Field | Content |
|---|---|---|
| 1 | Term (EN) | record |
| 2 | Term (AR) | **absent** — X1 breach |
| 3 | Defining instrument | [GM-01 precedence](../00-governance-map/precedence-and-conflict-rules.md) §2 (authority classes) |
| 4 | Orientation | An authority class. A document that reports facts and creates no obligation. (17 words) |
| 5 | **Not** | **Not** an entry in a register — that sense is [MX-013](../corpus/mx-013-records-and-versioning.md)'s. **Not** subject to the precedence ladder: records sit outside it entirely |
| 6 | Confusable pair | *record* (authority class) ↔ *record* (register entry). Distinction: the first is **what a document is**; the second is **what a register contains** |
| 7 | Imported from | — not applicable |
| 8 | First use | [MX-013](../corpus/mx-013-records-and-versioning.md), earlier than GM-01 in drafting order |
| 9 | Superseded sense | — none |

**Terminal state: `result`, one mandatory field unfillable.**

### 4.1 What the instance exposed

**Field 6 revealed that a term can be confusable with itself, and X2 cannot express
it.** X2 requires field 3 to name exactly one defining instrument. For *record*
there genuinely are two senses, each properly defined in a different instrument,
and both are needed.

So the compliant entry above is **misleading**: it names GM-01 as *the* defining
instrument and demotes MX-013's sense to field 5, as though it were a confusion
rather than a legitimate second sense. That is not accurate. It is an artefact of a
rule designed for terms with one meaning.

Per [ST-17 W6](../standards/st-17-worked-instance-standard.md), the discovery is
filed as a clarification rather than patched away:

> **X2, clarified.** Where a term has two legitimate senses defined in different
> instruments, the term takes **two entries**, distinguished by a parenthetical
> qualifier in field 1 — *record (authority class)* and *record (register entry)* —
> each naming one defining instrument, each carrying the other in field 6. A single
> entry demoting one sense to field 5 is non-compliant.

This also supplies [ST-10](../standards/st-10-terminology-and-definition-standard.md)
with a remedy shape it lacked for two of its four T1 breaches. ST-10 §5 proposed
*splitting the term* for `designated` and found the split blocked, because renaming
a front matter field breaks eighty files and a published schema. **Splitting the
entry is not blocked**: the lexicon has no schema dependency and no published route
per term.

So the T1 breaches for **record** and **notice** are remediable at the lexicon
level even though they are not remediable at the source level — which is a genuinely
useful finding and the reason this instance was worth working.

## 5. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Field 2 absent** | **All 20 entries** ([LEX-01](keyword-register.md)) |
| F2 | **Entry becomes a definition** | Guarded by X3's 25-word bound |
| F3 | **Field 5 empty or "none"** | Guarded by X4; the field authors most want to skip |
| F4 | **Two senses in one entry** | **Actual** — §4.1; now non-compliant under X2-as-clarified |
| F5 | **Divergence guessed** | Guarded by X5's mandatory `uncertain` |
| F6 | **Entry amended over a changed meaning** | Guarded by X6; field 9 preserves the former sense |
| F7 | **Single collation order** | **Actual** — §3.1; the Arabic order does not exist |
| F8 | **Unregistered terms** | **~80 of ~100** ([ST-10 §7.1](../standards/st-10-terminology-and-definition-standard.md)) |

## 6. Limits

1. **Field 2 is mandatory and universally absent.** By its own rules this standard
   governs zero compliant entries.
2. **X7's Arabic order cannot be produced**, because collation practice for this
   corpus is unsettled ([ST-11](../standards/st-11-arabic-authoring.md)).
3. **X2 was wrong as first drafted** (§4.1) and the clarification puts at least two
   existing entries in breach.
4. **~80 terms unregistered**, so the standard's reach is a fifth of its subject.
5. **No check runs.** X1's field count and X3's word bound are trivially
   mechanisable; [ST-13 SENTINEL](../standards/st-13-static-build-and-sentinel.md)
   does not run ([DEF-001](../00-governance-map/defect-register.md)).
6. **The 25-word bound in X3 is asserted**, not derived.

## 7. Falsifier

> **IF FALSE.** This standard is falsified if:
>
> - **(a)** an entry lacks any of fields 1–5 — **fires on all twenty**, field 2
>   (§6.1);
> - **(b)** field 3 names more than one instrument, or an entry carries two senses
>   (X2 as clarified) — **fires now**;
> - **(c)** field 4 exceeds 25 words or states an obligation;
> - **(d)** field 5 is empty or reads "none";
> - **(e)** field 7 states a divergence the estate has no basis for (X5);
> - **(f)** a registered term is shown to be defined in an instrument other than
>   its field 3 — which would be an [ST-10 T1](../standards/st-10-terminology-and-definition-standard.md)
>   breach discovered through the lexicon rather than the source.
>
> **(f) is the valuable one**: the lexicon is the only place in the corpus where
> every term's defining instrument is asserted in one list, so it is the cheapest
> available instrument for finding T1 breaches. Running (f) across twenty entries is
> an hour's reading and has not been done.

## 8. Obligation

**On an author:**
- Nine fields, in order; 1–5 always (X1).
- **Never** state the operative meaning in field 4 (X3, §1.1).
- **Never** leave field 5 empty; find the boundary (X4, §2.1).
- Record `uncertain` rather than guessing divergence (X5).
- Two senses → **two entries** with parenthetical qualifiers (X2 as clarified,
  §4.1).
- Preserve a former sense in field 9; do not overwrite (X6).

**On the estate:**
- Supply **field 2** for all twenty entries, or state expressly that the corpus's
  terms have no authoritative form (§2.2). One of the two is owed.
- Split the **record** and **notice** entries per §4.1 — remedies unavailable at
  source level and available here.
- Settle Arabic collation and publish the second order
  ([ST-11](../standards/st-11-arabic-authoring.md), X7).
- Register the ~80 missing terms
  ([ST-10](../standards/st-10-terminology-and-definition-standard.md)).
- Run falsifier §7(f) — an hour's reading against twenty entries.

---

### Related

**Rules this standard implements** — [ST-10](../standards/st-10-terminology-and-definition-standard.md) ·
[ST-15](../standards/st-15-amendment-and-versioning-standard.md) ·
[ST-09](../standards/st-09-summary-and-abstract-standard.md) ·
[ST-14](../standards/st-14-machine-surfaces-and-json-schemas.md)

**Where the entries live** — [LEX-01](keyword-register.md) ·
[GM-02 document index](../00-governance-map/document-index.md) ·
[REG-02](../registries/reg-02-page-registry.md) ·
[MX-004](../corpus/mx-004-terms-of-top-levels.md)

**Why field 2 is empty** — [MX-020](../corpus/mx-020-language-authority.md) ·
[ST-11](../standards/st-11-arabic-authoring.md) ·
[MX-005 Annex A row 15](../corpus/mx-005-scope-and-boundaries.md) ·
[defect register](../00-governance-map/defect-register.md)

**Standards a reader of this page may have wanted instead** —
[ST-18](../standards/st-18-related-blocks-and-exit-pairs.md) ·
[ST-17](../standards/st-17-worked-instance-standard.md) ·
[ST-16](../standards/st-16-audience-tier-standard.md) ·
[ST-02](../standards/st-02-front-matter-schema.md)

### Exit pair

1. **Hunt T1 breaches through the lexicon.** Falsifier §7(f) — twenty entries, one
   hour, and the lexicon is the only list that makes it possible.
2. **Read what field 2's absence means.** [§2.2](#22-field-2-and-the-authority-inversion)
   — the corpus's terms have no authoritative form at all.

<!-- mx-pagestamp: LEX-02 · v2026.10.1 · operative-form · tier 5 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; no lexicon entry carries the mandatory Arabic term -->
