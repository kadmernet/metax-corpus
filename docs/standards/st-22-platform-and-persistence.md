---
doc_id: "ST-22"
title_en: "Platform, Persistence and the Capacity Meter"
title_ar: "المنصّة والتخزين ومقياس السعة"
family: "standards"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 4
depth: 5
evidence_class: "perishable"
review_interval_months: 3
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["standards", "persistence", "data-tiers", "capacity", "d1"]
route: "/library/stack/data-tiers/"
derived_from: "MetaX.Academy Platform Data Persistence Architecture v2026.09.3"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# ST-22 · Platform, Persistence and the Capacity Meter

**What this standard governs.** Where a byte may live, what may be written to each store, and how
the estate knows when a store is running out. [MX-024](../corpus/mx-024-infrastructure-and-migration.md)
states the doctrine; this standard is the **enforceable specification** a build can be checked
against.

**Evidence class `perishable`, reviewed quarterly.** Every quantitative figure here is a claim
about a third party's terms and decays without notice. A persistence standard written as though
platform limits were durable is a standard that will be quietly wrong within a year.

---

## 1. Position

Persistence is where an estate's principles become schemas, and a schema is a far stronger
commitment than a policy. This standard exists because the estate has learned — from its own
[Corrections Log](../00-governance-map/corrections-log.md) — that a stated prohibition is enforced
by whoever remembers it, while a **missing column** is enforced by the database.

Its parent is [ST-19 Two-Plane Architecture](st-19-two-plane-architecture.md), which draws the
boundary between the content and identity planes; this standard says which store sits on which
side of it. Its published route is `/library/stack/data-tiers/`.

**The claim it makes, stated once so the rest of the document can be read against it:** a store's
*capability* determines what will eventually be written to it, regardless of what policy says.
Restricting a store by doctrine and then giving it general write capability is a plan to be
surprised. Every rule below is therefore expressed as a **capability restriction** wherever the
platform allows one.

---

## 2. Definition — the four tiers

| Tier | Store | Authority | May hold | May **never** hold |
|---|---|---|---|---|
| **T1** | Build artefacts | Source of truth for everything published | Pages, JSON, the corpus, the search index | Anything per-user |
| **T2** | Workers KV | Configuration | Flags, thresholds, published rates, feature switches | Per-user records, session state, request-time writes |
| **T3** | D1 (SQLite) | Source of truth for identity, commerce, credentials | Six databases per §4 | Anything reconstructible from T1 |
| **T4** | IndexedDB | **Cache and outbox only** | A copy of T1 for offline read; a queue of pending writes | Any record of record |

### 2.1 The four boundary rules, each stated as a test

**T1 → nothing per-user.** T1 is a static file served identically to everyone. A per-user value in
T1 means a build per user, which is not a static estate. *Test:* if two readers could receive
different bytes for the same path, the value does not belong in T1.

**T2 → configuration only, never request-time writes.** The budget is **1,000 writes per day**.
*Test:* if the write count scales with traffic rather than with deployments, it does not belong in
T2. One feature writing per request exhausts the daily budget before noon.

**T3 → nothing reconstructible from T1.** A course title, a series description or a harm's text
belongs in T1. Copying it into D1 for convenience creates two sources of truth and guarantees
drift. *Test:* if the value appears in a published file, D1 stores a reference, not a copy.

**T4 → no record of record.** *Test:* if deleting the browser's storage would lose something a
person cannot recover, T4 is holding a record it may not hold.

**T4's rule protects the reader rather than the system**, and it is the one most often violated by
well-meaning offline features. Browser storage is deletable by the browser, by a privacy sweep,
by a disk-cleanup utility, and by the person themselves without warning. A system keeping a
learner's only copy of an artefact there has silently made them custodian of a record they never
agreed to keep — which under [ML-2.3 §H.23](../license/ml-2-3.md) is custody without horizon,
imposed on the party least able to bear it.

---

## 3. Mechanism — the outbox pattern

The one non-obvious mechanism in the standard, and the one that makes T4's restriction survivable.

A learner submits an artefact while offline. The submission enters the **T4 outbox** with a local
id and a `pending` state. The interface shows it as *pending, not stored* — the wording matters,
because "saved" would be false. On reconnection the outbox drains to T3, the record acquires its
canonical id, and the outbox entry is deleted.

```
submit → T4 outbox (pending)  ──online──→  T3 (canonical)  ──→ outbox entry deleted
                │
                └── shown to the reader as "pending — not yet stored"
```

**Three properties are required and each is a failure mode if omitted.**

**Idempotent drain.** The local id is carried to T3 as a deduplication key, so a drain interrupted
mid-flight and retried does not create two records. Without it, a flaky connection produces
duplicate submissions and the learner is blamed.

