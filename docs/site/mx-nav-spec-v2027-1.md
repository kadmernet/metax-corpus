---
doc_id: "SITE-06"
source_designation: "MX-NAV-SPEC v2027.1 (delta)"
title_en: "MX-NAV-SPEC v2027.1 — Navigation Delta for the license, metax and toptech Pillars"
title_ar: "مواصفة التنقّل v2027.1"
family: "site"
version: "v2027.1"
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
last_reviewed: "2026-09-30"
domain_tags: ["site", "navigation", "routes", "license-pillar", "metax-pillar", "reader"]
route: "/about/universe/nav/"
supersedes: ["MX-NAV-SPEC v2026.10.1 §3 for the license, metax and toptech pillars only"]
derived_from: "sources/METAX_CORPUS_SOURCE_BUNDLE_v2027.1.md Part 2"
human_read: "none"
conformance_state: "partial"
ratification: "PENDING — RAT-19 (method pillar), RAT-35"
authorship_note: "Compiled by an AI system under AG-000. One structural correction is applied to the source (§2, D-13). Everything else is reproduced as specified."
hreflang: "en, ar"
---

# SITE-06 · MX-NAV-SPEC v2027.1 (delta)

> **Authority.** A standard, subordinate to [SITE-01](route-manifest.md), which is amended by this
> delta for three pillars. §§1, 2 and 4–10 of v2026.10.1 and the routing law carry forward unchanged.
> **Nine pillars, unchanged.**

> **Disclosure first.** As written, the source would have put the **unsigned, unratified ML-2.4**
> in the license pillar as *"The Instrument (ML-2.4)" · badge `live`*, filed **ML-2.3**, the licence
> of record, under *"Falsification & History"* labelled *superseded*, and 301-redirected
> `/license/ml-2-3/*` there. That misrepresents what a licensee is bound by. **It is corrected in §2**
> (GM-16 D-13, DEF-046). None of the routes below exists as a page.

---

## 1. What carries forward

The routing law, trailing-slash canonical form, root-absolute paths, `navKeyFor()` and the Arabic
mirror all carry forward unchanged ([SITE-01 §1](route-manifest.md), [SITE-03](routing-law.md)).

## 2. `license` pillar (corrected)

| Group (hub) | Badge | Leaves |
|---|---|---|
| **The Instrument of Record (ML-2.3)** `/license/ml-2-3/` | **live** | Parts 0, A–H · Schedules 1–5 · `ml-2-3.txt` · `license.json` |
| **Pending Amendment (ML-2.4)** `/license/ml-2-4/` | **draft** | §§1–7 · Track 1 / Track 2 · comment period (CPF-1) · `ml-2-4.txt` · `license.json` |
| **The Register (HX-000 v2027.1)** `/license/harms/` | draft | Strata I–VII (`stratum-i-cognitive` … `stratum-vii-custodial`) · falsifiers · rejected candidates · **concordance (CON-002)** · `hx-000.json` |
| **Operative Machinery** `/license/machinery/` | live | absolutes · roles · scale gate · conditions vs covenants · cure · riba · determinations · welfare reviewer (substrate only) |
| **Compliance** `/license/statement/` | live | form · generator · ours (BHS-2027-001, draft) · compliance file (CF-1) · comment-period format (CPF-1) · examples · compatibility and SPDX |
| **Profiles** `/license/profiles/` | draft | ML-B-1.0 · rationale · conformance · authoring |
| **Falsification & History** `/license/falsification/` | live | objections · withdrawals · defects (ML-D-nnn) · changelog 2.1 → 2.3 → 2.4 · **ML-2.2 (never adopted)** · **ML-2.1 (predecessor)** · open questions |

**Corrections against the source:**
- "Stratum VI · Inheritance" becomes **"Successor"**, and **Stratum VII Custodial** is added, to match the adopted register.
- The source's stratum labels (e.g. "III · HX-07–09,13") follow Family B's register for V and VI and are replaced.

## 3. `metax` pillar

Groups as in the source:
- **The Umbrella** (7 leaves).
- **Programs**: nine hubs `/metax/programs/{agora|mana|metabolism|soma|paideia|athar|afaq|mizan|bcia}/`, each with 7 leaves.
- **BCIA** `/metax/bcia/`: document-zero · what-it-is · series · roadmap · charter · governance · notation · taxonomy · licence · bibliography · contribution · gateway.
- **The Honesty Layer** `/metax/bcia/status/`: remediation · audit · protocol · defects · open-problems · refused-inference.

| Route | Holds |
|---|---|
| `/metax/bcia/document-zero/`, `/metax/bcia/charter/` | [BX-010](../bcia/bx-010-document-zero-and-research-charter.md) |
| `/metax/bcia/taxonomy/` | [BX-013](../bcia/bx-013-observed-taxonomy.md) |
| `/metax/bcia/notation/` | [BX-014](../bcia/bx-014-notation-freeze.md) |
| `/metax/bcia/licence/` | [ML-B-1.0](../license/ml-b-1-0.md) + [BX-018](../bcia/bx-018-register-of-substrate-harms.md) |
| `/metax/bcia/contribution/` | [BX-017](../bcia/bx-017-contribution-without-a-laboratory.md) |
| `/metax/bcia/status/` and `…/remediation/` | [BX-012](../bcia/bx-012-remediation-gates-and-public-status.md) |
| `/metax/bcia/status/audit/`, `…/open-problems/` | [BX-015](../bcia/bx-015-critical-audit-and-open-problems.md) |
| `/metax/bcia/status/refused-inference/` | [BX-016](../bcia/bx-016-refused-inference.md) |
| `/metax/bcia/series/` ("The Eight Series") | **Unexplained count.** Branch D has 10 books (S38–S47). LEX-05 CT-17 |

**Route reconciliation.** BX-015, BX-016 and BX-017 had front-matter routes from v2026.10.2. They
are realigned to the paths above.

## 4. `toptech` · The Reader group

Twelve leaves under `/toptech/reader/`, as in the source. They document MX-READER-01
([SITE-07](mx-site-design-v2027-1.md#mx-reader-01)). **The reader has not been built.**

## 5. Census

| Pillar | Total (source) |
|---|---|
| metax | 110 (41 + 63 programme leaves + hubs) |
| license | 58 → **60** after the correction (+ ML-2.3 hub, + stratum VII) |
| others | as in the source |
| **EN total** | **428 → ≈430** |

Plus an Arabic mirror. File headroom is about 2,400 against the 20,000 file limit. The binding
constraint is still Workers requests. **Counts are to be computed, not typed** (Rule 6). These
figures are the source's estimates.

## 6. Redirects

| Source line | Disposition |
|---|---|
| `/license/ml-2-3/* → /license/falsification/ml-2-3/ 301` | **Refused** (D-13) |
| `/license/ml-2-2/* → /license/falsification/ml-2-2/ 301` | Adopted |
| `/metax/programs/bcia → /metax/bcia/ 301` | Adopted |
| `/macrolifetach/* → /metax/:splat 301` | Adopted. This is the only permitted survival of the misspelling |

---

**Related:** [SITE-01](route-manifest.md) · [SITE-03](routing-law.md) · [SITE-05](information-architecture.md) · [SITE-07](mx-site-design-v2027-1.md) ·
[ML-2.3](../license/ml-2-3.md) · [ML-2.4](../license/ml-2-4.md) · [MLT-000](../metax/programs/mlt-000-programme-register.md) · [GM-16](../00-governance-map/source-intake-v2027-1.md)
