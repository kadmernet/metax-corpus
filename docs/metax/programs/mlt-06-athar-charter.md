---
doc_id: "MLT-06"
title_en: "MLT-06 · Athar: Trace and Record. Programme Charter"
title_ar: "MLT-06 · أثر: الأثر والسجلّ [AR-DRAFT]"
family: "metax"
version: "v2026.10.3"
status: "draft"
authority: "governing within MLT-06, on adoption"
prevailing_text: "en"
audience_tier: 3
depth: 4
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-08"
domain_tags: ["metax", "MLT-06", "athar", "provenance", "archives", "attestation", "deep-time", "HX-12", "HX-23"]
route: "/metax/programs/athar/charter/"
programme_status_declared: "research-preview"
programme_status_charter_rule: "planned"
human_read: "none"
conformance_state: "partial"
derived_from: "Bundle Part 5 §5.2 MLT-06; part 5 agent-proposed"
authorship_note: "Parts 1–4, 6 and 7 are from the Curator-supplied bundle. Part 5, the objections section and the falsifier are AI-drafted proposals."
hreflang: "en, ar"
---

# MLT-06 · Athar: Trace and Record

> **Conformance declaration (§H.19).** Machine-assisted draft. `human_read: none`. Not governing until adopted.

> **Disclosure first.**
> - The bundle says Athar "supplies Part J D1 and the verification-bundle design". Part J is Family B's and **not adopted** (GM-16 D-07). The corresponding adopted text is HX-000 v2027.1 §12 D1 and ML-2.4 §E.10.
> - The estate itself fails this programme's founding question today. No key exists (CR-01), so a stranger in eighty years could not establish who said anything in this corpus.

---

## 1. Founding question

**What must be true of a record for a stranger in eighty years to establish what it says and who said it?**

## 2. Scope

- Provenance chains.
- Content addressing.
- Format obsolescence and migration.
- Archival institutions and their failure modes.
- The two-sided problem of preservation and expiry.
- Cryptographic attestation over deep time.

## 3. Exclusions

- **No blockchain advocacy, and no blockchain critique framed as advocacy for anything else.**
- **No DRM.**
- **Costly exclusion.** The programme will not endorse any specific archival vendor or protocol, which is the question every practitioner actually asks it.

## 4. Method

- Historical analysis of archival failure.
- Formal work on attestation lifetimes.
- Every claim about a format's longevity carries a **dated basis**.

## 5. Evidence policy *(agent-proposed)*

| Strength | Admissible support |
|---|---|
| `position (P1)` | Analysis, or a formal argument about attestation |
| `supported position` | A documented historical archival failure or survival, read by a named human with locator. Or a published cryptanalytic result with its date |

Specific rules:
- **Longevity claims are perishable** (ST-05). Each carries a review date no later than 3 years out, whatever the claim's tone.
- **The estate's own records are a case, not a proof.** A claim that the estate's method works may cite the estate only after an independent party has attempted verification from the static artefacts alone.
- Common rule E-0 applies.

## 6. Status and gates

- **Declared:** `research-preview`.
- **Charter rule:** `planned`.
- **Proposed gates:**
  - G-At1: a key exists and one artefact is signed, so the programme has a live case (B-01).
  - G-At2: `/license/digests.txt` is published as a static file (ST-34 §1).

## 7. Sunset criteria

**Wound down if a durable standard emerges that the programme has not shaped.**

*Strength: weak.* It has the same defect as MLT-04: it rewards influence, not correctness. If a sound
standard emerged without Athar, that would be a good outcome, and the programme's work would be done
rather than failed. **Proposed replacement:** wound down when (a) a published, independently implemented standard
meets the founding question's test for a named record class, so the question is answered for that class by
others, **and** (b) the estate adopts it for its own records.

---

## Key positions (P1)

1. **Signature schemes have shorter reliable lifetimes than the records they attest.** Deep-time attestation is therefore a re-attestation problem, not a signing problem.
2. **Preservation and expiry are one obligation, not two.** An institution that decides only one has decided neither. *(This matches ML-2.3 §H.28(c) and (e) and the §H.31.3 conflict rule.)*
3. **The most reliable long-term format property is redundant independent implementation, not openness.**

## Dependencies

- **Supplies:** the design of the migration obligation (ML-2.4 §H.28 am.), the Migration Ledger, and `/license/digests.txt`.
- **Depends on:** B-01 and B-02.

## Objections (strongest counter-argument, without reply)

Eighty years is beyond any evidence the programme can gather, so its founding question can only be
answered by analogy with archives that survived for reasons nobody planned. The historical record of
deliberate deep-time preservation is mostly a record of failure. The survivors were accidents. A
programme that studies how to design what has historically survived only by accident may be studying
something that cannot be designed.

## Falsifier (for this charter)

The charter is defective if the estate publishes a longevity claim about its own records that this
programme's evidence policy would reject.

---

**Related:** [MLT-000](mlt-000-programme-register.md) · [ML-2.4 §H.28 am., §E.10](../../license/ml-2-4.md) · [ST-34](../../standards/st-34-licence-and-register-machine-forms.md) ·
[REG-12](../../registries/reg-12-processors-keys-mirrors.md) · [Continuity Register](../../00-governance-map/continuity-register.md) · [GM-17](../../00-governance-map/corpus-review-v2027.1.md)
