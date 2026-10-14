---
doc_id: "MX-009"
title_en: "Advertising and Commercial Policy"
title_ar: "سياسة الإعلانات والأنشطة التجارية"
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
domain_tags: ["corpus", "advertising", "commerce", "disclosure"]
route: "/about/legal/advertising/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# MX-009 · Advertising and Commercial Policy

**What this instrument governs.** Whether and how the estate may take money from anyone other than
the reader, and what it owes the reader when it does.

**The disclosure this instrument must lead with.** The estate **currently violates its own policy
here.** Google AdSense (`ca-pub-4463113802541266`, three slots) and an Adsterra slot run on the
content plane. Under [ML-2.3](../license/ml-2-3.md) that engages **HX‑01** (attention
expropriation) and **HX‑04** (the human as product) directly, and
[HX-002](../harms/hx-002-harm-instrument-map.md) records both as **FAILS** — not `partial`.

This is the estate's most-cited self-criticism, and MX-009 is where it belongs, because a policy
whose breach is documented everywhere except in the policy has been quietly demoted.

---

## 1. Position

Every institution publishing at scale faces the same question, and most answer it by not asking it:
**who pays, and what do they buy?**

A reader-funded estate sells access. An advertiser-funded estate sells attention. A sponsor-funded
estate sells association. These are not degrees of one thing — they determine what the institution
optimises for, and under [ML-2.3 §H.4](../license/ml-2-3.md) the estate must be able to state its
objective function in public.

Its route is `/about/legal/advertising/`, and
[SITE-01 §5.9](../site/route-manifest.md) requires that page to exist and *"must not be quiet"*: an
estate running ad networks while publishing a register naming attention expropriation owes its
reader a policy at a findable address, **written in the register's own vocabulary rather than in a
compliance idiom.** This is the route where HX‑01 and HX‑04 are either defended or conceded.

Its siblings are [MX-023](mx-023-attention-and-human-sovereignty.md), which states the doctrine
this policy implements, [MX-021](mx-021-payments-and-commerce.md) on reader-side commerce, and
[ST-23](../standards/st-23-affiliate-and-referral.md) on paid referral.

---

## 2. Definition — the four revenue classes

| Class | What is sold | Permitted |
|---|---|---|
| **Reader-funded** | Access to curriculum | **Yes** — the estate's intended model |
| **Contribution** | Nothing. Voluntary support | **Yes** |
| **Referral** | An introduction, disclosed at the point of influence | **Yes**, under [ST-23](../standards/st-23-affiliate-and-referral.md)'s four cumulative elements |
| **Advertising** | Reader attention, or reader data | **See §3** — and the estate's practice contradicts its policy |

### 2.1 Prohibited outright, at any scale

Five things, none subject to a scale gate or a disclosure exception.

**Selling or sharing reader data.** No transfer of reader records to any third party for
consideration, ever. No data broker, no audience segment, no hashed-email match.

**Behavioural profiling on the content plane.** Building a per-reader interest profile for
commercial purposes. This is the prohibition the estate currently breaches: an ad network's script
on a content page performs exactly this, on readers who never signed in.

**Advertising inside assessed material.** No advertisement on a course page, lesson, assessment or
credential record, nor anywhere under `/license/` or `/metax/bcia/status/`. A reader being examined
is not an audience.

**Paid placement in the curriculum or the registries.** No series, tool, vendor or academy may
purchase position, prominence or inclusion. The catalogue and registries are the estate's factual
claims about itself, and a purchasable fact is not one.

**Sponsored content presented as editorial.** Commercially originated content is labelled at its
head, in body type, or it does not publish.

---

## 3. Mechanism — the six conditions

If advertising exists at all, six conditions bind **cumulatively** — failing any one makes the
arrangement non-compliant, on the [§C.9](../license/ml-2-3.md) four-element model the estate uses
for all money questions.

**1. Contextual only.** Served on the page's subject, never the reader's history. No cookie, no
device identifier, no cross-site signal.

**2. Off the assessed and governance surfaces.** §2.1's third prohibition.

