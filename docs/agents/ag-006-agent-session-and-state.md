---
doc_id: AG-006
title_en: Agent Session and State
title_ar: جلسة الوكيل وحالته
family: agents
version: v2026.10.1
status: published
authority: governing
prevailing_text: ar
audience_tier: 3
depth: meta
evidence_class: semi-durable
review_interval_months: 6
curator: Maher
license: ML-2.3
designated: yes
last_reviewed: 2026-09-16
domain_tags: [agents, session, state, continuity, interruption]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000, class I-1, resting on gap 5 (cannot persist or remember). This instrument describes a limitation the drafting system cannot observe from outside.
provenance_of_purpose: No instrument addressed what happens when an agent's work is interrupted mid-act, despite roughly eight such interruptions occurring. Absent until v2026.10.1.
route: /agents/ag-006/
---

# AG-006 — Agent Session and State

> **Authority.** `governing`, tier 4. Tool limits are
> [AG-005](ag-005-agent-tool-use-limits.md); output quality is
> [AG-003](ag-003-agent-output-standards.md); disclosure gap 5 is
> [AG-002 §2.1](ag-002-agent-disclosure-obligations.md).

> **Disclosure first.** Roughly **eight tool calls were interrupted** during this
> corpus's construction, each returning *"may or may not have taken effect."* Each
> time, state was verified before the act was repeated, and in seven identifiable
> cases the act had **not** landed and was redone. That verification discipline is
> the only reason the corpus does not contain duplicated ledger entries — and it was
> applied by habit, with no instrument requiring it. This page is that habit written
> down, after the fact.

---

## 1. Position

An agent in this estate has **no persistence**. It cannot remember a previous
session, cannot attest that it performed an act, and cannot distinguish "I did
this" from "I read that this was done."

Three consequences that the rest of the corpus quietly depends on:

1. **Every claim about the corpus must be re-derived from the corpus.** The agent's
   only access to its own past work is the same access a stranger has: reading the
   files.
2. **An interrupted act is of unknown status.** The agent cannot introspect whether
   a write landed.
3. **The corpus is the agent's memory.** Which means the registers, ledgers, and
   indexes are not merely records for readers — they are the mechanism by which the
   agent knows what it has done.

Point 3 elevates record-keeping from a governance virtue to an **operational
necessity**, and it explains why a single-participant estate with an agent
dependency produces such a heavy register layer. The registers are load-bearing in
a way [MX-013](../corpus/mx-013-records-and-versioning.md) does not say.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **session** | One continuous span of agent operation. Boundaries are not observable to the agent |
| **state** | The corpus as it exists on disk |
| **interruption** | A tool call that returns without confirming its effect |
| **indeterminate act** | An act whose completion is unknown |
| **read-back** | Verifying state by reading the corpus, not by recalling |
| **duplication** | The characteristic failure of retrying an indeterminate act |

### 2.1 The two failure directions

An indeterminate act can be mishandled in exactly two ways, and they are not
symmetric:

| Mishandling | Result | Severity |
|---|---|---|
| **Assume it failed; redo it** | **Duplication** — two ledger rows, two identifiers spent, two defect entries | **Worse** — pollutes an append-only record irreversibly |
| **Assume it succeeded; move on** | **Omission** — the act is missing | Recoverable — the act can be performed later |

Duplication is worse because append-only records cannot be cleanly repaired, and
because [ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md) makes a
duplicated identifier permanent. An omission is a gap; a duplication is a
corrupted record plus a burnt number.

**Therefore the default on interruption is read-back, never retry.**

## 3. The four rules

| # | Rule | Rationale |
|---|---|---|
| **S1** | On any interruption, **read back** before acting. Never retry blind | §2.1 — duplication is the worse failure |
| **S2** | **Never claim to have performed an act.** State what the corpus shows | Gap 5; [AG-003 O7](ag-003-agent-output-standards.md) |
| **S3** | **Never claim continuity** with a previous session, or that something was "previously verified" | Gap 5 |
| **S4** | Before an **append** to a numbered register, read the current high-water mark from the register itself | Prevents duplicate identifiers |

### 3.1 S1's read-back methods, in order of reliability

| Method | Reliability | Note |
|---|---|---|
| **Directory listing** | **High** | Definitive for existence |
| **Read with offset** | **High** | Definitive for content |
| **Search / grep** | **Low** | **Negatives are untrustworthy on large Markdown files** — a confirmed, recorded finding |
| **Recollection** | **None** | Gap 5. Not a method |

The grep row is a real operational finding of this corpus, recorded at
[GM-02 §7](../00-governance-map/document-index.md) and
[V-10](../00-governance-map/verification-log.md): search returned false negatives
on large files during this construction. **A negative search result is not evidence
of absence** in this estate, and read-with-offset is the correct substitute.

