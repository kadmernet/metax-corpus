---
doc_id: "DS-07"
title_en: "Navigation Geometry and the Fluid Nav"
title_ar: "هندسة التنقّل والقائمة المرنة"
family: "design"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 3
depth: 4
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["design", "navigation", "responsive", "accessibility"]
derived_from: "MX-NAV-SPEC v2026.10.1 §§2, 3, 6.5; DS-00 §8"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# DS-07 · Navigation Geometry

**What this instrument governs.** How the estate's nine-pillar navigation behaves across viewport
widths: the fluid scale, the breakpoint that replaces the old 1000px switch, the mega-panel hub
links, the glyph-only utility state, and the accessibility floors all four must respect.

**Its relation to DS-00.** [DS-00](ds-00-as-built-token-layer.md) is the as-built token layer read
directly from live code and it governs colour, type, radius and motion. DS-07 governs **geometry
under constraint** — what happens when nine items must fit in a space designed for eight. It adds
no tokens and invents no colours; the estate's last design instrument to invent values was
corrected for it ([C-03](../00-governance-map/corrections-log.md)).

---

## 1. Position

This document exists because a governance decision — adding a ninth pillar — produced a layout
problem, and because the honest response to a layout problem caused by a governance decision is
to fix the layout rather than to hide the decision.

