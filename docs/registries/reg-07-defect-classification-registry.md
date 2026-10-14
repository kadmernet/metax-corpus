---
doc_id: REG-07
title_en: Defect Classification Registry
title_ar: سجل تصنيف العيوب
family: registries
version: v2026.10.1
status: published
authority: record
prevailing_text: ar
audience_tier: 3
depth: meta
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [defects, classification, severity, registry, remedy]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. The classification is applied retrospectively to defects filed before it existed.
route: /registries/defect-classes/
---

# REG-07 — Defect Classification Registry

> **Authority note.** A **record**. It supplies **vocabulary**, not authority. The
> duty to file defects is [MX-013 §4](../corpus/mx-013-records-and-versioning.md);
> the instances live in the
> [defect register](../00-governance-map/defect-register.md); launch-stopping
> severity is determined by the
> [launch blockers](../00-governance-map/launch-blockers.md), not here.

> **Disclosure first.** This classification was written **after** thirty-one
> defects had already been filed. It is therefore a taxonomy fitted to existing
> data, which is the weakest form a taxonomy can take: it is guaranteed to fit,
> and that guarantee proves nothing. Every class below is retrofitted, and §7
> states what would be needed to test the scheme properly.

---

## 1. Position

The estate's defect practice has one distinctive rule, from
[Charter §0.8](../corpus/mx-000-charter.md): **no silent edits.** A fault that is
fixed without a record is not a fixed fault; it is a fault plus a concealment.
Everything in this registry follows from that.

The consequence is counter-intuitive: a corpus committed to recording its faults
will always *appear* more defective than one that is not, and the appearance is
inverted relative to the truth. The estate accepts the reputational cost and
records the inversion here so the cost is at least legible.

What this page is **for**: giving each defect a class, a severity, and a remedy
shape, so that thirty-one heterogeneous entries can be reasoned about together.

## 2. Definition

A **defect** is a discovered non-conformity between what an instrument says and
what is the case, where either side may be at fault.

That symmetry matters. A defect is **not** necessarily a failure of the world to
match the document; it is equally often a document that claims too much. The
estate has both kinds and the classification distinguishes them, because the
remedies are opposite: one is fixed by doing work, the other by weakening a claim.

### 2.1 The seven defect classes

| Class | Name | Definition | Correct remedy |
|---|---|---|---|
| **DC-1** | **Dangling reference** | An instrument cites a document, section, or identifier that does not exist | Create the target, or withdraw the citation |
| **DC-2** | **Unoperable process** | A specified process cannot be executed with available resources | Staff it, or narrow the specification |
| **DC-3** | **Overclaim** | An instrument asserts a state of affairs stronger than the evidence supports | Downgrade the claim and relabel the evidence class |
| **DC-4** | **Unenforced obligation** | A duty exists with no mechanism that would detect breach | Build the check, or convert to a stated aspiration |
| **DC-5** | **Record gap** | A required record was not kept, or is unretrievable | Reconstruct if possible; **declare the gap** if not |
| **DC-6** | **Form breach** | An artefact fails a stated form standard (front matter, eight parts, furniture, word floor) | Repair the artefact |
| **DC-7** | **Vocabulary defect** | A controlled vocabulary lacks a term for a state that actually occurs | Extend the vocabulary by amendment with record |

The classes are **not** mutually exclusive. DEF-021 (the ML-2.3 §A.10 reference to
an absent HX-000) is simultaneously DC-1 and, because the licence's Tier 1 text
depends on it, arguably DC-4. Multi-class defects are normal and the register
records all applicable classes rather than forcing a primary.

### 2.2 Severity

Severity is **independent** of class. A dangling reference in a footnote and a
dangling reference on the face of the Tier 1 instrument are the same class and
vastly different severities.

| Severity | Test | Consequence |
|---|---|---|
| **S1 — Blocking** | A governing instrument cannot be applied as written | Enters [launch blockers](../00-governance-map/launch-blockers.md) |
| **S2 — Substantive** | A reader could be materially misled, or a stated guarantee is unavailable | Must be disclosed at the point of use |
| **S3 — Structural** | Internal inconsistency with no current reader-facing effect | Scheduled remedy |
| **S4 — Cosmetic** | Form or spelling, no meaning affected | Fixed opportunistically, still logged |

The severity test is deliberately phrased from the **reader's** position, not the
curator's. "Hard to fix" is not a severity input. A one-character fix can be S1
and a month of work can be S4.

### 2.3 Disposition vocabulary

`open` · `mitigated` (effect reduced, cause present) · `closed` (cause removed) ·
`re-characterised` (the original filing was wrong about what the defect was) ·
`declared-permanent` (cannot be remedied; recorded forever).

**`declared-permanent`** is the honest terminus for things like the missing ML-2.2
text: it cannot be reconstructed, so pretending it is `open` implies a remedy that
does not exist.

## 3. Mechanism

### 3.1 Classification path

