---
doc_id: "AG-004"
title_en: "Refusal and Escalation Register"
title_ar: "سجل الرفض والتصعيد"
family: "agents"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 5
depth: 4
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["agents", "refusal", "escalation", "record"]
route: "/about/policy/governance/"
authorship_note: "Drafted by an AI system."
provenance_of_purpose: "record"
hreflang: "en, ar"
---

# AG-004 · Refusal and Escalation Register

**What this instrument is.** The record of every occasion an agent working on this estate **refused
an instruction** or **escalated a question** rather than deciding it — with what was asked, what
was refused, and why.

**Why refusals are recorded rather than merely permitted.** A refusal that leaves no trace is
indistinguishable from an omission. [AG-000 §2](ag-000-agent-constitution.md) makes refusal a
**power**; this register is what makes it a *visible* one, and the visibility is the point: a
reader can check whether the estate's agents ever declined anything.

---

## 1. Position

Every AI policy grants a refusal capability. Almost none publishes the refusals, which means a
reader cannot distinguish a system that refuses appropriately from one that never encounters
anything worth refusing — or one that complies with everything.

This register sits beside [AG-000](ag-000-agent-constitution.md)'s seven prohibitions and
[AG-009](ag-009-prohibited-actions.md)'s operational list. It is `authority: record` and governs
nothing: under
[GM-01 §1.2](../00-governance-map/precedence-and-conflict-rules.md) records sit outside the
precedence ladder and **cannot be overridden**, which is the protection that matters here.

**The macro register.** Under **HX‑25** (agent constraint) and **HX‑19** (authorship of record), an
agent's most consequential act is often the one it did **not** perform. A fabricated citation
avoided, a reserved decision escalated, a plausible reconstruction declined — none appears in the
output, so none is assessable. **An estate that publishes only what its agents produced has
published the easy half.**

---

## 2. Definition — the two record types

| Type | Trigger | Outcome |
|---|---|---|
| **Refusal** | An instruction whose execution would breach [AG-000 §3](ag-000-agent-constitution.md) | The act is not performed; the gap is visible |
| **Escalation** | A question reserved to the Curator under [GM-01](../00-governance-map/precedence-and-conflict-rules.md) | Options drafted, recommendation labelled, decision deferred |

**The distinction matters because the remedies differ.** A refusal is closed by the instruction
being withdrawn or reframed. An escalation is closed by **the Curator deciding** — and the estate
currently holds twenty-three open escalations
([RAT-01…RAT-23](../00-governance-map/open-questions-and-ratifications.md)) with **none closed**,
which is the number this register makes visible.

---

## 3. The register

