---
doc_id: "ST-13"
title_en: "Static Build and the SENTINEL Contract"
title_ar: "البناء الساكن وعقد الحارس"
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
domain_tags: ["standards", "build", "validation", "sentinel"]
route: "/library/standards/generation-prompt/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# ST-13 · Static Build and the SENTINEL Contract

**What this standard governs.** The build that turns this corpus into the published estate, and
**SENTINEL** — the set of checks that must pass before anything ships.

**The disclosure this standard must lead with.** SENTINEL **does not run.** It is a specification,
not a pipeline ([DEF-001](../00-governance-map/defect-register.md#def-001)), and it has been cited
as an operating mechanism by a dozen instruments across three releases. Every check below is
*specified* and *unperformed*. This standard is therefore the corpus's largest single instance of
its own recurring failure — **rules without mechanisms** — and it is the document that either fixes
that or perpetuates it.

---

## 1. Position

Nearly every commitment in this corpus terminates here. [ST-02](st-02-front-matter-schema.md)'s
eighteen required fields, [ST-05](st-05-decay-and-review-intervals.md)'s staleness arithmetic,
[ST-07](st-07-evidence-and-verify.md)'s dated numbers, [ST-01](st-01-identifier-and-url-grammar.md)'s
immortal identifiers, [SITE-02](../site/page-contract.md)'s twenty acceptance lines,
[SITE-03](../site/routing-law.md)'s root-absolute paths — each is enforced *by the build* or by
nobody.

That makes ST-13 the load-bearing standard of the estate and, currently, the emptiest. The estate
has stated the finding against itself three times in one release:

> The estate's recurring failure is not bad rules; it is **rules without mechanisms**
> ([HX-002 §8](../harms/hx-002-harm-instrument-map.md)).

**The macro register.** A governance corpus that cannot check itself is in the same position as the
systems it criticises: it audits its own coherence, which is the property it can verify cheaply,
and mistakes coherence for accuracy. The
[Corrections Log §Method](../00-governance-map/corrections-log.md#method-what-this-log-has-learned)
records the consequence precisely — thirty-seven entries of cross-source reconciliation found
**one** error; fetching the live code found **nine** in an afternoon. A build is the only mechanism
that makes the second method routine rather than occasional.

---

## 2. Definition — the five check families

SENTINEL is five families of check, each either **blocking** (build fails) or **reporting**.

| Family | Checks | Mode |
|---|---|---|
| **S1 · Structure** | Front matter, identifiers, file naming | Blocking |
| **S2 · References** | Internal links, anchors, cited paths | Blocking |
| **S3 · Computed values** | Counts, capacity figures, dates | Blocking |
| **S4 · Single-source pairs** | Summaries against their governing texts | Blocking |
| **S5 · Page acceptance** | The twenty lines of SITE-02 §9 | Blocking, per page |

### 2.1 S1 — structure

Every instrument: eighteen required fields present ([ST-02 §2](st-02-front-matter-schema.md));
every enum value permitted; `evidence_class` consistent with `review_interval_months`; `doc_id`
valid under [ST-01 §2](st-01-identifier-and-url-grammar.md); filename beginning with the
identifier; `designated` matching [the Designation List](../license/designation-list.md) exactly.

**The check this family exists for:** `designated: true` on an instrument absent from the list, or
absent on one present. That is a **legal** inconsistency — `designated` invokes Part G supremacy —
and it is invisible to reading because the two documents are never read together.

Also blocking: **conditional fields required by condition**. A document describing a live artefact
without `provenance_of_purpose` fails. Nine claims shipped without it in one release
([DEF-024](../00-governance-map/defect-register.md#def-024)), and a field check is the only remedy
that scales.

### 2.2 S2 — references

Every internal link resolves. Every anchor exists in its target. Every path cited in prose exists.

**This is the check the estate most needs and least has.** The
[Document Index §7](../00-governance-map/document-index.md) admits the estate cannot count its own
dangling references — `Grep` returns false negatives on these files reliably enough that a negative
result is untrustworthy, so the figure "**approximately seventy** unresolving paths in
`docs/index.md`" is an estimate from reading, tagged
[V-10](../00-governance-map/verification-log.md).

**A link checker produces that number in minutes.** It is the single cheapest high-value check in
this standard, and it would immediately expose the estate's most consequential dangling reference:
`docs/harms/hx-000-structural-harms.md`, incorporated by **ML-2.3 §A.10** into a Tier 1 governing
instrument, cited by six instruments written this session, and **absent**
([DEF-021](../00-governance-map/defect-register.md#def-021)).

S2 additionally enforces the **anchor immortality** rule of
[ST-01 §6](st-01-identifier-and-url-grammar.md): an anchor that existed in a previous build and is
absent from this one fails, unless an explicit `<a id>` alias preserves it.

### 2.3 S3 — computed values

**No number is typed.** Defect counts, harm counts, route counts, capacity percentages — each is
computed from its source artefact at build time, and a literal where a computed value belongs
fails the build.

The rule's justification is in [the defect register](../00-governance-map/defect-register.md): *a
typed count is a claim with no falsifier, and a typed count that undercounts defects is the specific
failure this register exists to prevent.*

**A necessary admission.** This standard's own prose carries typed counts — "thirty-three defects,"
"321 routes," "sixteen corrections." Under S3 those are defects, and they exist because the
mechanism that would compute them does not. They are the honest state of a corpus specifying a
check it cannot yet run, and they should be replaced with `data-count-src` bindings the day S3
operates.

S3 also computes **staleness** — `last_reviewed + review_interval_months` against build date — and
renders it into the `.mx-pagestamp`. That arithmetic is
[ST-05](st-05-decay-and-review-intervals.md)'s central operative requirement and it is currently
performed by nobody.

### 2.4 S4 — single-source pairs

Where one instrument summarises another, the summary must not assert an obligation absent from the
source. The pairs are enumerated in
[GM-01 §3](../00-governance-map/precedence-and-conflict-rules.md) and now include the advertising
disposition (MX-023 §3.6 against HX-002) and the forbidden schema columns (ST-22 §4.2 against
ML-2.3 §C.9 and ST-23 §3.3).

**Why mechanical checking rather than care.** Exact textual mirroring between two instruments is a
known drafting failure: two copies of a normative sentence **drift at the first amendment**, and the
drift is invisible until somebody exploits it. Summaries never govern
([GM-01 §3](../00-governance-map/precedence-and-conflict-rules.md)) — S4 is what stops one becoming
a second source of truth by accident.

### 2.5 S5 — page acceptance

The twenty lines of [SITE-02 §9](../site/page-contract.md), per page. Word floor or declared
`mx-thin`; eight recipe sections; `.mx-related` with four groups and ≥8 resolving links, one
cross-pillar; the pagestamp; exactly two exit actions; the demo strip; root-absolute paths;
canonical and both `hreflang`; script order; nine `.mm-top` items with the correct `.active`; badge
text labels; no undated number; `.img-slot` shimmer; legible with CSS off; **renders with
JavaScript off**; contrast ≥4.5:1; touch targets ≥44px; reduced-motion suppression; **MacroLifeTech
spelt correctly**.

**Three of the twenty are currently failed by the estate's own demo** — no-JS rendering
([DEF-018](../00-governance-map/defect-register.md#def-018)), the reduced-motion block
([B-16](../00-governance-map/launch-blockers.md)) and the 44px touch targets
([DEF-022](../00-governance-map/defect-register.md#def-022)). The contract is stricter than the
artefact it derives from, which is the correct direction for a contract to point.

---

## 3. Mechanism — the build order

```
1  Parse front matter of every instrument        → S1
2  Build the reference graph                     → S2
3  Compute every derived value                   → S3
4  Diff summaries against governing texts        → S4
5  Generate routes from SITE-01                  →
6  Render pages, inject computed values          →
7  Check every page                              → S5
8  Emit sitemap.xml, MENU, search-index, _redirects
9  Fail loudly, or publish
```

**Step 8 is generation, never authorship.** Four artefacts are derived and **must not be
hand-written**: `sitemap.xml`, the `MENU` array, `/data/search-index.json`, and `_redirects`
([SITE-01 §9](../site/route-manifest.md)). A derived artefact editable independently of its source
**will** diverge from it, and the divergence is discovered by a reader rather than by the estate —
which is the class of failure that produced nine of sixteen corrections.

**Step 9 has no soft mode.** A blocking check fails the build; it does not warn. A warning is a
check that will be ignored under deadline, and the estate has enough evidence about deferred cheap
work — [DEF-030](../00-governance-map/defect-register.md#def-030) records four verifications
costing minutes each, deferred at the moment they were cheapest.

### 3.1 What the build must never do

**Never repair.** SENTINEL fails; it does not fix. An auto-corrected front-matter field is a silent
edit, forbidden by [MX-000 §0.8](../corpus/mx-000-charter.md), and it would let an author's error
disappear without a record.

**Never emit an unwritten page.** A route in SITE-01 with no content is **not published** as a stub.
Emitting a 1,200-word page for an unwritten course *"is HX‑15 in miniature"*
([SITE-01 §6.2](../site/route-manifest.md)); emitting an empty one is the same harm with less
effort.

**Never lower a floor to pass.** If a page cannot meet the word floor honestly, it declares
`mx-thin` and files under
[DEF‑2026‑043](../00-governance-map/defect-register.md#def-2026-043) with a stated reason. A build
that quietly relaxes a threshold has changed the standard without a changelog line.

---

## 4. Worked instance — what S2 would find today, if it ran

Run against the corpus at v2026.10.1, the reference check would report at minimum:

**`docs/harms/hx-000-structural-harms.md` — absent, cited by ML-2.3 §A.10, `docs/index.md`, the
README and six instruments.** Blocking. The build would not publish, which is the correct outcome:
a Tier 1 instrument incorporating an absent register should not ship.

**Approximately seventy unresolving paths in `docs/index.md` §§4–11** — MX-002…MX-020,
AG-000…AG-012, ST-03/06/08–12/14–18, RB-01…RB-04, REG-01…REG-08, BX-000…BX-009, the lexicon set.

**Cross-citations from instruments written this session** — ST-22 → ST-19, ST-13; MX-023 → MX-009,
MX-007; SITE-01 → ST-01; RB-05 → RB-03. Each is *architecturally* correct — that is where the duty
will live — and each is a dangling link today
([Document Index §6](../00-governance-map/document-index.md)).

**Every obligation block in the harms draft** — all link `../license/ml-2-2.md`, a licence version
that does not exist ([version history §3](../license/version-history.md)).

**What the instance demonstrates.** The build would fail on its first run, and the failure list
would be long, accurate, and generated in seconds. The estate has spent three releases producing
that list by hand, incompletely, and recording its incompleteness as
[V-10](../00-governance-map/verification-log.md). **That is the entire argument for building
SENTINEL**, stated as a measured comparison rather than a preference.

---

## 5. Failure modes

**The specification cited as a mechanism.** This standard's defining failure, in its third release.
A dozen instruments say "checked by SENTINEL"; nothing is checked. Signature: a corpus confident
about properties nobody has measured.

**Warnings instead of failures.** A blocking check softened to keep a deadline. It never hardens
again.

**Auto-repair.** The build fixing what it should report. §3.1.

**Hand-edited derived artefacts.** A `_redirects` line added directly, a `MENU` entry typed. Works
immediately, diverges permanently.

**Green build, wrong output.** S1–S5 all pass and pages render incorrectly, because none of the five
families checks *appearance*. This is why the estate's operating guidance requires visual
verification — a clean console does **not** prove correct rendering, and a markup-level bug such as
script source leaking as visible text produces zero errors.

**The build that becomes the standard.** The most insidious: checks are relaxed until the corpus
passes, and the standard silently becomes whatever the build tolerates. The control is that every
relaxation requires a changelog line and a
[RB-05](../rubrics/rb-05-harm-review-gate.md)-style record.

---

## 6. Limits

**Class: technical.** SENTINEL does not exist. This document specifies five check families,
twenty-five-plus individual checks and a nine-step order, and **not one line of it runs.** Every
"blocking" above is aspirational.

**Class: epistemic.** No check here detects a well-formed page that is **wrong**. S1–S5 verify
structure, references, arithmetic and consistency — the properties a machine can check — which is
exactly the *"audits its own coherence"* failure §1 quotes against the estate. A build makes the
corpus internally consistent faster; it does not make it accurate.

**Class: economic.** Unbudgeted. Steps 1–4 and 8 are a few hundred lines of scripting; S5 requires
headless rendering across 642 routes ×2 languages, which is a real cost against a capacity ceiling
([ST-22 §5](st-22-platform-and-persistence.md)).

**Class: governance.** The build cannot decide the two questions blocking the estate — the ad slots
([RAT-15](../00-governance-map/open-questions-and-ratifications.md#rat-15)) and the demo exit
([RAT-20](../00-governance-map/open-questions-and-ratifications.md#rat-20)). It can only refuse to
publish while B-20 is open.

---

## 7. Falsifier

This standard is wrong if:

1. **SENTINEL is built, passes clean, and the corpus still contains the class of error it was built
   to catch** — showing the five families under-inclusive.
2. **A blocking check proves so frequently wrong that it must be softened**, showing it a
   preference misfiled as a rule. S5's word floor is the candidate:
   [DEF‑2026‑043](../00-governance-map/defect-register.md#def-2026-043) already exempts six page
   classes, and a seventh, eighth and ninth would falsify the floor rather than justify another
   exemption.
3. **The build's cost exceeds its value** — if S5 across 1,284 routes consumes more capacity than
   the estate can spare, the check is right and unaffordable, which is a different problem than
   being wrong.
4. **The corpus proves to have been substantially conformant all along** when first measured. That
   would falsify this standard's implicit premise that unenforced rules decay — and it is the one
   result the estate would be glad to be wrong about.

---

## 8. Obligation

**For the estate, in this order** — chosen by value per hour, not by completeness:

1. **S2's link checker.** Minutes of work. Closes [V-10](../00-governance-map/verification-log.md),
   replaces the corpus's most embarrassing estimate with a count, and finds every dangling
   reference including the Tier 1 one.
2. **S1's front-matter validator.** Closes [DEF-008](../00-governance-map/defect-register.md#def-008)
   and prevents the copy-paste inheritance [ST-02 §5](st-02-front-matter-schema.md) names.
3. **S3's staleness arithmetic.** Makes [ST-05](st-05-decay-and-review-intervals.md) operative
   rather than declarative.
4. Then S4, then S5.

**For any author:** do not write "checked by SENTINEL" in any instrument until it is. Three
releases of that sentence are what produced DEF-001's persistence.

**For any reviewer:** a clean build does not license skipping visual verification. §5's
green-build-wrong-output failure is real and produces no console error.

**Under ML-2.3:** §H.17 (non-theatre — a specified-but-unrun check is the paradigm case), §H.15
(compliance theatre), §H.19 (authorship of record), §H.26 (corpus hygiene), §H.20 (inheritance of
unauditable systems — a successor inheriting an unchecked corpus inherits one whose properties
nobody has measured).

---

**Related:** [ST-02 Front-Matter Schema](st-02-front-matter-schema.md) ·
[ST-01 Identifier and URL Grammar](st-01-identifier-and-url-grammar.md) ·
[ST-05 Decay and Review Intervals](st-05-decay-and-review-intervals.md) ·
[ST-07 Evidence and VERIFY](st-07-evidence-and-verify.md) ·
[SITE-02 Page Contract](../site/page-contract.md) ·
[SITE-01 Route Manifest §9](../site/route-manifest.md) ·
[Defect Register DEF-001](../00-governance-map/defect-register.md#def-001)

*Curated by Maher. Five check families, nine build steps, zero of them running — which makes this
the corpus's largest instance of the failure it keeps diagnosing in itself.*