Its parent in the design family is DS-00. Its parent in the published estate is
`/about/policy/accessibility/`, which is where the floors in §6 are stated to readers. Its
upstream constraint is the [Route Manifest §3](../site/route-manifest.md), which fixes the pillar
count at nine — provisionally, pending
[RAT-19](../00-governance-map/open-questions-and-ratifications.md#rat-19).

The question this instrument answers: **how does an estate add a top-level destination without
either burying one or breaking its own nav?**

---

## 2. Definition — the problem, stated numerically

Nine top-level items do not fit at 1000px. They do not fit at 1120px either.

The previous specification set a fixed `0.9rem` label size and a fixed `22px` gap between nav
items, with the mobile→desktop switch at 1000px. At nine items the arithmetic fails: nine labels
at `0.9rem` plus eight gaps at `22px` plus the utility bar plus the word-mark exceeds the
available width well before 1120px, and the failure mode is not graceful. Items wrap to a second
line, the 66px sticky header grows to 112px, and every page's hero offset is wrong.

**The three available responses, and why two were rejected.**

*Bury a pillar.* Fold `Method` under TopTech as `/toptech/method/`, returning to eight items and
the 1000px switch. The source's own assessment: this *"costs one nav slot and buries the most
defensible thing on the site."* Rejected here as a **design** matter, while remaining open as a
**governance** matter — the fold is still available to the Curator at RAT-19, and this document
records what it would cost in §9.

*Add an overflow menu.* A "More ▾" item collecting the last two or three pillars. Rejected
because an overflow menu is a claim about relative importance made silently by a layout
constraint, and the items that land in it are determined by array order rather than by any
decision anyone made.

*Make the nav fluid.* Adopted. The type and gap scale with the viewport, and the desktop
breakpoint moves outward to where nine items genuinely fit.

---

## 3. Mechanism

### 3.1 The fluid scale

```css
/* Nav scale — replaces the fixed 0.9rem / 22px gap */
.nav-links.mega { gap: clamp(10px, 1.15vw, 22px); }
.mm-top { font-size: clamp(0.78rem, 0.72vw + 0.4rem, 0.9rem); }
```

Two `clamp()` declarations, and each of the six values is load-bearing.

The **gap** floor of `10px` is the point below which adjacent nav items become ambiguous as
targets — a reader aiming at "Ascent" hits "Method". Its ceiling of `22px` is the original fixed
value, so at wide viewports the nav is *identical* to the previous specification and nothing that
was tuned by eye is disturbed. The `1.15vw` preferred value is set so that the transition from
floor to ceiling completes across the range where nine items are tight rather than continuing to
grow indefinitely.

The **font-size** ceiling of `0.9rem` is likewise the original value. Its floor of `0.78rem` is
the more consequential number: it is set above the point where the nav labels fall below the
estate's minimum legible size for secondary chrome. A fluid scale with no floor will happily
shrink text into unreadability to satisfy a layout, which converts a design problem into an
accessibility problem — and the accessibility problem is invisible to the person who set the
`vw` value on a large monitor.

The `0.72vw + 0.4rem` preferred value is a mixed unit deliberately. A pure `vw` preferred value
scales with the viewport but ignores the reader's root font size, so a reader who has increased
their browser's default text size gets no benefit from it. Adding the `0.4rem` term means the
scale respects user preference and viewport simultaneously — which is the whole reason to use
`clamp()` rather than a media-query ladder.

### 3.2 The breakpoint moves 1000px → 1180px

```css
@media (min-width: 1180px) {
  .nav-links.mega { display: flex; }
  .nav-toggle, .nav-cta { display: none !important; }
}
```

1180px is where nine fluid items fit without either wrapping or hitting the type floor. Below it,
the mobile pattern applies: `.nav-toggle` and `#mobileMenu`.

**What this costs, stated plainly.** Every viewport between 1000px and 1179px now receives the
mobile navigation where it previously received the desktop mega-menu. That range is not marginal
— it includes a large population of laptops at scaled resolutions and tablets in landscape. The
trade is deliberate and it is the correct one: a hamburger menu that works is better than a
mega-menu that wraps, and the mobile pattern in this estate is a full-height panel rather than a
degraded afterthought.

**What survives unchanged.** The `matchMedia("(hover: hover)")` guard in `wireMobileToggle()` and
the `#mobileMenu` `max-height: calc(100dvh - 66px)` both stay exactly as built. Only the numeric
breakpoint moves. The `hover` guard matters because hover-intent on a touch device produces
menus that open on scroll; the `100dvh` unit matters because `vh` on mobile browsers measures the
viewport as though the address bar were hidden, which pushes the panel's last items below the
fold.

### 3.3 The glyph-only utility band

```css
@media (max-width: 1279px) { .nav-utility .util-link .ul-word { display: none; } }
```

Between 1180px and 1280px the desktop nav is present but tight, so the utility links — Start
Here, Verify, Sign in — collapse to their glyphs `⊢ ◉ →`.

**This is the most accessibility-sensitive rule in the document**, because a glyph-only control is
an unlabelled control unless it is explicitly labelled. The markup contract is therefore
mandatory, not advisory:

```html
<a class="util-link util-verify" href="/credentials/verify/lookup/" aria-label="Verify a credential">
  <span aria-hidden="true">◉</span><span class="ul-word">Verify</span>
</a>
```

The word is hidden with `display: none`, so it leaves the accessibility tree entirely — which is
why the `aria-label` on the anchor is required rather than optional. The glyph is marked
`aria-hidden`, because `◉` announced literally is noise. A screen-reader user in this range hears
"Verify a credential, link", which is better than the sighted experience, and that asymmetry is
acceptable; the reverse never is.

### 3.4 Group headings become links

```js
var head = f.hub
  ? '<h6><a class="mm-hub" href="' + f.hub + '">' + f.heading + '</a>' + badgeHtml(f.badge) + '</h6>'
  : '<h6>' + f.heading + badgeHtml(f.badge) + '</h6>';
```

`.mm-hub` inherits `<h6>` type, takes `color: var(--cyan)` on hover, and carries a 1px underline
at 3px offset.

This eight-line ternary is what makes the estate's **third tier reachable**. Before it, a group
heading was a label inside a mega-panel, and the 45 group hubs enumerated in the manifest were
addressable but unreachable from the navigation — present to a crawler, absent to a reader. That
is a worse state than not existing, because it publishes 45 pages that no human path leads to.

The `f.hub` ternary rather than an unconditional link is deliberate: a heading with no hub renders
as plain text, so the array can carry a grouping label that is not a destination without
generating a dead link.

---

## 4. Worked instance — the `license` panel at 1200px

At 1200px viewport width, the `license` pillar's mega-panel renders as follows.

The nav gap computes to `1.15vw` = 13.8px, within the clamp range, so items sit tighter than the
22px maximum but above the 10px ambiguity floor. `.mm-top` computes to
`0.72vw + 0.4rem` = 8.64px + 6.4px = 15.04px ≈ `0.94rem`, which exceeds the `0.9rem` ceiling and
is therefore clamped **to** `0.9rem` — the original fixed value. Nine items render at full
specified size.

The viewport is above 1180px, so the mega-menu displays and `.nav-toggle` is hidden. It is below
1280px, so the utility band is glyph-only: `⊢ ◉ →` with `aria-label`s intact.

The panel itself carries five group headings, each now an `.mm-hub` anchor: The Instrument
(`/license/ml-2-3/`), The Register (`/license/harms/`), Operative Machinery
(`/license/machinery/`), Compliance (`/license/statement/`), Falsification & History
(`/license/falsification/`). Each carries a `live` badge with a text label. Hover-intent is 220ms,
unchanged from DS-00 §4.

One reader-visible consequence is worth naming: at 1200px, a reader can reach
`/license/falsification/` — the hub collecting objections, withdrawals, defects and open questions
— **in one click from any page in the estate.** Before the `.mm-hub` change that hub existed and
required a reader to first visit a leaf beneath it. The geometry of a menu determines what is
one click away, and what is one click away is a statement of priorities.

---

## 5. Failure modes

**The type floor breached by a future item.** Adding a tenth pillar re-runs the arithmetic of §2
and this time `clamp()` cannot absorb it: nine was the number the floors were computed against.
The signature is nav labels rendering at the `0.78rem` floor at wide viewports rather than only at
narrow ones. The remedy is a governance decision, not a CSS change.

**Glyph-only state shipped without `aria-label`.** Silent, invisible in review, and total for the
affected reader: three unlabelled links. This is the failure this document is most concerned to
prevent, and it is the reason §3.3 states the markup rather than describing it.

**Hover-intent on touch.** Removing the `matchMedia("(hover: hover)")` guard — an easy
simplification that appears to change nothing — makes mega-panels open on scroll on every touch
device in the desktop range.

**`vh` instead of `dvh`.** Reintroducing `max-height: calc(100vh - 66px)` puts the last items of
the mobile menu below the fold on mobile browsers whose address bar is visible. The bug reproduces
only on a real device.

**Wrap at 1000–1179px if the breakpoint is reverted.** Someone restoring the 1000px switch to
"recover" the desktop nav on laptops gets a two-line header, a 112px sticky bar, and a broken
hero offset on all 321 pages. Recorded here because it is the most plausible well-intentioned
regression in the document.

---

## 6. Accessibility floors this instrument must respect

| Floor | Requirement | Status |
|---|---|---|
| Touch target | `.nav-toggle` `min-height: 44px`; `.btn` `padding: 15px 26px` | **Fixes [DEF-022](../00-governance-map/defect-register.md#def-022)** (was 42px / `14px 26px`) |
| Reduced motion | The `prefers-reduced-motion` block suppresses all nine ambient animations, including hover-intent transitions | **Unshipped — [B-16](../00-governance-map/launch-blockers.md)** |
| Labelling | Every glyph-only control carries `aria-label`; every glyph carries `aria-hidden` | Required by §3.3 |
| Contrast | Nav labels and badges ≥4.5:1 against `--bg` and against every gradient they overlay | Required |
| Badge semantics | Every `.mm-badge` renders a text label; colour is never the sole carrier | Required |
| Keyboard | Mega-panels open on focus as well as hover; `Esc` closes; focus order follows visual order | Required |

**On the reduced-motion gap.** It is a **design-system** defect, not a demo defect — the token
layer is what the live demo was built to establish, so the defect is inherited by production
intact ([C-14](../00-governance-map/corrections-log.md#c-14)). It survives the demo re-levelling
at full authority and remains launch-blocking. The user preference exists precisely so that a
site need not guess: the reader has already answered, and nine infinite animations run over that
answer.

**On the touch-target fix.** The margin is small — 42px against a 44px floor — and the reason to
fix it before launch rather than after is that it is the *cheapest possible falsification* of an
accessibility claim. [MX-010](../corpus/mx-010-accessibility.md) asserts conformance; a ruler
disproves it. No expertise and no assistive technology required.

---

## 7. Limits

**Class: technical.** This instrument governs the nine-item case and does not generalise. The
`clamp()` floors were computed against nine labels of the estate's actual lengths; a tenth pillar,
or renaming "Method" to something longer, invalidates the arithmetic rather than degrading it.

**Class: epistemic.** 1180px is derived from label lengths in **English**. The Arabic mirror's
labels — توب‑تِك, المنهج, الصعود, ميتا‑إكس, الأكاديميات, الشهادات, المكتبة, الرخصة, عن ميتا‑إكس —
have different metrics in a different script and RTL flow, and this document does **not** claim to
have verified that 1180px is correct for them. That is an unverified claim and is marked as one;
it must be measured before the mirror ships
([RAT-22](../00-governance-map/open-questions-and-ratifications.md#rat-22)).

**Class: governance.** It does not decide whether the ninth pillar exists. If RAT-19 folds
`Method`, §§2–3 are superseded and the estate reverts to eight items and a 1000px switch.

---

## 8. Falsifier

This instrument is wrong if any of the following is observed:

1. Nine nav items wrapping to a second line at any viewport ≥1180px — falsifying the breakpoint.
2. `.mm-top` rendering at the `0.78rem` floor at viewports above 1180px — falsifying the
   `0.72vw + 0.4rem` preferred value.
3. A mega-panel opening on scroll on a touch device — falsifying the `hover` guard's sufficiency.
4. The Arabic nav wrapping at 1180px where the English does not — which would falsify §7's
   unverified parity assumption and is the most likely of the five.
5. A reader unable to reach any of the 45 group hubs from the navigation — falsifying §3.4.

---

## 9. Obligation

**For the build agent:** ship §3's four rules together. Shipping the 1180px breakpoint without the
`clamp()` scale produces a nav that fits at 1180px and wraps at 1181–1400px, which is worse than
either change alone. Emit `aria-label` on every utility link without exception.

**For the reviewer:** test at 999px, 1000px, 1179px, 1180px, 1279px, 1280px and 1400px. Six of
those seven are boundaries, and boundary behaviour is the entire content of this document.

**For the editor, if RAT-19 folds `Method`:** the reversion is bounded and should be recorded, not
improvised. Eight items, breakpoint back to 1000px, `clamp()` retained (it is harmless at eight
and protects against the next addition), 46 routes re-parented under `/toptech/method/`, 46 lines
appended to the redirect record — never deleted from it — and a changelog line stating why.

**Under ML‑2.3:** §H.21 (proportionate imposition) bears on the 1000–1179px trade, because the
readers who lose the mega-menu did not choose their viewport; §H.22 (language parity) is why §7's
Arabic limit is stated as an unverified claim rather than assumed away; and §H.24 (developmental
default) is why the reduced-motion block is a blocker rather than a defect.

---

**Related:** [DS-00 As-Built Token Layer](ds-00-as-built-token-layer.md) ·
[Route Manifest](../site/route-manifest.md) · [Page Contract](../site/page-contract.md) ·
[Routing Law](../site/routing-law.md) ·
[Launch Blockers](../00-governance-map/launch-blockers.md) ·
[Defect Register](../00-governance-map/defect-register.md) · [ML-2.3](../license/ml-2-3.md)

*Curated by Maher. Two `clamp()` declarations, one breakpoint moved 180px outward, and 45 group
hubs made reachable by an eight-line ternary. The Arabic metrics are unverified and this document
says so.*
