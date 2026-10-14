---
doc_id: "MX-024"
title_en: "Infrastructure, Capacity and Migration"
title_ar: "البنية التحتية والسعة والترحيل"
family: "corpus"
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
domain_tags: ["corpus", "infrastructure", "capacity", "migration", "continuity"]
route: "/about/status/migration/"
derived_from: "MetaX.Academy Platform Data Persistence Architecture, Part 14"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# MX-024 · Infrastructure, Capacity and Migration

**What this instrument is.** The estate's position on the infrastructure it runs on: what it
depends on, what happens when a limit is reached, and how it leaves a provider without losing the
record.

**Numbering note.** The architecture source proposed this as "MX-022 Infrastructure & Migration."
`MX-022` was already Identity and Sessions, and `MX-023` had been allocated to Attention and Human
Sovereignty, so under [ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md#3-rule-2--numbers-are-immortal)
— numbers are immortal from first assignment — this instrument takes **MX-024**. Same reasoning as
[R-25](../00-governance-map/reconciliation-ledger.md#r-25--the-mx-020-numbering-collision).

---

## 1. Position

Infrastructure is where an estate's stated commitments meet a bill and a rate limit, and it is
where governance corpora characteristically stop looking. The reason is understandable: hosting
feels like an implementation detail, and implementation details do not belong in a charter.

They belong here for one reason. **Every durability claim this estate makes is a claim about
infrastructure.** [ML-2.3 §E.7](../license/ml-2-3.md) requires the licence text in three
independent locations. [SITE-03 §6](../site/routing-law.md) requires that an address published in
2026 resolve in 2031. [MX-013](mx-013-records-and-versioning.md) requires superseded text retained
permanently. [HX-002 §7](../harms/hx-002-harm-instrument-map.md) maps HX‑23 (custody without
horizon) against this estate. None of those is satisfiable by a document; each is a statement
about where bytes live and who controls them.

Its published route is `/about/status/migration/`, alongside the capacity meter. Its sibling is
[ST-22](../standards/st-22-platform-and-persistence.md), which specifies the persistence tiers;
this instrument states the **doctrine** those tiers implement.

**The macro register.** A body of knowledge on rented infrastructure is a body of knowledge whose
continuity is a commercial relationship. That is the ordinary condition of nearly everything
published this century, and it is why so much of the last two decades of the web is simply gone —
not censored, not refuted, just discontinued. Under Stratum VI this is **HX‑20** (inheritance of
unauditable systems) and **HX‑23** (custody without horizon): a successor inherits not a corpus
but a dependency they did not choose and cannot audit. An estate claiming to write for the
successor owes a plan for the day its provider changes terms, and this instrument is that plan.

---

## 2. Definition — the four data tiers and what each may hold

From the architecture source, adopted with the boundaries stated as prohibitions rather than
guidance.

| Tier | Store | May hold | May **never** hold |
|---|---|---|---|
| **T1** | Build artefacts (static files) | Everything published: pages, JSON, the corpus | Anything per-user |
| **T2** | Workers KV | **Configuration only** — flags, thresholds, published rates | Per-user records, session state, anything written at request time |
| **T3** | D1 (SQLite) | Identity, learning, credentials, commerce, academies, governance | Anything reconstructible from T1 |
| **T4** | IndexedDB (browser) | **Cache and outbox only** | Anything that exists only here |

**T2's write budget is the constraint that shapes the design:** 1,000 writes per day. That is a
configuration budget, not an application budget, and it is why T2 is restricted to config by
doctrine rather than by preference. A single feature that writes per-request to KV exhausts the
estate's daily budget before noon, and the failure is not graceful.

**T4's restriction is the one that protects the reader.** IndexedDB holds a cache and an outbox —
never a record of record. A learner's artefact submitted offline sits in the outbox until it
reaches T3; it does not *live* in the browser. The reason is that browser storage is deletable by
the browser, by the user, by a privacy sweep or by a disk-cleanup utility, and a system that keeps
a person's only copy there has made them the custodian of a record they did not agree to keep.

### 2.1 The six databases

`mx_identity` · `mx_learn` · `mx_credentials` · `mx_commerce` · `mx_academies` · `mx_governance`

Separated rather than unified, and the separation is a governance choice with three consequences.
A breach of one is not a breach of all. `mx_commerce` can be audited for riba compliance in
isolation — which is what makes the schema-level prohibition in
[MX-021](mx-021-payments-and-commerce.md) and
[ST-23 §3.3](../standards/st-23-affiliate-and-referral.md) checkable rather than aspirational. And
`mx_governance` can be **published in full**, since it holds no personal data by construction:
determinations, defects, corrections, registry state.

**The riba prohibition is enforced in schema, not policy.** `mx_commerce` contains no
`interest_rate`, no `late_fee`, no `financing_partner` column. A future developer implementing
instalment interest must first alter the schema — a visible, reviewable, changelog-generating act.
The estate's general method is to make a prohibited thing **unrepresentable** rather than merely
disallowed.

---

## 3. Mechanism

### 3.1 The 80% tripwire

Every metered resource carries a threshold at **80% of its limit**, published on the capacity
meter at `/about/status/capacity/`. Crossing it triggers a migration decision, not an alarm.

| Resource | Limit | Tripwire | Current state |
|---|---|---|---|
| Pages files | 20,000 | 16,000 | ≈2,000 planned — **not binding** |
| Workers requests | 100,000/day | 80,000/day | **The first real tripwire** |
| KV writes | 1,000/day | 800/day | Config only, far below |
| D1 storage | Per-plan | 80% | No rows exist |

**The binding constraint moved in this release**, and the correction is instructive.
[DEF‑2026‑041](../00-governance-map/defect-register.md#def-2026-041) was filed as a file-count
crisis: at ~91 pre-rendered routes per series, 20,000 files arrives at ~219 series. Under directory
routing the arithmetic is ≈2,000 files including assets, leaving headroom for roughly **450 further
series** ([R-54](../00-governance-map/reconciliation-ledger.md#r-54--the-file-ceiling-is-no-longer-binding)).

The defect stays open under its original number because **the risk was real and its subject
changed**: it is now a request-rate constraint wearing a file-count constraint's identifier.
Renumbering it would have concealed that the estate's capacity thinking had been aimed at the
wrong resource for a month.

**Why 80% and not 95%.** A tripwire exists to leave time to decide. At 95% the decision is made
under duress, and a migration decided under duress is a migration that loses things. The estate
would rather move early and pay for capacity it does not need than move late and drop a record.

### 3.2 Migration doctrine — three properties, in order

**Property 1: the content plane must be movable by copying.** T1 is static files. A complete
migration of the published estate is `rsync` to any static host, and the only host-specific
artefacts are `_redirects` and the Workers routing. This is the single most important property in
this instrument, and it is what makes the estate's durability claims true rather than hopeful.

It also constrains the design permanently: **no feature may make the content plane
non-copyable.** A server-side render, an edge-computed personalisation, a build step requiring a
proprietary service — each would trade this property for a convenience, and each is refused.

**Property 2: the identity plane may be harder to move, and must be movable.** T3 is SQLite; D1
exports to standard SQL. The six-database separation means each can move independently.
`mx_governance` moves first in any migration, because it holds the record.

**Property 3: the record moves before the features.** Migration order is fixed:
`mx_governance` → T1 static estate → `mx_credentials` → `mx_identity` → the rest. A partial
migration that lands the courseware and leaves the corrections log behind has moved the product
and abandoned the accountability, which is the precise inversion this estate exists to refuse.

### 3.3 The VPS path

The published migration target is a self-hosted VPS with the same shape: static files served
directly, SQLite on disk, no managed-platform dependency. It is documented at
`/about/status/migration/` **before it is needed**, because a migration plan written under
pressure is a migration plan that discovers its own gaps in production.

**What the estate loses by moving:** edge distribution, automatic TLS renewal, DDoS absorption,
and the operational simplicity of a managed platform. **What it gains:** no dependency on a
provider's terms, no metered request ceiling, and custody of its own record.

The estate does not claim the VPS is better. It claims the *option* must exist and must be
exercised before it is forced, because an option never tested is not an option.

### 3.4 What the estate does not control

Stated plainly, because a dependency list is only useful when it is complete.

| Dependency | Failure consequence | Mitigation |
|---|---|---|
| Cloudflare Pages/Workers | Content plane offline | T1 copyable; VPS path documented |
| D1 | Identity and commerce offline; **content plane unaffected** | The two-plane boundary is the mitigation |
| Binance Pay | No payments; single rail — [DEF-014](../00-governance-map/defect-register.md#def-014) | **None.** [RAT-13](../00-governance-map/open-questions-and-ratifications.md#rat-13) |
| The domain registrar | Every address in the estate breaks | **None currently** — see §5 |
| Google Fonts CDN | Type falls back | Acceptable; local hosting available |
| AdSense / Adsterra | Revenue stops | Not mitigated, and see [MX-023 §3.6](mx-023-attention-and-human-sovereignty.md) |

**Two rows read "none," and the second is the more serious.** Every permanent address this estate
publishes — the whole basis of [SITE-03](../site/routing-law.md)'s citation-durability claim —
depends on continued control of one domain name. §E.7's requirement for a content-addressed mirror
is the intended answer, and it does not exist
([B-02](../00-governance-map/launch-blockers.md)).

---

## 4. Worked instance — the day the request ceiling is reached

Workers requests are the first tripwire, so: the estate has published, traffic grows, and the
meter reads 80,000/day.

**What happens at 80%.** The capacity meter shows amber at `/about/status/capacity/`, publicly —
readers see the constraint at the same time the Curator does, because a capacity meter visible only
internally is a dashboard, not a disclosure. A migration decision is opened with a stated deadline.

**The three options, with their real costs.** Pay for the higher tier: cheapest in effort, and
increases dependency on one provider. Reduce requests: the search index fetch and the island
hydration are the two largest consumers, and cutting either degrades the reader's experience to
protect a bill. Migrate to the VPS: highest effort, removes the ceiling entirely, loses edge
distribution.

**What the estate is committed to doing first, regardless of which it chooses.** Publish the
figure and the decision. Under [MX-013](mx-013-records-and-versioning.md) and
[ML-2.3 §H.28](../license/ml-2-3.md) a capacity decision that changes what readers receive is a
change to the record's availability, and it is announced rather than absorbed quietly.

**What it may not do.** Silently degrade. Serving a lighter page, dropping the Arabic mirror, or
disabling the search index to stay under a ceiling — without saying so — is a change to what was
published, presented as continuity. That is **HX‑25** (silence in the record), and it is the
failure mode this whole instrument is written against: infrastructure decisions are the easiest
place in an estate to break a promise invisibly.

---

## 5. Failure modes

**The silent degradation.** §4's last paragraph. The characteristic infrastructure failure,
because it is invisible to everyone except the reader who noticed the Arabic page is gone.

**Migration deferred past the tripwire.** 80% exists to leave decision time; the failure is
treating amber as informational until it is red.

**The convenient dependency.** A feature that requires a managed service — a server-rendered
personalisation, an edge-computed recommendation — trading Property 1 for a convenience. Each
individual case is defensible and the aggregate is a content plane that can no longer be moved by
copying.

**The unmitigated single points, unrevisited.** §3.4's two "none" rows. A dependency table whose
gaps are published and never closed has converted a risk into a disclosure, which is
[HX-001](../harms/hx-001-harm-audit-rubric.md)'s D=1: disclosure is a floor, never a remedy.

**Capacity metrics becoming performance metrics.** Reporting request growth as success. Requests
are a cost, and an estate that celebrates them has adopted the engagement frame
[MX-023 §3.1](mx-023-attention-and-human-sovereignty.md) refuses.

---

## 6. Limits

**Class: technical.** This instrument specifies a shape and not an implementation. No D1 database
exists, no row has been written, and the four-tier model is untested against real traffic. It is a
design, and designs discover their errors at load.

**Class: economic.** The VPS path is documented and uncosted. Whether the estate can afford
self-hosting at the point the ceiling arrives is unknown, and the honest reading is that a
migration option requiring money the estate may not have is weaker than this document makes it
sound.

**Class: epistemic.** Every figure here — 20,000 files, 100,000 requests, 1,000 KV writes — is a
**perishable** claim about a third party's terms, dated 2026‑10‑01. Provider limits change without
notice, and under [ST-05](../standards/st-05-decay-and-review-intervals.md) this instrument
reviews every six months for exactly that reason.

**Class: governance.** The domain-name dependency (§3.4) has no mitigation and this instrument
cannot create one. It requires a content-addressed mirror under §E.7, which requires
[B-02](../00-governance-map/launch-blockers.md), which is the Curator's.

---

## 7. Falsifier

This instrument is wrong if:

1. **A complete content-plane migration by copying is attempted and fails** — falsifying
   Property 1, which every durability claim in the corpus rests on. Testable now, cheaply, and
   **untested**.
2. **The 80% tripwire fires and the decision cannot be made in the time it leaves** — showing 80%
   to be too late rather than early.
3. **A resource limit is reached that appears nowhere in §3.1's table** — showing the capacity
   model incomplete. The likeliest candidate is a limit the estate has not thought to meter.
4. **`mx_governance` proves to contain personal data**, falsifying §2.1's claim that it can be
   published in full.

Falsifier 1 should be run before the estate needs it. A migration property asserted and never
exercised is the same class of claim as a backup never restored.

---

## 8. Obligation

**For the estate:** publish the capacity meter at 80% thresholds before wave 1
([Launch Blockers](../00-governance-map/launch-blockers.md)). Test falsifier 1 — copy the whole T1
estate to a second host and serve it — before publication rather than after. Close §3.4's two
unmitigated rows, or state annually that they remain open and why.

**For the build:** no feature may make the content plane non-copyable (Property 1). No per-request
write to T2. No record of record in T4. Any change to these is a specification change requiring a
changelog line.

**For a successor:** the migration order of Property 3 is `mx_governance` first, then the static
estate, then credentials, then identity. **The record moves before the features.** If you inherit
this estate mid-migration and must choose, choose the record — the courseware can be rewritten and
the corrections log cannot.

**Under ML-2.3:** §E.7 (registry continuity — the mirrors this instrument cannot supply), §H.10
(material cost), §H.11 (fragility and dependency), §H.23 (custody without horizon), §H.24
(irreversible commitment — currently `unexamined` against this estate, per
[HX-002 §7](../harms/hx-002-harm-instrument-map.md)), §H.27 (reversibility), §H.28 (custody and
horizon).

---

**Related:** [ST-22 Platform and Persistence](../standards/st-22-platform-and-persistence.md) ·
[MX-021 Payments and Commerce](mx-021-payments-and-commerce.md) ·
[MX-022 Identity and Sessions](mx-022-identity-and-sessions.md) ·
[MX-023 Attention and Human Sovereignty](mx-023-attention-and-human-sovereignty.md) ·
[MX-015 Succession](mx-015-succession-and-continuity.md) ·
[SITE-03 Routing Law](../site/routing-law.md) ·
[Registry and Mirrors](../license/registry-and-mirrors.md) · [ML-2.3](../license/ml-2-3.md)

*Curated by Maher. Four tiers, six databases, one tripwire at 80%, and two dependencies with no
mitigation at all — one of which is the domain name every permanent address in this estate depends
on.*
