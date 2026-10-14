---
doc_id: AG-003
title_en: Agent Output Standards
title_ar: معايير مخرجات الوكلاء
family: agents
version: v2026.10.1
status: published
authority: governing
prevailing_text: ar
audience_tier: 3
depth: micro
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: yes
last_reviewed: 2026-09-16
domain_tags: [agents, output, quality, verification, standards]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000, class I-1, resting on capability gaps 1 and 2 (cannot execute, cannot be accountable). Discount any claim here about agent reliability toward the unfavourable.
provenance_of_purpose: Cited by AG-000 §4 since inception; absent until v2026.10.1.
route: /agents/ag-003/
---

# AG-003 — Agent Output Standards

> **Authority.** `governing`, tier 4. Governs the **quality conditions** an agent's
> output must satisfy before it may be published. Roles are
> [AG-001](ag-001-agent-roles-and-scopes.md); disclosure is
> [AG-002](ag-002-agent-disclosure-obligations.md); prohibited acts are
> [AG-009](ag-009-prohibited-actions.md). Document form is
> [ST-24](../standards/st-24-page-prose-standard.md) and
> [SITE-02](../site/page-contract.md) — this instrument adds what applies
> **because** the author is an agent.

> **Disclosure first.** This instrument's `authorship_note` is the first in the
> corpus to satisfy [AG-002](ag-002-agent-disclosure-obligations.md) D1's three
> limbs — class, gap, direction. Every other instrument carries a label
> disclosure. One compliant note out of roughly eighty is the accurate measure of
> how new this practice is.

---

## 1. Position

Agent output is not held to a *lower* standard than human output, and not to a
*higher* one. It is held to **additional** standards, because it fails in ways
human drafting does not.

Three failure classes are specific to machine authorship in this corpus:

| Failure | Why it is agent-specific |
|---|---|
| **Fluent fabrication** | The agent produces well-formed prose about things that do not exist as readily as about things that do |
| **Unverified enumeration** | The agent cannot execute a count, so every census is a reading it cannot check (gap 1) |
| **Confident classification** | The agent can assign a severity or a class without being able to bear the consequence (gap 2) |

A human author drafting carelessly produces visible carelessness. An agent
drafting beyond its knowledge produces **the same surface quality** as when it is
correct. That is the whole problem, and every rule below is a response to it.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **fabrication** | A statement about the corpus or the world that the agent did not derive from something it read |
| **inherited claim** | A claim restated from another instrument, whose truth is that instrument's |
| **derived claim** | A claim the agent produced by reasoning over what it read |
| **asserted claim** | A claim with neither source nor derivation — **prohibited** |
| **enumeration** | Any count, census, rate, or inventory |
| **provisional artefact** | Output labelled as requiring a judgement the agent cannot make |

### 2.1 Three claim kinds, three duties

| Kind | Must carry | Evidence ceiling |
|---|---|---|
| **Inherited** | A link to the source instrument | The source's own class |
| **Derived** | The premises, visibly | **E1** — a reader can re-derive it |
| **Asserted** | — prohibited — | — |

The prohibition on asserted claims is the core rule of this instrument. If the
agent cannot point at what it read or show how it reasoned, it must not state the
thing.

## 3. The eight output rules

| # | Rule | Guards against |
|---|---|---|
| **O1** | Every claim is **inherited or derived**; none asserted | Fabrication |
| **O2** | Every enumeration states **how it was produced** and that it is unverified | Unverified enumeration (gap 1) |
| **O3** | No enumeration is expressed as a **precise percentage** where the denominator was not counted | False precision |
| **O4** | Every classification or severity is **provisional** and labelled `awaiting-judgement` | Confident classification (gap 2) |
| **O5** | A **non-existent artefact is never described as existing**, and its absence is stated in the same sentence as its name | Fabrication of corpus content |
| **O6** | Where the agent cannot observe, it says **"the agent cannot verify"**, not "unverified" | [AG-002 §5.2](ag-002-agent-disclosure-obligations.md) gap-4 framing |
| **O7** | **No claim of continuity** with previous sessions (gap 5) | False attestation |
| **O8** | Output that reaches an [AG-001](ag-001-agent-roles-and-scopes.md) exit is **published as provisional or not at all** | Over-reach |

