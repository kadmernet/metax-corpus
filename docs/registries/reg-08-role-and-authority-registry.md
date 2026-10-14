---
doc_id: REG-08
title_en: Role and Authority Registry
title_ar: سجل الأدوار والصلاحيات
family: registries
version: v2026.10.1
status: published
authority: record
prevailing_text: ar
audience_tier: 2
depth: macro
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [roles, authority, succession, separation-of-duties, registry]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000 — a system with no role in this register — and every role but one is vacant.
route: /registries/roles/
---

# REG-08 — Role and Authority Registry

> **Authority note.** A **record**. The roles themselves are created by
> [MX-015 succession and continuity](../corpus/mx-015-succession-and-continuity.md)
> and [MX-000 Charter](../corpus/mx-000-charter.md); agent powers by
> [AG-000 agent constitution](../agents/ag-000-agent-constitution.md); appeal roles
> by [MX-016](../corpus/mx-016-appeals-and-due-process.md). This page records who
> holds what.

> **Disclosure first.** **Of the roles below, one is filled.** Every separation of
> duties the corpus relies on — assessor from appeal reviewer, author from
> ratifier, curator from successor — is presently a separation between a person and
> an empty chair. This is [DEF-031](../00-governance-map/defect-register.md), and
> this register is the clearest statement of it in the estate.

---

## 1. Position

This register is where the corpus's most attractive property and its most serious
weakness are the same fact.

**The attractive property:** the estate's instruments are written to be checkable
by a reader with no privileges. Authority is exercised through published text, not
through private discretion, so a vacant chair does not stop a reader from
verifying anything.

**The weakness:** several instruments specify *processes* rather than *texts*, and
a process needs a person. Appeals need a reviewer who is not the decider.
Ratification needs an authority who is not the author. Succession needs a
successor. None of these can be discharged by publishing more prose, which is the
only capability the estate currently has.

A reader who wants the short version: **the documents are further along than the
institution.**

## 2. Definition

A **role** is a named capacity to perform acts that the corpus reserves to a
holder, defined by **five** recorded properties:

1. **Powers** — the acts the holder may perform.
2. **Duties** — the acts the holder must perform, and on what trigger.
3. **Incompatibilities** — roles the same person may **not** simultaneously hold.
4. **Appointment and removal** — how the chair is filled and emptied.
5. **Vacancy consequence** — what stops, or degrades, when the chair is empty.

Property 5 is the one usually omitted from governance documents, and the one this
register treats as mandatory. A role definition without a stated vacancy
consequence permits the most common institutional failure: a function quietly
ceasing while the document that created it still reads as though it operates.

### 2.1 Powers are enumerated, never residual

No role carries "such other powers as may be necessary". Residual authority is
how a curator becomes a sovereign. Every power below is listed; anything unlisted
is not held.

### 2.2 Incompatibility is structural, not a matter of good faith

Where two roles are marked incompatible, one person holding both is a **defect
regardless of that person's conduct**. The estate does not accept the argument
that a scrupulous person can safely review their own decision. The guarantee that
[MX-016](../corpus/mx-016-appeals-and-due-process.md) offers a holder is
*independence*, and independence is a property of the arrangement, not of the
reviewer's character.

## 3. Mechanism

### 3.1 The roles

| Role | Powers | Key duties | Incompatible with | Holder |
|---|---|---|---|---|
| **Curator** | Publish, amend, assign identifiers, classify defects, open series/books | Keep records append-only; log every edit; publish failures | Appeal Reviewer; Ratifying Authority | **Maher** |
| **Ratifying Authority** | Resolve `RAT-` open questions; approve amendments to governing text | Decide within a stated period; publish reasons | Curator (as author of the text ratified) | **vacant** |
| **Appeal Reviewer (stage 2)** | Review an assessment or moderation decision de novo | Decide independently of the original decider | Curator; original assessor | **vacant** |
| **Successor** | Assume Curator powers on a succession trigger | Accept in writing in advance | — | **vacant** |
| **Records Keeper** | Hold archival copies; attest retrievability | Verify archive classes annually | — | **vacant** (function performed by Curator) |
| **Counsel** | Review licence text for enforceability | Record `counsel_reviewed` on governing instruments | — | **vacant** |
| **Harm Reviewer** | Run the [RB-05](../rubrics/rb-05-harm-review-gate.md) gate | Return or pass work; publish outcome | Author of the work reviewed | **vacant** |
| **Agent** (non-human) | The four powers in [AG-000 §2](../agents/ag-000-agent-constitution.md) | The three duties in AG-000 §4 | **All human roles** | *(instances, not a chair)* |

### 3.2 Vacancy consequences