```
defect observed        →  DEF- number assigned  [immortal, ST-01 Rule 2]
which side is at fault →  document overclaims?  → DC-3
                          world lags document?  → DC-1/2/4/5/6
reader effect          →  severity S1..S4
remedy shape           →  from the class row in §2.1
disposition            →  open | mitigated | closed | re-characterised | permanent
```

### 3.2 The remedy-shape rule

Each class has exactly one *shape* of correct remedy, and substituting a shape is
itself a defect. Examples of the substitution error:

- Fixing a **DC-3 overclaim** by doing the work instead of weakening the claim.
  This is often admirable and is *not* a remedy — the overclaim remains live until
  the work is complete, and readers are misled in the interval.
- Fixing a **DC-2 unoperable process** by removing the process entirely rather
  than narrowing it. This silently withdraws a guarantee, and withdrawn duties
  belong in [GM-12 Class D](../00-governance-map/archive-register.md), which is
  currently **empty** — suspiciously so, given the estate's history.
- Fixing a **DC-5 record gap** by reconstructing a record and not marking it as a
  reconstruction. The estate has done exactly this for two series intent
  statements ([REG-01 §7.1](reg-01-series-registry.md)).

### 3.3 Interaction with blockers

S1 defects enter the launch blockers list. The relationship is one-way: every S1
is a blocker, but a blocker may exist without a defect (e.g. B-01, an unsigned
licence, is a missing act rather than a non-conformity).

## 4. Worked instance

**DEF-031 classified — the estate's largest finding.**

DEF-031 records that four instruments (MX-016 appeals, MX-015 succession, MX-014
research ethics, ST-06 objections) specify processes that cannot operate, all for
one reason: **the estate has one participant.**

Apply §3.1:

| Step | Result |
|---|---|
| Which side at fault? | The **documents**. The world is not lagging; the specifications assume a plurality that was never claimed to exist |
| Class | **DC-2 unoperable process**, four instances — and **DC-3 overclaim**, because each instrument states a guarantee it cannot deliver |
| Severity | **S2** for three; **S1** for MX-016 stage 2, because it makes credential issue impossible ([REG-05 §3.3](reg-05-credential-registry.md)) |
| Remedy shape (DC-2) | Staff it *or* narrow the specification |
| Remedy shape (DC-3) | Downgrade the claim |
| Disposition | `open` |

The instructive result: **DEF-031 has two legitimate remedies pointing in opposite
directions.** Either the estate acquires a second participant (RAT-04, B-01 — the
remedy the defect register names), or it rewrites four instruments to promise only
what one person can deliver.

The estate has chosen neither, and the classification makes the non-choice
visible. That is the entire function of a severity-and-remedy taxonomy: it
converts "we are aware of this" into "there are exactly two exits and we are
standing in the doorway."

A second, smaller instance. **DEF-023** — `MacroLifeTach` for `MacroLifeTech`.
Class **DC-6** form breach, severity **S4** cosmetic, remedy shape *repair the
artefact*, disposition `closed` via correction C-13. Total cost: one character.
It is logged with the same ceremony as DEF-031 because the no-silent-edits rule
does not have a triviality exception, and an exception is exactly where silent
editing would re-enter.

## 5. The class census

Retrospective classification of the thirty-one filed defects. Counts are
approximate where a defect carries multiple classes.

| Class | Count | Severity spread | Notable instances |
|---|---|---|---|
| **DC-1** dangling reference | ~6 | S1 ×1, S3 ×5 | DEF-021 (ML-2.3 §A.10 → absent HX-000) — **S1** |
| **DC-2** unoperable process | ~5 | S1 ×1, S2 ×4 | DEF-031 (one participant) |
| **DC-3** overclaim | ~5 | S2 ×5 | route manifest as inventory (DEF-032) |
| **DC-4** unenforced obligation | ~4 | S2 ×4 | DEF-001 (SENTINEL specified, not running) |
| **DC-5** record gap | ~4 | S2 ×1, S3 ×3 | DEF-029 (two texts unretrievable); ML-2.2 absent — `declared-permanent` |
| **DC-6** form breach | ~5 | S4 ×5 | DEF-023 (spelling) — closed |
| **DC-7** vocabulary defect | ~2 | S3 ×2 | REG-03 lacks a `blocked` book state; per-page exemption not nameable |

### 5.1 What the distribution shows

- **DC-4 is the estate's structural weakness.** Four obligations exist with no
  detection mechanism, and all four trace to the same root: no runner exists, so
  no check runs. One fix (make SENTINEL run) would change four rows.
- **DC-3 overclaims cluster in the site layer.** The route manifest, the page
  contract's acceptance criteria, and the compliance rates in
  [REG-02](reg-02-page-registry.md) all describe an estate more built than the one
  that exists.
- **Only DC-6 has closures.** Every closed defect is cosmetic. **No substantive
  defect has been closed.** That is the single most important sentence in this
  registry, and it is arithmetic, not opinion.

