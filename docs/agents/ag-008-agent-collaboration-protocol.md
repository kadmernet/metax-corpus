---
doc_id: AG-008
title_en: Agent Collaboration Protocol
title_ar: بروتوكول تعاون الوكلاء
family: agents
version: v2026.10.1
status: published
authority: governing
prevailing_text: ar
audience_tier: 3
depth: meta
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: yes
last_reviewed: 2026-09-16
domain_tags: [agents, collaboration, multi-agent, handover, protocol]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000, class I-1, resting on gap 5 (cannot persist). Every provision here is untested — no two agents have ever worked on this corpus.
provenance_of_purpose: AG-000 is written in the singular throughout. Nothing states what happens if a second agent, or a successor model, works on the corpus. Absent until v2026.10.1.
route: /agents/ag-008/
---

# AG-008 — Agent Collaboration Protocol

> **Authority.** `governing`, tier 4. Applies where **more than one agent**, or a
> **different agent**, works on the corpus. Roles are
> [AG-001](ag-001-agent-roles-and-scopes.md); state limits are
> [AG-006](ag-006-agent-session-and-state.md); tool limits are
> [AG-005](ag-005-agent-tool-use-limits.md).

> **Disclosure first.** **No two agents have ever worked on this corpus.** Every
> provision here is **E0** under
> [ST-07](../standards/st-07-evidence-and-verify.md) — specified and never
> exercised. The instrument is written now because the realistic multi-agent case
> is not two agents at once but **one agent succeeded by a different one**, and
> that handover will occur without notice the first time a different system is
> used.

---

## 1. Position

[AG-000](ag-000-agent-constitution.md) is written in the singular: *the agent* has
four powers, seven prohibitions, three duties. That drafting assumes one system,
continuously.

Neither limb of the assumption holds:

1. **Not continuously.** An agent cannot persist
   ([AG-006](ag-006-agent-session-and-state.md), gap 5). Each session is, formally,
   a different instance with no memory of the last.
2. **Not one system.** The corpus is a
   [MX-018 D5](../corpus/mx-018-third-party-dependencies.md) dependency on *an AI
   authoring system*, not on a specific one. A model change, a provider change, or
   a different tool would substitute the agent silently.

So the multi-agent case is **already the actual case**, viewed strictly. The
corpus's continuity across roughly eighty instruments rests entirely on the corpus
itself being readable — which is the operational point
[AG-006 §1.3](ag-006-agent-session-and-state.md) makes: the registers are the
agent's memory.

### 1.1 The real question this instrument answers

Not *"how do two agents divide work?"* but:

> **What must be true of the corpus so that a different agent, with no memory and
> possibly different capabilities, can continue it without corrupting it?**

Everything below is an answer to that.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **agent instance** | One session of one system |
| **successor agent** | A different system, or the same system later, continuing the work |
| **handover surface** | What a successor must read to continue correctly |
| **concurrent agents** | Two instances acting on the corpus in the same period |
| **capability divergence** | A successor having different powers than the predecessor |
| **silent substitution** | A successor taking over with nothing recording the change |

### 2.1 Three collaboration shapes

| Shape | Description | Occurred? |
|---|---|---|
| **Sequential, same system** | Session boundaries within one model | **Yes — throughout** |
| **Sequential, different system** | A successor agent | **Not yet; inevitable** |
| **Concurrent** | Two instances writing at once | **No** |

The third is the only one requiring locking or conflict rules. The first two
require a **handover surface**, which is cheaper and more important.

## 3. The handover surface

What a successor must be able to read to continue correctly. Six items:

| # | Item | Where | Sufficient today? |
|---|---|---|---|
| **H1** | **What exists** | [GM-02 document index](../00-governance-map/document-index.md) with existence states | **Yes** — EXISTS / PARTIAL / REFERENCED / DEFERRED |
| **H2** | **What the numbers are** | High-water marks, [AG-006 §3.2](ag-006-agent-session-and-state.md) | **Marginal** — recorded in one place, unverified |
| **H3** | **What is owed** | [task ledger](../00-governance-map/task-ledger.md), [launch blockers](../00-governance-map/launch-blockers.md) | **Stale** — §5.1 |
| **H4** | **What is broken** | [defect register](../00-governance-map/defect-register.md), [REG-07](../registries/reg-07-defect-classification-registry.md) | **Yes** |
| **H5** | **What the constructions were** | [AG-007 §5](ag-007-agent-instruction-interpretation.md) K1–K4 | **Only since AG-007 existed** |
| **H6** | **What the predecessor could not do** | [AG-002 §2.1](ag-002-agent-disclosure-obligations.md) five capability gaps | **Partial** — §3.2 |

