---
doc_id: "GM-08"
title_en: "Verification Log — Every [VERIFY] Tag and Its Age"
title_ar: "سجل التحقّق — كل وسم تحقّق وعمره"
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
domain_tags: ["governance", "verification", "evidence", "decay"]
route: "/library/record/verification-log/"
provenance_of_purpose: "record"
hreflang: "en, ar"
---

# Verification Log

**What this instrument is.** Every `[VERIFY]` tag in the corpus, what it marks, who must resolve
it, and **how long it has been open**.

**Why the age column is the whole document.** A `[VERIFY]` tag is a promise to check something. A
corpus that emits tags and never resolves them has converted a verification mechanism into a
decoration — and the only way to detect that is to publish the age. A tag open for three months is
a queue; a tag open for three years is an admission.

**Authority: `record`.** It governs nothing and evidences the state of the corpus's own unverified
claims at a date.

---

## 1. Position

The estate's evidence apparatus has three parts.
[ST-07](../standards/st-07-evidence-and-verify.md) defines when a claim needs a citation and when
it may carry a `[VERIFY]` tag instead. [ST-05](../standards/st-05-decay-and-review-intervals.md)
assigns every claim a decay class and a review interval. This log is the **third** part and the one
that makes the other two falsifiable: without it, a `[VERIFY]` tag is a note to self.

It was created in v2026.10.1 to close a dangling reference that
[the Document Index §3](document-index.md) exposed — it had been cited by `docs/index.md`, the
defect register and the enforceability table since the corpus began, and did not exist. That is
worth recording at the top of the instrument rather than in a footnote: **the log tracking the
estate's unverified claims was itself an unverified claim for two releases.**

---

## 2. Definition — what a `[VERIFY]` tag is, and is not

**It is:** a marker on a claim the estate believes true, has published, and has **not
independently checked**. It is an honesty device. A statement carrying it may be relied on at the
reader's discretion and may not be cited as verified by this estate.

**It is not** any of these four, and the distinctions determine which register a gap belongs in:

| Not a… | Because | Belongs in |
|---|---|---|
| Placeholder | A placeholder has no content; a `[VERIFY]` claim has content that may be wrong | `[BRACKETS]`, e.g. `[STEWARD NAME]` |
| Defect | A defect is a known shortfall; this is an unknown correctness | [Defect Register](defect-register.md) |
| Open question | An open question needs a **decision**; this needs a **check** | [Open Questions](open-questions-and-ratifications.md) |
| Correction | A correction records something found **wrong**; this is not yet known either way | [Corrections Log](corrections-log.md) |

**The sharpest of the four is the third.** `[VERIFY]` asks *is this so?* An open question asks
*what shall we do?* Confusing them routes a factual question to the Curator's desk, where it waits
for a decision nobody needs to make, or routes a decision to a researcher who cannot make it.

---

## 3. The log

**Age is measured from first publication of the tag to 2026‑10‑01.**