**3. Labelled before it is seen.** The label appears when an ad is present and is absent when the
slot is unfilled. The live build gets this right: `.ad-slot` collapses unfilled slots via
`[data-ad-status="unfilled"]` and reveals "Advertisement" only when filled. **A genuine mitigation
— and under [HX-001 §2.1](../harms/hx-001-harm-audit-rubric.md) disclosure alone scores D=1**, a
floor, never a remedy.

**4. Budgeted.** Ad payload counts against
[ST-21](../standards/st-21-performance-budgets.md)'s performance budget. **The estate fails this**:
third-party ad scripts are the heaviest thing the content plane loads and appear in no budget
([HX-002 §5](../harms/hx-002-harm-instrument-map.md)). A budget excluding the calls it does not
control measures the wrong system.

**5. Disclosed in the Part H Statement.** Every network named, with its HX‑01 and HX‑04 disposition
([ML-S1](../license/part-h-statement.md)).

**6. Severable within thirty days.** No arrangement may create a dependency the estate cannot exit
in a month — [§H.27](../license/ml-2-3.md)'s reversibility duty applied to revenue. **An estate
that cannot afford to stop is an estate whose policy is written by its advertisers.**

---

## 4. Worked instance — the estate's own arrangement, assessed

| Condition | State |
|---|---|
| 1. Contextual only | **FAILS.** AdSense and Adsterra are behavioural by default |
| 2. Off assessed surfaces | Partially met — no assessment exists yet to breach |
| 3. Labelled | **Met.** The unfilled-slot collapse works |
| 4. Budgeted | **FAILS.** Ad payload appears in no budget |
| 5. Disclosed in a Statement | **FAILS.** No Statement is issued |
| 6. Severable in thirty days | Met — no contractual lock-in |

**Three of six failed. Under §3's cumulative rule the arrangement is non-compliant with this
instrument.**

