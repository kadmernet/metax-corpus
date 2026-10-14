---
doc_id: "GM-15"
title_en: "Corpus Review v2026.10.2 — Conflicts, Adjustments and Refinements"
title_ar: "مراجعة المتن v2026.10.2 — التعارضات والتعديلات والتحسينات"
family: "governance-map"
version: "v2026.10.2"
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
last_reviewed: "2026-09-26"
domain_tags: ["governance", "review", "conflicts", "audit", "completion"]
route: "/library/record/reviews/v2026-10-2/"
derived_from: "Full pass over docs/ after executing GM-14; directory listings; direct reads of MX-000, MX-014, GM-01, ML-2.3, SITE-01, index.md, document-index, the 00_BCIA_* sources and source MX-014"
provenance_of_purpose: "record"
authorship_note: "Written by the same AI system that drafted most of the instruments it reviews. It is therefore a self-review, and it carries the blind spot DEF-035 describes. It does not replace the human L-1 pass in §5."
hreflang: "en, ar"
---

# GM-15 · Corpus Review v2026.10.2

> **Authority.** A **record**. It governs nothing ([GM-01 §1.2](precedence-and-conflict-rules.md)).
> Each item names an owner and a proposed action. **No canonical text was edited on the strength of
> this review.** The A-items are edits for the Curator to approve, because they touch instruments at
> tiers 1–3.

> **Disclosure first.** (1) The reviewer is the drafter of about 100 of the files reviewed.
> (2) Text search returned false negatives throughout the pass. Every finding below comes from a
> direct read or a directory listing, never from an empty search. (3) The reviewer found three
> arithmetic errors **in its own registers** during this review (C-03). Assume there are more.

---

## 1. Scope and method

**Scope:** every file under `docs/` as of 2026-09-26, 17 families, about 230 files. That is
roughly 130 ingested, 55 new instruments and 48 pointers.

**Method:**
- **L-2 form audit.** Directory listing against [index.md](../index.md), [GM-13](identifier-reallocation-record.md) and the [Document Index](document-index.md).
- **Targeted reads** of every instrument on the precedence ladder's upper tiers (ML-2.3, MX-000, GM-01, MX-014).
- **Source comparison** for every restored BCIA claim.

**Not done:** a link checker (V-10), a front-matter validator (DEF-001), or a human read of any file.

**Severity scale:**
- **S1:** misleads a reader on a governing matter or on an absolute rule.
- **S2:** a contradiction between instruments that a careful reader would notice.
- **S3:** staleness, form or style.

**Owner codes:** **C** Curator · **A** agent (can apply once the Curator approves) · **B** build or tooling.

---

## 2. Summary

| Class | S1 | S2 | S3 | Total |
|---|---:|---:|---:|---:|
| Conflicts (C) | 3 | 8 | 2 | 13 |
| Adjustments (A) | 2 | 6 | 7 | 15 |
| Refinements (F) | — | — | — | 10 |

**The three S1 conflicts in one paragraph.**
1. The acronym BCIA meant two unrelated things, and the corpus's most absolute rule (the
   human-cell exclusion) was reached through a link to the wrong one (**C-02**).
2. Forty immortal identifiers were reused (**C-04**, with DEF-035 and DEF-039).
3. The estate's governance does not close anything. There are twenty-eight open questions and none
   is closed, and seventeen `[VERIFY]` tags with none closed (**C-01**).

The first two are now **mitigated** by pointers and refuge numbers. None of the three is **resolved**.

---

## 3. Conflicts

