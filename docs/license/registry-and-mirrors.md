---
doc_id: "ML-OPS-1"
title_en: "Registry, Mirrors and Continuity — §E.7 in Operational Form"
title_ar: "السجل والمرايا والاستمرارية — المادة هـ.٧ في صورتها التشغيلية"
family: "license"
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
domain_tags: ["license", "registry", "mirrors", "continuity", "signing"]
route: "/license/machinery/registry/"
derived_from: "ML-2.1 §E.4, §E.7 (carried into ML-2.3); THE METAX CORPUS Part I §E.7"
provenance_of_purpose: "specification"
authorship_note: "Drafted by an AI system under AG-000. Specifies infrastructure that does not exist (B-02). Unreviewed by counsel."
counsel_reviewed: false
hreflang: "en, ar"
---

# Registry, Mirrors and Continuity

> **Authority.** `operative-form`. It governs nothing that [ML-2.3 §E.7](ml-2-3.md) does not
> already require; it states **how** the requirement is met. Where it differs from the licence,
> the licence governs and the difference is a defect.

> **Disclosure first.** **No Registry exists. No mirror exists. No signing key exists.** Every
> clause below describes an obligation the Steward is currently failing, and is the discharge
> specification for [B-02](../00-governance-map/launch-blockers.md). The licence text itself
> points readers at `license.metax.academy`, which does not resolve.

---

## 1. Position (meta)

A licence whose canonical text lives at one address is a licence that can be silently rewritten
by whoever controls that address, and can be lost by whoever forgets to renew it. §E.7 exists
because the estate's central claim — that its rules can be checked by strangers — is void if the
stranger cannot establish **which text** is the rule. The Registry is therefore not a website. It
is the **evidentiary basis of every other instrument**.

## 2. Definition

| Term | Meaning |
|---|---|
| **Registry** | The canonical, Steward-operated location for: licence texts, version history, Determinations, the evaluated-licenses list, succession instruments, delegation notices, and the key fingerprint |
| **Mirror** | An independent, publicly readable copy of the Registry's signed contents |
| **Content-addressed mirror** | A mirror where the address is derived from the bytes (e.g. an IPFS CID or a Git commit hash), so tampering changes the address |
| **Jurisdictionally distinct archive** | A mirror operated by a party the Steward does not control, in a different legal jurisdiction (e.g. a national library web archive or a public web archive) |
| **Signed release** | A text accompanied by a detached signature verifiable against the published fingerprint |

## 3. Mechanism (micro)

### 3.1 The minimum configuration

| Slot | Requirement | Candidate type (not a selection) | State |
|---|---|---|---|
| M1 | Steward-operated primary | Static host at the licence subdomain | **Absent** |
| M2 | Content-addressed | Public Git repository with signed tags; or IPFS pin | **Absent** |
| M3 | Jurisdictionally distinct, not Steward-controlled | Public web archive capture of every signed release | **Absent** |

The candidate column names **types**, not vendors. Choosing vendors is a Curator decision and is
recorded, when made, in [REG-12](../registries/reg-12-processors-keys-mirrors.md).

### 3.2 What each release must contain

1. The text in Markdown and plain text.
2. `SHA-256` digest of each.
3. A detached signature over the digest list.
4. The key fingerprint, repeated inside the text itself.
5. A changelog entry with reasons ([GM-06](../00-governance-map/changelog.md)).

### 3.3 Verification procedure — for any reader

1. Download the text from any mirror.
2. Compute its SHA-256.
3. Compare with the digest published at **two** other mirrors.
4. Verify the signature against the fingerprint printed in the text **and** in REG-12.
5. If any step fails, the copy is not canonical; report under
   [MX-011](../corpus/mx-011-security-and-disclosure.md).

A reader with a terminal can run this in five minutes. That property — **verifiable by a stranger
without asking the estate** — is the whole design goal.

### 3.4 The 180-day rule

If M1 is unreachable for 180 consecutive days, the most recent signed mirror is canonical and
new Determinations are suspended (§E.7(c)). The clock is started by any reader's dated, public
report; the estate does not control when the clock starts.

## 4. Worked instance

A licensee in 2031 finds two copies of ML-2.3 that differ in §F.4's cure period (30 vs 60 days) —
the attack traced in [MX-011 §8](../corpus/mx-011-security-and-disclosure.md). Under this
procedure: the 60-day copy's digest matches no mirror; the 30-day copy matches M2 and M3 and
verifies against the fingerprint. The 30-day copy governs, and the licensee needed nothing from
the estate to know it. **Today, the same licensee has no procedure at all.**

## 5. Failure modes

- **Mirrors that are not independent** — three buckets on one account are one mirror.
- **Fingerprint published only on the primary** — an attacker controlling M1 replaces both.
- **Signing without key custody planning** — a lost key is a Registry that can never issue again;
  the successor must hold, or be able to receive, signing authority
  ([ML-OPS-2](steward-succession.md)).

## 6. Limits

A signature proves who issued a text, not that the text is wise, lawful, or enforceable. Mirrors
preserve a text; they do not preserve the institution that interprets it.

## 7. Falsifier

This specification is wrong if a reader following §3.3 can be deceived by an attacker who
controls fewer than two mirrors, or if a mirror type in §3.1 proves unable to hold a signed
release unchanged for ten years.

## 8. Obligation

**Steward:** generate the key; publish the fingerprint in ML-2.3 and REG-12; stand up M1–M3;
sign ML-2.1 and ML-2.3; record all in REG-12. Closes B-02 and part of B-01.

## 9. Macro register

The web's default is that the most-linked copy wins. For a text that governs other people's
rights, that default transfers authority to whoever has the most traffic. A three-mirror signed
registry is a small, cheap refusal of that default — **authority by verifiable provenance rather
than by reach** — and it is available to any institution willing to spend an afternoon on it.

---

**Related:** [ML-2.3](ml-2-3.md) · [Steward Succession](steward-succession.md) ·
[Determinations Procedure](determinations-procedure.md) · [Exhibits](exhibits.md) ·
[REG-12](../registries/reg-12-processors-keys-mirrors.md) ·
[MX-011](../corpus/mx-011-security-and-disclosure.md) ·
[MX-024](../corpus/mx-024-infrastructure-and-migration.md) ·
[Launch Blockers](../00-governance-map/launch-blockers.md)
