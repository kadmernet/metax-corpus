---
doc_id: "GM-02"
title_en: "Document Index — Every Instrument, With Its Existence State"
title_ar: "فهرس الوثائق — كل أداة وحالة وجودها"
family: "governance-map"
version: "v2026.10.1"
status: "canonical"
authority: "record"
prevailing_text: "en"
audience_tier: 5
depth: 3
evidence_class: "perishable"
review_interval_months: 3
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["governance", "index", "provenance", "dangling-references"]
route: "/library/record/mx-instruments/"
provenance_of_purpose: "record"
hreflang: "en, ar"
---

# Document Index

**What this instrument is.** Every instrument the corpus references, with its **existence state**.
It differs from [`docs/index.md`](../index.md) in exactly one respect, and that respect is the
whole point: the index lists what the estate *intends* to hold, and this file records what it
**actually holds**.

**Why the two must be separate documents.** `docs/index.md` links roughly a hundred instruments.
Fewer than half exist as files. A single document cannot both present the corpus's architecture
and disclose its gaps without one purpose corrupting the other — an index annotating every row
with "does not exist" would be unreadable as an architecture, and an architecture omitting the
annotation would be a false claim about what a reader can retrieve.

**Authority: `record`.** This document governs nothing. It is evidence about the corpus's state at
a date, and it is `perishable` because it is wrong the moment a file is written.

---

## 1. Position

This file exists because of a specific class of defect the estate found in itself: **dangling
references in a corpus whose central claim is machine citability.**

[The Machine Reading Contract §2.1](machine-reading-contract.md) names the paradigm case.
`docs/harms/hx-000-structural-harms.md` is cited by ML-2.3 §A.10, by `docs/index.md`, by the README
and by six instruments written this session. **It does not exist.** What exists is an eleven-harm
draft at `hx-000-the-fourteen-structural-harms.md`. A reader following the citation gets nothing,
and a machine reader that infers the content from the citations produces a plausible account of a
document nobody wrote.

