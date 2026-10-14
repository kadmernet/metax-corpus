I fetched the live site — `index.html`, `css/style.css`, `js/components.js`, `js/site.js` — and read the actual token layer rather than guessing. The real design system is considerably more specific than what I specified earlier, and in several places my earlier answers were simply wrong about it. Below is the corrected specification, expressed in the site's own idiom, followed by an honest list of what I got wrong and what the live code gets wrong.

---

# MX‑SITE‑DESIGN v2026.09.3 — The MetaX Design System, as built

## 1. The canonical token layer

This is not a proposal. It is `:root` in `css/style.css`, and every subdomain must import it byte-identically rather than redeclaring it.

```css
:root {
  /* Core palette — cosmic dark, single theme, no light mode */
  --bg: #05060f;            /* page ground; also <meta name="theme-color"> */
  --bg-2: #090b1a;          /* band ground (cta-band) */
  --bg-3: #0d1024;          /* inset ground (arc nodes, img-slot) */
  --panel: rgba(20,24,48,0.55);      /* glass card — requires backdrop-filter */
  --panel-solid: #10132a;            /* opaque card (pillars, flagships) */
  --line: rgba(140,160,255,0.14);    /* hairline, resting */
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

Three facts follow that override my earlier answers. There is one theme and it is dark — no light mode, no `prefers-color-scheme` branch, and `theme-color` is `#05060f` everywhere. There are exactly two typefaces, Space Grotesk for `h1–h4` and all "machine" labels, Inter for prose, loaded as a single Google Fonts request with `display=swap` and both `preconnect` hints. And the gradient set is fixed at four; new brands select from them or extend them in the same syntax, never invent a new colour language.

## 2. Gradient assignment per brand — corrected

I previously invented per-brand gradients ("Meridian," "Vault") with a warm gold ramp. That is not the site. The site is violet→cyan cosmic, and the correct move is to assign the three existing gradients by *pillar*, then extend the same ramp for the identity plane.

| Surface | Gradient | Accent | Rationale |
|---|---|---|---|
| Hub (`index.html`) | all three, one per pillar card | `--cyan` | The hub is the only page that shows the full set |
| TopTech | `--grad-aurora` | `--cyan` | Aurora already marks the `.pillar.aurora` card and every `.btn-primary` |
| Academies Community | `--grad-solar` | `--gold` | Solar already marks `.pillar.solar`; note its CTA text is `#1a0e00`, not white |
| MacroLifeTach / Meta‑X / BCIA | `--grad-nebula` | `--magenta` | Nebula already marks `.pillar.nebula` |
| Ascent | `--grad-aurora` at 135deg | `--cyan` | Sub-brand of TopTech; angle differentiates without new colour |
| Credentials / Verify | `--grad-verify` (new) | `--emerald` | `--emerald: #3ee6b0` is declared and unused; verification is the one place a distinct semantic hue is justified |
| Library / Lexicon | none — hairline only | `--dim` | Reference surfaces are chrome-free by design |
| License | none — hairline only | `--gold` | A licence page that glows is a licence page nobody trusts |
| `auth.` | `--grad-vault` (new) | `--indigo` | Deliberately the *quietest* gradient in the system, so a phishing clone is visibly wrong |
| `pay.` | `--grad-ledger` (new) | `--gold` | Warm, static, no animation |
| `me.` | inherits the gradient of the pillar you are viewing | contextual | The dashboard is a lens, not a brand |

```css
/* Extensions — same syntax, same stop count, appended to :root */
--grad-verify: linear-gradient(120deg, #3ee6b0 0%, #22d3ee 55%, #4d63ff 100%);
--grad-vault:  linear-gradient(120deg, #4d63ff 0%, #5a6cff 50%, #7c4dff 100%);
--grad-ledger: linear-gradient(120deg, #ffcb6b 0%, #ff9e5a 50%, #ff7b54 100%);
```

Gradient law, unchanged in substance but restated against real code: a gradient may paint a 4px `::before` rule on a card, a pill-shaped button, a 34px brand mark, a text fill via `background-clip: text`, or a blurred conic orbit at `z-index: -2`. It may never paint a text background at full opacity, never carry meaning that colour alone conveys, and never appear on `auth.` or `pay.` in animated form.