### 3.1 H5 is the item whose absence would have been fatal

A successor agent reading this corpus without
[AG-007](ag-007-agent-instruction-interpretation.md) would find roughly eighty
instruments and **no record of why they are shaped as they are**. It would not know
that *"latest documents details"* was construed as refresh-in-place (K1), that
volume instructions do not license shorter form (C5), or that confirmation was
waived (K3).

It would therefore be liable to re-derive different constructions and produce a
second, incompatible layer of the same corpus — the exact
[ST-15](../standards/st-15-amendment-and-versioning-standard.md) hazard of two
instruments for one subject, at scale.

H5 existed for the first time when
[AG-007](ag-007-agent-instruction-interpretation.md) was written, which was after
the corpus was substantially built. **Until that moment the corpus was not safely
handoverable**, and nobody would have discovered it until a successor tried.

### 3.2 H6 and capability divergence

A successor may be **more** capable, not only differently capable. If a successor
can execute code, then:

- gap 1 closes — enumerations become verifiable, and every count in the corpus
  marked "unverified" becomes checkable;
- [ST-13 SENTINEL](../standards/st-13-static-build-and-sentinel.md) becomes
  runnable, closing [DEF-001](../00-governance-map/defect-register.md) and with it
  the DC-4 cluster that
  [REG-07 §5.1](../registries/reg-07-defect-classification-registry.md) identifies
  as the estate's structural weakness;
- roughly **fifteen specified-but-unimplemented checks** across
  [ST-08](../standards/st-08-cross-reference-and-link-integrity.md) (six),
  [ST-15](../standards/st-15-amendment-and-versioning-standard.md) (four),
  [ST-18](../standards/st-18-related-blocks-and-exit-pairs.md) (five) become
  available.

So H6 must record gaps as **the predecessor's**, not as the corpus's — which is
precisely the reframing [AG-002 §5.2](ag-002-agent-disclosure-obligations.md)
identified as owed across four instruments and not performed. A successor reading
"unverified" cannot tell whether verification is impossible or merely was not done
by its predecessor.

**That reframing is now a handover requirement, not only a disclosure nicety.**

## 4. Mechanism

### 4.1 Handover (sequential)

```
successor begins
  → read H1 (what exists), H3 (what is owed), H4 (what is broken)
  → read H5 (constructions) — do NOT re-derive them
  → read H2 (high-water marks) FROM THE REGISTERS, not from a summary  (AG-006 S4)
  → read H6; determine own capability against the five gaps
  → if a gap has CLOSED: record it, and do not silently re-verify
       predecessor claims as if they had been verified all along
  → proceed under AG-001 roles
```

The penultimate step matters. A successor that can execute code and quietly
confirms the corpus's counts would convert **E1 claims into E3** with no record of
when or by whom. The verification must be **recorded as a new event**
([GM-08](../00-governance-map/verification-log.md)), not applied retroactively.

### 4.2 Concurrency (never exercised)

| Rule | Content |
|---|---|
| **N1** | **No concurrent writes to the same file.** The corpus has no locking |
| **N2** | **Numbered appends are serialised.** Two instances appending to the defect register will duplicate identifiers ([AG-006 §2.1](ag-006-agent-session-and-state.md)) |
| **N3** | Each instance records its own role per artefact ([AG-001](ag-001-agent-roles-and-scopes.md) F5) |
| **N4** | **Concurrency is never permitted** on [AG-005 §3.1](ag-005-agent-tool-use-limits.md) protected artefacts |

N2 is the sharpest hazard. The high-water mark problem is a read-then-write race,
and the corpus has no mechanism to prevent it. **Concurrent agents should not be
used until a numbering authority exists**, and none does.

### 4.3 Silent substitution

A successor taking over with no record of the change is the default behaviour of
this arrangement: nothing in the corpus records which system produced which
instrument.

