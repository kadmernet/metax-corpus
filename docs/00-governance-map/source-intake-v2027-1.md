---
doc_id: "GM-16"
title_en: "Source Intake v2027.1 — Review, Answers and Decisions"
title_ar: "استلام مصادر v2027.1 — المراجعة والإجابات والقرارات"
family: "governance-map"
version: "v2027.1-intake"
status: "draft"
authority: "record"
prevailing_text: "en"
audience_tier: 5
depth: 5
evidence_class: "perishable"
review_interval_months: 3
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-09-30"
domain_tags: ["governance", "intake", "reconciliation", "v2027.1", "licence-chain", "harms"]
route: "/library/record/intake/v2027-1/"
derived_from: "sources/METAX_CORPUS_SOURCE_BUNDLE_v2027.1.md; sources/BX-000_and_HX-000_v2027.1.md; sources/ML-2.4_clauses.md; sources/ML-2.4_requirements.md; sources/ML-B-1.0_profile.md; sources/README_v2027.1.md; held docs/license/ml-2-3.md and docs/harms/*"
provenance_of_purpose: "record"
human_read: "none"
conformance_state: "partial"
authorship_note: "Written by an AI system under AG-000 BEFORE any v2027.1 document was generated, as the Source Bundle Part 7 §1 requires. Every decision marked PROPOSED is the Curator's."
hreflang: "en, ar"
---

# GM-16 · Source Intake v2027.1

> **Authority.** A **record** ([GM-01 §1.2](precedence-and-conflict-rules.md)). It sets out what the
> joined files contain, where they contradict each other and the held corpus, and which reading has
> been adopted. Decisions marked **ADOPTED** follow from a rule already in force. Decisions marked
> **PROPOSED** wait on the Curator.

> **Disclosure first.** The joined folder does **not** contain one v2027.1 release. It contains
> **two incompatible releases sharing one version number** (Families A and B below), plus a README
> (Family C) that describes a different repository. Taking "you'll find all answers" literally
> would have meant adopting contradictory answers. The contradictions are resolved by the
> precedence ladder against the held tier-1 text of ML-2.3, not by preference.

---

## 1. What arrived (27 files)

| Files | Status |
|---|---|
| 00_BCIA_* ×4, 00_CREDENTIALING_*, 00_METAX_COURSE_SERIES_REGISTRY, 00_METAX_SOURCE_INDEX, 00_PUBLIC_CANON_PATCH, 00_TOPTECH_CANONICAL_INDEX, AG-011 charter, MX-NAV-SPEC v2026.10.1, MX-SITE-DESIGN v2026.09.3, ML-2.0, Meta-Review, Page Spec, Platform Persistence, UI-UX, Deep review, THE_METAX_CORPUS | **Already held.** Byte sizes are identical, so nothing was re-ingested |
| ML-2.3_full_text.md | **Duplicate** of `sources/The_Maher_License_ML-2.3.md` (65,530 B). Not stored twice |
| hx-000-the-fourteen-structural-harms.md | Already held in `docs/harms/`. Now also retained in `sources/` |
| **BX-000_and_HX-000_v2027.1.md** · **ML-2.4_clauses.md** · **ML-2.4_requirements.md** · **ML-B-1.0_profile.md** | **New: Family A** |
| **METAX_CORPUS_SOURCE_BUNDLE_v2027.1.md** | **New: Family B** |
| **README.md (v2027.1)** | **New: Family C**, stored as `sources/README_v2027.1.md` |

**Family A** is internally consistent. It agrees with the held ML-2.3 §H.2.2 on the identity of
all 25 harms and on all 8 absolutes, and extends them to 28 harms, 7 strata and 9 absolutes.
**Family B** is built on an eighteen-harm "HX-000 v2026.09.5" that this corpus never held. It
assigns different harms to HX-15…HX-25 than ML-2.3 does, and describes an ML-2.4 and an ML-B-1.0
that share no clause with Family A's. **Family C** reports the state of another repository. Its
paths (e.g. `docs/metax/bcia/…`) and its identifiers (DEF-037, RAT-22, RAT-23, B-25) mean
different things here or do not exist here.

## 2. Decisions

