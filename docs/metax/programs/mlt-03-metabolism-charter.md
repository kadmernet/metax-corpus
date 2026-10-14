---
doc_id: "MLT-03"
title_en: "MLT-03 · Metabolism: Energy and Flow. Programme Charter"
title_ar: "MLT-03 · الأيض: الطاقة والتدفّق [AR-DRAFT]"
family: "metax"
version: "v2026.10.3"
status: "draft"
authority: "governing within MLT-03, on adoption"
prevailing_text: "en"
audience_tier: 3
depth: 4
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-08"
domain_tags: ["metax", "MLT-03", "metabolism", "energy", "water", "LCA", "jevons", "HX-10"]
route: "/metax/programs/metabolism/charter/"
programme_status_declared: "research-preview"
programme_status_charter_rule: "planned"
human_read: "none"
conformance_state: "partial"
derived_from: "Bundle Part 5 §5.2 MLT-03; part 5 agent-proposed"
authorship_note: "Parts 1–4, 6 and 7 are from the Curator-supplied bundle. Part 5, the objections section and the falsifier are AI-drafted proposals."
hreflang: "en, ar"
---

# MLT-03 · Metabolism: Energy and Flow

> **Conformance declaration (§H.19).** Machine-assisted draft. `human_read: none`. Not governing until adopted.

> **Disclosure first.** The bundle says this programme "supplies the estate's own D4 and capacity
> accounting". **D4 is a Family B proposal (DT-4, wind-down cost) and is not adopted**, and no capacity
> accounting exists. The estate's own Part H position marks **HX-10 unremedied** (HX-000 v2027.1 §13).
> The programme's first natural object is therefore the estate itself, and that is a conflict of
> interest it must declare, as MLT-05 does.

---

## 1. Founding question

**What is the true resource cost of a computation, counted to the mine and the water table, and what does honest accounting change about what gets built?**

## 2. Scope

- Embodied versus operational energy.
- Water in cooling and in generation.
- Landauer's bound and its practical distance.
- Jevons dynamics in compute.
- E-waste flows.
- Lifecycle assessment methodology and its systematic gaps.

## 3. Exclusions

- **No carbon-offset advocacy.**
- **No vendor sustainability-claim validation.**
- **Costly exclusion.** The programme will not produce a "green computing" framework, which is the only commercially viable output in the area.

## 4. Method

- Published LCA data.
- Vendor disclosures, treated as **claims about documentation** rather than measurements.
- Explicit uncertainty ranges on every figure.

## 5. Evidence policy *(agent-proposed)*

| Strength | Admissible support |
|---|---|
| `position (P1)` | Reasoned from stated boundary assumptions |
| `supported position` | At least one Tier 1–2 LCA or measurement study, read by a named human, **with its system boundary stated** and the figure given as a range |

Specific rules:
- **The boundary is part of the number.** A figure reported without its boundary is inadmissible, because choosing the boundary is how the number is made to look best (HX-10's mechanism).
- **Vendor figures never support a position on their own.** They support only a position *about what the vendor discloses*.
- **Point estimates are forbidden** where the sources disagree by more than a factor of two. Report the range and the reason the sources diverge.
- Common rule E-0 applies.

## 6. Status and gates

- **Declared:** `research-preview`.
- **Charter rule:** `planned`.
- **Proposed gates:**
  - G-Me1: the estate's own boundary statement for its hosting, build and processor footprint is published (the HX-10 self-instance).
  - G-Me2: the three key positions carry V-numbered verification (V-19).

## 7. Sunset criteria

**Wound down if total-sector consumption decouples from output for three consecutive years.**

*Strength.* Strong in form, because it is observable and adverse. It is **weak in reach**. Sector-level
decoupling is measured by others with boundaries the programme distrusts, so the programme would be
sunset by the kind of figure it says is unreliable. **Proposed clarification:** decoupling must hold
under a full-boundary measure (embodied + operational + water), reported as a range whose upper bound
also shows decoupling.

---

## Key positions (P1; [VERIFY] V-19)

1. **For personal devices, embodied carbon dominates.** Support-window length, which is a pure software decision, is therefore the single highest-leverage variable. *(This links to ML-2.3 §H.14: "do not shorten software support windows below hardware service life".)*
2. **Efficiency gains in this sector have never reduced total consumption.** Any projection that assumes they will is a projection, not a finding.
3. **Indirect water use through generation usually exceeds direct cooling use**, and most reporting conflates the two in both directions.

## Dependencies

- **Supplies (planned):** the estate's HX-10 accounting.
- **Depends on:** the processor list (REG-12) and hosting disclosures.

## Objections (strongest counter-argument, without reply)

A programme that refuses to validate vendor claims or produce a framework has chosen to have no
effect on what gets built, which is the second half of its own founding question. Accounting that
nobody adopts changes nothing, and refusing the only adoptable form is a choice for purity over consequence.

## Falsifier (for this charter)

The charter is defective if the programme could publish a resource figure about the estate itself
that omits a boundary the estate controls.

## Annex · Defects filed

New DEF-057: the "D4 and capacity accounting" dependency names an unadopted proposal (DT-4) and an absent artefact.

---

**Related:** [MLT-000](mlt-000-programme-register.md) · [HX-000 v2027.1](../../harms/hx-000-register-v2027-1.md) · [ML-2.3 §H.14](../../license/ml-2-3.md) ·
[REG-12](../../registries/reg-12-processors-keys-mirrors.md) · [Part H Statement](../../license/part-h-statement.md) · [GM-17](../../00-governance-map/corpus-review-v2027.1.md)