**Honest state in the interface.** A pending item is never rendered as complete. This is the
[MX-023](../corpus/mx-023-attention-and-human-sovereignty.md) doctrine applied to a progress
indicator: showing a submission as saved because it is *probably* saved is a small false claim
made to avoid an awkward truth.

**Bounded outbox.** If the outbox exceeds its size or age limit, the interface says so and stops
accepting new offline submissions. A silently growing outbox is a T4 store that has become a
record of record by accident, which is precisely the boundary §2.1 draws.

---

## 4. The six databases

| Database | Holds | Publishable |
|---|---|---|
| `mx_identity` | Accounts, sessions, identity marks | No |
| `mx_learn` | Enrolment, progress, artefact submissions | No |
| `mx_credentials` | Issued credentials, revocations, review records | **Partly** — the public registry |
| `mx_commerce` | Orders, entitlements, referrals | No |
| `mx_academies` | Applications, charters, audit records | **Partly** — the directory |
| `mx_governance` | Determinations, defects, corrections, registry state | **In full** |

**Separated rather than unified, for three reasons that are governance reasons.** A breach of one
is not a breach of all. `mx_commerce` can be audited for riba compliance in isolation, which is
what makes the schema prohibition below checkable rather than aspirational. And `mx_governance`
holds no personal data **by construction**, which is what makes publishing it in full possible.

### 4.1 Identity marks are derived, never stored as images

A user's visual identity mark is generated deterministically from `SHA-256(usr_id + fixed_salt)`
and rendered as SVG at request time. **No image file is stored and no upload is accepted.**

This is a persistence rule with three consequences worth naming. There is no avatar-upload
pipeline, so no image moderation problem and no store of user-supplied binaries. The mark is
stable across devices without synchronisation, because it is a function rather than a record. And
the estate holds no photographs of anyone, which is the strongest privacy position available: a
record that does not exist cannot be breached, subpoenaed or leaked.

User ids are `usr_{ULID}` — sortable by creation time, non-sequential, non-guessable.

### 4.2 The riba prohibition, enforced in schema

`mx_commerce` contains **no** `interest_rate`, `late_fee` or `financing_partner` column.
`mx_commerce`'s referral tables additionally forbid six columns per
[ST-23 §3.3](st-23-affiliate-and-referral.md): `parent_referrer_id`, `recurring_period`,
`commission_schedule`, `tier`, `bonus_rate`, `negotiated_rate`, `clawback_until`,
`attribution_cookie`.

**Why schema and not policy.** A policy prohibition is enforced by whoever remembers it; a schema
prohibition is enforced by the database refusing to store the value. A future developer
implementing instalment interest — or a "small" tiered referral bonus — must first **alter the
schema**, which is a visible, reviewable, changelog-generating act. This is the estate's general
method for structural commitments: make the prohibited thing *unrepresentable* rather than merely
disallowed.

**The limit of the method, stated honestly.** A determined implementer can store interest in a
generically named column, or compute it in application code and store only the result. Schema
enforcement raises the cost of the prohibited act and makes it visible in review; it does not make
it impossible. It is a speed bump with a paper trail, and that is worth more than a policy
sentence and less than a proof.

---

## 5. The capacity meter

Published at `/about/status/capacity/`, computed at build time, **never typed**.

| Resource | Limit | 80% tripwire | Source of the figure |
|---|---|---|---|
| Pages files | 20,000 | 16,000 | Provider terms, 2026‑10‑01 |
| Workers requests | 100,000/day | 80,000/day | Provider terms, 2026‑10‑01 |
| KV writes | 1,000/day | 800/day | Provider terms, 2026‑10‑01 |
| KV reads | Per-plan | 80% | Provider terms, 2026‑10‑01 |
| D1 storage | Per-plan | 80% | Provider terms, 2026‑10‑01 |
| D1 rows read/day | Per-plan | 80% | Provider terms, 2026‑10‑01 |

**Every figure is dated, because every figure is perishable.** A capacity meter rendering
undated third-party limits is asserting as current something it learned once.

**Computed, never typed** — the same rule [SITE-02 §9](../site/page-contract.md) line 13 applies
to every number in the estate. A typed capacity figure is a claim with no falsifier, and a typed
figure that *understates* usage is the specific failure a capacity meter exists to prevent.

