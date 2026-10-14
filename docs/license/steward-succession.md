---
doc_id: "ML-OPS-2"
title_en: "Steward Succession — §E.8 in Operational Form"
title_ar: "خلافة الأمين — المادة هـ.٨ في صورتها التشغيلية"
family: "license"
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
designated: false
last_reviewed: "2026-09-25"
domain_tags: ["license", "succession", "steward", "continuity"]
route: "/license/machinery/succession/"
derived_from: "ML-2.1 §E.8 (carried into ML-2.3); THE METAX CORPUS Part I §E.8; Public Canon Patch Sentences §2"
ratification: "PENDING — RAT-04"
provenance_of_purpose: "specification"
authorship_note: "Drafted by an AI system under AG-000. No successor is named; the form is written so that naming one is a fill-in, not a drafting task."
counsel_reviewed: false
hreflang: "en, ar"
---

# Steward Succession

> **Authority.** `operative-form` under [ML-2.3 §E.8](ml-2-3.md). The Curator-level parallel is
> [MX-015](../corpus/mx-015-succession-and-continuity.md); the agent-level parallel is
> [AG-022](../agents/ag-022-degraded-mode-and-succession.md).

> **Disclosure first.** **No successor Steward and no alternate is named.** §E.8(a) requires both.
> The licence is therefore currently in breach of its own succession clause, and — because
> §E.8(c) lets stewardship lapse 180 days after a trigger with no accession — the estate's charter
> layer is, today, one trigger away from lapse. Filed at
> [B-04](../00-governance-map/launch-blockers.md) and [RAT-04](../00-governance-map/open-questions-and-ratifications.md#rat-04--name-the-ethics-reviewer-and-the-successors).

---

## 1. Position

§E.8(c) is the clause that matters and it is deliberately unglamorous: on failed succession the
charter machinery (Parts D and G) lapses and **the direct grant survives**. The corpus outlives the
institution. This document exists to make the more ambitious outcome — the institution also
survives — achievable by filling in a form rather than by drafting under grief.

## 2. The succession instrument (form)

```text
MAHER'S LICENSE — STEWARD SUCCESSION INSTRUMENT
Instrument version: ____   Signed: ____ (Steward key ____)

1. Steward of record: Maher                         (natural person)
2. Successor Steward: ________________   Acceptance signed on: ____
   Public key fingerprint of successor: ________________
3. Alternate:         ________________   Acceptance signed on: ____
   Public key fingerprint of alternate: ________________
4. Triggers (ML-2.3 §E.8(b)): death · adjudicated incapacity · 365 days of
   unexplained Registry inactivity.
5. Evidence of trigger accepted: death certificate or court record; or the
   Registry's own last-signed-release timestamp for the inactivity trigger.
6. Accession: successor publishes a signed accession notice to all three
   mirrors (ML-OPS-1). Accession is effective on publication.
7. Key custody: the Steward's signing key is ______ (escrowed with ______ /
   not transferred; successor signs with own key and the accession notice
   binds the new fingerprint to the Registry).
8. Constraints accepted by successor (§E.8(d),(e)): may not weaken Foundational
   Principles, §C.9, §G.5, Part H absolutes; stewardship not transferable as a
   commercial asset.
9. Amendment: once a successor has signed item 2, this instrument may be
   amended only with the successor's countersignature or documented refusal
   (MX-000 §0.5, source text).
```

## 3. Mechanism — the timeline

| Day | Event | Who acts |
|---|---|---|
| T | Trigger occurs | — |
| T to T+180 | Successor may accede; agents enter read-only archival mode ([AG-022](../agents/ag-022-degraded-mode-and-succession.md)) | Successor; alternate if successor declines |
| T+180 | If no accession: Parts D and G lapse; Parts A, B, C, E, F, H continue; existing Determinations frozen as record | Nobody — automatic |

## 4. Worked instance — the estate as it stands

Trigger today. There is no named successor, no alternate, no key, no Registry. Day T+180 arrives
with no possible accession. Result: every published Determination (there are none) is frozen;
no one can ever again issue a compatibility ruling; the licence text continues as a direct grant
at whatever copies survive — with no signed canonical copy to distinguish from forgeries
([ML-OPS-1 §4](registry-and-mirrors.md)). **The grant survives; its meaning becomes contestable.**

## 5. Failure modes

- A successor named but never shown the key custody plan.
- The alternate is the successor's employee or relative — one failure takes both
  ([MX-017](../corpus/mx-017-conflicts-of-interest.md)).
- Inactivity clock measured from a Registry that never existed: the trigger can never fire.

## 6. Limits

No instrument can compel a named person to accept. Succession can be arranged, not guaranteed.

## 7. Falsifier

Wrong if a fully completed form in §2, lodged at three mirrors, still leaves a successor unable to
issue a signed release that a stranger can verify.

## 8. Obligation

**Curator:** name two people; obtain signed acceptances; decide item 7; lodge. That is the entire
remedy for B-04 at licence level.

## 9. Macro register

Most institutions that govern knowledge die with their founder or are captured by whoever holds
the domain afterwards. The anti-capture clause (§E.8(e)) and the lapse rule (§E.8(c)) together
state a priority: **the commons outlives the institution, and the institution may not be sold to
someone who would enclose the commons.**

---

**Related:** [ML-2.3](ml-2-3.md) · [Registry and Mirrors](registry-and-mirrors.md) ·
[MX-015](../corpus/mx-015-succession-and-continuity.md) ·
[AG-022](../agents/ag-022-degraded-mode-and-succession.md) ·
[REG-08](../registries/reg-08-role-and-authority-registry.md) ·
[REG-12](../registries/reg-12-processors-keys-mirrors.md) ·
[Launch Blockers](../00-governance-map/launch-blockers.md) · [Exhibits](exhibits.md)