| D | Decision | Basis | State |
|---|---|---|---|
| D-01 | **Harm identity follows ML-2.3 §H.2.2 and Family A.** [HX-000 v2027.1](../harms/hx-000-register-v2027-1.md): 28 harms, 7 strata, 9 absolutes. Family B's register is not adopted | ML-2.3 is tier 1, and §H.2.1/§E.9 say the licence governs. Family A needs no renumbering. Family B would reassign 11 identifiers already issued by the tier-1 text (ST-01 Rule 2) | ADOPTED |
| D-02 | Family B's new harms go to the **first unnamed-harm review** (ML-2.4 §H.34) as candidates | Adding a harm amends the register, which is the Curator's act (§E.4) | ADOPTED as record; admission PROPOSED (RAT-34) |
| D-03 | The corpus's own **HX-000 v2026.10.1 is superseded**. Its H1–H25 diverge from ML-2.3 on most identities. [CON-002](../harms/con-002-harm-numbering-concordance.md) maps them by subject | DEF-040, which GM-15 missed | ADOPTED |
| D-04 | **ML-2.3 is NOT recorded as signed.** Sources B and C say "SIGNED 2027-01-14" (ML-2.4: 2027-02-02) | Both dates are later than today (2026-09-30). The fingerprint is still `[FPR]`, and [REG-12 §2](../registries/reg-12-processors-keys-mirrors.md) holds no key. B-01 stays open | ADOPTED; DEF-042 |
| D-05 | **ML-2.2: skipped, never adopted.** RAT-14 answered | Curator-supplied decision (B §0.2, C). No ML-2.2 text was ever published, so no grant is lost | ADOPTED; ML-2.3 §E.3 amendment PROPOSED |
| D-06 | **ML-2.4 published as a pending draft** ([ml-2-4.md](../license/ml-2-4.md)) from Family A. Collisions are renumbered: new §H.31→**§H.34**, new §E.6→**§E.10**, new §E.7→**§E.11** | ML-2.3 already holds §H.31 (Interaction, including §H.31.3, the only Part H conflict rule), §E.6 (profiles) and §E.7 (registry continuity) | ADOPTED as draft; DEF-043 |
| D-07 | **Family B's ML-2.4** (Part J D1–D6, §H.30 welfare, §H.31 successor duty) is not adopted. It is kept as proposals DT-1…6, WR-1, SI-1 (§6) | Its §H.30 and §H.31 collide with ML-2.3. Its D1–D6 collide with HX-000 v2027.1 §12 D1–D6, which have different content. Same doc_id, different instrument | ADOPTED as record; DEF-045 |
| D-08 | **ML-B-1.0 published as a draft** ([ml-b-1-0.md](../license/ml-b-1-0.md)) from Family A. Family B's B.1–B.6 are kept as a conformance annex | Family A is the full instrument. Family B agrees with it in intent | ADOPTED as draft |
| D-09 | **The Register of Substrate Harms is written at BX-018**, with `source_designation: "BX-000 v1.0"` | "BX-000" now has **four** claimants: the reading model (held), Document Zero (BX-010), Family B's Document Zero v1.0, and Family A's substrate register. Rule 2 forbids a fifth reuse | ADOPTED; DEF-044; RAT-29 |
| D-10 | **Family B's Document Zero v1.0 is merged into BX-010 §9** | Same subject. It agrees clause by clause | ADOPTED |
| D-11 | **BCIA = Bio-Computational Intelligence Architecture, programme MLT-09.** RAT-28(a) answered in substance | Stated in source. The reading model (BX-000…009) needs another name; renaming is the Curator's act | ADOPTED as meaning; rename PROPOSED (RAT-29) |
| D-12 | **The nine MacroLifeTech programmes are published** ([MLT-000](../metax/programs/mlt-000-programme-register.md)), each with its declared status and its status under the charter rule | By the bundle's own rule, a programme without all seven charter parts "may not leave `planned`". None states a complete charter, yet seven declare `research-preview` | ADOPTED; DEF-049 |
| D-13 | **MX-NAV-SPEC v2027.1 adopted with one correction:** ML-2.3 is shown as the licence of record and ML-2.4 as a draft. The redirect `/license/ml-2-3/* → /license/falsification/ml-2-3/` is **refused** | As drafted, the spec presents an unratified text as "The Instrument (live)" and files the binding licence under "Falsification & History". That misrepresents what a licensee is bound by | ADOPTED; DEF-046 |
| D-14 | **MX-SITE-DESIGN v2027.1** is recorded with `conformance_state: unmet`. A static hero with no Owl is recommended | ≈118 KB of third-party JS against a 12 KB first-party budget (ST-21/ST-19). Autoplay conflicts with DS-02 and MX-023 | PROPOSED (RAT-35) |
| D-15 | **BHS-2027-001 (draft)** marks **HX-01 and HX-04 `unremedied`**, in addition to Family A §13's seven | Family A's estate statement omits the live ad slots (REG-12 P-02/P-03) | Draft; issuing is the Curator's act; DEF-047 |
| D-16 | **Source open-question numbers are re-keyed:** HX-000 v2027.1 RAT-17→**RAT-30**, RAT-18→**RAT-31**, RAT-19→**RAT-32**, RAT-20→**RAT-33**. Source RAT-16 matches GM-04 RAT-16 and is kept. RAT-B-01…06 form their own namespace | GM-04 already holds RAT-17…20 with other subjects | ADOPTED; DEF-048 |
| D-17 | Source defect strings **DEF-2026-055…079 and DEF-2027-001 are imported as issued.** Family C's numbers are not | No collision. Family C describes another repository | ADOPTED |