| Id | Sev | Conflict | Evidence (read directly) | Proposed resolution | Owner | Filed |
|---|---|---|---|---|---|---|
| **C-01** | S1 | **Governance that never closes.** 28 RATs are open and none is closed. 17 V-tags, none closed. The GM-04 amendment of 2026-10-01 said that another release with none closed should itself be filed as a defect | GM-04 amendments; verification log §3 | One Curator ruling session. Priority order: RAT-25, RAT-28(a), RAT-01, RAT-15, RAT-04 | C | DEF-039 |
| **C-02** | S1 | **BCIA: research programme vs reading model** | Sources 00_BCIA_* and source MX-014 §14.4 vs BX-000 §1 ("B·C·I·A — four phases") | Restored as BX-010…017. Recommend renaming the reading model (LEX-05 CT-01) | C | DEF-037, R-60, RAT-28(a) |
| **C-03** | S1 | **Arithmetic errors in this release's own registers.** GM-13 said "37 collisions" for a 40-row table. DEF-039 said "fifteen" where 40 − 22 = 18. The changelog said "50 stubs" where 46 were written (plus 2 licence pointers) | GM-13 §3 row count; LS of 8 directories | **Corrected during this review**, with the correction visible in each file | A | this item |
| **C-04** | S1 | **Forty reused identifiers** | GM-13 §3 | Refuge numbers plus 46 stubs. The Curator rules on RAT-25 | C | DEF-035, DEF-036, DEF-039 |
| **C-05** | S2 | Decay intervals 36/12/3 vs 12/6/3 | MX-026; ST-05 | RAT-26 | C | R-57 |
| **C-06** | S2 | Ads are live (AdSense, Adsterra) vs MX-009 and MX-029 §6 | REG-12 P-02/P-03; R-45/R-50 | Remove them during the demo window (R-50) | C | R-58(b), RAT-15 |
| **C-07** | S2 | Three estate models: a single domain with 9 pillars, a hub with 8 properties, and wildcard academy subdomains | SITE-01 §1; Meta-Review D.1.1 and B.9; Platform Persistence §1 | Keep M-A. Decide on M-C for academies separately | C | SITE-05, R-59(a), RAT-28(g) |
| **C-08** | S2 | "Pillar": three (Charter §0.2) vs nine (SITE-01 `KEYS`, MX-014 §1 "nine programs") vs DS-00's eight menu keys | MX-000 §0.2; SITE-01 §1.4; MX-014 §1 | "Pillar" means the three. "Programme" and "nav key" cover the others | C | LEX-05 CT-02, RAT-19, RAT-28(e) |
| **C-09** | S2 | Three defect-ID grammars | defect register; MX-NAV-SPEC; Meta-Review R5 | Choose one for new issues. Keep all existing strings | C | LEX-04 X-3, RAT-28(d) |
| **C-10** | S2 | **Status values are inconsistent within this release.** New instruments MX-025…029, AG-013…022, ST-25…33 and REG-09…12 say `canonical`. BX-010…017, LEX-04/05, SITE-05 and GM-15 say `draft`. BX-000 says `published`, and the stubs say `pointer`. None of these files has had a human read | front matter across families | **F-04 sweep:** every AI-drafted, unread instrument is set to `draft`, and `pointer` is added to the ST-02 enum | C then A | LEX-05 CT-09 |
| **C-11** | S2 | CC BY-SA 4.0 dual licensing vs the ML-2.3 conditions | source MX-012; MX-029 §6 | Counsel review | C + counsel | RAT-27(a), RAT-18 |
| **C-12** | S2 | BX-000 says it is "the first BCIA document to exist" and that BCIA had "zero written instruments". The estate held five 00_BCIA_* source documents and source MX-014 §14 | BX-000 disclosure block; `sources/` | Add a correction note to BX-000 (Corrections Log entry C-17) | A | this item |
| **C-13** | S3 | The series ID width is S01 vs S001 | REG-01; Meta-Review R1 | Treat both as one identifier in two renderings | C | RAT-27(b) |

---

## 4. Adjustments (edits to existing canonical text, awaiting approval)

