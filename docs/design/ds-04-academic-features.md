---
doc_id: "DS-04"
title_en: "The Twelve Academic Features"
title_ar: "الميزات الأكاديمية الاثنتا عشرة"
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
derived_from: ["MX-DESIGN-001 Part 9", "MX-DESIGN-001 Part 12"]
last_reviewed: "2026-08-30"
domain_tags: ["design", "pedagogy", "governance"]
ai_disclosure_url: "../corpus/mx-007-ai-use-and-disclosure.md"
hreflang: "en, ar"
---

# DS-04 — The Twelve Academic Features

**Governs:** the twelve features added in v2026.09.2, their plane placement, and the failure mode
each exists to prevent.

Each feature is split at the **read/write seam** per
[ST-19 §5.1](../standards/st-19-two-plane-architecture.md#51-the-readwrite-seam): the **ledger**
is content-plane, static, citable and archived; the **transaction** is identity-plane, private
and unarchived. Where the source document placed a stateful feature on a content-plane route, the
split is recorded at
[R-31](../00-governance-map/reconciliation-ledger.md#r-31--content-plane-routes-in-part-9-that-cannot-be-static).

**Build order** (from Part 12, adopted as normative): **1, 3, 9, 2, 11, 5, 6, 4, 8, 12, 7, 10.**
Pre-registration, decay watch and the passport come first *because they make existing doctrine
binding rather than advisory*. The viva and the exchange come last *because they require human
capacity that does not yet exist* — which is a scheduling constraint stated honestly rather than a
priority judgement.

---

## 1 · The Pre-Registration Desk

| | |
|---|---|
| **Ledger** | `toptech.metax.academy/prereg/{id}/` — build-generated mirror of a closed filing |
| **Transaction** | `me.metax.academy/prereg/` |

Before a capstone begins, the learner files a **hypothesis, an explicit null, a decision rule and
a stopping condition**. The filing is hashed and timestamped, and it **publishes automatically
when the capstone concludes — whatever the result.**

The UI makes editing after the start **impossible rather than merely discouraged**: the edit
control is replaced by an **"amend with public diff"** control.

**Failure mode prevented:** the retrofitted success story — *"the single most common lie in
professional education."* A learner who chooses their hypothesis after seeing their data has
learned nothing except how to look competent.

---

## 3 · Decay Watch

| | |
|---|---|
| **Ledger** | `library.metax.academy/decay/` — overdue claims by pillar; public count on the hub's honesty strip |
| **Transaction** | `me…/digest/` — per-series subscription |

Every claim in the estate carries a decay class and a review date
([ST-05](../standards/st-05-decay-and-review-intervals.md)). Learners subscribe per series and
receive a digest line when material they have **completed** expires.

**The uncomfortable feature is the point: MetaX publishes its own staleness.** Most institutions
know which of their material is out of date and treat that knowledge as internal. Publishing it
means a reader can see the estate ageing in real time, and can hold the Curator to the review
interval rather than trusting it.

---

## 9 · The Bridge Passport

| | |
|---|---|
| **Ledger** | Rung-entry gating rules, published |
| **Transaction** | `me.metax.academy/passport/` |

A cumulative record of which Limits modules and Bridge lessons a learner has completed, rendered
as a ladder.

**It is not decorative.** Ascent rung entry and any future Branch E access are **gated** on
specific passport entries. This is the mechanism that makes the
[Limits-before-Bridge doctrine](../standards/st-03-limits-and-bridge.md) **binding rather than
advisory** — before the passport existed, "learn the limits first" was a recommendation with no
enforcement point.

---

## 2 · Adversarial Review Exchange

**`me.metax.academy/reviews/`** — identity plane. Inter-reviewer agreement is published in the
Integrity Report (content plane).

A **reciprocity market**: one structured critique received for each one delivered, scored against
the frozen **D1–D5** rubric ([RB-01](../rubrics/rb-01-d1-d5-rubric.md) — note the D-prefix
collision resolved at
[R-04](../00-governance-map/reconciliation-ledger.md#r-04--the-d-prefix-collision)).

| Rule | Reason |
|---|---|
| Five-axis rubric form | Matches RB-01 dimensions exactly |
| **Forces a stated weakness before a stated strength** | Order determines what gets written; strengths-first reviews taper into praise |
| **Refuses submission under 120 words** | A review too short to contain a reason is not a review |
| Anonymous by default, de-anonymised on **mutual** consent | |
| Reviewers calibrated against gold-standard artefacts **quarterly** | Drift is measured, not assumed |

---

## 11 · The Correction Bounty

| | |
|---|---|
| **Ledger** | `library.metax.academy/corrections/` |
| **Transaction** | `me…/corrections/new/` |

Public defect submission against **any page in the estate**. Accepted corrections are credited by
name in the changelog **and on the corrected page's stamp**, and contributors accumulate a
Corrections standing visible on their profile.

**The ledger publishes rejected submissions too, with reasons** — *"which is what stops the queue
becoming a black box."* A corrections process that shows only its successes tells the reader
nothing about what it declines to fix.

Categories: factual error · stale claim · broken citation · accessibility defect · notation
inconsistency · translation divergence.

---

## 5 · The Artefact Vault

**`me.metax.academy/artefacts/`** — identity plane. Optional public artefact URL on the content
plane.

Version-controlled, **content-hashed** storage for capstone evidence. Each artefact receives a
permanent citable identifier.

**Because the hash is recorded in the credential record, evidence cannot be swapped after
certification.** This is the technical fact that makes a MetaX credential mean something specific:
it attests to a *particular* artefact, not to a category of work.

Supports documents, datasets, repositories by reference, and recorded walkthroughs. **Storage
quotas are stated in plain numbers on the pricing page** — before purchase, per
[MX-021 §21.1.2](../corpus/mx-021-payments-and-commerce.md#2112-the-disclosure-rule).

---

## 6 · Deterministic Scenario Assessment — **unresolved**

**`/s/{id}/c/{nn}/scenario/`** — the sixth beat of the lesson arc. A seeded branching scenario
with a fixed decision tree and **published scoring logic**. **No language model participates in
scoring.**

After completion the learner opens the **full tree** and sees every path not taken and its
consequence — *"the debrief is the actual teaching, and the assessment is the pretext."*

> **This feature does not resolve cleanly against the plane boundary and is the one open design
> question in this document.** A tree that ships in static HTML can be read before deciding; a
> tree that is withheld requires request-time state. Three options, their trade-offs, and the
> provisional resolution (fully public tree, reframed as a **rehearsal rather than a gate**) are
> at [RAT-11](../00-governance-map/open-questions-and-ratifications.md#rat-11--how-the-scenario-assessment-resolves-against-the-plane-boundary).
> **It may not be built until Maher decides.**

---

## 4 · Time-Boxed Asynchronous Cohorts

**`toptech.metax.academy/cohorts/`** — content plane for the archive; enrolment on the identity
plane.

Ninety-day capstone cohorts with a fixed open and a **fixed permanent close**. **No live video
requirement, no timezone tyranny** — the cadence is weekly artefact drops and peer critique
windows. The calendar renders as a single vertical spine with three states per week: **due,
delivered, reviewed.**

**When a cohort closes it becomes a read-only public archive including the post-mortems, so
cohort N+1 learns from cohort N's failures.** Publishing the post-mortems is what distinguishes
this from a course that merely ran repeatedly.

---

## 8 · The Citation Ledger

**`library.metax.academy/citations/`** — content plane, static.

Every source in the estate, monitored for **link rot, retraction and version drift**, with an
**archived snapshot recorded at citation time**.

**Any lesson citing a retracted source is automatically flagged as a defect on its own page
within one build cycle.** Learners see source health inline as a small state marker next to each
citation.

The automatic flag is the substantive part. Retractions are usually discovered by whoever was
already suspicious; a system that surfaces them on the citing page tells the reader who was not.

---

## 12 · The Determination Queue

**`metax.academy/about/governance/queue/`** — content plane, static.

Every pending governance decision — charter applications, appeals, ethics reviews, licence
determinations — visible as an **anonymised** queue with filing date, class, service-level target,
and **an escalation timer that turns amber then red in public when a target is missed.**

Under [AG-000 §A.6](../agents/ag-000-agent-constitution.md#a6-degraded-mode-and-prompter-succession)
degraded mode, the queue displays the degraded banner and the **reduced authority ceiling**.

*"Governance that can be watched is governance that can be held to account, and this is the
feature that makes the Curator's own performance falsifiable."* It is the only feature in this
document whose primary cost falls on Maher.

---

## 7 · The Mastery Viva

**`me.metax.academy/viva/`** — identity plane for scheduling; outcomes on the content plane.

The **P3 rung's oral defence** ([RB-02](../rubrics/rb-02-proof-ladder.md)): a scheduled
sixty-minute examination by **two calibrated reviewers**, with a published question bank of
**domain areas but not questions**.

**The transcript is published with holder consent; the outcome is published regardless.**

*"This is the operational meaning of 'mastery is judgment under scrutiny,' and until it existed
that sentence was a slogan."* Recorded verbatim because it is the clearest statement in the source
of why these features exist: each one converts a sentence the corpus already asserted into a
mechanism that could fail.

---

## 10 · Academy Exchange

**`academies.metax.academy/exchange/`** — content plane, static.

Chartered academies publish modules against a shared schema. Cross-credit recognition is expressed
as **explicit equivalence mappings**, each requiring **both curators' signatures and a stated
basis**.

The UI shows a mapping as a **two-column comparison of learning outcomes with the delta
highlighted**, so recognition is *"always inspectable rather than mutual back-scratching."*
Mutual recognition without a published delta is how credential inflation begins between
institutions that like each other.

---

## Reserved slots

Two slots are **reserved and deliberately unspecified**:

- An **Arabic Translation Bench**
- An **Open Problem Claims** register

*"So that the roadmap has stated capacity for growth rather than presenting itself as complete."*
Both are honest reservations rather than placeholders: they are named, unspecified, and carry no
implied delivery date. They may not be rendered as forthcoming features.

---

## Summary — plane placement

| # | Feature | Content plane (ledger) | Identity plane (transaction) |
|---:|---|---|---|
| 1 | Pre-Registration Desk | `toptech…/prereg/{id}/` | `me…/prereg/` |
| 2 | Adversarial Review | Integrity Report agreement stats | `me…/reviews/` |
| 3 | Decay Watch | `library…/decay/` | `me…/digest/` |
| 4 | Cohorts | `toptech…/cohorts/` archive | enrolment |
| 5 | Artefact Vault | optional public artefact URL | `me…/artefacts/` |
| 6 | Scenario Assessment | **unresolved — [RAT-11](../00-governance-map/open-questions-and-ratifications.md#rat-11--how-the-scenario-assessment-resolves-against-the-plane-boundary)** | — |
| 7 | Mastery Viva | outcomes, transcripts on consent | `me…/viva/` |
| 8 | Citation Ledger | `library…/citations/` | — |
| 9 | Bridge Passport | gating rules | `me…/passport/` |
| 10 | Academy Exchange | `academies…/exchange/` | signatures |
| 11 | Correction Bounty | `library…/corrections/` | `me…/corrections/new/` |
| 12 | Determination Queue | `/about/governance/queue/` | — |

---

**Related:** [DS-05 Certification Surfaces](ds-05-certification-surfaces.md) ·
[ST-19 Two-Plane Architecture](../standards/st-19-two-plane-architecture.md) ·
[ST-03 Limits and Bridge](../standards/st-03-limits-and-bridge.md) ·
[RB-01 D1–D5 Rubric](../rubrics/rb-01-d1-d5-rubric.md) ·
[RB-02 Proof Ladder](../rubrics/rb-02-proof-ladder.md) ·
[MX-005 Credentialing](../corpus/mx-005-credentialing-and-assessment.md)

*Curated by Maher. Eleven of these twelve features make an existing MetaX claim falsifiable. The
twelfth is unresolved and says so.*
