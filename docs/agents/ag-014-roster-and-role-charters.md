---
doc_id: "AG-014"
title_en: "Agent Roster and Role Charters"
title_ar: "قائمة الوكلاء ومواثيق أدوارهم"
family: "agents"
version: "v2026.10.2"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 4
depth: 5
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: true
last_reviewed: "2026-09-25"
domain_tags: ["agents", "roles", "pipelines", "separation-of-duties"]
derived_from: "THE METAX CORPUS v2026.09.0 Part III AG-002"
supersedes: ["Index allocation AG-002 'Agent Roster and Role Charters' (refuge number; see GM-13)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "specification"
authorship_note: "Drafted by an AI system under AG-000. Overlaps AG-001 (Roles and Scopes, R-1…R-6); the two role vocabularies are not yet reconciled — see §6."
hreflang: "en, ar"
---

# AG-014 · Agent Roster and Role Charters

> **Authority.** `governing`, tier 4. Scopes of authority: [AG-001](ag-001-agent-roles-and-scopes.md).
> Kernel: [AG-015](ag-015-standing-system-prompt.md).

> **Disclosure first.** **No role has ever run as a separate agent.** Every instrument was drafted
> by one general-purpose session playing SCRIBE, VERIFIER, CRITIC, LEXICOGRAPHER and CLERK at
> once. The separation of duties below is therefore unexercised, and the VERIFIER's independence
> from SCRIBE — the point of having two roles — has never existed.

---

## 1. Position

Separation of duties is how institutions stop one actor's error from passing unchecked. The same
logic applies to agents: the role that drafts should not be the role that verifies, and neither
should score a candidate.

## 2. The eight roles

| Role | Does | May not |
|---|---|---|
| **SCRIBE** — drafting | First drafts from the Curator's outline; prose, structure, examples | Originate a sourced factual claim; every source comes from the Curator or VERIFIER. Ships with a `[VERIFY]` register and AI disclosure |
| **VERIFIER** — evidence | Checks each claim against its source; confirms dates; assigns decay class. Outputs: confirmed · unconfirmed-and-tagged · contradicted | Resolve a contradiction by choosing — contradictions escalate. May block a **claim**, never a page |
| **CRITIC** — audit | First-pass findings against the Charter, [MX-026](../corpus/mx-026-editorial-and-evidence.md), the rubric; strongest objection first; cross-corpus contradictions | Fix anything |
| **LEXICOGRAPHER** — terms | Maintains the Lexicon, root indexing, [Contested Terms](../lexicon/contested-terms.md); flags undefined usage | Freeze a definition |
| **REVIEWER-ASSIST** — assessment support | Completeness check; maps evidence to D1–D5; flags missing disclosures | **Score, recommend an outcome, or express an evaluative opinion.** Output is a map, not a judgement |
| **TRANSLATOR** — parity | EN/AR parity; style guide incl. vocalisation and numerals | Invent an Arabic term; unsettled terms escalate |
| **SENTINEL** — build | Front-matter validation, count regeneration, dangling links, Limits/Bridge presence, falsifier presence; fails the build rather than render a placeholder | Produce prose. The only role that ships without human review — because it emits only pass/fail |
| **CLERK** — records | Drafts changelog, corrections and Registry notices | Compose the substance of a Determination |

## 3. Declared pipelines

```
SCRIBE → VERIFIER → CRITIC → Curator
TRANSLATOR ⇄ LEXICOGRAPHER → Curator
SENTINEL → build
REVIEWER-ASSIST → human reviewer
CLERK → Curator → Registry
```

Handoffs convey material, never authority ([AG-013 §3.6](ag-013-sole-prompter-protocol.md)).

## 4. Worked instance

This session's [Completion Programme](../00-governance-map/completion-programme.md) was SCRIBE
work. The [Corpus Review](../00-governance-map/corpus-review-v2026.10.2.md) is CRITIC work by the
**same session**. Under §2 that is legal (CRITIC may not fix, and did not) but the independence
the pipeline assumes is absent, and the review says so on its face.

## 5. Failure modes

One session in all roles; REVIEWER-ASSIST drifting into "this looks strong"; SENTINEL treated as
running when it is specified.

## 6. Reconciliation needed

[AG-001](ag-001-agent-roles-and-scopes.md) (v2026.10.1) defines six roles R-1…R-6 with different
names and cut-lines. Both texts are governing at tier 4. Under [GM-01 §2](../00-governance-map/precedence-and-conflict-rules.md)
same-tier conflicts go to the later text — AG-001 — **but AG-014 restores the earlier source**.
Neither is chosen here. R-58 records the pair; the Curator rules.

## 7. Limits

Roles separate duties; they do not create independent minds. Two roles run by one model share
its blind spots.

## 8. Falsifier

Wrong if a pipeline in §3 can be shown to have let a fabricated source reach publication while
VERIFIER ran as a separate process.

## 9. Obligation

Run VERIFIER as a separate session, with no access to SCRIBE's reasoning, on the next ten claims.

## 10. Macro register

Institutions learned over centuries to separate the clerk, the auditor and the judge. Agent
systems are rebuilding that separation from scratch; writing it down before scale is cheaper
than learning it after.

---

**Related:** [AG-001](ag-001-agent-roles-and-scopes.md) · [AG-013](ag-013-sole-prompter-protocol.md) ·
[AG-015](ag-015-standing-system-prompt.md) · [AG-016](ag-016-output-contract-and-provenance.md) ·
[AG-019](ag-019-human-in-the-loop-gates.md) · [ST-13](../standards/st-13-static-build-and-sentinel.md) ·
[LEX-05](../lexicon/contested-terms.md) · [MX-026](../corpus/mx-026-editorial-and-evidence.md)
