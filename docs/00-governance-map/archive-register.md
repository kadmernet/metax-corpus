---
doc_id: "GM-12"
title_en: "Archive Register — Superseded Text, Retained Permanently"
title_ar: "سجل الأرشيف — النصوص المنسوخة، محفوظة دائمًا"
family: "governance-map"
version: "v2026.10.1"
status: "canonical"
authority: "record"
prevailing_text: "en"
audience_tier: 5
depth: 3
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["governance", "archive", "supersession", "permanence"]
route: "/library/record/errata/"
provenance_of_purpose: "record"
hreflang: "en, ar"
---

# Archive Register

**What this instrument is.** The destination for every text this corpus has superseded, and the
record of what each superseded text said, when it stopped governing, and why.

**Why it exists.** [MX-000 §0.8](../corpus/mx-000-charter.md) forbids silent edits: superseded text
is retained with a non-governing banner rather than rewritten. That rule is cited by nearly every
instrument in this corpus as its authority for recording a correction instead of making one — and
until this release **it had no destination.** The Archive Register was cited by `docs/index.md` and
by the changelog and did not exist, which is a defect
[the Document Index §3](document-index.md) exposed and this file closes.

**Authority: `record`.** Nothing here governs. Every text in this register is non-governing by
definition; that is what being here means.

---

## 1. Position

Three instruments in this corpus record change, and they are routinely confused:

| Instrument | Records | Question it answers |
|---|---|---|
| [Changelog](changelog.md) | Releases, with reasons | *What changed, and why?* |
| [Corrections Log](corrections-log.md) | Claims found **wrong** | *What did we get wrong?* |
| **Archive Register** | Text that no longer governs | *What did it used to say?* |

The third is the one an auditor needs and the one estates omit. A changelog says a clause was
amended; a corrections log says a claim was wrong. **Neither preserves the superseded words**, and
without the words a reader cannot check whether the amendment did what the changelog claims, or
whether a party's conduct conformed to the text in force at the time.

**The macro register.** An institution that rewrites its own instruments is an institution whose
past cannot be audited, and the failure is nearly always innocent: text is improved, the
improvement is obviously better, and the previous version is deleted because nobody can imagine
needing it. Under Stratum VI this is **HX‑25** (silence in the record) and **HX‑20** (inheritance
of unauditable systems) — a successor inherits a corpus that appears always to have been correct.
This register is the estate's structural refusal, and the same refusal appears in the
**append-only redirect record** at [SITE-03 §6](../site/routing-law.md), where deleting a retired
address is likewise forbidden. Both implement one principle: **an estate may improve its text and
may not improve its history.**

---

## 2. Definition — what belongs here

Four classes. A text belongs in this register if it falls in any of them.

**Class A — Superseded instrument versions.** A whole instrument replaced by a later version. The
earlier text is retained in full.

**Class B — Superseded sections.** A section of a surviving instrument replaced by text with
different substance. Retained with the instrument's version at the time.

**Class C — Retired specifications.** A specification the estate abandoned, where the abandonment
is itself a governance fact — the reader needs to know the estate once specified this.

**Class D — Withdrawn or narrowed duties.** A duty withdrawn under [ML-2.3 §E.5](../license/ml-2-3.md)
following a demonstrated falsification. **The most important class and currently empty** — see §5.

### 2.1 What does not belong

**Editorial improvements.** Fixing a typo, tightening a sentence, correcting a broken link. If the
substance did not change, there is nothing to preserve. The test: *would a party's conduct have
been assessed differently under the old text?* If no, it is editorial.

**Unpublished drafts.** This register archives what **governed**. A draft that never governed has
no non-governing state to record.

**Defects.** A defect is a shortfall in current text, not superseded text.
[Defect Register](defect-register.md).