## 3. The eight review questions (Bundle Part 7 §1)

**Q1. Missing, ranked by citations.** The index-level gaps were closed in v2026.10.2. Still unwritten
after v2027.1: the **63 programme leaf pages**, **CF-1**, **CPF-1**, the **`license.json` machine
forms**, and the **premise register**. The most-cited item that cannot be written by an agent is
the **key fingerprint `[FPR]`**.

**Q2. The case against skipping ML-2.2.** ML-2.3 §E.3 grants ML-2.2 works transition rights, so
skipping 2.2 voids a tier-1 clause. *Reply, accepted:* nothing was ever licensed under an
unpublished text, so nothing is lost. §E.3 should still be amended (§4 F-01).

**Q3. Does Family B's renumbering breach ST-01?** **Yes, and more than it admits.** ST-01 allows a
family change with a concordance. It does not allow reassigning identifiers **already issued in the
target family**, and HX-15…HX-25 were issued by ML-2.3 §H.2.2. Under Family B's CON-001, "HX-20"
would mean *linguistic erasure* while the tier-1 licence says *synthetic agency without a
principal*. Family A needs no renumbering, and that settles it (D-01).

**Q4. A remaining defect that meets all five inclusion criteria.** Two:
- **Governance volume.** Family B's HX-17 is the same as this corpus's old H19 and the subject of DEF-035/039.
- **Uncalibrated attestation.** Family B's HX-19, against MX-025/REG-05 and DEF-038.

Both are filed as §H.34 review entries ([HX-000 v2027.1 §15](../harms/hx-000-register-v2027-1.md)) and are not added to the register.

**Q5. Is the carousel mitigation enough?** No. Self-hosting closes **provenance** and leaves
**weight**, about 118 KB against 12 KB. Rule 6 cannot be checked mechanically, and autoplay is an
attention mechanism (MX-023). The alternative is a static hero with a CSS-only fade, about 1 KB and
no autoplay (RAT-35).

**Q6. Weakest sunset.** **MLT-04 Soma**: "the field converges on a settled position the programme
has not contributed to". The programme judges its own contribution, and convergence has no
observable date. MLT-06 Athar has the same flaw. The strongest is **MLT-03 Metabolism**, which is
tied to external sector data.