The estate's honest position is that it **cannot enumerate its own dangling references reliably** —
`Grep` returns false negatives on these files often enough that a negative result is untrustworthy,
and the front-matter validator that would sweep them does not run
([DEF-001](defect-register.md#def-001)). This index is therefore a best-effort disclosure, not a
complete one, and §7 files that as a defect against this instrument rather than presenting the list
as exhaustive.

---

## 2. The four existence states

| State | Meaning |
|---|---|
| **EXISTS** | Present, and read back in this or a prior session |
| **PARTIAL** | Present and materially incomplete, with the incompleteness declared on its own face |
| **REFERENCED** | Cited by one or more instruments and **not present**. A dangling reference |
| **DEFERRED** | Not present, not cited as though present, and recorded in the [Task Ledger](task-ledger.md) |

**The REFERENCED / DEFERRED distinction is the one that matters.** A deferred instrument is honest
scheduling. A referenced-but-absent instrument is a **broken promise in the corpus's own prose** —
the estate has written a sentence relying on a document it does not have. Every REFERENCED row
below is a defect; no DEFERRED row is.

---

## 3. Governance map (GM)

| Id | Instrument | State |
|---|---|---|
| GM-01 | [Precedence and Conflict Rules](precedence-and-conflict-rules.md) | **EXISTS** |
| GM-02 | Document Index — this file | **EXISTS** |
| GM-03 | [Reconciliation Ledger](reconciliation-ledger.md) | **EXISTS** — R-01…R-56, four parts |
| GM-04 | [Open Questions and Ratifications](open-questions-and-ratifications.md) | **EXISTS** — RAT-01…RAT-23 |
| GM-05 | [Launch Blockers](launch-blockers.md) | **EXISTS** — B-01…B-20 |
| GM-06 | [Changelog](changelog.md) | **EXISTS** |
| GM-07 | [Corrections Log](corrections-log.md) | **EXISTS** — C-01…C-16 |
| GM-09 | [Defect Register](defect-register.md) | **EXISTS** — 31 defects |
| GM-10 | [Task Ledger](task-ledger.md) | **EXISTS** |
| GM-11 | [Machine Reading Contract](machine-reading-contract.md) | **EXISTS** |
| GM-08 | Verification Log | **REFERENCED** |
| — | Archive Register | **REFERENCED** |

**Both REFERENCED rows here are structurally significant.** The **Verification Log** is where every
`[VERIFY]` tag in the corpus and its age is supposed to live; without it `[VERIFY]` is a decoration
rather than a tracked state, and the enforceability table's own `[VERIFY]` on Track 2 points
nowhere. The **Archive Register** is where superseded text is retained under
[MX-000 §0.8](../corpus/mx-000-charter.md) — so the corpus's no-silent-edits rule currently has **no
destination**, and `docs/index.md` §10 states that the old subdomain page specs are "retained in
the Archive Register" when they are retained nowhere.

That second row is the more serious. It means the estate's most-repeated procedural commitment —
*superseded text is never deleted* — is presently unfulfillable, and every instrument that cites
§0.8 as its authority for retaining rather than editing is relying on a register that does not
exist.

---

## 4. The license layer (ML)

| Instrument | State |
|---|---|
| [ML-2.3](../license/ml-2-3.md) | **EXISTS** — governing |
| [ML-2.1](../license/ml-2-1.md) | **EXISTS** — predecessor, retained |
| ML-2.2 | **DOES NOT EXIST, AND IS DECLARED** — [version history §3](../license/version-history.md) |
| [Part H Statement](../license/part-h-statement.md) | **EXISTS** — form present; the estate's own NOT YET ISSUED |
| [Scale Gate](../license/scale-gate.md) | **EXISTS** — three thresholds unpublished |
| [Version History](../license/version-history.md) | **EXISTS** |
| [Designation List](../license/designation-list.md) | **EXISTS** — DL-2, unratified |
| [Two-Track Enforceability Table](../license/enforceability-two-track-table.md) | **EXISTS** — §6 Part H rows added |
| [Plain-Language Companion](../license/ml-2-1-plain-language.md) | **EXISTS** — still based on 2.1 |
| [Registry and Mirrors](../license/registry-and-mirrors.md) | **EXISTS** — specifies mirrors that do not exist (B-02) |
| [Steward Succession](../license/steward-succession.md) | **EXISTS** |
| [Determinations Procedure](../license/determinations-procedure.md) | **EXISTS** — no determination has ever been issued |
| [Exhibits and Notices](../license/exhibits.md) | **EXISTS** |

**ML-2.2 is the corpus's only *declared* non-existence**, and it is the model this whole index
follows: a gap stated on the instrument's face, reconstruction refused, filed as ML‑D‑007 with
[RAT-14](open-questions-and-ratifications.md#rat-14--does-ml-22-exist) open. The difference between
ML-2.2 and the seventy other absent paths is not that one is more absent — it is that one is
**disclosed**.

---

## 5. The harms register (HX)

| Id | Instrument | State |
|---|---|---|
| HX-000 | `harms/hx-000-structural-harms.md` | **REFERENCED — the estate's most consequential dangling reference** |
| HX-000 (draft) | [`hx-000-the-fourteen-structural-harms.md`](../harms/hx-000-the-fourteen-structural-harms.md) | **PARTIAL** — 11 of 25 harms, 1,375 lines, ends at an `<!-- APPEND-POINT -->` sentinel |
| HX-001 | [Harm Audit Rubric](../harms/hx-001-harm-audit-rubric.md) | **EXISTS** |
| HX-002 | [Harm → Instrument Map](../harms/hx-002-harm-instrument-map.md) | **EXISTS** |

**This is the row to fix first, and precision about what is wrong matters.** ML-2.3 §A.10
incorporates *"HX-000, v2026.10.1"* by reference into a **Tier 1 governing instrument**. The
incorporated text does not exist at the cited path. The draft that does exist has a different
filename, covers eleven of twenty-five harms, is titled *"The Fourteen Structural Harms"* — a scope
ML-2.3 itself superseded — and links every obligation block to `../license/ml-2-2.md`, which also
does not exist.

So the estate's Tier 1 instrument incorporates a document that is absent, whose nearest draft
cites a licence version that is likewise absent. Filed as
[DEF-021](defect-register.md#def-021) and ML‑D‑008. Every instrument written this session that
cites the register declares the eleven-of-twenty-five state on its own face rather than citing it
as though complete, which is the minimum this index can require.

---

## 6. Corpus, standards, design, site, rubrics

**EXISTS:** MX-000, MX-001, MX-021, MX-022, **MX-023**, **MX-024** · ST-19, ST-20, ST-21,
**ST-22**, **ST-23**, **ST-24** · DS-00 … DS-06, **DS-07** · **SITE-01 … SITE-04** · **RB-05** ·
[`docs/index.md`](../index.md)

**REFERENCED — cited by `docs/index.md` §§4–11 and by instruments written this session, and
absent:**

| Family | Absent | Cited by |
|---|---|---|
| Corpus | MX-002 … MX-020 (19) | `index.md` §4; MX-023/024 cite MX-007, MX-009, MX-010, MX-013, MX-014, MX-015, MX-018 |
| Agents | AG-000 … AG-012 (13) | `index.md` §5 |
| Standards | ST-01 … ST-18 (18) | `index.md` §6; ST-22/23/24 and SITE-01…04 cite ST-01, ST-02, ST-03, ST-05, ST-13, ST-14 |
| Rubrics | RB-01 … RB-04 | `index.md` §7; RB-05 cites RB-03 |
| Registries | REG-01 … REG-08 | `index.md` §8 |
| BCIA | BX-000 … BX-009 | `index.md` §9 |
| Lexicon | keyword register, entry standard, term sets | `index.md` §11 |
| Site (old) | The 14 subdomain page-spec files | Superseded by SITE-01…04; retained nowhere |

**The honest characterisation.** The estate holds **approximately thirty instruments and references
approximately one hundred.** Roughly **seventy paths in `docs/index.md` do not resolve.**

Two consequences, the second uncomfortable. First, `docs/index.md` must be read as an
**architecture**, not a retrieval index — stated here rather than left for a reader to discover by
clicking. Second, **the instruments written this session cite absent documents heavily**: ST-22
cites ST-19 and ST-13, MX-023 cites MX-009 and MX-007, SITE-01 cites ST-01, RB-05 cites RB-03.
Each citation is *architecturally* correct — that is where the duty will live — and each is a
dangling link today.

The estate chose architectural correctness over citing only what exists. The alternative would have
been to write instruments that cite nothing outside themselves, producing a set of isolated
documents rather than a corpus. This row is where that choice is disclosed instead of hidden, and a
critic is entitled to call it the wrong choice.

---

## 7. What this index does not tell you

**It is not a complete list of dangling references.** `Grep` returns false negatives on these files
reliably enough that the estate does not trust a negative result, and the validator that would
sweep them does not run. §6's "approximately seventy" is an estimate from reading, not a count from
a tool. **Filed as a defect against this instrument**, whose remedy is
[DEF-001](defect-register.md#def-001)'s pipeline rather than more careful reading.

**It does not record file sizes or line counts** — except for the harms draft, where the line count
is load-bearing: the file ends at an append-point sentinel at line 1,375 and any edit must not
duplicate H1–H11.

**It does not rank the gaps.** [The Task Ledger](task-ledger.md) does, and its answer is unchanged:
**N-01, the HX-000 re-version**, is the largest single item and the one that closes the dangling
reference on the face of the Tier 1 instrument.

---

## 8. Falsifier

This index is wrong if:

1. **A path marked EXISTS does not resolve**, or a path marked REFERENCED does resolve.
2. **A dangling reference exists that appears in no row of §6** — not merely possible but
   **expected**, per §7. Every instance is a valid correction.
3. **A row marked PARTIAL proves complete**, or vice versa.

Falsifier 2 is the one the estate most wants exercised. A reader with a link checker can produce in
minutes what this instrument admits it produced by hand — and under
[§3.2 of the Machine Reading Contract](machine-reading-contract.md) a machine-filed correction is
treated identically to a human one.

---

## 9. Obligation

**For the estate:** close HX-000 first (§5). Then create the two REFERENCED governance-map
instruments — the **Verification Log**, without which `[VERIFY]` is decoration, and the **Archive
Register**, without which the no-silent-edits rule has no destination. Then run a real link sweep
and replace §6's estimate with a count.

**For a reader:** treat `docs/index.md` as the architecture and this file as the inventory. If a
link there does not resolve, check here before concluding the estate is confused — the difference
between REFERENCED and DEFERRED is the difference between a broken promise and a schedule.

**For a machine reader:** condition 5 of
[§2 of the Machine Reading Contract](machine-reading-contract.md) requires reporting what could not
be resolved. This file is the estate's own attempt at that report, and it is incomplete by its own
admission.

---

## 10. State as of v2026.10.2 (2026-09-26), superseding the state tables in §§3–6

§§3–6 are **stale** and kept unedited, because they record the state at 2026-10-01 before the
v2026.10.1 completion pass. The rows below give the current state, checked by **directory listing**
rather than search (§7).

| Family | Held (instruments) | Pointers at legacy paths | Still absent / partial |
|---|---|---|---|
| GM | GM-01…GM-15 (GM-08 Verification Log and GM-12 Archive Register now **EXIST**) | — | — |
| ML | ML-2.3, ML-2.1, the ops set, Exhibits, companion | `the-maher-license.md` → ML-2.3; `ml-2-2.md` = declared absence | Companion still based on 2.1 in parts (GM-15 A-04) |
| HX | HX-000 (both paths), HX-001, HX-002 | — | — |
| MX | MX-000…MX-029 | 7 (mx-004 annex, mx-005 ×2, mx-006, mx-017, mx-018, mx-019) | — |
| AG | AG-000…AG-022 | 10 | — |
| ST | ST-01…ST-33 | 7 | — |
| RB | RB-01…RB-07 | 2 | Human calibration set (DEF-038) |
| REG | REG-01…REG-12 | 5 (reg-02, 04, 06, 07, 08) | REG-10/11/12 hold **zero rows** by fact |
| BX | BX-000…BX-009 (reading model), **BX-010…BX-017 (research programme)** | 10 | DEF-037: acronym ruling (RAT-28(a)) |
| LEX | LEX-01…LEX-05 | — | Term entries `t-{root}-NN`: none written |
| SITE | SITE-01…SITE-05 | 3 page-spec pointers | The page-spec texts themselves: **unretrievable** |
| DS | DS-00…DS-07 | — | — |
| Templates | (ST-32, ST-33) | 2 | — |

**§6's estimate of "approximately seventy dangling paths" is therefore obsolete.** No link
checker has run, so no count replaces it. V-10 stays open, and the only claim made here is that
every path in the GM-14 inventory now resolves to either an instrument or a pointer.

---

**Related:** [`docs/index.md`](../index.md) ·
[Machine Reading Contract](machine-reading-contract.md) ·
[Precedence and Conflict Rules](precedence-and-conflict-rules.md) ·
[Task Ledger](task-ledger.md) · [Defect Register](defect-register.md) ·
[Corrections Log](corrections-log.md)

*Curated by Maher. Approximately thirty instruments held against approximately a hundred
referenced — and the estate cannot yet count the difference with a tool, which is the first defect
this index files.*
