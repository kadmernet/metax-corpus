---
doc_id: "ST-28"
title_en: "Component Library Standard"
title_ar: "معيار مكتبة المكوّنات"
family: "standards"
version: "v2026.10.2"
status: "canonical"
authority: "operative-form"
prevailing_text: "en"
audience_tier: 3
depth: 4
evidence_class: "perishable"
review_interval_months: 3
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-25"
domain_tags: ["standards", "components", "design-system", "frontend"]
route: "/library/standards/components/"
derived_from: "DS-00 §§4–6 (as-built inventory); SITE-02 required components; MX-DESIGN-001 mx- vocabulary"
supersedes: ["Index allocation ST-15 'Component Library Standard' (refuge number; see GM-13)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "demo"
authorship_note: "Drafted by an AI system under AG-000. Two vocabularies exist (as-built CSS classes and specified mx- components); this standard maps them and does not choose."
hreflang: "en, ar"
---

# ST-28 · Component Library Standard

> **Authority.** `operative-form`, tier 5. Tokens and as-built classes: [DS-00](../design/ds-00-as-built-token-layer.md)
> (governing). Behaviour: [DS-03](../design/ds-03-responsive-components.md). Page furniture:
> [SITE-02](../site/page-contract.md).

> **Disclosure first.** **Two component vocabularies coexist.** The live demo uses plain classes
> (`.pillar`, `.series-card`, `.arc-step`…). The specifications use an `mx-` prefix
> (`mx-seriescard`, `mx-limitspanel`, `mx-pagestamp`…). Only four `mx-` components are required by
> SITE-02; the rest have no implementation. Recorded as R-59 (component naming).

---

## 1. Rule

**New pages compose from the library rather than inventing shapes.** A new component requires a
DS-03 mobile behaviour, an accessibility pattern ([ST-12](st-12-accessibility-implementation.md)),
and a changelog line.

## 2. The map

| Specified (`mx-`) | As-built class | State |
|---|---|---|
| `mx-pagestamp` | — | **Required** (SITE-02); unbuilt |
| `mx-related` | — | **Required**; unbuilt |
| `mx-exitpair` | — | **Required**; unbuilt |
| `mx-demo` | — | **Required** (B-20); unbuilt |
| `mx-seriescard` | `.series-card` | Built |
| `mx-archetypecard` | `.pillar` | Built |
| `mx-ladder` | `.level`, `.cred-ladder` | Built |
| `mx-arc` | `.arc-step` | Built |
| `mx-railcard` | `.rail` | Built |
| `mx-statusbadge` | `.mm-badge` (`mmb-live`, `mmb-planned`, `mmb-research-preview`, `mmb-gated`) | Built — **single source of truth for status** |
| `mx-limitspanel` | — | Unbuilt |
| `mx-claimcard` | — | Unbuilt |
| `mx-supersededheader` | — | Unbuilt |
| `mx-facetedtable` | `.filters` + table | Partial |
| `mx-imgslot` | `.img-slot` | Built — default rendered state, not a loading state |

## 3. Status badges — invariant

Four words, four treatments, never remapped per property, **never mirrored in RTL**, **always
text plus colour**, never colour alone.

## 4. Chrome freshness

Academies consume shared chrome partials at build time and refresh within **90 days** of a chrome
release ([MX-029 Annex A](../corpus/mx-029-academies-charter.md)).

## 5. Falsifier

Wrong if a page built only from §2 components cannot satisfy SITE-02's twenty acceptance lines.

## 6. Obligation

Build the four required `mx-` components before any page generation.

## 7. Macro register

A shared component library is how a federation keeps one visual language without central
control. It is also how a status word keeps one meaning across a hundred pages.

---

**Related:** [DS-00](../design/ds-00-as-built-token-layer.md) · [DS-03](../design/ds-03-responsive-components.md) ·
[SITE-02](../site/page-contract.md) · [ST-12](st-12-accessibility-implementation.md) ·
[DS-07](../design/ds-07-navigation-geometry.md) · [MX-029](../corpus/mx-029-academies-charter.md) ·
[ST-31](st-31-academy-json-manifest.md) · [ST-21](st-21-performance-budgets.md)
