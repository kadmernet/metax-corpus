---
doc_id: "ST-34"
title_en: "Licence and Register Machine Forms (license.json, hx-000.json, bx-018.json, plain-text siblings)"
title_ar: "الصيغ الآلية للرخصة والسجلات [AR-DRAFT]"
family: "standards"
version: "v2026.10.3"
status: "draft"
authority: "operative-form"
prevailing_text: "en"
audience_tier: 5
depth: 5
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-08"
domain_tags: ["standards", "machine-surfaces", "license-json", "schema", "role-discriminator", "spdx"]
route: "/library/sources/schemas/licence/"
extends: "ST-14 §2 (adds three licence-plane surfaces)"
human_read: "none"
conformance_state: "unmet"
derived_from: "ST-14; ML-2.3 front matter and Part H; HX-000 v2027.1 §14; BX-018; source DEF-2026-073 (no role discriminator)"
authorship_note: "Drafted by an AI system under AG-000 to close GM-17 M-17. ST-14's rule — machine surfaces are generated, never hand-written — is honoured: this file specifies the schemas and gives reference fixtures marked provenance_of_purpose 'specification'. No served JSON file is written by hand."
hreflang: "en, ar"
---

# ST-34 · Licence and Register Machine Forms

> **Authority.** An **operative form** extending [ST-14](st-14-machine-surfaces-and-json-schemas.md).
> It fixes the shape of the licence-plane surfaces. **The files themselves do not exist** and may
> exist only as build output ([M-32](../00-governance-map/corpus-review-v2027.1.md), DEF-001).

> **Disclosure first.** GM-17 M-17 listed "`license.json` and siblings" as agent-writable. That was
> half wrong. An agent can write the **schema**. Writing the **file** by hand would breach ST-14's one
> rule and produce exactly the divergent surface the rule exists to prevent. The fixtures in §5 are
> test vectors for the build, not publications.

---

## 1. Surfaces

| Path | Source instrument | Purpose |
|---|---|---|
| `/license/ml-2-3/license.json` | ML-2.3 | Duties, absolutes and tier gate in a form a machine can apply **per role** |
| `/license/ml-2-3/ml-2-3.txt` | ML-2.3 | Plain UTF-8 text, with no markup dependency (ML-2.4 §E.10; HX-000 §12 D1) |
| `/license/ml-2-4/license.json` | ML-2.4 (draft) | As above. `in_force: false` until ratified |
| `/license/harms/hx-000.json` | HX-000 v2027.1 | The register as data |
| `/metax/bcia/licence/register/bx-018.json` | BX-018 | The substrate register as data |
| `/license/digests.txt` | Migration Ledger | SHA-256 of every published artefact, one per line. **Static**, so that verification works with any Worker dead (ML-2.3 site note 1) |

All carry the ST-14 envelope: `generated_at`, `source_version`, `source_instrument`, `provenance_of_purpose`, `complete`.

## 2. `license.json`: the role discriminator (closes source DEF-2026-073)

The defect: without a role field, a machine consumer cannot tell which duties apply to *it*. Each duty therefore carries **`roles`**, **`tier_floor`** and **`class`**. A consumer filters by its own role and tier.

```json
{
  "$schema": "https://metax.academy/library/sources/schemas/licence/license.schema.json",
  "envelope": {"generated_at": "…", "source_version": "…", "source_instrument": "ML-2.3",
               "provenance_of_purpose": "production|specification", "complete": true},
  "licence": {"id": "ML-2.3", "spdx": "LicenseRef-ML-2.3", "in_force": true,
              "signature": {"status": "UNSIGNED|SIGNED", "fingerprint": null, "signed_at": null},
              "register": {"id": "HX-000", "version": "2026.10.1", "identity_authority": "ML-2.3 §H.2.2"},
              "counsel_reviewed": false},
  "roles": ["author", "integrator", "operator", "commissioner"],
  "tiers": [{"tier": 0, "label": "personal"}, {"tier": 1, "label": "small"},
            {"tier": 2, "label": "substantial"}, {"tier": 3, "label": "systemic"}],
  "absolutes": [{"id": "H.3(a)(i)", "name": "…", "harm": "HX-01", "elements": "cumulative|disjunctive",
                 "element_count": 4, "class": "condition", "tier_floor": 0}],
  "conditions_outside_h3": ["C.5", "C.9", "B.5(b)"],
  "duties": [{"id": "H.4", "name": "Optimisation disclosure", "harms": ["HX-01"], "roles": ["operator"],
              "tier_floor": 1, "class": "covenant", "cure_days": 30, "anchor": "#h4-optimisation-disclosure"}],
  "defects_open": ["ML-D-007", "ML-D-008", "ML-D-009", "ML-D-010"]
}
```

