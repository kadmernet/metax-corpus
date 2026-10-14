---
doc_id: "BX-013"
title_en: "BCIA Observed Taxonomy"
title_ar: "تصنيف BCIA المرصود"
family: "bcia"
version: "v2026.10.2"
status: "draft"
authority: "record"
prevailing_text: "en"
audience_tier: 3
depth: 4
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-26"
domain_tags: ["bcia", "taxonomy", "layers", "front-matter"]
route: "/metax/bcia/taxonomy/"
derived_from: "00_BCIA_TAXONOMY_OBSERVED v2026.08.14; 00_BCIA_FRONT_MATTER_MIGRATION v2026.08.14"
supersedes: ["Legacy slot bx-004-observed-taxonomy (see GM-13)"]
ratification: "PENDING — RAT-02 (gate 2 owner ratification); RAT-25"
provenance_of_purpose: "restoration"
authorship_note: "Compiled by an AI system under AG-000. It reports what the drafts contain and asserts no doctrine."
hreflang: "en, ar"
---

# BX-013 · BCIA Observed Taxonomy

> **Authority.** A **record** of evidence. The three-layer structure is adopted as the **working map**
> because the books declare it on their own covers. It remains subject to the Curator's ratification
> under gate 2.

> **Disclosure first.** The method was a full-text scan. Books 1–6 were scanned complete. Book 7 was
> scanned partially. Books 8–10 were scanned at cover, TOC and introduction level only. Book 9 is
> incomplete in the upload itself. The counts below therefore cover what was ingested, not the full books.

---

## 1. Position

The books have **three layers**. They do not use seven, and they do not use D1–D10. Every D-tag in
earlier TopTech front matter was a provisional invention of TopTech's own and never part of BCIA's
vocabulary.

## 2. Definition — the three layers

| Layer | Arabic (from covers) | Books | Series |
|---|---|---|---|
| `meta-x` | طبقة Meta-X (sub-series «مسار الإتقان», code **MX-MP-01** on Book 1) | 1–3 | S38–S40 |
| `transition` | الطبقة الانتقالية / طبقة التحول | 4–9 | S41–S46 |
| `higher-order` | طبقة المنظومات الأعلى | 10 | S47 |

**The books' working metadata vocabulary** (Finding C): `الطبقة` (layer) · `السلسلة الفرعية`
(sub-series) · `الرقم` (code) · `الشريحة المستهدفة` (tier 1→3) · `درجة العمق` (depth 1→5) · `اللغة`
(Arabic fuṣḥā, voweled).

## 3. Mechanism — front matter

Branch D front matter carries `bcia_layer`, `bcia_book_code`, `tier_range` and `depth_range`, and
**must not** carry `domain_tags: [D…]` (00_BCIA_FRONT_MATTER_MIGRATION, Rule 1). `bcia_layer` accepts
only the three values above. A fourth value requires a gate-2 amendment (Rule 2).

| Series | Book | bcia_layer | bcia_book_code | depth_range |
|---|---|---|---|---|
| S38 | 1 | meta-x | MX-MP-01 | 1-5 |
| S39 | 2 | meta-x | n/a | 1-5 |
| S40 | 3 | meta-x | n/a | per-TOC |
| S41–S46 | 4–9 | transition | n/a | per-TOC |
| S47 | 10 | higher-order | n/a | per-TOC |

## 4. Worked instance

The book code `MX-MP-01` begins with **MX**, the prefix the corpus uses for its governing instruments
(MX-000…MX-029). A reader or machine could take "MX-MP-01" for a corpus instrument. It is not one.
This is logged in [LEX-05](../lexicon/contested-terms.md) as a prefix collision. The proposed fix is to
always render book codes with the field name `bcia_book_code`, never bare.

## 5. Failure modes

- **Ingestion bias:** the evidence table shows AMN and LPN counts only for Books 1–2, the books ingested in full early on. Absence in Books 8–10 may reflect ingestion depth rather than content.
- **Counting inconsistency:** the evidence table in the source lists Book 9 as "0 files" and also as partially present (Ch1, 10–12). The source contradicts itself, and GM-15 records it.
- **Front-matter lag:** S38–S47 pages carrying D-tags after v2026.08.14 are out of project.

## 6. Limits

The taxonomy describes the structure of the books. It does not say whether the layering is correct
as an account of computation.

## 7. Falsifier

The finding is false if a full ingestion of Books 7–10 shows D1–D10 or a seven-layer scheme in use.

## 8. Obligation

- **Curator:** ratify gate 2, or reject it with reasons.
- **Agents:** complete the ingestion of Books 7, 8 and 10 and re-run the scan before gate 2 is closed.

## Macro register

A taxonomy imposed from outside and then taught as the author's own is a quiet form of
misattribution. This record keeps what the books say apart from what earlier TopTech front matter
assigned to them.

---

**Related:** [BX-012](bx-012-remediation-gates-and-public-status.md) · [BX-014](bx-014-notation-freeze.md) ·
[BX-010](bx-010-document-zero-and-research-charter.md) · [REG-09](../registries/reg-09-branch-registry.md) ·
[REG-03](../registries/reg-03-book-registry.md) · [ST-02](../standards/st-02-front-matter-schema.md) ·
[LEX-05](../lexicon/contested-terms.md) · [Keyword register](../lexicon/keyword-register.md)
