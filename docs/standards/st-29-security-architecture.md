---
doc_id: "ST-29"
title_en: "Security Architecture and Dynamic Exceptions"
title_ar: "هندسة الأمن والاستثناءات الديناميكية"
family: "standards"
version: "v2026.10.2"
status: "canonical"
authority: "operative-form"
prevailing_text: "en"
audience_tier: 4
depth: 5
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-25"
domain_tags: ["standards", "security", "architecture", "exceptions", "signing"]
route: "/about/policy/security/architecture/"
derived_from: "THE METAX CORPUS MX-011 §§11.1–11.5; R-27; ST-19 §3"
supersedes: ["Index allocation ST-16 'Security Architecture and Dynamic Exceptions' (refuge number; see GM-13)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "specification"
authorship_note: "Drafted by an AI system under AG-000. No security review by any party (MX-011)."
hreflang: "en, ar"
---

# ST-29 · Security Architecture and Dynamic Exceptions

> **Authority.** `operative-form`, tier 5. Policy: [MX-011](../corpus/mx-011-security-and-disclosure.md).
> Plane boundary: [ST-19](st-19-two-plane-architecture.md). Keys: [REG-12](../registries/reg-12-processors-keys-mirrors.md).

> **Disclosure first.** **None of the exceptions below is built.** The content plane runs third-party
> ad scripts ([DEF-019](../00-governance-map/defect-register.md#def-019)), which is a larger attack
> surface than every exception here combined.

---

## 1. Position

Static hosting removes most of the attack surface: no application server, no database in the
request path, no user content rendered dynamically. Every place state enters is an **enumerated
exception**, because a place where the record could in principle be forged must be public.

## 2. The exceptions (after R-27)

| # | Exception | Plane | Scope |
|---|---|---|---|
| E1 | Presigned upload URLs for dossiers | Identity | No client secrets; short-lived; degraded email route |
| E2 | Token-gated ON REQUEST evidence | Identity | Token scoped to one reviewer × one submission; access logged |
| E3 | Revocation-list signing | Content, **build-time only** | Signed at build; no request-time signer |
| E4 | The identity island | Content, request-time | ≤4 KB, one script, no dependencies or third-party origin; additive only; failure-transparent; no reserved space ([ST-19 §3](st-19-two-plane-architecture.md)) |

E4 is the **only** request-time exception on the content plane.

## 3. Disclosure timeline (from MX-011)

Acknowledge ≤3 working days · assess ≤10 · fix or documented decision ≤90. Good-faith researchers
in scope are not pursued. Out of scope: social engineering, physical access, DoS, academy sites
without their consent. `security.txt` at the root names the address.

## 4. Signing

Released licence versions, Determinations, and the revocation list are signed; fingerprint in the
canonical text and all mirrors ([ML-OPS-1](../license/registry-and-mirrors.md)).

## 5. Incidents

Post-incident report in the Record within **30 days** of resolution, whatever the legal duty:
what happened, what data, cause, what changed.

## 6. Worked instance

A dependency CDN serving the web font is compromised ([MX-011 T3](../corpus/mx-011-security-and-disclosure.md)).
Under this standard fonts are self-hosted, so the page is unaffected. **Today they are not
confirmed self-hosted**, so the estate is exposed.

## 7. Falsifier

Wrong if the estate is built twice — island stubbed to throw, and normal — and the two content
outputs differ by any byte.

## 8. Obligation

Remove third-party scripts from the content plane; self-host fonts; publish `security.txt`.

## 9. Macro register

Enumerating one's own attack surface in public is uncommon. It invites attack; it also invites
correction. **Security by obscurity protects the institution; security by enumeration protects
the reader.**

---

**Related:** [MX-011](../corpus/mx-011-security-and-disclosure.md) · [ST-19](st-19-two-plane-architecture.md) ·
[ST-20](st-20-payment-integration.md) · [ST-22](st-22-platform-and-persistence.md) ·
[REG-12](../registries/reg-12-processors-keys-mirrors.md) · [ML-OPS-1](../license/registry-and-mirrors.md) ·
[MX-022](../corpus/mx-022-identity-and-sessions.md) · [MX-018](../corpus/mx-018-third-party-dependencies.md)