**Rules.**
- `elements` must be `disjunctive` for H.3(a)(vii) and `cumulative` for every other absolute. A build that emits otherwise fails.
- **The elements' text is never in the JSON.** A machine reader follows the `anchor` to the licence text. Paraphrasing an absolute is how its boundary moves (HX-000 v2027.1 §5).
- `tier_floor` is the duty's **own header** value. Where §H.2-bis.1's Tier 1 list disagrees with a header (DEF-062: §H.21, §H.24), the emitter takes the **lower** floor and adds `"floor_conflict": "DEF-062"`.
- `signature.status` is `UNSIGNED` until a fingerprint resolves in REG-12. **No emitter may write `SIGNED` from a source's assertion** (DEF-042).

## 3. `hx-000.json`

```json
{"envelope": {"…": "…", "source_instrument": "HX-000", "complete": true},
 "register": "HX-000", "version": "2027.1", "in_force": false, "in_force_via": "ML-2.4 ratification",
 "strata": [{"id": "I", "name": "Cognitive", "harms": ["HX-01", "HX-02", "HX-03"]}],
 "harms": [{"id": "HX-01", "name": "Attention expropriation", "stratum": "I", "absolute": "H.3(a)(i)",
            "duties": ["H.4"], "status": "absolute", "verify": "2027-02", "estate_disposition": "unremedied",
            "flagged_tier34": false, "anchor": "/license/harms/hx-01/"}],
 "candidates": [{"id": "UH-03", "name": "Governance volume", "admitted": false}],
 "decay_rule": "2027-01 + (((n-1) mod 12) + 1) months"}
```

- `complete` is `true` only if every harm has its full eight-field text **inside `docs/`**. Today the text is in `sources/` (GM-17 M-49), so the build must emit **`complete: false`** until M-49 closes.
- `estate_disposition` comes from the **current issued** Part H Statement. With none issued (BHS-2027-001 is a draft), the value is `null`, not a draft value.

## 4. `bx-018.json`

As in §3, plus `substrate_class`, `interface_class`, `gate`, `refusal` (A-1…A-8 or null), and `crosswalk_hx`. Two numbering systems meet here (LEX-05 CT-13), so the top level carries **`"entry_id_pattern": "BX-\\d{2}"`** and **`"instrument_id": "BX-018"`**. No entry id may have three digits.

## 5. Reference fixtures (test vectors, `provenance_of_purpose: "specification"`)

The build must reproduce these fragments exactly from the Markdown. A mismatch means either the build or the Markdown is wrong, and the build fails until a human decides which.

```json
{"fixture": "ST-34-F1", "provenance_of_purpose": "specification",
 "expect": {"absolutes_count_ml23": 8, "absolutes_disjunctive": ["H.3(a)(vii)"],
            "hx_count_v2027_1": 28, "strata_v2027_1": 7, "bx_count": 24, "bx_refusals": 8,
            "duty_H.21_tier_floor": 0, "duty_H.24_tier_floor": 1, "duty_H.25_roles": ["integrator", "operator"],
            "ml23_signature_status": "UNSIGNED", "hx_json_complete": false,
            "verify_HX-12": "2028-01", "verify_HX-24": "2028-01", "verify_BX-12": "2028-06"}}
```

## 6. Plain-text siblings

The `.txt` form is UTF-8 with LF line endings and no markup beyond `#` headings. Every link is rendered as **its citation** (e.g. "ML-2.3 §H.31.3") followed by the URL in brackets, so the text stays meaningful when the link is dead (ML-2.4 §E.10, pending). The text's SHA-256 is listed in `/license/digests.txt`.

## 7. Falsifier

This standard fails if a consumer, given only `license.json`, its own role and its tier, would derive
a duty set different from the one a careful human reads off ML-2.3. Fixture F1 is the first test of that.

## Annex · Defects filed

DEF-062 (the Tier 1 list in §H.2-bis.1 disagrees with the headers of §H.21 and §H.24). Source DEF-2026-073 is addressed by §2, pending acceptance.

---

**Related:** [ST-14](st-14-machine-surfaces-and-json-schemas.md) · [ST-13](st-13-static-build-and-sentinel.md) · [ML-2.3](../license/ml-2-3.md) · [HX-000 v2027.1](../harms/hx-000-register-v2027-1.md) ·
[BX-018](../bcia/bx-018-register-of-substrate-harms.md) · [CF-1](../license/cf-1-compliance-file-template.md) · [REG-13](../registries/reg-13-decay-calendar.md)
