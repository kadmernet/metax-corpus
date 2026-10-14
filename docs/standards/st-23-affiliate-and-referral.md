---
doc_id: "ST-23"
title_en: "Affiliate and Referral Standard"
title_ar: "معيار الإحالة والتسويق بالعمولة"
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
domain_tags: ["standards", "commerce", "riba", "disclosure", "affiliate"]
provenance_of_purpose: "specification"
authorship_note: "Designed from scratch. No supplied source contains an affiliate system."
hreflang: "en, ar"
---

# ST-23 · Affiliate and Referral Standard

**Provenance, stated first.** The Curator instructed that the platform architecture document
*"may adjust previous documents and add affiliate system if missed."* It was missed — and more
than missed: **no source document supplied to this estate contains an affiliate system in any
form.** Nineteen sources were read in full; none mentions referral, commission, affiliate or
revenue share. This standard is therefore **designed from scratch** by the documentation agent,
and it is marked as such in the front matter under ML‑2.3 §H.19 (authorship of record). It is the
only instrument in this corpus with no upstream source, and it should be read with the additional
scepticism that warrants.

**What it governs.** Whether, how and on what conditions the estate may pay a person for
introducing another person to it.

---

## 1. Position

Affiliate marketing sits at the intersection of three things this estate has already committed
itself on, and the intersection is where the difficulty lives.

