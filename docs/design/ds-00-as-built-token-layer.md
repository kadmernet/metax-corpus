---
doc_id: "DS-00"
title_en: "The As-Built Token Layer and Page Contract"
title_ar: "طبقة الرموز التصميمية كما هي مبنية وعقد الصفحة"
family: "design"
version: "v2026.09.4"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 3
depth: 4
evidence_class: "perishable"
review_interval_months: 3
curator: "Maher"
license: "ML-2.3"
supersedes: ["DS-01 §palette", "DS-01 §gradient-system", "MX-DESIGN-001 Part 1 (palette)", "MX-DESIGN-001 Part 2 (motion tiers)"]
derived_from: "Direct read of live index.html, css/style.css, js/components.js, js/site.js"
last_reviewed: "2026-09-02"
domain_tags: ["design", "tokens", "as-built", "accessibility"]
hreflang: "en, ar"
---

# DS-00 — The As-Built Token Layer and Page Contract

**This document is not a proposal.** Every value in it was read out of the live site's own
`css/style.css`, `index.html`, `js/components.js` and `js/site.js`. Where it disagrees with
[DS-01](./ds-01-foundations-and-tokens.md) or with MX-DESIGN-001, **this document governs** and
the disagreement is recorded in the [Corrections Log](../00-governance-map/corrections-log.md),
not resolved by preference.

> ## Why DS-00 and not a corrected DS-01
>
> [MX-000 §0.8](../corpus/mx-000-charter.md) forbids silent edits and requires superseded text to
> remain retrievable. DS-01 was not wrong in a detail; it described **a different design system**
> — an "Ink-and-Paper" identity with ten gradients and a warm-gold palette that exists nowhere in
> the code. Editing DS-01 until it agreed would destroy the evidence of how long the estate was
> wrong, which is the only number that reveals whether the correction obligation is real.
>
> DS-01 therefore keeps its text and gains a non-governing banner on its palette and gradient
> sections. This document takes number **DS-00** because it sits beneath the whole design family:
> everything in DS-01…DS-06 that survives, survives on top of these tokens.