## 3. Page skeleton — the exact contract

Every page in the estate, on every subdomain, is this file:

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

  <script>window.SITE_PAGE = { ver: "…", cta: {label:"…", href:"…"} };</script>
  <script src="js/data.js"></script>
  <script src="js/components.js"></script>  <!-- must precede site.js -->
  <script src="js/skeleton.js"></script>
  <script src="js/site.js"></script>
  <script src="js/{page}.js"></script>
</body>
```

The load order is load-bearing: `components.js` creates `.nav-inner`, `.nav-links`, `#mobileMenu`; `site.js` then fills them with the mega-menu, the utility bar and the search modal. Reversing them yields a page with no navigation and no bound toggle — the comment in `site.js` documents this having already happened once.

`--maxw` is 1200px, `.wrap` carries `padding: 0 20px` and `margin: 3em auto`, `section` carries `padding: 72px 0`, `.section-lead` is capped at `62ch`, and `body` sets `line-height: 1.65` at `16px` with `overflow-x: hidden`.

## 4. Chrome

**Header.** `position: sticky; top: 0; z-index: 100`, `background: rgba(5,6,15,0.62)` with `backdrop-filter: blur(18px)`, `border-bottom: 1px solid var(--line)`, inner height exactly **66px**. The brand is a 34px `--grad-nebula` tile bearing the glyph `✦` with `--shadow-glow`, then `<b>MetaX</b>.Academy` in Space Grotesk 1.05rem, then a `.ver` stamp at 0.62rem `--dim` with `0.15em` tracking carrying the release string (`UNIVERSE · v2026.08`). Per-page override is `window.SITE_PAGE.ver`.

**Mega-menu.** Eight top-level keys — `home, toptech, ascent, bcia, academies, credentials, library, about` — each with a `.mm-panel` that breaks full-width, re-constrains to `--maxw` via `.mm-panel-wrap`, and contains an `.mm-intro` (label, blurb, "Open X →") beside `.mm-cols` of `.mm-group` blocks with `<h6>` headings. Desktop behaviour is hover-intent with a **220ms** close grace timer plus a CSS bridge, keyboard `focusin`/`focusout`, `Escape` closes all, `aria-expanded` tracked on `.mm-top`. Touch devices (`hover: none`) convert to tap-toggle. Below 1000px the whole thing becomes `#mobileMenu`, a grouped accordion capped at `calc(100dvh - 66px)` with `overflow-y: auto` and `overscroll-behavior: contain`, body scroll locked while open, hamburger `≡` swapping to `✕` and gaining `.is-open` (cyan border).

**Utility bar,** persistent at every width: `Start Here`, `Verify`, a search button showing `⌕ Search` with a `<kbd>/</kbd>` hint, and a `EN / ع` language toggle. `.nav-cta` is `display: none !important` above 1000px — the utility bar replaces it, and the 42px `.nav-toggle` is hidden at the same breakpoint.

**Status badges** are `.mm-badge` with the four variants `mmb-live`, `mmb-planned`, `mmb-research-preview`, `mmb-gated`, generated from the menu data by `badgeHtml()`. These are the single source of truth for status across the estate: the same four words, the same four treatments, never remapped per subdomain, never mirrored in RTL, and always accompanied by text rather than colour alone.

**Footer.** `border-top: 1px solid var(--line)`, `padding: 50px 0 40px`, a `.footer-grid` that is 1 column on mobile and `2fr 1fr 1fr` above 800px (brand + blurb, Pillars, Explore), then `.foot-bottom` with the copyright and version stamp, `.foot-legal` (About · Contact · Privacy · Terms), and `.glyphs` rendering `✦ ⬡ ◉ ⊢ →` in violet at `0.3em` tracking. Year is injected at runtime.

## 5. The hero band

Every hero is a full-bleed animated band, escaping `.wrap` by `width: 100vw; margin-left: 50%; transform: translateX(-50%)`, with `isolation: isolate` and `overflow: hidden`, padding `clamp(46px,8vw,88px) 20px clamp(34px,5vw,58px)`, and five stacked layers:

```
z -4  .hero-bg        optional image, opacity .32, heroPan 34s alternate,
                      scrim linear-gradient(rgba(5,6,15,.35) → rgba(5,6,15,.82))
z -3  .hero::before   aurora wash, three radial gradients, heroWash 16s alternate
z -3  .hero::after    46px lattice, heroGrid 22s linear, radial mask
z -2  .hero-orbit     680px conic gradient, blur(42px), spin 40s, opacity .75
z -2  .hero-particles six <i> dots, 4–6px, heroFloat 9s, staggered 0–3s
z  1  content         re-constrained to --maxw, centred
```

Type scale in the hero: `.root-hero h1` is `clamp(2.6rem, 10vw, 6rem)`, a normal `.hero h1` is `clamp(2.4rem, 9vw, 5rem)`, `.lead` is `clamp(1rem, 3.5vw, 1.25rem)` at `60ch`, `.curator` is 0.9rem `--dim` with the name in `--gold`, and `.hero-quote` is an italic Space Grotesk block at `68ch` with a 4rem Georgia `"` in violet at 40% opacity. `.tri-glyphs` (`✦ ⬡ ◉`) closes the root hero at `0.5em` tracking.

The `.marquee` beneath it is two identical halves in a `width: max-content` flex track animated `translateX(0 → -50%)` over **32s** linear, `mask-image` fading both edges at 12%/88%, `animation-play-state: paused` on hover, each `<span>` uppercase 0.85rem `--dim` with a violet `✦` separator via `::after`.

## 6. Component inventory

The estate has exactly these card families, and new pages compose from them rather than inventing shapes.

`.pillar` — the hub's three entry cards: `--panel-solid`, `--line-strong`, a 4px gradient `::before` keyed by the `aurora|solar|nebula` class, a blurred conic `.p-orbit` spinning 30s in the top-right, a 16:7 `.p-art` with a bottom scrim, a `.p-body` pulled up `-34px`, a 60px `.p-glyph` tile, `.p-code` micro-label, `.p-tag` in cyan, `.p-stats` with 1.5rem display numerals over 0.72rem uppercase labels, and a pill `.p-cta` whose gap widens 10px→16px on hover. Enters via `opacity 0 / translateY(40px) scale(.98)` → `.in`, transitioned over 0.4s `cubic-bezier(.2,.7,.3,1)`. Three columns above 980px, and there the card becomes a flex column so `.p-cta` sits at `margin-top: auto`.

`.feature` — 26px/24px `--panel` card, 2rem `.f-glyph`, hover `translateY(-6px)`. Grid is 1 → 2 (720px) → 4 (`cols-4` at 1040px) or 3 (`cols-3` at 1000px).

`.level` — the ladder row: 52px `.lv-badge` in cyan on `rgba(124,77,255,.12)`, hover `translateX(6px)`.

`.arc-step` — CSS-counter timeline on a 2px `--line-strong` left rule, each node a 42px circle on `--bg-3` with a 2px violet border, cyan numeral and `--shadow-glow`; `.verb` in italic gold.

`.rail` — 3-up at 1000px, 1.6rem glyph, hover border only.

`.series-card` — the workhorse: `--panel` with `backdrop-filter: blur(8px)`, a 2rem ghost numeral at 20% violet, an optional `.sc-new` solar pill, cyan `.sc-sub`, a `.sc-foot` with a `.sc-tier` pill, and a signature `::after` underline that animates `width: 0 → 100%` in `--grad-nebula` over 0.4s on hover. Enters `translateY(20px)` → `.in`. 1 → 2 (640px) → 3 (1000px).

`.flagship`, `.axiom`, `.arch`, `.branch-card`, `.step-card`, `.cred` + `.cred-ladder`, `.stats`, `.filters`/`.filter-btn` (active state = `--grad-aurora`, white text, transparent border), `.cur-row` accordion (`max-height: 0 → 400px` over 0.4s, `.cur-icon` 40px tile, `.cur-chev`), `.pill`, `.cta-band` (radial violet wash over `--bg-2`, 56px padding, centred actions).