| Id | Sev | File · location | Current text / state | Proposed edit | Owner |
|---|---|---|---|---|---|
| **A-01** | S1 | `corpus/mx-014-research-ethics-and-exclusions.md` §3 exclusion 2 and §5 | Links `bx-002-human-cell-exclusion.md` and names "BX-002" | Repoint to BX-011. The stub already carries the verbatim exclusion, so the risk is mitigated | A |
| **A-02** | S1 | `00-governance-map/precedence-and-conflict-rules.md` §1 and §1.1 | The ladder stops at MX-024, AG-012, ST-24, RB-05, REG-08 and SITE-04. **BX and LEX are not on the ladder at all.** §1.1 still says "the Register does not currently exist" (HX-000 now exists at `harms/hx-000-structural-harms.md`) | Extend the ranges to MX-029, AG-022, ST-33, RB-07, REG-12 and SITE-05. Place BX at tier 3 and LEX at tier 5 (proposal). Strike the §1.1 absence paragraph with a dated note | C |
| **A-03** | S2 | `corpus/mx-000-charter.md` front matter and preamble | `license: "ML-2.1 …"`, `version: v2026.09.2`; authority derived from ML-2.1 | Re-base to ML-2.3 (the tier-1 instrument), keeping the "unsigned" status paragraph | C |
| **A-04** | S2 | `license/ml-2-3.md` header and Publication Note | Header points to ML-2.2 as predecessor. The note's ML-D-008 said HX-000 did not exist | Add a dated Publication Note item recording that HX-000 now exists. The ML-2.2 wording stands until RAT-14 is decided | C |
| **A-05** | S2 | `license/ml-2-1-plain-language.md` | Parts are still based on 2.1 | Complete the re-basing to 2.3 | A |
| **A-06** | S2 | `standards/st-01-identifier-and-url-grammar.md` prefix table | Lacks REG, BX, GM, LEX, SITE, DS, ML-OPS and HX (LEX-04 X-5) | Add rows, with high-water marks pointing to GM-13 §4 | A |
| **A-07** | S2 | `bcia/bx-000…009` front matter | `depth: macro/meta/micro` (strings; ST-02 requires 1–5). BX-000 `prevailing_text: ar`, unlike the rest of the family. `route: /bcia/` is not in SITE-01 | Map macro→5, meta→4, micro→3 (proposal). Move routes under `/metax/bcia/` (subject to the rename ruling). Confirm the prevailing text | C then A |
| **A-08** | S2 | `index.md` §1, §2, §13 | Typed counts ("roughly seventy", "Thirteen open", "Thirty-three defects", "Fifty-six source conflicts"). §13 says the release is v2026.09.2. §10 says the old specs are retained in the Archive Register | Replace with computed-count placeholders once ST-13 runs. Until then, date every count. §14 has been appended | A |
| **A-09** | S3 | `00-governance-map/defect-register.md` footer | "Thirty-four defects …" is a typed count, against its own "Counts" section | Remove the typed count, or date it | A |
| **A-10** | S3 | `00-governance-map/document-index.md` §§3–6 | Stale by two releases | §10 appended (done). Mark §§3–6 "historical" in the headings | A |
| **A-11** | S3 | `00-governance-map/task-ledger.md` §7 | High-water table stale | §10 now points to GM-13 §4 (done) | — |
| **A-12** | S3 | GM-01 §1.2 | "Six instruments carry `authority: record`". There are now 15 or more (GM-13, GM-15, REG-09…12, BX-012/013/015, LEX-05, …) | Generate the count instead of typing it | A |
| **A-13** | S3 | `bcia/bx-012` vs source MX-014 §14.4 | The source says the defects are "published with owners and dates", but none has an owner or date | The Curator assigns owners and dates, or states that none will be assigned | C |
| **A-14** | S3 | Meta-Review B.9 sentence (if carried into MX-001 §1.2 or MX-014) | Points to `bcia.metax.academy/status/` (M-B) | Use `/metax/bcia/status/` (M-A) | A |
| **A-15** | S3 | `agents/ag-015-standing-system-prompt.md` | Three `[+]` kernel proposals are inside the standing prompt text. AG-018 §4 calls this a borderline breach | Move them to an annex until the Curator ratifies them | C |

---

## 5. L-1 source pass: ten claims

**Limitation:** the reviewer chose these claims, so this is **not** a valid L-1 pass under AG-011 §3.1,
which requires that the claims not be chosen by the agent. It is reported so that the human pass has a
baseline to compare against.

