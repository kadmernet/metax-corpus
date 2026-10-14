---
doc_id: "ST-31"
title_en: "academy.json Manifest Specification"
title_ar: "مواصفات ملف academy.json"
family: "standards"
version: "v2026.10.2"
status: "canonical"
authority: "operative-form"
prevailing_text: "en"
audience_tier: 4
depth: 4
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-25"
domain_tags: ["standards", "academies", "manifest", "json", "machine-surface"]
route: "/academies/operating/technical/"
derived_from: "THE METAX CORPUS MX-004 §4.3(7); MX-DESIGN-001 academy subdomains; Page Content Specification 'technical guide'"
supersedes: ["Index allocation ST-18 'academy.json Manifest Specification' (refuge number; see GM-13)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "specification"
authorship_note: "Drafted by an AI system under AG-000. Field list derived from the design source's description; the schema itself is the agent's."
hreflang: "en, ar"
---

# ST-31 · academy.json Manifest

> **Authority.** `operative-form`, tier 5. Requirement: [MX-029 Annex A](../corpus/mx-029-academies-charter.md).
> Directory: [REG-10](../registries/reg-10-academy-registry.md).

> **Disclosure first.** No academy exists, so no manifest exists. The manifest is also the only
> machine surface **authored by a third party**, which [ST-14](st-14-machine-surfaces-and-json-schemas.md)'s
> "generated, never hand-written" rule does not anticipate (R-59).

---

## 1. Location

`https://{slug}.metax.academy/academy.json` — fixed path.

## 2. Schema

```json
{
  "schema": "metax-academy/1",
  "slug": "podcast-systems",
  "name": { "en": "…", "ar": "…" },
  "curator": { "display": "…", "pseudonym": false, "credential_id": "…" },
  "level": "L3",
  "accent_hue_index": 4,
  "languages": ["en", "ar"],
  "primary_language": "en",
  "ethics_reviewer": "…",
  "succession_clause_url": "/charter/#succession",
  "curriculum": [{ "series": "PS-01", "title": "…", "status": "live" }],
  "audits": [{ "date": "YYYY-MM-DD", "url": "…", "result": "finding|clear" }],
  "status": "active",
  "chrome_version": "v2026.10.1",
  "manifest_version": "v2026.10.2"
}
```

**Build derives** theme ramp (from `accent_hue_index`), routes, and directory entry.
`status` ∈ `active · suspended · revoked`; `suspended` and `revoked` still publish (tombstone).

## 3. Validation

Required fields present; `level` matches REG-10; `chrome_version` within 90 days of the current
release; `ethics_reviewer` and `succession_clause_url` non-empty.

## 4. Falsifier

Wrong if a manifest passing §3 can describe an academy whose REG-10 record says otherwise.

## 5. Macro register

A federation stays honest when each member **describes itself in a form the centre can check**.

---

**Related:** [MX-029](../corpus/mx-029-academies-charter.md) · [REG-10](../registries/reg-10-academy-registry.md) ·
[ST-14](st-14-machine-surfaces-and-json-schemas.md) · [ST-28](st-28-component-library.md) ·
[DS-03](../design/ds-03-responsive-components.md) · [DS-01](../design/ds-01-foundations-and-tokens.md) ·
[MX-020](../corpus/mx-020-language-authority.md) · [ST-33](st-33-assessment-and-academy-templates.md)