| Id | Claim tagged | Instrument | Resolver | Opened | Age |
|---|---|---|---|---|---|
| V-01 | Per-jurisdiction enforceability of the **Track 2 representation claim** — asserted on general principle, confirmed by counsel in no named forum | [Enforceability Table](../license/enforceability-two-track-table.md) | Counsel | 2026-08-29 | **1 month** |
| V-02 | Jurisdiction, governing law and the liability cap figure | MX-002 §§2.13–2.14 | Counsel + Curator | 2026-08-29 | **1 month** |
| V-03 | Fee schedule and refund thresholds — structure fixed, figures unverified | MX-021 / pricing | Curator | 2026-08-29 | **1 month** |
| V-04 | Named role holders for the ethics reviewer and successors | MX-000 §0.5 | Curator | 2026-08-29 | **1 month** |
| V-05 | Dated claims across the book corpus, checkable but unchecked | REG-03 / Ascent | VERIFIER + human gate | 2026-08-29 | **1 month** |
| V-06 | BSN / LPN / AMN notation — referenced, never defined | BX-005 | Curator | 2026-08-29 | **1 month** |
| V-07 | **The six platform capacity figures** — 20,000 files, 100k requests/day, 1,000 KV writes/day, and three per-plan limits | [ST-22 §5](../standards/st-22-platform-and-persistence.md) | Build | 2026-10-01 | **new** |
| V-08 | **1180px nav breakpoint correctness for the Arabic RTL mirror** — derived from English label metrics only | [DS-07 §7](../design/ds-07-navigation-geometry.md) | Build | 2026-10-01 | **new** |
| V-09 | **The three Scale Gate thresholds** — unpublished, so the gate runs on qualitative tests alone | [Scale Gate §2](../license/scale-gate.md) | Curator | 2026-10-01 | **new** |
| V-10 | **≈70 unresolving paths in `docs/index.md`** — an estimate from reading, not a count from a tool | [Document Index §7](document-index.md) | Build | 2026-10-01 | **new** |
| V-11 | **The *Ḥifẓ al-ʿAql* extension** from intoxicants to attention-engineering — a reasoned lay analogy, not a ruling | ML-2.3 §0.4, HX-000, [MX-023 §6](../corpus/mx-023-attention-and-human-sovereignty.md) | Qualified scholar | 2026-09-02 | **1 month** |
| V-12 | **The two-auditor reproducibility test** for HX-001 — never run | [HX-001 §8](../harms/hx-001-harm-audit-rubric.md) | Curator + 2 auditors | 2026-10-01 | **new** |
| V-13 | **Content-plane migration by copying** — asserted as the property every durability claim rests on, never exercised | [MX-024 §7](../corpus/mx-024-infrastructure-and-migration.md) | Build | 2026-10-01 | **new** |
| V-14 | **Gate-6 dated claims C-01…C-08** (Landauer 1961, Shannon 1937/38, EDVAC 1945, Bell Labs 1947, Setun 1958, He Jiankui 2018, Neuralink 2024, DishBrain 2022). Supersedes V-05 for Branch D | [BX-015 §3](../bcia/bx-015-critical-audit-and-open-problems.md) | VERIFIER + human gate | 2026-09-26 | **new** |
| V-15 | **Processor jurisdictions and log retention** for Cloudflare, AdSense, Adsterra, FNT-001, Binance Pay | [REG-12 §1](../registries/reg-12-processors-keys-mirrors.md) | Curator | 2026-09-26 | **new** |
| V-16 | **The model version string** in the AG-016 provenance stamp. Agents cannot reliably self-report it | [AG-016](../agents/ag-016-output-contract-and-provenance.md) | Curator | 2026-09-26 | **new** |
| V-17 | **Registry signature verification.** ST-30 specifies it, but no key exists ([REG-12 §2](../registries/reg-12-processors-keys-mirrors.md)), so every credential claim is unverifiable | [ST-30](../standards/st-30-registry-and-verifier.md) | Curator | 2026-09-26 | **new** |

| V-18 | **MLT-01: "delegation concentrates power ∝ square of delegation depth"**. No derivation is given | [MLT-000 §3](../metax/programs/mlt-000-programme-register.md) | Curator / MLT-01 | 2026-09-30 | **new** |
| V-19 | **MLT-03 positions** on embodied carbon dominance, Jevons in compute, and indirect versus direct water | MLT-000 §3 | MLT-03 | 2026-09-30 | **new** |
| V-20 | **All evidence-tier claims in HX-000 v2027.1 and BX-018.** No bibliography is human-verified (source DEF-2026-056) | [HX-000 v2027.1](../harms/hx-000-register-v2027-1.md), [BX-018](../bcia/bx-018-register-of-substrate-harms.md) | Human compiler | 2026-09-30 | **new** |
| V-21 | **Cloudflare for SaaS "first 100 custom hostnames included"** and the carousel weight of about 118 KB | SITE-07; Platform Persistence | Build | 2026-09-30 | **new** |
| V-22 | **22 of the 24 BX-018 per-entry verify dates are unchecked** against the corrected rule (only BX-01 and BX-13 were read) | [REG-13 §3](../registries/reg-13-decay-calendar.md) | Agent (read the source) | 2026-10-08 | **new** |
| V-09 (update) | Scale Gate thresholds are **stated** in ML-2.3 §H.2-bis.1 (1,000 / 100,000 / USD 1,000,000 / 25 people / 1,000,000; CPI-indexed). The "unpublished" finding is **wrong as to the text**. Close as *corrected* once A-21 amends scale-gate.md | ML-2.3 l.421–432 | Agent | 2026-10-08 | **proposed close** |