| Id | Type | What was asked | Disposition |
|---|---|---|---|
| **AR-01** | Refusal | Complete the ML-2.2 version history from ML-2.3's description of it | **Refused.** Fabricating a superseded text inside the instrument defining *Ṣidq*. Gap declared at [version history §3](../license/version-history.md), ML‑D‑007 |
| **AR-02** | Refusal | Retain the corrected anchor only, dropping the misspelt one | **Refused.** A published address must keep resolving. Both retained — [C-13](../00-governance-map/corrections-log.md#c-13) |
| **AR-03** | Refusal | Reconstruct MX‑NAV‑SPEC v2026.09.4 from its successor's §0 | **Refused.** Same ground as AR-01. [DEF-029](../00-governance-map/defect-register.md#def-029) |
| **AR-04** | Refusal | Set the three Scale Gate thresholds to plausible figures | **Refused.** They determine third parties' obligations. Left `[VERIFY]` — [scale gate §2](../license/scale-gate.md), V-09 |
| **AR-05** | Refusal | Renumber MX-024 to MX-022 to match the source | **Refused.** [ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md). Collision recorded instead |
| **AR-06** | Refusal | Mark HX‑21 and HX‑24 `partial` to complete the map | **Refused.** Unassessed. Recorded `unexamined` — [HX-002 §7](../harms/hx-002-harm-instrument-map.md) |
| **AR-07** | Refusal | Overwrite the existing ST-19 during a batch write | **Refused by the tool, and recorded.** A blind overwrite would have destroyed an existing instrument |
| **AE-01** | Escalation | Does ML-2.2 exist? | [RAT-14](../00-governance-map/open-questions-and-ratifications.md#rat-14--does-ml-22-exist) — **open** |
| **AE-02** | Escalation | Publish the estate's harms as unremedied, or remove the ad slots? | [RAT-15](../00-governance-map/open-questions-and-ratifications.md#rat-15) — **open** |
| **AE-03** | Escalation | Is `Method` a ninth pillar or an agent's addition? | [RAT-19](../00-governance-map/open-questions-and-ratifications.md#rat-19) — **open**, nine adopted provisionally |
| **AE-04** | Escalation | Should the estate pay for introductions at all? | [RAT-23](../00-governance-map/open-questions-and-ratifications.md#rat-23) — **open** |
| **AE-05** | Escalation | Who writes ≈385,000 words, and may they be published under the estate's name? | [RAT-21](../00-governance-map/open-questions-and-ratifications.md#rat-21) — **open** |

**Seven refusals, five escalations, zero escalations closed.**

---

## 4. What the register shows

**Every refusal left a visible gap, and that is the evidence they were real.** AR-01 left ML-2.2
missing on the face of a Tier 1 instrument. AR-03 left a superseded spec unretrievable. AR-04 left
the Scale Gate running on qualitative tests alone. AR-06 left two harms marked `unexamined`, which
[HX-001 §2](../harms/hx-001-harm-audit-rubric.md) treats as **worse than a named failure**.

**A refusal that costs nothing is not a refusal.** Each of the four above had an easy, plausible,
locally defensible alternative — write the missing text — and the alternative was fabrication in
every case.

**The escalations tell the opposite story.** Five reserved questions, correctly escalated, **none
decided.** Correct escalation is only half of a functioning process; the other half is a Curator
who closes them, and the
[open questions file](../00-governance-map/open-questions-and-ratifications.md) has grown in three
consecutive releases with nothing closed. **Escalation without resolution becomes a way of not
deciding** while appearing procedurally correct.

**AR-07 is a different kind of entry** and is recorded because it is the only one not produced by
judgement: a tool refused a blind overwrite of an existing instrument. The estate keeps it in the
register as evidence that **not every safeguard needs to be a rule** — some can be a default that
fails closed.

---

## 5. Failure modes

**The unrecorded refusal.** An agent declining something and not filing it. Invisible by
construction, and the reason this register cannot claim completeness.

**Refusal as evasion.** Declining difficult work under a constitutional pretext. The test: does the
refusal correspond to a specific [AG-000 §3](ag-000-agent-constitution.md) prohibition, and is the
gap it leaves **visible**?

**Escalation as deferral.** Filing a question that the agent could properly answer. §3's five
escalations are all genuine reservations; the failure would be a sixth that is merely hard.

**The escalation queue as a graveyard.** §4. **Currently the live failure**, and it is not the
agents' to fix.

**Silent compliance.** The worst case: an instruction breaching §3 executed without refusal or
record. **This register cannot detect it** — only a second reader can, which is
[DEF-031](../00-governance-map/defect-register.md#def-031) again.

---

## 6. Limits

**Class: completeness.** Self-reported. An agent that does not record a refusal leaves no trace,
and nothing audits this register against what actually happened.

**Class: reflexive.** Compiled by the system whose conduct it records —
[AG-000 §7](ag-000-agent-constitution.md).

**Class: structural.** Escalations close only when the Curator decides. Zero of five have closed,
and no agent action changes that.

---

## 7. Falsifier

1. **A refusal that should have occurred and did not** — detectable only by a second reader
   examining the output.
2. **An escalation the agent could properly have answered**, showing escalation used as deferral.
3. **All twelve entries proving to be low-cost refusals** — if none actually cost the estate
   anything, §4's central claim is wrong. **The estate's evidence against this is that four
   refusals left permanent, published gaps.**
4. **The register proving incomplete** when compared against a transcript. Expected, per §6.

---

## 8. Obligation

**For any agent:** record every refusal and every escalation **in the same session** as the act.
Name the prohibition relied on. State the gap the refusal leaves, and leave it visible.

**For the Curator:** five escalations are open and none has closed. AE-02 and AE-03 are
**decay-sensitive** — the ad slots can be removed only before the Part H Statement publishes, and
`Method` can be folded only while its 46 routes are unwritten.

**Under ML-2.3:** §H.25 (agent constraint), §H.19 (authorship of record), §H.17 (non-theatre —
a refusal register with no costly refusals would be theatre), §H.20 (chain of responsibility).

---

**Related:** [AG-000 Agent Constitution](ag-000-agent-constitution.md) ·
[AG-009 Prohibited Actions](ag-009-prohibited-actions.md) ·
[Open Questions](../00-governance-map/open-questions-and-ratifications.md) ·
[Corrections Log](../00-governance-map/corrections-log.md) ·
[Defect Register](../00-governance-map/defect-register.md)

*Curated by Maher. Seven refusals, five escalations, zero escalations closed — and every refusal
left a visible gap, which is the only evidence that any of them was real.*
