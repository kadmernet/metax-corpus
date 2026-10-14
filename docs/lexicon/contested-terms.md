---
doc_id: "LEX-05"
title_en: "Contested Terms Register"
title_ar: "سجل المصطلحات المتنازع عليها"
family: "lexicon"
version: "v2026.10.2"
status: "draft"
authority: "record"
prevailing_text: "en"
audience_tier: 3
depth: 4
evidence_class: "volatile"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-26"
domain_tags: ["lexicon", "contested-terms", "disambiguation", "bcia", "pillars"]
route: "/lexicon/contested/"
derived_from: "LEX-01 keyword register; LEX-03 term-set governance; GM-14 audit findings"
ratification: "PENDING — each row names its RAT"
provenance_of_purpose: "record"
authorship_note: "Compiled by an AI system under AG-000. Each row records a term that the corpus uses in two or more incompatible senses. The recommendations are proposals only. The Curator decides."
hreflang: "en, ar"
---

# LEX-05 · Contested Terms Register

> **Authority.** A **record**. It lists terms whose meaning the corpus has not settled. When a term
> is resolved, its row is marked `resolved` and points to the [keyword register](keyword-register.md)
> entry. The row itself stays in the file.

> **Disclosure first.** Most of these contests arose because agent passes wrote new definitions
> without first reading the existing ones. That is the failure the AG-015 [+] proposal "list before
> concluding absence" is meant to prevent.

---

## 1. Register

| CT | Term | Sense A (where) | Sense B (where) | Harm if left | Recommendation | Ruling |
|---|---|---|---|---|---|---|
| CT-01 | **BCIA** | A bio-computational research programme under remediation, with 7 gates (sources: 00_BCIA_*, source MX-014 §14.4; MX-014 §1 "bio-computational inquiry") | A reading model: Before · Contact · Internalisation · After (BX-000…BX-009) | Two unrelated things share one acronym. The authority of the exclusions and gates attaches to the wrong object | Keep the acronym for the research programme, which is the source sense. Rename the reading model (e.g. "the Encounter Model", `EM`) and retain BX-000…009 under their numbers with a note on the rename | **RAT-28(a)**; DEF-037 |
| CT-02 | **Pillar** | Three pillars (hub `/`, `/charter/pillars/`, Charter §0.2) | Nine MacroLifeTech programmes (MX-014 §1 "nine programs"); DS-00's eight-key menu | Readers cannot tell how many pillars exist | Keep "pillar" for the three. Use "programme" for the nine. Call DS-00's items "menu keys" | RAT-28(e) |
| CT-03 | **MX-004** | Terms of Top Levels (docs/corpus/mx-004) | Academies Charter, cited as "MX-004 §4.3(9)" in source MX-012 and elsewhere | Citations of academy rules resolve to the wrong text | The academies subject moves to MX-029 (done). MX-004 keeps Top Levels | DEF-036; RAT-25 |
| CT-04 | **Series** | A numbered TopTech course series (S01…S52, REG-01) | A generic "document series" (e.g. "the DOC series" in sources); AG-021 "series generation" | Counts drift ("47 series", "50", "52") | "Series" means an `S`-numbered object only. Give every count as computed (Rule 6) | REG-09 note |
| CT-05 | **MX-** prefix | A corpus instrument (MX-000…) | A BCIA book code (MX-MP-01) | A machine misidentifies a book as an instrument | Render book codes only in the `bcia_book_code` field | LEX-04 X-2 |
| CT-06 | **Tier** | Audience tier 1–5 (ST-02) | Precedence tier 1–7 (GM-01); the books' «الشريحة» Tier 1→3 | One word carries three scales | "audience tier", "precedence tier" and "book tier range" must always be qualified | RAT-28(e) |
| CT-07 | **Depth** | 1–5 integer (ST-02) | `depth: macro` string (BX-000 front matter) | Front matter fails schema validation | Use integers only. BX-000…009 need a front-matter fix | GM-15 A-item |
| CT-08 | **Determination** | A licence Compatibility / Charter Conformity decision (ML-2.1 Part D) | Any governance decision in the "Determination Queue" (UI-UX source §12, including appeals and ethics reviews) | A register of "zero Determinations" shows zero while the queue shows many | Keep ML-2.1's narrow sense. Rename the queue the "Decision Queue" | RAT-28(f) |
| CT-09 | **Canonical / live / published** | Status values in ST-02 | "live" in 00_* sources; "published" in BX-000 | Status filters miss documents | Map "live" and "published" to ST-02 values in one migration pass | F-04 sweep |
| CT-10 | **Refusals (three) vs exclusions (five)** | Charter §0.4: three refusals | MX-014 §3: five exclusions; source MX-014 §14.1: four "No …" sentences | "The exclusions" is ambiguous | Name every citation: "Charter refusal n" / "MX-014 exclusion n" / "BCIA bench exclusions" | — |
| CT-11 | **Kernel / standing prompt** | AG-003 (legacy slot) | AG-015 v2026.10.2 | Two prompts both claim to be standing | AG-015 governs. AG-003's legacy subject is a pointer | RAT-25 |

