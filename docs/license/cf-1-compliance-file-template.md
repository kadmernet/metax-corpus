---
doc_id: "CF-1"
title_en: "CF-1 · Part H Compliance File: Template"
title_ar: "CF-1 · ملفّ الامتثال للجزء H: نموذج [AR-DRAFT]"
family: "license"
version: "v2026.10.3"
status: "draft"
authority: "operative-form"
prevailing_text: "en"
audience_tier: 4
depth: 4
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-08"
domain_tags: ["license", "part-h", "compliance-file", "template", "scale-gate", "roles"]
route: "/license/compliance-file/"
operative_under: "ML-2.3 §H.1-bis, §H.2-bis, §H.16, §H.20, §H.31.3; ML-2.4 §H.32–§H.34 (pending)"
human_read: "none"
conformance_state: "unmet"
derived_from: "Bundle Part 4.4 (Family B, 'Schedule 1 / CF-1'); ML-2.3 Part H and Schedule 1; ML-2.4 draft §H.32(c)"
authorship_note: "Drafted by an AI system under AG-000 to close GM-17 M-15. The form adds no duty. Every field cites the clause that requires it. Where this template and ML-2.3 differ, ML-2.3 governs."
hreflang: "en, ar"
---

# CF-1 · Part H Compliance File: Template

> **Authority.** An **operative form** (tier 5). It creates no obligation. It is the place where a
> Licensee records how it meets the obligations [ML-2.3](ml-2-3.md) Part H already imposes.
> Where this form and the licence differ, the licence governs and the difference is a defect.

> **Disclosure first.**
> - (1) **Two artefacts, not one.** Family B's bundle labels this file "Schedule 1 / CF-1". In ML-2.3, **Schedule 1 is the Part H *Statement***: public, one to four pages, with four dispositions. The **Compliance File** is the *evidence behind* the Statement: internal, retained, and produced on request. Merging the two would let a public summary stand in for its evidence, which is HX-15. The two are kept apart here, and the mislabel is DEF-063.
> - (2) **Untested.** No Licensee has completed this form, the estate included. §9 is illustrative.
> - (3) Duties §H.32–§H.34 and absolute (ix) are **ML-2.4 drafts**. Their rows are greyed with *(pending)* and bind no one until ratification.

---

## 1. When a Compliance File is required

| Tier (ML-2.3 §H.2-bis.1) | Compliance File | Part H Statement (Schedule 1) |
|---|---|---|
| Tier 0 · Personal | Recommended. §3 (absolutes) only | Not required |
| Tier 1 · Small | **Required**: §§1–6, 8 | Short form (≤ 1 page) |
| Tier 2 · Substantial | **Required**: all sections | Full form (≤ 4 pages) |
| Tier 3 · Systemic | **Required**: all sections, plus the §H.16.6 independent-review record | Full form, with the review published unedited |

A Compliance File is **not** a safe harbour (§H.16.7). It is evidence of process, not of outcome (§H.17).

## 2. Disposition vocabulary

Two vocabularies meet here. They map one to one, and the file uses both so that it can generate the Statement mechanically.

| CF-1 disposition (internal) | Meaning | Statement disposition (§H.16.2) |
|---|---|---|
| `not-applicable-at-tier` | The duty's tier floor is above the Deployment's tier | *(omitted from the Statement)* |
| `disapplied-by-falsifier` | The harm's falsifier holds for this Deployment (§H.2.4: a falsifier may excuse, never impose) | **Not applicable**, with the falsifier relied on |
| `discharged` | The duty is done, not planned (§H.31.2) | **Remedied**, with the measure |
| `partly-discharged` | Done in part | **Partially remedied**, with what remains |
| `undischarged` | Applicable and not done | **Unremedied**, with the reason and a review date |

**Rule.** If no row is `partly-discharged` or `undischarged`, §H.16.3's presumption of non-compliance applies to the Statement. The file must then hold the rebuttal in §6.4.