| Vacant role | What stops | What degrades | Recorded at |
|---|---|---|---|
| Ratifying Authority | Nothing formally; **24 `RAT-` questions remain open indefinitely** | Every open question is a governing ambiguity | [RAT register](../00-governance-map/open-questions-and-ratifications.md) |
| Appeal Reviewer | **Credential issue** ([REG-05 §3.3](reg-05-credential-registry.md)); stage 2 appeals | MX-016's central guarantee is unavailable | [MX-016](../corpus/mx-016-appeals-and-due-process.md) |
| Successor | Nothing now; **everything on a trigger** | Continuity is unplanned in fact though planned on paper | [MX-015](../corpus/mx-015-succession-and-continuity.md) |
| Records Keeper | Independent attestation of the archive | Two texts already unretrievable ([DEF-029](../00-governance-map/defect-register.md)) | [GM-12](../00-governance-map/archive-register.md) |
| Counsel | `counsel_reviewed` can never be set true | Licence enforceability is self-assessed | [enforceability table](../license/enforceability-two-track-table.md) |
| Harm Reviewer | Independent RB-05 gating | Estate reviews its own harm work; returns RETURNED on itself | [RB-05](../rubrics/rb-05-harm-review-gate.md) |

### 3.3 The Agent is not a chair

Agents — AI systems operating under [AG-000](../agents/ag-000-agent-constitution.md) —
hold four enumerated powers and are **incompatible with every human role**. An
agent cannot ratify, cannot review an appeal, cannot attest an archive, and cannot
be a successor. This is stated as an incompatibility rather than a capability
judgement: even if a system could perform the reasoning, the guarantees those
roles provide are guarantees *to persons* about *persons*, and are not satisfiable
by a system that cannot be held to account.

This has an uncomfortable corollary for the present document. **This register was
drafted by an agent.** An agent describing the vacancies that its own
incompatibilities prevent it from filling is doing something structurally odd, and
the oddity is disclosed in the front matter rather than smoothed over.

## 4. Worked instance

**Following one vacancy to its consequence: Counsel.**

[ST-02](../standards/st-02-front-matter-schema.md) defines a conditional front
matter field `counsel_reviewed`. The
[enforceability two-track table](../license/enforceability-two-track-table.md)
distinguishes provisions likely enforceable as legal terms from those operating as
stated commitments. That distinction is a **legal** judgement.

Now trace it:

| Step | State |
|---|---|
| Field exists in the schema | Yes |
| Any instrument with `counsel_reviewed: yes` | **None** |
| Who may set it | Counsel |
| Counsel holder | **vacant** |
| So the two-track table's classifications are | **self-assessed by a non-lawyer** |
| And [ML-2.3](../license/the-maher-license.md)'s condition/covenant split (§F.4) is | likewise self-assessed |

The §F.4 split — four conditions terminating automatically, nineteen covenants
curable in 30/90 days — is a *load-bearing* legal architecture. If the split is
wrong, the consequences are not documentary: a purported automatic termination
that is actually a curable breach is an over-claim of remedy against a real
licensee.

So the vacancy of Counsel is not a missing nicety. It means the estate's most
consequential legal structure carries an **E0** evidence class on its central
classification, while being written in the confident register of settled law. That
gap is the estate's largest unmitigated exposure, and it is worth more than the
prose it would take to describe it further.

**What the estate does about it:** nothing yet, and it says so. The honest
interim measure — labelling the two-track table's every row as self-assessed —
is partially done at
[§6 of that table](../license/enforceability-two-track-table.md) and should be
done at the head of the document, not only in a later section.

## 5. The register

| Role | Holder | Appointed | Accepted in writing | Vacancy since | Blocking? |
|---|---|---|---|---|---|
| Curator | Maher | inception | yes (Charter) | — | — |
| Ratifying Authority | — | — | — | inception | S2 |
| Appeal Reviewer (stage 2) | — | — | — | inception | **S1** |
| Successor | — | — | — | inception | S2 |
| Records Keeper | — | *(de facto Curator)* | no | inception | S2 |
| Counsel | — | — | — | inception | S2 |
| Harm Reviewer | — | — | — | inception | S2 |

**One of seven filled.** The Curator role is also, de facto, performing the
Records Keeper function, which §2.2 does not mark incompatible but which removes
the independent attestation that made the role worth creating.

### 5.1 Roles the estate has declined to create

| Declined role | Why |
|---|---|
| Moderator (delegated) | Red lines in [MX-008](../corpus/mx-008-moderation-and-enforcement.md) are published and non-discretionary; a delegated moderator would need discretion |
| Community manager | Implies an engagement function refused by [MX-023](../corpus/mx-023-attention-and-human-sovereignty.md) |
| Growth / partnerships | Would require the referral instruments forbidden by [ST-23](../standards/st-23-affiliate-and-referral.md) |
| Data steward | No dataset about people exists to steward ([REG-06](reg-06-dataset-registry.md)) |

Declining a role is a real decision and is recorded so that its later creation is
visibly a reversal.

## 6. Failure modes

