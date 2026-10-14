---
doc_id: "MX-INDEX"
title_en: "The MetaX Universe — Canonical Source of Truth"
title_ar: "كون MetaX — المصدر المرجعي"
family: "governance-map"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 5
evidence_class: "durable"
curator: "Maher"
license: "ML-2.3 · Work of Foundational Character"
supersedes: ["THE METAX CORPUS v2026.09.0 (as consolidated)", "METAX v2026.09.1 Meta-Review (as consolidated)", "MetaX.Academy Page Content Specification (as consolidated)", "MX-DESIGN-001 numbering of MX-020/MX-021 (see R-25)", "MX-DESIGN-001 palette, route grammar and pillar hierarchy (see R-41, R-42, R-43)"]
last_reviewed: "2026-10-01"
hreflang: "en, ar"
---

# The MetaX Universe — Canonical Source of Truth

**Release v2026.10.1 · Founded, built and curated by Maher · Licensed under [ML-2.3](license/ml-2-3.md)**

This directory is the single entry point for humans and for machines. Every instrument
that governs the MetaX universe is a file here, at a permanent path, with front matter,
a version, and a stated authority. Nothing in this release is a summary of something
held elsewhere: where a document is a summary, it says so and names the text that governs.

> **Read this first.** Four prior documents were consolidated into this release: the
> corpus at v2026.09.0, the meta-review at v2026.09.1, the page content specification, and
> the UI/UX & Design System documentation (MX-DESIGN-001). They disagreed in thirty-seven
> places. Every disagreement is resolved, and every resolution is recorded with its reason in
> the [Reconciliation Ledger](00-governance-map/reconciliation-ledger.md).
> Where a resolution needs Maher's ratification rather than an editor's judgement, it is
> listed in [Open Questions and Ratifications](00-governance-map/open-questions-and-ratifications.md)
> and is marked in the affected instrument. No resolution was made silently.

