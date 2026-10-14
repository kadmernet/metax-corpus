---
doc_id: "GM-13"
title_en: "Identifier Reallocation Record"
title_ar: "سجل إعادة تخصيص المعرّفات"
family: "governance-map"
version: "v2026.10.2"
status: "canonical"
authority: "record"
prevailing_text: "en"
audience_tier: 4
depth: 5
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-25"
domain_tags: ["governance", "identifiers", "collisions", "immortality"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "record"
authorship_note: "Drafted by an AI system under AG-000. Records collisions caused by an earlier AI pass and resolves none of them; resolution is the Curator's."
hreflang: "en, ar"
---

# GM-13 · Identifier Reallocation Record

> **Authority.** A **record**, outside the precedence ladder
> ([GM-01](precedence-and-conflict-rules.md)). It states which subject each contested identifier
> was first given, which subject now occupies it, and where the displaced subject now lives. It
> decides nothing; the decision is [RAT-25](open-questions-and-ratifications.md#rat-25).

> **Disclosure first.** [ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md) — *numbers
> are immortal from first assignment* — is the most-cited rule in this corpus. It has now been
> broken **forty times** (§3 has 40 rows; an earlier draft of this sentence said "thirty-seven",
> corrected 2026-09-26, see GM-15 C-03), all in one release, all by the drafting agent, including the
> twenty-two already filed at [DEF-035](defect-register.md#def-035). No identifier was renamed to
> repair this. Renaming would be the same breach again.

---

## 1. Position

Two claims to one number cannot both be honoured. The index allocated the number first; the file
now at the path was published second but has been cited more. Each side has an ST-01 argument:
**first assignment** favours the index, **citation in the wild** favours the file. The estate
has no rule for this case, which is why the record exists before the ruling.

## 2. Definition

A **collision** is an identifier with two subjects across the record. A **displaced subject** is
the one that lost its number. A **refuge number** is the next-free identifier at which a displaced
subject is written so that it exists at all while the ruling is pending.

## 3. The collision table

| Id | First subject (index / source) | Occupant | Displaced subject now at |
|---|---|---|---|
| MX-004 | Terms of Top Levels — academies charter (source MX-004) | Nine-pillar scope | **MX-029** |
| MX-005 | Credentialing and Assessment | Scope and Boundaries | **MX-025** |
| MX-006 | Editorial and Evidence | Contact | **MX-026** |
| MX-017 | Trademark and Brand | Conflicts of Interest | **MX-027** |
| MX-018 | Data Retention | Third-Party Dependencies | **MX-028** |
| MX-019 | Conflicts of Interest | Sunset | **MX-017** (the occupant of MX-017 is the displaced subject of MX-019) |
| ST-08 | Cognitive Arc | Cross-Reference | **ST-25** |
| ST-09 | Unit Economics and Kill Criteria | Summaries | **ST-26** |
| ST-10 | Style Guide (English) | Terminology | **ST-27** |
| ST-15 | Component Library | Amendment | **ST-28** |
| ST-16 | Security Architecture | Audience Tier | **ST-29** |
| ST-17 | Registry and Verifier | Worked Instance | **ST-30** |
| ST-18 | academy.json Manifest | Related Blocks | **ST-31** |
| AG-001 | Sole Prompter Protocol | Roles and Scopes | **AG-013** |
| AG-002 | Roster and Role Charters | Disclosure Obligations | **AG-014** |
| AG-003 | Standing System Prompt | Output Standards | **AG-015** |
| AG-005 | Output Contract and Provenance | Tool Use Limits | **AG-016** |
| AG-006 | Evidence and Citation Protocol | Session and State | **AG-017** |
| AG-007 | Change Control | Instruction Interpretation | **AG-018** |
| AG-008 | Human-in-the-Loop Gates | Collaboration Protocol | **AG-019** |
| AG-010 | Evaluation Rubric | Error and Correction | **AG-020** |
| AG-011 | Series Generation Charter (source AG-011 v2026.08.28) | Review and Audit | **AG-021** |
| AG-012 | Degraded Mode and Prompter Succession | Sunset and Withdrawal | **AG-022** |
| RB-03 | Structural Review and Build Gates | Instrument Quality | **RB-06** |
| RB-04 | Agent Evaluation Specimen Set | Reader Comprehension | **RB-07** |
| REG-02 | Branch Registry | Page Registry | **REG-09** |
| REG-04 | Document Registry | Media Registry | **GM-02** (folded; no refuge number) |
| REG-06 | Academy Registry | Dataset Registry | **REG-10** |
| REG-07 | Determinations Registry | Defect Classification | **REG-11** |
| REG-08 | Processors, Keys and Mirrors | Role and Authority | **REG-12** |
| BX-000 | Document Zero | "BCIA Charter" (reading model) | **BX-010** |
| BX-001 | Research Charter | Before Phase | **BX-010** (combined) |
| BX-002 | Human-Cell Exclusion | Contact Phase | **BX-011** |
| BX-003 | Remediation Gates and Public Status | Internalisation | **BX-012** |
| BX-004 | Observed Taxonomy | After Phase | **BX-013** |
| BX-005 | Notation Freeze | Phase Audit Method | **BX-014** |
| BX-006 | Critical Audit | Failure Catalogue | **BX-015** |
| BX-007 | Open Problems | BCIA and Harms | **BX-015** (combined) |
| BX-008 | The Refused Inference | Machine Readers | **BX-016** |
| BX-009 | Contribution Without a Laboratory | Limits and Objections | **BX-017** |

Where a legacy path is cited (e.g. `bcia/bx-003-remediation-gates.md`), a **pointer stub** now
exists at that path naming the refuge number. The stub is non-governing and carries no
identifier of its own.

## 4. High-water marks after this session

| Family | Next free |
|---|---|
| MX | MX-030 |
| ST | ST-34 |
| AG | AG-023 |
| RB | RB-08 |
| REG | REG-13 |
| BX | BX-018 |
| LEX | LEX-06 |
| SITE | SITE-06 |
| GM | GM-16 |
| DEF | DEF-040 |
| RAT | RAT-29 *(RAT-28 was used by the omnibus entry; corrected 2026-09-26)* |
| R | R-61 *(R-57…R-60 used)* |
| V | V-18 *(V-14…V-17 used)* |

### 4a. High-water marks after the v2027.1 intake (2026-09-30), superseding §4

| Family | Next free | Notes |
|---|---|---|
| BX (instruments) | **BX-019** | BX-018 = the substrate register (source label "BX-000 v1.0") |
| GM | **GM-17** | GM-16 = source intake |
| SITE | **SITE-08** | SITE-06 nav delta, SITE-07 design and reader |
| CON | **CON-003** | CON-002 harm concordance. CON-001 is Family B's (not adopted) and is **reserved, unissued here** |
| MLT | **MLT-10** | MLT-000 register; MLT-01…09 programmes |
| DEF | **DEF-054** | plus imported DEF-2026-055…079 and DEF-2027-001 |
| RAT | **RAT-39** | plus RAT-B-01…06 |
| R | **R-68** | |
| V | **V-22** | |
| B (blockers) | **B-26** | B-21…24 are **unissued** |
| HX harms | **HX-29** | candidates UH-01…11 are not numbered |

### 4b. High-water marks after the completion pass (2026-10-08), superseding §4a

| Family | Issued this pass | Next free |
|---|---|---|
| GM | GM-17 (review), **GM-18** Anomaly Register, **GM-19** Continuity Register, **GM-20** Decision Record Register | **GM-21** |
| ST | **ST-34** licence machine forms | **ST-35** |
| REG | **REG-13** Decay Calendar, **REG-14** programme series | **REG-15** |
| SITE | **SITE-08** Decision Queue | **SITE-09** |
| LEX | **LEX-06** term entries, governance set 1 | **LEX-07** |
| MLT | MLT-01…MLT-09 charters | **MLT-10** |
| Forms (new prefixes) | **CF-1**, **CPF-1**, **PR-1**, ML-B-1.0-SCH (schedules B-1/B-2) | CF-2, CPF-2, PR-2 |
| HX strata pages | HX-000-S-I … S-VII | — |
| Retained licence text | **ML-2.0** (docs/license/ml-2-0.md) | — |
| C (corrections) | **C-17**, **C-18** | **C-19** |
| DEF | DEF-054 … DEF-067 | **DEF-068** |
| RAT | RAT-39 … RAT-44 | **RAT-45** |
| V | V-22 | **V-23** |
| B | B-26 | **B-27** |
| AN (anomalies) | AN-001 … AN-007 | AN-008 |
| CR (continuity) | CR-01 … CR-14 | CR-15 |
| DR (decisions) | DR-ML-2.3-2026-01 … DR-INTAKE-2027-01 | per instrument |

**New prefixes CF, CPF, PR, AN, CR and DR are owed rows in the ST-01 prefix table** (GM-17 M-46, A-06).

The fourth BX-000 claimant is recorded here: **BX-000 · "Register of Substrate Harms v1.0" (source) → BX-018.**

## 5. Worked instance

A reader follows [MX-000 §0.2](../corpus/mx-000-charter.md) to "BX-003 Remediation Gates". The
path `bcia/bx-003-remediation-gates.md` now resolves to a stub → BX-012, which holds the seven
gates. Without this record, the same reader following `BX-003` by identifier lands on
*The Internalisation Phase* and cannot tell the corpus is wrong. **The stub fixes the path; only
the ruling fixes the identifier.**

## 6. Failure modes

- A successor "tidies" by renumbering the occupants. Forbidden; it spends a third set.
- The refuge numbers become permanent by default because RAT-25 is never ruled. That is the
  likely outcome and it should be a decision, not a drift.

## 7. Limits

This record cannot tell which assignment a third party has cited. Neither can anyone else.

## 8. Falsifier

Wrong if any row's "first subject" was not in fact allocated before its occupant was written, or
if a collision exists that §3 omits.

## 9. Obligation

**Curator:** rule on [RAT-25](open-questions-and-ratifications.md#rat-25) — (a) ratify refuge
numbers and mark the index allocations superseded, or (b) reverse. **Agents:** allocate from §4
only; cite displaced subjects by refuge number.

---

**Related:** [Completion Programme](completion-programme.md) · [DEF-035](defect-register.md#def-035) ·
[DEF-037](defect-register.md#def-037) · [ST-01](../standards/st-01-identifier-and-url-grammar.md) ·
[Archive Register](archive-register.md) · [Routing Law](../site/routing-law.md) ·
[Task Ledger](task-ledger.md) · [Document Index](document-index.md)
