---
doc_id: "PR-1"
title_en: "PR-1 · Pre-registration Form (MX-014 §4)"
title_ar: "PR-1 · نموذج التسجيل المسبق [AR-DRAFT]"
family: "templates"
version: "v2026.10.3"
status: "draft"
authority: "operative-form"
prevailing_text: "en"
audience_tier: 3
depth: 3
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-08"
domain_tags: ["templates", "pre-registration", "research-ethics", "MX-014", "kill-criterion"]
route: "/method/instruments/prereg/"
operative_under: "MX-014 §4"
human_read: "none"
conformance_state: "unmet"
authorship_note: "Drafted by an AI system under AG-000 to close GM-17 M-25. The six MX-014 §4 fields are reproduced exactly. The exclusion checklist and registry rules are added form, and add no obligation."
hreflang: "en, ar"
---

# PR-1 · Pre-registration Form

> **Authority.** An **operative form** implementing [MX-014 §4](../corpus/mx-014-research-ethics-and-exclusions.md).
> MX-014 governs. The desk route it names ("does not exist", MX-014 §7) is specified here and **still
> has no build behind it**.

> **Disclosure first.** No research has ever been pre-registered. While the ethics veto is unheld
> (M-03), a BCIA pre-registration can be filed and **cannot proceed** (BX-010 basis 7: charter before
> experiment, including a published ethics reviewer).

---

## 1. The form

```
PRE-REGISTRATION  PR-{programme}-{YYYY}-{NN}
Programme ........ MLT-__     Registrant (natural person) ____     Filed (UTC) ____
Digest of this form at filing (SHA-256) ____

QUESTION     [what is asked]
HYPOTHESIS   [what is expected]
NULL         [what result would count as no effect]
KILL         [what result would end this line of inquiry]
EXCLUSIONS   [which of MX-014 §§2–3 were considered and how they apply]  ← §2 below, every line answered
PUBLICATION  [committed, in advance, regardless of outcome]  ← where, by when, in full
```

## 2. EXCLUSIONS: every line must be answered

"No exclusion applies" without addressing each line is a failed form (MX-014 §4; RB-05 §2).

| Item | Engaged? | How it applies / why not engaged |
|---|---|---|
| Charter refusal: attention-economic mechanics (MX-000 §0.4.1) | | |
| Charter refusal: Core Riba (§0.4.2) | | |
| Charter refusal: claims beyond evidence (§0.4.3) | | |
| Charter refusal: dark patterns (§0.4.4) | | |
| *MX-014 §2 "laboratory instruction in biology"* | | |
| *MX-014 §2 "sexualisation of minors"* | | |
| MX-014 exclusion 1: human subjects | | |
| MX-014 exclusion 2: human cells and human-derived material, **even theoretically modelled** | | |
| MX-014 exclusion 3: capability uplift (primary-use test) | | |
| MX-014 exclusion 4: covert research on readers | | |
| MX-014 exclusion 5: research the estate cannot publish in full | | |
| BCIA only: refused inference (BX-016); notation freeze (BX-014); method withholding (ML-B-1.0 A-6) | | |

*Rows in italics follow MX-014 §2's list, which differs from MX-000 §0.4's (GM-17 X-20). **Both lists are asked** until the Curator rules, so that no refusal is missed by either reading.*

## 3. Registry rules

1. **Filed before data or analysis begins.** The filing timestamp and digest are published at once, and the registry is append-only.
2. **Amendment after filing** creates a new version with a stated reason. The original stays visible. An amendment filed after any result is known is marked `post-result` and **voids the KILL criterion's protective value**, so the line is treated as unregistered.
3. **Outcome row** is added on completion: `confirmed` · `null` · `killed` · `abandoned`, with the publication link. `abandoned` requires a reason and still triggers PUBLICATION of what exists.
4. **A study with no outcome row 24 months after filing** is shown as `overdue` in Decay Watch.

## 4. Worked instance (from MX-014 §5, filed as a specimen, not a registration)

- **QUESTION:** information-processing dynamics in a simple biological substrate.
- **EXCLUSION 2: engaged.** The dataset includes human-derived lines. **The proposal stops at the form.** The surviving variant uses non-human data only, with a new form.

---

**Related:** [MX-014](../corpus/mx-014-research-ethics-and-exclusions.md) · [MLT-000](../metax/programs/mlt-000-programme-register.md) · [BX-010](../bcia/bx-010-document-zero-and-research-charter.md) ·
[RB-05](../rubrics/rb-05-harm-review-gate.md) · [MX-000 §0.4](../corpus/mx-000-charter.md) · [GM-17](../00-governance-map/corpus-review-v2027.1.md)
