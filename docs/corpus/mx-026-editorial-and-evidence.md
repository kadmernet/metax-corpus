---
doc_id: "MX-026"
title_en: "Editorial and Evidence Policy"
title_ar: "السياسة التحريرية وسياسة الأدلة"
family: "corpus"
version: "v2026.10.2"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 2
depth: 5
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: true
last_reviewed: "2026-09-25"
domain_tags: ["corpus", "editorial", "evidence", "review", "corrections"]
route: "/method/"
derived_from: "THE METAX CORPUS v2026.09.0 Part II MX-006 §§6.1–6.8"
supersedes: ["Index allocation MX-006 'Editorial and Evidence Policy' (refuge number; see GM-13)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "specification"
authorship_note: "Drafted by an AI system under AG-000. The seven rules restate source MX-006; the mapping to standards is the agent's."
hreflang: "en, ar"
---

# MX-026 · Editorial and Evidence Policy

> **Authority.** `governing`, tier 3. The **parent policy** of the epistemic standards: ST-03
> (Limits and Bridge), ST-04 (falsifiers), ST-05 (decay), ST-06 (objections), ST-07 (evidence and
> `[VERIFY]`). Each of those cites "MX-006 §6.x"; that text lives **here** under a refuge number
> ([GM-13](../00-governance-map/identifier-reallocation-record.md)).

> **Disclosure first.** The standards this policy parents were written before it, and some cite
> sections of it that did not exist. The rule most often cited — §6.3, *falsifiers enforced
> mechanically, not editorially* — has **no mechanism**: SENTINEL does not run
> ([ST-13](../standards/st-13-static-build-and-sentinel.md)). The three-pass review in §8 has
> never been performed, because the science and ethics passes need people who do not exist.

---

## 1. Position (meta)

An editorial policy for a corpus with one author is a policy the author writes about himself. It
can only be credible if its rules are **checkable by a reader against the page** — a tag either
exists or it does not; a falsifier is either stated or it is not. The policy therefore prefers
visible, ugly, countable marks to good intentions.

## 2. The evidence standard (§6.1)

Every substantive claim carries **a decay class, and either a dated source or a visible
`[VERIFY]` tag.** The tag renders in amber and is deliberately unattractive: it is a debt on the
page, and the [Verification Log](../00-governance-map/verification-log.md) tracks its age.
**No undated statistic appears anywhere.** Operative form: [ST-07](../standards/st-07-evidence-and-verify.md).

## 3. Decay classes (§6.2)

| Class | Source interval | Examples |
|---|---|---|
| Durable | **36 months** | Physical constants, mathematical results, historical facts |
| Semi-durable | **12 months** | Institutions, regulatory regimes, established practice |
| Perishable | **3 months** | Platform behaviour, pricing, tooling, markets |

> **Conflict recorded, not resolved.** The source gives 36/12/3. [ST-02](../standards/st-02-front-matter-schema.md)
> and [ST-05](../standards/st-05-decay-and-review-intervals.md) use **12/6/3**, and most front
> matter follows them. This policy restates the source faithfully and does not choose. Filed as
> [R-57](../00-governance-map/reconciliation-ledger.md) and [RAT-26](../00-governance-map/open-questions-and-ratifications.md#rat-26).

A page past its interval displays a stale marker on its own face.

## 4. Falsifiability (§6.3)

Every claim card carries a falsifier. **A card without one fails the build** — enforced
mechanically because editorial enforcement of a discipline the editor also authors is not
enforcement. Operative form: [ST-04](../standards/st-04-falsifiability-and-claim-cards.md).

## 5. Limits and Bridge (§6.4)

Every series carries a Limits module across four classes — **physical, economic, epistemic,
ethical** — and a Bridge lesson naming the successor discipline, what it inherits, and what it
discards. A series lacking either does not ship. The pattern is borrowed openly from the Meta-X
book library, where every volume ends with a limits chapter and a bridge chapter: the curriculum
and the research library are meant to be recognisably the same intellectual object at different
altitudes. Operative form: [ST-03](../standards/st-03-limits-and-bridge.md).

## 6. Objections (§6.5)

Every course carries an Objections and Answers block: the objection at full strength, in the
objector's framing, before the answer; concessions where honest. **An objections block whose
every answer ends in total victory is flagged as insufficiently written.** Operative form:
[ST-06](../standards/st-06-objections-standard.md).

## 7. Banned comparisons (§6.6)

Any quantitative comparison between experiments with materially different conditions, presented
as like-for-like, is banned corpus-wide. **Named instance:** the DishBrain-versus-DeepMind speed
figure (the "28,800×" claim). Where both experiments are discussed, the page states that they are
not comparable and why. Register of banned claims: `/method/epistemics/banned-claims/`.

## 8. Corrections (§6.7)

Errors are corrected by **publishing a correction**, never by silent edit. The
[Corrections Log](../00-governance-map/corrections-log.md) carries what was wrong, what it
affected, the correct statement, and the date. Superseded documents keep their URLs, gain a
superseded header, and point to the replacement. **Nothing is deleted.**

## 9. The three-pass review (§6.8)

**Language, then science, then ethics — in that order, never merged.** Merging them is how ethical
review becomes a copy-edit. Operative gate: [RB-06](../rubrics/rb-06-structural-review.md).

| Pass | Who | Exists? |
|---|---|---|
| Language | Editor | Curator only |
| Science | Subject reviewer | **No** |
| Ethics | Named ethics reviewer with veto | **No** ([B-03](../00-governance-map/launch-blockers.md)) |

## 10. Worked instance

[DS-04](../design/ds-04-academic-features.md) mentions a "correction bounty". Under §2, the
bounty amount would be a claim needing a source or tag. Under §8, if the amount changes, the old
amount stays visible with a correction entry. Under §9, the ethics pass would ask whether paying
for corrections creates an incentive to plant errors. None of the three has been applied.

## 11. Limits

This policy governs **how** claims are made. It cannot make an author right; it can only make an
author's wrongness findable.

## 12. Falsifier

The policy fails if a reader can find, in any instrument, an undated statistic with no tag, or a
claim card with no falsifier, that has stood for more than one review interval. **Expected to
fail today**, given SENTINEL does not run.

## 13. Obligation

Appoint science and ethics reviewers. Run SENTINEL's F-2 check ([ST-13](../standards/st-13-static-build-and-sentinel.md)).
Rule on RAT-26.

## 14. Macro register

The dominant information economy rewards confident claims and punishes visible uncertainty. An
amber tag is a small act of refusing that trade: **it makes the estate look worse in order to be
more useful.** The policy is a bet that, over decades, readers learn to trust the source that
shows its debts.

---

**Related:** [ST-03](../standards/st-03-limits-and-bridge.md) · [ST-04](../standards/st-04-falsifiability-and-claim-cards.md) ·
[ST-05](../standards/st-05-decay-and-review-intervals.md) · [ST-06](../standards/st-06-objections-standard.md) ·
[ST-07](../standards/st-07-evidence-and-verify.md) · [RB-06](../rubrics/rb-06-structural-review.md) ·
[Corrections Log](../00-governance-map/corrections-log.md) · [Verification Log](../00-governance-map/verification-log.md) ·
[ST-27 Style Guide](../standards/st-27-style-guide-en.md)
