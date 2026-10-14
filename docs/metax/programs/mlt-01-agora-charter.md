---
doc_id: "MLT-01"
title_en: "MLT-01 · Agora: Collective Decision. Programme Charter"
title_ar: "MLT-01 · أغورا: القرار الجماعي [AR-DRAFT]"
family: "metax"
version: "v2026.10.3"
status: "draft"
authority: "governing within MLT-01, on adoption"
prevailing_text: "en"
audience_tier: 3
depth: 4
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-08"
domain_tags: ["metax", "MLT-01", "agora", "social-choice", "deliberation", "delegation"]
route: "/metax/programs/agora/charter/"
programme_status_declared: "research-preview"
programme_status_charter_rule: "planned"
human_read: "none"
conformance_state: "partial"
derived_from: "Bundle Part 5 §5.2 MLT-01 (parts 1, 2, 3, 4, 6, 7 and key positions); part 5 agent-proposed"
authorship_note: "Parts 1–4, 6 and 7 are reproduced in substance from the Curator-supplied bundle. Part 5 (evidence policy), the objections section and the falsifier are drafted by an AI system under AG-000 and are proposals."
hreflang: "en, ar"
---

# MLT-01 · Agora: Collective Decision

> **Conformance declaration (§H.19).** Drafted with machine assistance. No natural person has read this text in full (`human_read: none`). It is not governing until the Curator adopts it.

> **Disclosure first.**
> - The bundle declares this programme `research-preview` with "2 gates open". It does not say what the two gates are, and this charter cannot name them. Under the umbrella's own rule its status is `planned` (DEF-049).
> - The delegation-depth claim in the key positions has no derivation (V-18).

---

## 1. Founding question

**Under what conditions does a mechanised aggregation of preferences produce a decision that the aggregated parties would endorse on reflection?**

The question is answerable in principle. "Endorse on reflection" can be operationalised against
stated criteria, such as a counterfactual agreement test or a retrospective endorsement under full
information. A mechanism either meets them under stated conditions or it does not. The question is
not "what is the best voting system", which the impossibility results show has no answer independent
of the failures one is willing to accept.

## 2. Scope

- Voting and preference-aggregation mechanisms.
- Deliberation systems.
- Quadratic and conviction methods.
- Sortition.
- The formal impossibility results and their practical reach.
- Reputation and delegation graphs.

The programme treats each mechanism as a claim about which property it gives up. It does not treat any mechanism as a candidate for "the" solution.

## 3. Exclusions

- **No mechanism design for any live political process.**
- **No partisan modelling.**
- **No electoral-outcome forecasting.**
- **Costly exclusion.** The programme declines all consulting on real governance systems, which is where its funding would come from.

The costly exclusion is the one that does work. A programme studying how aggregation produces
decisions that people would not endorse is badly placed to sell aggregation advice. The conflict
would be invisible, because the client would choose the mechanism whose failures it prefers.

## 4. Method

Formal analysis and simulation only. A mechanism enters the position set when:
- its properties are **proved**, or **simulated with published code and seed**; and
- its failure modes are stated.

No simulation result is reported without the parameter range over which it holds.

## 5. Evidence policy *(agent-proposed; awaiting the Curator)*

| Claim strength | Admissible support |
|---|---|
| `position (P1)` | Formal argument with stated assumptions, or a simulation with published code and seed |
| `supported position` | A proof checked by a second party, **or** a simulation replicated by a second party from the published seed, **or** a Tier 1–2 empirical source on a real mechanism, read by a named human |
| — | **No claim about a real electorate's or organisation's reflective endorsement** may be made, because the programme does not study live processes (§3) |

Specific rules:
- **Impossibility theorems are cited in their own terms.** "Arrow shows X" must state the axioms. A theorem stretched beyond its axioms is a Tier 4 claim wearing Tier 1 clothes.
- **Simulation is not observation.** A simulated failure mode supports a position about the model, and becomes a position about the world only with a stated bridge assumption.
- Common rule [E-0](mlt-000-programme-register.md) applies.

## 6. Status and gates

- **Declared:** `research-preview`, "2 gates open", unnamed.
- **Charter rule:** `planned` until the Curator adopts parts 1–7.
- **Proposed promotion gates:**
  - G-A1: the delegation-depth claim is derived or withdrawn (V-18).
  - G-A2: one mechanism analysis is published with code, seed and stated failure modes.

**Series.** MLT-01-S01…S04 are declared `planned`. None is specified. A programme-series registry is owed (REG-14).

## 7. Sunset criteria

**Wound down if three consecutive review cycles produce no position that is not already in the social-choice literature.**

*Strength.* Moderate. It is observable: a reviewer can compare positions to the literature. It is
adverse: a programme that only restates the literature has no reason to exist. Its weakness is that
"not already in the literature" is judged by the programme. **Proposed strengthening:** the novelty
judgement is made by a party outside the programme, named at each cycle.

---

## Key positions (all P1, unverified)

1. **Arrow and Gibbard–Satterthwaite bound what any mechanism can do.** Mechanism choice is therefore a choice of which failure to accept, not a search for a good mechanism. *Status:* reasoned, and standard in the literature. It still needs the axioms stated wherever it is cited.
2. **Delegation graphs concentrate power at a rate proportional to the square of delegation depth.** *Status:* **no derivation given**, and no source. **[VERIFY] V-18.** It is published here only as a claim under examination, never as a position.
3. **Past an unlocated threshold, deliberation quality and participation scale are inversely related.** *Status:* reasoned. The programme admits it has not located the threshold.

## Dependencies

None declared. Agora is the programme closest to the estate's own governance (the Decision Queue,
the comment period CPF-1, and the dissent channel). **It may not study them**, because they are live governance
systems of the estate (§3, applied to itself).

## Objections (the strongest counter-argument, stated without reply)

A programme that refuses to engage with any real governance system will produce work that no real
governance system can use. The impossibility results are fifty years old. Their practical reach is a
matter of empirical institutional detail, and that detail is exactly what the exclusion removes.
Formal analysis without engagement is the most comfortable form of social choice research and the
least consequential.

## Falsifier (for this charter)

This charter is defective if a reader can name a mechanism the programme would analyse that the
exclusions do not distinguish from consulting on a real governance system.

## Annex · Defects filed

- DEF-049 (status).
- V-18 (delegation-depth derivation).
- New DEF-055: the declared "2 gates open" are unnamed anywhere in the corpus or sources.

---

**Related:** [MLT-000](mlt-000-programme-register.md) · [MX-014](../../corpus/mx-014-research-ethics-and-exclusions.md) · [CPF-1](../../license/cpf-1-comment-period-publication-format.md) ·
[Decision Queue spec](../../site/site-08-decision-queue.md) · [Verification log](../../00-governance-map/verification-log.md) · [GM-17](../../00-governance-map/corpus-review-v2027.1.md)