---

## 3. Section A · Identification

```
CF-1 COMPLIANCE FILE
File id ............ CF-{deployment-slug}-{YYYY}-{NN}
Deployment ......... (name, URL or system identifier)
Licence ............ ML-2.3 | ML-2.4 (once ratified) | ML-B-1.0 profile (use Schedule B-1 as well)
Register version ... HX-000 v______ (ML-2.3 Works: v2026.10.1 as named; identity per ML-2.3 §H.2.2)
File version ....... ____  Opened ____  Last entry ____  Next review ____
Accountable person (§H.16.4, natural person) ____  Contact that reaches them ____
```

## 4. Section B · Roles (§H.1-bis; §H.20(a))

| Role | Party (legal name) | Natural person answerable | Accepted in writing (date, ref.) |
|---|---|---|---|
| Author | | | |
| Integrator | | | |
| Operator | | | |
| Commissioner | | | |

- **Joint holding (§H.20(b)).** Where two parties could each say a decision was the other's, list both. The duty is held jointly until one accepts it **publicly**. Record the acceptance here.
- **Unallocated role (§H.1-bis.3).** If there is no identifiable Operator, the last-supplying Integrator holds the Operator's duties. Name it.
- **Incapacity override (§H.20(c)).** Record any contractual allocation to a party lacking capacity. It is void for licence purposes, and the duty rests with the party that has the capacity.

## 5. Section C · Scale Gate determination (§H.2-bis)

| Input | Value | Counting basis | Source / evidence ref. |
|---|---|---|---|
| Affected Persons, last 12 months | | distinct natural persons | |
| People working on the Deployment | | headcount, any contract form | |
| Annual Deployment revenue (USD, CPI-indexed from 2026-10-01, §H.2-bis.3) | | Deployment only, not total business | |
| Material consequence? (liberty, livelihood, housing, health, education, benefits) | yes / no | | |
| Critical function? | yes / no | | |
| Any Agent acting on third parties? | yes / no | **any Agent triggers Tier 2** (§H.25 header) | |
| Public authority exercising statutory power? | yes / no | | |
| Another Tier 2+ Deployment structurally depends on this one? | yes / no | | |

```
Computed tier ..... T0 / T1 / T2 / T3      Computed on ____  by ____
Uncertain? ........ yes / no
If yes (§H.2-bis.4): applied the HIGHER candidate tier ____
                     OR filed determination request ref. ____ and applied the lower tier pending response
Recompute trigger . annually, and on any change crossing a threshold (§H.2-bis.1)
```

**Known defect in the gate (DEF-062).** ML-2.3 §H.2-bis.1 lists the Tier 1 duties as §H.3, §H.4, §H.6, §H.11, §H.16, §H.18, §H.19, §H.26 and §H.29. But the clause headers of **§H.21** ("all Tiers") and **§H.24** ("T1+") put those duties at Tier 1 as well, and §H.21 also at Tier 0. Until the Curator rules (RAT-43), **record §H.21 and §H.24 as applicable at the tier their own headers give**. That is the more protective reading. Mark the row "per clause header; DEF-062".

## 6. Section D · The absolutes (conditions; every tier, including private use, §H.2-bis.2)

For each absolute, record **engaged** or **not engaged**. For "not engaged", name **the element that is absent** (§H.3(a): all elements are cumulative, except (vii), which is disjunctive). The elements are ML-2.3 §H.3(a)'s and are **not paraphrased here**. Open the licence.

