---
doc_id: "DS-03"
title_en: "Responsive Component Behaviour"
title_ar: "سلوك المكوّنات المتجاوب"
family: "design-system"
version: "v2026.09.2"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 3
evidence_class: "semi-durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.1"
derived_from: ["MX-DESIGN-001 Part 3", "MX-DESIGN-001 Part 7"]
supersedes: ["Component notes, v2026.08.12"]
last_reviewed: "2026-08-30"
domain_tags: ["design", "frontend", "accessibility"]
ai_disclosure_url: "../corpus/mx-007-ai-use-and-disclosure.md"
hreflang: "en, ar"
---

# DS-03 — Responsive Component Behaviour

**Governs:** how each named component behaves from 360 px upward. Breakpoint tokens are at
[DS-01 §1](ds-01-foundations-and-tokens.md#1-mobile-first-and-what-that-actually-constrains).
Component APIs are at [ST-15](../standards/st-15-component-library.md).

Every component is authored at `xs` first. A component with no mobile counterpart fails the
build. Two rules below are content decisions dressed as layout decisions, and they are marked as
such — they may not be overridden for space.

---

## §3.1 The mega-nav — the hardest case

| Breakpoint | Behaviour |
|---|---|
| `< md` | Full-screen drawer from the **inline-end** edge, **pillar-first**: seven pillar rows, each expanding in place to reveal its sections |
| `≥ lg` | Seven-pillar horizontal bar, drop panels capped at **4 columns × 7 links**, opening on 120 ms fade with **no slide** |

**`mx-statusbadge` is preserved at every level, on every breakpoint.** Status is structural and
**must not be a desktop luxury** — a phone reader deciding whether to trust a page needs the
`GATED` or `DEFECT` marker exactly as much as a desktop reader does, and arguably more, because
they are likelier to be reading in transit.

The utility bar (Start Here · Verify · Search · EN/ع) becomes a fixed four-icon row at the
drawer's foot, **always reachable by thumb**.

---

## §3.2 Component matrix

| Component | `xs` | `md` | `lg` |
|---|---|---|---|
| `mx-branchmatrix` | 5 full-width cards | 2 × 3 grid | True 5-column matrix |
| `mx-facetedtable` | Card list, **3 highest-value fields** visible, rest behind a disclosure | Horizontally scrollable table, **sticky first column** | Full table with column sorting |
| — its facet rail | Bottom sheet | Bottom sheet | Persistent inline-start rail |
| `mx-lessonarc` | Six-step accordion, **one beat open at a time** | ↓ | Two-column stepper with persistent progress rail |
| `mx-ladder` | **Vertical** | **Vertical** | **Vertical** + inline-start progress rail and rung annotations |
| `mx-leveltable` (5 academy levels) | Five stacked level cards, each carrying entry criteria, rights, obligations and downgrade triggers as labelled pairs | ↑ | Table |
| `mx-limitspanel` | **Single column** | **Single column** | **Single column** |
| `mx-defectcard` | **Single column** | **Single column** | **Single column** |

`mx-facetedtable` is used by the catalog, the directory and the record — one component, three
surfaces, which is why its mobile disclosure rule is defined here rather than per-page.

---

## §3.3 The two rules that are content decisions

### `mx-ladder` never rotates

The Ascent stays vertical at **every** breakpoint. Rotating it horizontally on wide screens
**would be a lie about the content**: the Ascent is a climb, the rungs are ordered and
dependent, and a horizontal row of ten items reads as a menu of alternatives. The layout carries
a claim about the structure of the material, so the layout is not free to change.

### `mx-limitspanel` and `mx-defectcard` are never compressed

The two highest-fidelity components in the estate are single-column **at any width**. They are
never placed in a grid, never truncated, never collapsed behind a disclosure, and never
abbreviated for space.

The reason is [Charter §0.3](../corpus/mx-000-charter.md#03-shared-dna): declared limits and
published defects are two of the four Shared DNA properties. A limits panel compressed into a
two-column grid to fit a viewport has been editorially downgraded by a layout decision — and
that is exactly how an institution stops publishing its own weaknesses without ever deciding to.
Space pressure is the mechanism; nobody has to intend it.

---

## §3.4 Academy subdomains

Each chartered academy receives `{slug}.metax.academy`, provisioned at charter grant, static, on
the **shared** component library, driven by its `academy.json` manifest
([ST-18](../standards/st-18-academy-json-manifest.md)). The manifest supplies name, curator,
level, accent hue index, language set, curriculum index and audit history; the build derives the
theme ramp, the routes and the directory entry from it.

### §3.4.1 The four things an academy cannot change

1. `mx-statusbadge` colour semantics
2. The shape and copy of `mx-limitspanel` and the Bridge card
3. The footer standing strip showing **level and last audit date**
4. Anything on `auth.` or `pay.`

Items 2 and 3 are the honesty surfaces, and item 1 is what makes them legible. An academy that
could soften its own limits panel or hide its own audit date would be an academy that had bought
the appearance of MetaX standing without accepting its cost.

### §3.4.2 Standing notices

| Level | Notice |
|---|---|
| Sandbox | **Persistent, non-dismissible** banner; excluded from search indexing |
| Provisional | Lighter standing notice |
| Chartered | May add a **verified** custom domain — which changes the URL and **not a single component** |

### §3.4.3 Admin lives elsewhere

The academy admin surface is at `me.metax.academy/academy/{slug}/`, **not** on the academy's own
subdomain. This keeps every academy subdomain entirely static and puts every privileged operation
behind one audited plane
([ST-19 §5.1](../standards/st-19-two-plane-architecture.md#51-the-readwrite-seam)).

---

## §3.5 Conformance

| Rule | Enforced by | Failure |
|---|---|---|
| Mobile counterpart exists for every component | Desktop-only-CSS lint | Build failure |
| `mx-statusbadge` present at every nav level | Nav render test at `xs` | Build failure |
| `mx-ladder` vertical at all widths | Layout assertion | Build failure |
| `mx-limitspanel` / `mx-defectcard` single-column | Layout assertion | Build failure |
| Academy override of the four locked items | Manifest and token validation | Build failure |
| Touch targets ≥ 44 × 44 px, 8 px separation | Automated hit-area audit | Build failure |

---

**Related:** [DS-01 Foundations and Tokens](ds-01-foundations-and-tokens.md) ·
[DS-02 Motion and Attention](ds-02-motion-and-attention.md) ·
[ST-15 Component Library](../standards/st-15-component-library.md) ·
[ST-18 academy.json](../standards/st-18-academy-json-manifest.md) ·
[Page Specs — Academy Subdomains](../site/page-spec-academy-subdomains.md)

*Curated by Maher. Two components in this document refuse to compress. That refusal is the
document's actual subject.*