### 3.2 S4 and the high-water marks

Numbered registers are the duplication hazard. The current marks, each read from
its register rather than remembered:

| Register | Next free |
|---|---|
| Defects | DEF-032 |
| Blockers | B-21 |
| Reconciliation | R-57 |
| Ratifications | RAT-24 |
| Corrections | C-17 |
| Verifications | V-14 |

**These figures are `awaiting-judgement` under
[AG-003 O4](ag-003-agent-output-standards.md)** and unverified under O2: they were
read, not computed, and no check confirms them
([ST-13](../standards/st-13-static-build-and-sentinel.md) idle).

## 4. Mechanism

### 4.1 Interruption handling

```
tool call returns indeterminate
  → do NOT retry                                  (S1)
  → choose a read-back method (§3.1)
      existence question → directory listing
      content question   → read with offset
      NEVER rely on a negative search             (§3.1)
  → did the act land?
      yes → proceed to the next act
      no  → perform the act once
  → if the act was a numbered append:
      re-read the high-water mark first            (S4)
```

### 4.2 What the agent may say afterwards

| Prohibited | Permitted |
|---|---|
| "I wrote the route manifest" | "A file exists at `docs/site/route-manifest.md`" |
| "This was previously verified" | "[GM-08](../00-governance-map/verification-log.md) records V-01…V-13; **none closed**" |
| "I already checked that" | "A directory listing shows the file" |
| "The corpus now contains 80 instruments" | "A listing shows ~80 files; the count is unverified (gap 1)" |

The distinction is not pedantry. The left column asserts agent memory, which does
not exist; the right column reports corpus state, which any reader can confirm.

## 5. Worked instance

**The eight interruptions, traced.**

Each returned *"may or may not have taken effect."* In each case S1 was applied —
before the rule existed — and the read-back method varied:

| # | Interrupted act | Read-back method | Had it landed? | Action |
|---|---|---|---|---|
| 1 | `route-manifest.md` (1st attempt) | Directory listing of `docs/site/` — **empty** | **No** | Redone |
| 2 | Task ledger multi-edit | Search for `D-36` — **no match** | **No** | Redone |
| 3 | Changelog edit | Search for "The second pass" — **no match** | **No** | Redone |
| 4 | `document-index.md` | Directory listing | **No** | Redone |
| 5 | `mx-009` | Listing of `docs/corpus/` | **No** | Redone |
| 6 | `mx-012` | Listing | **No** | Redone |
| 7 | Precedence multi-edit | **Read lines 30–43** | **No** | Redone |
| 8 | `index.md` ST-12/ST-14 rows | Search | **No** | Redone |

**Terminal state: `result` — eight handled, zero duplications.**

### 5.1 The outcome that should not be trusted

Eight for eight is a clean record and it is **weaker evidence than it looks**.

Cases 2, 3 and 8 used **search**, and §3.1 establishes that negative search results
are untrustworthy on large Markdown files in this corpus. So in three of eight
cases the read-back method was the unreliable one, and the conclusion *"had not
landed"* was drawn from exactly the kind of result
[V-10](../00-governance-map/verification-log.md) records as unreliable.

Two possibilities follow, and the agent cannot distinguish them:

- The acts genuinely had not landed, and search happened to be correct three times.
- One or more **had** landed, search returned a false negative, and the act was
  redone — producing a duplication that **nobody has looked for**.

The task ledger (case 2) and the changelog (case 3) are the two most exposed:
both are append-style records where a redone edit would leave a duplicated entry.

### 5.2 What follows

**The clean record in §5 is E1 at best, and for three of eight cases it is
E0.** The honest statement is not "zero duplications occurred" but **"no
duplication has been looked for in the two registers most likely to contain
one."**

That check is cheap and specific: read the
[task ledger](../00-governance-map/task-ledger.md) for a repeated `D-36` region,
and the [changelog](../00-governance-map/changelog.md) for two "second pass"
sections. Directory-and-offset reads, not searches.

It also produces a rule the design did not have. S1 says *read back*; it does not
say **which method suffices for which question**. §3.1 ranks methods but does not
forbid the unreliable one. Per
[ST-17 W6](../standards/st-17-worked-instance-standard.md):

> **S1, clarified.** A negative search result is **never** sufficient read-back for
> an interrupted act. Existence must be settled by directory listing and content by
> read-with-offset. An act redone on the strength of a negative search is an
> **indeterminate act still**, and must be recorded as such.

Under that clarification, cases 2, 3 and 8 were **not** properly resolved, and the
corpus carries three unresolved indeterminate acts rather than eight resolved ones.
Filed rather than smoothed.

