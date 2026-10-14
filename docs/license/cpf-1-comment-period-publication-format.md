---
doc_id: "CPF-1"
title_en: "CPF-1 · Comment-Period Publication Format (Track 2 adoption)"
title_ar: "CPF-1 · صيغة نشر فترة التعليقات [AR-DRAFT]"
family: "license"
version: "v2026.10.3"
status: "draft"
authority: "operative-form"
prevailing_text: "en"
audience_tier: 4
depth: 4
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-08"
domain_tags: ["license", "comment-period", "track-2", "ml-2-4", "decision-record", "dissent"]
route: "/license/ml-2-4/comments/"
operative_window: "2027-04-01 → 2027-06-30 (planned; ML-2.4 §2 Track 2 step 2)"
human_read: "none"
conformance_state: "unmet"
derived_from: "Bundle Part 4.4 (Family B, CPF-1 one-line description); ML-2.4 draft §2, §7, §H.33(b)–(c); ML-2.3 §E.4 (60-day register amendment comment)"
authorship_note: "Drafted by an AI system under AG-000 to close GM-17 M-16. Retention is set here because the source left it unstated (source DEF-2026-078). That choice is the Curator's to confirm."
hreflang: "en, ar"
---

# CPF-1 · Comment-Period Publication Format

> **Authority.** An **operative form** for publishing a comment period, and the comments received
> in it, whenever an instrument requires public comment before adoption. Its first planned use is
> [ML-2.4](ml-2-4.md) Track 2 (§H.32 and absolute §H.3(a)(ix)), from 2027-04-01 to 2027-06-30. It
> applies equally to any §E.4 register amendment, such as admitting UH-03 and UH-05.

> **Disclosure first.**
> - (1) **The comment period cannot yet be honest.** A comment period whose only receiver is the steward has a receiver who decides on comments about itself. ML-2.4 §H.33(c) requires a dissent channel that does not route through the steward. **None exists (DEF-053).** Until one does, every CPF-1 publication must carry the banner in §2, and the comment period is a *steward-run consultation*, not an independent one.
> - (2) No comment period has yet been opened.

---

## 1. When CPF-1 applies

| Trigger | Minimum period | Source |
|---|---|---|
| Adding an **absolute** (Track 2) | **90 days** | ML-2.4 §2 Track 2 step 2 |
| Adding a **covenant** under Track 2 | 90 days | ML-2.4 §2 |
| Register amendment (new harm, narrowing) | 60 days | ML-2.3 §E.4 (as cited in HX-000 v2027.1 §15) |
| Any Charter amendment under MX-000 §0.8 | as §0.8 states | MX-000 |

**A shorter period than the trigger requires is a nullity.** The adoption that follows it is not an adoption.

## 2. The publication: what must be on the page at opening

```
COMMENT PERIOD CP-{instrument}-{YYYY}-{NN}
Instrument and clauses ....... (e.g. ML-2.4 §H.32, §H.3(a)(ix))
Opens ____  Closes ____  (≥ minimum in §1; dates in UTC)
Draft text ................... link to the exact text, with SHA-256 digest of that text
Evidentiary basis ............ link (Track 2 step 1)
What becomes prohibited ...... operative statement (Track 2 step 3), in one paragraph
Who is disadvantaged, by how much ... (Track 2 step 4); an empty answer is not accepted
Receivers .................... (a) the steward: ____  (b) the independent receiver: ____ / NONE (DEF-053)
How to comment ............... at least one route requiring no account, no identity provider, no JavaScript
Languages accepted ........... English, Arabic (§H.22 parity applies to the consultation itself)
Retention of comments ........ see §5
Decision record due .......... ≤ 30 days after close (§6)
```

**Mandatory banner while DEF-053 is open:**

> *This comment period is received and decided by the steward of the instrument under comment. No
> independent receiver exists yet (DEF-053). Comments that the steward rejects will be published with
> the reason, so that a reader can judge the reasons. Nobody but the steward can overturn them.*

## 3. The comment register

Every comment received, **including those rejected, withdrawn, abusive or off-topic**, receives a row. A comment is never silently dropped.

