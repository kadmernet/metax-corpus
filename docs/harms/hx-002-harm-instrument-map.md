---
doc_id: "HX-002"
title_en: "Harm → Instrument Map, Including the Harms MetaX Itself Fails"
title_ar: "خريطة الأضرار إلى الأدوات، بما فيها أضرار ميتا-إكس نفسها"
family: "harms"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 5
depth: 5
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["harms", "governance", "self-assessment", "traceability"]
route: "/license/harms/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# HX-002 · Harm → Instrument Map

**What this instrument is.** For each of the twenty-five harms in [HX-000](.), the instrument in
this corpus that answers it — and, in the third column, **whether MetaX itself currently commits
it.**

**Why the third column exists.** A register of harms mapped to a corpus of instruments produces a
document that reads as a defence: every harm has an answer, therefore the estate is answered. That
would be [HX‑15](.) performed by the very document meant to make HX‑15 checkable. The third column
is the correction, and it is the only part of this file that carries information a critic could
not have inferred.

**Status caveat, stated first.** HX-000 exists at **eleven of twenty-five harms**
([DEF-021](../00-governance-map/defect-register.md#def-021)). Rows for HX‑12…HX‑25 map against the
harm titles and stratum definitions supplied in ML‑2.3 Part H, not against published register
text. Those rows are marked **`register text pending`** and are provisional.

---

## 1. How to read the map

| Column | Meaning |
|---|---|
| **Harm** | The register entry, by identifier |
| **Answering instrument** | The document in this corpus that creates a duty, a check or a refusal against it |
| **MetaX's own state** | `refused` · `answered` · `partial` · **`FAILS`** · `unexamined` |

**The five states, defined so they can be wrong.**

`refused` — the estate has structurally excluded the mechanism, not merely declined to use it.
`answered` — an instrument exists **and** operates.
`partial` — an instrument exists and is incompletely implemented, or the mechanism is present and
mitigated.
**`FAILS`** — the estate currently commits the harm. Named, with the evidence.
`unexamined` — no honest assessment has been made. **This is a worse state than `FAILS`**, because
a named failure is at least on the record.

---

## 2. Stratum I — Cognitive (HX‑01 … HX‑03)

| Harm | Answering instrument | MetaX's own state |
|---|---|---|
| **HX‑01** Attention expropriation | [DS-02 Motion and Attention](../design/ds-02-motion-and-attention.md) · [MX-009 Advertising](../corpus/mx-009-advertising-and-commercial.md) · [SITE-02 §4](../site/page-contract.md) two-action exit pair · no streaks or leaderboards on `me.` | **FAILS** |
| **HX‑02** Epistemic dependency | [ST-04 Falsifiability](../standards/st-04-falsifiability-and-claim-cards.md) · [ST-07 Evidence and VERIFY](../standards/st-07-evidence-and-verify.md) · [ST-24 §2.1](../standards/st-24-page-prose-standard.md) falsifier requirement | **partial** |
| **HX‑03** Engineered compulsion | DS-02 · [MX-023 Attention and Human Sovereignty](../corpus/) *(unwritten)* · five-tier motion with T‑3 unused | **partial** |

**HX‑01 — FAILS, and this is the estate's central failure.** Google AdSense
(`ca-pub-4463113802541266`, three slots) and an Adsterra slot run on the content plane
([DEF-019](../00-governance-map/defect-register.md#def-019)). Behavioural ad networks are the exact
mechanism the harm names. The estate's answering instruments are real and are outweighed by a
script tag.

To the live code's credit: `.ad-slot` collapses unfilled slots via `[data-ad-status="unfilled"]`
and shows the "Advertisement" label only when an ad is present. That is a genuine mitigation and
it does not change the disposition — under [HX-001 §2.1](hx-001-harm-audit-rubric.md), disclosure
alone scores D=1.

**HX‑02 — partial, for a reason worth naming.** The estate publishes falsifiers on every
substantive claim, which is more than most corpora do. But the build that would *enforce* the
falsifier and evidence-class requirements does not run
([DEF-001](../00-governance-map/defect-register.md#def-001)), so compliance rests on the diligence
of whoever is writing. An unenforced standard is a habit, not a mechanism.

**HX‑03 — partial.** The motion system declares five tiers and leaves T‑3 (signal) deliberately
unused, which is a real refusal. Against it: **nine infinite ambient animations with no
`prefers-reduced-motion` escape** ([DEF-016](../00-governance-map/defect-register.md#def-016),
[B-16](../00-governance-map/launch-blockers.md)). Animation that continues over an expressed user
preference is compulsion at small scale.

---

## 3. Stratum II — Relational and political (HX‑04 … HX‑06)

| Harm | Answering instrument | MetaX's own state |
|---|---|---|
| **HX‑04** The human as product | MX-009 · [ST-19 Two-Plane](../standards/st-19-two-plane-architecture.md) · [ST-23 §2](../standards/st-23-affiliate-and-referral.md) four elements | **FAILS** |
| **HX‑05** Asymmetry of the record | [MX-016 Appeals](../corpus/mx-016-appeals-and-due-process.md) · [Corrections Log](../00-governance-map/corrections-log.md) · rejected submissions published with reasons | **answered** |
| **HX‑06** Erosion of the deliberative commons | [ST-06 Objections](../standards/st-06-objections-standard.md) · `/license/falsification/objections/` · [MX-008 Moderation](../corpus/mx-008-moderation-and-enforcement.md) | **partial** |

**HX‑04 — FAILS, for the same reason as HX‑01.** Ad delivery makes the reader the transacted
party. Note the design work that *would* answer this if the slots went: the two-plane architecture
keeps the content plane free of per-user state; the affiliate standard refuses cookie attribution
and accepts worse attribution accuracy as the price
([ST-23 §3.1](../standards/st-23-affiliate-and-referral.md)). The estate built the answer and then
ran the harm anyway.

**HX‑05 — `answered`, and it is the one row the estate can defend without qualification.** The
Curator **cannot** decline a valid correction, delete a published defect, or remove a superseded
claim ([MX-000 §0.5.2](../corpus/mx-000-charter.md#2-the-correction-obligation)). Rejected
correction submissions are published *with reasons*. Sixteen corrections are on the record,
including a misspelling of the estate's own subject that no automated check could have caught. The
mechanism is not merely stated; it has been used against its author.

**HX‑06 — partial.** Objections standard exists, objections route exists, and **no external
objection has ever been filed** — because nothing is published. An untested commons mechanism.

---

## 4. Stratum III — Economic and structural (HX‑07, 08, 09, 13)

| Harm | Answering instrument | MetaX's own state |
|---|---|---|
| **HX‑07** Access foreclosure | `/about/access/free/` · [MX-021 Payments](../corpus/mx-021-payments-and-commerce.md) · [DEF-014](../00-governance-map/defect-register.md#def-014) single rail | **partial** |
| **HX‑08** Intermediation rent | [ML-2.3 §C.9](../license/ml-2-3.md) four elements · **ST-23 element 2** (paid once, never recurring) · six forbidden schema columns | **answered** |
| **HX‑09** Labour displacement without transfer | [MX-007 AI Use and Disclosure](../corpus/mx-007-ai-use-and-disclosure.md) · §H.29 substitution disclosure | **partial** |
| **HX‑13** Concentration of capability | [ML-2.3 §E.8](../license/ml-2-3.md) anti-capture · §E.7 registry redundancy · [MX-015 Succession](../corpus/mx-015-succession-and-continuity.md) | **partial** — `register text pending` |

**HX‑08 — `answered`, and the mechanism is unusual enough to state.** The prohibitions are
enforced **in the database schema**: `mx_commerce` has no `parent_referrer_id`, no
`recurring_period`, no `tier`, no `negotiated_rate`, no `clawback_until`, no `attribution_cookie`.
A future developer implementing a "small" tiered bonus must first alter the schema — a visible,
reviewable, changelog-generating act. The estate's general method is to make a prohibited thing
**unrepresentable** rather than merely disallowed, and this is its clearest instance.

**HX‑07 — partial, and the tension is real.** The estate publishes its entire governance corpus
free and gates curriculum behind payment on a **single crypto rail** (Binance Pay), which
[RAT-13](../00-governance-map/open-questions-and-ratifications.md#rat-13) records *"will exclude a
meaningful share of the audience this curriculum is written for, particularly in the
Arabic-speaking markets where Meta-X is authoritative."* An estate committing to Arabic as an
*authoritative* language while its commerce rail is disproportionately unavailable in
Arabic-speaking markets has made that commitment partly decorative.

**HX‑09 — partial, and this document is itself the evidence.** MX-007 requires AI-use disclosure
and the estate's instruments carry `authorship_note` fields where authorship is mixed. Against
it: a large fraction of this corpus is agent-drafted, and
[RAT-21](../00-governance-map/open-questions-and-ratifications.md#rat-21) asks openly whether
770,000 words of agent-generated prose published under an estate's name is a claim about what that
estate has thought about. The question is filed, not answered.

---

## 5. Stratum IV — Material and temporal (HX‑10, 11, 12, 14)

| Harm | Answering instrument | MetaX's own state |
|---|---|---|
| **HX‑10** Material and infrastructural cost | [ST-21 Performance Budgets](../standards/st-21-performance-budgets.md) · the no-image regime · static estate | **partial** |
| **HX‑11** Fragility and dependency | [ST-13 Static Build](../standards/st-13-static-build-and-sentinel.md) · [SITE-03](../site/routing-law.md) append-only redirects · four-tier persistence | **partial** — `register text pending` |
| **HX‑12** Harm to the record | **[SITE-03 §6](../site/routing-law.md)** append-only redirect record · [MX-013 Records and Versioning](../corpus/mx-013-records-and-versioning.md) · [Archive Register](../00-governance-map/archive-register.md) · MX-000 §0.8 | **partial** — `register text pending` |
| **HX‑14** Temporal foreclosure | [ST-05 Decay and Review Intervals](../standards/st-05-decay-and-review-intervals.md) · `.mx-pagestamp` on every page · kill criteria per series | **partial** — `register text pending` |

**HX‑10 — partial, and the omission is specific.** Static files, no images, small payloads,
performance budgets: a genuinely low-footprint estate. But **third-party ad scripts are not
accounted for in any budget**, and they are the heaviest thing the content plane loads. A
performance budget that excludes the network calls it does not control is a budget measuring the
wrong system.

**HX‑12 — partial, and the answering instruments are the estate's best work.** Addresses are
permanent; the redirect record is **append-only** with deletion forbidden outright; superseded text
is retained with a non-governing banner; the corrections log cannot be pruned by its author. Set
against that: **zero Arabic pages** ([DEF-002](../00-governance-map/defect-register.md#def-002)),
no §E.7 mirrors ([B-02](../00-governance-map/launch-blockers.md)) — so the record's only custodian
is its own subject — and 321 specified routes of which none exists.

**HX‑14 — partial.** Every page carries an evidence class and a review date; every series must
publish a kill criterion. And [DEF-024](../00-governance-map/defect-register.md#def-024) records
that nine live-code claims were published **without provenance of purpose**, which is a temporal
defect of exactly this kind: true statements a reader cannot date to a system state.

---

## 6. Stratum V — Reflexive (HX‑15 … HX‑19)

**All five rows are `register text pending`, and this stratum is where the estate is most exposed
— because these harms are about the act of governing, which is the only thing the estate currently
does.**

| Harm | Answering instrument | MetaX's own state |
|---|---|---|
| **HX‑15** Compliance theatre | [ML-2.3 §H.16.3](../license/ml-2-3.md) all-clear presumption · [HX-001 §4](hx-001-harm-audit-rubric.md) no total score · §7.4 thin-page exemptions · no course route for a non-`live` series | **FAILS** |
| **HX‑16** Metric capture | HX-001 §4 refusal to sum · §H.4 optimisation disclosure · [SITE-02 §9](../site/page-contract.md) line 13 | **partial** |
| **HX‑17** The audit that certifies itself | HX-001 §3 counterproductivity test · [RB-05](../rubrics/rb-05-harm-review-gate.md) · `/metax/bcia/status/` at hub tier | **partial** |
| **HX‑18** Consent integrity | ML-2.3 §H.18 · ST-23 element 1 · `/about/legal/cookies/` | **partial** |
| **HX‑19** Authorship of record | ML-2.3 §H.19 · `authorship_note` front matter · ST-23's own provenance declaration | **answered** |

**HX‑15 — FAILS, and it is the most serious row in this document.**

The estate is a **demo** ([C-14](../00-governance-map/corrections-log.md#c-14)). It renders a
catalogue of forty-seven series, credential ladders, an academy path and a nine-program research
umbrella, and **most of that content does not exist**. No page carries the required provenance
strip; `/about/universe/demo-notice/` is specified and unbuilt
([DEF-025](../00-governance-map/defect-register.md#def-025),
[B-20](../00-governance-map/launch-blockers.md)).

That is compliance theatre at the level of the whole estate: an apparatus of governance presented
as an operating institution. **An estate that knows it is a demo and does not say so commits
HX‑15 on the exact pages a reader would consult to check whether it commits HX‑15.**

The disposition is entered as `FAILS` rather than `partial` deliberately, even though the
answering instruments in that row are substantial and several are genuinely novel — the all-clear
presumption, the refusal to sum a rubric, the rule against generating a course page for an
unwritten course. Good instruments do not offset a live failure. That is precisely the
substitution HX‑15 describes.

**HX‑19 — `answered`, and it is the row that cost something.** ML-2.3 §H.19 requires a recorded
natural author for assertions issued in the estate's name. Applied honestly, it produced three
uncomfortable admissions: HX-000's harms H1–H11 are the documentation agent's while Strata V and
VI arrived with the Curator's ML-2.3 text ([C-11](../00-governance-map/corrections-log.md#c-11));
`Method` as a ninth pillar is *"my addition, not yours"* in the nav spec's own words
([RAT-19](../00-governance-map/open-questions-and-ratifications.md#rat-19)); and ST-23 is marked
in its front matter as designed from scratch with no upstream source
([RAT-23](../00-governance-map/open-questions-and-ratifications.md#rat-23)). A duty that never
embarrasses its holder is not operating.

---

## 7. Stratum VI — Successor (HX‑20 … HX‑25)

**All six rows are `register text pending`.** These harms concern people who do not yet exist and
cannot object, which makes them the hardest to assess and the easiest to score generously.

| Harm | Answering instrument | MetaX's own state |
|---|---|---|
| **HX‑20** Inheritance of unauditable systems | Whole-corpus publication · [Machine Reading Contract](../00-governance-map/machine-reading-contract.md) · permanent paths | **partial** |
| **HX‑21** Foreclosure of the successor's options | §H.27 reversibility · §H.3(a)(vii) developmental substitution *(disjunctive)* | **unexamined** |
| **HX‑22** Loss of transmissible skill | [ST-03 Limits and Bridge](../standards/st-03-limits-and-bridge.md) · [MX-014 Research Ethics](../corpus/mx-014-research-ethics-and-exclusions.md) · the six-beat arc | **partial** |
| **HX‑23** Custody without horizon | §H.28 · [MX-018 Data Retention](../corpus/mx-018-data-retention.md) · [MX-015 Succession](../corpus/mx-015-succession-and-continuity.md) | **partial** |
| **HX‑24** Irreversible commitment | §H.27 · [MX-024 Infrastructure and Migration](../corpus/) *(unwritten)* · the 80% capacity tripwire | **unexamined** |
| **HX‑25** Silence in the record | Corrections Log · Defect Register · Archive Register · append-only redirects | **partial** |

**Two rows read `unexamined`, and that is a real answer rather than a placeholder.**

**HX‑21** and **HX‑24** have not been honestly assessed against this estate. There is an
instrument named against each, and no one has asked whether *this* corpus forecloses a successor's
options or commits them irreversibly. Under [HX-001 §2](hx-001-harm-audit-rubric.md) `unexamined`
is a **worse state than `FAILS`**, because a named failure is at least on the record and can be
argued with. These two rows are the most honest thing in the document precisely because they admit
that the work was not done.

**HX‑20 — partial, with the estate's characteristic pattern.** The whole governance corpus is
published in Markdown at permanent paths, designed to be read by machines, with a reading contract
for AI systems — a genuine answer to inheriting unauditable systems. Against it: the estate's own
build pipeline does not run, its registry mirrors do not exist, and the only custodian of its
record is itself.

---

## 8. What the map shows when read as a whole

**Three `FAILS`, two `unexamined`, three `answered`, seventeen `partial`.**

Three observations, in ascending order of discomfort.

**The failures cluster.** HX‑01, HX‑04 and HX‑15 are not three independent problems. Two are the
ad slots and one is the demo status, which means **two decisions** account for every outright
failure in the register. Both are on the Curator's desk
([RAT-15](../00-governance-map/open-questions-and-ratifications.md#rat-15),
[RAT-20](../00-governance-map/open-questions-and-ratifications.md#rat-20)) and both are currently
*cheap to fix*: the ad slots can be removed before any Statement is issued, and the demo strip is
a component and a page.

**The `answered` rows are all governance, and every `FAILS` row is operational.** HX‑05
(asymmetry of the record), HX‑08 (intermediation rent) and HX‑19 (authorship) are answered because
the estate is *good at writing rules for itself and mediocre at running a website*. That is the
characteristic profile of a governance corpus, and it is exactly the profile Stratum V exists to
catch.

**Seventeen `partial` rows is not a comfortable middle.** In most cases the pattern is identical:
a well-designed instrument exists, and the mechanism that would enforce it does not run. The
falsifier standard is unenforced because the build does not run. The record is durable but
custodied by its own subject. The performance budget excludes the ad scripts. **The estate's
recurring failure is not bad rules; it is rules without mechanisms**, and a corpus that keeps
writing better rules in response is treating the symptom.

---

## 9. Falsifier

This map is wrong if any of the following is observed:

1. A harm whose answering instrument does not in fact create a duty, check or refusal against its
   mechanism — a citation that looks like an answer and is not.
2. A row marked `answered` where the instrument exists but does not operate. **`answered` requires
   both**, and this is the failure a critic should look for first, since seventeen rows were
   downgraded to `partial` on exactly this test.
3. A row marked `partial` that is honestly `FAILS`. The estate's incentive runs in this direction
   and the three named failures do not discharge it.
4. A harm in HX-000 absent from this map entirely.

---

## 10. Obligation

**For the estate:** examine HX‑21 and HX‑24, which are `unexamined` and should not remain so
through another release. Complete HX-000 so the fourteen `register text pending` rows can be
mapped against published text. Resolve the two decisions that account for all three failures.

**For a reader or critic:** this map is the fastest route to the estate's weakest points, and it
is published for that purpose. Falsifier 2 in §9 is the productive attack — check whether an
`answered` row's mechanism actually runs.

**Under ML-2.3:** §H.16 (the Statement this map feeds), §H.16.3 (why no row may be flattered),
§H.19 (why the authorship admissions are in §6), §H.7 (why good instruments do not offset a live
failure).

---

**Related:** [HX-000 The Register](.) · [HX-001 Harm Audit Rubric](hx-001-harm-audit-rubric.md) ·
[Part H Statement](../license/part-h-statement.md) ·
[RB-05 Harm Review Gate](../rubrics/rb-05-harm-review-gate.md) ·
[Defect Register](../00-governance-map/defect-register.md) ·
[Corrections Log](../00-governance-map/corrections-log.md) · [ML-2.3](../license/ml-2-3.md)

*Curated by Maher. Twenty-five harms, three of which this estate currently commits and two of
which it has not honestly examined. Two decisions account for all three failures, and both are
still cheap.*