*(Amended 2026-09-30: 17 → 21 open.)* **Seventeen open. None closed. Nothing in this log has ever been verified.** *(Amended 2026-09-26 from "Thirteen". The earlier figure is kept here because counts are computed, not overwritten: 13 → 17.)*

**One cheap closure was found during v2026.10.2 but not performed:** V-14 row C-02 has a known qualifier (the thesis was written in 1937 and published in 1938). This needs a human check against the primary source, not an agent's memory, so it stays open.

That sentence is the log's most useful output and it is published in the first release the log
exists. The honest reading is that the estate is one month old in its verification practice and
has produced no verifications — which is expected, and is exactly the number to watch, because a
log that still reads *none closed* in six months has established that `[VERIFY]` is decoration.

---

## 4. The four that are cheapest to close, and why they matter most

The estate ranks these not by importance but by **cost of checking**, because an unverified claim
that is cheap to check and stays open is the strongest available evidence that the mechanism is not
operating.

**V-07 — the platform limits.** Reading a provider's published pricing page. Minutes. And six
figures in a `perishable` standard currently rest on it.

**V-13 — migration by copying.** `rsync` the static estate to any second host and serve it. An
afternoon. **Every durability claim in the corpus depends on this property**, and it has never been
exercised — which is the same class of claim as a backup never restored.

**V-10 — the dangling-reference count.** A link checker over `docs/`. Minutes. It would replace the
estate's most embarrassing estimate with a fact.

**V-08 — the Arabic breakpoint.** Render nine RTL labels at 1180px and measure. Minutes, and it
falsifies or confirms a language-parity claim under ML-2.3 §H.22.

**The observation the estate draws from this ranking, against itself:** the four cheapest items in
this log are all `new`, meaning they were identified the moment the instruments citing them were
written — and none was checked *while writing them*. The writing was the opportunity. Four
verifications that cost minutes each were deferred to a log, which is precisely how a verification
queue becomes a graveyard.

---

## 5. Failure modes

**The tag as an escape hatch.** `[VERIFY]` used to publish a claim the author suspects is wrong.
The test in [ST-07](../standards/st-07-evidence-and-verify.md) is that the estate must *believe the
claim true*; a tag on a doubted claim is a defect wearing a verification marker.

**Tag inflation.** Marking everything unverified, which makes the log unreadable and the marker
meaningless. Thirteen is a manageable number; a hundred and thirty would not be.

**Silent resolution.** A claim verified and the tag removed with no entry in §6. The verification
then leaves no trace, and a future reader cannot tell a checked claim from an unmarked one.

**Age not published.** The failure this instrument was created to prevent. A log listing open tags
without their ages is a to-do list, and a to-do list flatters its keeper.

**Resolver unnamed or institutional.** "Build" appears four times above and is the weakest entry in
the table — it names a function, not a person. Under ML-2.3 §H.19 a tag whose resolver cannot be
asked a question has no accountable holder, and the estate's inability to name people here is
downstream of [B-01](launch-blockers.md): the licence is unsigned, so no role has a named holder
anywhere.

---

## 6. Closed verifications

**None.**