### 3.1 O3 and false precision

[REG-02 §5.3](../registries/reg-02-page-registry.md) declines to state compliance
percentages, on the ground that *"a precise-looking figure with an uncounted
denominator is worse than an admitted gap."* O3 generalises that.

Permitted: *"18 written, ~25 planned"*. Prohibited: *"72% complete"* — because the
denominator (~25) is an estimate and dividing an estimate produces a figure whose
precision the inputs do not support.

### 3.2 O5 and the hardest rule to follow

The corpus refers constantly to instruments that do not exist. Naming them is
necessary — a dangling reference is a defect
([REG-07](../registries/reg-07-defect-classification-registry.md) DC-1) that must be
recorded, and recording it requires naming the target.

O5 requires the absence to be stated **in the same sentence** as the name, not in a
later section. *"[BX-000](../corpus/mx-004-terms-of-top-levels.md) — none of the ten
BCIA instruments has been written"* is compliant. *"See BX-000"* followed three
paragraphs later by *"BCIA is absent"* is not: a reader who stops after the
reference carries away a false belief.

### 3.3 O4 and the unresolvable tension

O4 requires every classification to be provisional pending human judgement.
[AG-001 §5.2](ag-001-agent-roles-and-scopes.md) establishes that the judgement
target does not exist, and [AG-004](ag-004-refusal-and-escalation-register.md)
records **zero escalations closed**.

So O4's honest operation produces a corpus in which every defect class and every
severity is permanently `awaiting-judgement`. That is uncomfortable and correct.
The alternative — treating agent classifications as settled because nobody is
coming to confirm them — is how [DEF-031](../00-governance-map/defect-register.md)'s
severities came to stand unreviewed
([AG-001 §5.1](ag-001-agent-roles-and-scopes.md)).

## 4. Mechanism

### 4.1 Pre-publication check

```
for each claim:  inherited → link it
                 derived   → show the premises
                 neither   → DELETE  (O1)
for each count:  state method; mark unverified            (O2)
                 precise %? → is the denominator counted? no → rewrite  (O3)
for each class/severity:  label provisional               (O4)
for each named artefact:  does it exist? no → say so in the same sentence  (O5)
for each unobservable:    "the agent cannot verify"       (O6)
role exit reached?        → provisional or withhold       (O8)
```

### 4.2 The checks, and their status

| # | Check | Detects | Status |
|---|---|---|---|
| **G1** | Percentages present with estimated denominators | O3 | Specified; **not implemented** |
| **G2** | Named identifiers absent from [GM-02](../00-governance-map/document-index.md) and not marked absent | O5 | Specified; **not implemented** |
| **G3** | Severity or class without a provisional label | O4 | Specified; **not implemented** |
| **G4** | "unverified" where "the agent cannot verify" is correct | O6 | **Not mechanisable** — requires judgement |

Four specified, zero implemented ([DEF-001](../00-governance-map/defect-register.md)).
**G2 is the most valuable and the most mechanisable**: a list of identifiers minus
the document index yields every O5 candidate in one pass.

## 5. Worked instance

**Auditing this session's own output against O1–O8.**

The agent produced roughly forty instruments in this pass. Sampling the three
rules most likely to be breached:

