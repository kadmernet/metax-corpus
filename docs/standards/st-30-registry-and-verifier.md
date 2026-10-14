---
doc_id: "ST-30"
title_en: "Credential Registry and Verifier Specification"
title_ar: "مواصفات سجل الشهادات ومُحقِّقها"
family: "standards"
version: "v2026.10.2"
status: "canonical"
authority: "operative-form"
prevailing_text: "en"
audience_tier: 4
depth: 5
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: true
last_reviewed: "2026-09-25"
domain_tags: ["standards", "credentials", "verification", "json-ld", "revocation"]
route: "/credentials/verify/"
derived_from: "THE METAX CORPUS MX-005 §5.10, MX-002 §2.10; DS-05; Page Content Specification (issuers list)"
supersedes: ["Index allocation ST-17 'Credential Registry and Verifier Specification' (refuge number; see GM-13)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "specification"
authorship_note: "Drafted by an AI system under AG-000. Standard names (JSON-LD, W3C status lists) are cited by type; no specification version is asserted `[VERIFY]`."
hreflang: "en, ar"
---

# ST-30 · Credential Registry and Verifier

> **Authority.** `operative-form`, tier 5. Policy: [MX-025](../corpus/mx-025-credentialing-and-assessment.md).
> Record: [REG-05](../registries/reg-05-credential-registry.md). Surfaces: [DS-05](../design/ds-05-certification-surfaces.md).

> **Disclosure first.** Zero credentials; zero verifier pages; no signing key.

---

## 1. Rule of three states

**valid · expired · revoked.** An identifier never issued returns **"never issued"** — never
confused with revoked. Three artefacts (record, document, share card) **must never disagree**
([DS-05](../design/ds-05-certification-surfaces.md)).

## 2. The record — per credential

Route: `/credentials/verify/c/{id}/` (pre-rendered, static).

```json
{
  "@context": ["https://www.w3.org/ns/credentials/v2"],
  "type": ["VerifiableCredential", "MetaXCredential"],
  "id": "https://metax.academy/credentials/verify/c/{id}/",
  "issuer": "https://metax.academy/",
  "track": "Series Practitioner",
  "series": ["S20"],
  "proof_level": "P1",
  "rubric": "RB-01@v2026.10.1",
  "issued": "YYYY-MM-DD",
  "expires": null,
  "evidence_sha256": "…",
  "status": { "type": "StatusList", "index": 0, "list": "/credentials/verify/revocations/status.json" }
}
```

Context URL and status-list type name are `[VERIFY]` V-17 against the current W3C text before
build.

## 3. Revocation list

Signed at **build time** ([ST-29 E3](st-29-security-architecture.md)). A revoked entry shows date
and reason category **permanently**.

## 4. Offline bundle

If the verifier is unavailable, a **signed offline verification bundle** in Downloads suffices
(source MX-002 §2.10).

## 5. Issuers

Only MetaX and chartered academies (L3+ within their grant) issue in MetaX grammar; each listed
with key fingerprint and scope ([REG-12](../registries/reg-12-processors-keys-mirrors.md)).

## 6. Worked instance

An employer receives a PDF saying "Professional Operator". They open the record URL: status
`revoked`, 2028-03, reason category *fraud in submission*. The PDF is stale; the record governs.

## 7. Falsifier

Wrong if a record, document and share card for one credential can be shown to disagree for more
than one build cycle.

## 8. Macro register

Paper credentials are forged because checking them is costly. **A free, stranger-checkable record
with permanent revocation** makes the forgery pointless rather than merely illegal.

---

**Related:** [MX-025](../corpus/mx-025-credentialing-and-assessment.md) · [REG-05](../registries/reg-05-credential-registry.md) ·
[DS-05](../design/ds-05-certification-surfaces.md) · [ST-29](st-29-security-architecture.md) ·
[ST-14](st-14-machine-surfaces-and-json-schemas.md) · [REG-12](../registries/reg-12-processors-keys-mirrors.md) ·
[RB-02](../rubrics/rb-02-proof-ladder.md) · [MX-016](../corpus/mx-016-appeals-and-due-process.md)