| # | Claim | Checked against | Result |
|---|---|---|---|
| 1 | BX-011 §1 exclusion text | 00_BCIA_PUBLIC_STATUS "Absolute exclusions" | **Verbatim match** |
| 2 | BX-016 §1 refused inference | source THE_METAX_CORPUS §14.5 | **Verbatim match** |
| 3 | BX-010 §3 "charter before experiment" quotation | source §14.2 | **Match** |
| 4 | BX-012 gate table (7 gates and v2026.08.14 statuses) | PUBLIC_STATUS and STATUS_PAGE_PATCH | **Match** |
| 5 | BX-012 "defect outside the gates" (the missing exclusion) | source §14.4 | **Match.** No gate tracks it |
| 6 | BX-014 AMN 19 / LPN 15 | PATCH gate 3; Taxonomy table (6+13, 2+13) | **Match** |
| 7 | BX-013 §5: Book 9 is listed as "0 files" while its chapters are present | Taxonomy report: method section vs table row 9 | **Confirmed.** The source contradicts itself |
| 8 | GM-01 §1.1 "Register does not exist" | LS `docs/harms/` (hx-000-structural-harms.md, 37 KB) | **Stale** → A-02 |
| 9 | MX-000 derives its authority from ML-2.1 | MX-000 lines 14, 26 | **Confirmed stale** → A-03 |
| 10 | SITE-01 places BCIA at `/metax/bcia/` | SITE-01 §1.5 redirects | **Confirmed.** The BX-010…017 routes were corrected to match |

**For the human pass (D-111):** take the **first sentence of §4 (Worked instance) of every fifth
file** in `ls docs/*/` order, open the cited source, and record each result in the verification log.
Twenty minutes.

---

## 6. Refinements

| Id | Refinement | Why | Owner |
|---|---|---|---|
| F-01 | Redraft archive-before-overwrite as a **prohibition** in AG-009 | DEF-034: every prohibition held and every affirmative duty failed | C |
| F-02 | Run a link checker over `docs/` and replace every "approximately" with a count | V-10; this review could not count broken links either | B |
| F-03 | Build the ST-02 front-matter validator | C-10 and A-07 would be caught mechanically | B |
| F-04 | **Draft sweep:** `status: draft` on every AI-drafted instrument without a human read. Add `pointer` to the ST-02 status enum | C-10; H19 (volume as evidence) | C |
| F-05 | Split RAT-28 into separate RATs as each letter is ruled | Omnibus entries tend to be left half-answered | A |
| F-06 | Add the component **"What BCIA claims here, and what is not yet settled"** to ST-28 | A source requirement with no component specified | A |
| F-07 | Write the human calibration set (≥12 specimens) | DEF-038 | C |
| F-08 | Adopt the kernel rule "list the directory before concluding absence" | Every S1 in this release was found by listing and none by search | C |
| F-09 | Ingest Books 7–10 fully and re-run the taxonomy scan | BX-013 §5 ingestion bias; RAT-05 | A + C |
| F-10 | Publish counts from a generator only (ST-13), including in records | C-03 shows that even records get typed counts wrong | B |

---

## 7. What this review did not find, and why that is not reassuring

No contradiction was found **between the eight-part bodies** of the new instruments. That is
expected, because one author with one prompt wrote them. Internal consistency across one author's
output is the property DEF-035 showed to be worthless as evidence. **Only a second reader can test
that.**

## 8. Falsifier

This review is wrong if any item cites evidence that does not say what the item claims, or if a
human L-1 pass finds a fabricated claim in any BX-010…017 file. BX-010…017 are the files where the
restoration's credibility is concentrated.

## 9. Obligation

- **Curator:** approve or reject the A-items one by one. Rule on RAT-25 and RAT-28(a) first.
- **Agents:** apply approved A-items with a changelog entry each, and never in bulk.

---

**Related:** [GM-14 Completion Programme](completion-programme.md) · [GM-13 Reallocation Record](identifier-reallocation-record.md) ·
[Defect Register](defect-register.md) · [Open Questions](open-questions-and-ratifications.md) · [Reconciliation Ledger](reconciliation-ledger.md) ·
[Verification Log](verification-log.md) · [Changelog](changelog.md) · [Task Ledger](task-ledger.md) · [LEX-05](../lexicon/contested-terms.md) ·
[BX-010](../bcia/bx-010-document-zero-and-research-charter.md) · [SITE-05](../site/information-architecture.md)
