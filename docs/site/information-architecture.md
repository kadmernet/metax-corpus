---
doc_id: "SITE-05"
title_en: "Information Architecture — Reconciliation of the Three Estate Models"
title_ar: "معمارية المعلومات — مواءمة النماذج الثلاثة للمنظومة"
family: "site"
version: "v2026.10.2"
status: "draft"
authority: "standard"
prevailing_text: "en"
audience_tier: 4
depth: 4
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-26"
domain_tags: ["site", "information-architecture", "subdomains", "pillars", "routing"]
route: "/about/universe/architecture/"
derived_from: "SITE-01 Route Manifest; Meta-Review Part D (sitemap); MetaX.Academy Platform Data Persistence Architecture; MX-NAV-SPEC v2026.10.1"
ratification: "PENDING — RAT-28(g)"
provenance_of_purpose: "reconciliation"
authorship_note: "Compiled by an AI system under AG-000. It records three incompatible estate models and proposes a mapping between them. It does not replace SITE-01, which remains governing for routes."
hreflang: "en, ar"
---

# SITE-05 · Information Architecture

> **Authority.** A `standard`, subordinate to [SITE-01](route-manifest.md). **SITE-01 governs every
> route.** This file explains how SITE-01's model relates to the other two models found in the sources.

> **Disclosure first.** The sources describe the estate in **three incompatible ways**. The page-spec
> files for TopTech, the hub and the academy subdomains, cited in the legacy plan, are **not held**.
> Their texts could not be retrieved, and they appear here only as pointers.

---

## 1. Position — the three models

| Model | Source | Shape | Top-level units |
|---|---|---|---|
| **M-A: Single domain, nine pillar keys** | SITE-01, MX-NAV-SPEC v2026.10.1 | `metax.academy/{pillar}/{group}/{leaf}/` | toptech · method · ascent · metax · academies · credentials · library · license · about (9) |
| **M-B: Hub with eight properties** | Meta-Review Part D | Subdomains: `toptech.metax.academy`, `bcia.metax.academy`, etc. | "all eight properties" |
| **M-C: Wildcard academy subdomains** | Platform Data Persistence §1 | `*.metax.academy` served by a single Worker; academy slugs at subdomain level | N academies |

The "three pillars" of the hub home page and Charter §0.2 are a **conceptual** grouping, not a
routing unit. See [LEX-05 CT-02](../lexicon/contested-terms.md).

## 2. Definition — proposed mapping

| Object | M-A (governing) | M-B equivalent | Notes |
|---|---|---|---|
| TopTech series | `/toptech/s/{S##}-{slug}/` | `toptech.metax.academy/s/{id}-{slug}/` | Same identifier. The host differs |
| BCIA status | `/metax/bcia/status/` | `bcia.metax.academy/status/` (Meta-Review B.9) | **X-R1** (fixed v2026.10.2): the BX-010…017 drafts used `/bcia/…`, which is in neither model. They have been corrected to `/metax/bcia/…`. BX-000 still uses `/bcia/` |
| Refused inference | *(no M-A route)* | `/refused-inference/` (M-B hub) | **X-R2**: add `/metax/bcia/refused-inference/` to SITE-01 |
| Human-subject exclusion | `/method/notation/human-subject-exclusion/` (MX-014) | — | BX-011 route should be a child of this |
| Licence | `/license/…` | `/license/…` | Agree |
| Academy | `/academies/{slug}/` | `{slug}.metax.academy` (M-C) | **X-R3**: M-C needs 1 Worker and a wildcard. M-A is pure static. See ST-28 / R-59(a) |

## 3. Mechanism

1. Until RAT-28(g) is decided, **M-A is authoritative** for every published link.
2. M-B and M-C addresses may appear only in design documents, marked "proposed host".
3. If a subdomain model is later adopted, every M-A path gets a permanent 301 to its host form. **Both forms resolve for ever** (LEX-04, slug stability).

## 4. Worked instance

A BCIA lesson links to the status page. Under M-A it links to `/metax/bcia/status/`. The legacy
redirect `/bcia-status.html → /metax/bcia/status/` (SITE-01 §1.5) already assumes M-A, and BX-012's
front-matter route now agrees with it.

## 5. Failure modes

- **Silent host migration:** moving to subdomains without 301s. This breaks every citation.
- **Count confusion:** "nine pillars", "eight properties" and "three pillars" presented as a single count.
- **Relative paths across hosts:** a relative link that works on one host fails on another (SITE-01 §1.3).

## 6. Limits

This file does not add or remove any route. Only SITE-01 does that.

## 7. Falsifier

The mapping is wrong if any object in §2 has an M-A route different from the one shown.

## 8. Obligation

The Curator chooses M-A, M-B, or M-A with M-C for academies only, and SITE-01 is updated to match.

## Macro register

An estate that describes itself in three incompatible ways gives readers and crawlers no reliable
picture of where its content lives. Settling on one model is a precondition for the estate being
citable at all.

## Annex — unretrievable page specifications (pointers)

| Legacy path | State |
|---|---|
| `page-spec-toptech.md` | not held. The nearest text is MetaX.Academy_Page_Content_Specification (sources) |
| `page-spec-hub.md` | not held. The nearest text is Meta-Review D.1.1 |
| `page-spec-academy-subdomains.md` | not held. The nearest text is Platform Data Persistence §1 |

---

**Related:** [SITE-01](route-manifest.md) · [SITE-02](page-contract.md) · [SITE-03](routing-law.md) · [SITE-04](demo-notice.md) ·
[LEX-04](../lexicon/metax-grammar.md) · [LEX-05](../lexicon/contested-terms.md) · [MX-029](../corpus/mx-029-academies-charter.md) ·
[ST-28](../standards/st-28-component-library.md) · [BX-012](../bcia/bx-012-remediation-gates-and-public-status.md)
