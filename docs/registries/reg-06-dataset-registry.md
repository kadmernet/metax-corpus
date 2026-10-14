---
doc_id: REG-06
title_en: Dataset Registry
title_ar: سجل مجموعات البيانات
family: registries
version: v2026.10.1
status: published
authority: record
prevailing_text: ar
audience_tier: 3
depth: meta
evidence_class: semi-durable
review_interval_months: 6
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [datasets, data, retention, registry, research-ethics]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. The estate holds no dataset about people and this register exists largely to record what is refused.
route: /registries/datasets/
---

# REG-06 — Dataset Registry

> **Authority note.** A **record**. Collection limits are set by
> [MX-014 research ethics](../corpus/mx-014-research-ethics-and-exclusions.md),
> [MX-023](../corpus/mx-023-attention-and-human-sovereignty.md) and
> [MX-022](../corpus/mx-022-identity-and-sessions.md); storage tiers by
> [MX-024](../corpus/mx-024-infrastructure-and-migration.md) and
> [ST-22](../standards/st-22-platform-and-persistence.md); retention by
> [MX-013](../corpus/mx-013-records-and-versioning.md). This page records holdings.

> **Disclosure first.** The estate holds **no dataset describing people**. Most of
> this register is therefore a record of **refusals** — data the estate could
> trivially collect, has decided not to, and lists so that a future decision to
> start would have to overturn a written commitment rather than fill a silence.
> Two datasets exist and both are about the corpus itself.

---

## 1. Position

Datasets are the point at which a documentation estate becomes a data controller,
and the transition is usually accidental: analytics enabled for one question,
retained forever; a form field added "in case"; a log kept because deleting logs
feels reckless.

The estate's position, stated once and applied everywhere below:

> **A dataset must be justified by a question that is written down before the
> collection starts, and must be destroyed when that question is answered or
> abandoned.**

This is the pre-registration requirement of
[MX-014 §4](../corpus/mx-014-research-ethics-and-exclusions.md), applied to
operational data and not merely to research. It is the single control that
prevents "we might need it" from becoming a retention policy.

## 2. Definition

A **dataset** is any structured, retained collection of records, satisfying **six**
recorded properties:

1. **Prior question** — the written question the dataset answers, dated **before**
   first collection.
2. **Subject class** — `corpus` (about documents) · `system` (about machines) ·
   `person` (about people, directly or by inference).
3. **Fields**, enumerated. Not "and other metadata".
4. **Retention** — a duration or a destruction condition. **Never "indefinite"**
   for subject class `person`.
5. **Storage tier**, per [MX-024](../corpus/mx-024-infrastructure-and-migration.md)'s
   four tiers.
6. **Destruction record** — where the fact of destruction will be written when it
   happens.

### 2.1 Forbidden fields

[ST-22](../standards/st-22-platform-and-persistence.md) names **nine** forbidden
schema columns and [ST-23](../standards/st-23-affiliate-and-referral.md) names
**six**. They are not repeated exhaustively here; the shape of the prohibition is:

| Forbidden category | Examples | Why |
|---|---|---|
| Cross-page reader identity | persistent visitor id, fingerprint hash | [MX-022](../corpus/mx-022-identity-and-sessions.md) — sessions are not identities |
| Engagement metrics per reader | time on page, scroll depth, return streak | [MX-023](../corpus/mx-023-attention-and-human-sovereignty.md) — these exist to optimise attention |
| Inferred attributes | interests, segment, propensity | Inference about a person is data about a person |
| Referral attribution chains | affiliate click ids, partner tokens | [ST-23](../standards/st-23-affiliate-and-referral.md) |
| Unbounded free text about a person | "notes" | No retention condition can bound it |

A forbidden field is forbidden **even if the data is never used**. Collection is
the harm, not analysis — this is the reasoning at
[HX stratum I](../harms/hx-000-the-fourteen-structural-harms.md) applied to the
estate's own conduct.

### 2.2 The `person` class is presumptive

If a dataset *could* be joined to a person by any party holding it, it is class
`person`, regardless of intent. IP addresses, session tokens, and timing patterns
are all class `person` under this test. The estate does not accept the argument
that data is anonymous because the estate does not personally intend to deanonymise
it.

## 3. Mechanism

### 3.1 Opening a dataset

```
question written + dated      →  [gate 1: does the question need records?]
subject class determined      →  [gate 2: is it class `person`?]
fields enumerated             →  [gate 3: any forbidden field? → refuse]
retention stated              →  [gate 4: `person` + indefinite → refuse]
storage tier assigned         →  MX-024 tiers 1..4
row written here              →  collection may begin
```

Collection before the row exists is prohibited. The row is not documentation of
collection; it is the **precondition** of it.

### 3.2 Destruction

Destruction is an **event with a record**, not a lapse. When a retention condition
is met:

1. the data is destroyed;
2. the row's state becomes `destroyed` with a date;
3. the fields list **remains** in the register.

Step 3 is the interesting one. The estate keeps the *schema* of destroyed
datasets forever, while destroying the *contents*. This preserves the accountable
fact of what was once collected — a destruction that also erases the record of
collection is indistinguishable from never having disclosed it.

### 3.3 The capacity interaction

[MX-024](../corpus/mx-024-infrastructure-and-migration.md) sets an **80% capacity
tripwire** across six databases. Datasets consume that capacity. A dataset with no
retention condition is therefore not merely an ethical problem but an
infrastructural one: it guarantees the tripwire will eventually fire, and the
migration path to a VPS will be forced by accumulated data nobody chose to keep.

## 4. Worked instance

**A refusal, worked through properly** — because the refusals are where this
register does its work.

A reasonable request: *"Which pages do readers actually read? We should know
whether the 1200-word floor helps or hurts."* This is a **good question**. It is
answerable. It would improve the corpus. Walk the gates:

| Gate | Result |
|---|---|
| 1. Question written, dated | Passes — the question above is legitimate and prior |
| 2. Subject class | `person` — per-page reading is joinable to a reader (§2.2) |
| 3. Forbidden fields | **Fails** — "time on page" and "scroll depth" are engagement metrics per reader |
| 4. Retention | Moot |

So the request is **refused at gate 3**, and the refusal costs the estate a real
answer to a real question. That cost is the point: the refusals in
[MX-023](../corpus/mx-023-attention-and-human-sovereignty.md) were not adopted on
the assumption they were free.

**What the estate does instead.** The same question can be approached without
reader data:

- Count words per page and publish the distribution — class `corpus`, no person
  involved. This is `DSET-002` below.
- Solicit **volunteered** written feedback, retained under a stated condition, with
  no linkage to browsing. Not currently collected.
- Reason from the document structure: if a page's eight ST-24 parts cannot be
  followed without the omitted sections, the page is too thin regardless of
  whether anyone read it.

The third substitute is weaker evidence — **E1** rather than the E3 that
instrumentation would give. The estate accepts weaker evidence as the price of the
refusal, and says so rather than pretending the substitutes are equivalent.

## 5. The register

Subject class: `corpus` · `system` · `person`. State: `open` · `closed` · `destroyed` · `refused`.

| ID | Prior question | Class | Fields | Retention | Tier | State |
|---|---|---|---|---|---|---|
| `DSET-001` | Which instruments exist, at which paths, in which state? | `corpus` | doc_id, path, family, version, status, authority, last_reviewed | Indefinite — permitted, no person | 1 | `open` |
| `DSET-002` | What is the word-count distribution across written pages, against the 1200 floor? | `corpus` | doc_id, word_count, exemption_claimed | Indefinite — permitted | 1 | `open` (**not yet populated**) |
| `DSET-R01` | Which pages do readers read, and for how long? | `person` | *(would require)* time_on_page, scroll_depth, visitor_id | — | — | **`refused`** at gate 3 |
| `DSET-R02` | Where does traffic come from? | `person` | referrer, campaign token, affiliate id | — | — | **`refused`** — [ST-23](../standards/st-23-affiliate-and-referral.md) forbidden columns |
| `DSET-R03` | Who are our readers? | `person` | inferred interests, segment | — | — | **`refused`** at gate 3; also [MX-014](../corpus/mx-014-research-ethics-and-exclusions.md) hard exclusion |
| `DSET-R04` | Which readers returned after a harm notice? | `person` | visitor_id, notice_id, return_flag | — | — | **`refused`** — the most tempting refusal, see §5.1 |

### 5.1 On `DSET-R04`

This is the refusal the estate finds hardest, and it is recorded at length because
a refusal nobody was tempted by proves nothing.

The question is *whether harm notices change behaviour*. That is arguably the most
important empirical question the estate could ask about its own licence — the
whole of [ML-2.3 Part H](../license/the-maher-license.md) rests on the premise
that disclosure does something. Answering it requires following individual readers
across a notice boundary, which is per-reader behavioural tracking, which is
exactly what stratum I harms describe.

So the estate holds an unfalsifiable premise rather than acquire the data that
would test it. That is a **genuine cost to the estate's own credibility**, and the
honest statement of position is: *we would rather our licence's central premise
remain E0 than instrument readers to promote it to E2.* A reader who thinks that
trade is wrong has found a real objection, and it is filed as `open` under
[ST-06 §4](../standards/st-06-objections-standard.md).

### 5.2 `DSET-002` is empty

The word-count dataset is opened and **not populated**. Populating it requires a
script; scripts are [ST-13 SENTINEL](../standards/st-13-static-build-and-sentinel.md)
territory; SENTINEL does not run ([DEF-001](../00-governance-map/defect-register.md)).
So the estate cannot currently state its own compliance with its own word floor —
see [REG-02 §5.3](reg-02-page-registry.md), where that gap forced the omission of a
percentage.