[MX-021 Payments and Commerce](../corpus/mx-021-payments-and-commerce.md) fixes the commerce
plane: Binance Pay, no interest, no late fees, no financing partner, and the prohibition enforced
in the **database schema** rather than in policy prose. [MX-009](../corpus/) commits the content
plane to carrying no per-user tracking — a commitment the live demo currently breaks
([DEF-019](../00-governance-map/defect-register.md#def-019)). And
[ML‑2.3 Part H](../license/ml-2-3.md) makes twenty-five structural harms operative, of which four
bear directly: **HX‑01** (attention expropriation), **HX‑04** (the human as product), **HX‑08**
(intermediation rent) and **HX‑15** (compliance theatre).

The question this standard answers is not *how do we build an affiliate program.* That is a solved
commercial problem with well-known mechanics. It is: **can a referral system exist that does not
convert the estate's readers into a distribution channel, and if so what does it have to give
up?**

The parent hub in the published estate is `/about/access/`, alongside pricing, entitlements and
refunds. It is deliberately *not* under `/academies/`, because an academy curator recruiting
students is a different relationship from a reader recruiting readers, and conflating them is the
first mistake most programs make.

---

## 2. Definition — the four elements of a compliant referral

A payment for an introduction is a **compliant referral** under this standard if and only if all
four elements hold. They are cumulative, modelled on the four-element structure of
[ML‑2.3 §C.9](../license/ml-2-3.md) (Core Riba), because the estate should use one analytical
form for its money questions rather than inventing a new one per instrument.

**Element 1 — Disclosed at the point of influence.** The referral relationship is visible to the
*referred* person before they act, in the same view as the recommendation, in the same typeface,
without interaction. Not in a footer, not on a separate policy page, not behind a tooltip. If the
recommendation reaches the reader, the disclosure reaches them at the same moment.

**Element 2 — Paid on a completed enrolment, once.** Compensation attaches to a single event — a
person enrolling and remaining past the refund window — and is paid once. No recurring
commission, no lifetime revenue share, no second-tier payment for referrals made by the referred
person.

**Element 3 — Fixed at a published rate.** The amount is a published figure or a published
percentage of a published price, identical for every referrer. No negotiated rates, no tiered
bonuses, no leaderboards, no time-limited multipliers.

**Element 4 — Severable without penalty on either side.** The referrer may withdraw and the estate
may terminate, at any time, with no clawback of already-earned amounts and no forfeiture
conditions.

### 2.1 What would not count, and why each exclusion is the interesting one

**A recurring commission on a subscription.** Fails element 2. This is the industry default and it
is excluded deliberately: a recurring payment converts a one-time introduction into an ongoing
income stream derived from another person's continued payment, which under
[ML‑2.3 §C.9](../license/ml-2-3.md) is the structure the estate analyses as **intermediation rent**
— return accruing to a position rather than to work performed. The referrer did work once. Paying
them once is proportionate; paying them for thirty-six months is a rent.

**A two-tier structure.** Fails element 2. Paying A for B's referrals makes A's income depend on
recruiting recruiters, which is the mechanism by which a referral program becomes a recruitment
pyramid. The estate does not need a definition of "pyramid scheme" to exclude it; element 2 does
the work structurally.

**A performance leaderboard.** Fails element 3, and independently engages **HX‑01**. A
leaderboard converts referral into a competitive game with variable rewards, which is precisely
the engagement mechanic the estate refused on `me.metax.academy` when it excluded streaks and
leaderboards from the dashboard. An estate cannot refuse that mechanic for learners and adopt it
for referrers.

**A tiered bonus at volume.** Fails element 3. Volume tiers reward *scale of distribution*, which
means the program's best-compensated participants are those treating the estate as an audience to
be monetised rather than a thing to be recommended. The rate must not reward reach.

**A cookie-based attribution window.** Fails element 1 and independently breaches MX-009. A
30-day cookie tracks a reader across the content plane in order to attribute a commission, which
is per-user tracking on the content plane for a commercial purpose — the exact thing the estate
committed against. §3.2 specifies the alternative.

**An affiliate link that does not announce itself.** Fails element 1. This is the most common
practice in the industry and the estate treats it as the central harm rather than a technicality:
a recommendation whose financial interest is undisclosed is a recommendation the reader cannot
weight.

---

## 3. Mechanism

### 3.1 The referral code, not the tracking link

A referrer receives a **code**, not a URL parameter: `MX-REF-{6 chars}`, derived
deterministically from their `usr_{ULID}` and a fixed salt, published on their own page at
`me.metax.academy`.

The referred person enters the code **at checkout**, on the commerce plane, of their own volition.
No link carries it. No cookie stores it. No script on the content plane observes it.

This single design choice is what makes the standard compatible with MX-009, and it is worth being
explicit about the trade, because it is a real cost and not a clever trick.

| Property | Cookie attribution | Code at checkout |
|---|---|---|
| Content-plane tracking | Required | **None** |
| Attribution accuracy | High | **Lower — some referrals go unpaid** |
| Referrer effort | None | Must communicate a code |
| Referred person's agency | Passive, usually unaware | **Active and informed** |
| Auditable by the referred person | No | **Yes — they typed it** |

**The estate accepts lower attribution accuracy as the price of not tracking readers.** Some
genuine referrals will go uncompensated because the referred person forgot the code. That is a
real loss to real referrers and it must be disclosed to them before they join, not discovered
afterwards. The alternative — accurate attribution via surveillance — is a cost borne by every
reader of the content plane, including the overwhelming majority who never enrol. Concentrating a
small cost on the participants who chose to participate is more defensible than diffusing a
larger cost across everyone who reads a page.

### 3.2 The disclosure component

Any page, post or message carrying a referral code must render the disclosure inline:

```html
<p class="mx-refdisclose" role="note">
  <strong>Paid referral.</strong> The author of this recommendation receives a
  one-time payment of <span data-count-src="/data/referral.json#rate">…</span> if you
  enrol using their code. They receive nothing further, and nothing if you refund.
  <a href="/about/access/referrals/">How referrals work here →</a>
</p>
```

Three properties are mandatory. The rate renders from `data-count-src`, so it cannot drift from
the published figure — the [Page Contract](../site/page-contract.md) line 13 rule applied to
money. The words *"receives nothing further"* are required verbatim, because the single most
common reader assumption about affiliate links is an ongoing relationship. And the disclosure
carries `role="note"`, styled as `--panel` with a `--gold` left rule and **no animation** — the
same treatment as the demo strip, for the same reason: it is a notice, not a promotion.

### 3.3 Schema-level prohibition

Following the pattern MX-021 established for riba, the prohibitions are enforced in the **database
schema** and not in policy prose. The `mx_commerce` referral tables must contain **no** column
capable of expressing an excluded structure:

| Forbidden column | Would enable |
|---|---|
| `parent_referrer_id` | Two-tier / pyramid structures |
| `recurring_period` · `commission_schedule` | Recurring commission |
| `tier` · `bonus_rate` · `rank` | Volume tiers and leaderboards |
| `negotiated_rate` | Per-referrer rate variation |
| `clawback_until` | Penalty on severance |
| `attribution_cookie` · `landing_referrer` | Content-plane tracking |

**Why schema rather than policy.** A policy prohibition is enforced by whoever remembers it. A
schema prohibition is enforced by the database refusing to store the data, which means a future
developer implementing a "small" tiered bonus must first alter the schema — a visible, reviewable,
changelog-generating act. This is the estate's general method for structural commitments: make the
prohibited thing *unrepresentable* rather than merely disallowed.

### 3.4 Who may refer, and who may not

| May refer | May not refer |
|---|---|
| Any enrolled learner | Anyone reviewing credentials |
| A credential holder | Anyone assessing an academy application |
| An academy curator, for their **own** academy's learners | The Curator and anyone in a named governance role |
| An unaffiliated reader with an account | Anyone whose referral income would exceed a published proportion of their total income from the estate |

The last exclusion is the substantive one and it is the standard's own invention. If a person's
compensation from the estate becomes predominantly referral income, their relationship to the
estate has changed from participant to distributor, and their recommendations acquire an interest
the disclosure component cannot adequately convey. The threshold is a published figure requiring
Curator ratification (§8) — it is not set here, because setting it would be the documentation
layer deciding a commercial term.

The reviewer exclusions are absolute and follow from
[MX-016](../corpus/) and `/credentials/review/conflicts/`: a person who both assesses submissions
and profits from enrolments has an interest in the volume of the thing they gatekeep.

---

## 4. Worked instance

A learner completes series S01 and writes a public field note about it, including her referral
code `MX-REF-K7QP2A`.

**At publication.** The `.mx-refdisclose` block renders inline beneath her recommendation, stating
the one-time rate from `/data/referral.json#rate`, the words "receives nothing further," and a
link to `/about/access/referrals/`. A reader sees the financial interest in the same view as the
recommendation, without interaction.

**At enrolment.** A reader decides to enrol. He navigates to `pay.metax.academy/checkout/{sku}`
and types `MX-REF-K7QP2A` into the referral field. Nothing tracked him from her post to the
checkout; nothing on the content plane observed the transit. He typed a code he chose to type,
which means he can also audit the transaction he took part in.

**At the refund window's close.** Thirty days later, with no refund, the payment is issued once.
`mx_commerce` records a single row: referrer, referred enrolment, published rate, date. There is
no `recurring_period` column to populate, no `parent_referrer_id` to attribute upward, no `tier`
to advance.

**What did not happen, and what it cost.** Four other readers enrolled after reading her post and
none entered the code — two forgot, two never noticed the field. She is compensated for one
referral out of five. **This is the standard operating correctly, not failing.** She was told
before she joined that attribution is voluntary and lossy. The four unattributed enrolments are
the price of the other several thousand readers of that post who were not tracked, profiled or
cookied in order to make her attribution accurate.

**The counterfactual, stated to make the trade visible.** Under a conventional 30-day-cookie
program she would have been paid five times, the estate would have earned the same revenue, and
every reader of her post would have carried a commercial identifier across the content plane for a
month. The estate judges the second outcome worse, and it is important that this instrument states
the judgement rather than implying that the compliant design has no cost.

---

## 5. Failure modes

**The disclosure that recedes.** Signature: a referral disclosure moved to a footer, collapsed
behind "details," or set at 0.7rem grey-on-grey. Each step is individually defensible on layout
grounds and the aggregate is a disclosure nobody reads. The remedy is the mandated component of
§3.2, and the reason it specifies typeface and placement rather than merely requiring
"disclosure."

**The attribution complaint that becomes a tracking proposal.** The most likely failure of this
standard, and it will arrive as a reasonable request. Referrers *will* report unpaid referrals,
because §3.1 guarantees some. The fix that will be proposed is a cookie, a link parameter, or a
"lightweight" fingerprint. Each reintroduces content-plane tracking to solve a problem the estate
created deliberately, and the answer must be no — with the cost acknowledged rather than denied.

**Tier creep.** A volume bonus for the estate's most effective advocates, framed as fairness.
Excluded at the schema level precisely because it is the change most likely to seem harmless.

**The academy curator referring their own learners.** Permitted, and the boundary is finer than it
looks. A curator recommending their own academy is disclosing an interest a reader can already
infer. A curator recommending *another* academy while holding a referral interest is not, and
falls under the general disclosure rule with no exception.

**Referral income becoming the relationship.** §3.4's last exclusion. Signature: a participant
whose public writing about the estate correlates with enrolment cycles rather than with anything
they learned.

**HX‑15 in the program's own reporting.** A referral program publishing only its totals — amounts
paid, referrers active — while omitting its unattributed-referral rate is reporting the flattering
half of a system whose defining characteristic is the unflattering half. §7 requires both.

---

## 6. Limits

**Class: economic.** This standard is plausibly uncompetitive. Every mechanic that makes affiliate
programs effective — recurring commission, tiers, leaderboards, accurate cookie attribution — is
excluded. A referrer choosing between this program and a conventional one will earn less here, and
this instrument does not claim otherwise. Whether the estate can attract referrers on these terms
is an untested commercial question.

**Class: ethical.** The standard does not resolve whether the estate should pay for introductions
**at all**. A defensible position holds that any payment for a recommendation compromises it,
however disclosed, and that the estate's better answer is no program. This document specifies what
a compliant program would look like *if* there is one; it does not argue that there should be
([RAT-23](../00-governance-map/open-questions-and-ratifications.md)).

**Class: technical.** Attribution is lossy by construction and the loss rate is unknown until the
program runs. If it proves severe — most referrals unattributed — the program is not merely
inefficient but *unfair to referrers*, and §7's falsifier is written against exactly that.

**Class: epistemic.** This standard has **no upstream source.** Every other instrument in this
corpus reconciles supplied material; this one was reasoned from the estate's existing commitments
by an agent. Its four elements are modelled on §C.9's structure by analogy, and that analogy has
not been reviewed by anyone qualified in the underlying jurisprudence
([RAT-12](../00-governance-map/open-questions-and-ratifications.md#rat-12) is the nearest existing
review and does not cover this).

---

## 7. Falsifier

This standard is wrong if any of the following is observed:

1. **A compliant referral that is nonetheless deceptive** — all four elements satisfied and a
   reader still materially misled about the recommender's interest. That would show the four
   elements to be insufficient rather than merely necessary.
2. **An unattributed-referral rate above a published threshold**, showing §3.1's code mechanism to
   be unfair to referrers rather than merely lossy. The rate must be published for this falsifier
   to be runnable at all, which is why §8 requires it.
3. **A referrer whose income structure evades all four elements while functioning as a recurring
   commission** — for instance repeated single payments arranged to approximate a subscription
   share. This would show the elements to be formally satisfiable and substantively empty, which
   is the standard failure mode of element-based tests.
4. **The program running with no measurable difference in reader behaviour on the content plane**
   compared to a cookie-based program — which would falsify the premise that the tracking
   avoidance is worth its attribution cost.

---

## 8. Obligation

**Before the program launches**, four figures require the Curator's ratification and none may be
set by the documentation layer: the referral rate; the refund-window length before payment issues;
the income-proportion threshold of §3.4; and the unattributed-referral threshold above which
falsifier 2 fires. All four are commercial terms.

**Quarterly publication**, at `/about/access/referrals/`, of both halves:

| Must publish | Why |
|---|---|
| Total referrals paid, and the rate | Ordinary transparency |
| **Unattributed-referral estimate** | The unflattering half; omitting it is §5's HX‑15 failure |
| Number of referrers, and the share of total enrolments referred | Lets a reader judge whether the estate has become referral-dependent |
| Any exclusion applied under §3.4 | With reasons, per the estate's general rule on rejected submissions |

**Under ML‑2.3:** §C.9 (riba's four elements — the analytical model for §2), §H.4 (optimisation
disclosure), §H.8 (intermediation rent — the reason element 2 exists), §H.18 (consent integrity —
the reason element 1 is at the point of influence), §H.19 (authorship of record — the reason this
document's front matter names it as designed from scratch), §H.29 (substitution disclosure).

**Standing obligation on this instrument specifically.** Because it has no upstream source, it
must be reviewed against a supplied source the moment one exists. If the Curator holds a referral
design of his own, **his supersedes this in its entirety** and this document becomes a
non-governing draft retained under
[Charter §0.8](../corpus/mx-000-charter.md). An agent-designed commercial instrument governing by
default, merely because nobody supplied an alternative, is a governance defect in itself — and it
is filed as one.

---

**Related:** [MX-021 Payments and Commerce](../corpus/mx-021-payments-and-commerce.md) ·
[ST-22 Platform and Persistence](st-22-platform-and-persistence.md) ·
[ST-24 Page Prose Standard](st-24-page-prose-standard.md) ·
[ML-2.3](../license/ml-2-3.md) ·
[Route Manifest](../site/route-manifest.md) ·
[Defect Register](../00-governance-map/defect-register.md)

*Curated by Maher. Designed from scratch with no upstream source, and marked as such. Four
cumulative elements, six forbidden schema columns, one accepted loss of attribution accuracy — and
an open question about whether the program should exist at all.*
