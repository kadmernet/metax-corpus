---
doc_id: "BX-015"
title_en: "BCIA Critical Audit and Open Problems"
title_ar: "التدقيق النقدي لـ BCIA والمسائل المفتوحة"
family: "bcia"
version: "v2026.10.2"
status: "draft"
authority: "record"
prevailing_text: "en"
audience_tier: 4
depth: 5
evidence_class: "volatile"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-26"
domain_tags: ["bcia", "audit", "open-problems", "verification"]
route: "/metax/bcia/status/open-problems/"
derived_from: "Source MX-014 §14.4 (seven defects); 00_BCIA_STATUS_PAGE_PATCH (gate 6 claim list)"
supersedes: ["Legacy slots bx-006-critical-audit and bx-007-open-problems (merged here; see GM-13)"]
ratification: "PENDING — RAT-25; RAT-10 (gate-6 verification sweep)"
provenance_of_purpose: "restoration"
authorship_note: "Compiled by an AI system under AG-000. No claim listed here has been verified in this pass. Every dated claim carries [VERIFY]."
hreflang: "en, ar"
---

# BX-015 · BCIA Critical Audit and Open Problems

> **Authority.** A **record**. Source MX-014 §14.4 requires courses to "link to the open problem where
> a claim exceeds the settled literature". This file is where those links point.

> **Disclosure first.** The audit has not been carried out. This file is its **worklist**. The legacy
> plan had two slots, bx-006 (audit) and bx-007 (open problems). They are merged here because an
> audit with no findings has nothing to say except what remains open. The merge is recorded in GM-13.

---

## 1. Position

Two kinds of problem are open. **Defects** are internal contradictions that remediation can close.
**Open problems** are scientific questions that only evidence can close. They are listed separately,
because closing a defect never settles an open problem.

## 2. Defect worklist (from source MX-014 §14.4)

| # | Defect | Gate | State |
|---|---|---|---|
| D-1 | Duplicated Volume I | 1 | open |
| D-2 | D1–D10 versus the seven layers | 2 | triangulated |
| D-3 | AMN/LPN, Arabic chapters versus the English glossary | 3 | unresolvable (no glossary held) |
| D-4 | Universality versus revelatory grounding | 4 | open |
| D-5 | Stewardship versus ownership | 5 | open |
| D-6 | Unverified quantitative claims | 6 | open, checkable |
| D-7 | The exclusion missing from one version of Volume I | 1a (proposed) | open |

## 3. Gate-6 claim worklist

Each claim needs a source at L-1, meaning the primary document or a scholarly reference, before any
course may state it without [VERIFY].

| C-id | Claim as it appears | Verification target | State |
|---|---|---|---|
| C-01 | 1961, Landauer | Landauer, "Irreversibility and Heat Generation in the Computing Process", *IBM J. Res. Dev.* 1961 | [VERIFY] |
| C-02 | 1937, Shannon | Shannon's MIT master's thesis on relay and switching circuits (1937, published 1938) | [VERIFY]: the year differs depending on whether the thesis or the publication is meant |
| C-03 | 1945, EDVAC | von Neumann, "First Draft of a Report on the EDVAC", 1945 | [VERIFY] |
| C-04 | 1947, Bell Labs | point-contact transistor, December 1947 | [VERIFY] |
| C-05 | 1958, Setun era | Setun ternary computer, Moscow State University (c. 1958) | [VERIFY] |
| C-06 | 2018, He Jiankui | the germline editing case announced November 2018 | [VERIFY]: cite only as a cautionary record (BX-011 §5) |
| C-07 | 2024, a Neuralink case | the first human implant, publicly reported in early 2024 | [VERIFY]: human-subject material, so history only |
| C-08 | DishBrain | Kagan et al., *Neuron* 2022 | [VERIFY]: the **DishBrain–DeepMind non-comparability** standing rule applies |

**Standing rule (from the source patch):** DishBrain and DeepMind results may not be compared as
though they measured the same thing.

## 4. Open problems (scientific)

- **OP-1:** Is there any computational task where a biological substrate beats silicon on a stated metric, under controlled comparison? (This is the question behind the refused inference, [BX-016](bx-016-refused-inference.md).)
- **OP-2:** Can a description language (the proposed AMN/LPN/BSN) be specified without human-cell work? If it cannot, BX-011 ends that line of inquiry.
- **OP-3:** Does the three-layer taxonomy predict anything, or does it only arrange the material?

## 5. Falsifier

This file is wrong if any course states a C-row claim without [VERIFY] before the row is closed.

## 6. Obligation

Agents run the gate-6 pass using [AG-017](../agents/ag-017-evidence-and-citation-protocol.md) and log
each result in the [verification log](../00-governance-map/verification-log.md).

## Macro register

An audit that is announced but not carried out gives the appearance of scrutiny without any. Listing
the work outstanding is the minimum honest position.

---

**Related:** [BX-012](bx-012-remediation-gates-and-public-status.md) · [BX-014](bx-014-notation-freeze.md) ·
[BX-016](bx-016-refused-inference.md) · [BX-011](bx-011-human-cell-exclusion.md) · [AG-017](../agents/ag-017-evidence-and-citation-protocol.md) ·
[Verification log](../00-governance-map/verification-log.md) · [MX-014](../corpus/mx-014-research-ethics-and-exclusions.md) ·
[MX-026](../corpus/mx-026-editorial-and-evidence.md)
