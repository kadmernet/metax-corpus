---
doc_id: "DS-02"
title_en: "Motion, Attention and the Anti-Engagement Commitments"
title_ar: "الحركة والانتباه والتزامات مقاومة الإدمان"
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
derived_from: ["MX-DESIGN-001 Part 2", "MX-DESIGN-001 Part 6", "MX-DESIGN-001 Part 10"]
last_reviewed: "2026-08-30"
domain_tags: ["design", "accessibility", "ethics"]
ai_disclosure_url: "../corpus/mx-007-ai-use-and-disclosure.md"
hreflang: "en, ar"
---

# DS-02 — Motion, Attention and the Anti-Engagement Commitments

**Governs:** every animation in the estate, and the commitments that constrain them.
**Reconciled at** [R-29](../00-governance-map/reconciliation-ledger.md#r-29--animation-against-the-refusal-of-attention-economics)
and [R-36](../00-governance-map/reconciliation-ledger.md#r-36--anti-engagement-commitments-are-given-falsifiers).

## 0. The problem this document solves

Animation was requested to draw attention to important elements.
[Charter §0.4](../corpus/mx-000-charter.md#04-what-metax-refuses) refuses attention-economic
mechanics. The source document states the tension in its own words:

> *"A corpus that rejects attention economics cannot itself run on attention mechanics."*

The resolution is a single principle from which every rule below follows: **motion is admitted
only where it carries information, and it is spent on what the reader would be harmed by
missing — never on what MetaX would benefit from them noticing.**

That asymmetry is testable. Look at §1's T3 tier: all four permitted looping elements are **bad
news**. Nothing good ever loops. If a future release adds a celebratory loop, this document has
been violated, and §5 makes that a published defect rather than a matter of taste.

---

## 1. The four tiers

### T0 — Static

Body copy, tables, source lists, legal text. **Never animates.**

This is roughly **80% of the estate by page count, and that ratio is a budget, not an
accident.** It is measured per release. A release in which T0 falls below 75% is a defect
against this document, because the drift from "documentation with some motion" to "an
experience" happens one justified exception at a time.

### T1 — Entrance reveal

One-shot, on **first** viewport entry only.

| Property | Value |
|---|---|
| Duration | 240 ms |
| Transform | 12 px translate + opacity |
| Stagger | 40 ms across siblings |
| Stagger cap | **6 items** |
| Replay | **Never on scroll-back** |

Applied to: `mx-archetypecard`, `mx-branchmatrix` cells, `mx-principlegrid`, `mx-seriescard`
grids. The stagger cap exists because a 12-item stagger is a performance, and the seventh item
carries no information the first six did not.

### T2 — State feedback

**120–180 ms**, responds to input only.

Permitted: hover lift on cards (2 px, **desktop pointer only**), focus ring bloom, accordion
expansion of `mx-lessonarc`, mega-nav panel open, toast entry.

**Prohibited estate-wide: cursor-following effects and parallax.** Both are motion that
responds to the reader without telling them anything.

### T3 — Persistent signal

The only tier permitted to loop. **Exactly four elements qualify, ever:**

| Element | Why it may loop |
|---|---|
| A `DEFECT` badge | The reader is looking at something known to be wrong |
| A `GATED` badge on the BCIA Gateway | The reader is about to trust unreviewed research |
| A revoked credential on the verifier | Someone is checking a credential that was withdrawn |
| An expired-decay chip past review date | The claim in front of the reader may be stale |

| Property | Value |
|---|---|
| Animation | 2.4 s opacity breath, 0.72 → 1.0 |
| Scale change | **None** |
| Stop condition | Permanently, after 8 cycles **or** on any user interaction |

All four are warnings. **Nothing celebratory loops. There is no confetti in this universe.**

Adding a fifth T3 element requires amending this document, and the amendment must state which
of the four tests above the new element passes.

---

## 2. Named animations

| Name | Behaviour | The information it carries |
|---|---|---|
| `mx-reveal` | T1 base | Grouping and order |
| `mx-countup` | Computed statistics in `mx-metastrip` count from zero over 900 ms, easing out — **final value present in the DOM from the start** | Magnitude. Correct without JS, per [ST-19 §3.4](../standards/st-19-two-plane-architecture.md#34-failure-transparency-and-how-it-is-proved) |
| `mx-bridge-draw` | SVG line draws from the Limits panel to the Bridge card, 600 ms | Makes the pedagogical dependency **physically visible** |
| `mx-limits-unfold` | Four limit classes stagger open — **epistemic first, economic last** | The order MetaX considers them binding |
| `mx-ladder-climb` | Ascent rungs illuminate sequentially, 80 ms apart, **stopping at the visitor's current rung** if the identity bar reports one | Position in a sequence |
| `mx-verify-stamp` | Result lands with 180 ms scale-from-1.04 and one shadow settle | **The one moment in the estate designed to feel consequential** |
| `mx-gate-lock` | A gated card's border **draws closed** rather than pulsing | Closure, without the nag of a pulse |

Two of these are doing pedagogical work rather than decorative work, and they are the reason
this document permits motion at all. `mx-bridge-draw` makes the Limits-before-Bridge dependency
a thing the reader *sees* instead of a rule they are told. `mx-limits-unfold` encodes a
priority ordering into the order of appearance — the sequence is the argument.

`mx-verify-stamp` is the deliberate exception to the estate's flatness. Verification is the
moment where MetaX asserts something about a person to a third party, and it should not feel
like loading a table.

---

## 3. Reduced motion

`prefers-reduced-motion: reduce` is **honoured absolutely, not softened.** No "gentler
version", no reduced duration.

| Tier | Reduced-motion behaviour |
|---|---|
| T1 | Instant opacity 1 |
| T2 | Instant state change |
| T3 | **Static high-contrast outline + a text label** |
| `mx-countup` | Prints the final number immediately |
| `mx-bridge-draw` | Renders the completed line |

The T3 row is the one that matters: **the information survives, the motion does not.** A reader
who disables motion must still learn that the credential in front of them is revoked. Any T3
element whose meaning exists only in its loop is a defect, because it has made an accessibility
preference into an information loss.

---

## 4. Performance contract

| Constraint | Value |
|---|---|
| Animatable properties | `transform` and `opacity` **only** |
| Scroll-linked layout animation | Prohibited |
| CLS | Target **0.00**, hard ceiling 0.05 |
| INP | < 200 ms at p75, mid-tier Android on 4G |
| Total animation CSS | **< 6 KB** |

**Any component that cannot meet this ships without motion.** The component still ships. The
motion is what is negotiable, and it is negotiable in exactly one direction.

---

## 5. The anti-engagement commitments

These are stated **in the UI itself**, not only here, and each is a claim card with a falsifier
under [ST-04](../standards/st-04-falsifiability-and-claim-cards.md).

**Refused outright:** streaks · leaderboards · infinite feed · notification badges with counts
designed to itch.

**Notifications** are a weekly digest, **off by default** for everything except three classes
that have real consequences: credential status changes, review deadlines, and decay alerts.

**Progress is measured in artefacts, not minutes.** There is no video-percentage bar, because a
percentage of a video watched is not evidence of anything. A series shows, per course, three
binary states — artefact submitted, artefact reviewed, capstone pre-registered. **No fabricated
continuum.**

### 5.1 The falsifier

Published on `me.metax.academy/digest/`:

> *If MetaX ever ships a streak counter, that page becomes a published defect.*

This is the required form under ST-04 and it is why these commitments are canon rather than
copy. A commitment with a named falsifier can be checked by a stranger; a commitment without
one is a value statement, and value statements survive their own violation.

---

## 6. Conformance

| Rule | Enforced by | Failure |
|---|---|---|
| T0 ≥ 75% of pages | Per-release motion census | Defect |
| Animated properties limited to `transform`/`opacity` | CSS static analysis | Build failure |
| Animation CSS < 6 KB | Bundle gate | Build failure |
| Every animation has a reduced-motion equivalent **preserving information** | Reduced-motion render diff | Build failure |
| No fifth T3 element | Registry of T3 selectors | Build failure |
| No parallax / cursor-following | CSS + JS static analysis | Build failure |
| Anti-engagement commitments | Published falsifier + defect register | Public defect |

---

**Related:** [DS-01 Foundations and Tokens](ds-01-foundations-and-tokens.md) ·
[ST-15 Component Library](../standards/st-15-component-library.md) ·
[ST-12 Accessibility Implementation](../standards/st-12-accessibility-implementation.md) ·
[ST-04 Falsifiability and Claim Cards](../standards/st-04-falsifiability-and-claim-cards.md) ·
[MX-022 Identity & Sessions](../corpus/mx-022-identity-and-sessions.md)

*Curated by Maher. Motion was requested. What was granted is motion that warns, teaches or
confirms — and nothing that flatters MetaX for having been visited.*