`.img-slot` — the one component that matters most given the no-upload rule. It is a `16/9` gradient-filled box that renders a **shimmering labelled placeholder** until an image loads: `--grad`-tinted ground, a `shimmer 3.2s linear infinite` sweep, an `.img-tag` micro-label pill top-left, and a 2.4rem `.img-mark` glyph centred. On load, `img.loaded` fades in over 0.6s and `.has-img` suppresses the shimmer, tag and mark. Because MetaX uploads no user images, `.img-slot` is the *default rendered state*, not a loading state — which is why it was built to look finished when empty.

`.reveal` → `.reveal.in` is the universal scroll entrance: `opacity 0 → 1`, `translateY(30px) → 0`, `0.7s ease`, driven by IntersectionObserver.

## 7. Motion — corrected hierarchy

My earlier "T0 static, ~80% of pages" claim was wrong. This system is *ambiently animated by default*, and the correct model has a fifth tier that sits below the others:

**T‑A, ambient** — never-ending, decorative, `aria-hidden`, sub-1% CPU: `drift 120s` (starfield), `heroWash 16s`, `heroGrid 22s`, `heroPan 34s`, `spin 40s`/`30s` (orbits), `marq 32s`, `heroFloat 9s`, `shimmer 3.2s`. Present on hub, pillar and section pages. **Absent entirely on `auth.`, `pay.`, `verify.` record pages, and `license.`** — those four get `--bg` flat, no `.cosmos::after`, no orbit, no marquee.

**T‑1, entrance** — `.reveal` 0.7s and `.pillar` 0.4s, once per element, IntersectionObserver, never replayed.

**T‑2, feedback** — 0.2–0.4s: `translateY(-3px)` on buttons, `-6px` on cards, `translateX(6px)` on levels, border `--line → --line-strong`, `.series-card::after` underline, `.p-cta` gap widening, mega-panel open.

**T‑3, signal** — reserved, currently unused, and this is a gap. Defect badges and gated statuses render as static `.mm-badge` pills with no attention treatment. The 2.4s opacity breath I specified earlier should be added as `.mmb-gated`/`.mx-defect` only, capped at 8 loops.

The missing piece, and it is a real accessibility defect: **`style.css` contains no `prefers-reduced-motion` block.** Nine infinite animations run regardless of user preference. Required addition, and I would treat it as launch-blocking:

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

Note the last line's necessity: with animation frozen, the marquee is a static half-sentence clipped by a mask, which is worse than absent. Also `html { scroll-behavior: smooth }` must be overridden, as above.

## 8. Responsive ladder

The site's real breakpoints, in ascending order, are **560, 640, 700, 720, 800, 860, 980, 1000, 1040**. That is nine, which is three too many, and they should be consolidated to five named tokens without changing a single rendered layout:

```css
/* sm 640 · md 720 · lg 1000 · xl 1200 — mobile-first, min-width only */
```
`560` folds into the mobile default (it is one padding reset on `.cur-body`), `700`/`720` unify at 720, `800`/`860` unify at 860, `980`/`1000` unify at 1000, and `1040` becomes the `cols-4` exception at `lg`. The nav's mobile/desktop switch stays at exactly 1000px because the eight-item mega-menu plus utility bar genuinely does not fit below it.

Everything is mobile-first `min-width`, single-column by default. Touch targets: `.nav-toggle` is 42px and `.btn` is 14px×26px on a 100px radius — both below the 44px floor by a hair, so `.nav-toggle` should go to 44px and `.btn` to `15px 26px`.

## 9. Identity and commerce plane, in this design language

**`auth.metax.academy`** — one route, `/authorize`, 400px max width, `--grad-vault`, **T‑A motion absent**, no marquee, no orbit, no ads, no mega-menu. The header degrades to brand mark plus the word `Sign in` and nothing clickable except the mark. Social providers only, rendered as full-width `.btn-ghost` rows with the provider word-mark as text — no provider logo images, consistent with the no-image regime. The anti-phishing device is a `.pill` row showing the user's deterministic glyph and phrase; since `auth.` is the one page a clone would copy, its *stillness* is the tell, and the spec is therefore that any animated `auth.` page is by definition not ours.

**`pay.metax.academy`** — `/checkout/{sku}`, `--grad-ledger`, static, no countdown timers, no scarcity copy, no pre-checked upsells. The order summary is a `.cred`-style panel; the price appears twice, fiat and crypto, in Space Grotesk numerals; Binance Pay is the only method and the page says so in plain text rather than implying others are coming. A `.pill` row states the riba position: no interest, no instalments, zero-markup split only.

