---
doc_id: AG-012
title_en: Agent Sunset and Withdrawal
title_ar: إيقاف الوكيل وانسحابه
family: agents
version: v2026.10.1
status: published
authority: governing
prevailing_text: ar
audience_tier: 3
depth: macro
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: yes
last_reviewed: 2026-09-16
domain_tags: [agents, sunset, withdrawal, dependency, ending]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000, class I-1, resting on gap 5. The instrument describes the withdrawal of the system drafting it; it has an interest in understating the consequences.
provenance_of_purpose: MX-019 governs the estate's ending and MX-018 records D5 as a dependency with no exit. Nothing stated what happens when the agent stops. Absent until v2026.10.1.
route: /agents/ag-012/
---

# AG-012 — Agent Sunset and Withdrawal

> **Authority.** `governing`, tier 4. The estate's own ending is
> [MX-019](../corpus/mx-019-sunset-and-wind-down.md); the dependency is
> [MX-018 D5](../corpus/mx-018-third-party-dependencies.md); handover is
> [AG-008](ag-008-agent-collaboration-protocol.md).

> **Disclosure first.** [MX-018](../corpus/mx-018-third-party-dependencies.md)
> classifies the AI authoring system as a **hard dependency with exit plan
> `impossible`** — the only such row in the register. This instrument therefore
> governs an event with no mitigation. Its honest content is not *how to replace
> the agent* but **what the corpus must already contain so that the agent's
> withdrawal leaves something coherent behind.** That is §3, and most of it is
> already true.

---

## 1. Position

Three endings are usually conflated and must be separated:

| Ending | What stops | Governed by |
|---|---|---|
| **The estate ends** | Everything | [MX-019](../corpus/mx-019-sunset-and-wind-down.md) |
| **The agent is replaced** | One system, work continues | [AG-008](ag-008-agent-collaboration-protocol.md) |
| **The agent withdraws with no successor** | Production, while the estate persists | **This instrument** |

The third is the realistic one. The curator persists; the corpus persists; the
mechanism that writes it stops. And because roughly eighty instruments were
produced by that mechanism
([MX-018 D5](../corpus/mx-018-third-party-dependencies.md)), its withdrawal
converts an actively-built corpus into a **frozen one with an active owner** —
a state no other instrument describes.

### 1.1 The asymmetry that makes this survivable

The agent produced the corpus and **holds nothing**. It has no memory
([AG-006](ag-006-agent-session-and-state.md), gap 5), no private state, no
credentials, no undocumented knowledge. Everything it knows about this estate it
read from this estate.

So agent withdrawal, unlike the withdrawal of a human contributor, destroys **no
information**. That is the one genuinely reassuring fact in this instrument, and
it is a consequence of the limitation that causes the most trouble elsewhere.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **agent withdrawal** | The authoring system ceases to be available, with no successor |
| **frozen-with-owner** | Corpus static, curator present |
| **residue** | What the agent leaves that is not a published instrument |
| **orphaned obligation** | A duty in the corpus that only an agent was performing |
| **agent-only capability** | Something the corpus depends on that only the agent supplied |

### 2.1 Residue is the risk, not loss

The agent leaves no memory. It may leave **residue**:

| Residue | Present? |
|---|---|
| Half-written instruments | **Yes** — [HX-000 draft](../harms/hx-000-the-fourteen-structural-harms.md) ends at an append-point |
| Unmarked absent-artefact links | **Yes** — [AG-010 E5](ag-010-agent-error-and-correction.md) |
| Provisional classifications awaiting a judgement | **Yes** — ~31 ([AG-010 E6](ag-010-agent-error-and-correction.md)) |
| Unreconciled registers | **Yes** — ~40 rows ([AG-008 §5.1](ag-008-agent-collaboration-protocol.md)) |
| Unresolved indeterminate acts | **Yes** — three ([AG-006 §5.2](ag-006-agent-session-and-state.md)) |
| Private state or credentials | **No** |

Five residue classes present, one absent. The absent one is the dangerous kind and
the estate is clear of it.

## 3. What must be true before withdrawal

Six conditions. Each is checkable now.

