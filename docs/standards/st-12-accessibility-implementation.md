---
doc_id: "ST-12"
title_en: "Accessibility Implementation"
title_ar: "تنفيذ إمكانية الوصول"
family: "standards"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 4
depth: 5
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["standards", "accessibility", "implementation", "wcag"]
route: "/library/standards/accessibility/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# ST-12 · Accessibility Implementation

**What this standard governs.** The techniques that implement
[MX-010](../corpus/mx-010-accessibility.md)'s commitment: the CSS, the markup patterns, the
required attributes, and the tests.

**Its own failure, stated first.** ST-12 existed, specified target sizes, and **did not catch the
42-pixel button** ([DEF-022](../00-governance-map/defect-register.md#def-022)). The defect was found
by fetching the live site and reading the CSS. A standard that specifies a measurement and never
measures anything is a habit, and §6 is where that is accounted for rather than explained away.

---

## 1. Position

[MX-010](../corpus/mx-010-accessibility.md) states the commitment — WCAG 2.2 AA plus five extras —
and is written for a reader. ST-12 is written for whoever builds, and the division is strict: if a
requirement can be expressed as a selector, an attribute or a measurement, it belongs here.

Published at `/library/standards/accessibility/`. Its enforcement surfaces are
[SITE-02 §9](../site/page-contract.md) lines 15–19 and
[DS-07 §6](../design/ds-07-navigation-geometry.md).

**The macro register.** An implementation standard is where an accessibility commitment either
becomes real or becomes a page. The gap between them is not knowledge — every technique below is
well documented and decades old — but **measurement**, and measurement is what nobody funds.
Under **HX‑21** (proportionate imposition), the cost of the gap falls entirely on readers who did
not choose their circumstances and who, as
[MX-010 §4](../corpus/mx-010-accessibility.md) records, **do not file complaints**: they mis-tap,
get the wrong page, and leave. **A defect whose victims are silent cannot be found by listening**,
which is the whole argument for §5's test list.

---

## 2. Definition — the required patterns

### 2.1 Motion

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
  .cosmos, .grid-veil, .marquee { animation: none !important; }
}
```

**Suppressed, not reduced.** All nine ambient animations stop. The preference exists precisely so
a site need not guess — **the reader has already answered** — and a site that merely slows its
animations has substituted its judgement for theirs.

`animation-iteration-count: 1` matters along`duration`: an infinite animation with a near-zero
duration still runs forever, consuming battery and compositor.

**Status: unshipped, launch-blocking** ([B-16](../00-governance-map/launch-blockers.md),
[DEF-016](../00-governance-map/defect-register.md#def-016)). It is a **design-system** defect
inherited by production intact, not a demo artefact
([C-14](../00-governance-map/corrections-log.md#c-14)).

### 2.2 Target size

```css
.nav-toggle { min-height: 44px; min-width: 44px; }
.btn        { padding: 15px 26px; }
```

44px floor, no exceptions. **Currently 42px and `14px 26px`**
([DEF-022](../00-governance-map/defect-register.md#def-022)) — two pixels, and the cheapest
possible falsification of an accessibility claim, requiring no expertise and no assistive
technology, only a ruler.

### 2.3 Decoration and labelling

```html
<div class="cosmos" aria-hidden="true"></div>
<div class="grid-veil" aria-hidden="true"></div>
<div class="marquee" aria-hidden="true">…</div>

<a class="util-link" href="/credentials/verify/lookup/" aria-label="Verify a credential">
  <span aria-hidden="true">◉</span><span class="ul-word">Verify</span>
</a>
```

**Decoration unmarked is content for the readers least able to ignore it.** The marquee is the sharp
case: a moving text strip exposed to a screen reader interleaves meaningless fragments into the
reading order, which is **worse than absent**.

**Glyph-only controls require `aria-label` on the anchor**, because `.ul-word` is hidden with
`display: none` and leaves the accessibility tree entirely
([DS-07 §3.3](../design/ds-07-navigation-geometry.md)). Between 1180px and 1280px the utility band
is glyph-only, so this is a live requirement and not a hypothetical.

### 2.4 Status without colour

Every `.mm-badge` renders a **text label**. Four permitted values — `live`, `planned`,
`research-preview`, `gated` — and colour is never the sole carrier
([SITE-01 §3](../site/route-manifest.md)).

### 2.5 Structure and keyboard

Heading order is sequential and conveys the document with CSS disabled. One `<h1>` per page.
Semantic landmarks — `<header>`, `<nav>`, `<main>`, `<footer>` — not generic containers.

Mega-panels open on **focus** as well as hover; `Esc` closes; focus order follows visual order; the
`matchMedia("(hover: hover)")` guard prevents hover-intent firing on touch.

### 2.6 No time limits

No session timeout on reading, no countdown on an assessment, no auto-advance, no carousel that
moves itself. A time limit converts a comprehension task into a speed task for readers who process
differently.

---

## 3. Mechanism — contrast against gradients

The estate's specific difficulty, and the one most likely to be got wrong in good faith.

Text over a gradient has **no single contrast ratio**. It must be measured at the **worst point**
along the gradient, not at its midpoint or its endpoints.

| Surface | Requirement |
|---|---|
| Body text on `--bg` (#05060f) | ≥4.5:1 |
| Text on `--grad-aurora` / `--grad-nebula` / `--grad-solar` | ≥4.5:1 **at the worst point** |
| `--grad-solar` CTA text | `#1a0e00`, **not white** — per [DS-00 §2](../design/ds-00-as-built-token-layer.md) |
| `--muted` (#a6adcf) on `--bg` | ≥4.5:1 |
| `--dim` (#6f77a3) on `--bg` | **Decorative only** — never body text |

The `--grad-solar` row is a real finding already recorded in DS-00: warm gradients invert the
expected text colour, and an author applying white text across all three gradients will fail on one
of them without noticing on the other two.

---

## 4. Worked instance — the mobile menu

`#mobileMenu` below 1180px.

**Height.** `max-height: calc(100dvh - 66px)` — **`dvh`, not `vh`.** On mobile browsers `vh`
measures the viewport as though the address bar were hidden, so the panel's last items sit below the
fold. The bug reproduces only on a real device, which is why it survives desktop review.

**Trigger.** `.nav-toggle` at `min-height: 44px` (§2.2), `aria-expanded` reflecting state,
`aria-controls` naming the panel.

**Keyboard.** Focus moves into the panel on open, is trapped while open, returns to the toggle on
close, and `Esc` closes.

**Touch.** The `hover: hover` guard prevents hover-intent opening panels on scroll.

**Motion.** The open transition is suppressed under `prefers-reduced-motion` (§2.1).

**What this instance demonstrates.** Five separate requirements converge on one component, and
**four of the five fail invisibly on a desktop reviewer's machine**: `dvh` versus `vh`, the
two-pixel target, hover-on-touch, and reduced motion. None produces a console error. None is
detected by reading the markup. This is why §5 specifies tests at named viewports on real devices
rather than a review checklist.

---

## 5. The test list

Automated checks catch roughly a third of WCAG criteria, so **"zero automated violations" is a
third of an answer.**

| Test | Method | State |
|---|---|---|
| Contrast at gradient worst points | Measured, not eyeballed | **Never run** |
| Target size | A ruler on the rendered page | Run once, **failed** |
| Keyboard-only traversal | Whole estate, no pointer | Never run |
| Screen-reader pass | A real screen reader, a real user | **Never run** |
| CSS disabled | Structure legible from headings | Never run |
| JavaScript disabled | Main prose renders | Run, **failed** ([DEF-018](../00-governance-map/defect-register.md#def-018)) |
| `prefers-reduced-motion` | All nine animations stop | Run, **failed** |
| Viewport boundaries | 999 / 1000 / 1179 / 1180 / 1279 / 1280 / 1400px | Never run |
| RTL parity | The Arabic tree | **No Arabic pages exist** ([DEF-002](../00-governance-map/defect-register.md#def-002)) |

**Three run, two passed nothing, six never attempted.** And the most important row is the one the
estate cannot run alone: **no assistive-technology user has ever tested this estate.** A corpus can
be technically conformant and practically unusable, and the estate has no evidence either way
([MX-010 §7](../corpus/mx-010-accessibility.md)).

---

## 6. Failure modes

**The standard that specifies and never measures.** ST-12's own history. It named a 44px floor and
a 42px button shipped, found later by reading CSS rather than by testing. **A specification is not
a check**, and this is the estate's recurring finding —
[HX-002 §8](../harms/hx-002-harm-instrument-map.md) — arriving in the standard that most needs to
resist it.

**Automated results reported as conformance.** §5.

**Overlay remediation.** An accessibility widget over an inaccessible site. **Prohibited
outright** — it degrades the experience for actual assistive-technology users while producing a
compliance appearance, which is **HX‑15** in its purest form.

**`vh` restored for simplicity.** §4. Reproduces only on a device.

**ARIA added where semantics would do.** `role="navigation"` on a `<nav>`; `aria-label` on an
element whose text already labels it. Redundant ARIA is not neutral — it produces double
announcements.

**Contrast measured at the gradient midpoint.** §3. Passes the measurement and fails the reader at
one end.

---

## 7. Limits

**Class: technical, and binding.** **No automated check runs.** The contrast, target-size and
heading-order checks would live in
[SENTINEL](st-13-static-build-and-sentinel.md)
([DEF-001](../00-governance-map/defect-register.md#def-001)), and the screen-reader and
keyboard tests cannot be automated at all.

**Class: epistemic.** §5's ninth row: zero tests by an assistive-technology user. Everything this
standard claims about usability is inference from technique.

**Class: linguistic.** RTL accessibility is entirely untested, and
[DS-07 §7](../design/ds-07-navigation-geometry.md) admits the 1180px breakpoint was derived from
**English** label metrics and is unverified for Arabic
([V-08](../00-governance-map/verification-log.md)).

**Class: economic.** A real screen-reader pass with a paid expert user is the single highest-value
unfunded item in this standard, and the estate has no budget line for it.

---

## 8. Falsifier

1. **A conformance failure found by a reader** that §2 specifies. Expected, given §5.
2. **An assistive-technology user finding the estate unusable despite every §2 pattern being
   correct** — falsifying technique-as-proxy-for-usability, which is this standard's central
   assumption.
3. **A §2 pattern that harms rather than helps.** §2.1's absolute motion suppression is the
   candidate: if suppressing all animation removes a cue some readers rely on, the rule needs
   narrowing rather than defending.
4. **The three known failures persisting through publication.** Individually trivial, surviving
   three releases. **Closest to firing.**

---

## 9. Obligation

**For the build, in order of cost.** Ship §2.1's reduced-motion block and §2.2's two corrections —
**CSS measured in minutes** standing between this corpus and an honest conformance claim. Then
resolve [RAT-17](../00-governance-map/open-questions-and-ratifications.md#rat-17) toward
pre-rendering so the JavaScript-disabled row can pass.

**For any author:** decoration carries `aria-hidden`. Glyph-only controls carry `aria-label`. Status
is never colour alone. No time limits. Semantics before ARIA.

**For the estate:** commission a screen-reader pass with a real user. §7 records that the estate has
no evidence about the thing it claims, and **that is the one gap no further specification closes.**

**Under ML-2.3:** §H.21 (proportionate imposition — the burden falls on readers who did not choose
it), §H.23 (channel parity), §H.22 (language parity — the untested RTL tree), §H.24 (developmental
default), §H.15 (compliance theatre — §6's overlay prohibition and §5's third-of-an-answer rule).

---

**Related:** [MX-010 Accessibility Statement](../corpus/mx-010-accessibility.md) ·
[DS-07 Navigation Geometry](../design/ds-07-navigation-geometry.md) ·
[DS-00 As-Built Token Layer](../design/ds-00-as-built-token-layer.md) ·
[SITE-02 Page Contract](../site/page-contract.md) ·
[ST-13 Static Build and SENTINEL](st-13-static-build-and-sentinel.md) ·
[Launch Blockers B-16](../00-governance-map/launch-blockers.md)

*Curated by Maher. Six pattern families, nine tests of which three have run and two of those
failed, and one row no specification can close: nobody using assistive technology has ever tested
this estate.*