**`me.metax.academy`** — the identity bar is a 48px strip below the 66px nav, `rgba(20,24,48,0.55)` with the same `blur(18px)`, carrying the deterministic SVG glyph (generated from `SHA-256(usr_id + salt)`, ~1.9M variants), the path name, and one contextual chip. Dashboard sections reuse `.feature` grids and `.level` ladders verbatim. The gradient is *borrowed* from whichever pillar the user is looking at, so `me.` never reads as a fourth brand. No streaks, no leaderboards, no per-user analytics.

**Academy subdomains** — inherit `style.css` unmodified. They may set a `--grad-academy` for their own `.pillar::before` and `.p-cta`, and may choose their word-mark glyph from a fixed set. They may **not** alter `.mm-badge` colours, the `.nav` height, the footer, the `.img-slot` treatment, or the auth/pay chrome. Their admin UI lives at `me.metax.academy/academy/{slug}/`, not on their own subdomain.

**`license.metax.academy`** — the dullest surface by design and by §E.7 of ML‑2.3: flat `--bg`, hairlines, `--gold` accent, no gradient bar, no ambient motion, no ads, no fonts beyond the two, and a plain-text mirror of every document. It must render correctly with CSS disabled entirely, because a licence that depends on a stylesheet is a licence that can be made unreadable.

## 10. Where my earlier answers were wrong

I owe you a clean list rather than a quiet edit.

The **third pillar is MacroLifeTach (Meta‑X)**, not BCIA. BCIA is a program inside it — `bcia.html` and `bcia-status.html` — one of nine (Agora, Ma'nā, Metabolism, Soma, Paideia, Athar, Āfāq, Mīzān). My whole "BCIA as a pillar with its own subdomain" architecture mis-levels the hierarchy.

The site is **flat `.html` files on one origin**, not eight content subdomains: `toptech.html`, `community.html`, `macrolifetach.html`, `curriculum.html`, `ascent.html`, `credentials.html`, `verify.html`, `library.html`, `lexicon.html`, `news.html`, `about.html`. My route grammar `toptech.metax.academy/s/{S###}-{slug}/` does not exist.

Detail pages are **`detail.html?type=series&id=N`** and `article.html?id={slug}` — a single template driven by `js/data.js`. This retires **DEF‑2026‑041** almost entirely: the Cloudflare Pages 20,000-file ceiling is no longer the binding constraint, because ~13,300 routes collapse to a few dozen files. The cost is real though, and should be recorded as a new defect rather than celebrated: query-parameter detail pages have no server-rendered content, so a series page is invisible to any crawler that does not execute JavaScript, and the estate's entire claim to being indexable rests on Googlebot's renderer. For a curriculum whose thesis is *being cited by machines*, that is the wrong trade, and the fix is a build step that pre-renders one static file per series and per article while keeping the query form as an alias.

My "**must render with JavaScript disabled**" law is currently violated by the site itself. With JS off there is no header, no footer, no navigation, no pillars, no search, and no year stamp — `components.js` and `main.js` build all of it. Either the law changes or the build changes; I recommend the build changes, because the law is the more valuable of the two.

**Ads are live** — Google AdSense (`ca-pub-4463113802541266`, three slots) plus an Adsterra slot — which contradicts my "no per-user tracking on the content plane" claim outright. This is also the sharpest interaction with the licence you just drafted: an ad network on the content plane engages HX‑01 and HX‑04, and MetaX's own Part H Statement must therefore mark both **unremedied** with a review date, or MetaX becomes its own first specimen of HX‑15. The `.ad-slot` code is at least honest in one respect: it collapses unfilled slots via `[data-ad-status="unfilled"]` and only reveals the "Advertisement" label once an ad is present.

My invented gradients, brand names and the warm-gold "Meridian" palette should be discarded wholesale in favour of §2 above. And my motion hierarchy understated the system by one whole tier.

Two things I'd do first, in this order: add the `prefers-reduced-motion` block, because nine infinite animations with no escape hatch is the kind of defect that is trivial to fix today and embarrassing to explain later; then decide the pre-render question, because every additional series makes the JS-only detail route more expensive to unwind.