**Q7. Enforcement claimed but not built.** Six cases. All of them are the [DEF-001](defect-register.md#def-001) pattern:
1. MX-READER-01 says "build fails if…". No build exists and the package is unpublished.
2. The B-profile conformance test with 11 checks is not built.
3. The "signed" chain and "a registry with three mirrors": REG-12 shows none.
4. CON-001 "the build emits a redirect for each". There is no build.
5. The nav spec's "build failure" rules have no build to fail.
6. "Unverified count printed in every release" sits next to `unverified_citations: null`.

**Q8. Three unstated premises.** These are *candidates* only. Founding the premise register is the Curator's act (RAT-36).
- **PR-C1.** A text governs once it is labelled `canonical`, before anyone has read it. Contradicted by `human_read`.
- **PR-C2.** A one-steward estate can hold due-process powers (HX-28; RAT-33).
- **PR-C3.** The religious mappings add warrant, yet both registers say their failure "would not vacate a single duty". If so, they are commentary, and should be labelled as commentary.

## 4. Refinements made or proposed

| F | Instrument | Refinement | State |
|---|---|---|---|
| F-01 | ML-2.3 §E.3 | Record "ML-2.2 never adopted". Propose deleting the ML-2.2 sentence in ML-2.4 | Note added; amendment PROPOSED |
| F-02 | HX-000 v2026.10.1 | Supersession banner pointing to v2027.1 and CON-002 | Done |
| F-03 | version-history | Chain 2.1 → [2.2 never adopted] → 2.3 → 2.4 draft → ML-B-1.0 draft | Done |
| F-04 | BX-010 | §9 from Family B Document Zero | Done |
| F-05 | LEX-05 | Contested terms CT-12…CT-18 | Done |
| F-06 | GM-13 §4 | High-water marks | Done |
| F-07 | ML-B-1.0 §B-E.3 vs MX-014 | §B-E.3 excludes only S4 and I3 from the estate. MX-014 and BX-011 exclude **all** cultivation and bench work. Read alone, §B-E.3 understates the estate's own limits | Annotated; RAT-37; DEF-052 |
| F-08 | Nav BCIA group "The Eight Series" | Branch D has **ten** books (S38–S47) | LEX-05 CT-17 |

## 5. Open items the new sources answer

| Item | Answer | State |
|---|---|---|
| RAT-14 | ML-2.2 skipped | **Answered** |
| RAT-28(a) | BCIA = MLT-09, the research programme | **Answered in substance**; rename open (RAT-29) |
| RAT-28(g) | Nine pillars on one origin. Academy subdomains run the reader | **Partly answered**: M-A + M-C |
| RAT-28(e) | "Programme" for the nine MLT units | **Partly answered** |
| RAT-15 | BHS-2027-001 must mark HX-01/HX-04 unremedied | Drafted |
| RAT-04 | "The ethics veto holder is unnamed" | Unchanged |
| RAT-05 | Book 9 is `[GAP IN SOURCE]` | Unchanged |
| B-01 | Future-dated "signature" claims | **Unchanged** |
| GM-15 C-10 | `human_read` and `conformance_state` are introduced | Used in all v2027.1 documents; ST-02 amendment PROPOSED |

## 6. Family B content kept as proposals

| Proposal | Content | Why not adopted as written |
|---|---|---|
| DT-1…DT-6 | Readable without the maintainer · stated horizon · successor instrument · wind-down cost · worst-future-holder assessment · premise register | Labelled D1–D6, which collides with HX-000 §12 D1–D6. Overlaps §H.28, §H.33 and §H.9 |
| WR-1 | Cognitive-system welfare and a Welfare Reviewer | Its §H.30 collides. The substrate case is covered by ML-B-1.0 |
| SI-1 | Successor-instrument duty | Its §H.31 collides. Covered by ML-2.4 §H.33(a) |
| Harm candidates | Declared standard unmet · disclosure as licence · governance volume · self-administered adjudication · uncalibrated attestation · externalised security debt · revocable possession · temporal compression · continuity default · premise ossification | The first §H.34 review ([HX-000 v2027.1 §15](../harms/hx-000-register-v2027-1.md)) |

## 7. Falsifier

This intake is wrong if the held `license/ml-2-3.md` §H.2.2 gives any HX identifier a different
harm than Family A does. That was checked for HX-01…25 on 2026-09-30. It is also wrong if a key
fingerprint for ML-2.3 exists anywhere in the estate.

---

**Related:** [GM-15](corpus-review-v2026.10.2.md) · [GM-13](identifier-reallocation-record.md) · [HX-000 v2027.1](../harms/hx-000-register-v2027-1.md) ·
[CON-002](../harms/con-002-harm-numbering-concordance.md) · [ML-2.3](../license/ml-2-3.md) · [ML-2.4](../license/ml-2-4.md) · [ML-B-1.0](../license/ml-b-1-0.md) ·
[BX-018](../bcia/bx-018-register-of-substrate-harms.md) · [MLT-000](../metax/programs/mlt-000-programme-register.md) · [Nav v2027.1](../site/mx-nav-spec-v2027-1.md) ·
[Defect Register](defect-register.md) · [Open Questions](open-questions-and-ratifications.md)