## 6. Failure modes

| # | Failure | Mechanism | Current state |
|---|---|---|---|
| F1 | **Collection before row** | Convenient default in a hosting platform enabled without review | **Live risk** — platform defaults are not audited |
| F2 | **Class misdeclaration** | Class `person` data filed as `system` because it is "just logs" | Prevented by §2.2's presumptive test; unaudited |
| F3 | **Indefinite retention creep** | No destruction event scheduled | Two `corpus` rows are indefinite; permitted |
| F4 | **Destruction without record** | Data deleted, disclosure deleted with it | Prevented by §3.2(3); never exercised |
| F5 | **Refusal erosion** | A refused dataset reopened under a new name | **Detectable only here** — the `DSET-R*` rows exist to make reopening visible |
| F6 | **Capacity-forced migration** | Unretained data fills six databases to the 80% tripwire | Not yet — holdings are tiny |
| F7 | **Substitute presented as equivalent** | E1 reasoning reported as if it were E3 measurement | **Live risk** — §4 names this explicitly |

## 7. Limits

1. **Platform defaults are unaudited.** The estate asserts it collects no reader
   data. It has **not** verified what its hosting layer logs by default. F1 is
   therefore not merely possible but *unchecked*, and this is the most likely place
   the register is currently wrong. Filed as a verification item.
2. **`DSET-002` cannot be populated** without a runner. Consequence: the word floor
   is an unmeasured obligation.
3. **The central licence premise is E0 by choice** (§5.1) and will remain so.
4. **No Arabic text**, while `prevailing_text: ar`.
5. **No destruction has ever occurred**, so §3.2 is entirely untested.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** any retained record about a reader exists anywhere in the estate's
>   systems — including hosting logs the estate did not configure;
> - **(b)** any dataset is collected whose row is absent from §5;
> - **(c)** a `DSET-R*` refused question is shown to be answered anywhere in the
>   estate's outputs, which would imply the data was obtained;
> - **(d)** `DSET-001`'s field list omits a field actually held.
>
> **(a) is the test the estate most expects to fail**, because it depends on
> platform behaviour nobody has inspected (§7.1). A reader with access to the
> hosting configuration could falsify this register in minutes, and the estate
> would rather that happen than continue asserting a clean posture it has not
> checked.

## 9. Obligation

None from the record. Bearing duties:

- Write the question before collecting — [MX-014 §4](../corpus/mx-014-research-ethics-and-exclusions.md).
- Treat joinable data as class `person` — §2.2, [MX-022](../corpus/mx-022-identity-and-sessions.md).
- Never collect a forbidden field, used or unused —
  [ST-22](../standards/st-22-platform-and-persistence.md),
  [ST-23](../standards/st-23-affiliate-and-referral.md).
- Destroy on condition, and keep the record of what was destroyed — §3.2.
- Do not present a substitute as equivalent evidence —
  [ST-07](../standards/st-07-evidence-and-verify.md).
- Audit the platform before asserting a clean collection posture — §7.1, owed.

---

### Related

**Collection limits** — [MX-014](../corpus/mx-014-research-ethics-and-exclusions.md) ·
[MX-022](../corpus/mx-022-identity-and-sessions.md) ·
[MX-023](../corpus/mx-023-attention-and-human-sovereignty.md) ·
[ST-23](../standards/st-23-affiliate-and-referral.md)

**Storage and capacity** — [MX-024](../corpus/mx-024-infrastructure-and-migration.md) ·
[ST-22](../standards/st-22-platform-and-persistence.md) ·
[ST-13](../standards/st-13-static-build-and-sentinel.md) ·
[MX-013](../corpus/mx-013-records-and-versioning.md)

**Evidence and objection** — [ST-07](../standards/st-07-evidence-and-verify.md) ·
[ST-04](../standards/st-04-falsifiability-and-claim-cards.md) ·
[ST-06](../standards/st-06-objections-standard.md) ·
[HX-002](../harms/hx-002-harm-instrument-map.md)

**Siblings** — [REG-02](reg-02-page-registry.md) ·
[REG-04](reg-04-media-registry.md) · [REG-05](reg-05-credential-registry.md)

### Exit pair

1. **Falsify §8(a).** Inspect the hosting layer's default logging. The estate has
   not, and says so.
2. **Read the refusal that costs most.** §5.1 and
   [MX-023](../corpus/mx-023-attention-and-human-sovereignty.md) — the estate
   declines to test its own licence's premise.

<!-- mx-pagestamp: REG-06 · v2026.10.1 · record · reviewed 2026-09-16 · next review 2027-03-16 -->
<!-- mx-demo: the published site is a demonstration; no dataset described here is served or queryable -->
