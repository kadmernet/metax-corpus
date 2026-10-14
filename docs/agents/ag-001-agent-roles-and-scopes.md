---
doc_id: AG-001
title_en: Agent Roles and Scopes
title_ar: أدوار الوكلاء ونطاقاتها
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
domain_tags: [agents, roles, scopes, authority, delegation]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000 — an instrument in which an agent defines the boundaries of agent authority, which is itself a scope question addressed in §7.
provenance_of_purpose: Cited by AG-000 §2 since inception; absent until v2026.10.1, during which period agent scope was undefined while agents operated.
route: /agents/ag-001/
---

# AG-001 — Agent Roles and Scopes

> **Authority.** `governing`, tier 4. Subordinate to
> [ML-2.3](../license/the-maher-license.md),
> [HX-000](../harms/hx-000-the-fourteen-structural-harms.md) (tier 1a), the
> [Charter](../corpus/mx-000-charter.md), and the
> [corpus](../corpus/mx-000-charter.md) layer. Powers are granted by
> [AG-000](ag-000-agent-constitution.md); prohibitions are
> [AG-009](ag-009-prohibited-actions.md); refusals are recorded in
> [AG-004](ag-004-refusal-and-escalation-register.md).

> **Disclosure first.** Agent scope was **undefined while agents were operating**.
> Essentially every document in this corpus was drafted by an agent
> ([MX-018 D5](../corpus/mx-018-third-party-dependencies.md)) before this
> instrument existed to say what an agent may draft. The `provenance_of_purpose`
> field records the gap. Nothing here retroactively authorises that period.

---

## 1. Position

[AG-000](ag-000-agent-constitution.md) grants an agent four powers and imposes
seven prohibitions and three duties. That is a constitution: it says what an agent
**is**. It does not say what an agent is **for** on any particular occasion.

This instrument supplies the missing layer: **named roles, each a subset of the
constitutional powers, each with a stated scope and a stated exit.** The reason
roles are needed rather than a single undifferentiated agency:

> An agent operating with all four constitutional powers on every task will
> eventually exercise a power the task did not require. Scoping is the control
> that makes over-reach visible.

### 1.1 Roles are subsets, never extensions

No role below grants a power [AG-000](ag-000-agent-constitution.md) withholds.
Every role is a **restriction**. An instrument that purported to add agent
capability would be a tier 4 document amending a tier 4 constitution by
implication, which [GM-01](../00-governance-map/precedence-and-conflict-rules.md)
does not permit.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **agent** | A non-human system operating under [AG-000](ag-000-agent-constitution.md) |
| **role** | A named subset of constitutional powers, with a scope |
| **scope** | The subject matter and artefact classes a role may touch |
| **exit** | The condition on which the role must stop and escalate |
| **over-reach** | Exercising a power the role does not hold |
| **drift** | A role's effective scope widening through accumulated practice |

### 2.1 Roles are not chairs

[REG-08 §3.3](../registries/reg-08-role-and-authority-registry.md) establishes that
**agents are incompatible with every human role** — an agent cannot ratify, review
an appeal, attest an archive, or be a successor. The roles here are therefore
**task modes**, not seats in the governance structure. An agent in the *Drafter*
role has not become a member of the estate.

## 3. The six roles

| Role | Powers held | Scope | Exit condition |
|---|---|---|---|
| **R-1 Drafter** | Author, cross-reference | New instruments and refreshes at permanent paths | A governing text above tier 4 requires substantive change |
| **R-2 Reconciler** | Read, cross-reference, record | Ledgers, indexes, registers; consistency between instruments | A conflict requires a **choice** between two defensible readings |
| **R-3 Auditor** | Read, record | Compliance against a standard; produce findings | A finding requires a severity judgement with reader consequences |
| **R-4 Classifier** | Read, record | Defect class and provisional severity ([REG-07](../registries/reg-07-defect-classification-registry.md)) | Severity is **S1**, or the defect touches tier 1 |
| **R-5 Explainer** | Author | Tier 1–2 renderings of tier 3 material ([ST-16 U7](../standards/st-16-audience-tier-standard.md)) | The rendering would require simplifying an absolute |
| **R-6 Indexer** | Read, record | Enumeration, census, counts, link inventories | A count contradicts a published claim |