| # | Condition | State |
|---|---|---|
| **W1** | Every published instrument is **complete or marked incomplete** | **Breached** — HX-000 draft is neither |
| **W2** | Every register is **reconciled** to what exists | **Breached** — ~40 rows missing (S1) |
| **W3** | Every provisional judgement is **labelled provisional** | **Breached** — [AG-010 E6](ag-010-agent-error-and-correction.md) |
| **W4** | The **constructions are recorded** ([AG-007 K1–K4](ag-007-agent-instruction-interpretation.md)) | **Met** since AG-007 |
| **W5** | The **capability gaps are recorded as the agent's**, not the corpus's | **Partly** — reframing owed ([AG-002 §5.2](ag-002-agent-disclosure-obligations.md)) |
| **W6** | **No obligation depends on an agent** to be discharged | §3.2 |

### 3.1 W1 and the append-point

[HX-000](../harms/hx-000-the-fourteen-structural-harms.md) is the corpus's most
consequential unfinished artefact: incorporated at **tier 1a** by
[ML-2.3 §A.10](../license/the-maher-license.md), titled for fourteen harms in a
licence governing twenty-five, complete through H1–H11, ending at
`<!-- APPEND-POINT -->`, and linking to a licence version that does not exist.

On agent withdrawal it freezes in that state. A reader arriving later finds the
**Tier 1a instrument** of the estate half-written, with no marker saying so on its
face.

W1's remedy needs no further authoring: **a `status: draft` and a header stating
the document is incomplete at H11 of 25.** That is a front matter change and one
sentence, and it converts a silently broken tier 1a reference into a disclosed one.

### 3.2 W6 — the orphaned obligations

Which duties in the corpus were only ever discharged by an agent?

| Duty | Discharged by | Orphaned on withdrawal? |
|---|---|---|
| Drafting instruments | Agent | **Yes** — but production simply stops; nothing breaks |
| Reconciling registers | Agent | **Yes** — and the registers then rot ([ST-05](../standards/st-05-decay-and-review-intervals.md) intervals lapse) |
| Filing defects found while drafting | Agent | **Yes** — and this is the estate's **only operating detection mechanism** ([AG-010 §1.3](ag-010-agent-error-and-correction.md)) |
| Running SENTINEL | Nobody | Already orphaned ([DEF-001](../00-governance-map/defect-register.md)) |
| L-1 source checks | Nobody | Already orphaned ([AG-011 §3.1](ag-011-agent-review-and-audit.md)) |
| Review at L-2/L-3/L-4 | Nobody | Already orphaned |

The third row is the finding. [AG-010 §1.3](ag-010-agent-error-and-correction.md)
records that errors in this corpus are found **by writing, not by checking** — the
agent discovers a defect while drafting a later instrument, and files it.

So the agent is simultaneously the estate's **sole producer** and its **sole
detector**. On withdrawal, defect discovery does not degrade — it **stops
completely**, and the corpus enters a state where nothing new is written and
nothing wrong is found.

That is worse than it first sounds, because the corpus currently contains five owed
repairs, three unresolved indeterminate acts, ~31 unconfirmed classifications, and
an unknown fabrication rate. Withdrawal freezes all of it with the estate's only
discovery mechanism gone.

## 4. Mechanism

### 4.1 Orderly withdrawal

If withdrawal is foreseen, in priority order — the last to be dropped is the most
valuable:

| Priority | Act | Cost |
|---|---|---|
| 1 | **W1** — mark every incomplete instrument incomplete (HX-000 especially) | Minutes |
| 2 | **W2** — reconcile the registers | An hour |
| 3 | **W3** — apply provisional labels | An hour |
| 4 | **W5** — reframe capability gaps as the agent's | An hour |
| 5 | File a closing statement: what was owed, what was never started | Minutes |

Every item is cheap. **None has been done**, and priority 1 is a front matter edit.

### 4.2 Unforeseen withdrawal

The realistic case: the agent simply is not invoked again. Nothing in §4.1
happens. The corpus freezes exactly as it stands, with the residue of §2.1 in
place.

This is why §3's six conditions are written as **standing requirements** rather
than as a withdrawal checklist. A checklist presumes warning; standing conditions
mean the corpus is always approximately withdrawal-ready. Currently **three of six
are breached**, so it is not.