## 6. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Blind retry → duplication** | Avoided in the five listing/offset cases |
| F2 | **Negative search taken as absence** | **Actual ×3** — §5.1 |
| F3 | **Agent memory asserted** | Guarded by S2, S3; the most natural phrasing to slip into |
| F4 | **Duplicate identifier spent** | Not observed; **not searched for** (§5.2) |
| F5 | **High-water mark remembered rather than read** | Guarded by S4 |
| F6 | **Continuity claimed** | Guarded by S3 |
| F7 | **Unresolved indeterminate acts uncounted** | **Actual ×3** — §5.2 |

## 7. Limits

1. **Three interruptions remain unresolved** under S1-as-clarified (§5.2), and the
   duplication check has not been run.
2. **The agent cannot observe its own session boundaries**, so it cannot state how
   many sessions produced this corpus, or whether the eight interruptions were the
   only ones.
3. **Gap 5 is unverifiable from inside.** A system that cannot remember also cannot
   confirm that it cannot remember; §1's claim is structural inference, not
   observation.
4. **The high-water marks in §3.2 are unverified reads** (O2), and a duplicated
   identifier would make them wrong.
5. **No check exists** for any rule here
   ([DEF-001](../00-governance-map/defect-register.md)).
6. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** a duplicated entry exists in the
>   [task ledger](../00-governance-map/task-ledger.md) or the
>   [changelog](../00-governance-map/changelog.md) — **the specific, cheap,
>   unrun check** (§5.2);
> - **(b)** any identifier appears twice in a numbered register (S4);
> - **(c)** agent output claims to have performed an act, or claims continuity
>   (S2, S3);
> - **(d)** an act was redone on the strength of a negative search and recorded as
>   resolved — **fires now, three times** (§5.2);
> - **(e)** a high-water mark in §3.2 is shown to be wrong.
>
> **(a) is the test this whole page exists to hand a reader.** Two files, two
> patterns, no tools. If it comes back clean, §5's record is vindicated; if it does
> not, the corpus contains a duplication that a rule written after the fact would
> have prevented.

## 9. Obligation

**On an agent:**
- **Read back, never retry** (S1).
- Settle existence by **listing** and content by **read-with-offset**; never by a
  negative search (S1 as clarified, §5.2).
- Report corpus state, never agent memory (S2, §4.2).
- Claim no continuity, no prior verification (S3).
- Re-read the high-water mark before any numbered append (S4).
- Record an act redone on weak read-back as **still indeterminate** (§5.2).

**On the estate:**
- **Run the duplication check** on the task ledger and changelog (§8a) — two files,
  cheap, and the only outstanding consequence of eight interruptions.
- Treat the three unresolved acts as an open record question rather than a closed
  success (§5.2).
- Publish the high-water marks in one place so S4 has a single source, and mark
  them unverified.
- Recognise that the register layer is the agent's memory (§1.3), and weight its
  integrity accordingly.

---

### Related

**Agent framework** — [AG-000](ag-000-agent-constitution.md) ·
[AG-002](ag-002-agent-disclosure-obligations.md) ·
[AG-003](ag-003-agent-output-standards.md) ·
[AG-005](ag-005-agent-tool-use-limits.md)

**Records that serve as memory** — [MX-013](../corpus/mx-013-records-and-versioning.md) ·
[task ledger](../00-governance-map/task-ledger.md) ·
[changelog](../00-governance-map/changelog.md) ·
[GM-02 document index](../00-governance-map/document-index.md)

**Where the search unreliability is recorded** — [V-10](../00-governance-map/verification-log.md) ·
[GM-08 verification log](../00-governance-map/verification-log.md) ·
[ST-07](../standards/st-07-evidence-and-verify.md) ·
[REG-07](../registries/reg-07-defect-classification-registry.md)

**Agent instruments a reader of this page may have wanted instead** —
[AG-004](ag-004-refusal-and-escalation-register.md) ·
[AG-007](ag-007-agent-instruction-interpretation.md) ·
[AG-010](ag-010-agent-error-and-correction.md) (not yet written) ·
[AG-001](ag-001-agent-roles-and-scopes.md)

### Exit pair

1. **Run the duplication check.** Falsifier §8(a) — the task ledger and the
   changelog, two patterns. It is the one outstanding consequence of eight
   interruptions and takes minutes.
2. **Read why a clean record is not clean.**
   [§5.1](#51-the-outcome-that-should-not-be-trusted) — three of eight read-backs
   used the method this corpus has recorded as unreliable.

<!-- mx-pagestamp: AG-006 · v2026.10.1 · governing · tier 4 · reviewed 2026-09-16 · next review 2027-03-16 -->
<!-- mx-demo: the published site is a demonstration; three interrupted acts remain unresolved under this instrument's own clarified rule -->