**The binding constraint is requests, not files.** The file ceiling was the estate's stated
capacity risk for a month and the arithmetic was aimed at the wrong resource: under directory
routing the estate plans ≈2,000 files against a 20,000 ceiling, leaving room for roughly 450
further series. [DEF‑2026‑041](../00-governance-map/defect-register.md#def-2026-041) stays open
under its original number, re-characterised rather than renumbered, so that the misdirection stays
visible in the record.

**Amber is public.** The meter shows its state to readers at the same moment as to the Curator. A
capacity meter visible only internally is a dashboard, not a disclosure, and the estate's
commitment under [MX-024 §4](../corpus/mx-024-infrastructure-and-migration.md) is that a capacity
decision affecting what readers receive is announced rather than absorbed.

---

## 6. Failure modes

**T2 used as a cache.** The most likely violation, because KV is fast and reads are cheap. Reads
are not the problem; the 1,000-write budget is, and a feature that writes on cache-miss scales
writes with traffic. §2.1's test catches it: does the write count scale with traffic or with
deployments?

**T3 mirroring T1 for convenience.** Copying course titles into D1 to simplify a query. Creates
two sources of truth and guarantees drift — the same *document-versus-artefact* divergence class
that produced nine corrections in this estate's own log.

**T4 promoted by accident.** An offline feature that works so well the outbox stops being drained
promptly, then a "resume where you left off" feature that reads from it, and then it is a record
of record with no one having decided so.

**The undrained outbox with no bound.** §3's third property omitted. Silent until a learner loses
work.

**Capacity figures aging quietly.** The subtlest failure here: the meter renders correctly, the
percentages compute, and the *limits* are eighteen months stale. This is why the standard is
`perishable` at a three-month interval and why every row in §5 carries a date.

---

## 7. Limits

**Class: technical.** Nothing in this standard has been built. No D1 database is provisioned, no
row exists, no outbox has drained. It is a specification, and specifications discover their errors
at load.

**Class: epistemic.** Six of the six figures in §5 are third-party terms that may have changed
since 2026‑10‑01. The estate cannot verify them without checking, and the standard's honesty
depends on the quarterly review actually running — which, given
[DEF-001](../00-governance-map/defect-register.md#def-001) (the build pipeline does not run), is
currently a commitment rather than a mechanism.

**Class: governance.** Schema enforcement (§4.2) raises the cost of a prohibited act and makes it
visible. It does not make it impossible, and this standard should not be cited as though it did.

**Class: economic.** The standard sets tripwires and cannot fund the responses to them. Whether
the estate can pay for the higher tier or the VPS at the moment amber fires is
[MX-024 §6](../corpus/mx-024-infrastructure-and-migration.md)'s open limit.

---

## 8. Falsifier

This standard is wrong if any of the following is observed:

1. **A value that belongs in no tier under §2** — showing the four-tier model incomplete rather
   than merely untested.
2. **T2 restricted to configuration proving insufficient for the estate's actual config needs**,
   forcing either request-time writes or a fifth store.
3. **The outbox pattern losing a submission in normal operation** — falsifying §3's three
   properties as sufficient.
4. **A capacity limit reached that appears in no row of §5.** The likeliest of the four: the
   estate can only meter limits it knows about, and the first unmetered ceiling will be discovered
   by hitting it.
5. **A published `mx_governance` export proving to contain personal data**, falsifying §4's
   by-construction claim.

---

## 9. Obligation

**For the build:** enforce §2's four boundary rules at review. Compute every capacity figure from
provider terms at build time and render its date. Never type a number.

**For the schema owner:** the forbidden columns of §4.2 are not a style preference. Adding one is
a specification change requiring a changelog line at
[`changelog.md`](../00-governance-map/changelog.md) and a reassessment under
[RB-05](../rubrics/rb-05-harm-review-gate.md), because both prohibitions implement licence-level
duties.

**For the reviewer:** re-verify all six figures in §5 quarterly against the provider's published
terms, and record the date even when nothing changed. A review that records no change is evidence
that someone looked; a missing review is indistinguishable from a stale figure.

**Under ML-2.3:** §C.9 (riba, enforced at §4.2), §H.10 (material cost), §H.11 (fragility and
dependency), §H.18 (consent integrity — §4.1's derived marks avoid a store of user images
entirely), §H.23 (custody without horizon — §2.1's T4 rule), §H.28 (custody and horizon).

---

**Related:** [MX-024 Infrastructure and Migration](../corpus/mx-024-infrastructure-and-migration.md) ·
[MX-021 Payments and Commerce](../corpus/mx-021-payments-and-commerce.md) ·
[MX-022 Identity and Sessions](../corpus/mx-022-identity-and-sessions.md) ·
[ST-19 Two-Plane Architecture](st-19-two-plane-architecture.md) ·
[ST-23 Affiliate and Referral](st-23-affiliate-and-referral.md) ·
[SITE-01 Route Manifest §8](../site/route-manifest.md) · [ML-2.3](../license/ml-2-3.md)

*Curated by Maher. Four tiers, six databases, six dated capacity figures and nine forbidden
columns — enforced by a database that refuses the value rather than by a policy someone has to
remember.*
