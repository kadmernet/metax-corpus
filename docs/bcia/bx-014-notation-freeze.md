---
doc_id: "BX-014"
title_en: "BCIA Notation Freeze"
title_ar: "تجميد ترميز BCIA"
family: "bcia"
version: "v2026.10.2"
status: "draft"
authority: "governing"
prevailing_text: "en"
audience_tier: 3
depth: 4
evidence_class: "durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-26"
domain_tags: ["bcia", "notation", "freeze", "glossary", "amn", "lpn", "bsn"]
route: "/metax/bcia/notation/"
derived_from: "Source MX-014 §14.4 (notation frozen); 00_BCIA_TAXONOMY_OBSERVED Finding B; 00_BCIA_STATUS_PAGE_PATCH gates 3, 7"
supersedes: ["Legacy slot bx-005-notation-freeze (see GM-13)"]
ratification: "PENDING — RAT-03 (specify or retire BSN/LPN/AMN; gate 7); RAT-25"
provenance_of_purpose: "restoration"
authorship_note: "Drafted by an AI system under AG-000. The role split AMN/BSN/LPN is inferred from context, not stated in the corpus, and is labelled accordingly."
hreflang: "en, ar"
---

# BX-014 · BCIA Notation Freeze

> **Authority.** `governing`. Source MX-014 §14.4: *"The formal notation is frozen and must not be
> taught or cited until the notation contradiction closes."*

> **Disclosure first.** The contradiction in the gate text ("conflicting definitions of AMN and LPN")
> could not be verified: **no definition of either term exists** in the ingested corpus. MX-014 §14.4
> refers to a conflict "between the Arabic chapters and the English glossary", but **no English
> glossary is held**. Either the glossary is lost or it never existed. That question is filed as RAT-28(b).

---

## 1. Position

Three terms are declared and none is specified: **BSN, LPN, AMN**. Status:
**defined-in-intent, undefined-in-specification.**

## 2. Definition — what may be said

| Term | Occurrences (ingested) | Permitted phrasing | Forbidden |
|---|---|---|---|
| AMN | 19 (Books 1–2 only) | "a declared future BCIA language, specification pending" | any definition, any role as working notation |
| LPN | 15 (Books 1–2 only) | same | same |
| BSN | present in the Book 1 triad | same | same |
| D1–D10 | 0 | "a deprecated TopTech-internal tag" | use in Branch D |
| "seven layers" | 0 | "a claim not found in the books" | use as a taxonomy |

**Context-inferred and unconfirmed** (may be quoted only with this label): AMN ≈ the human-command or
intent side; BSN ≈ the biological-signal side; LPN ≈ the bridge between the two. The supporting
passage in Book 1 reads: «من الأوامر الإنسانية (بـ AMN) إلى إشارات حيوية (بـ BSN)».

## 3. Mechanism

1. [RB-06](../rubrics/rb-06-structural-review.md) G4 flags any BCIA term used without the permitted phrasing.
2. Gate 7 closes only when every term in §2 is either **specified** (a formal definition, examples and a counter-example, per the [lexicon entry standard](../lexicon/lexicon-entry-standard.md)) or **retired** (a keyword-register row marked `retired` with a reason).
3. The patch recommends retiring AMN and LPN. Retirement keeps the terms, since numbers and terms are immortal (ST-01 Rule 2). The terms are marked dead but not erased.

## 4. Worked instance

A draft says: "Using AMN, a teacher encodes intent that LPN translates into BSN." That sentence uses
all three terms as working notation and presents the inferred role split as fact. **Fail.** Rewrite:
"Book 1 names three future description languages, AMN, LPN and BSN, whose specifications are pending
([BX-014](bx-014-notation-freeze.md))."

## 5. Failure modes

- **Plausibility capture:** the inferred roles read naturally, so they drift into being treated as definitions.
- **Arabic/English asymmetry:** the terms have Latin acronyms and appear inside Arabic text, which lets English readers assume a formal source exists.
- **Retirement without record:** dropping the terms silently instead of retiring them.

## 6. Limits

The freeze applies to BCIA's own notation. It does not restrict discussion of other notations
(Setun ternary, fuzzy logic and so on) that belong to the settled literature.

## 7. Falsifier

The freeze has failed if any published MetaX page defines AMN, LPN or BSN, or uses D1–D10 in Branch D.

## 8. Obligation

- **Curator:** choose specify or retire for each term (gate 7).
- **Agents:** search for the "English glossary" before assuming it is absent (the AG-015 [+] "list before concluding absence" proposal).

## Macro register

Notation carries authority. A symbol that looks formal will be cited as formal. Freezing the
notation holds that authority back until a specification has earned it.

---

**Related:** [BX-012](bx-012-remediation-gates-and-public-status.md) · [BX-013](bx-013-observed-taxonomy.md) ·
[BX-015](bx-015-critical-audit-and-open-problems.md) · [Keyword register](../lexicon/keyword-register.md) ·
[Lexicon entry standard](../lexicon/lexicon-entry-standard.md) · [LEX-05](../lexicon/contested-terms.md) ·
[MX-014](../corpus/mx-014-research-ethics-and-exclusions.md) · [RB-06](../rubrics/rb-06-structural-review.md)
