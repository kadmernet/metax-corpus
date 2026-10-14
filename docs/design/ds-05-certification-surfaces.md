---
doc_id: "DS-05"
title_en: "Certification Surfaces — Record, Document, Share Card"
title_ar: "أسطح الاعتماد — السجل والوثيقة وبطاقة المشاركة"
family: "design-system"
version: "v2026.09.2"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 3
evidence_class: "durable"
review_interval_months: 36
curator: "Maher"
license: "ML-2.1"
derived_from: ["MX-DESIGN-001 Part 8"]
last_reviewed: "2026-08-30"
domain_tags: ["design", "credentialing", "verification"]
ai_disclosure_url: "../corpus/mx-007-ai-use-and-disclosure.md"
hreflang: "en, ar"
---

# DS-05 — Certification Surfaces

**Governs:** the three artefacts of a MetaX certification and the rule that binds them.

> **A certification is three artefacts that must never disagree.**

That sentence is the whole document. Every rule below exists to make disagreement between the
three either impossible or immediately visible.

---

## §5.1 The record — authoritative

**`verify.metax.academy/c/{id}/`** · permanent · static · content plane · individually
addressable.

| Carries | Note |
|---|---|
| JSON-LD | Machine-readable, per [ST-14](../standards/st-14-machine-surfaces-and-json-schemas.md) |
| The plain-language assertion | What the credential says, in a sentence a non-specialist can evaluate |
| The proof rung | P0–P3, [RB-02](../rubrics/rb-02-proof-ladder.md). **P2 is *instrumented evidence*, not peer review** |
| The **evidence hash** | Binds the credential to a specific artefact in the vault, so evidence cannot be swapped after certification |
| Reviewer signatures | |
| Revocation status | Live |

The record is the **authoritative** artefact. Where the document or the share card disagrees with
it, the record governs and the disagreement is a defect.

---

## §5.2 The document — printable

A **printable A4/Letter PDF**, generated at issuance.

| Requirement | Note |
|---|---|
| **Bilingual** — the assertion in **both Arabic and English** | Not a translated edition; both on the same page |
| Short verification code | Human-transcribable |
| QR to the record | |
| Proof rung as a **four-segment indicator with the earned segments filled** | Shows the rung *and* the ceiling — a P1 holder's document displays the two rungs they did not earn |
| **A line stating what the credential does *not* assert** | See §5.4 |

The four-segment indicator is a small decision with a large effect. A credential rendered as a
badge implies completeness; the same credential rendered as one filled segment of four states its
own position in a ladder, and a reader who has never heard of MetaX can see it.

---

## §5.3 The share card — minimal by design

A **build-generated OG image** using the Seal gradient
([DS-01 §3.2](ds-01-foundations-and-tokens.md#32-the-ten-ramps)).

**Shows:** credential type, rung, and code. **Only.**

**Never the holder's photo.** A share card is a social-media surface, and a face on it turns a
statement about work into a statement about a person. The code is what a reader can check; the
face is what a reader would substitute for checking.

---

## §5.4 The negative assertion

Every document carries a line stating **what the credential does not assert** — and this is
critical rather than cosmetic.

A credential's danger is not what it claims but what a reader **infers**. A Series Practitioner
credential says a specific artefact was submitted and reviewed against
[D1–D5](../rubrics/rb-01-d1-d5-rubric.md) at a stated rung. It does not say the holder is
employable in a role, competent in an adjacent domain, licensed, insured, or endorsed. Absent an
explicit negative line, every one of those inferences is available to a reader who wants it, and
the credential accumulates meaning MetaX never granted.

Wording is specified per credential type in
[MX-005 Annex A](../corpus/mx-005-annex-a-credential-naming-map.md). The **Completion Marker** is
not a credential at all and its negative line says so first.

---

## §5.5 Revocation — the load-bearing rule

> **Revoked credentials do not vanish.**

| On revocation | |
|---|---|
| The record page | **Remains** at the same URL |
| Status | Flips to a **T3 defect state** ([DS-02 §1](ds-02-motion-and-attention.md#t3--persistent-signal)) — one of only four looping elements in the estate |
| The ground for revocation | **Stated** |
| The PDF's QR | Resolves to **the same honest page** |

*"A verification system that can quietly delete is not a verification system."*

This is why revocation is a named exception to the data-deletion right at
[MX-022 §22.5.4](../corpus/mx-022-identity-and-sessions.md#2254-data-rights-stated-with-the-exception),
and the exception is stated on the page rather than buried in a policy. The third party checking a
credential is the person the verifier exists to serve. If a holder could remove an adverse record
on request, every *absence* of a record would become ambiguous — and the whole verifier would
degrade to "no news is probably good news," which is not verification.

Under reduced motion the T3 loop becomes a **static high-contrast outline plus a text label**. A
reader who disables animation must still learn that the credential is revoked
([DS-02 §3](ds-02-motion-and-attention.md#3-reduced-motion)).

---

## §5.6 `mx-verify-stamp`

The verification result lands with a **180 ms scale-from-1.04 and a single subtle shadow
settle** — *"the one moment in the estate designed to feel consequential."*

It is the deliberate exception to the estate's flatness, and it is justified: verification is the
moment MetaX asserts something about a person to a third party. That should not feel like loading
a table. Under `prefers-reduced-motion` it is instant, and the result is identical.

---

## §5.7 Conformance

| Rule | Enforced by | Failure |
|---|---|---|
| Record, document and share card agree | Build-time cross-check of all three against the registry | Build failure |
| Evidence hash present and resolvable | [ST-17](../standards/st-17-registry-and-verifier.md) validation | Build failure |
| Negative-assertion line present on every document | Template gate | Build failure |
| Revoked record still reachable at its original URL | Route-permanence test | Build failure |
| Share card contains no photo | Asset audit | Build failure |
| Both locales present on every document | Bilingual gate | Build failure |

The bilingual gate is the one currently unmet: Arabic editions do not exist
([B-09](../00-governance-map/launch-blockers.md#b-09--arabic-parity-is-claimed-but-not-built--soft-blocker)),
so no document can be issued until either the Arabic assertion exists or the gate is amended in
public.

---

**Related:** [MX-005 Credentialing and Assessment](../corpus/mx-005-credentialing-and-assessment.md) ·
[RB-02 Proof Ladder](../rubrics/rb-02-proof-ladder.md) ·
[ST-17 Registry and Verifier](../standards/st-17-registry-and-verifier.md) ·
[REG-05 Credential Registry](../registries/reg-05-credential-registry.md) ·
[DS-02 Motion and Attention](ds-02-motion-and-attention.md) ·
[MX-022 Identity and Sessions](../corpus/mx-022-identity-and-sessions.md)

*Curated by Maher. Three artefacts, one truth. Where they disagree, the record governs and the
disagreement is published as a defect.*
