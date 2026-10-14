---
doc_id: "GM-10"
title_en: "Task Ledger — Work in Progress and Committed Backlog"
title_ar: "سجل المهام — العمل الجاري والمتأخرات الملتزم بها"
family: "governance-map"
version: "v2026.09.4"
status: "canonical"
authority: "procedural"
prevailing_text: "en"
audience_tier: 1
depth: 2
evidence_class: "perishable"
review_interval_months: 1
curator: "Maher"
license: "ML-2.3"
last_reviewed: "2026-09-02"
domain_tags: ["governance", "process", "continuity"]
hreflang: "en"
---

# GM-10 — Task Ledger

## Why this document exists

An earlier agent working on this estate **lost its task list mid-way** when new design
documents were added, and produced a partial corpus with no record of what remained. That is a
continuity defect of exactly the kind [HX-23](../harms/hx-000-the-fourteen-structural-harms.md)
describes — work that outlives the competence of the party holding it — and the remedy is the
one §E.7 applies to the License itself: **write the state down, in the repository, where it
survives the worker.**

This ledger is therefore **operative**, not decorative. Any agent or person resuming work on
this estate reads this file first. It is updated in the same commit as the work it describes.
A task marked `DONE` here must be verifiable by opening the file it names.

> **Rule of this ledger.** No task is marked `DONE` on the strength of a tool call that
> reported success. It is marked `DONE` only when the artefact has been read back. One
> interrupted `Edit` in this project silently did not land (see §4), and the ledger is the
> reason that was caught rather than assumed.

---

## 1. Provenance of the backlog

Three instruction sets are live at once, and they are ordered, not merged.

| Set | Origin | Standing |
|---|---|---|
| **A** | The original 11-item list from the previous agent, supplied by the Curator | **Deferred** — explicitly "after next request" |
| **B** | Turn-1 new instructions: architecture source, harms research, License injection, downstream adjustments | **Active** |
| **C** | Turn-2 new instructions: ML-2.3 + as-built site design, then continue | **Active, takes precedence within B's ordering** |

The Curator's ordering instruction, still governing verbatim:

> "So, you'll start by License task, and continue with all required tasks."

---

## 2. Set A — the original 11-item list (DEFERRED, verbatim)

Preserved exactly as supplied, so that resuming it requires no reconstruction.