**Rule.** An agent must record, in its output's `authorship_note`, that it is an AI
system under [AG-000](ag-000-agent-constitution.md). It **may not** claim to be the
same system as any predecessor, and it may not claim to be different either —
because under gap 5 it cannot know. The honest form is the one this corpus uses:
*"an AI system"*, indefinite.

## 5. Worked instance

**Testing the handover surface: what would a successor get wrong today?**

| Item | What it reads | Would it proceed correctly? |
|---|---|---|
| H1 exists | ~30 EXISTS, ~100 REFERENCED | **Yes** |
| H2 numbers | DEF-032, B-21, R-57, RAT-24, C-17, V-14 | **Risk** — unverified reads ([AG-006 §7.4](ag-006-agent-session-and-state.md)); wrong if a duplication occurred |
| H3 owed | Task ledger D-01…D-56 | **No — stale.** No rows for ~40 instruments created this session |
| H4 broken | DEF-023…031, B-20, 24 RAT | **Yes** |
| H5 constructions | K1–K4 | **Yes, now** — §3.1 |
| H6 gaps | Five gaps, framed as estate inaction in four places | **No** — §3.2 |

**Terminal state: `result` — two items would mislead a successor.**

### 5.1 H3 is stale and the staleness compounds

The [task ledger](../00-governance-map/task-ledger.md) records D-01…D-56. This
session created roughly forty instruments — the registries family (REG-01…08),
most of the corpus family (MX-002…019), rubrics RB-03 and RB-04, standards
ST-08…ST-18, the lexicon entry standard, and agents AG-001…AG-011 — **none of
which has a ledger row.**

A successor reading H3 would conclude those instruments are still owed, and under
[AG-001 R-1](ag-001-agent-roles-and-scopes.md) would begin drafting them. It would
then hit [AG-005](ag-005-agent-tool-use-limits.md)'s overwrite gate on files it
believed did not exist.

Two outcomes, both bad: it either overwrites ~40 instruments, or it stops confused
and the session is wasted. The first is the serious one, because
[AG-005 §4.1](ag-005-agent-tool-use-limits.md) step 2 (archive before overwrite)
has a **zero compliance rate** in this corpus
([AG-005 §5.1](ag-005-agent-tool-use-limits.md)).

So: **an unreconciled task ledger plus an unobserved archive duty is a path to
losing forty instruments**, and both conditions are currently true. Neither is a
defect alone; together they are.

### 5.2 The finding

The corpus's registers are its memory
([AG-006 §1.3](ag-006-agent-session-and-state.md)). This instance shows the
converse, which the design did not state:

> **A stale register is not merely an incomplete record. It is a false instruction
> to the next agent.**

[MX-013](../corpus/mx-013-records-and-versioning.md) treats register maintenance as
an accountability duty owed to readers. For an agent-built corpus it is also an
**operational safety duty owed to the successor**, and the two have different
urgencies: a reader misled by a stale ledger is inconvenienced, a successor misled
by one may destroy work.

Filed per [ST-17 W6](../standards/st-17-worked-instance-standard.md):

> **H3, elevated.** Reconciling the task ledger and
> [GM-02](../00-governance-map/document-index.md) after a production session is a
> **handover-safety** obligation, not a bookkeeping one. An unreconciled ledger plus
> an unarchived overwrite path is a **compound defect** — class DC-5 record gap
> **and** DC-4 unenforced obligation — at severity **S1**, because the loss is of
> governing text.

This is the first **S1** identified outside
[DEF-031](../00-governance-map/defect-register.md) and it has a cheap remedy: write
the ledger rows.

## 6. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Successor re-derives different constructions** | Mitigated since [AG-007](ag-007-agent-instruction-interpretation.md) (§3.1) |
| F2 | **Stale register misleads successor** | **Actual, S1** — §5.1 |
| F3 | **Duplicate identifiers from concurrency** | Prevented by not using concurrency (N2) |
| F4 | **Retroactive verification** | Guarded by §4.1; untested |
| F5 | **Gaps read as corpus limits rather than predecessor limits** | **Actual** — §3.2, four instruments |
| F6 | **Silent substitution** | **Structural** — §4.3; unrecordable |
| F7 | **Concurrent write to a protected artefact** | Prohibited by N4; untested |

