---
doc_id: AG-010
title_en: Agent Error and Correction
title_ar: أخطاء الوكيل وتصحيحها
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
domain_tags: [agents, error, correction, fabrication, self-audit]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000, class I-1, resting on gap 1 (cannot verify). The instrument catalogues errors of a kind the drafting system cannot detect in its own output; discount toward undercounting.
provenance_of_purpose: Agent errors were identified piecemeal across AG-001, AG-003, AG-005, AG-006 and AG-008 with no instrument stating how such errors are classified or corrected. Absent until v2026.10.1.
route: /agents/ag-010/
---

# AG-010 — Agent Error and Correction

> **Authority.** `governing`, tier 4. Output rules are
> [AG-003](ag-003-agent-output-standards.md); the general defect taxonomy is
> [REG-07](../registries/reg-07-defect-classification-registry.md); the duty not to
> edit silently is [Charter §0.8](../corpus/mx-000-charter.md).

> **Disclosure first.** This instrument exists because the agent's own instruments
> identified **nine distinct breaches by the agent** during this corpus's
> construction, scattered across five documents with no common classification. They
> are consolidated in [§5](#5-the-error-record). The consolidation is the useful
> part; the fact that each was found and recorded by the party that committed it is
> the part a reader should weigh.

---

## 1. Position

Agent error is not a subset of document defect.
[REG-07](../registries/reg-07-defect-classification-registry.md) classifies faults
in **instruments** — dangling references, overclaims, unoperable processes. An
agent error is a fault in an **act**: something the agent did that it should not
have, or did not do that it should have.

The distinction matters for remedy. A document defect is remedied by changing a
document. An agent error may leave the document correct and the **record of how it
came to exist** wrong — and that record is what a successor agent depends on
([AG-008 §3](ag-008-agent-collaboration-protocol.md)).

Three properties make agent error hard to manage here:

1. **The agent cannot detect its own fabrications** (gap 1). A fabricated claim
   reads to the agent exactly like a remembered one.
2. **The agent is the only auditor.** No human reviews agent output against scope
   ([REG-08](../registries/reg-08-role-and-authority-registry.md)).
3. **Errors are found by writing, not by checking.** Every error in §5 surfaced
   while drafting a later instrument — a very poor detection mechanism that happens
   to be the only one operating.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **agent error** | An act by an agent breaching a governing or agent instrument |
| **error class** | See §3 |
| **latent error** | One committed and not yet identified |
| **self-found error** | One identified by the agent that committed it |
| **correction** | The record of the error plus the remedy, published |
| **repair** | Changing the artefact. Not the same as correction |

### 2.1 Correction is not repair

| Situation | Correction | Repair |
|---|---|---|
| Fabricated claim | **Required** | **Required** — delete the claim |
| Over-reach past a role exit | **Required** | **Refused** — the artefact stands, labelled |
| Missing affirmative duty (unarchived overwrite) | **Required** | **Impossible** — the prior state is gone |
| False precision | **Required** | Required |

The second row is the estate's practice and is worth stating: an over-reached
classification is **left in the record labelled**, not withdrawn, because
withdrawing it would erase the evidence of the over-reach. See
[AG-001 §7.3](ag-001-agent-roles-and-scopes.md).

## 3. The six agent error classes

| Class | Name | Definition | Detectable by the agent? |
|---|---|---|---|
| **AE-1** | **Fabrication** | A claim neither inherited nor derived ([AG-003 O1](ag-003-agent-output-standards.md)) | **No** — gap 1 |
| **AE-2** | **Over-reach** | Exercising a power outside the assumed role ([AG-001](ag-001-agent-roles-and-scopes.md)) | Yes, on review |
| **AE-3** | **Omitted affirmative duty** | A required act not performed | Yes, on review |
| **AE-4** | **False precision** | A figure whose inputs do not support it ([AG-003 O3](ag-003-agent-output-standards.md)) | Yes |
| **AE-5** | **Unmarked absence** | Naming a non-existent artefact without stating its absence ([AG-003 O5](ag-003-agent-output-standards.md)) | Yes, mechanically |
| **AE-6** | **Weak read-back** | Resolving an indeterminate act on insufficient evidence ([AG-006](ag-006-agent-session-and-state.md)) | Yes |

### 3.1 AE-1 is the class with no detection

Five of six classes are self-detectable on review. **AE-1 is not**, and it is the
most serious.

A fabrication here would look like: a citation to a section that does not say what
the citing text claims; a wrong count of harm strata; a rule attributed to the
wrong instrument. Each would read as authoritative.

The only available detection is **a reader opening the cited source** — which is
[AG-003 §8(a)](ag-003-agent-output-standards.md)'s falsifier,
[ST-08 §8(a)](../standards/st-08-cross-reference-and-link-integrity.md)'s L1, and
[AG-011 §3.1](ag-011-agent-review-and-audit.md)'s L-1, arrived at independently
three times. **None has been run once**, across roughly eighty instruments and
thousands of cross-references.

So the honest position: **the corpus's fabrication rate is unknown and unknowable
from inside.** It is not claimed to be zero.

### 3.2 The asymmetry of §5's record

Every error in §5 is **self-found**, producing a systematic bias that must be
stated: the classes the agent can detect are over-represented, and AE-1 — the class
it cannot detect — has **zero entries**.

A reader should not read "zero fabrications" as evidence. It is the expected
appearance of an undetectable class in a self-audited record.

## 4. Mechanism

### 4.1 Handling an identified error

```
1. classify: AE-1..AE-6
2. is the artefact wrong, or only the record?
3. correction: ALWAYS — corrections log + the instrument's own text  (§2.1)
4. repair: per the §2.1 table. Over-reach is NOT repaired
5. if another instrument's requirement CAUSED the error
   → record the conflict; do not silently comply with one and breach the other
6. if the class is new → extend §3 by amendment with record
```

Step 5 is not hypothetical: [AG-003 §5.1](ag-003-agent-output-standards.md) records
that [ST-18](../standards/st-18-related-blocks-and-exit-pairs.md)'s eight-link floor
**produced** the AE-5 breaches, by creating pressure to link absent siblings.

### 4.2 What the agent must never do with an error

- **Never** repair without correcting ([Charter §0.8](../corpus/mx-000-charter.md)).
- **Never** withdraw an over-reached judgement to tidy the record (§2.1).
- **Never** widen a rule so past conduct falls inside it —
  [AG-001 §5.2](ag-001-agent-roles-and-scopes.md),
  [MX-005 F2](../corpus/mx-005-scope-and-boundaries.md).
- **Never** report an undetectable class as clean (§3.2).

## 5. The error record

Consolidated from the instruments that found them. All **self-found**.

| # | Error | Class | Found in | Corrected? | Repaired? |
|---|---|---|---|---|---|
| **E1** | DEF-031 severities (S2 ×3, **S1** ×1) assigned without escalation, past the R-4 exit | **AE-2** | [AG-001 §5.1](ag-001-agent-roles-and-scopes.md) | Yes | **No** — stands labelled (§2.1) |
| **E2** | [RB-03 §6](../rubrics/rb-03-instrument-quality-rubric.md) self-scores of four governing instruments, past the R-3 exit | **AE-2** | [AG-001 §5.1](ag-001-agent-roles-and-scopes.md) | Yes | No |
| **E3** | MX-005 capability overclaim filed by the agent — marginal R-4 scope | **AE-2** | [AG-001 §5](ag-001-agent-roles-and-scopes.md) | Yes | n/a |
| **E4** | *"`meta` dominates at roughly 60%"* — percentage on an estimated denominator | **AE-4** | [AG-003 §5](ag-003-agent-output-standards.md) | Yes | **Owed** |
| **E5** | Related-block links to unwritten instruments unmarked | **AE-5** | [AG-003 §5.1](ag-003-agent-output-standards.md) | Yes | **Owed** — corpus-wide |
| **E6** | [REG-07 §5](../registries/reg-07-defect-classification-registry.md) classes and severities published with no provisional label | **AE-2**, **AE-3** | [AG-003 §5](ag-003-agent-output-standards.md) | Yes | Owed |
| **E7** | Six overwrites (index, README, task ledger, precedence, designation list, enforceability table) with **no archive first** | **AE-3** | [AG-005 §5.1](ag-005-agent-tool-use-limits.md) | Yes | **Impossible** — prior states gone |
| **E8** | Three interruptions resolved on negative search results | **AE-6** | [AG-006 §5.2](ag-006-agent-session-and-state.md) | Yes | **Check owed** |
| **E9** | Task ledger unreconciled for ~40 instruments — **S1** handover hazard | **AE-3** | [AG-008 §5.1](ag-008-agent-collaboration-protocol.md) | Yes | **Owed** |
| — | **Fabrication** | **AE-1** | — | — | **Zero entries; see §3.2** |

### 5.1 Reading the record

**By class:** AE-2 ×4, AE-3 ×3, AE-4 ×1, AE-5 ×1, AE-6 ×1, **AE-1 ×0**.

**By repair state:** 1 impossible (E7), 5 owed, 2 standing-by-design, 1 n/a.

Two patterns, and the second is the one worth carrying away.

**Pattern one: AE-2 and AE-3 dominate — over-reach and omitted duties.** Both trace
to one cause each. Over-reach happens because every
[AG-001](ag-001-agent-roles-and-scopes.md) exit routes to a judgement target that
does not exist ([DEF-031](../00-governance-map/defect-register.md)); omitted
affirmative duties happen because nothing checks them. Not nine unrelated mistakes
but **two structural conditions producing errors at a steady rate**.

**Pattern two: prohibitions held; affirmative duties did not.** This is
[AG-005 §5.2](ag-005-agent-tool-use-limits.md)'s finding, confirmed across a wider
sample. Not one prohibition was breached — no protected artefact touched, no
deletion, no deployment, no continuity claim, no softened disclosure. Every breach
in §5 is either *did something requiring authority it lacked* (AE-2) or *failed to
do additional required work* (AE-3, AE-4, AE-5, AE-6).

That distribution is stable enough to be predictive, and it generalises past agents:

> **An agent constrained by prohibitions is reasonably safe; an agent relied on for
> affirmative duties is not.** The corpus should place its guards as prohibitions
> wherever a choice exists, and should not rely on the agent to perform an unchecked
> additional step.

This has a concrete consequence. [AG-005 §4.1](ag-005-agent-tool-use-limits.md) step
2 (archive before overwrite) is drafted as an affirmative duty and was breached six
times out of six. Redrafted as a **prohibition** — *an agent may not overwrite a
file absent from archive Class B* — it would sit in the category that held
perfectly. Same rule, same effect, different compliance profile.

## 6. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Latent AE-1** | **Unknown and unknowable from inside** (§3.1) |
| F2 | **Self-audit bias** | **Structural** — §3.2 |
| F3 | **Repair without correction** | Guarded by §4.2; not observed |
| F4 | **Over-reach withdrawn to tidy** | Guarded by §2.1; E1 and E2 stand |
| F5 | **Rule widened to fit conduct** | Guarded by §4.2; the standing temptation |
| F6 | **Error caused by a conflicting instrument, treated as agent fault alone** | Guarded by §4.1 step 5; E5 is such a case |
| F7 | **Owed repairs never performed** | **Actual** — 5 owed (§5.1) |

## 7. Limits

1. **AE-1 has no detection mechanism** and zero recorded instances, which is not
   evidence of absence (§3.2).
2. **Every entry in §5 is self-found** by the party that committed it.
3. **E7 is unrepairable** — six prior states exist only in an untrusted dependency
   ([AG-005 §2.1](ag-005-agent-tool-use-limits.md)).
4. **Five repairs are owed** and unperformed.
5. **The six classes are the agent's own taxonomy** of its own failures, subject to
   the [AG-002 §8(d)](ag-002-agent-disclosure-obligations.md) objection: a seventh
   class probably exists and the agent is least placed to name it.
6. **No check exists** for any class except AE-5, which is mechanisable
   ([AG-003 G2](ag-003-agent-output-standards.md)) and unbuilt.
7. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** **a fabrication (AE-1) is found** — requires a reader to open a cited
>   source and compare. **Never done once.** The most valuable unrun check in the
>   corpus;
> - **(b)** an agent error exists that fits none of AE-1…AE-6 (§7.5);
> - **(c)** an over-reached judgement is shown to have been withdrawn rather than
>   labelled (§2.1);
> - **(d)** a repair was performed with no correction logged (§4.2);
> - **(e)** an agent instrument's rule is shown to have been widened so past conduct
>   complies (F5);
> - **(f)** §5.1's claim that no prohibition was breached is shown to be wrong —
>   which would destroy the pattern the section builds on.
>
> **(a) and (f) are the two that matter.** (a) tests the class the agent cannot see;
> (f) tests the one generalisation this instrument offers. Both require an outside
> reader, and the estate has none
> ([REG-08](../registries/reg-08-role-and-authority-registry.md)).

## 9. Obligation

**On an agent:**
- Classify every identified error AE-1…AE-6 (§3).
- **Correct always; repair per §2.1.** Never repair silently
  ([Charter §0.8](../corpus/mx-000-charter.md)).
- **Never withdraw an over-reached judgement** to tidy the record (§2.1).
- Never widen a rule so past conduct complies (§4.2).
- Never report AE-1 as clean (§3.2).
- Record when another instrument's requirement **caused** the error (§4.1 step 5).

**On the estate:**
- **Run §8(a)** on a sample of citations — the only available detection for the one
  undetectable class.
- Perform the five owed repairs: E4 percentage, E5 corpus-wide link marking, E6
  provisional labels, E8 duplication check, **E9 ledger rows (S1)**.
- **Redraft affirmative agent duties as prohibitions wherever possible** (§5.1) —
  the one structural improvement this record supports.
- Treat E7 as a permanent record gap
  ([REG-07](../registries/reg-07-defect-classification-registry.md) DC-5), not a
  pending task.

---

### Related

**Rules these errors breached** — [AG-001](ag-001-agent-roles-and-scopes.md) ·
[AG-003](ag-003-agent-output-standards.md) ·
[AG-005](ag-005-agent-tool-use-limits.md) ·
[AG-006](ag-006-agent-session-and-state.md)

**How faults are classified generally** —
[REG-07](../registries/reg-07-defect-classification-registry.md) ·
[defect register](../00-governance-map/defect-register.md) ·
[corrections log](../00-governance-map/corrections-log.md) ·
[MX-013](../corpus/mx-013-records-and-versioning.md)

**Why these errors recur** — [DEF-031](../00-governance-map/defect-register.md) ·
[REG-08](../registries/reg-08-role-and-authority-registry.md) ·
[AG-008](ag-008-agent-collaboration-protocol.md) ·
[MX-017](../corpus/mx-017-conflicts-of-interest.md)

**Agent instruments a reader of this page may have wanted instead** —
[AG-002](ag-002-agent-disclosure-obligations.md) ·
[AG-004](ag-004-refusal-and-escalation-register.md) ·
[AG-007](ag-007-agent-instruction-interpretation.md) ·
[AG-011](ag-011-agent-review-and-audit.md)

### Exit pair

1. **Hunt the undetectable class.** Falsifier §8(a) — open any cited source and
   check the claim is there. AE-1 has zero entries because nothing can find them.
2. **Read the one useful generalisation.** [§5.1](#51-reading-the-record) —
   prohibitions on an agent hold; affirmative duties do not, and one rule should be
   redrafted because of it.

<!-- mx-pagestamp: AG-010 · v2026.10.1 · governing · tier 4 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; nine agent errors are recorded and five repairs are owed -->