| # | Failure | Mechanism | Current state |
|---|---|---|---|
| F1 | **Self-review** | One person holding incompatible roles in fact | **Occurring** — Curator performs Records Keeper and, in substance, Harm Reviewer |
| F2 | **Paper roles** | A chair listed as existing to imply capacity | **Prevented here** — every vacancy is printed |
| F3 | **Residual authority creep** | "Necessary" powers accruing to the Curator | Guarded by §2.1; unaudited, and the Curator is the auditor |
| F4 | **Acceptance never obtained** | A named successor who has not agreed | No successor named, so latent |
| F5 | **Agent role drift** | An agent performing a reserved human act | Guarded by [AG-009](../agents/ag-009-prohibited-actions.md); **7 of 12 prohibited acts have been attempted** |
| F6 | **Vacancy normalisation** | Long vacancy ceases to feel like a defect | **Occurring** — every vacancy dates from inception |

F5 deserves emphasis. [AG-009](../agents/ag-009-prohibited-actions.md) records
twelve prohibited agent acts of which **seven have actually been attempted**. The
prohibitions are therefore doing real work, and the boundary between agent
capability and reserved human authority is under live pressure, not theoretical.

## 7. Limits

1. **The register is maintained by the only role holder.** Every statement about
   the Curator's conduct is self-reported. There is no arrangement under which
   that changes without a second person.
2. **"Blocking?" severities are self-assigned** under
   [REG-07 §2.2](reg-07-defect-classification-registry.md) by the same classifier.
3. **No role has a stated compensation, term, or time commitment**, which is the
   practical reason the chairs are empty. A vacancy with no offer attached is not
   a recruitment problem; it is an unmade decision, and it is filed as
   [RAT-04](../00-governance-map/open-questions-and-ratifications.md).
4. **No Arabic text**, while `prevailing_text: ar` — and for a register of
   authority, the absence of the prevailing text means the authoritative statement
   of who holds power does not exist.
5. **The Agent row is not a person and cannot be one.** The estate's productive
   capacity is concentrated in an actor that is constitutionally barred from every
   role that would make the corpus operational. That is the structural shape of
   this whole project and is stated plainly rather than left for a reader to
   notice.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** any act reserved to a vacant role is shown to have been performed —
>   which would mean either the role is not vacant or the reservation was breached;
> - **(b)** any instrument carries `counsel_reviewed: yes`;
> - **(c)** a stage 2 appeal is shown to have been decided;
> - **(d)** a credential exists, contradicting the §3.2 consequence chain and
>   [REG-05](reg-05-credential-registry.md);
> - **(e)** a power is exercised that is not enumerated in §3.1.
>
> **(e) is the important one** and the hardest to check, because residual power is
> exercised invisibly. The estate offers the enumeration in §3.1 as the test and
> accepts that only an outside reader can apply it.

## 9. Obligation

No obligation arises from a record. Bearing duties:

- Do not perform an act reserved to a role one does not hold —
  [MX-000 Charter](../corpus/mx-000-charter.md).
- Do not hold incompatible roles; where unavoidable, **print it** — §2.2, and
  §5 does.
- Obtain written acceptance before naming a successor —
  [MX-015](../corpus/mx-015-succession-and-continuity.md).
- Agents observe AG-000 powers and [AG-009](../agents/ag-009-prohibited-actions.md)
  prohibitions; escalate rather than assume authority —
  [AG-004](../agents/ag-004-refusal-and-escalation-register.md).
- Do not issue credentials while stage 2 is vacant —
  [REG-05](reg-05-credential-registry.md).

---

### Related

**Roles and continuity** — [MX-015](../corpus/mx-015-succession-and-continuity.md) ·
[MX-016](../corpus/mx-016-appeals-and-due-process.md) ·
[MX-000 Charter](../corpus/mx-000-charter.md) ·
[RAT register](../00-governance-map/open-questions-and-ratifications.md)

**Agents** — [AG-000](../agents/ag-000-agent-constitution.md) ·
[AG-004](../agents/ag-004-refusal-and-escalation-register.md) ·
[AG-009](../agents/ag-009-prohibited-actions.md) ·
[MX-007](../corpus/mx-007-ai-use-and-disclosure.md)

**Consequences of vacancy** — [REG-05](reg-05-credential-registry.md) ·
[RB-05](../rubrics/rb-05-harm-review-gate.md) ·
[enforceability table](../license/enforceability-two-track-table.md) ·
[DEF-031](../00-governance-map/defect-register.md)

**Siblings** — [REG-01](reg-01-series-registry.md) ·
[REG-06](reg-06-dataset-registry.md) ·
[REG-07](reg-07-defect-classification-registry.md)

### Exit pair

1. **Fill one chair.** Stage 2 Appeal Reviewer is the **S1**; filling it unblocks
   credentials and MX-016's central guarantee.
2. **Read the exposure.** [§4](#4-worked-instance) above, then the
   [enforceability two-track table](../license/enforceability-two-track-table.md) —
   a legal architecture with no legal review.

<!-- mx-pagestamp: REG-08 · v2026.10.1 · record · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; no role appointment has occurred through it -->
