---
doc_id: "AG-016"
title_en: "Output Contract and Provenance"
title_ar: "عقد المخرجات والمصدرية"
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
domain_tags: ["agents", "provenance", "output", "audit-trail"]
derived_from: "THE METAX CORPUS v2026.09.0 Part III AG-005"
supersedes: ["Index allocation AG-005 'Output Contract and Provenance' (refuge number; see GM-13)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "specification"
authorship_note: "Drafted by an AI system under AG-000. No artefact in the corpus carries a complete provenance stamp, including this one."
hreflang: "en, ar"
---

# AG-016 · Output Contract and Provenance

> **Authority.** `governing`, tier 4. Output quality: [AG-003](ag-003-agent-output-standards.md).
> Disclosure: [AG-002](ag-002-agent-disclosure-obligations.md). Kernel output blocks:
> [AG-015](ag-015-standing-system-prompt.md).

> **Disclosure first.** **Zero of ~130 instruments carry a complete stamp.** Front-matter
> `authorship_note` records AI drafting; none records model and version, kernel version, task
> identifier, input versions, accepting human, or acceptance date. Under §3, SENTINEL should fail
> every one of them. SENTINEL does not run.

---

## 1. Position

Provenance is what lets a later reader ask "who made this, from what, and who said it was good
enough?" For agent output the question is sharper, because the maker cannot be asked.

## 2. The stamp — nine fields

```yaml
provenance:
  role: SCRIBE                      # AG-014
  kernel: v2026.10.2                # AG-015
  model: "[vendor model id and version]"
  task_id: "T-2026-09-25-01"
  date: 2026-09-25
  inputs: ["sources/THE_METAX_CORPUS.md@v2026.09.0", "..."]
  accepted_by: "[natural person]"
  accepted_on: "[date]"
  channel: "interim-chat"           # AG-013 §3.1
```

## 3. Rule

An artefact with an incomplete stamp **cannot enter the corpus**; SENTINEL fails the build.
Provenance is retained for the life of the artefact plus **seven years**, auditable by the
Curator, the ethics reviewer, and any successor Steward.

## 4. Worked instance

This file: role SCRIBE; kernel not loaded; model **unknown to the agent at the level of version
string** `[VERIFY]` V-16; task — the 2026-09-25 completion instruction; inputs — the uploaded
files listed in [GM-14](../00-governance-map/completion-programme.md); accepted_by — **empty**.
The stamp is incomplete in three fields, and saying which three is the minimum honest act.

## 5. Failure modes

Stamps filled with plausible defaults; `accepted_by` filled with the Curator's name because he
issued the instruction (instruction is not acceptance).

## 6. Limits

A stamp records claims about provenance; it is not proof. Signed commits would be.

## 7. Falsifier

Wrong if an artefact with a complete stamp is later found to have been produced from inputs the
stamp does not list.

## 8. Obligation

Add a `provenance:` block to ST-02 as a conditional field; backfill `accepted_by` only as the
Curator actually accepts.

## 9. Macro register

As machine-written text becomes the majority of text, **the provenance of a sentence becomes a
public good**. An estate that stamps its own output is practising the norm it will need everyone
else to adopt.

---

**Related:** [AG-002](ag-002-agent-disclosure-obligations.md) · [AG-003](ag-003-agent-output-standards.md) ·
[AG-015](ag-015-standing-system-prompt.md) · [AG-019](ag-019-human-in-the-loop-gates.md) ·
[ST-02](../standards/st-02-front-matter-schema.md) · [ST-13](../standards/st-13-static-build-and-sentinel.md) ·
[MX-007](../corpus/mx-007-ai-use-and-disclosure.md) · [Verification Log](../00-governance-map/verification-log.md)