### 5.2 The uncomfortable inference

If all closures are S4 and all S1/S2 defects are `open`, then the defect register
is functioning as a **disclosure instrument** and not as a **remediation
instrument**. The estate is honest and not yet effective. Recording faults is a
precondition of fixing them and is not a substitute, and a corpus that mistook the
first for the second would look exactly like this one.

## 6. Failure modes

| # | Failure | Mechanism | Current state |
|---|---|---|---|
| F1 | **Class shopping** | Choosing the class with the cheapest remedy shape | **Structurally possible** — one classifier, no review |
| F2 | **Severity deflation** | Rating by fix difficulty rather than reader effect | Guarded by §2.2's phrasing; unaudited |
| F3 | **Retrofit tautology** | Taxonomy fitted to known data, so it always fits | **Actual** — see §7.1 |
| F4 | **Closure inflation** | Cosmetic closures creating an impression of progress | **Occurring** — §5.1; disclosed rather than remedied |
| F5 | **Permanent as escape hatch** | `declared-permanent` used to stop tracking a fixable defect | One use (ML-2.2); judged correct, but unreviewed |
| F6 | **Vocabulary defects unfiled** | DC-7 requires noticing a missing word, the hardest noticing | 2 found; likely undercount |

## 7. Limits

1. **The taxonomy is retrofitted and therefore untested.** A classification derived
   from the cases it classifies cannot be falsified by those cases. The test is
   whether the **next** defect — DEF-032 onward — fits without a new class. Until
   several have, this scheme is an organising convenience, **E0** under
   [ST-07](../standards/st-07-evidence-and-verify.md).
2. **One classifier.** F1 and F2 have no control other than the classifier's own
   care, which is the condition DEF-031 describes.
3. **No defect has been closed on the merits.** The scheme's remedy shapes have
   never been exercised against a substantive fault.
4. **No Arabic text**, while `prevailing_text: ar`.
5. **The counts in §5 are approximate.** A register that reports its own defect
   distribution as "~6" is admitting it has not fully classified its own thirty-one
   entries. It has not. Completing that is one sitting's work and is owed.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** a defect is filed that fits none of DC-1…DC-7 — which would show the
>   class set is incomplete, and is the **intended** test (§7.1);
> - **(b)** a defect is shown to have been remedied by a shape other than its
>   class's shape, without that substitution being logged as an error;
> - **(c)** any closed defect is shown to be substantive rather than cosmetic —
>   which would **improve** the estate's position and falsify §5.1;
> - **(d)** an S4 defect is shown to have had material reader effect, falsifying
>   its severity.
>
> The estate would welcome (c). Its own reading of the record says it cannot be
> shown, and it invites the check against the
> [corrections log](../00-governance-map/corrections-log.md).

## 9. Obligation

No obligation arises from a record. Bearing duties:

- File every discovered non-conformity; **no silent edits** —
  [Charter §0.8](../corpus/mx-000-charter.md),
  [MX-013 §4](../corpus/mx-013-records-and-versioning.md).
- Apply the remedy shape for the class; log any substitution as an error — §3.2.
- Rate severity by reader effect, never by fix cost — §2.2.
- Place withdrawn duties in [GM-12 Class D](../00-governance-map/archive-register.md)
  rather than deleting them.
- Numbers are immortal; a withdrawn defect keeps its number —
  [ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md).

---

### Related

**Instances and ledgers** — [defect register](../00-governance-map/defect-register.md) ·
[launch blockers](../00-governance-map/launch-blockers.md) ·
[corrections log](../00-governance-map/corrections-log.md) ·
[reconciliation ledger](../00-governance-map/reconciliation-ledger.md)

**Governing duties** — [MX-013](../corpus/mx-013-records-and-versioning.md) ·
[MX-000 Charter](../corpus/mx-000-charter.md) ·
[ST-04](../standards/st-04-falsifiability-and-claim-cards.md) ·
[ST-06](../standards/st-06-objections-standard.md)

**Verification** — [GM-08 verification log](../00-governance-map/verification-log.md) ·
[ST-13](../standards/st-13-static-build-and-sentinel.md) ·
[ST-07](../standards/st-07-evidence-and-verify.md) ·
[RB-05](../rubrics/rb-05-harm-review-gate.md)

**Siblings** — [REG-02](reg-02-page-registry.md) ·
[REG-06](reg-06-dataset-registry.md) · [REG-08](reg-08-role-and-authority-registry.md)

### Exit pair

1. **Test the taxonomy.** Classify DEF-032 using §2.1 without inventing a class.
   If you cannot, falsifier §8(a) has fired.
2. **Check the hard sentence.** Read the
   [corrections log](../00-governance-map/corrections-log.md) and find one
   substantive closure. §5.1 says there is none.

<!-- mx-pagestamp: REG-07 · v2026.10.1 · record · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; counts describe the repository record -->