**What the demo status changes, and what it does not.** The live site is a **demo**
([C-14](../00-governance-map/corrections-log.md#c-14)), which does not make the arrangement
acceptable — it makes it **removable before consequence attaches.** MX‑NAV‑SPEC §10 states the
window plainly: there is *"a clean window to remove the ad slots before the statement is ever
published,"* and if they stay, *"the honest text stays too, and it will sit two clicks from the
licence you are asking people to adopt."*

**Two honest paths, and a third named as dishonest.**

| Path | Consequence |
|---|---|
| Remove the networks | HX‑01 and HX‑04 become genuinely remediable; revenue falls to zero |
| Publish them as **unremedied**, with reasons and review dates | The instrument keeps its integrity; the estate publishes its own failure |
| Publish an all-clear Statement | **MetaX becomes the first specimen of HX‑15**, the harm its own licence introduced |

This is [RAT-15](../00-governance-map/open-questions-and-ratifications.md#rat-15) and
[B-19](../00-governance-map/launch-blockers.md). **No editor may decide it.** What this instrument
*can* decide, and does: if the slots survive, conditions 1, 4 and 5 must be brought into compliance
regardless — contextual serving, budgeted payload, disclosed disposition. Those are failures of
**policy administration**, not of principle, and none awaits the Curator's revenue decision.

---

## 5. Failure modes

**The gradual exception.** One slot on a low-traffic page, then two, then the pattern is
established and the policy reads as aspirational. The estate is a live case study: the networks
were added without a policy amendment and the policy was left standing.

**"Contextual" claimed for a behavioural network.** A vendor's self-description is not evidence.
Condition 1 is satisfied by the **absence of cross-site identifiers**, verifiable in the browser.

**The label that recedes.** 0.6rem grey-on-grey, or below the fold. Each step defensible on layout
grounds; the aggregate is an unlabelled ad.

**Revenue dependency by increments.** Condition 6 exists because dependency arrives without a
decision: costs rise to meet income, and then the policy cannot be enforced without cutting
something the estate now needs.

**Disclosure treated as remedy.** The failure this instrument most needs to resist. The labelling
is real and it is D=1. An estate citing its labelling as an answer to HX‑01 has mistaken a floor
for a fix.

---

## 6. Limits

**Class: economic, and binding.** This policy is plausibly incompatible with funding the estate.
Reader-funded access via a single crypto rail already excludes part of the target audience
([DEF-014](../00-governance-map/defect-register.md#def-014),
[RAT-13](../00-governance-map/open-questions-and-ratifications.md#rat-13)), and contextual-only
advertising earns a fraction of behavioural. The estate does not claim to have solved this. It
claims only that the trade must be **stated** rather than resolved by drift.

**Class: governance.** The revenue decision is the Curator's. This instrument specifies conditions
and cannot choose between §4's paths.

**Class: epistemic.** The claim that behavioural advertising harms readers rests on the
[harms register](../harms/) and the autonomy argument at
[MX-023 §6](mx-023-attention-and-human-sovereignty.md), which is **E1** — the estate's own
position, marked as such under [ST-07 §2.1](../standards/st-07-evidence-and-verify.md).

**Class: technical.** No mechanism enforces any condition. Ad-payload budgeting requires
[SENTINEL](../standards/st-13-static-build-and-sentinel.md), which does not run
([DEF-001](../00-governance-map/defect-register.md#def-001)).

---

## 7. Falsifier

1. **Contextual-only advertising proves to fund the estate adequately** — falsifying §6's economic
   limit rather than the policy, and removing the tension §4 documents. Testable, untested.
2. **Readers, told plainly what behavioural advertising does, prefer it to paying.** That is
   [MX-023 §7](mx-023-attention-and-human-sovereignty.md) falsifier 3 applied to revenue; if robust
   under full disclosure, §2.1's second prohibition narrows.
3. **The six conditions prove satisfiable by an arrangement that plainly expropriates attention**,
   showing §3 under-inclusive.
4. **The estate's non-compliance persists through publication** — falsifying not the policy but
   the estate's claim to operate one. **The closest to firing.**

---

## 8. Obligation

**For the estate, in order.** Decide
[RAT-15](../00-governance-map/open-questions-and-ratifications.md#rat-15) **before publication,
while removal is still free.** If the slots stay: bring conditions 1, 4 and 5 into compliance —
they do not await the revenue decision — and publish HX‑01 and HX‑04 as **unremedied** with reasons
and review dates in [the Part H Statement](../license/part-h-statement.md). Either way, write
`/about/legal/advertising/` in the register's vocabulary, not a compliance idiom.

**For an academy chartered under [MX-004](mx-004-terms-of-top-levels.md):** §2.1's five
prohibitions are inherited and not waivable on a subdomain. Requirement 11 obliges the academy's
own Part H Statement to record its Stratum I dispositions.

**For a reader:** an advertisement on an assessed page, inside `/license/`, or under
`/metax/bcia/status/` is a breach of this instrument and a valid correction. File at
`/library/record/corrections-log/` — rejected submissions are published with reasons.

**Under ML-2.3:** HX‑01, HX‑04, §H.4 (optimisation disclosure), §H.15 (compliance theatre), §H.16
(the Statement), §H.18 (consent integrity), §H.21 (proportionate imposition — the reader who never
signed in bears the profiling), §H.27 (reversibility — condition 6).

---

**Related:** [MX-023 Attention and Human Sovereignty](mx-023-attention-and-human-sovereignty.md) ·
[MX-021 Payments and Commerce](mx-021-payments-and-commerce.md) ·
[ST-23 Affiliate and Referral](../standards/st-23-affiliate-and-referral.md) ·
[ST-19 Two-Plane Architecture](../standards/st-19-two-plane-architecture.md) ·
[HX-002 Harm → Instrument Map](../harms/hx-002-harm-instrument-map.md) ·
[Part H Statement](../license/part-h-statement.md) ·
[Defect Register DEF-019](../00-governance-map/defect-register.md#def-019)

*Curated by Maher. Four revenue classes, five outright prohibitions, six cumulative conditions —
three of which the estate currently fails on its own demo, stated here rather than only in the
defect register.*