> **The three changes in release v2026.10.1.** First, the estate learnt that it had **misspelt
> its own subject**: the name is **MacroLifeTech**, not MacroLifeTach, and the error had
> propagated with perfect consistency through forty-six ledger entries, a published anchor and
> four instruments. Every mechanism this corpus operates is a *consistency* mechanism, and a name
> wrong everywhere passes all of them ([C-13](00-governance-map/corrections-log.md#c-13)).
> Second, **the live site is a demo** — which does not falsify the nine code-derived findings of
> the last release but re-levels them: the design system stands at full authority, the content,
> copy, counts and posture findings are demoted to findings about a prototype
> ([C-14](00-governance-map/corrections-log.md#c-14)). Third, the estate acquired a **route
> grammar**: directory routes, three tiers, 321 English addresses, which discharges a task that
> had been blocked since the first day of this work.
>
> The methodological finding is the real content of the release. The last one established that
> reading the code found nine errors the documents could not. This one establishes the limit of
> that method: **reading an artefact tells you what is there, and cannot tell you what it is for
> or what its subject is called.** Both of this release's deepest corrections required the
> Curator, and the [Corrections Log §Method](00-governance-map/corrections-log.md#method-what-this-log-has-learned)
> now carries the resulting taxonomy — three error-finding methods, three blind spots, and only
> two of the three automatable.

> **The two changes in release v2026.09.4.** First, [**ML-2.3**](license/ml-2-3.md) supersedes the
> license layer, carrying a **Part H** that names twenty-five structural harms and makes them
> operative — conditioning permission on *structure* rather than only on *conduct*. Second, the
> estate was checked against its own running code for the first time, which produced **nine
> corrections** and six new defects. The documents were internally consistent and externally
> wrong; see the [Corrections Log](00-governance-map/corrections-log.md#method-what-this-log-has-learned).
>
> Three things in this release are unresolved **on the face of the instruments**, deliberately:
> ML-2.3 cites an ML-2.2 the estate has never published
> ([RAT-14](00-governance-map/open-questions-and-ratifications.md#rat-14--does-ml-22-exist));
> behavioural ad networks are live on the content plane, engaging HX-01 and HX-04
> ([RAT-15](00-governance-map/open-questions-and-ratifications.md#rat-15--will-the-estate-publish-its-own-harms-as-unremedied));
> and the site does not render without JavaScript, contrary to its own stated law
> ([RAT-17](00-governance-map/open-questions-and-ratifications.md#rat-17--pre-render-or-remain-javascript-only)).
> None is presented as settled.

> **The architectural change in release v2026.09.2.** MX-DESIGN-001 introduced authentication,
> payment and per-user state into a universe whose published doctrine denied all three. The
> Static Principle is therefore **partitioned, not abandoned**: the estate now runs a
> **Content Plane** (static, archivable, crawlable) and an **Identity & Commerce Plane**
> (`auth.`, `pay.`, `me.` — stateful, never indexed, never archived), separated by one
> load-bearing rule — *the content plane may be decorated by the identity plane but never
> depends on it.* The doctrine page at `/about/static/` is **rewritten and dated**, not
> quietly contradicted. See [ST-19](standards/st-19-two-plane-architecture.md) and
> [R-26](00-governance-map/reconciliation-ledger.md#r-26--the-static-principle-is-partitioned-not-abandoned).

---

## 1. How to read this corpus

| If you are | Start at | Then |
|---|---|---|
| A human reader | [MX-001 About MetaX](corpus/mx-001-about-metax.md) | [MX-000 The Charter](corpus/mx-000-charter.md) |
| An AI system | [Machine Reading Contract](00-governance-map/machine-reading-contract.md) | [ST-14 Machine Surfaces](standards/st-14-machine-surfaces-and-json-schemas.md) |
| A builder of the site | [Site Information Architecture](site/information-architecture.md) | [ST-01 Identifier & URL Grammar](standards/st-01-identifier-and-url-grammar.md) |
| A reviewer or assessor | [RB-01 The D1–D5 Rubric](rubrics/rb-01-d1-d5-rubric.md) | [MX-005 Credentialing](corpus/mx-005-credentialing-and-assessment.md) |
| A founding curator | [MX-004 Terms of Top Levels](corpus/mx-004-terms-of-top-levels.md) | [ST-18 academy.json](standards/st-18-academy-json-manifest.md) |
| A lawyer or counsel | [ML-2.3](license/ml-2-3.md) | [Two-Track Enforceability Table](license/enforceability-two-track-table.md) |
| A skeptic | [Corrections Log](00-governance-map/corrections-log.md) | [Defect Register](00-governance-map/defect-register.md) |
| A designer | **[DS-00 As-Built Token Layer](design/ds-00-as-built-token-layer.md)** | [DS-02 Motion and Attention](design/ds-02-motion-and-attention.md) |
| An engineer on auth or pay | [ST-19 Two-Plane Architecture](standards/st-19-two-plane-architecture.md) | [ST-16 Security Architecture](standards/st-16-security-architecture.md) |
| Anyone resuming this work | **[Task Ledger](00-governance-map/task-ledger.md)** | [Open Questions](00-governance-map/open-questions-and-ratifications.md) |
| Assessing a deployment's harms | **[HX-000 The Register](harms/hx-000-structural-harms.md)** | [ML-2.3 Part H](license/ml-2-3.md#part-h--structural-harms-and-the-duty-of-non-amplification) |
| Building or generating pages | **[SITE-01 Route Manifest](site/route-manifest.md)** | [SITE-02 Page Contract](site/page-contract.md) · [ST-24 Prose Standard](standards/st-24-page-prose-standard.md) |
| Wondering what is actually built | **[SITE-04 Demo Notice](site/demo-notice.md)** | [Defect Register](00-governance-map/defect-register.md) |

Authority is resolved by one document and one document only:
**[Precedence and Conflict Rules](00-governance-map/precedence-and-conflict-rules.md).**
If two files in this directory appear to conflict, that file decides which governs, and
the conflict is a defect to be filed — not a matter for interpretation.

---

## 2. Governance map

| Document | Purpose |
|---|---|
| [Precedence and Conflict Rules](00-governance-map/precedence-and-conflict-rules.md) | Which instrument governs when two disagree. |
| **[Document Index](00-governance-map/document-index.md)** | Every instrument with its **existence state** — EXISTS / PARTIAL / REFERENCED / DEFERRED. **Read this before concluding a broken link here is confusion:** this index is an *architecture*, and roughly seventy of its paths do not yet resolve. |
| [Reconciliation Ledger](00-governance-map/reconciliation-ledger.md) | Fifty-six source conflicts and how each was resolved, in four parts. |
| [Task Ledger](00-governance-map/task-ledger.md) | Work in progress and committed backlog, so it survives context loss. |
| [Open Questions and Ratifications](00-governance-map/open-questions-and-ratifications.md) | What only Maher can decide, with the decision each blocks. |
| [Launch Blockers](00-governance-map/launch-blockers.md) | What must be true before anything ships publicly. |
| [Changelog](00-governance-map/changelog.md) | This release and its predecessors, with reasons. |
| [Corrections Log](00-governance-map/corrections-log.md) | Every claim the estate published and later found **wrong**, corrected in public. |
| **[Verification Log](00-governance-map/verification-log.md)** | Every `[VERIFY]` tag and **its age**. Thirteen open, **none ever closed**, four checkable in minutes. |
| [Defect Register](00-governance-map/defect-register.md) | Thirty-three defects with owners and target dates, published deliberately. |
| **[Archive Register](00-governance-map/archive-register.md)** | Superseded text, retained permanently — and **§4 discloses two texts already unretrievable**, because the archive rule predated the archive (DEF-029). Class D, withdrawn duties, is **empty**. |
| **[Machine Reading Contract](00-governance-map/machine-reading-contract.md)** | Five conditions on a machine reader, six signals owed by the corpus — of which the estate currently delivers three. |

## 3. The license layer

| Document | Purpose |
|---|---|
| **[ML-2.3 — Maher's License](license/ml-2-3.md)** | **The governing instrument.** Constitutional substrate of everything else. Carries Part H. |
| [ML-2.1](license/ml-2-1.md) | Published predecessor, retained permanently. Superseded in estate practice. |
| [Plain-Language Companion](license/ml-2-1-plain-language.md) | Non-operative reader's edition. **Needs re-basing to 2.3.** |
| **[Two-Track Enforceability Table](license/enforceability-two-track-table.md)** | Per clause: contract, representation, or moral norm. **§6 adds 23 Part H rows** and the §F.4 condition/covenant split — four conditions that terminate automatically, nineteen covenants with a cure window. |
| **[Designation List](license/designation-list.md)** | Works of Foundational Character. **DL-2** adds HX-000, ML-2.3/Part H, HX-001 and the Schedule 1 form; two close calls excluded with reasons. Still unratified. |
| **[Part H Statement](license/part-h-statement.md)** | Schedule 1 form **and** the estate's own statement, which is **NOT YET ISSUED** and says why on its face — [RAT-15](00-governance-map/open-questions-and-ratifications.md#rat-15--will-the-estate-publish-its-own-harms-as-unremedied). |
| **[Scale Gate Worksheet](license/scale-gate.md)** | Schedule 2: four tiers, five qualitative tests, **three unpublished thresholds**. The absolutes bind at every tier including Tier 0. |
| [Registry, Mirrors and Continuity](license/registry-and-mirrors.md) | §E.7 in operational form. |
| [Steward Succession](license/steward-succession.md) | §E.8 in operational form. |
| [Determinations Procedure](license/determinations-procedure.md) | Parts D and G in operational form. |
| [Exhibits and Notices](license/exhibits.md) | Exhibits 1–3, copyable. |
| **[License Version History](license/version-history.md)** | ML-1.0 → 1.1 → 2.0 → 2.1 → **[gap]** → 2.3, with reasons — and the ML-2.2 gap declared rather than reconstructed. |

> **Two defects sit on the face of ML-2.3** and are declared in its Publication Note rather than
> hidden: it declares `supersedes: ML-2.2` where no ML-2.2 has ever been published (ML-D-007), and
> §A.10 incorporates HX-000 v2026.10.1, which does not yet exist (ML-D-008). It is also **not
> reviewed by counsel** in any jurisdiction (ML-D-010). `status: canonical` records its standing
> in the estate's own governance; it is not a representation that the instrument has been tested
> in any forum.

## 3a. The harms register (HX)

The register incorporated by [ML-2.3 Part H](license/ml-2-3.md#h2-the-twenty-five-named-harms).
Twenty-five structural harms in six strata, each with a mechanism, an evidence base, its
strongest counter-argument, a reply, an ethical mapping, **a falsifier**, and the obligation it
creates.

| Id | Document | Purpose |
|---|---|---|
| HX-000 | [The Structural Harms of Computing, Networking and Technological Order](harms/hx-000-structural-harms.md) | The Register. Incorporated by reference at §A.10. |
| HX-001 | **[Harm Audit Rubric](harms/hx-001-harm-audit-rubric.md)** | Five dimensions, twenty-five tuples, the §H.7 counterproductivity test — and **no total score**, deliberately. |
| HX-002 | **[Harm → Instrument Map](harms/hx-002-harm-instrument-map.md)** | Which instrument answers which harm, and **which three harms MetaX currently commits**: HX‑01, HX‑04, HX‑15. Two more are `unexamined`. |

> **The falsifier is the load-bearing part.** Every harm states the evidence that would withdraw
> or narrow it, and ML-2.3 §E.5 obliges the steward to narrow or withdraw the corresponding duty
> when a falsification is demonstrated. *A register whose entries have never been narrowed is
> presumptively a doctrine and should be distrusted accordingly.*

## 4. The corpus instruments (MX)

| Id | Document |
|---|---|
| MX-000 | [The MetaX Charter](corpus/mx-000-charter.md) |
| MX-001 | [About MetaX](corpus/mx-001-about-metax.md) |
| MX-002 | [Terms of Service](corpus/mx-002-terms-of-service.md) |
| MX-003 | [Privacy Notice](corpus/mx-003-privacy-notice.md) |
| MX-004 | [Terms of Top Levels](corpus/mx-004-terms-of-top-levels.md) · [Annex A — Technical](corpus/mx-004-annex-a-technical-requirements.md) |
| MX-005 | [Credentialing and Assessment](corpus/mx-005-credentialing-and-assessment.md) · [Annex A — Naming Map](corpus/mx-005-annex-a-credential-naming-map.md) |
| MX-006 | [Editorial and Evidence Policy](corpus/mx-006-editorial-and-evidence.md) |
| MX-007 | **[AI Use and Disclosure](corpus/mx-007-ai-use-and-disclosure.md)** — four use classes, five prohibitions, a volume gate; **discloses its own AI authorship** |
| MX-008 | **[Content Governance and Moderation](corpus/mx-008-moderation-and-enforcement.md)** — nine red lines; a policy that is largely a list of surfaces the estate **declined to build** |
| MX-009 | **[Advertising and Commercial Policy](corpus/mx-009-advertising-and-commercial.md)** — six cumulative conditions, **three of which the estate currently fails** |
| MX-010 | **[Accessibility Statement](corpus/mx-010-accessibility.md)** — WCAG 2.2 AA plus five extras; **three known failures, zero tests by an assistive-technology user** |
| MX-011 | [Security and Responsible Disclosure](corpus/mx-011-security-and-disclosure.md) |
| MX-012 | **[Licensing and Reuse](corpus/mx-012-licensing-and-reuse.md)** — a summary that governs nothing and is what most readers will rely on |
| MX-013 | **[Records, Versioning and Corrections](corpus/mx-013-records-and-versioning.md)** — six registers, four permanence rules |
| MX-014 | **[Research Ethics and Hard Exclusions](corpus/mx-014-research-ethics-and-exclusions.md)** — three refusals, five exclusions, **no ethics reviewer** |
| MX-015 | **[Succession and Institutional Continuity](corpus/mx-015-succession-and-continuity.md)** — four roles of which **three are unfilled**; §4 walks through the estate dying tonight |
| MX-016 | **[Complaints, Appeals and Due Process](corpus/mx-016-appeals-and-due-process.md)** — five guarantees, three stages, **one unstaffable** |
| MX-017 | [Trademark and Brand Use](corpus/mx-017-trademark-and-brand.md) |
| MX-018 | [Data Retention Schedule](corpus/mx-018-data-retention.md) |
| MX-019 | [Conflicts of Interest](corpus/mx-019-conflicts-of-interest.md) |
| MX-020 | [Language Authority and Bilingual Parity](corpus/mx-020-language-authority.md) |
| MX-021 | [Payments and Commerce](corpus/mx-021-payments-and-commerce.md) |
| MX-022 | [Identity and Sessions](corpus/mx-022-identity-and-sessions.md) |
| MX-023 | [Attention and Human Sovereignty](corpus/mx-023-attention-and-human-sovereignty.md) |
| MX-024 | [Infrastructure, Capacity and Migration](corpus/mx-024-infrastructure-and-migration.md) |

> **Second numbering note.** The architecture source's Part 14 proposes "MX-022 Infrastructure &
> Migration." `MX-022` is already Identity and Sessions, so under the same immortal-numbers rule
> the infrastructure instrument takes **MX-024** — MX-023 having been allocated to Attention and
> Human Sovereignty, required by ML-2.3 Part H. Same reasoning as R-25.

> **Numbering note.** MX-DESIGN-001 Part 11 requested Payments as `MX-020` and Identity as
> `MX-021`. `MX-020` was already allocated in this release to Language Authority, and under
> [ST-01 Rule 2](standards/st-01-identifier-and-url-grammar.md#3-rule-2--numbers-are-immortal)
> numbers are immortal from first assignment. Payments is therefore **MX-021** and Identity is
> **MX-022**. Reasoning at [R-25](00-governance-map/reconciliation-ledger.md#r-25--the-mx-020-numbering-collision).

## 5. The agent instruments (AG)

| Id | Document |
|---|---|
| AG-000 | [Agent Constitution](agents/ag-000-agent-constitution.md) |
| AG-001 | [The Sole Prompter Protocol](agents/ag-001-sole-prompter-protocol.md) |
| AG-002 | [Agent Roster and Role Charters](agents/ag-002-roster-and-role-charters.md) |
| AG-003 | [The Standing System Prompt (Kernel)](agents/ag-003-standing-system-prompt.md) |
| AG-004 | [Refusal and Escalation Register](agents/ag-004-refusal-and-escalation-register.md) |
| AG-005 | [Output Contract and Provenance](agents/ag-005-output-contract-and-provenance.md) |
| AG-006 | [Evidence and Citation Protocol](agents/ag-006-evidence-and-citation-protocol.md) |
| AG-007 | [Agent Change Control](agents/ag-007-change-control.md) |
| AG-008 | [Human-in-the-Loop Gates](agents/ag-008-human-in-the-loop-gates.md) |
| AG-009 | [Prohibited Agent Actions](agents/ag-009-prohibited-actions.md) |
| AG-010 | [Agent Evaluation Rubric](agents/ag-010-evaluation-rubric.md) |
| AG-011 | [Series Generation Agent Charter](agents/ag-011-series-generation-charter.md) |
| AG-012 | [Degraded Mode and Prompter Succession](agents/ag-012-degraded-mode-and-succession.md) |

## 6. The standards (ST)

| Id | Document |
|---|---|
| ST-01 | **[Identifier, Naming and URL Grammar](standards/st-01-identifier-and-url-grammar.md)** — nineteen prefixes; **numbers are immortal** |
| ST-02 | **[Front-Matter Schema](standards/st-02-front-matter-schema.md)** — eighteen required fields, eleven conditional, **no validator** |
| ST-03 | **[The Limits and Bridge Standard](standards/st-03-limits-and-bridge.md)** — four limit classes; the Bridge may point **out of the estate** |
| ST-04 | **[Falsifiability and Claim Cards](standards/st-04-falsifiability-and-claim-cards.md)** — four counterfeit falsifiers named; `IF FALSE` is the operative field |
| ST-05 | **[Decay Classes and Review Intervals](standards/st-05-decay-and-review-intervals.md)** — three classes; carries the **provenance-of-purpose** amendment |
| ST-06 | **[The Objections Standard](standards/st-06-objections-standard.md)** — §4 files the estate's strongest objection to itself as **`open`** |
| ST-07 | **[Evidence, Citation and the VERIFY Tag](standards/st-07-evidence-and-verify.md)** — E0–E4; E1 is legitimate and under-used |
| ST-08 | [The Cognitive Arc and Series Architecture](standards/st-08-cognitive-arc.md) |
| ST-09 | [Unit Economics and Kill Criteria](standards/st-09-unit-economics-and-kill-criteria.md) |
| ST-10 | [Style Guide (English)](standards/st-10-style-guide-en.md) |
| ST-11 | [Arabic Authoring and Bilingual Parity](standards/st-11-arabic-authoring.md) |
| ST-12 | **[Accessibility Implementation](standards/st-12-accessibility-implementation.md)** — six pattern families, nine tests; **three have run, two of those failed** |
| ST-13 | **[Static Build and the SENTINEL Contract](standards/st-13-static-build-and-sentinel.md)** — five check families, **none running**; the corpus's largest rules-without-mechanisms instance |
| ST-14 | **[Machine Surfaces and JSON Schemas](standards/st-14-machine-surfaces-and-json-schemas.md)** — nine surfaces, three refused; **none exists yet** |
| ST-15 | [Component Library Standard](standards/st-15-component-library.md) |
| ST-16 | [Security Architecture and Dynamic Exceptions](standards/st-16-security-architecture.md) |
| ST-17 | [Credential Registry and Verifier Specification](standards/st-17-registry-and-verifier.md) |
| ST-18 | [academy.json Manifest Specification](standards/st-18-academy-json-manifest.md) |
| ST-19 | [Two-Plane Architecture and the Island Contract](standards/st-19-two-plane-architecture.md) |
| ST-20 | [Payment Integration and Webhook Trust](standards/st-20-payment-integration.md) |
| ST-21 | [Performance Budgets and Enforcement](standards/st-21-performance-budgets.md) |
| ST-22 | [Platform, Persistence and the Capacity Meter](standards/st-22-platform-and-persistence.md) |
| ST-23 | **[Affiliate and Referral Standard](standards/st-23-affiliate-and-referral.md)** — *designed from scratch; no upstream source exists* |
| ST-24 | **[Page Prose Standard](standards/st-24-page-prose-standard.md)** — the eight-part recipe and the three registers |

## 6a. The design system (DS)

Added in v2026.09.2 from [MX-DESIGN-001](../sources/MetaX.Academy_UI-UX_and_Design_System_Documentation.md).

> **Corrected in v2026.09.4.** The as-built review established that DS-01's "Ink-and-Paper"
> identity, its ten gradients and its per-brand palettes **are not the live system**, and that the
> motion hierarchy was understated by a whole tier. **[DS-00](design/ds-00-as-built-token-layer.md)
> is now the governing token document.** DS-01's palette sections are retained with a
> non-governing banner rather than rewritten, per
> [Charter §0.8](corpus/mx-000-charter.md) — a corpus that edits its errors into agreement cannot
> be audited for how long it was wrong. See [C-02](00-governance-map/corrections-log.md#c-02),
> [C-03](00-governance-map/corrections-log.md#c-03), [C-06](00-governance-map/corrections-log.md#c-06).

| Id | Document |
|---|---|
| **DS-00** | **[The As-Built Token Layer](design/ds-00-as-built-token-layer.md)** — governing |
| DS-01 | [Design Foundations, Tokens and the Gradient System](design/ds-01-foundations-and-tokens.md) — *superseded in part* |
| DS-02 | [Motion, Attention and the Anti-Engagement Commitments](design/ds-02-motion-and-attention.md) |
| DS-03 | [Responsive Component Behaviour](design/ds-03-responsive-components.md) |
| DS-04 | [The Twelve Academic Features](design/ds-04-academic-features.md) |
| DS-05 | [Certification Surfaces — Record, Document, Share Card](design/ds-05-certification-surfaces.md) |
| DS-06 | [Error, Empty and Degraded States](design/ds-06-error-and-empty-states.md) |
| **DS-07** | **[Navigation Geometry and the Fluid Nav](design/ds-07-navigation-geometry.md)** — nine pillars, the 1180px breakpoint |

## 7. Rubrics (RB)

| Id | Document |
|---|---|
| RB-01 | **[The D1–D5 Assessment Rubric](rubrics/rb-01-d1-d5-rubric.md)** — five dimensions, **no total score**, frozen per cohort |
| RB-02 | **[The Proof Ladder P0–P3](rubrics/rb-02-proof-ladder.md)** — P0 is uncreditable; the level is printed on the credential |
| RB-03 | [Structural Review and Build Gates](rubrics/rb-03-structural-review.md) |
| RB-04 | [Agent Evaluation Specimen Set](rubrics/rb-04-agent-evaluation-specimens.md) |
| RB-05 | **[The Harm Review Gate](rubrics/rb-05-harm-review-gate.md)** — six checks, three outcomes, **no pass**; the estate's own artefact returns RETURNED |

## 8. Registries (REG)

| Id | Document |
|---|---|
| REG-01 | [Series Registry](registries/reg-01-series-registry.md) |
| REG-02 | [Branch Registry](registries/reg-02-branch-registry.md) |
| REG-03 | [Book Registry](registries/reg-03-book-registry.md) |
| REG-04 | [Document Registry](registries/reg-04-document-registry.md) |
| REG-05 | [Credential Registry Specification and Roster](registries/reg-05-credential-registry.md) |
| REG-06 | [Academy Registry](registries/reg-06-academy-registry.md) |
| REG-07 | [Determinations Registry](registries/reg-07-determinations-registry.md) |
| REG-08 | [Processors, Keys and Mirrors Registry](registries/reg-08-processors-keys-mirrors.md) |

## 9. BCIA (BX)

| Id | Document |
|---|---|
| BX-000 | [BCIA Document Zero](bcia/bx-000-document-zero.md) |
| BX-001 | [BCIA Research Charter](bcia/bx-001-research-charter.md) |
| BX-002 | [The Human-Cell Exclusion](bcia/bx-002-human-cell-exclusion.md) |
| BX-003 | [Remediation Gates and Public Status](bcia/bx-003-remediation-gates.md) |
| BX-004 | [Observed Taxonomy — Evidence Report](bcia/bx-004-observed-taxonomy.md) |
| BX-005 | [Notation Freeze — AMN, LPN, BSN](bcia/bx-005-notation-freeze.md) |
| BX-006 | [Critical Audit](bcia/bx-006-critical-audit.md) |
| BX-007 | [Open Problems Register](bcia/bx-007-open-problems.md) |
| BX-008 | [The Refused Inference](bcia/bx-008-refused-inference.md) |
| BX-009 | [Contribution Without a Laboratory](bcia/bx-009-contribution.md) |

## 10. The site layer (SITE)

**Rewritten in v2026.10.1.** The estate is **one origin with directory routes**, not eight
content subdomains. The previous entries in this section described `toptech.metax.academy`,
`bcia.metax.academy` and a route grammar that do not exist
([C-04](00-governance-map/corrections-log.md#c-04), C-15). They are retained in the
[Archive Register](00-governance-map/archive-register.md) rather than deleted, and superseded by
the four instruments below.

| Id | Document | Purpose |
|---|---|---|
| **SITE-01** | **[The Route Manifest](site/route-manifest.md)** | Every address the estate publishes: 9 pillars, 45 group hubs, 266 leaves, 321 English routes, plus the parametric families and the tier contract. **Discharges task A-09.** |
| **SITE-02** | **[The Page Contract](site/page-contract.md)** | The skeleton, the four required components (`.mx-pagestamp`, `.mx-related`, `.mx-exitpair`, `.mx-demo`) and twenty acceptance criteria. |
| **SITE-03** | **[Routing Law and the Redirect Record](site/routing-law.md)** | Seven conditions for a well-formed address; the append-only redirect record; the root-absolute build law. |
| **SITE-04** | **[The Demo Notice](site/demo-notice.md)** | Audience-tier-1 statement of what is real and what is scaffolding. Required by [B-20](00-governance-map/launch-blockers.md). |

> **Three of the twenty acceptance criteria are currently failed by the estate's own demo:**
> no-JavaScript rendering ([DEF-018](00-governance-map/defect-register.md#def-018)), the
> `prefers-reduced-motion` block ([B-16](00-governance-map/launch-blockers.md)) and the 44px touch
> target floor ([DEF-022](00-governance-map/defect-register.md#def-022)). The contract is stricter
> than the artefact it derives from, which is the correct direction for a contract to point.

> **Nothing in the site layer has been generated.** The estate now holds a route manifest, a page
> contract, a routing law, a prose standard and a nav geometry — the complete apparatus for
> producing 321 pages — and has produced none of them. That order is deliberate: a structure can
> be criticised cheaply before it is full, and after ≈385,000 words are written, criticising the
> structure costs a rewrite.

## 11. Lexicon and MetaX grammar

| Document | Purpose |
|---|---|
| [Keyword Register](lexicon/keyword-register.md) | Every MetaX keyword, resolving to the document that defines it. |
| [MetaX Grammar](lexicon/metax-grammar.md) | The full notation: identifiers, versions, statuses, glyphs, tags. |
| [Lexicon Entry Standard](lexicon/lexicon-entry-standard.md) | The six required fields of a term entry. |
| [Contested Terms Register](lexicon/contested-terms.md) | Terms that currently mean two things, with resolution state. |

## 12. Templates

| Document | Purpose |
|---|---|
| [Document and Page Templates](templates/document-and-page-templates.md) | Front matter, changelog entry, correction, determination, defect. |
| [Assessment and Academy Templates](templates/assessment-and-academy-templates.md) | Dossier, evidence log, pre-registration, application, term sheet. |

---

## 13. Release posture, stated honestly

- **Canonical release:** v2026.09.2 · **Last reviewed:** 2026-08-30 · **Curator:** Maher.
- **Properties:** seven content-plane properties + three identity-plane properties + an
  unbounded set of academy subdomains ([R-30](00-governance-map/reconciliation-ledger.md#r-30--the-property-count-changes-again--seven-becomes-seven-plus-three)).
  Identity-plane routes are **not** added to the published route count, because a route behind
  a session is not a published page.
- **Series in the registry:** enumerated in [REG-01](registries/reg-01-series-registry.md).
  Counts on any generated page are computed from front matter and never typed
  ([ST-13](standards/st-13-static-build-and-sentinel.md)).
- **Nothing here is public yet.** Publication is blocked by
  [Launch Blockers](00-governance-map/launch-blockers.md), of which the unsigned license
  placeholders are the first and the hardest.
- **Known gaps are published, not managed.** See
  [Defect Register](00-governance-map/defect-register.md) and
  [Open Questions](00-governance-map/open-questions-and-ratifications.md).
- **Source history is retained** in [`/sources/`](../sources/) and indexed in
  [Archive Register](00-governance-map/archive-register.md). Nothing was deleted and
  nothing was silently edited.

---

## 14. Release v2026.10.2: displaced subjects and new instruments

> **Read this before following any link in §§4–12.** Forty identifiers in those sections were
> allocated to one subject and are now occupied by another ([GM-13](00-governance-map/identifier-reallocation-record.md)).
> The links in §§4–12 still resolve, but many resolve to a **pointer stub** that names the refuge
> number below. §§4–12 are left unedited, because they are the record of the original allocations.
> Ruling pending: [RAT-25](00-governance-map/open-questions-and-ratifications.md#rat-25).
> **The review of this release is [GM-15](00-governance-map/corpus-review-v2026.10.2.md).**

| Family | Refuge / new instruments |
|---|---|
| GM | [GM-13 Identifier Reallocation Record](00-governance-map/identifier-reallocation-record.md) · [GM-14 Completion Programme](00-governance-map/completion-programme.md) · **[GM-15 Corpus Review v2026.10.2](00-governance-map/corpus-review-v2026.10.2.md)** |
| MX | [MX-025 Credentialing and Assessment](corpus/mx-025-credentialing-and-assessment.md) · [MX-026 Editorial and Evidence](corpus/mx-026-editorial-and-evidence.md) · [MX-027 Trademark and Brand](corpus/mx-027-trademark-and-brand.md) · [MX-028 Data Retention](corpus/mx-028-data-retention.md) · [MX-029 Academies Charter](corpus/mx-029-academies-charter.md) |
| AG | [AG-013 Sole Prompter](agents/ag-013-sole-prompter-protocol.md) · [AG-014 Roster](agents/ag-014-roster-and-role-charters.md) · [AG-015 Standing Prompt](agents/ag-015-standing-system-prompt.md) · [AG-016 Output Contract](agents/ag-016-output-contract-and-provenance.md) · [AG-017 Evidence](agents/ag-017-evidence-and-citation-protocol.md) · [AG-018 Change Control](agents/ag-018-change-control.md) · [AG-019 HITL Gates](agents/ag-019-human-in-the-loop-gates.md) · [AG-020 Evaluation](agents/ag-020-evaluation-rubric.md) · [AG-021 Series Generation](agents/ag-021-series-generation-charter.md) · [AG-022 Degraded Mode](agents/ag-022-degraded-mode-and-succession.md) |
| ST | [ST-25 Cognitive Arc](standards/st-25-cognitive-arc.md) · [ST-26 Unit Economics](standards/st-26-unit-economics-and-kill-criteria.md) · [ST-27 Style Guide](standards/st-27-style-guide-en.md) · [ST-28 Components](standards/st-28-component-library.md) · [ST-29 Security](standards/st-29-security-architecture.md) · [ST-30 Registry/Verifier](standards/st-30-registry-and-verifier.md) · [ST-31 academy.json](standards/st-31-academy-json-manifest.md) · [ST-32 Templates](standards/st-32-document-and-page-templates.md) · [ST-33 Assessment Templates](standards/st-33-assessment-and-academy-templates.md) |
| RB | [RB-06 Structural Review](rubrics/rb-06-structural-review.md) · [RB-07 Agent Specimens](rubrics/rb-07-agent-evaluation-specimens.md) |
| REG | [REG-09 Branch](registries/reg-09-branch-registry.md) · [REG-10 Academy](registries/reg-10-academy-registry.md) · [REG-11 Determinations](registries/reg-11-determinations-registry.md) · [REG-12 Processors, Keys, Mirrors](registries/reg-12-processors-keys-mirrors.md) |
| **BX (research programme)** | [BX-010 Document Zero + Charter](bcia/bx-010-document-zero-and-research-charter.md) · [BX-011 Human-Cell Exclusion](bcia/bx-011-human-cell-exclusion.md) · [BX-012 Gates and Status](bcia/bx-012-remediation-gates-and-public-status.md) · [BX-013 Observed Taxonomy](bcia/bx-013-observed-taxonomy.md) · [BX-014 Notation Freeze](bcia/bx-014-notation-freeze.md) · [BX-015 Audit and Open Problems](bcia/bx-015-critical-audit-and-open-problems.md) · [BX-016 Refused Inference](bcia/bx-016-refused-inference.md) · [BX-017 Contribution](bcia/bx-017-contribution-without-a-laboratory.md) |
| BX (reading model, v2026.10.1) | [BX-000 "BCIA Charter"](bcia/bx-000-bcia-charter.md) … BX-009: they keep their numbers. The acronym ruling is pending (RAT-28(a)) |
| LEX | [LEX-04 Grammar](lexicon/metax-grammar.md) · [LEX-05 Contested Terms](lexicon/contested-terms.md) |
| SITE | [SITE-05 Information Architecture](site/information-architecture.md) |

### 14a. v2027.1 intake (2026-09-30): all new instruments are **drafts**

| Family | Instruments |
|---|---|
| GM | **[GM-16 Source Intake v2027.1](00-governance-map/source-intake-v2027-1.md)**: start here for this release |
| HX | [HX-000 v2027.1 · The Register of Structural Harms](harms/hx-000-register-v2027-1.md) (28 harms) · [CON-002 Harm Concordance](harms/con-002-harm-numbering-concordance.md) |
| ML | [ML-2.4 (draft delta)](license/ml-2-4.md) · [ML-B-1.0 BCIA Profile (draft)](license/ml-b-1-0.md). **ML-2.3 remains the licence of record and is unsigned** |
| BX | [BX-018 · Register of Substrate Harms](bcia/bx-018-register-of-substrate-harms.md) (source label "BX-000 v1.0") · BX-010 §9 Document Zero v1.0 |
| MLT | [MLT-000 · Programme Register: the nine MacroLifeTech programmes](metax/programs/mlt-000-programme-register.md) |
| SITE | [SITE-06 Nav v2027.1](site/mx-nav-spec-v2027-1.md) · [SITE-07 Design v2027.1 and MX-READER-01](site/mx-site-design-v2027-1.md) |

### 14b. Review and completion pass (2026-10-08): all **drafts**

> **The review of the v2027.1 corpus is [GM-17](00-governance-map/corpus-review-v2027.1.md).** It lists 56 missing
> documents and 54 conflicts. §8 maps what this pass wrote and what still cannot be written.

| Family | Instruments |
|---|---|
| GM | **[GM-17 Corpus Review v2027.1](00-governance-map/corpus-review-v2027.1.md)** · [GM-18 Anomaly Register](00-governance-map/anomaly-register.md) · [GM-19 Continuity Register](00-governance-map/continuity-register.md) · [GM-20 Decision Record Register](license/decision-record-register.md) |
| Licence forms | [CF-1 Compliance File](license/cf-1-compliance-file-template.md) · [ML-B-1.0 Schedules B-1/B-2](license/ml-b-1-0-schedules-b1-b2.md) · [CPF-1 Comment Period](license/cpf-1-comment-period-publication-format.md) · [ML-2.0 (retained)](license/ml-2-0.md) |
| HX strata | [I](harms/strata/stratum-i-cognitive.md) · [II](harms/strata/stratum-ii-relational-political.md) · [III](harms/strata/stratum-iii-economic-structural.md) · [IV](harms/strata/stratum-iv-material-temporal.md) · [V](harms/strata/stratum-v-reflexive.md) · [VI](harms/strata/stratum-vi-successor.md) · [VII (not in force)](harms/strata/stratum-vii-custodial.md) |
| MLT | [01 Agora](metax/programs/mlt-01-agora-charter.md) · [02 Maʿnā](metax/programs/mlt-02-mana-charter.md) · [03 Metabolism](metax/programs/mlt-03-metabolism-charter.md) · [04 Soma](metax/programs/mlt-04-soma-charter.md) · [05 Paideia](metax/programs/mlt-05-paideia-charter.md) · [06 Athar](metax/programs/mlt-06-athar-charter.md) · [07 Āfāq](metax/programs/mlt-07-afaq-charter.md) · [08 Mīzān](metax/programs/mlt-08-mizan-charter.md) · [09 BCIA](metax/programs/mlt-09-bcia-charter.md) |
| ST / REG | [ST-34 Licence machine forms](standards/st-34-licence-and-register-machine-forms.md) · [REG-13 Decay Calendar](registries/reg-13-decay-calendar.md) · [REG-14 Programme series](registries/reg-14-programme-series-registry.md) |
| SITE / templates / LEX | [SITE-08 Decision Queue](site/site-08-decision-queue.md) · [PR-1 Pre-registration](templates/pr-1-preregistration-form.md) · [LEX-06 Term entries](lexicon/lex-06-term-entries-governance-set.md) |

**§1 routing table, corrected here rather than in place:** "A reviewer or assessor → MX-005" now
means [MX-025](corpus/mx-025-credentialing-and-assessment.md). "A founding curator → ST-18" now
means [ST-31](standards/st-31-academy-json-manifest.md) and [MX-029](corpus/mx-029-academies-charter.md).
"An engineer → ST-16" now means [ST-29](standards/st-29-security-architecture.md).

*Curated by Maher. Where this corpus is wrong, the correction is published — not the
argument that it was never wrong.*
