---
doc_id: "LEX-04"
title_en: "The MetaX Identifier and Naming Grammar"
title_ar: "قواعد المعرّفات والتسمية في MetaX"
family: "lexicon"
version: "v2026.10.2"
status: "draft"
authority: "standard"
prevailing_text: "en"
audience_tier: 3
depth: 4
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-26"
domain_tags: ["lexicon", "grammar", "identifiers", "numbering", "naming"]
route: "/lexicon/grammar/"
derived_from: "Meta-Review Part C (Rules 1–6); ST-01; GM-13"
ratification: "PENDING — RAT-25, RAT-27(b)"
provenance_of_purpose: "consolidation"
authorship_note: "Compiled by an AI system under AG-000. It consolidates grammar rules scattered across ST-01, Meta-Review Part C and the registers. Where they disagree, the disagreement is recorded here and left unresolved."
hreflang: "en, ar"
---

# LEX-04 · The MetaX Identifier and Naming Grammar

> **Authority.** A `standard`, tier 5. Where it conflicts with [ST-01](../standards/st-01-identifier-and-url-grammar.md),
> ST-01 prevails. This file adds no rule of its own. It gathers the existing rules in one place and
> marks each point where they disagree.

> **Disclosure first.** The corpus has **four identifier grammars in use at once**: the ST-01
> instrument grammar, the Meta-Review Part C grammar, the two-digit series grammar of the canon
> (S01…S52), and the date-based defect grammar (DEF-2026-041). §4 lists every point where they
> disagree. None is resolved here.

---

## 1. Position

An identifier is a promise that one number means one thing for ever (Rule 2). The grammar exists so
that a machine can tell from the string alone what kind of object it refers to.

## 2. Definition — the six rules (Meta-Review Part C, restated)

1. **One monotonic counter** per namespace. No branch semantics, no reserved blocks, no gaps.
2. **Numbers are immortal.** Never reused, reassigned or freed. A retired object keeps its number with `status: retired` and a pointer.
3. **Branch is metadata, not identity.**
4. **Canonical URLs are branch-free:** `/s/{id}-{slug}/`.
5. **Families for non-series objects** (§3).
6. **Every count is computed.** No typed number appears on an index page.

**Slug stability:** the identifier is authoritative and the slug is decorative. A slug change emits a
301 redirect, and both forms resolve permanently.

## 3. Mechanism — namespace table

| Namespace | Pattern | Example | Source | High-water (GM-13 §4) |
|---|---|---|---|---|
| Corpus instrument | `MX-NNN` | MX-029 | Part C R5 | MX-029 |
| Agent charter | `AG-NNN` | AG-022 | Part C R5 | AG-022 |
| Standard | `ST-NN` | ST-33 | Part C R5 | ST-33 |
| Rubric | `RB-NN` | RB-07 | Part C R5 | RB-07 |
| Registry | `REG-NN` | REG-12 | *corpus practice only* | REG-12 |
| BCIA instrument | `BX-NNN` | BX-017 | *corpus practice only* | BX-017 |
| Harms | `HX-NNN` / `HX-NN` (harm) | HX-000, HX-24 | corpus practice | — |
| Governance map | `GM-NN` | GM-15 | corpus practice | GM-15 |
| Lexicon doc | `LEX-NN` | LEX-05 | corpus practice | LEX-05 |
| Site doc | `SITE-NN` | SITE-05 | corpus practice | SITE-05 |
| Design system | `DS-NN` | DS-07 | corpus practice | — |
| Series | `S` + digits | S38 / S038? | **conflict**, §4 X-1 | — |
| Book | `bk-{family}-{NNN}` | bk-bx-001 | Part C R5 | — |
| Credential | `cr-{track}-{NNNNNN}` | — | Part C R5 | — |
| Determination | `det-{YYYY}-{NNN}` vs `D-id` | — | Part C R5 / REG-11 | **conflict**, X-4 |
| Defect | `def-{pillar}-{NNN}` vs `DEF-NNN` vs `DEF-YYYY-NNN` | DEF-037 | **conflict**, X-3 | DEF-039 |
| Lexicon term | `t-{root}-{NN}` | — | Part C R5 | — |
| Ratification | `RAT-NN` | RAT-28 | corpus practice | RAT-28 |
| Reconciliation | `R-NN` | R-60 | corpus practice | R-60 |
| Verification | `V-NN` | V-17 | corpus practice | V-17 |

## 4. Worked instances — known grammar conflicts

| X | Conflict | Evidence | Proposed disposition |
|---|---|---|---|
| X-1 | The series width: Part C says `S001`; the canon and REG-01 use `S01`/`S38` | Meta-Review R1 vs REG-01 | Treat `S38` ≡ `S038` as **one identifier in two renderings**. Canonical form is the Curator's choice (RAT-27(b)) |
| X-2 | Book code `MX-MP-01` collides with the `MX-` instrument prefix | BX-013 §4 | Render it only as `bcia_book_code: MX-MP-01` and never bare |
| X-3 | Three defect grammars | defect-register (DEF-035), MX-NAV-SPEC (DEF-2026-041), Part C (`def-{pillar}-NNN`) | Keep all issued strings (Rule 2). Choose one for new issues (RAT-28(d)) |
| X-4 | Determinations: `det-YYYY-NNN` (Part C) vs `D-id` (REG-11) | — | Adopt `det-YYYY-NNN`. REG-11 has no rows, so nothing needs to change |
| X-5 | REG, BX, GM, LEX, SITE and DS are not in Part C R5 | — | Add them to ST-01's prefix table (GM-15 item) |
| X-6 | `bx` is both a book family (`bk-bx-`) and an instrument family (`BX-`) | Part C R5 | No collision in the strings, because the `bk-` prefix differs. Record only |
| X-7 | The v2026.10.1 pass reused 16+ instrument numbers | GM-13, DEF-035/039 | Refuge numbers plus pointer stubs (RAT-25) |

## 5. Failure modes

- **Gap-filling:** taking a "free-looking" number below the high-water mark. Forbidden.
- **Semantic numbering:** reading meaning into a number, e.g. "S38–S47 = Branch D". This breaks Rule 3 the moment a series moves branch.
- **Typed counts:** "52 series" typed in prose. Rule 6 requires the count to be computed (REG-09 note).

## 6. Limits

The grammar governs strings. It does not govern titles, which are governed by the lexicon entry standard.

## 7. Falsifier

The grammar has failed if any single identifier string resolves to two different objects anywhere
in the published estate.

## 8. Obligation

Before minting any identifier, agents read the GM-13 §4 high-water row, and they add a row after minting.

## Macro register

Identifiers are how a corpus lets itself be cited. A reused number is a silent edit to every
citation that used it. This is why Rule 2 is treated as absolute.

---

**Related:** [ST-01](../standards/st-01-identifier-and-url-grammar.md) · [GM-13](../00-governance-map/identifier-reallocation-record.md) ·
[LEX-05](contested-terms.md) · [LEX-01](keyword-register.md) · [LEX-02](lexicon-entry-standard.md) · [LEX-03](term-set-governance.md) ·
[REG-01](../registries/reg-01-series-registry.md) · [SITE-03](../site/routing-law.md) · [BX-013](../bcia/bx-013-observed-taxonomy.md)
