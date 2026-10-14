---
doc_id: "SITE-07"
source_designation: "MX-SITE-DESIGN v2027.1 + MX-READER-01 v1.0"
title_en: "MX-SITE-DESIGN v2027.1 (Carousels and Animated Text) and MX-READER-01 (Course-Series Reader)"
title_ar: "تصميم الموقع v2027.1 وقارئ سلاسل الدورات"
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
domain_tags: ["site", "design-system", "carousel", "performance", "reader", "static-build"]
route: "/about/universe/design/"
supersedes: ["MX-SITE-DESIGN v2026.09.3 §§2, 6, 7, 8 — on ratification only; §1 token layer carried byte-identical"]
derived_from: "sources/METAX_CORPUS_SOURCE_BUNDLE_v2027.1.md Parts 1 and 6"
human_read: "none"
conformance_state: "unmet"
ratification: "PENDING — RAT-35 (carousel trade)"
authorship_note: "Compiled by an AI system under AG-000. The full CSS and JS are in the source and are not duplicated here. This file records the rules, the conflicts and the recommended alternative."
hreflang: "en, ar"
---

# SITE-07 · MX-SITE-DESIGN v2027.1 and MX-READER-01

> **Authority.** A standard, subordinate to [ST-21](../standards/st-21-performance-budgets.md) and
> [ST-19](../standards/st-19-two-plane-architecture.md). Those standards are higher on the ladder,
> so **this document cannot amend their budgets by declaration**.