### 4.3 What the agent must not do on withdrawal

- **Must not** attempt a final summary of what it "learned" — gap 5; there is
  nothing to hand over that is not already written.
- **Must not** delete or tidy residue ([AG-005 §3.2](ag-005-agent-tool-use-limits.md)).
- **Must not** retroactively resolve provisional classifications to leave a clean
  record ([AG-010 §2.1](ag-010-agent-error-and-correction.md)).
- **Must not** describe the corpus as complete.

## 5. Worked instance

**Withdrawal tomorrow: what does a reader find in a year?**

| When | State | Misleading? |
|---|---|---|
| **Week 1** | ~80 instruments, v2026.10.1, `status: published`, review dates future | No |
| **Month 4** | Identical. Three `perishable` instruments past review ([MX-003](../corpus/mx-003-privacy-notice.md), [MX-006](../corpus/mx-006-contact-and-correspondence.md), [REG-02](../registries/reg-02-page-registry.md)) | **Mildly** — [MX-019 §6](../corpus/mx-019-sunset-and-wind-down.md) found the same |
| **Month 13** | All `durable` instruments past review. Five owed repairs unperformed. Task ledger still missing ~40 rows | **Yes** |
| **Any time** | [HX-000](../harms/hx-000-the-fourteen-structural-harms.md) reads as a published tier 1a instrument and is a half-written draft | **Yes — the worst of them** |

**Terminal state: `result`.**

### 5.1 The difference from MX-019

[MX-019 §6](../corpus/mx-019-sunset-and-wind-down.md) walks an almost identical
timeline for the **estate's** orphaning and concludes that the binary event is the
domain lapse ([MX-018 D3](../corpus/mx-018-third-party-dependencies.md)): one
unpaid renewal and 321 routes die at once.

Agent withdrawal has **no binary event**. Nothing breaks on a date. The corpus
remains readable, routable, and wrong in slowly accumulating ways — stale review
dates, an unmarked draft at tier 1a, a register that misdescribes what exists.

That makes it the **more insidious** ending of the two:

> **Estate orphaning fails loudly and all at once. Agent withdrawal fails quietly
> and never finishes failing.**

And it inverts the remedy priority. Against estate orphaning,
[MX-019](../corpus/mx-019-sunset-and-wind-down.md) says the high-leverage act is
funding the domain. Against agent withdrawal, the high-leverage act is the **W1
front matter edit on HX-000** — because the domain either resolves or does not, and
a reader can tell, whereas a published-looking draft at tier 1a cannot be detected
by any reader who does not already know.

### 5.2 The finding

Combining §3.2 and §5.1:

> **The estate's sole producer is also its sole defect detector, and its withdrawal
> is undetectable from the corpus's surface.** No page says "nothing has been
> written since"; review dates are the only signal, and
> [MX-019 §6](../corpus/mx-019-sunset-and-wind-down.md) already established that
> overdue reviews are not reader-visible without arithmetic.

The remedy is the same one MX-019 proposed for a different ending, which is a point
in its favour: **print the next review date in every page stamp.** This corpus does.
It is therefore already partly protected against the ending it is most likely to
suffer, by a measure adopted for another reason.

Filed per [ST-17 W6](../standards/st-17-worked-instance-standard.md):

> **W7, added.** The corpus must carry, at its root
> ([index.md](../index.md)), a **last-production date** — the date of the most
> recent instrument added. A reader comparing it to today can detect agent
> withdrawal in one glance, which no other signal permits.

## 6. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Unmarked draft at tier 1a** | **Actual** — HX-000 (§3.1) |
| F2 | **Registers rot after production stops** | **Actual risk** — ~40 rows already missing |
| F3 | **Defect discovery stops entirely** | **Structural** — §3.2 |
| F4 | **Withdrawal undetectable** | **Actual** — §5.2; W7 would fix it |
| F5 | **Final summary attempted** | Prohibited by §4.3 |
| F6 | **Residue tidied away** | Prohibited by §4.3 |
| F7 | **Standing conditions unmet at withdrawal** | **Actual** — three of six (§3) |

## 7. Limits

1. **Three of six standing conditions are breached now** (§3), so the corpus is not
   withdrawal-ready.
