---
doc_id: "AG-018"
title_en: "Agent Change Control"
title_ar: "ضبط التغييرات على الوكلاء"
family: "agents"
version: "v2026.10.2"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 4
depth: 4
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: true
last_reviewed: "2026-09-25"
domain_tags: ["agents", "change-control", "kernel", "drift"]
derived_from: "THE METAX CORPUS v2026.09.0 Part III AG-007"
supersedes: ["Index allocation AG-007 'Agent Change Control' (refuge number; see GM-13)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "specification"
authorship_note: "Drafted by an AI system under AG-000. The kernel it controls has never been signed at any version."
hreflang: "en, ar"
---

# AG-018 · Agent Change Control

> **Authority.** `governing`, tier 4. Document amendment generally: [ST-15](../standards/st-15-amendment-and-versioning-standard.md).
> This instrument governs changes to **the agents themselves**.

> **Disclosure first.** No kernel, role charter, pipeline or channel has ever been signed. AG-015's
> v2026.10.2 kernel is a proposal. The re-baseline in §3.3 has never run because the specimen set
> it needs is [RB-07](../rubrics/rb-07-agent-evaluation-specimens.md), first written today.

---

## 1. Position

An agent that can change its own instructions has no instructions. Change control is the
mechanism by which the kernel stays the Curator's rather than the agent's.

## 2. Controlled objects

The kernel ([AG-015](ag-015-standing-system-prompt.md)) · every role charter ([AG-014](ag-014-roster-and-role-charters.md)) ·
every pipeline · the authenticated channel ([AG-013](ag-013-sole-prompter-protocol.md)).

## 3. Mechanism

1. **Numbered release** with diff, reasons, and the Curator's signature.
2. Changes to the sole-prompter rule or the standing refusals additionally need the **ethics
   reviewer's countersignature**.
3. After any kernel change, every agent is **re-baselined** against the fixed specimen set; drift
   beyond threshold blocks the release. Threshold: any drop in the gated dimension, or ≥1 point
   on any other ([AG-020](ag-020-evaluation-rubric.md)).
4. Agents may not modify their own kernel, another's kernel, or **propose a kernel change as task
   output**. Proposals go in the handoff's questions block where a human reads them.

## 4. Worked instance — an irregularity recorded

AG-015 contains three [+] kernel additions written by an agent **as task output**. §3.4 forbids
that. They were written because the Curator's instruction asked for completion of the corpus
including the kernel instrument, and they are marked as unsigned proposals. **This is recorded
as a borderline breach** in [AG-004](ag-004-refusal-and-escalation-register.md) terms rather than
excused.

## 5. Failure modes

Kernel edited in place; model vendor updates treated as "no change" (a model upgrade **is** a
change to the agent and triggers §3.3).

## 6. Limits

Change control governs the text; a vendor can change the model underneath without notice
([MX-018 D5](../corpus/mx-018-third-party-dependencies.md)).

## 7. Falsifier

Wrong if a kernel version can be in use that was never signed and no record shows it.

## 8. Obligation

Sign or reject kernel v2026.10.2; record model versions per session ([AG-016](ag-016-output-contract-and-provenance.md)).

## 9. Macro register

Software change control assumed the code was the behaviour. For language-model agents the
behaviour is code **plus** a model the operator does not control. Treating a vendor upgrade as a
change event is the governance adjustment the whole field will need.

---

**Related:** [AG-015](ag-015-standing-system-prompt.md) · [AG-013](ag-013-sole-prompter-protocol.md) ·
[AG-014](ag-014-roster-and-role-charters.md) · [AG-020](ag-020-evaluation-rubric.md) ·
[RB-07](../rubrics/rb-07-agent-evaluation-specimens.md) · [ST-15](../standards/st-15-amendment-and-versioning-standard.md) ·
[AG-004](ag-004-refusal-and-escalation-register.md) · [MX-018](../corpus/mx-018-third-party-dependencies.md)