> ## Evidence class: perishable, and this is a standing correction
>
> A claim about the live system is **not durable evidence**. It decays the moment someone commits
> a stylesheet change, and this document is therefore `perishable` with a three-month review
> under [ST-05](../standards/st-05-decay-and-review-intervals.md) — unlike DS-01, which was
> written as though a design description were durable. That misclassification is part of what
> allowed the drift. The permanent remedy is a build-time check that reads the artefact rather
> than the document; see [DEF-001](../00-governance-map/defect-register.md#def-001) and the
> standing obligation in the
> [Corrections Log](../00-governance-map/corrections-log.md#method-what-this-log-has-learned).

---

## 1. The canonical token layer

This is `:root` in `css/style.css`. **Every subdomain imports it byte-identically and never
redeclares it.** A surface that redeclares a token has forked the design system.

```css
:root {
  /* Core palette — cosmic dark, single theme, no light mode */
  --bg: #05060f;            /* page ground; also <meta name="theme-color"> */
  --bg-2: #090b1a;          /* band ground (cta-band) */
  --bg-3: #0d1024;          /* inset ground (arc nodes, img-slot) */
  --panel: rgba(20,24,48,0.55);          /* glass card — requires backdrop-filter */
  --panel-solid: #10132a;                /* opaque card (pillars, flagships) */
  --line: rgba(140,160,255,0.14);        /* hairline, resting */
  --line-strong: rgba(140,160,255,0.32); /* hairline, hover/active */

  --text: #eef1ff;   /* body + headings */
  --muted: #a6adcf;  /* secondary prose */
  --dim: #6f77a3;    /* metadata, stamps, labels */

  /* Gradient stops */
  --violet: #7c4dff;  --indigo: #4d63ff;  --cyan: #22d3ee;
  --magenta: #ff4dcd; --gold: #ffcb6b;    --emerald: #3ee6b0;

  /* The three canonical gradients */
  --grad-aurora: linear-gradient(120deg, #7c4dff 0%, #4d63ff 35%, #22d3ee 100%);
  --grad-solar:  linear-gradient(120deg, #ff4dcd 0%, #ff7b54 50%, #ffcb6b 100%);
  --grad-nebula: linear-gradient(135deg, #7c4dff, #ff4dcd 45%, #22d3ee);
  --grad-text:   linear-gradient(100deg, #b39bff, #6fe8ff 55%, #ff9be0);

  --radius: 20px;  --radius-sm: 12px;
  --shadow-glow: 0 0 60px -12px rgba(124,77,255,0.5);
  --maxw: 1200px;
  --font: "Space Grotesk", "Inter", system-ui, sans-serif;  /* display */
  --font-body: "Inter", system-ui, sans-serif;              /* body */
}
```

### Three facts that override every earlier design statement

1. **One theme, and it is dark.** No light mode, no `prefers-color-scheme` branch, and
   `theme-color` is `#05060f` everywhere. Any document describing a light default is wrong.
2. **Exactly two typefaces.** Space Grotesk for `h1`–`h4` and all "machine" labels; Inter for
   prose. Loaded as a **single** Google Fonts request with `display=swap` and both `preconnect`
   hints.
3. **The gradient set is fixed at four.** New brands select from them or extend them **in the
   same syntax**; they never invent a new colour language. The warm-gold "Meridian" ramp and the
   "Vault" brand gradient in earlier documents were invented and are discarded
   ([C-03](../00-governance-map/corrections-log.md#c-03)).

---

## 2. Gradient assignment per surface

The correct method is to assign the **three existing** gradients by pillar, then extend the same
ramp for the identity plane.

| Surface | Gradient | Accent | Rationale |
|---|---|---|---|
| Hub (`index.html`) | all three, one per pillar card | `--cyan` | The hub is the only page showing the full set |
| TopTech | `--grad-aurora` | `--cyan` | Aurora already marks `.pillar.aurora` and every `.btn-primary` |
| Academies Community | `--grad-solar` | `--gold` | Solar already marks `.pillar.solar`. **Its CTA text is `#1a0e00`, not white** |
| MacroLifeTech (Meta-X) / BCIA | `--grad-nebula` | `--magenta` | Nebula already marks `.pillar.nebula`. Spelling corrected per [C-13](../00-governance-map/corrections-log.md#c-13) |
| Ascent | `--grad-aurora` at 135deg | `--cyan` | Sub-brand of TopTech; angle differentiates without new colour |
| Credentials / Verify | `--grad-verify` (new) | `--emerald` | `--emerald: #3ee6b0` is declared and unused; verification is the one place a distinct semantic hue is justified |
| Library / Lexicon | none — hairline only | `--dim` | Reference surfaces are chrome-free by design |
| License | none — hairline only | `--gold` | A licence page that glows is a licence page nobody trusts |
| `auth.` | `--grad-vault` (new) | `--indigo` | Deliberately the **quietest** gradient in the system, so a phishing clone is visibly wrong |
| `pay.` | `--grad-ledger` (new) | `--gold` | Warm, static, no animation |
| `me.` | inherits the gradient of the pillar being viewed | contextual | The dashboard is a lens, not a brand |

```css
/* Extensions — same syntax, same stop count, appended to :root */
--grad-verify: linear-gradient(120deg, #3ee6b0 0%, #22d3ee 55%, #4d63ff 100%);
--grad-vault:  linear-gradient(120deg, #4d63ff 0%, #5a6cff 50%, #7c4dff 100%);
--grad-ledger: linear-gradient(120deg, #ffcb6b 0%, #ff9e5a 50%, #ff7b54 100%);
```

### Gradient law

A gradient **may** paint: a 4px `::before` rule on a card; a pill-shaped button; a 34px brand
mark; a text fill via `background-clip: text`; or a blurred conic orbit at `z-index: -2`.

A gradient **may never**: paint a text background at full opacity; carry meaning that colour
alone conveys (an [MX-010](../corpus/mx-010-accessibility.md) requirement, not a stylistic
preference); or appear on `auth.` or `pay.` in animated form.

---

## 3. The page skeleton contract

Every page in the estate, on every surface, is this file:

```html
<body class="page-fade">
  <div class="cosmos" aria-hidden="true"></div>     <!-- fixed, z -2, drift 120s -->
  <div class="grid-veil" aria-hidden="true"></div>  <!-- fixed, z -1, 60px lattice, masked -->

  <div id="site-header"></div>                      <!-- components.js -->

  <main>
    <section class="hero [root-hero] wrap">…</section>
    <div class="marquee" aria-hidden="true">…</div>
    <section class="wrap reveal" id="…">
      <span class="eyebrow">✦ …</span>
      <h2 class="section-title">… <span class="gradient-text">…</span></h2>
      <p class="section-lead">…</p>
      …component grid…
    </section>
    <div class="ad-slot reveal">…</div>
    <section class="wrap reveal"><div class="cta-band">…</div></section>
  </main>

  <div id="site-footer"></div>                      <!-- components.js -->
</body>
```

Scripts load in this order, and **the order is load-bearing**: a page-level `SITE_PAGE` config
object, then `data.js`, then `components.js`, then `skeleton.js`, then `site.js`, then the
per-page script.

`components.js` creates `.nav-inner`, `.nav-links` and `#mobileMenu`; `site.js` then fills them
with the mega-menu, the utility bar and the search modal. **Reversing them yields a page with no
navigation and no bound toggle** — and the comment in `site.js` documents this having already
happened once, which is why it is recorded here as a contract rather than a convention.

Layout constants: `--maxw` is 1200px; `.wrap` carries `padding: 0 20px` and `margin: 3em auto`;
`section` carries `padding: 72px 0`; `.section-lead` caps at `62ch`; `body` sets
`line-height: 1.65` at `16px` with `overflow-x: hidden`.

> **Note the `.ad-slot` in the skeleton.** It is in the contract because it is in the live code,
> and its presence on the content plane is [DEF-019](../00-governance-map/defect-register.md#def-019)
> — a live contradiction of the estate's no-tracking claim, engaging **HX-01** and **HX-04** under
> [ML-2.3 Part H](../license/ml-2-3.md#h2-the-twenty-five-named-harms). This document records the
> skeleton as built; it does not endorse that slot.

---

## 4. Chrome

**Header.** `position: sticky; top: 0; z-index: 100`, `background: rgba(5,6,15,0.62)` with
`backdrop-filter: blur(18px)`, `border-bottom: 1px solid var(--line)`, inner height exactly
**66px**. Brand is a 34px `--grad-nebula` tile bearing `✦` with `--shadow-glow`, then
`<b>MetaX</b>.Academy` in Space Grotesk 1.05rem, then a `.ver` stamp at 0.62rem `--dim` with
`0.15em` tracking carrying the release string. Per-page override via the page config's `ver`.

**Mega-menu.** Eight top-level keys — `home, toptech, ascent, bcia, academies, credentials,
library, about`. Each `.mm-panel` breaks full-width, re-constrains to `--maxw` via
`.mm-panel-wrap`, and holds an `.mm-intro` beside `.mm-cols` of `.mm-group` blocks. Desktop is
hover-intent with a **220ms** close grace timer plus a CSS bridge; keyboard `focusin`/`focusout`;
`Escape` closes all; `aria-expanded` tracked on `.mm-top`. Touch devices (`hover: none`) convert
to tap-toggle. Below 1000px the whole thing becomes `#mobileMenu`, a grouped accordion capped at
`calc(100dvh - 66px)` with `overflow-y: auto` and `overscroll-behavior: contain`, body scroll
locked while open, hamburger `≡` swapping to `✕`.

**Utility bar**, persistent at every width: `Start Here`, `Verify`, a search button showing
`⌕ Search` with a `<kbd>/</kbd>` hint, and an `EN / ع` language toggle. `.nav-cta` is
`display: none !important` above 1000px — the utility bar replaces it.

**Status badges** are `.mm-badge` with four variants — `mmb-live`, `mmb-planned`,
`mmb-research-preview`, `mmb-gated` — generated from menu data by `badgeHtml()`. These are **the
single source of truth for status across the estate**: the same four words, the same four
treatments, never remapped per subdomain, never mirrored in RTL, and **always accompanied by text
rather than colour alone**.

**Footer.** `border-top: 1px solid var(--line)`, `padding: 50px 0 40px`, a `.footer-grid` that is
1 column on mobile and `2fr 1fr 1fr` above 800px, then `.foot-bottom`, `.foot-legal`
(About · Contact · Privacy · Terms), and `.glyphs` rendering `✦ ⬡ ◉ ⊢ →` in violet at `0.3em`
tracking. Year injected at runtime.

---

## 5. The hero band

Full-bleed animated band escaping `.wrap` by `width: 100vw; margin-left: 50%;
transform: translateX(-50%)`, with `isolation: isolate`, `overflow: hidden`, and padding
`clamp(46px,8vw,88px) 20px clamp(34px,5vw,58px)`. Five stacked layers:

| z | Layer | Behaviour |
|---:|---|---|
| −4 | `.hero-bg` | optional image, `opacity .32`, `heroPan 34s alternate`, scrim `rgba(5,6,15,.35)` → `rgba(5,6,15,.82)` |
| −3 | `.hero::before` | aurora wash, three radial gradients, `heroWash 16s alternate` |
| −3 | `.hero::after` | 46px lattice, `heroGrid 22s linear`, radial mask |
| −2 | `.hero-orbit` | 680px conic gradient, `blur(42px)`, `spin 40s`, `opacity .75` |
| −2 | `.hero-particles` | six `<i>` dots, 4–6px, `heroFloat 9s`, staggered 0–3s |
| 1 | content | re-constrained to `--maxw`, centred |

Type scale: `.root-hero h1` is `clamp(2.6rem, 10vw, 6rem)`; a normal `.hero h1` is
`clamp(2.4rem, 9vw, 5rem)`; `.lead` is `clamp(1rem, 3.5vw, 1.25rem)` at `60ch`; `.curator` is
0.9rem `--dim` with the name in `--gold`; `.hero-quote` is italic Space Grotesk at `68ch` with a
4rem Georgia quote mark in violet at 40% opacity. `.tri-glyphs` (`✦ ⬡ ◉`) closes the root hero.

The `.marquee` beneath is two identical halves in a `width: max-content` flex track animated
`translateX(0 → -50%)` over **32s** linear, `mask-image` fading both edges at 12%/88%,
`animation-play-state: paused` on hover, each `<span>` uppercase 0.85rem `--dim` with a violet
`✦` separator via `::after`.

---

## 6. Component inventory

The estate has exactly these card families. **New pages compose from them rather than inventing
shapes.**

- **`.pillar`** — the hub's three entry cards: `--panel-solid`, `--line-strong`, a 4px gradient
  `::before` keyed by `aurora|solar|nebula`, a blurred conic `.p-orbit` spinning 30s, a 16:7
  `.p-art` with bottom scrim, a `.p-body` pulled up `-34px`, a 60px `.p-glyph` tile, `.p-code`
  micro-label, `.p-tag` in cyan, `.p-stats` with 1.5rem numerals over 0.72rem uppercase labels,
  and a pill `.p-cta` whose gap widens 10px→16px on hover. Enters
  `opacity 0 / translateY(40px) scale(.98)` → `.in` over 0.4s `cubic-bezier(.2,.7,.3,1)`. Three
  columns above 980px, where the card becomes a flex column so `.p-cta` sits at `margin-top: auto`.
- **`.feature`** — 26px/24px `--panel` card, 2rem `.f-glyph`, hover `translateY(-6px)`. Grid 1 → 2
  (720px) → 4 (`cols-4` at 1040px) or 3 (`cols-3` at 1000px).
- **`.level`** — ladder row: 52px `.lv-badge` in cyan on `rgba(124,77,255,.12)`, hover
  `translateX(6px)`.
- **`.arc-step`** — CSS-counter timeline on a 2px `--line-strong` left rule; each node a 42px
  circle on `--bg-3` with a 2px violet border, cyan numeral, `--shadow-glow`; `.verb` italic gold.
- **`.rail`** — 3-up at 1000px, 1.6rem glyph, hover border only.
- **`.series-card`** — the workhorse: `--panel` with `backdrop-filter: blur(8px)`, a 2rem ghost
  numeral at 20% violet, optional `.sc-new` solar pill, cyan `.sc-sub`, a `.sc-foot` with
  `.sc-tier` pill, and a signature `::after` underline animating `width: 0 → 100%` in
  `--grad-nebula` over 0.4s on hover. Enters `translateY(20px)` → `.in`. 1 → 2 (640px) → 3 (1000px).
- **Also:** `.flagship`, `.axiom`, `.arch`, `.branch-card`, `.step-card`, `.cred` + `.cred-ladder`,
  `.stats`, `.filters`/`.filter-btn` (active = `--grad-aurora`, white text, transparent border),
  `.cur-row` accordion (`max-height: 0 → 400px` over 0.4s), `.pill`, `.cta-band` (radial violet
  wash over `--bg-2`, 56px padding, centred actions).
- **`.reveal` → `.reveal.in`** — the universal scroll entrance: `opacity 0 → 1`,
  `translateY(30px) → 0`, `0.7s ease`, driven by IntersectionObserver.

### `.img-slot` — the component the no-image regime depends on

A `16/9` gradient-filled box rendering a **shimmering labelled placeholder** until an image
loads: `--grad`-tinted ground, a `shimmer 3.2s linear infinite` sweep, an `.img-tag` micro-label
pill top-left, and a 2.4rem `.img-mark` glyph centred. On load, `img.loaded` fades in over 0.6s
and `.has-img` suppresses shimmer, tag and mark.

**Because MetaX uploads no user images, `.img-slot` is the *default rendered state*, not a loading
state** — which is why it was built to look finished when empty. This is the single most
important component fact in the estate, and it is the reason the no-upload rule in Phase 1 costs
nothing visually.

---

## 7. Motion — the corrected five-tier hierarchy

The earlier "T0 static, ~80% of pages" claim was wrong by a whole tier
([C-06](../00-governance-map/corrections-log.md#c-06)). This system is **ambiently animated by
default**.

| Tier | Character | Members |
|---|---|---|
| **T-A** ambient | never-ending, decorative, `aria-hidden`, sub-1% CPU | `drift 120s`, `heroWash 16s`, `heroGrid 22s`, `heroPan 34s`, `spin 40s`/`30s`, `marq 32s`, `heroFloat 9s`, `shimmer 3.2s` |
| **T-1** entrance | once per element, IntersectionObserver, never replayed | `.reveal` 0.7s, `.pillar` 0.4s |
| **T-2** feedback | 0.2–0.4s | `translateY(-3px)` buttons, `-6px` cards, `translateX(6px)` levels, `--line → --line-strong`, `.series-card::after`, `.p-cta` gap, mega-panel open |
| **T-3** signal | **reserved, currently unused — a gap** | defect badges and gated statuses render as static pills with no attention treatment |

**T-A is absent entirely on `auth.`, `pay.`, `verify.` record pages and `license.`** — those four
get `--bg` flat, no `.cosmos::after`, no orbit, no marquee. On `auth.` this is a **security
property**, not an aesthetic one: since `auth.` is the page a phishing clone would copy, its
*stillness* is the tell, and any animated `auth.` page is by definition not ours.

### The accessibility defect this tier count exposed

`css/style.css` contains **no `prefers-reduced-motion` block**. Nine infinite animations run
regardless of user preference, and `html { scroll-behavior: smooth }` is unqualified. Required
addition, and it is [B-16](../00-governance-map/launch-blockers.md), a hard blocker:

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
  .cosmos::after, .hero-orbit, .hero-particles, .hero-bg,
  .marquee-track, .img-slot::after { animation: none !important; }
  .reveal { opacity: 1 !important; transform: none !important; }
  .marquee { display: none; }
}
```

**The last line is not optional.** With animation frozen, the marquee is a static half-sentence
clipped by a mask — worse than absent. Freezing is not the same as remedying.

---

## 8. Responsive ladder

The site's real breakpoints are **560, 640, 700, 720, 800, 860, 980, 1000, 1040** — nine, which
is three too many. They consolidate to five named tokens **without changing a single rendered
layout**:

```css
/* sm 640 · md 720 · lg 1000 · xl 1200 — mobile-first, min-width only */
```

`560` folds into the mobile default (one padding reset on `.cur-body`); `700`/`720` unify at 720;
`800`/`860` unify at 860; `980`/`1000` unify at 1000; `1040` becomes the `cols-4` exception at
`lg`. **The nav's mobile/desktop switch stays at exactly 1000px**, because the eight-item
mega-menu plus utility bar genuinely does not fit below it.

Everything is mobile-first `min-width`, single-column by default.

**Touch targets fail the 44px floor by a hair** — `.nav-toggle` is 42px and `.btn` is
`14px 26px`. Corrections: `44px` and `15px 26px`. Filed as
[DEF-022](../00-governance-map/defect-register.md#def-022), because a conformance claim a ruler
falsifies is still a false claim.

---

## 9. The identity and commerce plane in this language

**`auth.metax.academy`** — one route, `/authorize`, 400px max width, `--grad-vault`, **T-A motion
absent**, no marquee, no orbit, no ads, no mega-menu. Header degrades to the brand mark plus the
word `Sign in`, with nothing clickable except the mark. Social providers only, rendered as
full-width `.btn-ghost` rows with the provider word-mark **as text** — no provider logo images,
consistent with the no-image regime. The anti-phishing device is a `.pill` row showing the user's
deterministic glyph and phrase.

**`pay.metax.academy`** — `/checkout/{sku}`, `--grad-ledger`, static. **No countdown timers, no
scarcity copy, no pre-checked upsells** — these are [ML-2.3 §H.3(a)(i)](../license/ml-2-3.md#h3-the-duty-of-non-amplification)
concerns, not style choices. Order summary is a `.cred`-style panel; the price appears twice,
fiat and crypto, in Space Grotesk numerals; Binance Pay is the only method **and the page says so
in plain text** rather than implying others are coming. A `.pill` row states the riba position:
no interest, no instalments, zero-markup split only.

**`me.metax.academy`** — a 48px identity strip below the 66px nav, `rgba(20,24,48,0.55)` with the
same `blur(18px)`, carrying the deterministic SVG glyph generated from `SHA-256(usr_id + salt)`
(~1.9M variants), the path name, and one contextual chip. Dashboard sections reuse `.feature`
grids and `.level` ladders verbatim. The gradient is **borrowed** from whichever pillar the user
is viewing, so `me.` never reads as a fourth brand. **No streaks, no leaderboards, no per-user
analytics.**

**Academy subdomains** — inherit `style.css` unmodified. They may set a `--grad-academy` for their
own `.pillar::before` and `.p-cta`, and may choose a word-mark glyph from a fixed set. They may
**not** alter `.mm-badge` colours, the `.nav` height, the footer, the `.img-slot` treatment, or
the auth/pay chrome. Their admin UI lives at `me.metax.academy/academy/{slug}/`.

**`license.metax.academy`** — the dullest surface by design and by
[ML-2.3 §E.7](../license/ml-2-3.md#e7-registry-continuity-and-canonical-text-redundancy): flat
`--bg`, hairlines, `--gold` accent, no gradient bar, no ambient motion, no ads, no fonts beyond
the two, and a plain-text mirror of every document. **It must render correctly with CSS disabled
entirely**, because a licence that depends on a stylesheet is a licence that can be made
unreadable.

---

## 10. What the live code itself gets wrong

Recorded here so that this document is not merely a transcription. Four items, each filed:

| Finding | Filed as |
|---|---|
| No `prefers-reduced-motion` block; nine infinite animations | [DEF-016](../00-governance-map/defect-register.md#def-016) · [B-16](../00-governance-map/launch-blockers.md) |
| Detail pages are `?type=&id=` routes with no server-rendered content — invisible to non-JS crawlers | [DEF-017](../00-governance-map/defect-register.md#def-017) · [RAT-17](../00-governance-map/open-questions-and-ratifications.md#rat-17--pre-render-or-remain-javascript-only) |
| The site does not render with JavaScript disabled, contrary to its own law | [DEF-018](../00-governance-map/defect-register.md#def-018) |
| Behavioural ad networks live on the content plane | [DEF-019](../00-governance-map/defect-register.md#def-019) · [B-19](../00-governance-map/launch-blockers.md) |
| Touch targets below 44px | [DEF-022](../00-governance-map/defect-register.md#def-022) |
| T-3 signal tier reserved but unused; defect and gated badges have no attention treatment | Design gap — see below |

**On the T-3 gap.** A 2.4s opacity breath should be added to `.mmb-gated` and `.mx-defect`
**only**, capped at **8 loops**. The cap is the point: an indefinite pulse is an attention
mechanism, and DS-02's anti-engagement posture forbids one. It must also sit inside the
reduced-motion block.

**Recommended order of work**, and the reasoning is worth keeping: add the `prefers-reduced-motion`
block **first**, because nine infinite animations with no escape hatch is trivial to fix today and
embarrassing to explain later; then decide the pre-render question, because **every additional
series makes the JS-only detail route more expensive to unwind.** That second item decays — it is
cheaper today than it will ever be again.

---

**Related:** [DS-01](./ds-01-foundations-and-tokens.md) (superseded in part) ·
[DS-02 Motion and Attention](./ds-02-motion-and-attention.md) ·
[ST-19 Two-Plane Architecture](../standards/st-19-two-plane-architecture.md) ·
[ST-22 Platform and Persistence](../standards/st-22-platform-and-persistence.md) ·
[Corrections Log](../00-governance-map/corrections-log.md) ·
[MX-010 Accessibility](../corpus/mx-010-accessibility.md)

*Read from the live artefact on 2026-09-02. Perishable: re-read the code before trusting this
document after 2026-12-02.*