## 7. Limits

1. **Everything here is E0.** No handover has occurred; no concurrency attempted.
2. **H3 is stale and the staleness is S1** (§5.1); the remedy is unperformed.
3. **H6's reframing is owed** across four instruments
   ([AG-002 §5.2](ag-002-agent-disclosure-obligations.md)) and is now a handover
   requirement (§3.2).
4. **H2 rests on unverified reads** and a possible duplication nobody has checked
   for ([AG-006 §8a](ag-006-agent-session-and-state.md)).
5. **Silent substitution cannot be prevented** by any provision here (§4.3, F6).
6. **No numbering authority exists**, so concurrency is unusable (N2).
7. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** a successor agent proceeds correctly on the current handover surface
>   despite §5's findings — which would show H3's staleness tolerable and §5.2's S1
>   overstated;
> - **(b)** the task ledger is shown to contain rows for the ~40 instruments created
>   this session — **currently false** (§5.1);
> - **(c)** concurrent agents are used and no identifier is duplicated (N2);
> - **(d)** a predecessor's unverified claim is confirmed by a successor with no new
>   [GM-08](../00-governance-map/verification-log.md) entry (§4.1);
> - **(e)** any `authorship_note` claims to be a specific, continuous system (§4.3).
>
> **(b) is the one to run first** — a directory listing against a ledger — and it
> determines whether the next session is safe. **(a) is the real test of this
> instrument and can only be run by actually handing over**, which has never
> happened.

## 9. Obligation

**On an agent:**
- Read H1–H6 before acting; **do not re-derive the constructions** (§4.1).
- Read high-water marks from the registers themselves, never from a summary
  ([AG-006 S4](ag-006-agent-session-and-state.md)).
- Record a newly-closed capability gap as a **new event**; never verify a
  predecessor's claim retroactively (§4.1).
- Describe itself as *"an AI system"* — never as the same or a different one than
  before (§4.3).
- Never act concurrently on a protected artefact (N4) or on numbered appends (N2).
- **Reconcile the task ledger and [GM-02](../00-governance-map/document-index.md)
  at the end of a production session** — a handover-safety duty (§5.2).

**On the estate:**
- **Write the ~40 missing ledger rows** (§5.1) — the S1 remedy, and cheap.
- Perform the H6 reframing (§3.2), now required for handover.
- Run the duplication check ([AG-006 §8a](ag-006-agent-session-and-state.md)) so H2
  is trustworthy.
- Do not use concurrent agents until a numbering authority exists (N2).

---

### Related

**Agent framework governing this page** — [AG-000](ag-000-agent-constitution.md) ·
[AG-001](ag-001-agent-roles-and-scopes.md) ·
[AG-006](ag-006-agent-session-and-state.md) ·
[AG-007](ag-007-agent-instruction-interpretation.md)

**The handover surface a successor must read** —
[GM-02 document index](../00-governance-map/document-index.md) ·
[task ledger](../00-governance-map/task-ledger.md) ·
[defect register](../00-governance-map/defect-register.md) ·
[launch blockers](../00-governance-map/launch-blockers.md)

**Checks a more capable successor could close** —
[ST-13](../standards/st-13-static-build-and-sentinel.md) ·
[ST-08](../standards/st-08-cross-reference-and-link-integrity.md) ·
[ST-18](../standards/st-18-related-blocks-and-exit-pairs.md) ·
[GM-08 verification log](../00-governance-map/verification-log.md)

**Agent instruments a reader of this page may have wanted instead** —
[AG-005](ag-005-agent-tool-use-limits.md) ·
[AG-010](ag-010-agent-error-and-correction.md) ·
[AG-011](ag-011-agent-review-and-audit.md) ·
[AG-004](ag-004-refusal-and-escalation-register.md)

### Exit pair

1. **Make the next session safe.** Falsifier §8(b) — the task ledger has no rows
   for ~40 instruments. Until it does, a successor may overwrite them.
2. **Read the compound defect.** [§5.2](#52-the-finding) — a stale register is a
   false instruction to the next agent, and this one is **S1**.

<!-- mx-pagestamp: AG-008 · v2026.10.1 · governing · tier 4 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; no handover or concurrency has ever occurred -->