**The `MacroLifeTach` spelling.** Instructive as a boundary case. The misspelling was corrected in
four instruments, and it is **not** archived here — a name spelt wrongly was never a different
substantive claim. It is recorded at [C-13](corrections-log.md#c-13) as a correction, and the
defective **anchor** is retained *in place* in R-42 rather than archived, because a published
address must keep resolving. Three registers, three different treatments, one error.

---

## 3. The register

### Class A — Superseded instrument versions

| # | Text | Superseded by | Date | Retained where |
|---:|---|---|---|---|
| A-01 | **ML-2.1** | [ML-2.3](../license/ml-2-3.md) in estate practice | 2026-09-02 | **In place** at [`ml-2-1.md`](../license/ml-2-1.md) — a published licence version is never moved |
| A-02 | THE METAX CORPUS v2026.09.0 | `docs/index.md` v2026.09.1 | 2026-09-01 | [`sources/`](../../sources/) — retained verbatim as supplied |
| A-03 | METAX v2026.09.1 Meta-Review | Consolidated into the index and ledger | 2026-09-01 | `sources/` |
| A-04 | MetaX.Academy Page Content Specification | Consolidated; route grammar superseded by SITE-01 | 2026-09-01 | `sources/` |
| A-05 | MX‑NAV‑SPEC v2026.09.4 | **MX‑NAV‑SPEC v2026.10.1, in its entirety** | 2026-10-01 | **NOT RETAINED — see §4** |
| A-06 | MX-SITE-DESIGN v2026.09.3 (route sections) | SITE-01, SITE-03 | 2026-10-01 | `sources/` — retained; design sections still govern via DS-00 |
| A-07 | Designation List **DL-1** | [DL-2](../license/designation-list.md) | 2026-10-01 | **In place** — DL-2 retains DL-1's twelve rows and its ML-2.1 clause citations unchanged |

### Class B — Superseded sections

| # | Text | Superseded by | Date | Retained where |
|---:|---|---|---|---|
| B-01 | **DS-01's palette, ten gradients and per-brand ramps** | [DS-00](../design/ds-00-as-built-token-layer.md), read from live code | 2026-09-02 | **In place** at `ds-01-foundations-and-tokens.md` with a non-governing banner |
| B-02 | DS-01's "Ink-and-Paper" identity | DS-00 | 2026-09-02 | In place, banner |
| B-03 | DS-01–DS-06's four-tier motion hierarchy | DS-00 §7's five-tier system | 2026-09-02 | In place, banner |
| B-04 | MX-ARCH-001's **eight content subdomains** and `toptech.metax.academy/s/{S###}-{slug}/` route grammar | SITE-01, SITE-03 — one origin, directory routes | 2026-10-01 | In place; recorded at [C-04](corrections-log.md#c-04), C-15 |
| B-05 | `docs/index.md` §10's **fourteen subdomain page-spec rows** | SITE-01 … SITE-04 | 2026-10-01 | **See §4 — this is the register's own first failure** |
| B-06 | The estate's proposed local `H{n}` → duty citation convention | ML-2.3's upstream `HX-{nn}` rename | 2026-09-02 | Withdrawn at [C-10](corrections-log.md#c-10) |
| B-07 | "The Fourteen Structural Harms" as the register's scope and title | ML-2.3's twenty-five harms in six strata | 2026-09-02 | In place in the PARTIAL draft, whose title still reads "Fourteen" |

### Class C — Retired specifications

| # | Text | Why retired | Date |
|---:|---|---|---|
| C-01 | The query-parameter detail route `detail.html?type=series&id=N` | **Dissolved**, not repaired — directory routing removed its subject. [DEF‑2026‑042](defect-register.md#def-2026-042) | 2026-10-01 |
| C-02 | DEF‑2026‑041 as a **file-count** constraint | Re-characterised as a request-rate constraint under the same number | 2026-10-01 |
| C-03 | The 1000px mobile→desktop nav breakpoint | Nine pillars do not fit; moved to 1180px by [DS-07](../design/ds-07-navigation-geometry.md) | 2026-10-01 |
| C-04 | Hand-written `SEARCH_INDEX` | Generated at build time; [DEF-027](defect-register.md#def-027) | 2026-10-01 |

### Class D — Withdrawn or narrowed duties (§E.5)

**Empty.** See §5.

---

## 4. Where this register is already in breach

Two rows above disclose that the register cannot presently do its job, and both are recorded as
defects against this instrument rather than smoothed over.

**A-05 — MX‑NAV‑SPEC v2026.09.4 is not retained anywhere.** The v2026.10.1 spec supersedes it *"in
its entirety,"* and the estate **never held the v2026.09.4 text**. It was described to the estate
by its successor and cannot be archived. So the corpus contains an instrument whose supersession is
recorded and whose superseded text is unavailable — and a reader cannot check whether the four §0
corrections describe the previous spec accurately.

**B-05 — `docs/index.md` §10 claims the fourteen page-spec rows are "retained in the Archive
Register."** They are retained as **row B-05 of this table and nowhere else.** The rows were
replaced in the index, this register records that they existed, and their *text* is gone.

**What both failures have in common, stated plainly.** This register can record that a text
existed and cannot resurrect a text the estate never stored. That is not a flaw in the rule; it is
the rule arriving too late. §0.8 has been cited as authority since the corpus began, and its
destination was created in the third release — so **everything superseded before 2026‑10‑01 is
retained only where it happened to survive in place or in `sources/`.**

Filed as **DEF-029**: the archive rule predates the archive.

---

## 5. Class D is empty, and that is the number to watch

No duty in this corpus has ever been **withdrawn or narrowed**.

[ML-2.3 §E.5](../license/ml-2-3.md) obliges the steward to narrow or withdraw a duty when a
falsification is demonstrated. The twenty-five-harm register publishes a falsifier for every entry
precisely so that this can happen. Every instrument written this session carries a Falsifier
section. And Class D has no rows.

The estate's own standard, stated in `docs/index.md` §3a:

> *A register whose entries have never been narrowed is presumptively a doctrine and should be
> distrusted accordingly.*

**At one month old, an empty Class D is expected rather than damning.** Published unpublished, no
external reader has tested a falsifier, so nothing could have been narrowed. But this is the single
most informative empty table in the corpus, and its emptiness in twelve months' time would settle
the question the harms register keeps open about itself.

The most likely first entry is on the record already:
[MX-023 §7 falsifier 3](../corpus/mx-023-attention-and-human-sovereignty.md) — if readers, told
plainly what a streak counter does, endorse it anyway at scale, then §3.2's refusal is wrong as
written and would narrow to variable-ratio reward alone. The estate has named the duty it expects
to lose first, which is the cheapest available demonstration that Class D is meant to be used.

---

## 6. Failure modes

**The improvement that erases.** The characteristic failure and always innocent: text is bettered,
the previous version is deleted because nobody can imagine needing it. Detected only by an auditor
who wanted the old words, by which time they are gone.

**Archiving instead of retaining in place.** Moving a superseded licence version into an archive
directory **breaks every citation of it.** A-01 and B-01…B-03 are retained *in place* with
non-governing banners for exactly this reason. The register records *that* a text is superseded; it
does not necessarily hold the bytes.

**Editorial creep into Class B.** Archiving every tightened sentence, until the register is
unreadable and the substantive supersessions are lost among them. §2.1's test — *would a party's
conduct be assessed differently?* — is the control.

**Class D staying empty and nobody noticing.** §5 exists so this cannot happen quietly.

**Retroactive archiving to tidy a contradiction.** Moving an inconvenient text here to make the
current corpus look consistent, without a corrections entry. This would be the most serious
possible misuse: the register would become the mechanism of the concealment it was built to
prevent. Every row here must trace to a changelog release and, where the text was *wrong* rather
than merely superseded, to a corrections entry.

---

## 7. Limits

**Class: technical.** The register holds *pointers and descriptions*, not a content-addressed
store. §E.7's three-mirror requirement would provide the latter and does not exist
([B-02](launch-blockers.md)) — so the only custodian of the estate's superseded text is the estate,
in one repository, on one provider, which is the arrangement §E.7 was written to forbid.

**Class: epistemic.** Everything superseded before 2026‑10‑01 is retained only incidentally (§4).
The register's coverage begins now.

**Class: governance.** Nothing enforces this register. A future editor can delete superseded text
and not add a row, and no mechanism would detect it. The estate has no content-integrity check —
the pipeline at [DEF-001](defect-register.md#def-001) does not run.

---

## 8. Falsifier

This register is wrong if:

1. **A superseded text is found that appears in no row here** — expected for pre-October
   supersessions per §4, and a valid correction in every case after it.
2. **A row points at a "retained in place" location where the text is not in fact retained.**
   B-05 already fails this and says so.
3. **A row here describes text that still governs**, which would mean a supersession was recorded
   that did not happen.
4. **Class D acquires a row with no corresponding §E.5 falsification on the record**, which would
   mean a duty was quietly dropped rather than properly withdrawn — the inverse failure and the
   worse one.

---

## 9. Obligation

**For any editor superseding text:** add the row **in the same edit** as the supersession, and
prefer *retaining in place with a banner* over moving anything. A citation that stops resolving is
a worse outcome than an untidy file.

**For the estate:** file DEF-029 (§4). Reconstruct nothing — an estate that reconstructs a
superseded text it never held is fabricating a record, which is the failure the
[version history](../license/version-history.md) refused for ML-2.2 and the same refusal applies
here. Build the §E.7 mirrors so the archive is not custodied solely by its own subject.

**For a reader:** every text referenced here is **non-governing**. If a superseded text you need is
not retrievable, that is a defect and is filed at `/library/record/corrections-log/`, where rejected
submissions are published with reasons.

**Under ML-2.3:** §H.12 (harm to the record), §H.25 (silence in the record), §H.26 (corpus
hygiene), §H.27 (reversibility), §H.28 (custody and horizon), §E.5 (the withdrawal duty Class D
exists to record), §E.7 (the mirrors that would make this register durable).

---

**Related:** [MX-000 §0.8](../corpus/mx-000-charter.md) ·
[Changelog](changelog.md) · [Corrections Log](corrections-log.md) ·
[Document Index](document-index.md) · [Defect Register](defect-register.md) ·
[License Version History](../license/version-history.md) ·
[SITE-03 Routing Law §6](../site/routing-law.md)

*Curated by Maher. Fifteen superseded texts recorded, two of them already unretrievable, and one
empty table — Class D — whose emptiness in a year's time would settle whether this corpus keeps a
register or a doctrine.*