| Field | Content |
|---|---|
| `id` | `C-{CP-id}-{NNNN}`, sequential and never reused |
| `received` | timestamp (UTC) and channel |
| `commenter` | name as given, or `anonymous`, or `withheld at commenter's request`. The steward may hold identity privately for anti-abuse, and publishes only what the commenter consents to (§H.18) |
| `text` | verbatim. Redaction only for (a) personal data of third parties or (b) unlawful content, with the redaction marked and its ground stated |
| `clauses` | the clause or clauses addressed |
| `disposition` | `accepted` · `accepted-in-part` · `rejected` · `out-of-scope` · `withdrawn` · `duplicate-of {id}` |
| `reason` | **required for every disposition except `withdrawn`.** A reason must engage the comment's argument. "Noted" is not a reason |
| `change` | for `accepted*`: the exact text change, with before and after |
| `decided_by` | natural person (§H.19) |
| `decided_on` | date |

**Reasoned-reply obligation.** Every `rejected` row carries a reason that a third party could disagree with specifically. A rejection whose reason could be pasted onto any comment is treated as no reason, and the row counts as **unanswered** in §4.

## 4. Counts published at close

Computed from the register and never typed (Rule 6): received · accepted · accepted in part · rejected · out of scope · withdrawn · **unanswered**.

**If `unanswered` > 0 at the decision date, ratification may not proceed** for the clauses those comments address.

## 5. Retention (closes source DEF-2026-078, subject to the Curator's confirmation)

- The register, every comment as received, and the published dispositions are **retained permanently**. They are part of the decision record that ML-2.4 §H.33(b) requires, and the decision record has no expiry.
- The **private identity data** held for anti-abuse is deleted **12 months after the decision record** unless a claim or objection concerning that comment is open. This follows ML-2.3 §H.9 minimisation and the §H.3(a)(ix) tie-break (pending): if a claim is filed, the data goes to escrow and is not deleted.
- All superseded versions of the draft text are retained, with their digests (ML-2.4 §H.28 am., Migration Ledger).

## 6. The decision record

Published within 30 days of close, in the form ML-2.4 §7 uses:

```
DECISION RECORD DR-{instrument}-{YYYY}-{NN}
What changed ................ (clause list, with final text digests)
Why ......................... (reasons, citing the evidentiary basis)
Who decided ................. (natural person or persons)
Who objected ................ (count, and each objection's id; every objection must appear)
Rejected alternatives ........ (each, with the reason)
The steward's own dissent .... (where the steward disagrees with any part of what it adopted)
Effective date / transition .. 
Comments still unanswered .... (must be 0; see §4)
```

Decision records are filed in the [Decision Record Register](decision-record-register.md).

## 7. Worked instance (planned, not yet run): ML-2.4 Track 2

| Field | Planned value |
|---|---|
| CP id | `CP-ML-2.4-2027-01` |
| Clauses | §H.32, §H.3(a)(ix) |
| Opens / closes | 2027-04-01 / 2027-06-30 (91 days) |
| What becomes prohibited | Destroying, failing to retain, or making inaccessible a record whose effect is to defeat a foreseeable claim (the four elements of §H.3(a)(ix)) |
| Who is disadvantaged | Operators with short or ad-hoc retention, especially small actors without a published schedule. **The cost estimate is not yet written.** Without it, step 4 is unmet and the period may not open |
| Independent receiver | **NONE (DEF-053)**, so the §2 banner is mandatory |

**What the instance shows.** Two preconditions for opening the period are unmet today: the step-4 cost statement and an independent receiver. The form makes that visible six months before the planned date.

## 8. Falsifier

CPF-1 has failed if a comment period run under it produces a decision record that a commenter can
show omitted their comment, or rejected it with a reason that did not engage it. Such a record is
evidence of HX-15 (consultation as theatre), and it voids the adoption of the clauses concerned.

---

**Related:** [ML-2.4](ml-2-4.md) · [Decision Record Register](decision-record-register.md) · [CF-1](cf-1-compliance-file-template.md) ·
[ST-06 Objections](../standards/st-06-objections-standard.md) · [Launch Blockers](../00-governance-map/launch-blockers.md) · [GM-17](../00-governance-map/corpus-review-v2027.1.md)
