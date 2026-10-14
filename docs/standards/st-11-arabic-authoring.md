---
doc_id: "ST-11"
title_en: "Arabic Authoring and Bilingual Parity"
title_ar: "التأليف بالعربية والتكافؤ اللغوي"
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
domain_tags: ["standards", "arabic", "rtl", "translation", "typography"]
route: "/library/standards/bilingual/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# ST-11 · Arabic Authoring and Bilingual Parity

**What this standard governs.** How Arabic text is authored, rendered and checked in this estate:
the typography, the RTL mechanics, the terminology discipline, and what a translator is required to
do rather than merely permitted.

**Its state.** **No Arabic page exists** ([DEF-002](../00-governance-map/defect-register.md#def-002)).
This is a specification written before the work, deliberately — the alternative is a translation
pipeline whose conventions are settled by whoever translates first.

---

## 1. Position

[MX-020](../corpus/mx-020-language-authority.md) states which language governs what. ST-11 states
**how the Arabic is made**, and the division is strict: MX-020 is authority, ST-11 is craft.

Published at `/library/standards/bilingual/` alongside MX-020, with the lexicon method at
`/library/lexicon/method/`.

**The macro register.** Under **HX‑22** (language parity), the failure mode of technical Arabic is
not mistranslation — it is **transliteration as a substitute for terminology**. A corpus that
renders every technical term in Latin script inside Arabic prose has not translated; it has
produced English with Arabic connectives, and it teaches its readers that the concepts belong to
another language. §4 is the estate's answer, and it is the part of this standard with actual
intellectual content.

---

## 2. Definition — the authoring requirements

**Author, do not translate, where Arabic governs.** For the Meta‑X and BCIA libraries and the
Lexicon — [MX-020 limb 1](../corpus/mx-020-language-authority.md) — Arabic is the **source**. The
English is the rendering.

**Translate faithfully, not literally, where English governs.** A translation reproducing English
syntax in Arabic has achieved correspondence and lost readability. The test: **would a competent
Arabic reader, shown only the Arabic, recognise it as written rather than converted?**

**Preserve every structural element exactly.** Identifiers, `doc_id`, section numbering, anchors,
code, front-matter field *names*, and all four badge values — `live`, `planned`,
`research-preview`, `gated`. **Badges are never mirrored**
([MX-020 §3](../corpus/mx-020-language-authority.md)).

**Numerals are Western Arabic** (0–9), not Eastern Arabic-Indic. A deliberate choice for
citation stability: a figure copied from a page must match the figure in the data file.

**Same evidence class, same review date, same falsifier.** Editorial parity is not optional; a page
whose Arabic edition carries a stale review date **has diverged**, and under
[MX-020 limb 4](../corpus/mx-020-language-authority.md) that is a filed defect.

---

## 3. Mechanism — RTL rendering

```html
<html lang="ar" dir="rtl">
```

| Element | Requirement |
|---|---|
| Layout | Mirrors. Nav, rails, `.mx-related` groups, table column order |
| Gradients | **Unchanged.** Not mirrored — a gradient is not directional content |
| Glyphs `✦ ⬡ ◉ ⊢ →` | `⊢` and `→` **mirror**; `✦ ⬡ ◉` do not |
| Code blocks | **LTR inside an RTL page.** `dir="ltr"` on every `<pre>` |
| Inline identifiers | `MX-024`, `HX-15`, `/toptech/start/` — LTR, with explicit isolation |
| Punctuation | Arabic comma `،` and semicolon `؛` in prose; ASCII inside code and identifiers |
| Fonts | An Arabic face with full diacritic support; Space Grotesk and Inter are Latin-only |

### 3.1 Bidirectional isolation is the mechanical trap

An identifier or path inside Arabic prose reorders visually without isolation. `MX-024` adjacent to
Arabic text can render as `024-MX`, and **the text is not corrupt — only its display is**, so it
survives copy-paste review and fails on the page.

```html
<bdi>MX-024</bdi>   <span dir="ltr">/toptech/start/</span>
```

Every inline Latin-script identifier, route or code fragment is isolated. This is the single most
likely rendering defect in the Arabic tree and the least likely to be caught by a reviewer reading
the source rather than the render.

---

## 4. Terminology — the estate's substantive contribution

**Three permitted treatments, in order of preference.**

**1. An established Arabic term, where one exists.** Not a coined one.

**2. A coined term with the Latin term in parentheses at first use**, where the concept is genuine
and no Arabic term exists. The coinage enters the
[Lexicon](../lexicon/keyword-register.md) with its reasoning.

**3. Transliteration**, only where the term is a **proper name or a brand** — `MacroLifeTech`,
`Cloudflare`, `Binance Pay`.

**Transliteration of a concept is prohibited.** Rendering *falsifiability* phonetically in Arabic
script names nothing; it borrows a sound. Treatment 2 exists precisely to avoid it, and the
estate accepts that coinage is harder and sometimes contested — which is why
`/library/lexicon/contested/` exists as a route.

**The Lexicon governs**, and it is [MX-020 limb 1](../corpus/mx-020-language-authority.md)
material: **Arabic-authoritative.** So the Arabic term is the source and the English gloss is the
translation — the one place in this corpus where the ordinary direction reverses, and the reason
[the designation list](../license/designation-list.md) designates the Lexicon.

---

## 5. Worked instance — translating a `.mx-pagestamp`

`live · semi-durable · v2026.10.1 · reviewed 2026-10-01`

**Badge `live`** — **not translated.** An estate-wide status value with four permitted forms
([SITE-01 §3](../site/route-manifest.md)). Translating it breaks the badge vocabulary and makes the
two trees incomparable.

**`semi-durable`** — **translated**, using the Lexicon's established Arabic term for the decay
class. This is a *concept*, so treatment 1 or 2 applies and transliteration is prohibited.

**`v2026.10.1`** — **isolated LTR**, `<bdi>`. Without isolation the version renders reordered
beside Arabic text.

**`reviewed 2026-10-01`** — the word translated, the date **Western Arabic numerals, isolated**,
and **identical to the English page's date.** A different date is a divergence, and under
[MX-020 limb 4](../corpus/mx-020-language-authority.md) a defect.

**What the instance shows.** Four fields, four different treatments, and **only one is a
translation.** One is preserved verbatim, one is isolated, one must match exactly. A translator
working without this standard would translate all four — producing a page that reads well, reports
a mirrored badge, and has silently diverged from its twin.

---

## 6. Failure modes

**Transliteration as translation.** §4. The characteristic failure of technical Arabic, and it
compounds: once a transliteration is published it becomes the term.

**Missing bidirectional isolation.** §3.1. Invisible in source review, visible on every page.

**Badge translated.** Breaks comparability.

**Eastern Arabic-Indic numerals.** Breaks citation matching against data files.

**Review date diverging.** The Arabic page falls behind and its pagestamp is updated anyway, so
parity is asserted where it does not hold.

**Latin-only fonts inherited.** The Arabic tree rendering in a fallback face, usually without full
diacritic support. Nothing errors.

---

## 7. Limits

**Class: practical, and it dominates.** **Zero Arabic pages.** Every rule here is untested, and
§4's terminology discipline is the part most likely to need revision once a real translator
applies it.

**Class: competence.** This standard was drafted by an AI system whose Arabic authoring judgement
is **not established**. §4's terminology preferences and §3's typographic rules require review by a
competent Arabic technical editor, and **none has seen them.** Filed as a `[VERIFY]` claim
alongside [V-08](../00-governance-map/verification-log.md), and it is a more serious limit than
the breakpoint measurement.

**Class: technical.** No mechanism checks any of this. The tree diff and the isolation check would
live in [SENTINEL](st-13-static-build-and-sentinel.md), which does not run.

**Class: economic.** ≈385,000 words of authoritative Arabic with no translator and no budget
([RAT-22](../00-governance-map/open-questions-and-ratifications.md#rat-22)).

---

## 8. Falsifier

1. **A competent Arabic technical editor finding §4's terminology discipline unworkable** — that
   coinage is impractical and transliteration is how the field actually communicates. **The
   likeliest to fire**, and §7 records that no such editor has reviewed it.
2. **Structural preservation producing unreadable Arabic** — if identical paths, English slugs and
   preserved identifiers make the Arabic estate feel foreign, §2 has traded auditability for
   readability wrongly.
3. **Bidirectional isolation proving insufficient** for some construction the estate uses.
4. **Western Arabic numerals rejected by readers**, falsifying the citation-stability trade.

---

## 9. Obligation

**For a translator:** author where Arabic governs; translate faithfully where English governs.
Preserve identifiers, badges and structure. Isolate every Latin fragment. Never transliterate a
concept. Match the review date exactly, or **file the divergence as a defect** rather than papering
it.

**For the estate:** have this standard reviewed by a competent Arabic technical editor **before
the first page ships.** §7's competence limit is the one gap no further drafting closes — the same
shape as [DEF-031](../00-governance-map/defect-register.md#def-031), and the same remedy: a second
person.

**Under ML-2.3:** §H.22 (language parity), §H.23 (channel parity), §H.07 (access foreclosure),
§H.19 (authorship of record — a translator is an author and is recorded).

---

**Related:** [MX-020 Language Authority](../corpus/mx-020-language-authority.md) ·
[ST-01 Identifier Grammar §5](st-01-identifier-and-url-grammar.md) ·
[SITE-01 Route Manifest §1.6](../site/route-manifest.md) ·
[DS-07 Navigation Geometry](../design/ds-07-navigation-geometry.md) ·
[Keyword Register](../lexicon/keyword-register.md) ·
[Verification Log](../00-governance-map/verification-log.md)

*Curated by Maher. Seven RTL rules, three terminology treatments, one prohibition on
transliterating a concept — none of it reviewed by anyone who writes technical Arabic, which this
standard states rather than assumes away.*