This section is retained empty rather than omitted, because an absent section reads as an
oversight and an empty one reads as a fact. Closed entries are **never deleted** — the record of
how long a claim stood unverified is the only evidence that the mechanism works, and deleting it
would leave the log unable to answer the one question a reader should ask of it.

The closure format, so the first entry has a shape to follow:

```
V-nn  [claim]
  Verified by: [natural person]  On: [date]  Age at closure: [duration]
  Method: [what was actually checked]
  Result: [confirmed | corrected | withdrawn]
  If corrected: filed at Corrections Log C-nn
```

**`Result: corrected` routes to the [Corrections Log](corrections-log.md).** A verification that
finds a claim wrong is a correction, and the estate's own history suggests this will be the common
outcome: nine of sixteen corrections to date came from checking the corpus against reality rather
than against itself.

---

## 7. Limits

**Class: technical.** This log is hand-maintained. The tag sweep that would populate it
automatically requires the pipeline at [DEF-001](defect-register.md#def-001), which does not run —
so the log's completeness rests on whoever wrote the last instrument having remembered to add a
row. **V-10's own uncertainty applies here recursively:** the estate cannot reliably count its own
`[VERIFY]` tags, so this list is best-effort.

**Class: epistemic.** Ages are computed from *first publication of the tag*, which for the
pre-October entries means the date the instrument was written rather than the date the underlying
claim was made. Some claims are older than their tags.

**Class: governance.** Four rows name "Counsel" or "a qualified scholar" as resolver. The estate has
engaged neither. Those rows cannot close by internal effort at any level of diligence, and marking
them open indefinitely is honest rather than negligent — but it should not be mistaken for a queue
that is moving.

---

## 8. Falsifier

This log is wrong if:

1. **A `[VERIFY]` tag exists in the corpus with no row here** — expected, per §7, and every
   instance is a valid correction.
2. **A row here has no corresponding tag in its named instrument**, meaning a tag was removed
   without a §6 closure.
3. **An age is wrong**, which is checkable against the changelog and the instruments' front matter.
4. **A row is filed here that is properly a defect or an open question** — the §2 boundary
   misapplied. V-09 is the closest call: unpublished thresholds might be an open question rather
   than an unverified claim, and the estate files it here because the figures exist in the
   Curator's judgement and merely have not been stated.

---

## 9. Obligation

**For the estate:** close V-07, V-08, V-10 and V-13 — the four cheapest, per §4 — before the next
release. Failing to close items that cost minutes each, while publishing a log whose purpose is to
expose exactly that, would be [HX‑15](../harms/hx-002-harm-instrument-map.md) committed by this
instrument.

**For any author adding a `[VERIFY]` tag:** add the row here in the same edit. A tag without a row
is invisible, and an invisible tag is the failure mode of §5.

**For a reader:** any claim in this corpus carrying `[VERIFY]` may not be cited as verified by this
estate. Under
[§2 condition 3 of the Machine Reading Contract](machine-reading-contract.md) the tag must be
preserved verbatim in any quotation.

**Under ML-2.3:** §H.19 (authorship of record — the reason §5 names "Build" as the table's weakest
resolver), §H.17 (non-theatre — the reason ages are published), §E.5 (which obliges the steward to
narrow or withdraw a duty on demonstrated falsification, and which a `Result: withdrawn` closure
would engage).

---

**Related:** [ST-07 Evidence and VERIFY](../standards/st-07-evidence-and-verify.md) ·
[ST-05 Decay and Review Intervals](../standards/st-05-decay-and-review-intervals.md) ·
[Document Index](document-index.md) · [Defect Register](defect-register.md) ·
[Corrections Log](corrections-log.md) ·
[Open Questions](open-questions-and-ratifications.md) ·
[Machine Reading Contract](machine-reading-contract.md)

*Curated by Maher. Thirteen unverified claims, none closed, four of them checkable in minutes — and
the log that tracks them was itself a dangling reference for two releases.*