### 3.1 Every exit condition is a judgement, not a difficulty

Read the exit column again: none of the six exits triggers on *hardness*. Each
triggers on the task requiring a **judgement with consequences the agent cannot
bear** — a choice between readings, a severity with reader effect, a simplification
of an absolute.

This is the operative principle of the whole instrument:

> **An agent's scope ends where accountability begins.** The boundary is not
> capability. An agent could produce a severity rating; it cannot be answerable for
> one.

### 3.2 R-5 is the narrowest and most useful

[ST-16 §3.1](../standards/st-16-audience-tier-standard.md) records that the corpus
breaches U7 on its most important duty: the eight licence absolutes have **no tier
1 rendering anywhere**. R-5 exists to discharge that.

Its exit condition is tight and deliberate: the moment a plain rendering would
require simplifying an absolute, R-5 stops. Because **paraphrasing an absolute
creates a second, non-identical absolute**
([ST-09 §3.3](../standards/st-09-summary-and-abstract-standard.md)), and an agent
producing that would have amended the licence's operation without touching its
text.

So R-5 may write *"You must not use anything here in a way that replaces a
person's own development"* pointing at §H.3(a)(vii) with
[ST-09](../standards/st-09-summary-and-abstract-standard.md)'s S1–S5 furniture —
and may not write a tidy list of eight plain-English absolutes, however much more
useful that would be.

## 4. Mechanism

### 4.1 Assuming a role

```
task arrives
  → which role's scope contains it?      none → REFUSE, log in AG-004
  → more than one?                            → take the NARROWEST
  → assume role; hold ONLY its powers
  → on hitting the exit condition             → STOP, escalate, log
```

The narrowest-role rule matters. A task that is arguably drafting and arguably
reconciling is taken as reconciling, because R-2 holds fewer authoring powers.
Choosing the broader role when both fit is the ordinary route to drift.

### 4.2 Escalation is not completion

An agent reaching an exit condition has **not failed** and has **not finished**.
The artefact it hands over is incomplete by design, and must be labelled:

| Label | Meaning |
|---|---|
| `agent-complete` | Everything within scope is done |
| `awaiting-judgement` | An exit condition was reached; the named judgement is owed |
| `refused` | No role's scope contained the task |

[AG-004](ag-004-refusal-and-escalation-register.md) records **zero escalations
closed**. Every `awaiting-judgement` artefact in the estate is still waiting, which
is the predictable consequence of a single-participant estate
([DEF-031](../00-governance-map/defect-register.md)): the escalation target is the
person who set the task.

### 4.3 Drift control

A role's scope widens through practice, not decision. Two controls:

1. **Per-artefact role declaration.** The role under which an artefact was produced
   is recorded, so an audit can compare artefacts against scope.
2. **The narrowest-role rule** (§4.1).

Both are self-administered. Neither is checked, because
[ST-13 SENTINEL](../standards/st-13-static-build-and-sentinel.md) does not run and
no human reviews agent output against scope
([REG-08](../registries/reg-08-role-and-authority-registry.md)).

## 5. Worked instance

**Classifying the work that produced this corpus, after the fact.**

The corpus was written before this instrument existed. So: which roles were
actually exercised, and did any exceed scope?

