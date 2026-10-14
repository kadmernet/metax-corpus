---
doc_id: "MX-010"
title_en: "Accessibility Statement"
title_ar: "بيان إمكانية الوصول"
family: "corpus"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 2
depth: 5
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["corpus", "accessibility", "conformance", "inclusion"]
route: "/about/policy/accessibility/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# MX-010 · Accessibility Statement

**What this instrument governs.** What the estate owes a reader whose access to it is mediated by
assistive technology, by a motor or cognitive difference, by a slow connection, or by a preference
the reader has already expressed to their own browser.

**What it must not be.** A conformance badge. This estate publishes **three known accessibility
defects**, two of which are launch-blocking, and an accessibility statement that omitted them
would be the clearest possible instance of the compliance theatre its own licence names.

---

## 1. Position

Accessibility is usually written as a compliance obligation, which is why most statements of it
read like insurance documents. This instrument treats it as a **claim about who the estate is
for**, and the difference is testable in one respect: a compliance document lists conformance, and
this one leads with its failures.

Its sibling is [ST-12 Accessibility Implementation](../standards/st-12-accessibility-implementation.md),
which specifies the techniques; MX-010 states the commitment those techniques implement. Its
enforcement surface is [SITE-02 §9](../site/page-contract.md) lines 15–19, and its design surface
is [DS-07 §6](../design/ds-07-navigation-geometry.md).

**The macro register.** A corpus that asserts machine citability and neglects human accessibility
has made a revealing choice about which non-standard reader it takes seriously. Both cases are the
same problem — a reader whose access is mediated by something other than a sighted person at a
large screen — and an estate that invests in one while failing the other has optimised for the
reader who improves its reach rather than the reader who needs it. Under **HX‑21** (proportionate
imposition) the burden of an inaccessible interface falls entirely on people who did not choose
their circumstances and cannot decline them.

---

## 2. Definition — the commitment

**Target: WCAG 2.2 Level AA**, across both language trees, on every published route.

The estate additionally commits to five things WCAG does not require, each because the harms
register makes it a duty rather than a courtesy:

**1. Renders without JavaScript.** Main prose, navigation and footer present with scripting
disabled. This is the estate's own law and it is **currently violated**
([DEF-018](../00-governance-map/defect-register.md#def-018)).

**2. Legible without CSS.** Heading order alone conveys the document's structure.

**3. Honours `prefers-reduced-motion` absolutely.** All nine ambient animations suppressed — not
reduced. **Currently violated** ([B-16](../00-governance-map/launch-blockers.md)).

**4. No colour-only meaning.** Every status badge carries a text label. Four permitted values,
never a colour alone ([SITE-01 §3](../site/route-manifest.md)).

**5. No time limits anywhere.** No session timeout on reading, no countdown on an assessment, no
auto-advance. A time limit converts a comprehension task into a speed task for readers who process
differently.

### 2.1 Why "AA" and not "AAA"

AAA would be a stronger-sounding claim and a false one. It requires, among other things, a reading
level below lower-secondary education for all text — which this corpus, a governance estate written
at audience tier 5, cannot meet and should not pretend to.

**The honest position is a met AA plus five specific extras, not an unmet AAA.** An estate that
claims the higher level and fails it has taught its readers that its conformance claims are
aspirational, which devalues the ones it does meet.

---

## 3. Mechanism — the checks and where they live

| Requirement | Checked at | State |
|---|---|---|
| Contrast ≥4.5:1 against every gradient | [SITE-02 §9](../site/page-contract.md) line 17 | Specified, unrun |
| Touch targets ≥44px | line 18 | **FAILS — see §4** |
| Reduced-motion suppression | line 19 | **FAILS** |
| Renders with JS disabled | line 16 | **FAILS** |
| Legible with CSS disabled | line 15 | Specified, unrun |
| Badge text labels | line 12 | Specified, unrun |
| Glyph-only controls carry `aria-label` | [DS-07 §3.3](../design/ds-07-navigation-geometry.md) | Specified |
| Decorative layers `aria-hidden` | [SITE-02 §1.3](../site/page-contract.md) | Specified |
| Keyboard: mega-panels open on focus, `Esc` closes | [DS-07 §6](../design/ds-07-navigation-geometry.md) | Specified |

**Every row reads "specified."** [SENTINEL](../standards/st-13-static-build-and-sentinel.md) does
not run ([DEF-001](../00-governance-map/defect-register.md#def-001)), so no accessibility check in
this estate is automated. The three FAILS were found by reading code, not by testing — which means
**the estate does not know how many more there are.**

---

## 4. Worked instance — the 42-pixel button

`.nav-toggle` is 42px. `.btn` is `14px 26px` on a 100px radius. The floor is 44px. The corrections
are `min-height: 44px` and `padding: 15px 26px`
([DEF-022](../00-governance-map/defect-register.md#def-022)).

**Two pixels.** It is the smallest defect in the register, and it is worth the section because of
what it demonstrates.

**It is the cheapest possible falsification of an accessibility claim.** No expertise, no assistive
technology, no audit. A ruler. Anyone can check it in under a minute, and if they check it they
find this instrument's conformance claim false.

**It was not found by the accessibility standard.** [ST-12](../standards/st-12-accessibility-implementation.md)
exists, specifies target sizes, and did not catch it — because ST-12 is a specification and nothing
measured the built artefact against it. It was found by
[fetching the live site and reading the CSS](../00-governance-map/corrections-log.md#method-what-this-log-has-learned),
the same method that produced nine of the estate's sixteen corrections.

**Who it affects, concretely.** A reader with a tremor, or using a phone one-handed on a moving
train, or with larger fingers than the designer. They do not file accessibility complaints; they
mis-tap, get the wrong page, and leave. **The defect is invisible to the estate by construction** —
its cost is borne entirely by people who never report it.

That is the general shape of an accessibility failure, and it is why this instrument cannot rely
on complaints as a detection mechanism.

---

## 5. The three current failures, stated plainly

**No `prefers-reduced-motion` block.** Nine infinite ambient animations run over an expressed user
preference. The preference exists precisely so a site need not guess — **the reader has already
answered** — and the estate overrides it. [B-16](../00-governance-map/launch-blockers.md),
launch-blocking. It is a **design-system** defect, not a demo defect: the token layer is what the
demo was built to establish, so production inherits it intact
([C-14](../00-governance-map/corrections-log.md#c-14)).

**Nothing renders without JavaScript.** No header, no footer, no navigation, no pillars.
[DEF-018](../00-governance-map/defect-register.md#def-018),
[RAT-17](../00-governance-map/open-questions-and-ratifications.md#rat-17). The estate's position is
that **the build changes, not the law** — the law is the more valuable of the two, and it is the
same argument §E.7 makes for the licence text: a document that depends on a script is a document
that can be made unreadable.

**Touch targets below 44px.** §4.

**What these three have in common.** Each was already specified. Each is a few lines of CSS or a
build step. None is a hard problem, and all three have survived three releases — which supports
[HX-002 §8](../harms/hx-002-harm-instrument-map.md)'s finding that the estate's failure is **rules
without mechanisms**, not bad rules.

---

## 6. Failure modes

**The statement as a badge.** Publishing conformance without testing it. The failure this
instrument's structure is designed to prevent, by putting §5 before any claim of compliance.

**Overlay remediation.** An accessibility widget layered over an inaccessible site. Prohibited
outright: it degrades the experience for actual assistive-technology users while producing a
compliance appearance, which is **HX‑15** in its purest form.

**Automated testing mistaken for conformance.** Automated checks catch perhaps a third of WCAG
criteria. An estate reporting "zero automated violations" has reported a third of an answer.

**Accessibility deferred to a later wave.** Retrofitting costs an order of magnitude more than
building it in, and the deferral always lands on the same readers.

**Decoration unmarked.** `.cosmos`, `.grid-veil` and `.marquee` must carry `aria-hidden`. The
marquee is a moving text strip: unmarked, it interleaves meaningless fragments into the reading
order — **worse than absent**, and worst for exactly the readers least able to ignore it.

---

## 7. Limits

**Class: technical.** No automated check runs. Conformance is unmeasured, and §3's table is a
specification rather than a result.

**Class: epistemic.** **No assistive-technology user has tested this estate.** No screen-reader
pass, no keyboard-only pass, no cognitive-load review. The three known defects were found by
reading code, which detects a narrow class of failure — a corpus can be technically conformant and
practically unusable, and the estate has no evidence either way.

**Class: governance.** [DEF-003](../00-governance-map/defect-register.md#def-003) records that
accessibility conformance was *committed to but never tested*, and it has been open since the first
release.

**Class: linguistic.** The Arabic tree has **zero pages**
([DEF-002](../00-governance-map/defect-register.md#def-002)), so RTL accessibility is entirely
untested — including [DS-07 §7](../design/ds-07-navigation-geometry.md)'s admission that the 1180px
breakpoint was derived from English label metrics and is **unverified for Arabic**
([V-08](../00-governance-map/verification-log.md)).

---

## 8. Falsifier

1. **A conformance failure found by a reader** that §3's table claims is checked. Expected, and
   every instance is a valid correction.
2. **An assistive-technology user finding the estate unusable despite AA conformance** — falsifying
   AA as a sufficient target rather than falsifying this instrument.
3. **The three known defects persisting through publication.** They are individually trivial and
   have survived three releases; persisting into a public launch would falsify the estate's claim
   to treat accessibility as a commitment rather than a preference. **Closest to firing.**
4. **A reduced-motion suppression that degrades comprehension**, showing §2's requirement 3 too
   absolute. Unlikely, and the estate should test rather than assume.

---

## 9. Obligation

**For the estate, in order of cost.** Ship the `prefers-reduced-motion` block and the two
touch-target corrections — CSS measured in minutes, standing between this corpus and an honest
conformance claim. Then resolve [RAT-17](../00-governance-map/open-questions-and-ratifications.md#rat-17)
toward pre-rendering. Then commission a real assistive-technology pass, because §7 records that the
estate has no evidence about the thing it claims.

**For any author:** decoration carries `aria-hidden`. Glyph-only controls carry `aria-label`.
Status is never colour alone. No time limits, anywhere.

**For an academy under [MX-004](mx-004-terms-of-top-levels.md):** §2's commitment is inherited in
full, including the five extras, and is not waivable on a subdomain.

**For a reader:** if any part of this estate is unusable with your assistive technology, that is a
defect and it outranks most of what is in the register. File at
`/library/record/corrections-log/` — rejected submissions are published with reasons.

**Under ML-2.3:** §H.21 (proportionate imposition — the burden falls on readers who did not choose
it), §H.23 (channel parity), §H.22 (language parity — §7's Arabic limit), §H.24 (developmental
default), §H.15 (compliance theatre — why §5 precedes any conformance claim).

---

**Related:** [ST-12 Accessibility Implementation](../standards/st-12-accessibility-implementation.md) ·
[DS-07 Navigation Geometry](../design/ds-07-navigation-geometry.md) ·
[DS-00 As-Built Token Layer](../design/ds-00-as-built-token-layer.md) ·
[SITE-02 Page Contract](../site/page-contract.md) ·
[Launch Blockers B-16](../00-governance-map/launch-blockers.md) ·
[Defect Register](../00-governance-map/defect-register.md) ·
[MX-023 Attention and Human Sovereignty](mx-023-attention-and-human-sovereignty.md)

*Curated by Maher. A WCAG 2.2 AA target plus five extras, three known failures, zero tests by an
actual assistive-technology user — and the smallest defect in the register is a button two pixels
short of the floor, which anyone can disprove with a ruler.*