> **Disclosure first. `conformance_state: unmet`.** This is the only document that is unmet because
> of what it requires. OwlCarousel2 2.3.4 plus jQuery 3.7.1 come to about **118 KB** from two
> third-party origins, against a **12 KB first-party** content-plane budget. The source's mitigation
> (self-host, defer, and a declared 140 KB ceiling on carousel pages "recorded as an amendment to
> ST-21") closes **provenance**, not **weight**. An amendment to ST-21 can only be made in ST-21,
> under ST-15, so it is not made here (DEF-2027-001 imported; RAT-35).

---

## Part 1 · Carousels and animated text

### 1.1 New tokens
`--owl-dot`, `--owl-dot-active`, `--owl-nav-bg`, `--owl-nav-line`, `--slide-dur: 7200ms`,
`--slide-fade: 600ms`, `--word-step: 70ms`, `--word-rise: 22px`, plus `--grad-verify`, `--grad-vault`
and `--grad-ledger` restated. These are **appended**. The v2026.09.3 token layer is unchanged.

### 1.2 Hero carousel rules (the source's rules, adopted as constraints whatever is decided on Owl)

1. One item per view.
2. A minimum of 2 slides and a maximum of 5. A one-slide hero has no carousel.
3. Each slide has at most 1 H1, 1 deck and 2 actions, with no form, price or countdown.
4. Pause on hover and focus. **With `prefers-reduced-motion`, no carousel at all**: slides stack as sections.
5. Dots on the hero; arrows on card carousels only.
6. **No slide may be the only location of a fact.**
7. ARIA: `aria-roledescription="carousel"`, `role="group"` per slide, and a pause button as the first focusable element.
8. **No carousel** on Auth, Pay, Verify records, `/license/` or `/library/record/`.

*The first slide is server-rendered, and the others carry `hidden` until initialised, so a no-JS reader sees one complete hero.*

### 1.3 Animated text
`data-anim="rise"` applies to the H1 only, word by word, capped at 14 words. `fade` applies to the
deck, actions and stamp. Each runs once on entry and never loops. **The word split happens at build
time**, and `aria-label` carries the unsplit H1. Reduced motion disables both.

### 1.4 Card carousels (below 1000px only)
`.pillar`, `.series-card`, `.feature` and `.rail` are carousels on mobile and tablet and **grids at
≥1000px, where the instance is destroyed** (no clones in the DOM). These are never carousels: `.level`,
`.arc-step`, `.cred-ladder`, `.filters`, and anything in `/license/` or `/library/record/`.

### 1.5 Conflicts with higher instruments

| Conflict | Higher instrument | Status |
|---|---|---|
| About 118 KB of third-party JS against a 12 KB first-party budget | ST-21, ST-19 §3.1 | **Unresolved** |
| `autoplay: true` at 7.2 s | DS-02 (motion as attention), MX-023 (no engagement mechanics) | **Unresolved**. Autoplay is an attention-capture device whatever the content |
| Rule 6 cannot be enforced by any build check | ST-13 | Disclosed by the source |
| The "renders without JavaScript" thesis | SITE-02 acceptance criteria | Survivable only through rules 4 and 6 |

### 1.6 Recommended alternative (the "smaller change" the source offers)
- A **static hero**: slide 1 rendered, slides 2–n stacked as `<section>`s.
- An optional **CSS-only cross-fade** using `:target` or `animation`, about 1 KB, **with no autoplay**.
- Card rows use native `scroll-snap` below 1000px and grids above. That is zero JS and gives the same peek affordance.

This meets every §1.2 rule and keeps the 12 KB budget. **Recommended for adoption under RAT-35.**

<a id="mx-reader-01"></a>
## Part 2 · MX-READER-01 · the Course-Series Reader (specification; not built)

**What it is.** A static build that turns one Markdown directory tree into a complete course-series
reader, with no database, server or account. The licence named in the source is ML-2.4 plus
CC BY-SA 4.0 for the template. Read here as **ML-2.3 until ML-2.4 is ratified**, with CC BY-SA
compatibility open under RAT-27(a).

**Input contract.**
- `series.md`
- `c{NN}-{slug}/course.md` plus six lessons: l1-what-is · l2-why · l3-how · l4-lab · l5-artifact · l6-scenario
- Mandatory files: `limits.md`, `bridge.md`, `capstone.md`, `objections.md`, `sources.md`
- Optional `ar/` mirror

**The build fails** if a mandatory file is missing, a beat heading is missing, a claim card lacks a
falsifier, a count is typed rather than written as `{{count:…}}`, or a source is undated. *This is
specified and not built. No build exists and the package `@metax/series-reader` is unpublished
(GM-16 Q7).*

**Front matter (series.md)** includes `human_read`, `conformance_state`, `figures_read`,
`estimated_hours_basis` ("author estimate, unvalidated — P1"), and `prerequisites` with self-tests.
**Note:** the source's example uses `series_id: "S014"`, three digits. The canon uses `S14`.
[LEX-04 X-1](../lexicon/metax-grammar.md) and RAT-27(b) apply.

**Features.**
- A TOC with progress and keyboard navigation.
- **Epistemic chrome:** falsifiers visible on every claim card; `[VERIFY]` age chips that turn amber past the interval and strike through past twice the interval.
- **Limits rendered immediately before the Bridge, and not reorderable.**
- The scenario decision tree is revealed after completion.
- **No scoring, grade, streak or leaderboard.**
- Offline service worker, a whole-series print stylesheet, and an RTL mirror that never silently serves English.
- JSON emitted: series, courses, lessons, claims, sources, search-index, status.

**What it refuses.**
- Accounts, sync, analytics, comments and an embedded video player.
- **Completion certificates.** A reader that can issue a credential is a credential mill.

**Academy constraints.** One accent hue index (0–11) and a wordmark. Badge semantics, the
Limits/Bridge order, falsifier rendering, decay chips, the untranslated notice and the standing
strip may not be changed. `academy.json` is validated ([ST-31](../standards/st-31-academy-json-manifest.md)).

**Deploy.** Plain files on any static host. *The reader has no runtime, so a series outlives the
reader project.*

**One unresolved interaction.** The reader uses the §1.4 card carousels, and inherits the budget
conflict unless RAT-35 adopts §1.6.

---

**Related:** [ST-21](../standards/st-21-performance-budgets.md) · [ST-19](../standards/st-19-two-plane-architecture.md) · [DS-00](../design/ds-00-as-built-token-layer.md) ·
[DS-02](../design/ds-02-motion-and-attention.md) · [MX-023](../corpus/mx-023-attention-and-human-sovereignty.md) · [ST-28](../standards/st-28-component-library.md) ·
[ST-31](../standards/st-31-academy-json-manifest.md) · [SITE-06](mx-nav-spec-v2027-1.md) · [GM-16](../00-governance-map/source-intake-v2027-1.md)
