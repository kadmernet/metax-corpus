---
doc_id: "MX-020"
title_en: "Language Authority and Bilingual Parity"
title_ar: "سلطة اللغة والتكافؤ اللغوي"
family: "corpus"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 3
depth: 5
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["corpus", "language", "arabic", "parity", "translation"]
route: "/library/standards/bilingual/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# MX-020 · Language Authority and Bilingual Parity

**What this instrument governs.** Which language governs which material, what parity between the
two requires, and what a divergence between them *is*.

**The state it must disclose first.** **Zero Arabic pages exist**
([DEF-002](../00-governance-map/defect-register.md#def-002)). Every parity commitment below is a
target, and the instrument says so on its own face rather than letting a reader infer it from an
empty tree.

---

## 1. Position

Most bilingual policies are translation policies: one authoritative language, one courtesy
rendering. This estate's claim is different and more expensive — **Arabic is authoritative for part
of the corpus**, not a translation of it.

That claim has a cost the estate has not yet paid, and this instrument is where the gap between
claim and payment is recorded.

Published at `/library/standards/bilingual/`. Its implementation is
[ST-11](../standards/st-11-arabic-authoring.md); its routing consequence is
[SITE-01 §1.6](../site/route-manifest.md); its licence obligation is
[ML-2.3 §H.22](../license/ml-2-3.md), language parity.

**The macro register.** Under **HX‑07** (access foreclosure) and **HX‑22** (language parity), a
body of technical knowledge published only in English participates in a specific concentration:
the terms of the machine-mediated internet are set in one language, and practitioners elsewhere
inherit both the technology and its vocabulary. An estate whose subject is *that* concentration
cannot publish monolingually without performing it. **The commitment is therefore load-bearing
rather than decorative — and it is unfulfilled.**

---

## 2. Definition — the four limbs

**Limb 1 — Arabic governs** the Meta‑X and BCIA book libraries and the Lexicon. These were authored
in Arabic; an English rendering is the translation.

**Limb 2 — English governs** the License and the MX instruments, subject to a
**mandatory-consumer-law carve-out**: where local law gives a consumer a right in their own
language, that law governs and this limb yields.

**Limb 3 — Every instrument states its own prevailing text on its face.** The
`prevailing_text` field in front matter is **the operative statement for that document**, not a
global assumption.

**Limb 4 — A divergence between an authoritative text and its translation is a defect**, not a
matter for interpretation. Filed at `/library/record/corrections-log/`.

### 2.1 Prevailing text is not editorial standing

The distinction the estate most needs to keep visible, resolved at
[R-55](../00-governance-map/reconciliation-ledger.md#r-55--the-arabic-mirror-has-equal-standing):

| | Answers | Implication |
|---|---|---|
| **Prevailing text** | If the two texts say different things, which governs? | A conflict rule of **last resort** |
| **Editorial standing** | What does a divergence *mean*? | A **filed defect**, not an accepted consequence of translation |

`prevailing_text: "en"` on an instrument does **not** demote its Arabic edition. The Arabic page is
*"a translation of equal editorial standing and no superior authority"*
([SITE-01 §1.6](../site/route-manifest.md)) — the English governs only where they conflict, and
that they conflict at all is itself the defect.

**An estate that treats its second language as a courtesy commits the harm §H.22 names while
formally complying with it.** Limb 4 is what makes the difference operative.

---

## 3. Mechanism — what parity requires

**Structural parity.** Every route has an `/ar/` twin at the **identical path**, with English slugs
([ST-01 §5](../standards/st-01-identifier-and-url-grammar.md)). Percent-encoded Arabic paths are
legal and declined: they are unreadable in a citation, break under differing normalisation, and
**make the two trees structurally incomparable** — parity is auditable only when both trees have
the same shape.

**Presentational parity.** `<html lang="ar" dir="rtl">`, `hreflang` pairs on both, numerals Western
Arabic, gradients unchanged, **status badges never mirrored** — a badge is an estate-wide status
value, not a translatable string.

**Editorial parity.** Same evidence class, same review date, same falsifier, same
`.mx-pagestamp`. A page whose Arabic edition carries a stale review date has diverged.

**What parity does not require.** Identical sentences. A translation that reproduces English
syntax in Arabic has achieved correspondence and lost readability — and
[ST-11](../standards/st-11-arabic-authoring.md) governs the difference.

---

## 4. Worked instance — the nav breakpoint

[DS-07](../design/ds-07-navigation-geometry.md) moves the mobile→desktop switch to **1180px**,
derived from the width of nine **English** nav labels under a `clamp()` scale.

**The Arabic labels are different.** توب‑تِك · المنهج · الصعود · ميتا‑إكس · الأكاديميات · الشهادات ·
المكتبة · الرخصة · عن ميتا‑إكس — different metrics, a different script, RTL flow.

**DS-07 §7 states plainly that 1180px is unverified for Arabic**, and it is filed as
[V-08](../00-governance-map/verification-log.md). Under
[ST-07](../standards/st-07-evidence-and-verify.md) the claim is E1 for the Arabic tree and E2 for
the English.

**The check costs minutes.** Render nine RTL labels at 1180px and measure. It has not been done —
one of the four items
[DEF-030](../00-governance-map/defect-register.md#def-030) names as checkable in minutes and
deferred anyway.

**Why this instance is the right one.** It is not a translation question at all. It is a
**layout** decision made from one language's metrics and applied to both, and it would have shipped
silently: the English nav works, so the breakpoint looks correct. **Parity failures mostly look
like this** — not mistranslations, but decisions taken in one language and generalised without
checking.

---

## 5. Failure modes

**Translation-last.** The Arabic tree perpetually one release behind, each delay individually
reasonable. Limb 4 makes each instance a **filed defect**, which is the only control that keeps
the debt visible as debt.

**Decisions taken in one language and generalised.** §4. The commonest real failure and the least
recognised, because nothing about it looks linguistic.

**Badges mirrored.** `live` translated. Status values are estate-wide identifiers.

**Percent-encoded slugs.** §3. Breaks structural comparability and therefore auditability.

**Authoritative-language drift.** Limb 1 material amended in its English translation without the
Arabic being amended — **an amendment to a translation of a text that governs.** The most serious
failure here, because the governing text is now the stale one.

**The carve-out forgotten.** Limb 2's consumer-law yield silently dropped from consumer-facing
pages.

---

## 6. Limits

**Class: practical, and it dominates.** **No Arabic page exists.** Not a translation backlog — a
tree with nothing in it. Every claim in §3 is a specification.

**Class: economic.** The corpus is roughly forty instruments; the route census is 321 English
routes at a 1200-word floor. **Parity at that scale is ≈385,000 words of authoritative Arabic**,
and the estate has no translator, no budget and no schedule
([RAT-22](../00-governance-map/open-questions-and-ratifications.md#rat-22)).

**Class: epistemic.** Limb 1 asserts that Arabic governs material the estate has not published in
either language. The claim is currently untestable.

**Class: technical.** No mechanism detects divergence.
[SENTINEL](../standards/st-13-static-build-and-sentinel.md) would diff the trees and does not run
([DEF-001](../00-governance-map/defect-register.md#def-001)).

---

## 7. Falsifier

1. **A divergence that is not a defect** — a case where the two texts should legitimately differ,
   falsifying limb 4's absoluteness. Culturally specific examples are the candidate.
2. **Structural parity proving to force bad Arabic** — if identical paths and English slugs
   produce an unnatural Arabic estate, §3 trades auditability for readability wrongly.
3. **The mirror never shipping.** After a year of English-only publication, limb 1's authority
   claim is decorative and this instrument should be rewritten as a translation policy honestly.
   **Closest to firing.**
4. **Parity achieved and unused** — if the Arabic tree ships and no reader uses it, §1's access
   argument is wrong. The estate would rather learn this from traffic than from assumption.

---

## 8. Obligation

**For the estate:** decide [RAT-22](../00-governance-map/open-questions-and-ratifications.md#rat-22)
— mirror with the English, or trail it. The estate's own recommendation is **pillar-by-pillar
lockstep**, so that `/license/` and `/about/` exist in both languages before `/toptech/` exists in
either: parity where the estate claims its authority is, consistent with wave 1 publishing
governance before curriculum.

**And run [V-08](../00-governance-map/verification-log.md)** — nine RTL labels, one measurement,
minutes.

**For any author:** state `prevailing_text` on the instrument. Never mirror a badge. Never take a
layout decision from one language's metrics without checking the other (§4).

**For a reader:** a divergence between an Arabic and an English page is a **defect**, not a
translation artefact, and filing it at `/library/record/corrections-log/` is a correction the
estate cannot decline.

**Under ML-2.3:** §H.22 (language parity), §H.07 (access foreclosure), §H.23 (channel parity),
§H.02 (epistemic dependency), §E.7 (registry continuity — mirrors in both languages).

---

**Related:** [ST-11 Arabic Authoring](../standards/st-11-arabic-authoring.md) ·
[SITE-01 Route Manifest §1.6](../site/route-manifest.md) ·
[DS-07 Navigation Geometry §7](../design/ds-07-navigation-geometry.md) ·
[MX-012 Licensing and Reuse](mx-012-licensing-and-reuse.md) ·
[Verification Log V-08](../00-governance-map/verification-log.md) ·
[RAT-22](../00-governance-map/open-questions-and-ratifications.md#rat-22)

*Curated by Maher. Four limbs, three kinds of parity, and zero Arabic pages — which makes this the
estate's largest unpaid commitment and the one its own subject matter makes hardest to defer.*