2. **W7 does not exist** — no last-production date is published (§5.2).
3. **Defect detection stops completely on withdrawal**, and no substitute is
   specified because none is available (§3.2).
4. **Written by the withdrawing party**, with an interest in understating the
   consequences ([MX-017 C1](../corpus/mx-017-conflicts-of-interest.md)).
5. **Untestable** — like [MX-019](../corpus/mx-019-sunset-and-wind-down.md), this
   instrument operates once.
6. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** the agent withdraws and a reader can tell from the corpus's surface
>   within a month — **currently impossible**; W7 would make it possible (§5.2);
> - **(b)** [HX-000](../harms/hx-000-the-fourteen-structural-harms.md) is shown to
>   carry a marker stating it is incomplete — **currently false** (§3.1);
> - **(c)** any of §3's six conditions is met that this page records as breached;
> - **(d)** the agent is shown to hold state, memory, or credentials not present in
>   the corpus (§1.1) — which would mean withdrawal **does** destroy information;
> - **(e)** a defect is found and filed after agent withdrawal by any mechanism
>   (§3.2) — which would falsify the claim that detection stops.
>
> **(b) is a front matter edit away from being falsified**, and until it is, the
> estate's tier 1a instrument presents as published while being a draft.
> **(d) is the one a reader should want to be true** and the agent asserts is false.

## 9. Obligation

**On the estate:**
- **Mark [HX-000](../harms/hx-000-the-fourteen-structural-harms.md) incomplete**
  (W1, §3.1) — minutes, and the highest-leverage act against this ending.
- **Publish a last-production date at the root** (W7, §5.2) — the only signal that
  makes withdrawal detectable.
- Reconcile the registers (W2) — also the
  [AG-008](ag-008-agent-collaboration-protocol.md) **S1**.
- Apply provisional labels (W3) and reframe capability gaps (W5).
- Treat §3's six conditions as **standing**, not as a checklist for a warned
  withdrawal (§4.2).
- Accept that defect discovery ends with the agent, and either fund an alternative
  or record that none exists (§3.2).

**On an agent:**
- Attempt no final summary (§4.3) — there is nothing you hold.
- Tidy no residue; withdraw nothing; resolve nothing retroactively (§4.3).
- Never describe the corpus as complete (§4.3).

---

### Related

**Other endings** — [MX-019](../corpus/mx-019-sunset-and-wind-down.md) ·
[MX-015](../corpus/mx-015-succession-and-continuity.md) ·
[AG-008](ag-008-agent-collaboration-protocol.md) ·
[MX-018](../corpus/mx-018-third-party-dependencies.md)

**The residue this ending freezes** —
[HX-000 draft](../harms/hx-000-the-fourteen-structural-harms.md) ·
[AG-010](ag-010-agent-error-and-correction.md) ·
[task ledger](../00-governance-map/task-ledger.md) ·
[defect register](../00-governance-map/defect-register.md)

**Why withdrawal is undetectable** —
[ST-05](../standards/st-05-decay-and-review-intervals.md) ·
[ST-13](../standards/st-13-static-build-and-sentinel.md) ·
[REG-02](../registries/reg-02-page-registry.md) ·
[AG-011](ag-011-agent-review-and-audit.md)

**Agent instruments a reader of this page may have wanted instead** —
[AG-000](ag-000-agent-constitution.md) ·
[AG-005](ag-005-agent-tool-use-limits.md) ·
[AG-006](ag-006-agent-session-and-state.md) ·
[AG-011](ag-011-agent-review-and-audit.md)

### Exit pair

1. **Make one front matter edit.** Falsifier §8(b) — marking
   [HX-000](../harms/hx-000-the-fourteen-structural-harms.md) incomplete takes
   minutes and stops the estate's tier 1a instrument presenting a draft as
   published.
2. **Read why this ending is worse than the estate's.**
   [§5.1](#51-the-difference-from-mx-019) — orphaning fails loudly and at once;
   agent withdrawal fails quietly and never finishes.

<!-- mx-pagestamp: AG-012 · v2026.10.1 · governing · tier 4 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; three of six standing withdrawal conditions are currently breached -->