| # | Task | State |
|---|---|---|
| A-01 | Read and reconcile all source files | **DONE** — 19 sources in `sources/` |
| A-02 | Build docs backbone: index, precedence, reconciliation ledger, open questions, registers | **PARTIAL** — backbone present; registers need new entries (§5) |
| A-03 | Write ML-2.1 license layer (consolidated + companions) | **SUPERSEDED** by C-05 — target is now ML-2.3 |
| A-04 | Write MX-000 to MX-019 corpus instruments with adjustments integrated | **NOT STARTED** — MX-000, MX-001, MX-021, MX-022 exist |
| A-05 | Write AG-000 to AG-011 agent instruments + kernel | **NOT STARTED** |
| A-06 | Write standards (ST-01..ST-15) and rubric | **NOT STARTED** — ST-19, ST-20, ST-21 exist |
| A-07 | Write registries (series, books, branches, credentials, academies, provenance) | **NOT STARTED** |
| A-08 | Write BCIA instrument set (charter, doc zero, gates, taxonomy, notation, audit) | **NOT STARTED** — and see [R-42](reconciliation-ledger.md#r-42--the-third-pillar-is-macrolifetech-not-bcia): BCIA is *not* a pillar; it is one of nine programs under **MacroLifeTech (Meta‑X)**, routed at `/metax/bcia/` |
| A-09 | Write sitemap + route manifest + per-property page specs | **UNBLOCKED 2026‑10‑01** — supplied as MX‑NAV‑SPEC v2026.10.1; re-scoped as Phase 5 below |
| A-10 | Write lexicon standard + keyword register + term sets | **NOT STARTED** |
| A-11 | Write README and HTML documentation portal, verify rendering | **PARTIAL** — `README.md` written 2026-09-02; portal not started |

**A-03, A-08 and A-09 may not be executed as written.** Each rests on a premise the newer
sources falsify. They are re-scoped in §5 rather than deleted, because deleting a task is how a
premise change becomes invisible.

**Cross-reference errors corrected 2026‑10‑01.** A-08 previously cited "R-40" for the BCIA
re-levelling and A-09 cited "R-39" for the route-grammar finding. The correct entries are
**R-42** and **R-41** respectively. The errors are recorded rather than silently swapped,
because a ledger whose own citations are wrong cannot be used to check anything — and this file
is the one artefact in the corpus whose entire purpose is to be relied upon after the agent that
wrote it is gone.

---

## 3. Set B — turn-1 instructions

| # | Task | State |
|---|---|---|
| B-01 | Add the Platform Data Persistence Architecture to `sources/` | **DONE** |
| B-02 | Read it in full and extract obligations (Parts 0–14) | **DONE** |
| B-03 | Add the affiliate system if missing | **CONFIRMED MISSING** — must be designed from scratch (§5, task N-06) |
| B-04 | Deep research: top 14 cons of IT/networking/technology, academic + meta style, in an MD file | **PARTIAL** — see §4 |
| B-05 | Inject them into Maher's License | **DONE** as ML-2.3 Part H — but authored by the Curator, not by me (see §4 note) |
| B-06 | Adjust all previous documents and create new ones based on the new License version | **IN PROGRESS** (§5) |

---

## 4. Verified state of the harms register — read this before editing it

`docs/harms/hx-000-the-fourteen-structural-harms.md` — **89,359 bytes, 1,375 lines.**

Verified by direct read on 2026-09-02, not assumed:

- **Present and complete:** front matter, §0 Method, §1 Taxonomy + register table, §2 header,
  and harms **H1 through H11** in the full eight-part form
  (Thesis · Mechanism · Evidence · Strongest counter-argument · Reply · Ethical mapping ·
  Falsifier · Obligation this creates), each closing with an "In this estate:" paragraph.
- **Absent:** H12, H13, H14, §3 "What the register does not say", §4 "How the register is
  used", §5 "What this document refuses to claim", and "Works referenced".
- **The file ends at line 1375 with the sentinel `<!-- APPEND-POINT -->` intact.**

An `Edit` appending H12–H14 and §3–§5 was interrupted on 2026-09-01 and **did not land**. This
was confirmed by reading the file tail, not inferred. The sentinel is the append target.

### The register is now a re-version, not a completion

ML-2.3 §A.10 incorporates the Register as **"HX-000, *The Structural Harms of Computing,
Networking and Technological Order*", v2026.10.1** — not "The Fourteen Structural Harms". The
supplied License changes four things about the register that a tail-append cannot deliver:

1. **14 harms → 25 harms.** Stratum V (Reflexive, HX-15…HX-19) and Stratum VI (Successor,
   HX-20…HX-25) are new.
2. **Every harm ID is renamed** `H{n}` → `HX-{nn}`. This is the deliberate repair of the
   identifier collision between harms `H12–H14` and duties `§H.12–§H.14`, which the draft
   register had flagged as an unresolved citation hazard. **The collision rule in the draft's
   §4 is therefore obsolete and must not be carried forward.**
3. **5 absolutes → 8.** New: §H.3(a)(vi) unprincipled agency, (vii) developmental substitution,
   (viii) irreversible foreclosure. Absolute (vii) is **disjunctive**, not cumulative — the one
   deliberate exception to the §C.9.2 element model.
4. **The document is renamed**, so its path changes.

Consequently the register work is re-scoped as **N-01** in §5. The existing H1–H11 prose is
retained and re-based; it is good and the re-version does not discard it.

> *Note on authorship, recorded because §H.19 requires it.* Task B-04 asked me to research and
> write the fourteen harms; I drafted H1–H11. The ML-2.3 text supplied in turn 2 contains a
> **25-harm register authored by the Curator's other drafting agent**, which supersedes my
> taxonomy's scope. The eleven new harms in Strata V and VI are therefore **not my analysis**,
> and HX-000 v2026.10.1 must record that split honestly rather than presenting the whole
> register as one voice.

---

## 5. Set C — active work queue

Ordered. The License comes first because the Curator ordered it first, and because every other
instrument's front matter cites a License version.

### Phase 1 — the License layer

| # | Task | File | State |
|---|---|---|---|
| C-01 | Save this task ledger | `docs/00-governance-map/task-ledger.md` | **DONE** |
| C-02 | Download both turn-2 uploads to `sources/` | `sources/The_Maher_License_ML-2.3.md`, `sources/MX-SITE-DESIGN_v2026.09.3_as_built.md` | **DONE** |
| C-03 | Read both in full | — | **DONE** |
| C-04 | Verify the interrupted HX-000 edit | — | **DONE** (§4) |
| C-05 | Publish ML-2.3 as the canonical instrument | `docs/license/ml-2-3.md` | **DONE** |
| C-06 | Record the supersession and register growth in the reconciliation ledger | `reconciliation-ledger.md` R-38…R-46 | **DONE** — Part 3, nine entries |
| C-07 | Enforceability two-track table: rows for the condition/covenant split and all 8 absolutes | `docs/license/enforceability-two-track-table.md` | **PENDING** |
| C-08 | Designation list: designate HX-000 and ML-2.3 as Works of Foundational Character | `docs/license/designation-list.md` | **PENDING** |
| C-09 | Version history ML-1.0 → 1.1 → 2.0 → 2.1 → 2.2 → 2.3, with reasons | `docs/license/version-history.md` | **PENDING** |
| C-10 | Decide the ML-2.2 question (§6) | ledger entry R-38 | **OPEN — needs the Curator** |

### Phase 2 — the register re-version

| # | Task | File | State |
|---|---|---|---|
| N-01 | HX-000 v2026.10.1: rename, re-base H1–H11 → HX-01…HX-11, complete HX-12/13/14, add Strata V and VI (HX-15…HX-25), rewrite §3/§4/§5, add Works referenced | `docs/harms/hx-000-structural-harms.md` | **PENDING — largest single task** |
| N-02 | Harm audit rubric, incl. the §H.7 counterproductivity test | `docs/harms/hx-001-harm-audit-rubric.md` | **PENDING** |
| N-03 | Harm → instrument map, **including the harms MetaX itself fails** | `docs/harms/hx-002-harm-instrument-map.md` | **PENDING** |
| N-04 | MetaX's own Part H Statement (Schedule 1 form) — must mark HX-01, HX-04, HX-10 and HX-18 honestly | `docs/license/part-h-statement.md` | **PENDING — see §6** |
| N-05 | Harm review gate | `docs/rubrics/rb-05-harm-review-gate.md` | **PENDING** |

### Phase 3 — instruments the new sources require

| # | Task | File | State |
|---|---|---|---|
| N-06 | **Affiliate system** — designed from scratch; riba-compliant, disclosure-bearing, consistent with MX-009 and HX-04/HX-08 | `docs/standards/st-23-affiliate-and-referral.md` | **DONE** as D-17 — the prior question (*should it exist at all?*) is [RAT-23](open-questions-and-ratifications.md#rat-23) |
| N-07 | Platform and persistence standard | `docs/standards/st-22-platform-and-persistence.md` | **PENDING** |
| N-08 | Attention and human sovereignty | `docs/corpus/mx-023-attention-and-human-sovereignty.md` | **PENDING** |
| N-09 | Infrastructure and migration — at the **next free MX number, not MX-022** | `docs/corpus/mx-024-infrastructure-and-migration.md` | **PENDING** |
| N-10 | Design-system correction: the as-built cosmic-dark token layer | `docs/design/ds-00-as-built-token-layer.md` | **DONE** — governing; DS-01 superseded in part |
| N-11 | `prefers-reduced-motion` block — accessibility defect, treat as launch-blocking | DEF + B entry, then `css/style.css` | **PENDING** |
| N-12 | Scale Gate worksheet (Schedule 2) | `docs/license/scale-gate.md` | **PENDING** |

### Phase 4 — register maintenance

| # | Task | File | State |
|---|---|---|---|
| N-13 | `docs/index.md`: add `harms/` family, ML-2.3, new MX/ST/RB/HX entries, new release posture | `docs/index.md` | **DONE** — §3a added, release v2026.09.4 |
| N-14 | Defect register: DEF-016+, incl. **DEF-2026-041 downgraded** and the JS-only-crawlability defect | `defect-register.md` | **DONE** — DEF-016…DEF-022 + retirement |
| N-15 | Launch blockers: B-16+, incl. reduced-motion and cookie-gated-hydration adversarial test | `launch-blockers.md` | **DONE** — B-16…B-19, wave 1 gated |
| N-16 | Open questions: RAT-14+, incl. **RAT-16 the *ḥifẓ al-ʿaql* extension needs scholarly review** (cited by ML-2.3 §0.4) | `open-questions-and-ratifications.md` | **DONE** — RAT-14…RAT-18 |
| N-17 | Changelog: new release entry, reasons not diffs | `changelog.md` | **DONE** — v2026.09.4 |
| N-18 | Corrections log: one entry per CORRECTED disposition | `docs/00-governance-map/corrections-log.md` | **DONE** — C-01…C-12 + method section |
| N-19 | `README.md` | `README.md` | **DONE** |

### Phase 5 — the navigation and route layer (Set D, turn 4)

Arising from [MX‑NAV‑SPEC v2026.10.1](../../sources/MX-NAV-SPEC_v2026.10.1.md). This phase
discharges the long-blocked A-09.

| # | Task | File | State |
|---|---|---|---|
| D-01 | Download the nav spec to `sources/` | `sources/MX-NAV-SPEC_v2026.10.1.md` | **DONE** |
| D-02 | Read it in full (all ten sections) | — | **DONE** |
| D-03 | Apply `MacroLifeTach` → `MacroLifeTech` as a logged correction, not a silent edit | R-42, C-05, DS-00 §2, this file | **DONE** — [C-13](corrections-log.md#c-13), [DEF-023](defect-register.md#def-023) |
| D-04 | Fix this ledger's own cross-references (R-40→R-42, R-39→R-41) | this file §2 | **DONE** |
| D-05 | Reconcile the spec: ledger Part 4 | `reconciliation-ledger.md` R-47…R-56 | **DONE** — ten entries |
| D-06 | New defects arising | `defect-register.md` DEF-023…DEF-028 + DEF‑2026‑042/043 | **DONE** |
| D-07 | New blocker: the demo provenance strip | `launch-blockers.md` B-20 | **DONE** |
| D-08 | New open questions | `open-questions-and-ratifications.md` RAT-19…RAT-22 | **DONE** |
| D-09 | **The route manifest** — canonical, 321 EN routes, the discharge of A-09 | `docs/site/route-manifest.md` | **DONE** — SITE-01 |
| D-10 | The page contract: skeleton, `.mx-related`, `.mx-exitpair`, `.mx-pagestamp`, `.mx-demo`, acceptance checklist | `docs/site/page-contract.md` | **DONE** — SITE-02, 20 acceptance lines |
| D-11 | The prose standard: eight-part recipe, three registers, word floors, §7.4 exemptions | `docs/standards/st-24-page-prose-standard.md` | **DONE** — ST-24 |
| D-12 | Routing law and redirects: directory routes, root-absolute paths, `_redirects` table | `docs/site/routing-law.md` | **DONE** — SITE-03 |
| D-13 | Nav geometry and the `MENU` contract, incl. the 1180px breakpoint | `docs/design/ds-07-navigation-geometry.md` | **DONE** — DS-07 |
| D-14 | Demo notice instrument — what is real and what is scaffolding | `docs/site/demo-notice.md` | **DONE** — SITE-04, audience tier 1 |
| D-15 | Changelog entry for release v2026.10.1 | `changelog.md` | **DONE** |
| D-16 | `docs/index.md`: add the `site/` family, ST-24, DS-07, the new registers | `docs/index.md` | **DONE** — §10 rewritten |
| D-17 | **The affiliate system** — promoted from N-06; the nav spec routes it at `/about/access/` | `docs/standards/st-23-affiliate-and-referral.md` | **DONE** — no upstream source; RAT-23 filed |
| D-18 | README refresh | `README.md` | **DONE** |
| D-19 | Part H Statement (Schedule 1 form) + the estate's own statement | `docs/license/part-h-statement.md` | **DONE** |
| D-20 | Scale Gate worksheet (Schedule 2) | `docs/license/scale-gate.md` | **DONE** |
| D-21 | Licence version history ML-1.0 → 2.3 | `docs/license/version-history.md` | **DONE** |
| D-22 | Harm audit rubric | `docs/harms/hx-001-harm-audit-rubric.md` | **DONE** |
| D-23 | Harm → instrument map, incl. the harms MetaX fails | `docs/harms/hx-002-harm-instrument-map.md` | **DONE** |
| D-24 | Harm review gate | `docs/rubrics/rb-05-harm-review-gate.md` | **DONE** |
| D-25 | Attention and human sovereignty | `docs/corpus/mx-023-attention-and-human-sovereignty.md` | **DONE** |
| D-26 | Infrastructure, capacity and migration | `docs/corpus/mx-024-infrastructure-and-migration.md` | **DONE** |
| D-27 | Platform and persistence standard | `docs/standards/st-22-platform-and-persistence.md` | **DONE** |
| D-28 | Index + changelog reconciliation for D-19…D-27 | `docs/index.md`, `changelog.md` | **DONE** |
| D-29 | Designation List re-based to ML-2.3 as **DL-2** — HX-000, ML-2.3/Part H, HX-001, Schedule 1 form; two close calls excluded with reasons | `docs/license/designation-list.md` | **DONE** |
| D-30 | Enforceability table **§6**: 23 Part H rows + the §F.4 condition/covenant split | `docs/license/enforceability-two-track-table.md` | **DONE** |
| D-31 | Machine Reading Contract — closed a dangling reference in a corpus whose thesis is machine citability | `machine-reading-contract.md` | **DONE** |
| D-32 | **Document Index** with existence states — the estate's first honest count of its own dangling references | `document-index.md` | **DONE** |
| D-33 | Verification Log — 13 `[VERIFY]` claims with ages, none closed | `verification-log.md` | **DONE** |
| D-34 | Archive Register — closed the §0.8 rule's missing destination; DEF-029 filed against it | `archive-register.md` | **DONE** |
| D-35 | DEF-029, DEF-030 filed; index rows for the four new governance-map instruments | `defect-register.md`, `docs/index.md` | **DONE** |
| D-36 | Precedence ladder re-based to ML-2.3: **tier 1a** (the Register), **records outside the ladder**, the SITE rows, four new outside-precedence entries | `precedence-and-conflict-rules.md` | **DONE** |
| D-37 | ST-01 Identifier and URL Grammar — nineteen prefixes, four rules, the immortality doctrine | `standards/st-01-…md` | **DONE** |
| D-38 | ST-02 Front-Matter Schema — 18 required + 11 conditional fields | `standards/st-02-…md` | **DONE** |
| D-39 | ST-04 Falsifiability and Claim Cards — four counterfeits, the `IF FALSE` field | `standards/st-04-…md` | **DONE** |
| D-40 | ST-05 Decay Classes — three classes + the provenance-of-purpose amendment | `standards/st-05-…md` | **DONE** |
| D-41 | ST-07 Evidence and VERIFY — E0–E4, the four tag boundaries | `standards/st-07-…md` | **DONE** |
| D-42 | ST-13 Static Build and SENTINEL — five check families, all unrun | `standards/st-13-…md` | **DONE** |
| D-43 | MX-009 Advertising — six cumulative conditions, three currently failed | `corpus/mx-009-…md` | **DONE** |
| D-44 | MX-010 Accessibility — AA + five extras, three known failures | `corpus/mx-010-…md` | **DONE** |
| D-45 | MX-007 AI Use and Disclosure — discloses its own authorship | `corpus/mx-007-…md` | **DONE** |
| D-46 | MX-013 Records and Versioning — six registers, four permanence rules | `corpus/mx-013-…md` | **DONE** |
| D-47 | RB-01 the D1–D5 rubric; RB-02 the proof ladder | `rubrics/rb-01-…md`, `rb-02-…md` | **DONE** |
| D-48 | Index rows for D-37…D-47 | `docs/index.md` | **DONE** |
| D-49 | MX-016 Appeals and Due Process — five guarantees, three stages, the §4 conflict stated | `corpus/mx-016-…md` | **DONE** |
| D-50 | ST-06 Objections Standard — four properties, four counterfeits, four dispositions | `standards/st-06-…md` | **DONE** |
| D-51 | ST-03 Limits and Bridge — four limit classes, the outward-pointing Bridge | `standards/st-03-…md` | **DONE** |
| D-52 | MX-015 Succession — four roles, three triggers, the "dies tonight" walk-through | `corpus/mx-015-…md` | **DONE** |
| D-53 | MX-012 Licensing and Reuse — the summary that governs nothing | `corpus/mx-012-…md` | **DONE** |
| D-54 | MX-008 Moderation and Enforcement — nine red lines, the publication duty | `corpus/mx-008-…md` | **DONE** |
| D-55 | MX-014 Research Ethics — three refusals, five hard exclusions, pre-registration | `corpus/mx-014-…md` | **DONE** |
| D-56 | Index rows for D-49…D-55 | `docs/index.md` | **DONE** |

**ST-19 was found already present** and was **not** overwritten. The write attempt returned a
file-exists error, which is the intended behaviour and is recorded here because it is the third
verification event of this session: a blind overwrite would have destroyed an existing instrument.

**The pattern of this batch, stated as a finding.** Seven instruments, and **four of them had to
open by disclosing a structural gap in the estate rather than a rule**: MX-016's appeals process has
an unstaffable middle stage, MX-015's succession has three unfilled roles, MX-014's exclusions have
no ethics reviewer, ST-06's own strongest objection is filed `open` and unanswered.

These are not defects of the kind the register already holds. **They are the same gap seen four
times: the estate has one participant.** Appeals need a second reviewer, succession needs a
custodian, research ethics needs an independent veto, and objections need someone who is not the
author. Every one of those is blocked on
[RAT-04](open-questions-and-ratifications.md#rat-04--name-the-ethics-reviewer-and-the-successors)
and [B-01](launch-blockers.md) — naming people and signing the licence — and neither is difficult.

That is now the estate's **largest single structural finding** and it outranks the ad slots in
consequence, because the ad slots are one decision and this is four instruments that cannot
operate.

**Dangling references closed this pass.** D-37…D-47 were selected by one criterion: **which absent
instruments were most heavily cited by instruments that already exist.** ST-01, ST-02, ST-05 and
ST-13 were cited by nearly every document written this session; MX-009 by MX-023 and HX-002; RB-01
and RB-02 by MX-005 and the credentials routes. The
[Document Index §6](document-index.md) estimate of ~70 unresolving paths falls by roughly a dozen.

**What writing them surfaced.** Three instruments had to open by disclosing that the estate
violates them — MX-009 (three of six advertising conditions), MX-010 (three accessibility
failures), ST-13 (SENTINEL does not run at all). That is now the established pattern of this
corpus and is worth stating as a finding rather than a coincidence: **when the estate writes down
what it requires of itself, it discovers it is not doing it.** The instruments are not becoming
more flattering as they accumulate.

**What D-31…D-34 revealed, recorded because it was not the intended output.** Writing the four
governance-map instruments the corpus had been *citing* exposed a pattern the estate had not
named: **three of its most-repeated procedural commitments had no destination.** `[VERIFY]` was
cited as a tracked state with no log. §0.8's "retained permanently" was cited as authority with no
archive. The machine-reading contract was named as the entry point for AI systems and did not
exist. Each was quoted correctly in a dozen instruments while having nowhere to put anything.

This is [HX-002 §8](../harms/hx-002-harm-instrument-map.md)'s finding arriving a third time:
**the estate's recurring failure is not bad rules; it is rules without mechanisms.** Two of the
four instruments therefore file defects against themselves on creation — DEF-029 (the archive rule
predates the archive; two superseded texts are already unretrievable) and DEF-030 (thirteen
verifications open, four of them minutes of work, all deferred at the moment they were cheapest).

**Phase 2 and Phase 3 are hereby discharged.** N-02 (HX-001), N-03 (HX-002), N-04 (Part H
Statement), N-05 (RB-05), N-06 (ST-23), N-07 (ST-22), N-08 (MX-023), N-09 (MX-024) and N-12
(Scale Gate) were all completed in this session under Set D identifiers. **N-01 \u2014 the HX-000
re-version \u2014 is the sole survivor of Phase 2 and is now the largest single item in the entire
queue.** Every instrument written this session that cites the register cites eleven of
twenty-five harms and says so on its face.

### Phase 6 — then Set A resumes

Then §2, re-scoped by **R-41** (route grammar), **R-42** (BCIA re-levelled) and **R-48…R-56**,
then the HTML portal.

---

## 5b. Phase 7 — the completion pass (D-57…D-96)

> **This section discharges [DEF-034](defect-register.md#def-034), severity S1.** The rows below
> were absent for the whole of the release in which their instruments were written.
> [AG-008 §5.1](../agents/ag-008-agent-collaboration-protocol.md) established what that absence
> meant: a successor agent reading this ledger would have concluded ~40 written instruments were
> still owed, begun drafting them, and hit an overwrite path with **zero** archive compliance
> ([AG-005 §5.1](../agents/ag-005-agent-tool-use-limits.md)). **The realistic loss was forty
> instruments.** A stale register is not an incomplete record; it is a false instruction.

**Registries — the family was entirely absent and is now complete.**

| Id | Task | File | State |
|---|---|---|---|
| D-57 | REG-01 Series Registry — four series, one burnt by citation | `registries/reg-01-…md` | **DONE** |
| D-58 | REG-02 Page Registry — the census; 321 routes vs ~77 pages | `registries/reg-02-…md` | **DONE** |
| D-59 | REG-03 Book Registry — no completed book; the announcement clock | `registries/reg-03-…md` | **DONE** |
| D-60 | REG-04 Media Registry — four images `unexamined`; six properties | `registries/reg-04-…md` | **DONE** |
| D-61 | REG-05 Credential Registry — **published empty**; issue is blocked | `registries/reg-05-…md` | **DONE** |
| D-62 | REG-06 Dataset Registry — two held, four refused | `registries/reg-06-…md` | **DONE** |
| D-63 | REG-07 Defect Classification — DC-1…DC-7, S1…S4 | `registries/reg-07-…md` | **DONE** |
| D-64 | REG-08 Role and Authority — **one of seven roles filled** | `registries/reg-08-…md` | **DONE** |

**Corpus — the family is now complete, MX-000…MX-024.**

| Id | Task | File | State |
|---|---|---|---|
| D-65 | MX-002 Terms of Service — six promises, each falsifiable | `corpus/mx-002-…md` | **DONE** |
| D-66 | MX-003 Privacy Notice — §7, the unaudited hosting layer | `corpus/mx-003-…md` | **DONE** |
| D-67 | MX-004 Terms of the Top Levels — nine pillars, tie-break, Annex A census | `corpus/mx-004-…md` | **DONE** |
| D-68 | MX-005 Scope and Boundaries — Annex A, 20 out-of-scope rows | `corpus/mx-005-…md` | **DONE** |
| D-69 | MX-006 Contact and Correspondence — the unservable-notice hole | `corpus/mx-006-…md` | **DONE** |
| D-70 | MX-011 Security and Disclosure — eight threats, seven controls absent | `corpus/mx-011-…md` | **DONE** |
| D-71 | MX-017 Conflicts of Interest — nine unrecusable classes, four substitutes | `corpus/mx-017-…md` | **DONE** |
| D-72 | MX-018 Third-Party Dependencies — eight rows; **D5 exit `impossible`** | `corpus/mx-018-…md` | **DONE** |
| D-73 | MX-019 Sunset and Wind-Down — eight promises die, five survive | `corpus/mx-019-…md` | **DONE** |

**Standards — ST-01…ST-24 now complete.**

| Id | Task | File | State |
|---|---|---|---|
| D-74 | ST-08 Cross-Reference and Link Integrity — six checks, **L6 found by writing** | `standards/st-08-…md` | **DONE** |
| D-75 | ST-09 Summary and Abstract — S1–S5; absolutes never paraphrased | `standards/st-09-…md` | **DONE** |
| D-76 | ST-10 Terminology — T1…T7; **four T1 breaches named** | `standards/st-10-…md` | **DONE** |
| D-77 | ST-15 Amendment and Versioning — A1…A7; **A1 clarified mid-draft** | `standards/st-15-…md` | **DONE** |
| D-78 | ST-16 Audience Tier — U1…U7; **three of four tier 1 claims fail** | `standards/st-16-…md` | **DONE** |
| D-79 | ST-17 Worked Instance — W1…W6; four discoveries recorded | `standards/st-17-…md` | **DONE** |
| D-80 | ST-18 Related Blocks and Exit Pairs — R1…R8; **R3 clarified mid-draft** | `standards/st-18-…md` | **DONE** |

**Rubrics, lexicon.**

| Id | Task | File | State |
|---|---|---|---|
| D-81 | RB-03 Instrument Quality — six dimensions; **four of eight sampled fail** | `rubrics/rb-03-…md` | **DONE** |
| D-82 | RB-04 Reader Comprehension — C1…C5, run by the reader, never returned | `rubrics/rb-04-…md` | **DONE** |
| D-83 | LEX-02 Lexicon Entry Standard — nine fields; **X2 split rule found by writing** | `lexicon/lexicon-entry-standard.md` | **DONE** |
| D-84 | LEX-03 Term Set: Governance — twelve terms; **the authority-note tax, sized** | `lexicon/term-set-governance.md` | **DONE** |

**Agents — AG-000…AG-012 now complete.**

| Id | Task | File | State |
|---|---|---|---|
| D-85 | AG-001 Roles and Scopes — six roles; **three over-reaches found** | `agents/ag-001-…md` | **DONE** |
| D-86 | AG-002 Disclosure Obligations — D1's three limbs; **five capability gaps** | `agents/ag-002-…md` | **DONE** |
| D-87 | AG-003 Output Standards — O1…O8; **three breaches in the same session** | `agents/ag-003-…md` | **DONE** |
| D-88 | AG-005 Tool Use Limits — protected list; **six unarchived overwrites** | `agents/ag-005-…md` | **DONE** |
| D-89 | AG-006 Session and State — the eight interruptions; **three unresolved** | `agents/ag-006-…md` | **DONE** |
| D-90 | AG-007 Instruction Interpretation — **K1–K4 recorded, late** | `agents/ag-007-…md` | **DONE** |
| D-91 | AG-008 Collaboration Protocol — H1…H6; **found DEF-034** | `agents/ag-008-…md` | **DONE** |
| D-92 | AG-010 Error and Correction — AE-1…AE-6; nine errors consolidated | `agents/ag-010-…md` | **DONE** |
| D-93 | AG-011 Review and Audit — L-1…L-4; **review debt 100%** | `agents/ag-011-…md` | **DONE** |
| D-94 | AG-012 Sunset and Withdrawal — six standing conditions, **three breached** | `agents/ag-012-…md` | **DONE** |

**BCIA — the estate's largest empty division, now written.**

| Id | Task | File | State |
|---|---|---|---|
| D-95 | BX-000…BX-009 — charter, four phases, audit method, failure catalogue, harms map, machine readers, objections | `bcia/bx-000-…md` … `bx-009-…md` | **DONE** |

**N-01 — discharged.**

| Id | Task | File | State |
|---|---|---|---|
| D-96 | **N-01 — HX-000 v2026.10.1, twenty-five harms in six strata.** New path; predecessor retained and marked superseded on its face; redirect appended at [SITE-03 §6.1](../site/routing-law.md) | `harms/hx-000-structural-harms.md` | **DONE** |

### What Phase 7 found

**N-01 is closed and the queue's largest item is gone.** It had survived every prior phase.

**The re-version's finding was not the twenty-five harms.** It was the tally:
**twelve of twenty-five are instantiated by this estate, and ten of the twelve sit in the two
strata that did not previously exist** — V Reflexive (H15–H19, **all five FAIL**) and VI Successor
(H20–H25, five of six FAIL). Recorded at [DEF-033](defect-register.md#def-033).

The predecessor could not have found them. A register of fourteen harms about computing and
networking had no category in which *"we disclose faster than we remedy"* (H15), *"our honesty
makes our unchecked claims more persuasive"* (H16), or *"we are prolific and unchecked"* (H19)
could even be **stated**. **The count did not rise because eleven more harms were found in the
world. It rose because the register was turned on its author, and eleven of the additions
landed.**

**The session's method finding, which generalises past this estate.**
[AG-010 §5.1](../agents/ag-010-agent-error-and-correction.md) classified nine agent errors and
found the distribution stable: **every prohibition held; every affirmative duty failed.** No
protected artefact was touched, nothing was deleted, nothing deployed, no continuity claimed — and
archive-before-overwrite was missed **six times out of six**. The same rule redrafted as a
prohibition would sit in the category that held perfectly.

**Seven free remedies remain unadopted.** [BX-006 §5](../bcia/bx-006-phase-failure-catalogue.md)
lists them; none requires an amendment, a ratification, a vacant role, or reader data.
[BX-006 §5.1](../bcia/bx-006-phase-failure-catalogue.md) explains why they stayed invisible —
checklist completeness, a phase-blind quality rubric, and incapacity absorbing capability — and
under **H15** publishing that list is not itself a remedy.

**The cheapest outstanding check in the entire corpus** is an **L-1 source pass**
([AG-011 §3.1](../agents/ag-011-agent-review-and-audit.md)): ten claims, not chosen by the agent,
opened against their cited instruments. Twenty minutes. It needs no role, no authority and **no
second participant** — and it is the only available detection for **AE-1 fabrication**, the one
error class the agent cannot see in its own output. It has never been run once.

---

## 6. Decisions that need the Curator

These are blocking or near-blocking and I will not resolve them silently.

| Id | Question | Why it matters |
|---|---|---|
| **Q-01** | **Does ML-2.2 exist?** ML-2.3 declares `supersedes: "ML-2.2"`, §E.3 grants ML-2.2 grants validity until 2027-03-31, and the changelog documents 2.2 → 2.3 defect repairs. But **no ML-2.2 text was ever supplied or published** — the estate holds ML-2.1. Either 2.2 must be published for 2.3's transition provisions to refer to anything, or 2.3's references to it must be re-based onto 2.1. | §E.3 and the changelog are currently unresolvable references |
| **Q-02** | Will you publish MetaX's own Part H Statement marking **HX-01, HX-04, HX-10 and HX-18 unremedied**? §H.16.3 makes an all-clear Statement presumptively non-compliant, and ads are live on the content plane. | Refusing makes MetaX its own first specimen of HX-15 |
| **Q-03** | **Pre-render or not.** Detail pages are `detail.html?type=series&id=N`, invisible to non-JS crawlers. The estate's thesis is being cited by machines. | Every new series raises the unwind cost |
| **Q-04** | The "must render with JavaScript disabled" law is **violated by the live site today** (no header, footer, nav, or pillars without JS). Change the law or the build? | Recommendation on file: change the build |
| **Q-05** | RAT-16: the *Ḥifẓ al-ʿAql* extension from intoxicants to attention-engineering is a reasoned lay analogy, not a ruling. Who reviews it? | ML-2.3 §0.4 publishes it as contested |

---

## 7. Numbering high-water marks

Numbers are immortal from first assignment (ST-01 Rule 2). Next free:

| Series | Highest used | Next free |
|---|---|---|
| Defects | DEF-030 (+ DEF-2026-041/042/043) | **DEF-031** |
| Verifications | V-13 | **V-14** |
| Archive entries | A-07 · B-07 · C-04 · **D empty** | A-08 · B-08 · C-05 · **D-01** |
| Launch blockers | B-20 | **B-21** |
| Reconciliation | R-56 (this release) | **R-57** |
| Ratifications | RAT-23 | **RAT-24** |
| Site layer | SITE-04 | **SITE-05** |
| Corpus | MX-022 | **MX-023** |
| Standards | ST-23 and ST-24 both **written** | **ST-25** |
| Rubrics | RB-04 | **RB-05** |
| Harms register | HX-000 | **HX-001** |
| Governance map | GM-12 archive register; GM-02, GM-08 and GM-11 also **written** this session | **GM-13** |
| Design system | DS-07 **written** | **DS-08** (DS-00 sits beneath the family) |
| Corrections | C-16 | **C-17** |
| License defects | ML-D-010 | **ML-D-011** |
| Site layer (new family) | — | **`docs/site/`**, unnumbered by path, indexed in `docs/index.md` |

---

---

## 8. State at the close of this session

**Completed this session (each verified by reading the artefact back):**

| Artefact | What it is |
|---|---|
| `docs/00-governance-map/task-ledger.md` | This file — the durable task state |
| `docs/license/ml-2-3.md` | ML-2.3 published with Part H, plus a Publication Note declaring its three defects |
| `docs/00-governance-map/reconciliation-ledger.md` | Part 3 added: R-38…R-46 |
| `docs/00-governance-map/open-questions-and-ratifications.md` | RAT-14…RAT-18 added |
| `docs/00-governance-map/defect-register.md` | DEF-016…DEF-022 added; DEF-2026-041 retired-but-retained |
| `docs/00-governance-map/launch-blockers.md` | B-16…B-19 added; wave 1 preconditions updated |
| `docs/00-governance-map/corrections-log.md` | Created: C-01…C-12 and the method finding |
| `docs/00-governance-map/changelog.md` | Release v2026.09.4, with reasons |
| `docs/design/ds-00-as-built-token-layer.md` | Created: the governing token layer |
| `docs/index.md` | Release posture, §3a harms family, DS-00, MX-023/024, ST-22/23, RB-05 |
| `README.md` | Created |

**The single most important finding of this session**, recorded here because it should change how
the remaining work is done:

> Thirty-seven entries of careful cross-source reconciliation found **one** case where the estate
> was wrong about itself. Fetching the live site and reading `css/style.css` found **nine** in an
> afternoon. The corpus was internally consistent and externally wrong, and it drifted in one
> direction — toward describing a more principled system than the one running.

**Immediate next action.** Task **N-01**: re-version HX-000 to v2026.10.1. It is the largest
remaining item, `ML-2.3 §A.10` incorporates it by reference, and until it exists the estate's
Tier 1 instrument has a dangling reference (DEF-021). Its shape is fixed: re-base H1–H11 to
`HX-{nn}`, complete HX-12/13/14, add Strata V and VI, rewrite §3–§5, add the bibliography, and
carry an authorship note per R-39.

---

## 9. State at the close of the turn-4 session (2026‑10‑01)

**Instruction received:** check three joined files (License, design, sitemap); *"create latest
documents details, not new documents with versions"*; generate as many documents as possible in
full academic, meta and macro style **without asking permission**.

**Reading of the second clause, recorded because it governs every file touched this session.**
It is an instruction against version proliferation, not against versioning. The estate does not
create `ml-2-3-v2.md` or `ds-00-rev2.md`; it refreshes the **current canonical instrument at its
permanent path** and records the change in the registers. Two of the three joined files were
re-uploads of sources already held — ML-2.3 and MX‑SITE‑DESIGN v2026.09.3 — and were therefore
**not** re-downloaded under new filenames. Only MX‑NAV‑SPEC v2026.10.1 was new.

**Completed and verified this session:**

| Artefact | Change |
|---|---|
| `sources/MX-NAV-SPEC_v2026.10.1.md` | Downloaded, 50,773 bytes, read in full |
| `reconciliation-ledger.md` | Part 4 added: R-47…R-56; summary counts and character paragraph amended; R-42 spelling and anchor repaired |
| `corrections-log.md` | C-13…C-16 added; §Method amended with the three-method taxonomy; C-05 spelling repaired |
| `defect-register.md` | DEF-023…DEF-028 added; DEF‑2026‑042 closed structurally; DEF‑2026‑041 re-characterised; DEF‑2026‑043 declared |
| `launch-blockers.md` | B-20 added; wave-1 preconditions amended |
| `open-questions-and-ratifications.md` | RAT-19…RAT-22 added; cadence amended |
| `docs/design/ds-00-as-built-token-layer.md` | §2 spelling repaired |
| `task-ledger.md` | This §9; Phase 5 (Set D); §2 cross-references corrected; high-water marks updated |

**The finding of this session, which extends the one in §8 without contradicting it.** §8 recorded
that reading the live code found nine errors cross-source reconciliation could not. This session
records the limit of *that* method:

> Reading the artefact tells you what is there. It cannot tell you what the artefact is **for**,
> or what its subject is **called**. Two of this session's corrections — a proper name (C-13) and
> the difference between a demo and a production system (C-14) — were unreachable by documents
> and by code alike. They required the Curator. The estate now recognises three error-finding
> methods with three distinct blind spots, and records that **only two of the three can be
> automated**.

The practical consequence is a new required field: every claim about a live artefact must record
its **provenance of purpose** — `demo`, `staging` or `production` — alongside its date. Nine
claims published in v2026.09.4 lacked it. None was false; all nine were unlabelled, which is the
subtler defect and the one no consistency check will ever raise.

**Immediate next actions, in order:** D-09 (route manifest), D-10 (page contract), D-11 (prose
standard), D-12 (routing law), then N-01 (HX-000 re-version) which remains the largest single
item in the queue.

**Before touching `docs/harms/hx-000-*.md`, re-read §4 of this ledger.** The file is 1,375 lines
and ends at an `<!-- APPEND-POINT -->` sentinel; H1–H11 are present and must not be duplicated.

---

## 10. Phase 8: the v2026.10.2 restoration pass (2026-09-26)

**Instruction received:** check all joined files; list every missing document together with an
agent prompt for completing the corpus; execute that prompt; then review the whole corpus for
conflicts and record the review in an MD file.

**Correction to §7.** The high-water table in §7 is stale by two releases, which is the DEF-034
pattern again. It is not rewritten. **The current table is [GM-13 §4](identifier-reallocation-record.md).**
After this phase the next free numbers are: MX-030 · ST-34 · AG-023 · RB-08 · REG-13 · BX-018 ·
LEX-06 · SITE-06 · GM-16 · DEF-040 · RAT-29 · R-61 · V-18.

| Id | Task | File(s) | State |
|---|---|---|---|
| D-97 | GM-14 Completion Programme: inventory of 57 documents and the agent prompt | `00-governance-map/completion-programme.md` | **DONE** |
| D-98 | GM-13 Identifier Reallocation Record: 40 collisions | `00-governance-map/identifier-reallocation-record.md` | **DONE** |
| D-99 | License operational set: ML-OPS-1…3, Exhibits, plain-language companion, 2 pointers | `license/*` | **DONE** |
| D-100 | MX-025…MX-029 | `corpus/mx-025…029` | **DONE** |
| D-101 | AG-013…AG-022 | `agents/ag-013…022` | **DONE** |
| D-102 | ST-25…ST-33 | `standards/st-25…33` | **DONE** |
| D-103 | RB-06, RB-07 (rewritten after an interruption; read back) | `rubrics/rb-06, rb-07` | **DONE** |
| D-104 | REG-09…REG-12 (REG-09 to 11 rewritten after an interruption; read back) | `registries/reg-09…12` | **DONE** |
| D-105 | **BX-010…BX-017: the source BCIA programme restored** | `bcia/bx-010…017` | **DONE** |
| D-106 | LEX-04 Grammar, LEX-05 Contested Terms, SITE-05 Information Architecture | `lexicon/*`, `site/information-architecture.md` | **DONE** |
| D-107 | 46 pointer stubs (ST-32 T6) at legacy paths (+2 licence pointers under D-99) | corpus, standards, agents, rubrics, registries, bcia, templates, site | **DONE** |
| D-108 | Register appends: DEF-036…039, RAT-24…28, R-57…60, V-14…17, changelog | `00-governance-map/*` | **DONE** |
| D-109 | GM-15 Corpus Review | `00-governance-map/corpus-review-v2026.10.2.md` | **DONE** |
| D-110 | **Apply the GM-15 A-items** (repoint MX-014 §3, MX-000 §0.2, ST-01 prefix table, index titles, the ML-2.3 Publication Note, the BX-000…009 depth field) | many | **OPEN**: needs a Curator go-ahead, since each is an edit to canonical text |
| D-111 | **L-1 source pass by a human** on the 10 claims listed in GM-15 §5 | — | **OPEN** |
| D-112 | Curator ruling session: RAT-25, RAT-28(a–i) | — | **OPEN** |

**What Phase 8 found.** An empty search result is not evidence that something is absent. Text
search returned no matches for strings that were present (e.g. "T6" in ST-32, "## RAT-" in GM-04).
Every "missing" judgement in this phase was confirmed by listing the directory or reading the file.
The most consequential defect of the release, DEF-037, would have been missed by search alone.

---

## 11. Phase 9: v2027.1 source intake (2026-09-30)

**Instruction:** check the joined files ("you'll find all answers"), version and create new
documents, and adjust others where required.

| Id | Task | File | State |
|---|---|---|---|
| D-113 | Ingest 6 new sources; identify 21 held and 1 duplicate | `sources/` | **DONE** |
| D-114 | GM-16 intake review, written before any document | `00-governance-map/source-intake-v2027-1.md` | **DONE** (rewritten after an interruption, read back) |
| D-115 | HX-000 v2027.1 + CON-002 + v2026.10.1 banner | `harms/` | **DONE** |
| D-116 | ML-2.4 (draft, renumbered) · ML-B-1.0 (draft) · ML-2.3 note 5 · version history | `license/` | **DONE** |
| D-117 | BX-018 substrate register · BX-010 §9 · BX-010/011 HX corrections · BX-015…017 routes | `bcia/` | **DONE** |
| D-118 | MLT-000 programme register | `metax/programs/` | **DONE** |
| D-119 | SITE-06 nav delta · SITE-07 design and reader | `site/` | **DONE** |
| D-120 | BHS-2027-001 draft statement | `license/part-h-statement.md` §5.4 | **DONE** (draft, not issued) |
| D-121 | Registers: DEF-040…053, RAT-29…38, B-25, R-61…67, V-18…21, LEX-05, GM-13 §4a, changelog, index, README | many | **DONE** |
| D-122 | The 63 programme leaf pages; the 7 stratum pages; CF-1; CPF-1; the `license.json` forms | — | **PARTLY DONE 2026-10-08**: strata, CF-1, CPF-1, ST-34 schema done. Leaves staged (RAT-21). JSON files wait on the build |
| D-123 | Fix MX-014 §1 HX references (A-item, needs Curator approval) | `corpus/mx-014` | **OPEN** |
| D-124 | **Curator decisions:** RAT-29, RAT-33, RAT-34, RAT-35, RAT-36, RAT-37; B-25; signing (B-01) | — | **OPEN** |

**What Phase 9 found.** The v2026.10.2 self-review (GM-15) found no conflict in the harm layer.
Reading the new sources against the tier-1 text found that **the estate's own twenty-five-harm
register disagreed with its licence on most identities** (DEF-040). GM-15 §7 predicted that a
single-author review would miss exactly this kind of error, and it did.

---

## 12. Phase 10: review and completion (2026-09-30 → 2026-10-08)

**Instructions:** (1) "check all documents about missed documents … and any conflict or contradiction … save them into a review md file"; (2) "Complete the full documents in one session."

| Id | Task | File | State |
|---|---|---|---|
| D-125 | GM-17 full review (M-01…56, X-01…116, A-01…29) | `00-governance-map/corpus-review-v2027.1.md` | **DONE** |
| D-126 | CF-1 · ML-B-1.0 Schedules B-1/B-2 · CPF-1 · GM-20 decision records · ML-2.0 retained | `license/` | **DONE** |
| D-127 | GM-18 anomalies · GM-19 continuity · C-17, C-18 | `00-governance-map/` | **DONE** |
| D-128 | REG-13 decay calendar · REG-14 programme series | `registries/` | **DONE** |
| D-129 | ST-34 machine-form schemas | `standards/` | **DONE** (schemas only, by rule) |
| D-130 | MLT-01…09 charters; MLT-000 §4a–4b | `metax/programs/` | **DONE** (adoption: RAT-39) |
| D-131 | Seven stratum pages | `harms/strata/` | **DONE** |
| D-132 | SITE-08 Decision Queue · PR-1 · LEX-06 · 4 pointer stubs | various | **DONE** |
| D-133 | Registers: DEF-054…067, DEF-051 narrowed, RAT-39…44, V-22, V-09 close proposed, B-26, GM-13 §4b, GM-17 §8, index §14b, changelog, README | many | **DONE** |
| D-134 | GM-17 §5 A-items (edits to canonical text) | — | **OPEN: awaiting Curator approval** |
| D-135 | Human/third-party items M-01…M-11 etc.; build M-32…34; staged volume M-13, M-35, M-36 | — | **OPEN** (GM-17 §8.2) |

---

*Ledger opened 2026-09-02. Update in the same commit as the work.*