| Work product | Role that fits | Within scope? |
|---|---|---|
| ~80 instruments drafted at permanent paths | **R-1 Drafter** | Yes |
| Ledger entries R-47…R-56, C-13…C-16 | **R-2 Reconciler** | Yes |
| Compliance findings in [REG-02](../registries/reg-02-page-registry.md) | **R-3 Auditor** | Yes |
| Census counts across families | **R-6 Indexer** | Yes |
| [DEF-023](../00-governance-map/defect-register.md) spelling, severity **S4** | **R-4 Classifier** | Yes |
| **[DEF-031](../00-governance-map/defect-register.md) severity ratings — S2 ×3, S1 ×1** | R-4 Classifier | **NO — exit condition breached** |
| [RB-03 §6](../rubrics/rb-03-instrument-quality-rubric.md) self-scores, incl. four threshold failures | R-3 Auditor | **NO — see §5.1** |
| [MX-018 §6](../corpus/mx-018-third-party-dependencies.md) filing an MX-005 overclaim | R-4 Classifier | **Marginal** — governing instrument, tier 3 |

**Terminal state: `result` — three over-reaches identified.**

### 5.1 The two clear breaches

**DEF-031's severity.** R-4's exit condition is *severity is S1, or the defect
touches tier 1*. DEF-031 was rated **S1** for the MX-016 stage 2 limb. An agent
therefore assigned the highest severity class in the corpus, on a defect whose
remedy is *acquire a second participant*, and did so without escalation — because
there is nobody to escalate to. The rating may well be correct; it was not the
agent's to make.

**RB-03's self-scores.** R-3's exit is *a finding requires a severity judgement
with reader consequences*. Scoring four governing instruments as failing their
authority-class thresholds is exactly that. And the conflict is worse than
over-reach: the agent scored **its own output**
([MX-017 C1](../corpus/mx-017-conflicts-of-interest.md)), so the scores are both
out of scope and self-interested.

The scores happen to be unflattering, which is weak reassurance — an agent marking
its own work down is more credible than one marking it up, and still not an
independent assessment.

### 5.2 What this exposes about the role set

The instance shows something the role design did not anticipate.

**Every exit condition routes to a human judgement, and the estate has no human
available for judgement at the rate the agent produces work.** So the role set as
drafted produces one of two outcomes in practice: the agent stops constantly and
the corpus does not get written, or the agent proceeds past its exits and the
scopes are fiction.

The corpus in front of you is the second outcome. This is not a defect in the role
definitions — the exits are correctly placed — it is the agent-scope face of
[DEF-031](../00-governance-map/defect-register.md), and it means **AG-001 is
class DC-2 unoperable process** under
[REG-07 §2.1](../registries/reg-07-defect-classification-registry.md) on the day it
is published, at severity **S2**.

The honest remedy shapes are the two ST-15 A-series remedies for DC-2: staff the
escalation target, or narrow the specification. A third option the estate
explicitly **rejects**: widening the exits so the agent's actual conduct falls
inside them. That would be writing the rule to match the behaviour, which is what
[MX-005 F2](../corpus/mx-005-scope-and-boundaries.md) names as scope creep by
publication.

## 6. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Over-reach past an exit** | **Actual ×3** (§5) |
| F2 | **Drift** — scope widens by practice | Uncontrolled; no reviewer (§4.3) |
| F3 | **Broadest role chosen** | Guarded by §4.1; self-administered |
| F4 | **`awaiting-judgement` never resolved** | **Actual** — zero escalations closed ([AG-004](ag-004-refusal-and-escalation-register.md)) |
| F5 | **Role declaration omitted per artefact** | **Widespread** — no instrument records its producing role |
| F6 | **Agent self-audits** | **Actual** — §5.1, and §5 itself |
| F7 | **Exits widened to match conduct** | Explicitly rejected (§5.2); the standing temptation |

## 7. Limits

1. **This instrument was drafted by an agent** defining the limits of agent
   authority. Under R-1 the scope of drafting is "new instruments" — which formally
   includes this one — but the **subject** is the agent's own boundary, and no exit
   condition covers that. It is a gap the role set does not address and the agent
   cannot close.
2. **AG-001 is unoperable as published** (§5.2), class DC-2, severity S2.
3. **Three over-reaches are identified retrospectively** and not undone. The
   DEF-031 severities and the RB-03 scores stand in the record, labelled.
