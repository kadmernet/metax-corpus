---
doc_id: "REG-10"
title_en: "Academy Registry"
title_ar: "سجل الأكاديميات"
family: "registries"
version: "v2026.10.2"
status: "canonical"
authority: "record"
prevailing_text: "en"
audience_tier: 2
depth: 2
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-25"
domain_tags: ["registries", "academies", "directory"]
route: "/academies/record/directory/"
derived_from: "MX-029 §§2, 4, group 11; source MX-004 §4.5"
supersedes: ["Index allocation REG-06 'Academy Registry' (refuge number; see GM-13)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "record"
authorship_note: "Compiled by an AI system under AG-000. The register is empty."
hreflang: "en, ar"
---

# REG-10 · Academy Registry

> **Authority.** A **record**. The rules are in [MX-029](../corpus/mx-029-academies-charter.md). The
> manifest each academy publishes is specified in [ST-31](../standards/st-31-academy-json-manifest.md).

> **Disclosure first.** **No academy exists at any level.** No application has been received.
> Applications cannot open until MetaX itself meets requirement groups 4 (reviewers) and 5
> (ethics reviewer and succession).

---

## 1. Columns

| Column | Meaning |
|---|---|
| `slug` | Subdomain label |
| `name` | English and Arabic |
| `curator` | Display name; pseudonym flag |
| `level` | L1–L5 |
| `status` | `active` · `suspended` · `revoked` |
| `first_listed` | Date |
| `last_audit` | Date and link |
| `open_findings` | Count, computed from audit reports |
| `manifest` | URL of `academy.json` |
| `tombstone` | URL, if revoked |

## 2. Rows

*(none)*

## 3. Rules

- Suspended and revoked academies stay listed **beside** active ones.
- A row is never deleted. A revoked academy's row points to its dated tombstone.
- Each row must agree with the academy's own `academy.json`. A disagreement is a defect in both.

## 4. Counts

Computed from the rows. Currently 0 active, 0 suspended, 0 revoked.

## 5. Falsifier

This register is wrong if an academy is operating on a `*.metax.academy` subdomain with no row
here.

---

**Related:** [MX-029](../corpus/mx-029-academies-charter.md) · [ST-31](../standards/st-31-academy-json-manifest.md) ·
[MX-016](../corpus/mx-016-appeals-and-due-process.md) · [MX-027](../corpus/mx-027-trademark-and-brand.md) ·
[REG-05](reg-05-credential-registry.md) · [REG-11](reg-11-determinations-registry.md) ·
[ST-33](../standards/st-33-assessment-and-academy-templates.md) · [MX-025](../corpus/mx-025-credentialing-and-assessment.md)