### 1a. Added by the v2027.1 intake (2026-09-30)

| CT | Term | Sense A | Sense B | Recommendation | Ruling |
|---|---|---|---|---|---|
| CT-01 (update) | **BCIA** | — | — | Source supplies **Bio-Computational Intelligence Architecture (MLT-09)**. Sense A is confirmed | RAT-28(a) answered in substance; rename of BCIA-M is RAT-29 |
| CT-12 | **"HX-nn" vs "Hn"** | ML-2.3 harm identities | v2026.10.1 harm list (different subjects) | Map through CON-002. Never treat the two forms as equivalent | DEF-040 |
| CT-13 | **BX-nn vs BX-NNN** | BX-01…24 = substrate *harm entries* | BX-000…018 = *instruments* | Always quote the digit count. Prefer "BX-018 entry BX-05" | LEX-04 |
| CT-14 | **Gate** | Substrate Gate G0–GX (ML-B-1.0) | Seven BCIA remediation gates; also the Scale Gate tiers | Always qualify: "Substrate Gate G2", "remediation gate 3", "Scale Gate Tier 1" | — |
| CT-15 | **Series** | TopTech S01…S52 | MLT-{NN}-S{NN} programme series; "The Eight Series" of BCIA | Programme series are always written with their MLT prefix | CT-04 |
| CT-16 | **D1–D6 / D1–D10 / D1–D5** | HX-000 v2027.1 §12 deep-time properties | Family B "Part J" deep-time obligations; the retired TopTech D1–D10 tags; RB-01 rubric dimensions D1–D5 | Write DT-n for Family B proposals. Never use D1–D10 again | GM-16 D-07 |
| CT-17 | **"The Eight Series"** (BCIA) | Nav v2027.1 BCIA group | Branch D has 10 books (S38–S47) | Curator to explain or correct | — |
| CT-18 | **Signed** | Signed against a published key | "SIGNED 2027-01-14 against [FPR]" | "Signed" is used only where a fingerprint resolves | DEF-042 |

## 2. Rules

- A term enters this register when an agent or reader finds two senses of it in canonical text.
- Until its row is resolved, every use of the term in new text must state which sense is meant.

## 3. Falsifier

This register is incomplete if any other term appears in canonical text with two incompatible senses.

---

**Related:** [LEX-01](keyword-register.md) · [LEX-02](lexicon-entry-standard.md) · [LEX-03](term-set-governance.md) ·
[LEX-04](metax-grammar.md) · [BX-010](../bcia/bx-010-document-zero-and-research-charter.md) · [BX-000](../bcia/bx-000-bcia-charter.md) ·
[GM-13](../00-governance-map/identifier-reallocation-record.md) · [MX-029](../corpus/mx-029-academies-charter.md) ·
[Open questions](../00-governance-map/open-questions-and-ratifications.md)