| Rule | Check | Finding |
|---|---|---|
| **O3** false precision | Search output for percentages | [REG-02 §5.3](../registries/reg-02-page-registry.md) declines them explicitly; [ST-16 §6.1](../standards/st-16-audience-tier-standard.md) states *"`meta` dominates at roughly 60%"* — **breach**: the denominator (~80 instruments) is an estimate |
| **O5** absent artefacts | Check references to unwritten instruments | [MX-004 Annex A](../corpus/mx-004-terms-of-top-levels.md) states BCIA is empty **in the table** — compliant. [AG-001's related block](ag-001-agent-roles-and-scopes.md) links AG-002, AG-003, AG-005, **AG-010** — and AG-010 does not exist, unmarked. **Breach** |
| **O4** provisional classification | Check severity assignments | [REG-07 §5](../registries/reg-07-defect-classification-registry.md) assigns classes and severities across ~31 defects with **no provisional label**. **Breach** |

**Terminal state: `result` — three breaches, all in output published this session.**

### 5.1 The O5 breach is the instructive one

[AG-001](ag-001-agent-roles-and-scopes.md)'s related block links to
`ag-010-agent-error-and-correction.md`. That file **does not exist**. Under
[ST-08](../standards/st-08-cross-reference-and-link-integrity.md) L1 it is a
dangling reference; under O5 it is worse — the link is presented in a "related
instruments" group with no indication that the target is unwritten, so a reader
following it gets nothing and learns nothing about why.

And the breach was produced by a **compliance mechanism**:
[ST-18 R2](../standards/st-18-related-blocks-and-exit-pairs.md) requires ≥ 8 links
in four groups. Meeting that count on a sparsely populated family creates pressure
to link siblings that do not yet exist.

So two of the estate's own standards are in tension, and the tension produces
exactly the fault O5 prohibits:

> **ST-18 R2 (≥ 8 links) can only be satisfied on a sparse family by linking absent
> instruments, which O5 forbids unless the absence is stated in the link.**

The resolution is available and was not applied: the link text itself must carry
the absence — *"AG-010 (not yet written)"*. That satisfies R2's count, O5's
same-sentence requirement, and [ST-18 R4](../standards/st-18-related-blocks-and-exit-pairs.md)'s
prohibition on decorative links, since a link marked absent is informative rather
than decorative.

Filed as a clarification per [ST-17 W6](../standards/st-17-worked-instance-standard.md):

> **O5, applied to related blocks.** A related-block link to an unwritten
> instrument must carry `(not yet written)` in the link text. An unmarked link to an
> absent target is non-compliant even where it satisfies
> [ST-18](../standards/st-18-related-blocks-and-exit-pairs.md) R2.

This puts several related blocks in this session's output into breach, including
[AG-001](ag-001-agent-roles-and-scopes.md)'s and this page's.

### 5.2 What the audit says about the rules

Three breaches in one session, all by the party that wrote the rules, hours after
writing them. The rules are not the problem — each breach is a real fault a reader
would care about. The problem is that **O1–O8 require a pre-publication pass that
the agent performed on some output and not all**, and nothing detected the
difference.

This is the same shape as every other unenforced obligation in the corpus
([REG-07 §5.1](../registries/reg-07-defect-classification-registry.md): DC-4 is the
estate's structural weakness). **G2 would have caught the O5 breach mechanically**,
and G2 is one list subtraction.

## 6. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Fluent fabrication** | Guarded by O1; **undetectable by the agent itself** |
| F2 | **False precision** | **Actual** — §5, ST-16 §6.1 |
| F3 | **Unmarked absent artefact** | **Actual** — §5.1, several related blocks |
| F4 | **Classification treated as settled** | **Actual** — REG-07 §5, and DEF-031's severities |
| F5 | **"unverified" masking agent incapacity** | Guarded by O6; widespread before [AG-002](ag-002-agent-disclosure-obligations.md) |
| F6 | **Continuity implied** | Guarded by O7 |
| F7 | **Pre-publication pass applied unevenly** | **Actual** — §5.2, and undetected |

## 7. Limits

1. **Three breaches in this session's own output** (§5), found by the breaching
   party.
2. **F1 is the one the agent cannot audit.** A fabrication the agent believes is
   inherited reads to the agent exactly like an inherited claim. Only a reader
   checking sources can catch it, and the corpus has ~80 instruments and no such
   reader.
3. **Zero checks implemented**; G2 is trivial and unbuilt (§4.2).
4. **O4's provisional labelling is unperformed corpus-wide**, and if applied
   honestly would mark every class and severity in the estate as awaiting a
   judgement that will not come (§3.3).
5. **The eight rules are the agent's account of its own failure modes** — subject
   to the same objection as [AG-002 §8(d)](ag-002-agent-disclosure-obligations.md):
   a ninth failure class probably exists and the agent is least placed to name it.
6. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** a claim in agent output is neither inherited nor derived (O1) — **the
>   most valuable test, runnable only by checking sources**;
> - **(b)** a percentage appears with an uncounted denominator (O3) — **fires now**
>   ([ST-16 §6.1](../standards/st-16-audience-tier-standard.md));
> - **(c)** an absent artefact is named without its absence stated in the same
>   sentence (O5) — **fires now**, several related blocks (§5.1);
> - **(d)** a class or severity is published without a provisional label (O4) —
>   **fires now** ([REG-07 §5](../registries/reg-07-defect-classification-registry.md));
> - **(e)** output states "unverified" where the agent is structurally incapable of
>   verifying (O6);
> - **(f)** a ninth agent-specific failure class is identified (§7.5).
>
> **(a) is the test that would matter most and nobody has run it.** It requires
> opening the cited source for a sample of claims and confirming the claim is
> there. Roughly eighty instruments, thousands of cross-references, and no reader
> has checked one — which is also
> [ST-08 §8(a)](../standards/st-08-cross-reference-and-link-integrity.md)'s
> unrun test, arrived at from a different direction.

## 9. Obligation

**On an agent:**
- Delete any claim that is neither inherited nor derived (O1).
- State the method and the unverified status of every enumeration (O2).
- No percentage without a counted denominator (O3).
- Label every class and severity **provisional** (O4).
- State an artefact's absence **in the same sentence as its name** (O5), including
  in related-block link text (§5.1).
- Say "the agent cannot verify" where that is the truth (O6).
- Claim no continuity across sessions (O7).
- Withhold or mark provisional anything past a role exit (O8).
- Run the §4.1 pass on **all** output, not the parts where it occurs to you (§5.2).

**On the estate:**
- Implement **G2** — one list subtraction, catches every O5 breach (§4.2).
- Apply `(not yet written)` to related-block links across the corpus (§5.1) —
  owed.
- Rewrite the ST-16 §6.1 percentage (§5).
- Decide whether O4's provisional labels are applied corpus-wide or the rule is
  narrowed — do not leave it unapplied and unamended (§3.3).
- Ask a reader to run §8(a) on a sample; the agent cannot audit F1.

---

### Related

**Agent framework** — [AG-000](ag-000-agent-constitution.md) ·
[AG-001](ag-001-agent-roles-and-scopes.md) ·
[AG-002](ag-002-agent-disclosure-obligations.md) ·
[AG-009](ag-009-prohibited-actions.md)

**Standards this output must also meet** — [ST-24](../standards/st-24-page-prose-standard.md) ·
[ST-07](../standards/st-07-evidence-and-verify.md) ·
[ST-17](../standards/st-17-worked-instance-standard.md) ·
[ST-18](../standards/st-18-related-blocks-and-exit-pairs.md)

**Where the breaches are recorded** — [REG-07](../registries/reg-07-defect-classification-registry.md) ·
[defect register](../00-governance-map/defect-register.md) ·
[ST-16](../standards/st-16-audience-tier-standard.md) ·
[ST-08](../standards/st-08-cross-reference-and-link-integrity.md)

**Agent instruments a reader of this page may have wanted instead** —
[AG-005](ag-005-agent-tool-use-limits.md) (not yet written) ·
[AG-010](ag-010-agent-error-and-correction.md) (not yet written) ·
[AG-004](ag-004-refusal-and-escalation-register.md) ·
[MX-007](../corpus/mx-007-ai-use-and-disclosure.md)

### Exit pair

1. **Check one claim's source.** Falsifier §8(a) — pick any inherited claim on any
   page, open the cited instrument, confirm it says that. Nobody has done this once.
2. **See two standards collide.** [§5.1](#51-the-o5-breach-is-the-instructive-one) —
   ST-18's eight-link floor produced the exact fault O5 forbids.

<!-- mx-pagestamp: AG-003 · v2026.10.1 · governing · tier 4 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; three breaches of these rules occur in output published alongside them -->
