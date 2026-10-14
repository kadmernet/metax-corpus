---
doc_id: "GM-17"
title_en: "Corpus Review v2027.1 — Missing Documents, Conflicts and Contradictions (Full Register)"
title_ar: "مراجعة المتن v2027.1 — الوثائق الناقصة والتعارضات والتناقضات"
family: "governance-map"
version: "v2027.1-review"
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
domain_tags: ["governance", "review", "missing-documents", "conflicts", "contradictions", "audit"]
route: "/library/record/reviews/v2027-1/"
supersedes: ["GM-15 as the current review (GM-15 retained; its items are carried forward here with status)"]
derived_from: "Directory listing of all docs/ families (230 files); direct reads of MX-000, MX-001, MX-014, MX-026, MX-029, GM-01, ML-2.3, scale-gate, enforceability table, part-h-statement, HX-000 (both), HX-001, HX-002, AG-000, AG-015, AG-021, REG-01, REG-09, ST-01, ST-02, SITE-01, and all v2027.1 sources; front-matter status grep across docs/"
provenance_of_purpose: "record"
human_read: "none"
conformance_state: "partial"
authorship_note: "Written by the AI system that drafted ~110 of the files reviewed. This is a self-review and carries the blind spot that let GM-15 miss DEF-040. Every finding cites a file and, where verified, a line. Text search returned false negatives repeatedly on large files (e.g. 'refus' in THE_METAX_CORPUS.md, which does contain it), so no 'absent' finding rests on search alone."
hreflang: "en, ar"
---

# GM-17 · Corpus Review v2027.1: Missing Documents, Conflicts and Contradictions

> **Authority.** A **record**. It governs nothing ([GM-01 §1.2](precedence-and-conflict-rules.md)).
> Every item has an id, evidence, a severity, a proposed resolution, an owner and a state.
> **No canonical text was changed on the strength of this review.**

> **Disclosure first.** Four findings in this review contradict things this reviewer wrote earlier
> in the same programme. They are listed in §4.10 and not softened.

---

## 0. Scope, method, scales

**Scope.** All of `docs/`, about **230 files in 17 families**, as listed on 2026-09-30, plus the 27
source files. Front-matter `status` was read for every file:

| `status` value | Files (approx.) | Permitted by ST-02? |
|---|---:|---|
| `canonical` | ~109 | yes |
| `published` | ~49 | **no** |
| `pointer` | 46 | **no** (stubs; proposed in GM-15 F-04) |
| `draft` | ~21 | yes |
| `canonical · ratification pending` | 3 | **no** |
| `superseded` / `withdrawn` | 1 / 1 | yes |

**Method.**
- **L-2 form audit:** listings against the index, GM-13 and the document index.
- **Targeted reads** of every instrument on tiers 1–3 and every file that names harms.
- **Cross-reading** of every v2027.1 source against the held ML-2.3.

**Severity.**
- **S1:** misleads a reader about a governing matter, an absolute, or what binds them.
- **S2:** a contradiction between instruments that a careful reader would hit.
- **S3:** staleness, form, or count.

**Owner.** **C** Curator · **A** agent (with approval) · **B** build or tooling · **X** external party.

**Agent-writable?** **Y** an agent can draft it now · **N** needs a fact or decision only the Curator or a third party holds · **P** an agent can draft a scaffold, but it is not valid until a human acts.

---

## 1. Summary

| Class | S1 | S2 | S3 | Total |
|---|---:|---:|---:|---:|
| **Missing documents** (§2) | 9 | 33 | 14 | **56** |
| **Conflicts and contradictions** (§3–§4) | 14 | 27 | 13 | **54** |
| **Adjustments owed** (§5, consolidated) | — | — | — | **28** |

**The five things that matter most.**
1. **Nothing is signed.** Every instrument derives its authority from ML-2.3, and ML-2.3 has no signature, no key and no mirrors. The sources' "SIGNED 2027-01-14" is future-dated (X-01).
2. **The harm layer has four incompatible vocabularies.** These are ML-2.3 §H.2.2 (operative), HX-000 v2026.10.1 H1–H25, HX-002's own labels, and Family B's register. At least **six governing instruments** cite HX numbers with the wrong meaning (X-10…X-15).
3. **The Charter and MX-014 disagree about what the refusals are** (X-20). These are the corpus's most protected provisions.
4. **ST-02's own enums are violated by roughly half the corpus**, including every file this programme wrote (X-30…X-34). The front-matter contract the machine-reading thesis rests on does not hold.
5. **The most-cited missing artefacts cannot be written by an agent.** They are a key, a signature, an ethics reviewer, a successor's acceptance, a dissent receiver, a Welfare Reviewer, counsel review, and Arabic text (§2.1).

---

## 2. Missing documents and artefacts

### 2.1 Cannot be written by an agent: blockers on authority (S1 unless noted)

| M | Missing | Cited by (examples) | Why it matters | Owner | Agent? |
|---|---|---|---|---|---|
| M-01 | **Signing key, fingerprint `[FPR]`, signed ML-2.3** | ML-2.3 front matter; B-01; REG-12 §2; ST-30; Bundle §4.1 | Every authority claim downstream is "pending" (MX-000 Status block) | C | N |
| M-02 | **Registry and three mirrors (M1–M3)** | ML-2.3 §E.7; ML-OPS-1; REG-12 §3; B-02 | ML-2.3's continuity rule ("the most recent digest-verified mirror is canonical") has no referent | C | N |
| M-03 | **Named ethics-veto holder** | MX-000 §0.5.1; MX-014 §7; BX-010 C3; MX-029 group 5; B-03; RAT-04 | The only power placed beyond the Curator has no holder. All BCIA research is blocked | C | N |
| M-04 | **Executed succession instrument with written acceptance** | MX-015; ML-OPS-2; ML-2.4 §H.33(a); AG-022; HX-28 | HX-28 is the estate's own admitted harm | C + successor | P (form exists) |
| M-05 | **Dissent channel outside the steward** | ML-2.4 §H.33(c); ML-B-1.0 §B-E.4; BX-018 §7.7; DEF-053 | Required "at first issue" by ML-B-1.0 | C + X | N |
| M-06 | **Counsel review** of ML-2.3 (and of 2.4 and B-1.0) | ML-2.3 Publication Note 1; RAT-18; enforceability table | `counsel_reviewed: false` on every licence | X | N |
| M-07 | **Scale Gate thresholds as the Curator's ratified figures** (S2) | scale-gate.md §2 says "unpublished"; V-09 | **Contradicted by ML-2.3 §H.2-bis.1**, which states figures (X-05) | C | N |
| M-08 | **Welfare Reviewer** (substrate) and **Cloister/Atrium members** (S2) | BX-018 §1; ML-B-1.0 §B-C.2; BX-010 §9; RAT-38 | Dormant until a G2 holding exists, but the Cloister quorum of 3 is impossible today | C | N |
| M-09 | **Arabic editions of all instruments** | DEF-002; MX-020; RAT-09; RAT-22; every `title_ar` marked [AR-DRAFT] | Several files declare `prevailing_text: ar` while having no Arabic text (X-35) | C / human translator | N |
| M-10 | **Premise register: the first seven premises** | HX-25/UH-10; Family B DT-6; Bundle closing note; RAT-36 | "The one deliverable the agent genuinely cannot produce" (Bundle). Three candidates exist at GM-16 Q8 | C | P |
| M-11 | **Issued Part H Statement** (BHS-2027-001) with a named natural person | part-h-statement §5.4; ML-2.3 §H.16.4; RAT-15 | The draft exists. Issuing it, and the ad decision, are the Curator's | C | P (drafted) |