| § | Absolute | Engaged? | Element absent (if not engaged) | Evidence ref. |
|---|---|---|---|---|
| H.3(a)(i) | Engineered compulsion | | | |
| H.3(a)(ii) | Sensitive inference trading | | | |
| H.3(a)(iii) | Unappealable determination | | | |
| H.3(a)(iv) | Concealed synthesis | | | |
| H.3(a)(v) | Authorless judgement | | | |
| H.3(a)(vi) | Unprincipled agency | | | |
| H.3(a)(vii) | Developmental substitution (**disjunctive**: any one limb engages it) | | *n/a: name which limb is absent for each* | |
| H.3(a)(viii) | Irreversible foreclosure | | | |
| *H.3(a)(ix) (pending)* | *Record destruction defeating a claim* | | | |
| §C.5 | Weapons | | | |
| §C.9 | Core Riba (four cumulative elements) | | | |
| §B.5(b) | Defeating relicensure | | | |

**An "engaged" entry is not a compliance state.** It means that the grant terminated on occurrence (§F.4.2). Record the date and the §F.5/§F.6 position, and stop using the Work.

## 7. Section E · Per-duty disposition

The tier floor is the one each clause's own header states in ML-2.3, with DEF-062 noted.

| Duty | Harm(s) | Roles | Floor | Disposition | Measure / falsifier relied on / reason | Evidence ref. | Review date |
|---|---|---|---|---|---|---|---|
| §H.4 Optimisation disclosure | HX-01 | Operator | T1 | | | | |
| §H.5 Fallback competence | HX-02 | Operator, Integrator | T2 | | | | |
| §H.6 Provenance | HX-03 | Author, Operator | T1 | | | | |
| §H.7 Counterproductivity test | all | Operator, Commissioner | T2 (annual at T3) | | | | |
| §H.8 Inference inventory | HX-04 | Operator | T2 | | | | |
| §H.9 Minimisation and horizon (incl. worst-future-holder) | HX-05 | Operator | T2 | | | | |
| §H.10 Contestability | HX-06 | Operator, Commissioner | T2 | | | | |
| §H.11 Exit | HX-07 | Operator, Integrator | T1 | | | | |
| §H.12 Human labour disclosure | HX-08 | Operator | T2 | | | | |
| §H.13 Metric honesty | HX-09 | Operator, Commissioner | T2 | | | | |
| §H.14 Material accounting | HX-10 | Operator | T2 | | | | |
| §H.15 Dependency and fallback | HX-11 | Operator | T2 (exercise at T3) | | | | |
| §H.16 Part H Statement | HX-15 | all at T1+ | T1 | | link to Statement version | | |
| §H.17 Non-theatre | HX-15 | all | T2 | | | | |
| §H.18 Consent integrity | HX-16 | Operator | T1 | | | | |
| §H.19 Authorship of record | HX-14, HX-15 | Author, Operator | T1 | | | | |
| §H.20 Chain of responsibility | HX-17 | all | T2 | | → §4 above | | |
| §H.21 Proportionate imposition | HX-18 | Commissioner, Operator, steward | **all (DEF-062)** | | | | |
| §H.22 Language parity | HX-19 | Operator, Commissioner | T2 | | | | |
| §H.23 Channel parity | HX-13, HX-25 | Operator, Commissioner | T2 | | | | |
| §H.24 Developmental default | HX-24, HX-01, HX-04 | Operator | **T1 (DEF-062)** | | | | |
| §H.25 Agent constraint | HX-20 | Integrator, Operator | T2 (any Agent) | | envelope · authoriser · halt test date · log retention | | |
| §H.26 Corpus hygiene | HX-21 | Author, Operator | T1 | | | | |
| §H.27 Reversibility and sunset | HX-22 | Author, Operator, Commissioner | T2 | | sunset condition stated: ____ | | |
| §H.28 Custody and horizon (escrow (d) at T3) | HX-12, HX-23 | Operator | T2 | | custody plan ref. | | |
| §H.29 Substitution disclosure | HX-24 | Operator | T1 | | | | |
| §H.30 Non-participation | HX-25 | Operator, Commissioner | T2 | | | | |
| *§H.32 Forum, aggregation, retention, service (pending)* | *HX-27* | | *T1 (a),(c); T2 all* | | | | |
| *§H.33 Succession, decision record, dissent (pending)* | *HX-28* | *steward of a relied-upon instrument* | *T0/1 (a),(b); T2 all* | | | | |
| *§H.34 Unnamed-harm review (pending)* | *HX-26* | | *T0* | | search described: ____ | | |

