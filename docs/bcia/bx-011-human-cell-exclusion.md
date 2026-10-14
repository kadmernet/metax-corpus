---
doc_id: "BX-011"
title_en: "BCIA Human-Cell Exclusion"
title_ar: "استثناء الخلايا البشرية في BCIA"
family: "bcia"
version: "v2026.10.2"
status: "draft"
authority: "governing"
prevailing_text: "en"
audience_tier: 1
depth: 3
evidence_class: "durable"
review_interval_months: 24
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-26"
domain_tags: ["bcia", "exclusions", "human-cell", "research-ethics"]
route: "/method/notation/human-subject-exclusion/bcia/"
derived_from: "Source MX-014 §14.1; 00_BCIA_PUBLIC_STATUS 'Absolute exclusions'; MX-014 §3 exclusion 2"
supersedes: ["Legacy slot bx-002-human-cell-exclusion (cited by MX-014 §3; path now holds BCIA-M 'Contact Phase'; see GM-13)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "restoration"
authorship_note: "Drafted by an AI system under AG-000. The exclusion text is quoted verbatim from the sources and must never be paraphrased."
hreflang: "en, ar"
---

# BX-011 · BCIA Human-Cell Exclusion

> **Authority.** `governing`. It is the specific text of [MX-014](../corpus/mx-014-research-ethics-and-exclusions.md)
> §3 exclusion 2. The exclusion also lies within the three refusals (Charter §0.4), which sit **outside
> precedence** and cannot be weakened by any instrument ([GM-01 §5](../00-governance-map/precedence-and-conflict-rules.md)).

> **Disclosure first.** MX-014 §3 links this exclusion to `bx-002-human-cell-exclusion.md`. That file
> now holds the BCIA-M "Contact Phase" document, so **the corpus's own citation of its most absolute
> rule currently resolves to the wrong text.** That is recorded under DEF-036/DEF-039, and a pointer
> will be placed at the legacy path.

---

## 1. Position — the text, verbatim

> **Human-cell exclusion: absolute.**
> **No wet-lab protocols. No substrate cultivation. No synthetic-biology bench instruction. No organism engineering.**

Source MX-014 §14.1 adds: *"The human-cell exclusion in full, stated verbatim wherever bio-adjacent
material appears, never paraphrased and never collapsed. These are binding curriculum policy enforced
at review; a lesson violating them is pulled and logged in the Corrections Log."*

## 2. Definition

- **Human cell / human-derived material:** any cell, tissue, cell line, organoid, genetic material or derived dataset originating from a human being.
- **Bench instruction:** any text specific enough that a reader could perform the procedure.
- **Bio-adjacent material:** any page that mentions a biological substrate for computation. Every Branch D page qualifies.

The exclusion also covers theoretical modelling that proceeds **through** human-derived material
(MX-014 §3). A computational principle may be discussed in the abstract. A design for a human-cell
system may not, even on paper.

## 3. Mechanism

1. Every Branch D page carries the §1 block verbatim. Its front matter carries `human_cell_exclusion: "affirmed"` (00_BCIA_FRONT_MATTER_MIGRATION).
2. [RB-06](../rubrics/rb-06-structural-review.md) gate G5 fails any bio-adjacent page where the block is missing or its text differs by even one character.
3. A breach is pulled at once and logged in the [Corrections Log](../00-governance-map/corrections-log.md). There is no grace period.

## 4. Worked instance

Book 1 contains the phrase «مع حفظ العهد: لا خلايا إنسانية» ("keeping the covenant: no human cells")
(00_BCIA_TAXONOMY_OBSERVED, Finding B). The books therefore carry the exclusion themselves. The
English front matter must quote the full §1 block, not this summary. Using the summary alone would
count as "collapsing" under §14.1.

## 5. Failure modes

- **Paraphrase drift:** "we avoid human cells where possible." That is a breach.
- **Citation laundering:** a lesson describes a published human-cell study (e.g. the 2018 He Jiankui case) as a method rather than as a cautionary record. History is permitted. Protocol is not.
- **Collapsed block:** only "no human cells" appears, without the four "No …" sentences.

## 6. Limits

The exclusion does not prevent discussion of the ethics, history or regulation of human-cell
research. It does not cover non-human, non-cellular or purely silicon computation, although wet-lab
instruction is excluded for all substrates.

## 7. Falsifier

The exclusion has failed if any published MetaX page provides bench-level instruction on any
biological substrate, or if any bio-adjacent page lacks the verbatim block.

## 8. Obligation

- **Agents:** paste §1 verbatim. Never generate it from memory.
- **Curator:** repoint MX-014 §3's link to this file (see the GM-15 review).

## Macro register

Under **HX-22** (pre-emption of the successor; corrected 2026-09-30 from "HX-21", which ML-2.3 assigns to corpus poisoning, see DEF-040), a successor inherits whatever this estate normalises. A one-sentence exclusion
repeated everywhere is cheap. A single exception, once published, cannot be withdrawn from the record.

---

**Related:** [MX-014](../corpus/mx-014-research-ethics-and-exclusions.md) · [MX-000](../corpus/mx-000-charter.md) ·
[BX-010](bx-010-document-zero-and-research-charter.md) · [BX-012](bx-012-remediation-gates-and-public-status.md) ·
[BX-017](bx-017-contribution-without-a-laboratory.md) · [RB-06](../rubrics/rb-06-structural-review.md) ·
[Corrections log](../00-governance-map/corrections-log.md) · [GM-01](../00-governance-map/precedence-and-conflict-rules.md) ·
[LEX-05](../lexicon/contested-terms.md)
