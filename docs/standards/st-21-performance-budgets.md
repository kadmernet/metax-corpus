---
doc_id: "ST-21"
title_en: "Performance Budgets and Enforcement"
title_ar: "ميزانيات الأداء وإنفاذها"
family: "standard"
version: "v2026.09.2"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 4
evidence_class: "semi-durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.1"
derived_from: ["MX-DESIGN-001 Part 10", "MX-DESIGN-001 Part 2"]
last_reviewed: "2026-08-30"
domain_tags: ["performance", "accessibility", "build"]
ai_disclosure_url: "../corpus/mx-007-ai-use-and-disclosure.md"
hreflang: "en, ar"
---

# ST-21 — Performance Budgets and Enforcement

**Governs:** every byte the estate ships, and what happens when a page exceeds its allowance.

## §1 The rule that makes the rest work

> **A page exceeding budget fails the build. There is no override flag.**

The absence of an override is the entire control. A budget with an escape hatch is a suggestion,
and every suggestion loses to a deadline — not through bad faith but because the person holding
the deadline is always more specific than the person holding the principle.

There is no "exceptional page" class, no annotation that suspends a check, and no environment
variable. Adding one would require amending this standard in public, which is the intended cost.

---

## §2 The budgets

| Resource | Content plane | Identity plane |
|---|---|---|
| HTML | ≤ 60 KB | ≤ 60 KB |
| CSS | **≤ 40 KB estate-wide** — a single shared file | shared file |
| JS | **≤ 12 KB** (of which the island is ≤ 4 KB) | ≤ 60 KB |
| Fonts | ≤ 180 KB subset per locale | same |
| Animation CSS | < 6 KB | < 6 KB |
| LCP | < 1.8 s on 4G mid-tier | same |
| CLS | target **0.00**, ceiling 0.05 | same |
| INP | < 200 ms at p75, mid-tier Android on 4G | same |

**Fonts** ship with `font-display: swap` and **metric-compatible fallbacks** — a fallback with
different metrics converts a font swap into a layout shift, which is how a CLS target of 0.00 is
lost by a decision that looked typographic.

### §2.1 Why CSS is estate-wide rather than per-page

One shared 40 KB file, cached once, serves every page on both planes. Per-page CSS would let the
total grow without any single page exceeding a budget — the classic way an estate becomes heavy
while every individual measurement passes.

### §2.2 Why the content-plane JS budget is 12 KB

Because the content plane's contract is that it works **without** JavaScript
([ST-19 §1.1](st-19-two-plane-architecture.md#11-content-plane)). JS there is decoration, and 12 KB
is a generous allowance for decoration. The 4 KB island is the only script that runs on every
page.

### §2.3 The device the targets are measured on

**A mid-tier Android device on 4G.** Not a desktop, not a flagship phone, not a throttled
simulation of a fast connection.

This choice is substantive, not technical. MetaX claims Arabic-market authority
([MX-020](../corpus/mx-020-language-authority.md)), and a curriculum tested on the author's own
laptop is a curriculum optimised for the author's own market. The reference device is part of the
accessibility commitment, not separate from it.

---

## §3 What is measured, and where

| Measured | When | Method |
|---|---|---|
| Byte budgets | Every build | Static, per page and estate-wide |
| LCP, CLS, INP | Every build | Lab, on the reference device profile |
| CLS attributable to the island | Every build | Differential: island enabled vs stubbed |
| Reduced-motion equivalence | Every build | Render diff under `prefers-reduced-motion` |
| Third-party requests | Every build | Network audit; **expected count is zero** |
| Field metrics | Continuously | Aggregate, cookieless, **published** ([DS-06 §6.5](../design/ds-06-error-and-empty-states.md#65-analytics-posture)) |

Field metrics being **published** is what makes this standard falsifiable. Lab budgets prove the
build passed a test MetaX wrote; published field data lets a reader check whether the estate is
actually fast for anyone but its author.

---

## §4 The rule for components that cannot comply

> **Any component that cannot meet the performance contract ships without motion.**

The component still ships. The motion is what is negotiable, and it is negotiable in exactly one
direction. This is the same asymmetry as [DS-02](../design/ds-02-motion-and-attention.md): where
information and animation compete, information wins by default rather than by argument.

Only `transform` and `opacity` are animated; no scroll-linked layout animation exists anywhere.

---

## §5 Interaction with other gates

A build must pass **all** of the following, and they are not tradeable against one another:

| Gate | Standard |
|---|---|
| Performance budgets | This standard |
| Front-matter validity | [ST-02](st-02-front-matter-schema.md) |
| Computed counts — **no typed count anywhere** | [ST-13 §4](st-13-static-build-and-sentinel.md#4-computed-counts) |
| No dangling internal link | [ST-13](st-13-static-build-and-sentinel.md) |
| Limits-and-Bridge presence | [ST-03](st-03-limits-and-bridge.md) |
| Falsifier presence | [ST-04](st-04-falsifiability-and-claim-cards.md) |
| Single-source drift | [ST-13](st-13-static-build-and-sentinel.md) |
| **No unresolved placeholder rendered as a value** | [B-07](../00-governance-map/launch-blockers.md#b-07--no-page-may-render-a-placeholder-as-a-value--hard-blocker-standing) |
| Island failure transparency | [ST-19 §3.4](st-19-two-plane-architecture.md#34-failure-transparency-and-how-it-is-proved) |
| WCAG 2.2 AA, gradients tested at **both extreme stops** | [ST-12](st-12-accessibility-implementation.md) |

**None of these currently run.** SENTINEL is a specification, not a pipeline, which is
[B-06](../00-governance-map/launch-blockers.md#b-06--the-build-cannot-yet-enforce-its-own-rules--hard-blocker)
— and until it runs, every sentence in this standard describes an intention rather than a control.
That distinction is stated rather than blurred, because a corpus that claims mechanical enforcement
it does not have has made the exact error it built these gates to catch.

---

**Related:** [ST-13 Static Build and SENTINEL](st-13-static-build-and-sentinel.md) ·
[ST-19 Two-Plane Architecture](st-19-two-plane-architecture.md) ·
[ST-12 Accessibility Implementation](st-12-accessibility-implementation.md) ·
[DS-02 Motion and Attention](../design/ds-02-motion-and-attention.md) ·
[MX-010 Accessibility](../corpus/mx-010-accessibility.md)

*Curated by Maher. The budgets are unremarkable. The absence of an override flag is the standard.*