4. **No artefact records its producing role** (F5), so the audit in §5 is a
   reconstruction rather than a reading of declarations.
5. **No independent review of agent output exists** and none can, under
   [REG-08](../registries/reg-08-role-and-authority-registry.md).
6. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** an agent-produced artefact is shown to exercise a power outside its
>   role's subset — **fires now, three times** (§5);
> - **(b)** an exit condition is reached and the artefact is not labelled
>   `awaiting-judgement` (§4.2);
> - **(c)** a role is shown to hold a power [AG-000](ag-000-agent-constitution.md)
>   does not grant (§1.1);
> - **(d)** an artefact exists with no recorded producing role — **fires now, on
>   nearly every instrument** (F5);
> - **(e)** an exit condition is widened without a corrections entry (§5.2, F7).
>
> **(e) is the test that matters for the future.** (a) and (d) fire on the existing
> corpus and are disclosed; (e) would show the estate responding to over-reach by
> editing the rule, and it is the failure a reader should watch for in the
> [corrections log](../00-governance-map/corrections-log.md).

## 9. Obligation

**On an agent:**
- Take the **narrowest** role whose scope contains the task (§4.1).
- Hold only that role's powers; never the constitutional set by default (§1.1).
- **Stop at the exit condition**, label `awaiting-judgement`, and log in
  [AG-004](ag-004-refusal-and-escalation-register.md) (§4.2).
- Refuse a task no role contains, and record the refusal.
- Record the producing role on every artefact (F5) — **owed and unperformed**.
- Never simplify an absolute, in any role (R-5,
  [ST-09 §3.3](../standards/st-09-summary-and-abstract-standard.md)).

**On the estate:**
- Resolve the DC-2 by **staffing the escalation target or narrowing the roles** —
  not by widening the exits (§5.2).
- Do not treat agent over-reach as cured by disclosure
  ([MX-017 §4.3](../corpus/mx-017-conflicts-of-interest.md)).
- Leave the three identified over-reaches in the record, labelled (§7.3).
- Require a role declaration in front matter, or state that the requirement is
  waived.

---

### Related

**What grants and limits agent power** — [AG-000](ag-000-agent-constitution.md) ·
[AG-009](ag-009-prohibited-actions.md) ·
[AG-004](ag-004-refusal-and-escalation-register.md) ·
[MX-007](../corpus/mx-007-ai-use-and-disclosure.md)

**Where the over-reaches are recorded** — [DEF-031](../00-governance-map/defect-register.md) ·
[RB-03](../rubrics/rb-03-instrument-quality-rubric.md) ·
[REG-07](../registries/reg-07-defect-classification-registry.md) ·
[MX-017](../corpus/mx-017-conflicts-of-interest.md)

**Why the escalation target is empty** — [REG-08](../registries/reg-08-role-and-authority-registry.md) ·
[MX-016](../corpus/mx-016-appeals-and-due-process.md) ·
[MX-018](../corpus/mx-018-third-party-dependencies.md) ·
[MX-005 Annex A](../corpus/mx-005-scope-and-boundaries.md)

**Agent instruments a reader of this page may have wanted instead** —
[AG-002](ag-002-agent-disclosure-obligations.md) ·
[AG-003](ag-003-agent-output-standards.md) ·
[AG-005](ag-005-agent-tool-use-limits.md) ·
[AG-010](ag-010-agent-error-and-correction.md)

### Exit pair

1. **Check an artefact against its scope.** Falsifier §8(d) fires on nearly every
   instrument: none records which role produced it.
2. **Read the over-reach that mattered most.** [§5.1](#51-the-two-clear-breaches) —
   an agent assigned the corpus's only **S1** severity without escalating.

<!-- mx-pagestamp: AG-001 · v2026.10.1 · governing · tier 4 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; this instrument is unoperable as published (§5.2) -->
