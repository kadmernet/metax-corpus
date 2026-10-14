---
doc_id: "REG-14"
title_en: "REG-14 · Programme Series Registry (MLT-NN-SNN, MLT-NN-VNN)"
title_ar: "REG-14 · سجلّ سلاسل البرامج [AR-DRAFT]"
family: "registries"
version: "v2026.10.3"
status: "draft"
authority: "record"
prevailing_text: "en"
audience_tier: 4
depth: 3
evidence_class: "perishable"
review_interval_months: 3
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-08"
domain_tags: ["registry", "MLT", "programme-series", "identifiers"]
route: "/metax/programs/series/"
human_read: "none"
conformance_state: "met"
derived_from: "MLT-000 §1 identifier grammar; Bundle Part 5 §5.2 (MLT-01 'Series MLT-01-S01 … S04 planned')"
authorship_note: "Opened by an AI system under AG-000 to close GM-17 M-40. Records only identifiers declared in sources. Allocates none."
hreflang: "en, ar"
---

# REG-14 · Programme Series Registry

> **Authority.** A **record**. It holds every `MLT-{NN}-S{NN}` and `MLT-{NN}-V{NN}` identifier from the
> moment it is first declared. Numbers are immortal (ST-01 Rule 2). **This namespace is distinct from
> TopTech's S01…S52** ([REG-01](reg-01-series-registry.md)). Always write the MLT prefix (LEX-05 CT-15).

---

## 1. Register

| Id | Programme | Title | Declared in | State |
|---|---|---|---|---|
| MLT-01-S01 | Agora | *(untitled)* | Bundle §5.2 MLT-01 | planned, unspecified |
| MLT-01-S02 | Agora | *(untitled)* | same | planned, unspecified |
| MLT-01-S03 | Agora | *(untitled)* | same | planned, unspecified |
| MLT-01-S04 | Agora | *(untitled)* | same | planned, unspecified |

No other programme series or volume is declared in any held source. **MLT-09's BCIA books are not MLT-09
series.** They keep their TopTech identifiers (S38–S47) and BCIA book codes (REG-03).

## 2. Allocation rule

The next identifier in a programme is `max(existing) + 1`. An identifier exists from the moment it appears in any
instrument. **A planned identifier never withdrawn stays planned for ever** and is shown as such. It is never re-used.

## 3. Falsifier

Incomplete if any held text declares an `MLT-NN-SNN` or `MLT-NN-VNN` not listed in §1.

---

**Related:** [MLT-000](../metax/programs/mlt-000-programme-register.md) · [REG-01](reg-01-series-registry.md) · [ST-01](../standards/st-01-identifier-and-url-grammar.md) · [LEX-05](../lexicon/contested-terms.md)
