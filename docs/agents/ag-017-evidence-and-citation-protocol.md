---
doc_id: "AG-017"
title_en: "Evidence and Citation Protocol"
title_ar: "بروتوكول الأدلة والاستشهاد"
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
domain_tags: ["agents", "evidence", "citation", "fabrication"]
derived_from: "THE METAX CORPUS v2026.09.0 Part III AG-006, AG-000 §A.5"
supersedes: ["Index allocation AG-006 'Evidence and Citation Protocol' (refuge number; see GM-13)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "specification"
authorship_note: "Drafted by an AI system under AG-000. The agent that wrote this protocol has no canonical bibliography to draw from; none exists."
hreflang: "en, ar"
---

# AG-017 · Evidence and Citation Protocol

> **Authority.** `governing`, tier 4. The estate-wide evidence rule is
> [ST-07](../standards/st-07-evidence-and-verify.md) (tier 5, form) under
> [MX-026](../corpus/mx-026-editorial-and-evidence.md) (tier 3, policy). This protocol is what an
> **agent** must do.

> **Disclosure first.** **The canonical bibliography does not exist.** §2 requires sources to come
> from it or from the Curator. In practice every source in the corpus came from uploaded files,
> and no external source has been retrieved and quoted in a handoff as §3 requires.

---

## 1. Position

The single worst thing an agent can do is invent a fact, source, date, count or quotation. It is
worse than incompleteness, error or refusal, because the corpus rests on the claim that its
sources are real. Language models produce plausible citations fluently; the protocol exists
because that fluency is the hazard.

## 2. Where sources may come from

1. The canonical bibliography (to be created as `library/sources/bibliography/`).
2. The Curator.
3. A source the agent **retrieved and read** in the task — never one remembered.

An agent may *propose* a source; it may never *assert* one it was not given or did not retrieve.

## 3. What a citation carries

Author · year · title · locator · retrieval date · decay class · **quoted supporting passage in
the handoff** (not just a URL).

## 4. Contradictions

- Source contradicts a corpus claim → report; do not resolve.
- Two corpus documents contradict → quote both verbatim with paths; stop.

## 5. Numbers

Reproduce the number **exactly as the source states it**, with its units and conditions.
Restating a figure under different conditions is fabrication even when the digits match — the
named case is the DishBrain/DeepMind comparison ([MX-026 §7](../corpus/mx-026-editorial-and-evidence.md)).

## 6. Worked instance

The BCIA status patch lists dated claims — 1961 Landauer, 1937 Shannon, 1945 EDVAC, 1947 Bell
Labs ([source](../../sources/00_BCIA_STATUS_PAGE_PATCH_v2026.08.14.md)). This protocol forbids an
agent from "confirming" them from memory. They stay open under BCIA Gate 6 until a retrieved
source is quoted.

## 7. Failure modes

Memory citations; URL-only citations; "widely reported"; rounding a figure; citing a secondary
source as primary.

## 8. Limits

Retrieval proves the source exists and says the words; it does not prove the source is right.

## 9. Falsifier

Wrong if a citation that satisfies §3 is later found to misquote its passage.

## 10. Obligation

Create the bibliography file; run the L-1 source pass ([AG-011](ag-011-agent-review-and-audit.md)).

## 11. Macro register

When fabricated citations become cheap, **the cost of checking falls on every reader forever**.
Quoting the passage at the moment of citation moves that cost back to the one party who could pay
it once.

---

**Related:** [ST-07](../standards/st-07-evidence-and-verify.md) · [MX-026](../corpus/mx-026-editorial-and-evidence.md) ·
[AG-000](ag-000-agent-constitution.md) · [AG-011](ag-011-agent-review-and-audit.md) ·
[AG-015](ag-015-standing-system-prompt.md) · [AG-016](ag-016-output-contract-and-provenance.md) ·
[BX-012](../bcia/bx-012-remediation-gates.md) · [Verification Log](../00-governance-map/verification-log.md)
