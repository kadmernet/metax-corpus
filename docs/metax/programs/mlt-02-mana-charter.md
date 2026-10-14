---
doc_id: "MLT-02"
title_en: "MLT-02 · Maʿnā: Meaning and Semantics. Programme Charter"
title_ar: "MLT-02 · معنى: المعنى والدلالة [AR-DRAFT]"
family: "metax"
version: "v2026.10.3"
status: "draft"
authority: "governing within MLT-02, on adoption"
prevailing_text: "en"
audience_tier: 3
depth: 4
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-08"
domain_tags: ["metax", "MLT-02", "mana", "semantics", "grounding", "lexicon", "translation"]
route: "/metax/programs/mana/charter/"
programme_status_declared: "research-preview"
programme_status_charter_rule: "planned"
human_read: "none"
conformance_state: "partial"
derived_from: "Bundle Part 5 §5.2 MLT-02; part 5 agent-proposed"
authorship_note: "Parts 1–4, 6 and 7 are from the Curator-supplied bundle. Part 5, the objections section and the falsifier are AI-drafted proposals under AG-000."
hreflang: "en, ar"
---

# MLT-02 · Maʿnā: Meaning and Semantics

> **Conformance declaration (§H.19).** Machine-assisted draft. `human_read: none`. Not governing until adopted.

> **Disclosure first.**
> - The bundle says this programme "feeds `/library/lexicon/` directly" and is "the only programme with a live production dependency". **The lexicon has no entries in the prescribed form** (GM-17 M-31; LEX-02 says that none of LEX-01's twenty entries has the mandatory Arabic field). The dependency is planned, not live.
> - Its method studies drift in "the estate's own Arabic–English corpus". **There is no Arabic corpus** (DEF-002). The method cannot start.

---

## 1. Founding question

**What does a system that manipulates symbols correctly lack, if anything, relative to a system that understands them, and is the difference detectable from outside?**

The "if anything" matters. The programme does not presuppose a deficit. The question is answerable
in principle in two ways: by showing a detectable difference, or by an argument that no outside test
could detect one. Either answer would be a result.

## 2. Scope

- Reference, grounding and compositionality.
- The symbol-grounding problem.
- Translation as an epistemic act.
- Semantic drift in technical vocabularies.
- The relation between a lexicon and the community that maintains it.

## 3. Exclusions

- **No claims about machine consciousness, in either direction.**
- **No benchmark-based claims about understanding.**
- **Costly exclusion.** The programme may not cite model performance on any comprehension benchmark as evidence of anything about meaning, which removes most of the available literature.

The costly exclusion follows from the founding question. If benchmark success settled
understanding, the question would already be answered. Citing benchmarks would presuppose the
answer the programme exists to examine.

## 4. Method

- Philosophical analysis with stated commitments.
- Empirical work on lexicon drift in the estate's own Arabic–English corpus. **That corpus does not yet exist** (see Disclosure).

## 5. Evidence policy *(agent-proposed)*

| Strength | Admissible support |
|---|---|
| `position (P1)` | An argument whose premises are listed, with each premise marked as a commitment or as supported |
| `supported position` | For drift claims: a **measured** change in a governed term's defining instrument or its usage, across at least two dated corpus versions, with the measure published. For conceptual claims: an argument that has survived a published objection under ST-06 |

Specific rules:
- **A drift measurement may use only the estate's own published text**, never readers' text, searches or submissions (MX-014 exclusions 1 and 4).
- **A translation claim must be checked by a human bilingual reader**, named. Machine translation is never evidence about meaning in this programme.
- Common rule E-0 applies.

## 6. Status and gates

- **Declared:** `research-preview`.
- **Charter rule:** `planned`.
- **Proposed gates:**
  - G-M1: at least one lexicon entry exists in LEX-02 form with a human-written Arabic field 2.
  - G-M2: two dated corpus versions exist in both languages, so drift is measurable.

## 7. Sunset criteria

**Wound down if the lexicon-drift instrument produces no signal across two full corpus cycles.**

*Strength.* Moderate to weak. It tests only the empirical half of the programme. The philosophical
half (the founding question) has no sunset. It is also **unreachable today**: the instrument cannot
run without an Arabic corpus, so the clock cannot start. **Proposed addition:** a time-bound
condition. If G-M1 and G-M2 are not met within 24 months of adoption, the empirical method is withdrawn
and the programme is re-chartered as analysis only.

---

## Key positions (P1)

1. **The grounding question is not settled**, and the confident positions on both sides are under-argued.
2. **Translation between languages with different technical traditions is re-derivation, not lossy transmission.** This is why MetaX treats Arabic as authoritative. *Note:* the corpus currently has no Arabic, so this position describes an intention of the estate, not its practice (X-35).
3. **Semantic drift in a governed vocabulary is measurable, and it is a leading indicator of institutional drift.** *Instance:* [LEX-05](../../lexicon/contested-terms.md) records 18 contested terms. Most arose because agent passes defined terms without reading prior definitions. That is drift produced by volume, which bears on UH-03.

## Dependencies

- **Supplies:** the lexicon (planned).
- **Depends on:** the Arabic corpus (RAT-09, RAT-22) and LEX-02 entries (M-31).

## Objections (strongest counter-argument, without reply)

Excluding every benchmark leaves the programme only armchair argument and its own corpus. Its own
corpus is small, written mostly by one author and one machine, and in one language. A drift signal in
that corpus would measure that author's habits, not institutional drift. The programme has excluded
the data that could answer its question and kept the data that cannot.

## Falsifier (for this charter)

The charter is defective if a claim the programme would publish about meaning could be supported by
the very benchmark evidence that §3 excludes, without that support being visible.

## Annex · Defects filed

New DEF-056: the declared live production dependency on `/library/lexicon/` has no object. Also DEF-002 and M-31.

---

**Related:** [MLT-000](mlt-000-programme-register.md) · [LEX-01](../../lexicon/keyword-register.md) · [LEX-02](../../lexicon/lexicon-entry-standard.md) ·
[LEX-05](../../lexicon/contested-terms.md) · [MX-020](../../corpus/mx-020-language-authority.md) · [GM-17](../../00-governance-map/corpus-review-v2027.1.md)