### 7.1 Section F · Conflicts between duties (§H.31.3)

| Duties in conflict | Deployment fact causing it | Resolution | Reasoning | Recorded in Statement §F (date) |
|---|---|---|---|---|
| e.g. §H.6 provenance ↔ §H.9 minimisation | | | | |

**An unrecorded resolution is no defence** (§H.31.3).

### 7.2 Section G · Rebuttal of the §H.16.3 presumption (only if no harm is partly or wholly undischarged)

State why the Deployment is simple enough that an all-clear is credible. Name the features whose absence makes each harm inapplicable.

## 8. Section H · Evidence index, retention and survival

| Ref. | Artefact | Location | Created | Author (natural person) | Retained until |
|---|---|---|---|---|---|

**Retention (closes source DEF-2026-079).** Retain each entry for the **longer of**:
- (a) seven years from the entry date (Bundle §4.4);
- (b) the longest foreseeable claim horizon (ML-2.4 §H.32(c), pending). If that horizon is undetermined, retain until it is determined;
- (c) any period required by law.

**Survival.** The file **survives transfer of the Deployment** and passes with it. Under §H.28(a) the custody plan names who holds this file on insolvency, acquisition, death or incapacity. **Destroying the file while a claim is foreseeable** is the conduct ML-2.4 §H.3(a)(ix) would make a condition breach (pending).

**After-the-fact entries.** An entry made after the event it records is marked `retrospective`, with both dates. It is evidence of the record, not of the event (compare ML-B-1.0 §B-C.3).

## 9. Section I · Sign-off

```
I, ________ (natural person), am accountable for the accuracy of this file (§H.16.4, §H.19).
Machine assistance used in compiling it: yes / no. If yes, disclosed under §D.3: ________
Signed ________   Date ________
```

---

## 10. Worked instance (illustrative only, not a filed record): MetaX itself

**Section C.**
- **Affected Persons:** unknown. No analytics are retained under MX-023, so the count is genuinely not held.
- **Revenue:** ad slots exist (REG-12 P-02/P-03), and the amount is not recorded.
- **People working on it:** 1.
- **Material consequence:** credentials (MX-025) affect education standing, so **arguably yes**.

**Computed:** uncertain between T1 and T2. Under §H.2-bis.4 the estate must **apply T2** or file a determination. It has filed none.

**Section D.**
- (i) is not engaged: element four, "does not disclose the objective", is arguable, and the estate optimises nothing.
- (ii) is not engaged as to the estate. **The ad processors' own profiling is the open question** (HX-04, BHS-2027-001).

**Section E, selected rows:**
- §H.16 `partly-discharged`: draft only.
- §H.19 `undischarged`: `human_read: none` on most instruments.
- §H.21 `undischarged`: HX-18 self-instance.
- §H.22 `undischarged`: no Arabic.
- §H.28 `undischarged`: no executed succession (HX-28 under ML-2.4).

**What the instance shows.** The form forced a tier decision the estate had never made, and the honest answer was "the higher one".

## 11. Falsifier

This form is defective if a Licensee can complete it fully and still hide a disposition the
Statement would have to show. That would mean §2's mapping leaks. It is also defective if completing it at Tier 1 takes more than one afternoon for a single builder. That is the §H.21 test, applied to the estate's own form.

---

**Related:** [ML-2.3 Schedule 1](ml-2-3.md) · [Part H Statement](part-h-statement.md) · [Scale Gate](scale-gate.md) · [Schedule B-1/B-2](ml-b-1-0-schedules-b1-b2.md) ·
[CPF-1](cpf-1-comment-period-publication-format.md) · [ML-2.4](ml-2-4.md) · [GM-17](../00-governance-map/corpus-review-v2027.1.md)