### 2.2 Instruments and records cited but not written (agent-writable, S2)

| M | Missing | Cited by | Notes | Agent? |
|---|---|---|---|---|
| M-12 | **MLT-01…MLT-09 individual charter files** (9) | MLT-000; nav v2027.1 `/metax/programs/{slug}/` | The register summarises each. Full charters (≥1,400 words each per Bundle §2 Wave 2) are not written. MLT-04 has 3 of 7 parts | Y |
| M-13 | **63 programme leaf pages** (7 per programme) | SITE-06 §3; MLT-000 §4 | `charter`, `questions`, `method`, `exclusions`, `status`, `outputs`, `contribute`. **Must not be emitted thin** (ST-13 "never emit an unwritten page") | Y (slow) |
| M-14 | **Seven stratum pages** `/license/harms/stratum-i…vii/` | SITE-06 §2 | Should derive from HX-000 v2027.1 | Y |
| M-15 | **CF-1 Compliance File template** and **ML-B-1.0 Schedule B-1** | Bundle §4.4; ML-B-1.0 §B-C.3; SITE-06 §2 | The inverted grant turns on this record. Without it no grant can exist | Y |
| M-16 | **CPF-1 Comment-Period Publication Format** | ML-2.4 §2 Track 2; Bundle §4.4 | Needed before 2027-04-01 | Y |
| M-17 | **Machine forms:** `ml-2-3/license.json`, `ml-2-4/license.json`, `hx-000.json`, `bx-000.json`, `ml-2-3.txt` | ML-2.3 front matter; HX-000 §14; SITE-06 | Source DEF-2026-073: no `role` discriminator. ST-14 says "none exists yet" | Y |
| M-18 | **Decay Calendar** (recomputed with the corrected rule) | HX-000 v2027.1 §9; BX-018 §9; DEF-051 | The per-entry verify dates in both registers follow no single rule | Y |
| M-19 | **Migration Ledger ML-001** (digests per release) | ML-2.4 §H.28 am.; Bundle §4.2 | Cannot hold digests until there is a release (M-01) | P |
| M-20 | **Decision record** for each amendment | ML-2.4 §7 and §H.33(b) | ML-2.4 §7 is the only one | Y |
| M-21 | **Corrections Log entry C-17** (BX-000 "first BCIA document" claim) | GM-15 C-12 promised it | **Promised and never written** (X-61) | Y |
| M-22 | **Anomaly Register** | AG-015 kernel "Log such text in the Anomaly Register"; Bundle Part 7 §5(5) | Instruction-like text in sources (e.g. the Bundle's Part 7 prompt) has never been logged | Y |
| M-23 | **Continuity Register** | MX-015; Meta-Review `/about/continuity-register/` | Every dependency on the Curator as a dated defect | Y (from DEF-031, HX-28) |
| M-24 | **Determination / Decision Queue specification** | MX-001 §1.2 (links to a pointer stub, page-spec-hub); UI-UX source §12; LEX-05 CT-08 | MX-001 calls it "the one that costs something" and it does not exist | Y |
| M-25 | **Pre-registration desk** `/method/instruments/prereg/` | MX-014 §4, §7 | "Does not exist" (MX-014 line 218) | Y (form) |
| M-26 | **Human calibration specimen set (≥12)** | MX-025; RB-07; DEF-038 | Assessor calibration is impossible without it | P |
| M-27 | **Canonical bibliography (human-verified)** | AG-017 Disclosure; DEF-2026-056; V-20 | Must be human-compiled | N / P |
| M-28 | **Canonical inventory of Volume I** (Gate 1) and the **"English glossary"** (Gate 3) | BX-012; BX-014; RAT-28(b) | The glossary may never have existed | P |
| M-29 | **Book ingestion:** Book 7 ch. 3–12, Books 8 and 10 full, **Book 9 ch. 2–9 (`[GAP IN SOURCE]`)** | BX-012; BX-013; RAT-05 | Book 9 needs the Curator to supply it | N (Book 9) / Y (others, if supplied) |
| M-30 | **ML-2.0, ML-1.1, ML-1.0 retained texts** in `docs/license/` | Meta-Review D.1.1 `/license/ml-2-0/`, `/license/ml-1-1/`; version-history | ML-2.0 is held in `sources/`. ML-1.x texts are **held nowhere** | Y (2.0) / N (1.x) |
| M-31 | **Lexicon term entries** (`t-{root}-NN`) and the **sibling term sets** (harms, records, site) | Meta-Review R5; LEX-03 line 49 "Sibling sets (not yet written)" | Zero entries exist under the prescribed grammar | Y |
| M-32 | **SENTINEL / static build**, **link checker**, **front-matter validator** | ST-13; DEF-001; V-10; GM-15 F-02/F-03 | DEF-001 is the upstream cause of DEF-040, DEF-043 and the §4 schema violations | B |
| M-33 | **MX-READER-01 implementation** (`@metax/series-reader`) | SITE-07 Part 2 | It is specified to fail builds that do not exist | B |
| M-34 | **Generated surfaces:** `status.json`, `catalog.json`, `search-index.json`, `sitemap.xml`, `/.well-known/security.txt` | SITE-01 §9; MX-NAV-SPEC; MX-011 | All "generated at build", and there is no build | B |
| M-35 | **Course texts S01–S52** (and F1, F2) | REG-01; REG-09; AG-021 | "`live` means *specified*, not *written*" | Y (slow; AG-021 recipe) |
| M-36 | **Site pages:** 321 (SITE-01) or ≈430 (SITE-06) English routes, plus the Arabic mirror | SITE-01 §4; SITE-06 §5 | None generated | Y (slow) |
| M-37 | **The three lost page-spec texts** (TopTech, Hub, Academy subdomains) | MX-000 §0.2 links page-spec-toptech; MX-001 links page-spec-hub | Pointers only. Two governing instruments link to a pointer for substantive content | N (unretrievable) |
| M-38 | **Companion volumes** *Repairing the Machine* v2 (BOOK-RSM-01) and *Repairing the Life* (BOOK-RSL-00) | HX-000 v2027.1 numbering law; BX-018 §4 | "Chapter = harm" depends on books the estate does not hold | N |
| M-39 | **Defect register entries for the 4 legacy items GM-15 called A-items** | — | Tracked only in GM-15 and here | Y |
| M-40 | **Programme-series registry** (`MLT-NN-SNN`) | MLT-000 §1 grammar; MLT-01 "S01…S04 planned" | No register exists for programme series | Y |

### 2.3 Text owed inside existing files (S3)

| M | Owed | File |
|---|---|---|
| M-41 | §6.6 "banned comparisons", cited by MX-000 §0.4.3 as "MX-006 §6.6" | MX-026 has no §6.6 heading for the DishBrain rule (it is in BX-010 §9) |
| M-42 | `#04-the-three-refusals` anchor | MX-014 line 60 links to it, but MX-000 §0.4 is titled "What MetaX refuses" |
| M-43 | Anchor `#143-the-ethics-veto` in MX-014 | MX-000 line 200 links to it, but the held MX-014 has no §14.3 (that numbering is the source's) |
| M-44 | A `last-production date` at the root (W7) | HX-000 v2026.10.1 H25; AG-012 §5.2 |
| M-45 | `(not yet written)` marks on related-block links | AG-003 §5.1, O5. Still owed corpus-wide |
| M-46 | ST-01 prefix rows: LEX, MLT, CON, BHS, CF, CPF, ML-OPS, UH, RAT-B, PR | LEX-04 X-5; GM-16 |
| M-47 | ST-02 enum values: `pointer`, `volatile`, `standard`, `guidance`, `procedural`, `metax`, `templates`, plus fields `human_read` and `conformance_state` | §3.4 below |
| M-48 | Registers for **RAT-B-01…06** with full text (only a table row exists) | GM-04 |
| M-49 | A full eight-part body for each of the 28 harms **inside** `docs/` (the text currently lives only in `sources/`) | HX-000 v2027.1 §6 incorporates the source by reference, which means the governing text is not in the governed tree |
| M-50…M-56 | Pointer stubs still owed at seven cited legacy paths for the **v2027.1 names**: `harms/hx-000-the-twenty-five-structural-harms.md`, `metax/bcia/bx-000-document-zero.md`, `site/mx-reader-01-course-series-reader.md`, `site/mx-site-design-v2027-1.md` (exists), `site/mx-nav-spec-v2027-1.md` (exists), `license/ml-b-1-0.md` (exists), `metax/programs/mlt-000-the-programme-register.md` | README_v2027.1 (Family C) links four of these. If that README is ever adopted, they dangle |

---

## 3. Conflicts and contradictions: governing layer

### 3.1 The licence chain and precedence

| X | Sev | Contradiction | Evidence | Resolution proposed | Owner | State |
|---|---|---|---|---|---|---|
| **X-01** | S1 | "ML-2.3 SIGNED 2027-01-14" / "ML-2.4 SIGNED 2027-02-02" against unsigned text and `[FPR]` | Bundle §4.1–4.2; README_v2027.1 l.50; ML-2.3 front matter has no signature field; REG-12 §2 empty | Do not record. B-01 stays open | C | Recorded (DEF-042) |
| **X-02** | S1 | **The Charter derives its authority from ML-2.1**, while GM-01 puts ML-2.3 at tier 1 | MX-000 l.14 `license: ML-2.1`, l.26, l.31, l.153, l.214, l.292; GM-01 l.34 | Re-base MX-000 to ML-2.3 (GM-15 A-03) | C | **Open** |
| **X-03** | S1 | **Two reading laws.** HX-000 v2027.1 §0 says the register governs every derived document. ML-2.3 §E.9 and §H.2.1 say the licence governs the register | sources HX-000 §0; ML-2.3 l.255, l.342 | Split by role: the licence governs identity and absolutes, the register governs content (adopted in HX-000 v2027.1 header). Needs the Curator to ratify | C | Provisional |
| **X-04** | S2 | **Precedence tie-breaks differ.** ML-B-1.0 §B-A.3: the more protective reading prevails. BX-018 §7.6: HX governs shared apparatus. GM-01 §1: the higher tier governs | ML-B-1.0; BX-018; GM-01 | Adopt "more protective prevails" for substrate matter, and add it to GM-01 as a domain rule | C | Open |
| **X-05** | S2 | **Scale Gate thresholds: published or not?** ML-2.3 §H.2-bis.1 states 1,000 / 100,000 / USD 1,000,000 / 25 people / 1,000,000 and CPI indexing. scale-gate.md §2 says the thresholds are `[VERIFY]` and "unpublished". V-09 says the same. HX-000 v2027.1 §3 gives a third, simplified version | ML-2.3 l.408–417; scale-gate.md l.72–87; V-09 | The tier-1 text wins. **scale-gate.md and V-09 are wrong.** Close V-09 as "corrected" and amend the worksheet | A | **Open** |
| **X-06** | S2 | **Source DEF-2026-074** ("revenue threshold stated without a currency or index") is false against the held ML-2.3 §H.2-bis.3 (USD, CPI) | Bundle §4.2; ML-2.3 l.417 | Mark it as a Family B defect against a different text. Not a defect of this corpus | A | Open |
| **X-07** | S2 | ML-2.3 §F.4.4 says "**Eight** things terminate the grant", while §F.4.2 lists the eight absolutes **plus** §C.5, §C.9 and §B.5(b), making eleven conditions | ML-2.3 l.272–295 | A non-operative note in ML-2.4. Do not edit ML-2.3 in place | C | Open |
| **X-08** | S2 | ML-2.3 §E.3 grants transition rights to ML-2.2 works, but ML-2.2 was never adopted | ML-2.3 l.234; RAT-14 answered | ML-2.4 §E.3-bis (proposed) | C | Proposed |
| **X-09** | S2 | **ML-2.4 drafted against a remembered base.** It "adds" §H.31, §E.6 and §E.7, which ML-2.3 already holds | sources/ML-2.4_clauses.md §1.3; ML-2.3 l.243, l.246, l.629 | Renumbered to §H.34, §E.10, §E.11 (B-25) | C | Pending confirmation |

### 3.2 Harm identity: four vocabularies

| X | Sev | Contradiction | Evidence | Resolution | Owner | State |
|---|---|---|---|---|---|---|
| **X-10** | S1 | **HX-000 v2026.10.1 H1–H25 do not match ML-2.3 §H.2.2.** Only H1, H10, H11 and H15 correspond | docs/harms/hx-000-structural-harms.md headings vs ML-2.3 l.346–399 | Banner and CON-002 (done) | — | Mitigated (DEF-040) |
| **X-11** | S1 | **HX-002 uses a third vocabulary.** HX-02 "Epistemic dependency", HX-03 "Engineered compulsion", HX-05 "Asymmetry of the record", HX-06 "Erosion of the deliberative commons", HX-07 "Access foreclosure", HX-08 "Intermediation rent", HX-09 "Labour displacement", HX-13 "Concentration of capability", HX-16 "Metric capture", HX-17 "The audit that certifies itself", HX-18 "Consent integrity", HX-19 "Authorship of record", HX-20 "Inheritance of unauditable systems", HX-21 "Foreclosure of the successor's options", HX-22 "Loss of transmissible skill", HX-24 "Irreversible commitment", HX-25 "Silence in the record" | hx-002 l.67–69, 100–102, 127–130, 191–197, 235–242 | **HX-002 must be re-keyed to ML-2.3 names.** Its MetaX-state findings (FAILS/partial) stay valid as evidence about the estate. Until then, add a banner | A | **Open (new: DEF-054 proposed)** |
| **X-12** | S1 | The part-h-statement §5.1 table uses HX-02 "epistemic dependency", HX-10 "material and infrastructural cost", HX-12 "harm to the record", **HX-18 "consent integrity"** | part-h-statement l.173–180 | Noted in §5.4 (done). The table is kept | — | Mitigated |
| **X-13** | S2 | **AG-000 §1** cites HX-19 as "authorship of record" and HX-25 as "agent constraint". Under ML-2.3, HX-19 is ethical enclosure, HX-25 is erosion of exit, agent constraint is §H.25/HX-20, and authorship of record is §H.19/HX-14 | ag-000 l.47 | Correct to "**§H.19** (authorship of record) and **§H.25 / HX-20**". The text confuses duty numbers with harm numbers | A | **Open** |
| **X-14** | S2 | **MX-014 §1** cites "HX-24 (developmental default)" and "HX-21 (foreclosure of the successor's options)". Under ML-2.3, §H.24 is developmental default and **HX-22** is pre-emption of the successor | mx-014 l.47–48 | Correct to "§H.24" and "HX-22" (GM-16 D-123) | A | **Open** |
| **X-15** | S2 | The **archive register** cites "HX-25 (silence in the record)" and "HX-20 (inheritance of unauditable systems)", which are HX-002's vocabulary | archive-register l.59–60 | Re-key it to HX-12 (digital amnesia) and HX-22/HX-23 | A | **Open** |
| **X-16** | S1 | **Family B register** reassigns HX-15…HX-25 (e.g. HX-20 = linguistic erasure) | Bundle §3.3 | Not adopted. Candidates listed in UH-01…11 | — | Resolved (D-01) |
| **X-17** | S2 | **The enforceability table §6** maps duties by § number correctly, but titles "§H.2 The twenty-five harms" | enforceability l.145 | ML-2.4 removes the count | A | Open |
| **X-18** | S3 | HX-001 and HX-002 are `authority: governing` on tier 1a, yet HX-002 calls rows "register text pending" against a register that now exists | hx-002 l.36–39 | Update the caveat after re-keying | A | Open |
| **X-19** | S2 | **The stratum count.** ML-2.3: 6 strata, 25 harms, 8 absolutes. HX-000 v2027.1 / ML-2.4: 7, 28, 9. Family B: 6, 25, 8 with different members | as cited | ML-2.3 governs until ML-2.4 is ratified (HX-000 v2027.1 §0.2) | — | Recorded |

### 3.3 Charter, refusals and absolutes

| X | Sev | Contradiction | Evidence | Resolution | Owner | State |
|---|---|---|---|---|---|---|
| **X-20** | S1 | **What the refusals are.** MX-014 §2 says MX-000 §0.4's *three refusals* are (1) lab instruction in biology, (2) Core Riba, (3) sexualisation of minors. **MX-000 §0.4 lists four refusals:** (1) attention-economic mechanics, (2) Core Riba, (3) claims beyond evidence, (4) dark patterns. The human-cell exclusion is in §0.4.3 and §0.7. Sexualisation of minors is **not in §0.4 at all** (it is in MX-029 group 10 and AG-015 refusal 5) | mx-014 l.58–70; mx-000 l.133–180 | **The Charter governs (tier 2).** Either MX-014 §2 is re-written to quote §0.4, or §0.4 is amended under §0.8 to add the minors refusal and the lab-instruction refusal. The second is a Charter amendment and must be published before it takes effect | **C** | **Open (new)** |
| **X-21** | S2 | "Three refusals" also appears in GM-15, in LEX-05 CT-10 ("Charter §0.4: three refusals") and in the Meta-Review sitemap `/charter/refusals/` ("the three absolute refusals") | LEX-05; Meta-Review D.1.1 | Follows X-20 | A | Open |
| **X-22** | S3 | MX-000 §0.5 says "**Four** powers are placed beyond Maher's reach" and then has **five** sub-sections (§0.5.4 and §0.5.5 were added in v2026.09.2). §0.8 rule 5 refers to "§0.5.1–§0.5.5" | mx-000 l.186–238, l.312 | Correct the count, or compute it | A | Open |
| **X-23** | S2 | **Three expansions of BCIA.** MX-000 §0.2: "*Biological Computing and Intelligence Architecture*". Bundle/MLT-09: "*Bio-Computational Intelligence Architecture*". BX-000…009: "*Before · Contact · Internalisation · After*" | mx-000 l.94; Bundle §5.2 MLT-09; bx-000 l.54 | Adopt the Bundle form (D-11) and correct MX-000 §0.2 | C | **Open** |
| **X-24** | S2 | MX-000 §0.4.3 cites "MX-006 §6.6 banned comparisons". MX-006 is now *Contact*, and MX-026 has no §6.6 for banned comparisons | mx-000 l.168; GM-13 | Re-point to MX-026 and add the §6.6 section there (M-41), or point to BX-010 §9 | A | Open |
| **X-25** | S2 | MX-000 §0.4.3 and §0.7 link the human-cell exclusion to `bx-002-human-cell-exclusion.md`, which is now a pointer. MX-014 l.270 does the same | mx-000 l.169, l.295 | A-01 (GM-15): re-point to BX-011 | A | Open (mitigated by stub) |
| **X-26** | S1 | **ML-B-1.0 §B-E.3** limits the estate only for S4 and I3. **MX-014 / BX-011** exclude all wet-lab, cultivation and bench work. Read alone, the profile would let the estate's programme reach S1–S3 | ml-b-1-0 §B-E.3; mx-014 §3; bx-011 §1 | MX-014 prevails, annotated (DEF-052, RAT-37) | C | Annotated |
| **X-27** | S2 | **The ethics veto has two forms.** MX-000 §0.5.1 limits it to "**bio-adjacent** material". Source MX-014 §14.3 extends it to "**any** publication" on grounds of exclusions, harm, misrepresentation or Charter §0.4 | mx-000 l.192; sources THE_METAX_CORPUS §14.3; BX-010 §3 | Ratify one scope. BX-010 follows the source | C | Open |

### 3.4 Front-matter schema (ST-02) against practice

| X | Sev | Contradiction | Evidence | Resolution | Owner |
|---|---|---|---|---|---|
| **X-30** | S2 | `status` enum = canonical · draft · superseded · withdrawn. In use: `published` (~49), `pointer` (46), `canonical · ratification pending` (3) | ST-02 l.65; §0 table | Add `pointer` and `ratification-pending`, and map `published`→`canonical` in one sweep (GM-15 F-04) | C then A |
| **X-31** | S2 | `authority` enum = governing · operative-form · companion · record. In use: `standard`, `guidance`, `procedural`, `governing on ratification only`, `governing within MLT-09`, `governing for substrate class…` | ST-02 l.66; ML-2.4, ML-B-1.0, BX-017, LEX-04, SITE-05/06/07, task-ledger | Add `standard`, `guidance`, `procedural` and a separate `in_force` boolean | C |
| **X-32** | S2 | `evidence_class` enum = durable · semi-durable · perishable. In use: **`volatile`** (BX-012, BX-015, BX-018, REG-12, LEX-05, and others) | ST-02 l.70 | Replace `volatile` with `perishable` | A |
| **X-33** | S2 | **`review_interval_months` must match the class** (12/6/3). Violations include HX-000 v2027.1 (semi-durable/12), HX-000 v2026.10.1 (semi-durable/12), MX-000 (durable/36), BX-011 (durable/24), BX-016 (durable/24), CON-002 (durable/24), BX-018 (volatile/12). Separately, **MX-026 states 36/12/3** | ST-02 l.71, l.87–89; R-57; RAT-26 | RAT-26 decides the set, then one sweep | C |
| **X-34** | S2 | `depth` int 1–5 vs strings `macro`/`meta`/`micro` (BX-000…009, HX-000 v2026.10.1). `version` `vYYYY.MM.n` vs `v2027.1`, `v1.0`, `v2027.1-draft`, `v2027.1-intake`, `v2027.1-review`. `family` enum lacks `metax` and `templates`. Fields `human_read`, `conformance_state`, `source_designation`, `flagged_tier34` are not in ST-02 | ST-02 l.63–69 | Amend ST-02 under ST-15 to add the v2027.1 fields, then sweep | C then A |
| **X-35** | S2 | `prevailing_text: ar` on files with **no Arabic text**: BX-000, HX-000 v2026.10.1, REG-01, REG-03, REG-05, MX-002/003 (F5/F6) | front matter; reg-01 l.206 | Set `en` until an Arabic text exists, **or** keep `ar` and mark the instrument non-operative. The current state names a prevailing text that does not exist | C |
| **X-36** | S3 | Pointer stubs carry 3 fields, not 18. ST-02 says "a missing required field is a build failure" | 46 stubs | ST-32 T6 says a stub "has no identifier". Exempt `status: pointer` from ST-02 explicitly | C |

---

## 4. Conflicts and contradictions: structure, counts, process

### 4.1 Identifiers and numbering

| X | Sev | Contradiction | Evidence | Resolution | State |
|---|---|---|---|---|---|
| **X-40** | S2 | **RAT-24 means five things.** GM-04 has the "exemption field". scale-gate.md l.75 and l.296 use it for the *Scale Gate thresholds*. REG-03 l.212 uses it for the *state vocabulary ("blocked")*. REG-05 l.241 uses it for the *credential-face identity limit*. MX-004 l.160 and REG-02 l.217 use it for the exemption field | grep results; GM-04 l.57 | Letter it RAT-24(a)…(d) as was done for RAT-27, and keep every citation (Rule 2) | **Open (new)** |
| **X-41** | S2 | **Stale "next free" numbers taken as plans.** AG-006 l.124–126 and AG-008 l.206 list B-21, R-57, RAT-24, C-17 and V-14 as reserved next numbers. R-57, RAT-24 and V-14 were later issued with other subjects. B-21…24 and C-17 were never issued | as cited | Record them in GM-13 §4a (done for B). Add C-17 | Partly done |
| **X-42** | S2 | **BX-000 has four claimants** | GM-13 §4a | RAT-29 | Open |
| **X-43** | S2 | **Defect strings collide across source families.** Family A: DEF-2026-072/073 = decay arithmetic. Family B: DEF-2026-072 = schedule misnumbering, -073 = `license.json` role discriminator. Family B -076 has no Family A counterpart | ML-2.4_requirements §4; Bundle §4.2 | Import Family A's meaning (it travels with the adopted ML-2.4). Re-key Family B's as `DEF-B-072…079` in a namespace annex | **Open (new)** |
| **X-44** | S3 | **CON-001** (Family B) is reserved and unissued, while the nav spec (Family B) links `/license/harms/concordance/` as CON-001 | SITE-06 §2 uses CON-002 | Recorded | Resolved |
| **X-45** | S3 | The series identifier width is **S01 vs S001 vs S014 (reader example)** | REG-01; Meta-Review R1; SITE-07 | RAT-27(b) | Open |
| **X-46** | S3 | **Two "S" namespaces:** TopTech S01…S52 and MLT-NN-SNN | MLT-000 §1 | Always write the MLT prefix (CT-15) | Recorded |
| **X-47** | S3 | **"Gate" means three things:** Substrate Gate G0–GX, the 7 remediation gates, and Scale Gate tiers. **"D1–D…" means four things** | LEX-05 CT-14, CT-16 | Qualify every use | Recorded |
| **X-48** | S3 | The LEX-04 §3 high-water column (MX-029, BX-017, GM-15, DEF-039, RAT-28, R-60, V-17) is stale. GM-13 §4a governs | LEX-04 | Point it to GM-13 §4a | Open |

### 4.2 Estate model, routes and properties

| X | Sev | Contradiction | Evidence | Resolution | State |
|---|---|---|---|---|---|
| **X-50** | S1 | **One origin or subdomains?** SITE-01, SITE-06 and index §10 say one origin with directory routes, and C-04/C-15 say the subdomain grammar "does not exist". **MX-000 §0.6** and **MX-001 §1.1** still define *seven content-plane properties* including `toptech.`, `bcia.`, `academies.`, `library.`, `lexicon.`, `verify.` | mx-000 l.264; mx-001 l.41–51; route-manifest §1; index §10 | MX-000/MX-001 are tier 3 and SITE-01 is tier 7, so **on the ladder the subdomains win**, which is the opposite of what the corpus has decided. RAT-28(g) needs a ruling, and then MX-000 §0.6 and MX-001 §1.1 are amended | **C** · Open |
| **X-51** | S2 | **"Pillar".** MX-000 §0.2 and MX-001 §1.3 have *three pillars* (Meta-X, Transition, Higher-Order/BCIA, which is the **BCIA book taxonomy**). SITE-01, SITE-06 and DS-07 have *nine pillars* (nav keys). MX-014 §1 has "nine programs". DS-00 has eight menu keys | mx-000 l.65–107; route-manifest §1.4 | Pillar = the three *standing classes*. Nav key = the nine. Programme = MLT-01…09 (CT-02) | Open |
| **X-52** | S2 | **MX-000's three pillars reuse BCIA's internal layer names** (Meta-X / Transition / Higher-Order) for the whole estate. BX-013 shows those are layers *of the BCIA books* | mx-000 l.71–92; BX-013 §2 | Either the Charter adopted the book taxonomy deliberately (say so) or it is a category error. Curator to rule | C · **Open (new)** |
| **X-53** | S2 | BX-000…009 routes `/bcia/…` are not in SITE-01 or SITE-06 | bx-000 front matter | Move under `/metax/bcia/reading-model/` after RAT-29 | Open |
| **X-54** | S2 | **Nav v2027.1 labels** "The Instrument (ML-2.4) · live" and redirects ML-2.3 to Falsification | Bundle §2.2, §2.6 | Corrected in SITE-06 | Resolved (DEF-046) |
| **X-55** | S2 | **The carousel requires about 118 KB of third-party JS** against ST-21/ST-19's 12 KB first-party budget. Its source "amends ST-21" from a lower tier | SITE-07 | RAT-35 | Open |
| **X-56** | S3 | **Route census:** 321 (SITE-01) vs 428 (Bundle) vs ≈430 (SITE-06). File headroom 18,000 vs ≈17,600. "≈2,000 files" vs "≈2,400" | SITE-01 §4; SITE-06 §5 | Compute it once the build exists | Open |

### 4.3 Counts typed into prose (Rule 6 violations)

| X | Sev | Statement | Where | Conflicting figure |
|---|---|---|---|---|
| X-60 | S3 | "forty-seven series" | HX-002 l.202; MX-NAV-SPEC §5.4 | REG-09: 52-row canon, 48 live. AG-021: "S01–S50". Meta-Review: "S001–S050 current canon" |
| X-61 | S3 | "Sixteen corrections" | HX-002 l.114 | Corrections Log stops at C-16, **but GM-15 promised C-17 (never written)** |
| X-62 | S3 | "Thirty-four defects …" footer | defect-register | There are now 53 numbered entries plus 3 year-form entries plus imported source defects |
| X-63 | S3 | "Six instruments carry `authority: record`" | GM-01 §1.2 | 20+ |
| X-64 | S3 | "roughly seventy paths do not resolve" | index §2; document-index §6 | Obsolete per document-index §10. No count exists |
| X-65 | S3 | "Thirteen open" / "Seventeen open" | verification-log body | 21 open (V-01…V-21) |
| X-66 | S3 | "Fifty-six source conflicts" | index §2 | R-01…R-67 |

### 4.4 BCIA

| X | Sev | Contradiction | Evidence | Resolution | State |
|---|---|---|---|---|---|
| X-70 | S2 | **The seven gates have no owners or dates**, while source MX-014 §14.4 says they are "published with owners and dates" | BX-012 Disclosure | Curator to assign | Open |
| X-71 | S2 | **"Seven defects" vs "seven gates"**: the "exclusion missing from one version of Volume I" has no gate (proposed gate 1a) | BX-012 §1 | RAT-28(i) | Open |
| X-72 | S3 | The source taxonomy report lists **Book 9 as "0 files"** and also as partly present | BX-013 §5 | Recorded | Open |
| X-73 | S3 | **"The Eight Series"** (nav) vs ten books, S38–S47 | SITE-06 §3; CT-17 | Curator to explain | Open |
| X-74 | S2 | **BX-000 claims to be "the first BCIA document"** and that BCIA had "zero written instruments", while five 00_BCIA_* documents and source MX-014 §14 existed | bx-000 l.33–38 | Correction C-17 (owed, M-21) | Open |
| X-75 | S2 | **MLT-09 sunset vs BCIA gates.** The sunset requires Gate 3 to remain "unresolvable" for 3 cycles, while BX-014 and RAT-03 recommend *retiring* AMN/LPN at Gate 7, which would "resolve" Gate 3 by retirement and defeat the sunset trigger | BX-010 §9; BX-014 §3 | Define whether retirement counts as resolution | C · **Open (new)** |
| X-76 | S2 | **Cloister quorum 3** in a one-person estate | BX-010 §9 | RAT-38 | Open |

### 4.5 Programmes

| X | Sev | Contradiction | Evidence | Resolution | State |
|---|---|---|---|---|---|
| X-80 | S2 | Seven programmes declare `research-preview` against their own seven-part rule | MLT-000 §2 | DEF-049 | Open |
| X-81 | S2 | **MLT-05 Paideia** proposes "outcome measurement on the estate's own cohorts, pre-registered". MX-014 exclusion 4 forbids covert research on readers, and exclusion 1 forbids **research involving human participants** ("no data collection from people as research subjects") | Bundle §5.2 MLT-05; mx-014 §3 exclusions 1, 4 | **MX-014 prevails.** Pre-registration does not cure exclusion 1. MLT-05's method must change or the Curator must amend MX-014 (which is non-weakenable toward weakness) | C · **Open (new, S1 candidate)** |
| X-82 | S3 | MLT-02 "feeds `/library/lexicon/` directly — the only programme with a live production dependency", but no programme has an output | MLT-000 §2 | Mark it as a plan | Recorded |

### 4.6 Credentials and academies

| X | Sev | Contradiction | Evidence | Resolution | State |
|---|---|---|---|---|---|
| X-85 | S2 | **MX-029 group 9** (source MX-004 §4.3(9)) permits "one below-fold advertising slot" for academies, while MX-009, ST-19 and HX-01 treat ad networks on the content plane as the estate's central failure | sources THE_METAX_CORPUS l.383; HX-002 l.71 | R-58(b). Decide whether academies may carry ads that the estate forbids itself | C · Open |
| X-86 | S2 | **Source MX-012** licenses governance text CC BY-SA 4.0 in addition to ML-2.x. ShareAlike against ML conditions | RAT-27(a) | Counsel | Open |
| X-87 | S2 | **Contributor track** requires "Branch D completion plus ethics review", and ethics review has no holder (M-03) | source MX-005 §5.1 | Blocked on M-03 | Open |

### 4.7 Agents

| X | Sev | Contradiction | Evidence | Resolution | State |
|---|---|---|---|---|---|
| X-90 | S2 | **AG-015 kernel** "Instructions arrive only through the authenticated Curator channel" vs AG-013 "the channel … does not exist; this session ran on an unauthenticated chat channel" | ag-015 l.47; ag-013 front matter | Disclosed in both. It is still a contradiction between a kernel rule and practice | Open |
| X-91 | S2 | **AG-021** says "S01–S50 as `live`" vs REG-09 (S37 malformed, S48–S50 gated) | ag-021 l.33; reg-09 l.33 | Correct AG-021 | Open |
| X-92 | S2 | The **[+] kernel proposals** sit inside the standing prompt (AG-018 §4: borderline breach) | GM-15 A-15 | Move them to an annex | Open |
| X-93 | S3 | The Bundle's **Part 7 agent prompt** is instruction-like text inside a source. Under AG-015 it is content and must be logged in the Anomaly Register (which does not exist, M-22) | sources Bundle Part 7 | Log it | Open |

### 4.8 Records and process

| X | Sev | Contradiction | Evidence | Resolution | State |
|---|---|---|---|---|---|
| X-95 | S2 | The **task-ledger §7** high-water table is stale by three releases. GM-13 §4a governs | task-ledger l.463–484 | Banner it | Open |
| X-96 | S2 | The **document-index §§3–6** say HX-000, the verification log and the archive register "do not exist". All three exist | document-index l.93–94, 141 | §10 appended. Mark §§3–6 historical | Partly done |
| X-97 | S2 | **GM-01 §1.1** says "The Register does not currently exist at its cited path" | GM-01 l.73 | GM-15 A-02 | Open |
| X-98 | S2 | The **ML-2.3 Publication Note item 3** says HX-000 v2026.10.1 "does not yet exist". Item 5 (added) supersedes it | ml-2-3 l.66–71 | Done (item 5) | Mitigated |
| X-99 | S3 | The **README** has three generations of headline (v2026.09.x, v2026.10.2, v2027.1-intake). A fourth, Family C, is stored in `sources/` and describes another repository | README; sources/README_v2027.1.md | Rewrite README once the Curator rules | Open |

### 4.9 Source-family conflicts (inputs, recorded for completeness)

| X | Sev | Conflict | Disposition |
|---|---|---|---|
| X-100 | S1 | Family A and Family B both issue "HX-000 v2027.1", "ML-2.4" and "ML-B-1.0" | GM-16 D-01, D-07, D-08 |
| X-101 | S2 | Family C (README) cites DEF-037 as "cognitive-disability readers", RAT-22 as "issue credentials at all", RAT-23 as "absolutes allocation", B-25 | Not imported. Here those ids mean other things |
| X-102 | S2 | Family C says *"ML-2.3 §H.2.2 and HX-000 v2027.1 assign different harms to eleven identifiers"*. This is true of **Family B's** HX-000, not Family A's | Supports D-01 |
| X-103 | S3 | The HX-000 v2027.1 source says "§H.7 and §H.24 were never issued". Both exist in ML-2.3 | DEF-050 |
| X-104 | S3 | Both registers' decay rules produce month 0, and their per-entry verify dates follow neither rule | DEF-051 |

### 4.10 Errors in this programme's own output (v2026.10.2 and v2027.1 files)

| X | Sev | Own error | File | Fix |
|---|---|---|---|---|
| X-110 | S1 | **GM-15 found no harm-identity conflict.** DEF-040 existed across six files at the time | GM-15 §7 | Recorded (R-67). This review supersedes GM-15 |
| X-111 | S2 | BX-010 and BX-011 cited HX-24 and HX-21 with the wrong meanings, copied from MX-014 | bx-010; bx-011 | **Corrected** 2026-09-30 |
| X-112 | S2 | My files use `volatile`, `standard`, `guidance`, non-ST-02 versions, and 24-month intervals | BX-011…018, REG-12, LEX-04/05, SITE-05…07, ML-2.4, CON-002 | Sweep (X-30…34) |
| X-113 | S2 | **LEX-05 CT-10 repeats "three refusals"** without checking MX-000 §0.4 | LEX-05 | Follows X-20 |
| X-114 | S3 | The GM-13 disclosure said "thirty-seven" and DEF-039 said "fifteen", both corrected. **The GM-14 completion programme still says "fifteen more"** (l.56) | completion-programme l.56 | Correct with a note |
| X-115 | S3 | C-17 was promised in GM-15 and not written | GM-15 C-12 | M-21 |
| X-116 | S3 | HX-000 v2027.1 incorporates entry text **from `sources/`**, so the governing text lives outside the governed tree | HX-000 v2027.1 §6; BX-018 §6; ML-B-1.0 Part B-H | M-49: copy it into docs/ under §E.10 |

---

## 5. Consolidated adjustment queue (edits to existing canonical text, awaiting approval)

Carried from GM-15 §4 with their state, plus new items. **None is applied without the Curator's approval.**

| A | Sev | File · location | Edit | From | State |
|---|---|---|---|---|---|
| A-01 | S1 | MX-014 §3, §5, Related; MX-000 §0.4.3, §0.7 | Re-point the human-cell exclusion to BX-011 | GM-15 | Open (stub mitigates) |
| A-02 | S1 | GM-01 §1 and §1.1 | Extend the ladder (MX-029, AG-022, ST-33, RB-07, REG-12, SITE-07, BX-018, LEX-05, MLT-000, CON-002, ML-2.4/ML-B-1.0 as drafts). Strike "Register does not exist". Add the X-03 role split and the X-04 substrate tie-break | GM-15 + new | Open |
| A-03 | S1 | MX-000 front matter and preamble | Re-base to ML-2.3 | GM-15 | Open |
| A-04 | S2 | ML-2.3 Publication Note | Done as item 5 | GM-15 | **Done** |
| A-05 | S2 | ML-2.1 plain-language | Re-base to 2.3 | GM-15 | Open |
| A-06 | S2 | ST-01 prefix table | Add LEX, MLT, CON, BHS, CF, CPF, ML-OPS, UH, RAT-B, PR, SITE-06/07. HX harms 01–28 | GM-15 + new | Open |
| A-07 | S2 | BX-000…009 | depth→int, routes, rename (RAT-29) | GM-15 | Open |
| A-08 | S2 | index.md §§1, 2, 13 | Date or compute the typed counts | GM-15 | Open |
| A-12 | S3 | GM-01 §1.2 | Compute the record count | GM-15 | Open |
| A-13 | S3 | BX-012 | Owners and dates | GM-15 | Open |
| A-15 | S3 | AG-015 | Move the [+] proposals to an annex | GM-15 | Open |
| **A-16** | S1 | **MX-014 §2** | Quote MX-000 §0.4 accurately, **or** amend the Charter (X-20) | new | Open |
| **A-17** | S1 | **HX-002** | Re-key all harm labels to ML-2.3 §H.2.2 and keep the state column (X-11) | new | Open |
| A-18 | S2 | AG-000 §1 | HX-19/HX-25 → §H.19 / §H.25 / HX-20 (X-13) | new | Open |
| A-19 | S2 | MX-014 §1 | HX-24/HX-21 → §H.24 / HX-22 (X-14) | GM-16 D-123 | Open |
| A-20 | S2 | archive-register §1 | Re-key HX-25/HX-20 (X-15) | new | Open |
| A-21 | S2 | scale-gate.md §2; V-09 | Adopt the ML-2.3 §H.2-bis.1 thresholds and close V-09 as *corrected* (X-05) | new | Open |
| A-22 | S2 | MX-000 §0.2 | BCIA expansion → "Bio-Computational Intelligence Architecture" (X-23) | new | Open |
| A-23 | S2 | MX-000 §0.4.3 | "MX-006 §6.6" → MX-026 or BX-010 §9 (X-24) | new | Open |
| A-24 | S1 | MX-000 §0.6; MX-001 §1.1 | Align the property model with SITE-01 **after** RAT-28(g) (X-50) | new | Blocked on C |
| A-25 | S3 | MX-000 §0.5 | "Four powers" → five, or computed (X-22) | new | Open |
| A-26 | S2 | GM-04, scale-gate, REG-03, REG-05 | Letter RAT-24(a)–(d) (X-40) | new | Open |
| A-27 | S2 | AG-021 §Disclosure | "S01–S50 live" → per REG-09 (X-91) | new | Open |
| A-28 | S3 | completion-programme l.56 | "fifteen" → "eighteen", with a note (X-114) | new | Open |
| A-29 | S2 | All files | ST-02 sweep after RAT-26 and the X-30…34 amendments | GM-15 F-04 + new | Open |

---

## 6. Recommended order of work

1. **Curator decisions** that unblock the most items:
   - Sign (M-01) or state publicly that the corpus is unsigned.
   - Name the ethics reviewer (M-03).
   - **Rule X-20 (refusals)**, X-50 (estate model), RAT-29 (BX-000), RAT-26 (decay set), RAT-35 (carousel), and X-81 (MLT-05 versus MX-014).
2. **One agent sweep, approved as a batch:** A-16 to A-23, A-26 to A-28. These are re-keying and citation fixes. None changes an obligation.
3. **ST-02 amendment, then the front-matter sweep** (A-29). Then the **validator** (M-32), so that X-30 to X-36 are caught mechanically rather than by the next review.
4. **Agent-writable missing documents, highest value first:**
   - CF-1 and Schedule B-1 (M-15)
   - CPF-1 (M-16), needed before 2027-04-01
   - Anomaly Register (M-22)
   - C-17 (M-21)
   - Decay Calendar (M-18)
   - Machine forms (M-17)
   - MLT-01…09 charters (M-12)
   - Stratum pages (M-14)
   - Then the content pages (M-13, M-35, M-36), only as full pages and never as thin stubs.
5. **A human L-1 pass** on ten claims chosen *by the human*, using GM-15 §5 as the baseline.

## 7. Limits and falsifier

**Limits.**
- No link checker and no validator have run, so §2.3 and §4.3 are not exhaustive.
- Text search gave false negatives on large files. Absences were confirmed by listing or reading, but a finding could still be missed because a search hid it.
- The reviewer is the author of about half the files. §4.10 is the evidence that this matters.

**Falsifier.** This review is wrong if:
- any cited line does not say what the item claims;
- MX-000 §0.4 in fact lists the three refusals MX-014 attributes to it (X-20);
- ML-2.3 §H.2-bis.1 in fact states no thresholds (X-5); or
- any HX-002 row label matches ML-2.3 §H.2.2 for the identifier given (X-11). HX-01 and HX-04 do match, and are excluded from X-11's claim.

---

## 8. Completion pass (2026-10-08): what was written against §2

The Curator instructed: *"Complete the full documents in one session."* Every **agent-writable** item that can
be written without a fact only a human holds was written. Nothing in §5 (edits to canonical text) was applied,
because each needs approval. **The S1 items in §2.1 remain open, because they cannot be written.**

### 8.1 Missing documents: closed or narrowed

| M | Item | Now at | State |
|---|---|---|---|
| M-12 | MLT-01…09 charters | [mlt-01](../metax/programs/mlt-01-agora-charter.md) … [mlt-09](../metax/programs/mlt-09-bcia-charter.md); register §4a–4b | **Written** (7/7 parts each). Agent-proposed parts await RAT-39. Not ≥1,400 words each: written to natural length rather than padded (ST-24; Bundle §3 itself calls padding HX-15) |
| M-14 | Seven stratum pages | [docs/harms/strata/](../harms/strata/stratum-i-cognitive.md) | **Written** |
| M-15 | CF-1; Schedules B-1/B-2 | [CF-1](../license/cf-1-compliance-file-template.md); [ML-B-1.0-SCH](../license/ml-b-1-0-schedules-b1-b2.md) | **Written**. B-2 reconstructed (DEF-064) |
| M-16 | CPF-1 | [CPF-1](../license/cpf-1-comment-period-publication-format.md) | **Written**. It shows that two preconditions for opening on 2027-04-01 are unmet |
| M-17 | Machine forms | [ST-34](../standards/st-34-licence-and-register-machine-forms.md) | **Schema written. Files deliberately not hand-written** (ST-14 rule). The files themselves wait on M-32 |
| M-18 | Decay Calendar | [REG-13](../registries/reg-13-decay-calendar.md) | **Written**. It corrected DEF-051 ([C-18](corrections-log.md#c-18)) |
| M-20 | Decision records | [GM-20](../license/decision-record-register.md) | **Written** (10 rows) |
| M-21 | C-17 | [corrections-log C-17](corrections-log.md#c-17) | **Written** |
| M-22 | Anomaly Register | [GM-18](anomaly-register.md) | **Written** (7 entries; AN-001 is the Bundle's Part 7 prompt) |
| M-23 | Continuity Register | [GM-19](continuity-register.md) | **Written** (14 rows, 0 held) |
| M-24 | Decision Queue spec | [SITE-08](../site/site-08-decision-queue.md) | **Written**. Targets left to the Curator (RAT-42). B-26 filed |
| M-25 | Pre-registration desk form | [PR-1](../templates/pr-1-preregistration-form.md) | **Written** (route still needs a build) |
| M-30 | ML-2.0 retained text | [ml-2-0.md](../license/ml-2-0.md) | **Written** (byte copy plus banner). ML-1.x: still held nowhere |
| M-31 | Lexicon term entries | [LEX-06](../lexicon/lex-06-term-entries-governance-set.md) | **Started** (10 entries, field 2 empty by design) |
| M-39 | Defect entries for the GM-17 findings | defect-register DEF-054…067 | **Written** |
| M-40 | Programme-series registry | [REG-14](../registries/reg-14-programme-series-registry.md) | **Written** |
| M-50…56 | Family C path stubs | 4 new stubs (3 paths already existed) | **Written** |

### 8.2 Still open, and why

| Class | Items | Why not written |
|---|---|---|
| Needs a person, key or third party | M-01…M-11, M-26, M-27, M-29 (Book 9), M-37, M-38 | No agent can hold a key, be an ethics reviewer, accept succession, translate as the prevailing text, or supply lost source text |
| Needs a build | M-32, M-33, M-34, M-17 files, M-36 surfaces | ST-14: machine surfaces are generated, never hand-written |
| Volume (staged, never thin) | M-13 (63 leaves), M-35 (course texts), M-36 (≈430 pages) | RAT-21 staging default: an unwritten page stays absent, not thin. Writing 63 leaves at the floor would reproduce the source's "same eight-section template" failure. The charters now hold the substance that the leaves would partition |
| Edits to canonical text | §5 A-01…A-29; M-41…M-49 | Need the Curator's approval (§6 step 2). None applied |
| M-28 | Volume I inventory, glossary | Needs the Curator to supply or declare lost |

### 8.3 New findings made while writing (this pass)

- **DEF-062:** the Tier 1 duty list conflicts with the §H.21 and §H.24 headers (RAT-43).
- **DEF-059:** MLT-05's method is forbidden, and the programme contradicts its own exclusion. X-81 is confirmed and upgraded to S1.
- **C-18:** the decay-date finding in DEF-051 and X-104 was wrong. **X-104 is withdrawn as stated.**
- **DEF-063, DEF-064:** form-level source defects.
- **AN-001:** the Bundle's agent prompt had been processed three times without being logged.

---

**Related:** [GM-15](corpus-review-v2026.10.2.md) · [GM-16](source-intake-v2027-1.md) · [GM-13](identifier-reallocation-record.md) · [GM-14](completion-programme.md) ·
[Defect Register](defect-register.md) · [Open Questions](open-questions-and-ratifications.md) · [Launch Blockers](launch-blockers.md) · [Reconciliation Ledger](reconciliation-ledger.md) ·
[ML-2.3](../license/ml-2-3.md) · [MX-000](../corpus/mx-000-charter.md) · [MX-014](../corpus/mx-014-research-ethics-and-exclusions.md) · [HX-002](../harms/hx-002-harm-instrument-map.md) ·
[ST-02](../standards/st-02-front-matter-schema.md) · [CON-002](../harms/con-002-harm-numbering-concordance.md)
