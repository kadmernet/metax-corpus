---
doc_id: "DS-01"
title_en: "Design Foundations, Tokens and the Gradient System"
title_ar: "أساسات التصميم والرموز ونظام التدرجات"
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
derived_from: ["MX-DESIGN-001 Part 0", "MX-DESIGN-001 Part 1"]
supersedes: ["Component notes, v2026.08.12"]
last_reviewed: "2026-08-30"
domain_tags: ["design", "accessibility", "frontend"]
ai_disclosure_url: "../corpus/mx-007-ai-use-and-disclosure.md"
hreflang: "en, ar"
---

# DS-01 — Design Foundations, Tokens and the Gradient System

**Governs:** breakpoints, grid, type, logical properties, and the ten brand gradients.
**Corpus ref of the source:** MX-DESIGN-001 · **Reconciled at**
[R-28](../00-governance-map/reconciliation-ledger.md#r-28--gradients-against-the-ink-and-paper-identity).

The established identity is **Ink and Paper** — austere, print-derived, deliberately
unfashionable. This document adds gradients to it without dissolving it, which is possible only
because gradients are confined to a layer that never touches running text.

---

## 1. Mobile-first, and what that actually constrains

Every component is authored at **360 px first** and enhanced upward. No component may be
designed at desktop and "made responsive" afterwards — the build lints for desktop-only CSS
lacking a mobile counterpart, and the lint is a build failure.

| Token | Min width | Columns | Gutter | Container | Primary use |
|---|---:|---:|---:|---|---|
| `xs` | 360 | 4 | 16 | 100% − 32 | Baseline phone |
| `sm` | 480 | 4 | 20 | 448 | Large phone |
| `md` | 768 | 8 | 24 | 720 | Tablet portrait |
| `lg` | 1024 | 12 | 24 | 960 | Tablet landscape / small laptop |
| `xl` | 1280 | 12 | 32 | 1180 | Desktop |
| `2xl` | 1600 | 12 | 32 | 1320 (capped) | Large desktop |

### 1.1 Non-negotiables

- **Reading measure is capped at 68 characters at every width.** The container may grow; the
  paragraph may not. A 1600 px monitor gets whitespace, not a 140-character line.
- **Touch targets ≥ 44 × 44 px with 8 px separation.**
- On `xs` and `sm`, **all primary actions** sit in the bottom 40% thumb zone or in a sticky
  action bar. **Secondary and destructive actions never do** — placing "delete" where the thumb
  rests is a designed accident.

### 1.2 Type

Fluid via `clamp()`, on a **1.200 minor-third** mobile scale expanding to **1.250 at `lg`**.
Negative letter-spacing occurs at display sizes only, nowhere else.

| Role | Latin family | Notes |
|---|---|---|
| H1 / H2 | Transitional serif | Print-derived; carries the Ink and Paper claim |
| UI, H3+ | Grotesque | |
| Arabic, all roles | Naskh-derived, **matching x-height** | So bilingual pages do not visually jump between locales |

**Arabic never uses faux-bold or faux-italic.** Weight comes from the family or not at all. A
synthesised bold on Naskh is a rendering defect wearing the costume of emphasis.

### 1.3 Logical properties and the RTL mirror

Layout uses CSS logical properties throughout — `margin-inline-start`, never `margin-left` — so
the Arabic RTL mirror is a `dir` attribute change and **not a second stylesheet**. A second
stylesheet is a second thing to forget to update.

**Exceptions that never mirror:** code blocks, terminal output, LTR identifiers such as `S042`,
chart x-axes representing time, and the credential identifier field. See
[ST-11](../standards/st-11-arabic-authoring.md).

---

## 2. Colour foundation

Flat surfaces only. Body copy sits on one of these and never on anything else.

| Token | Role |
|---|---|
| `--mx-ink` | Primary text, dark surfaces |
| `--mx-paper` | Primary background |
| `--mx-ink-muted` | Secondary text, still AA |
| `--mx-rule` | Hairlines, table borders |

### 2.1 Semantic state — the closed set

Semantic state is carried by `mx-statusbadge` colour **only**, and the set is closed:

| State | Value |
|---|---|
| Valid | `#2E6F5E` |
| Pending | `#C98A17` |
| Defect | `#A33227` |
| Frozen | `#5A6472` |

**All state conveyed by colour is duplicated in text or glyph** — without exception, per
[ST-12](../standards/st-12-accessibility-implementation.md). A badge that means something only
to a reader who can distinguish green from amber means nothing.

---

## 3. The gradient system

### 3.1 The governing rule

> **Gradients are chrome, never substrate.**

They live in hero fields, section rules, badge fills, focus states and edge treatments. **Body
copy always sits on flat Paper or flat Ink.**

**Any gradient that ever appears behind running text is a defect and is logged as one** in the
[Defect Register](../00-governance-map/defect-register.md). Not a preference, not a review note
— a defect with an owner and a date.

### 3.2 The ten ramps

Each is a three-stop linear ramp, defined once in `mx-tokens` as a custom property, with a
**mandated solid fallback** for text and small surfaces.

| Brand / surface | Name | Stops | Angle | Character |
|---|---|---|---:|---|
| MetaX Hub | **Meridian** | `#2A2F36 → #7A5A2A → #B4884A` | 135° | Curator gold rising out of ink |
| TopTech | **Forge** | `#4A2E14 → #A5642A → #E3A857` | 120° | Brass, worked metal, warm |
| Ascent | **Ridge** | `#1E3A44 → #3C6E7F → #7FB2C0` | 150° | Cold steel, altitude |
| BCIA | **Nucleus** | `#241E3A → #4B3F72 → #8B7BB8` | 135° | Violet, laboratory, unresolved |
| Academies | **Kiln** | `#3A2216 → #9A5B3E → #D08F6A` | 120° | Clay, fired, built by hand |
| Credentials & Verify | **Seal** | `#12332B → #2E6F5E → #6FAE99` | 160° | Green, attested, closed |
| Library & Lexicon | **Slate** | `#1B2126 → #55606B → #97A3AC` | 180° | Neutral, archival |
| Auth | **Vault** | `#0A0C0F → #1C2530 → #33465C` | 90° | Cold, sober, unmistakable |
| Pay | **Ledger** | `#12242E → #1F4E5F → #2E7285` | 90° | Restrained, financial, no glow |
| Me (dashboard) | **Desk** | `#F6F4EF → #EFEAE0 → #E9E4D9` | 135° | Near-flat paper; user content dominates |

Two of these are chosen against fashion on purpose. **Nucleus** is *unresolved* because BCIA's
research state is unresolved and its surface should not look finished. **Desk** is near-flat
because a dashboard that competes with the user's own artefacts is a dashboard about itself.

### 3.3 The five rules

1. **Gradients carry no semantic meaning.** Semantic state is `mx-statusbadge` colour only
   (§2.1), and **no brand ramp may use a semantic hue as its dominant stop**. Seal is the near
   miss and is permitted because *attested* and *valid* are the same idea on that surface.
2. **Maximum two gradient surfaces visible in any single viewport.** Counted at every
   breakpoint, since a two-gradient desktop layout can stack into a five-gradient phone scroll.
3. **`background-clip: text` only at display sizes ≥ 32 px**, always shipping a solid-colour
   fallback.
4. **Any gradient adjacent to text must pass 4.5:1 against its darkest *and* lightest stop —
   tested at both, never at the midpoint.** Midpoint testing is how gradient text passes audit
   and fails readers.
5. **Auth and Pay ramps are locked.** No academy may theme them. This is a security control,
   not a brand one: *a payment screen that looks different on every subdomain is a phishing
   surface.*

### 3.4 Academy theming — constrained by construction

Academy subdomains choose **one hue from a 12-swatch wheel**. The build derives a three-stop
ramp at fixed lightness values from that index. **They cannot supply arbitrary hex.**

This keeps a thousand academies visually distinct and structurally identical, and it means no
academy can produce an inaccessible surface even by trying. Contrast is a property of the
generator, not of the academy's taste. See
[ST-18](../standards/st-18-academy-json-manifest.md) for the `accent_hue_index` field.

---

## 4. Focus and interaction states

Focus indicator: **2 px accent ring plus a 1 px inverse offset ring.** The inverse ring is what
makes focus visible on gradient edges, where a single ring disappears into one of the stops. It
is visible on every background in the estate, gradients included, and that is tested rather
than assumed.

---

## 5. Conformance

| Rule | Enforced by | Failure |
|---|---|---|
| Mobile-first authoring | Desktop-only-CSS lint | Build failure |
| 68-character measure | Layout test at `2xl` | Build failure |
| Gradient behind running text | Static analysis of gradient tokens against text containers | Build failure + defect |
| Two-gradient viewport cap | Per-breakpoint visual audit | Defect |
| Contrast at both stops | Automated contrast gate, both extremes | Build failure |
| Auth/Pay lock | Token override detection | Build failure |
| Arabic faux-bold | Font-synthesis lint | Build failure |

---

**Related:** [DS-02 Motion and Attention](ds-02-motion-and-attention.md) ·
[ST-15 Component Library](../standards/st-15-component-library.md) ·
[ST-12 Accessibility Implementation](../standards/st-12-accessibility-implementation.md) ·
[ST-11 Arabic Authoring](../standards/st-11-arabic-authoring.md) ·
[ST-19 Two-Plane Architecture](../standards/st-19-two-plane-architecture.md)

*Curated by Maher. Gradients were added because they were asked for. They were confined to
chrome because the alternative was a corpus about rigour that reads like a landing page.*
