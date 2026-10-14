---
doc_id: "ST-04"
title_en: "Falsifiability and Claim Cards"
title_ar: "قابلية التكذيب وبطاقات الادّعاء"
family: "standards"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 4
depth: 5
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["standards", "falsifiability", "epistemics", "claims"]
route: "/method/rails/falsifiability/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# ST-04 · Falsifiability and Claim Cards

**What this standard governs.** The form every substantive claim in this estate must take, and the
one thing it must carry: **the observation that would show it wrong.**

**The rule in one sentence.** A claim without a stated falsifier is not necessarily false; it is
**unfalsifiable**, which is a different and worse property for a document claiming academic
standing.

---

## 1. Position

This is the estate's central methodological commitment and the one from which most others descend.
[ST-05](st-05-decay-and-review-intervals.md) asks how long a claim survives; ST-04 asks **what
would kill it**. [ST-07](st-07-evidence-and-verify.md) asks what supports it. Together they are the
apparatus that makes a claim in this corpus something other than an assertion by a confident
author.

It is routed at `/method/rails/falsifiability/` — one of the six rails — and it is enforced through
[ST-24 §2](st-24-page-prose-standard.md), which makes a Falsifier section mandatory in the
eight-part page recipe, and through
[SITE-02 §9](../site/page-contract.md) line 2, which fails a page missing it.

**The macro frame.** Technical education is dominated by claims structurally immune to refutation:
best practices, industry standards, what "works." Each is a real generalisation and none states the
observation that would retire it, which means such a corpus cannot be *wrong* — only unfashionable.
Under **HX‑02** (epistemic dependency) that is the harm: a reader who cannot check a claim must
defer to whoever asserts it, and deference at scale is what makes an information ecosystem
unaccountable. A falsifier is the cheapest available refusal of that arrangement, and it costs one
sentence.

---

## 2. Definition — what counts as a falsifier

A falsifier is an **observation**, stated so that a reader could in principle make it and find the
claim wanting. Four properties, all required:

**1. Observable.** It names something a person could see, measure, count or test — not a state of
affairs knowable only by its author.

**2. Specific.** It names *this* claim's failure, not a general possibility of error. *"This may
be wrong"* is not a falsifier; nothing follows from it.

**3. Adverse.** If observed, the claim **fails**. A falsifier whose occurrence leaves the claim
intact is a caveat wearing a falsifier's clothes.

**4. Available in principle.** It need not be cheap. It must not be impossible: a falsifier
requiring a controlled trial the estate will never run is honest only if it says so.

### 2.1 The four counterfeits

Each of these passes casual reading and defeats the purpose. The estate names them because it has
written at least one of each.

**The tautological falsifier.** *"This page is wrong if the estate's whole method is wrong."*
Unfalsifiable in practice, since nothing short of total collapse counts. Named as a live risk in
[HX-001 §7](../harms/hx-001-harm-audit-rubric.md), where a deliberately unfalsifiable falsifier is
recorded as defeating the rubric's purpose.

**The unreachable falsifier.** *"This is wrong if a ten-year cohort study shows no effect."* True,
adverse, specific — and the estate will never run it. Permitted **only** when the cost is disclosed
in the same breath.

**The restated caveat.** *"This is wrong if the platform changes its limits."* That is a decay
class ([ST-05](st-05-decay-and-review-intervals.md)), not a falsifier. Decay says *when to
recheck*; falsification says *what would refute*.

**The falsifier nobody would ever check.** Formally fine, practically inert. The test the estate
applies: *if this were observed, would anyone notice and tell us?* If no, the claim needs a second
falsifier that someone has a reason to run.

---

## 3. Mechanism — the claim card

Any claim carrying operative weight is published as a **claim card**:

```
CLAIM      [the assertion, one sentence]
CLASS      [empirical | procedural | normative | definitional]
BASIS      [citation, or "the estate's own position, unsupported by external evidence"]
EVIDENCE   [E0–E4 per ST-07]
DECAY      [durable | semi-durable | perishable] + review date
FALSIFIER  [the observation that would refute it]
IF FALSE   [what changes in this corpus — the instrument and section affected]
```

### 3.1 `IF FALSE` is the field that makes falsification operative

The other six fields describe a claim. `IF FALSE` states **what the estate would have to do**, and
without it a falsifier is a gesture.

[ML-2.3 §E.5](../license/ml-2-3.md) obliges the steward to **narrow or withdraw** a duty when a
falsification is demonstrated. That duty is unusable unless each claim already names what would
narrow. So `IF FALSE` is where the harms register's promise about itself becomes checkable:

> *A register whose entries have never been narrowed is presumptively a doctrine and should be
> distrusted accordingly.*

The estate's withdrawal count stands at **zero**, recorded in the deliberately empty **Class D** of
[the Archive Register §5](../00-governance-map/archive-register.md). At one month old that is
expected. It is also the single most informative empty table in the corpus.

### 3.2 The four claim classes, and what falsifies each

| Class | Falsified by | Example |
|---|---|---|
| **Empirical** | Observation of the world | "Behavioural ads increase session length" |
| **Procedural** | The process failing to operate as described | "Every page past review is flagged" |
| **Normative** | An argument, not an observation — so the falsifier is **reflective**: would the position survive its own reasoning applied consistently? | "A reader's attention is theirs" |
| **Definitional** | An instance the definition cannot classify | "A hub is a page with its own thesis" |

**Normative claims are the hard case and the estate does not pretend otherwise.** A value cannot be
refuted by measurement. What it can be tested against is **consistency**: whether the estate
applies it where it is expensive.
[MX-023 §7](../corpus/mx-023-attention-and-human-sovereignty.md) does this properly — its
falsifier 3 states that if readers, told plainly what a streak counter does, endorse it anyway at
scale, then the refusal *narrows*. That names the duty the estate expects to lose first, which is
the strongest form a normative falsifier can take.

---

## 4. Worked instance — a claim card for this standard

```
CLAIM      A claim published without a stated falsifier is unfalsifiable, and
           unfalsifiable claims accumulate into a corpus that cannot be corrected.
CLASS      procedural
BASIS      The estate's own position. Popperian in ancestry; not a citation to Popper,
           whose demarcation criterion concerned theories rather than documents.
EVIDENCE   E1 — reasoned position with an internal test, no external study
DECAY      durable, 12 months — review 2027-10-01
FALSIFIER  A corpus operating this standard for two years that proves no more
           correctable than a comparable corpus without it — measured by
           corrections accepted from external readers per published claim.
IF FALSE   ST-04 §2 narrows to empirical claims only; ST-24's mandatory Falsifier
           section becomes conditional; the six-rail model loses one rail.
```

**Two things this card discloses that prose would have hidden.** Its `BASIS` admits the position is
the estate's own and that the Popper lineage is ancestry, not authority — an honest use of
[ST-24 §8](st-24-page-prose-standard.md)'s third option, *"the estate's own position, unsupported by
external evidence."* And its `FALSIFIER` is **expensive**: two years and a comparison corpus. Under
§2.1 that makes it an *unreachable* falsifier, permitted only with the cost disclosed — which this
card does, and which a reader is entitled to weigh against the confidence of the surrounding
prose.

---

## 5. Failure modes

**The falsifier written last.** Appended after the argument, to satisfy the template. Signature:
it restates the claim's negation rather than naming an observation. *"This is wrong if pages are
not flagged"* is the claim inverted, not a test.

**Falsifier inflation.** Every sentence acquires one, until the section is noise and the
load-bearing falsifier is lost among fifteen trivial ones. One per page, at the claim that carries
the page.

**`IF FALSE` omitted.** The commonest real failure and the most consequential, because it is what
converts §E.5 from a duty into a sentiment.

**The normative claim given an empirical falsifier.** *"This is wrong if a study shows attention
capture increases learning."* Even if true, it would not refute the position that a reader's
attention is theirs — it would raise the cost of holding it. Category error, and it produces a
falsifier that cannot fire.

**The estate's own live failure.** ST-04 is a rail, and the build that would enforce it does not
run ([DEF-001](../00-governance-map/defect-register.md#def-001)). So the falsifier requirement is
met by whoever remembers it, and
[HX-002 §2](../harms/hx-002-harm-instrument-map.md) records HX‑02 as **`partial`** for exactly this
reason: *"an unenforced standard is a habit, not a mechanism."*

---

## 6. Limits

**Class: epistemic.** Falsifiability is a **necessary** condition for a checkable claim, not a
sufficient one. A well-formed falsifier can sit under a wrong claim, and a claim card cannot detect
a falsifier chosen because it will never fire.

**Class: technical.** Nothing here is automatable beyond section presence. Whether a falsifier is
*honest* requires reading, which is why [SITE-02 §9](../site/page-contract.md) automates only the
existence check and RB-05-style review carries the rest.

**Class: normative.** §3.2's treatment of normative claims — testing consistency rather than truth
— is a compromise. It cannot distinguish a value the estate holds from one it merely professes,
except by watching where the value costs something. MX-023's four implemented refusals and two
violations are the estate's own evidence in both directions.

**Class: governance.** This standard cannot make anyone check a falsifier. **Zero falsifiers have
been tested by an external reader**, because nothing is published — which makes the whole apparatus
currently unexercised.

---

## 7. Falsifier

*(Reproduced from §4's card, because a standard about falsifiers that hid its own would be
self-refuting.)*

This standard is wrong if a corpus operating it for two years proves no more correctable than a
comparable corpus without it, measured by external corrections accepted per published claim.

**A cheaper interim test.** Sixteen corrections stand in
[the log](../00-governance-map/corrections-log.md). **None was produced by a reader exercising a
published falsifier** — nine came from reading the estate's own code, four from the Curator, three
from cross-source reconciliation. If that stays true after publication and after external readers
arrive, the falsifier apparatus is decorative and this standard should narrow rather than be
defended.

---

## 8. Obligation

**For any author:** one falsifier per page, at the claim the page carries, satisfying all four
properties of §2 and none of the four counterfeits of §2.1. `IF FALSE` is not optional — a
falsifier that does not say what would change cannot be acted on.

**For a reviewer:** check the falsifier *first*. It is the fastest available test of whether the
author knew what they were claiming, and a bad falsifier under a good argument almost always means
the argument is doing something other than it appears.

**For the estate:** record the first §E.5 narrowing in
[Archive Register Class D](../00-governance-map/archive-register.md) when it comes. The most likely
first entry is already named: [MX-023 §7](../corpus/mx-023-attention-and-human-sovereignty.md)
falsifier 3.

**For a reader:** every substantive claim here names what would refute it. **Exercising one is the
most useful thing you can do to this corpus** — file at `/library/record/corrections-log/`, where
rejected submissions are published with reasons.

**Under ML-2.3:** §E.5 (narrowing and withdrawal on demonstrated falsification), §H.2 (epistemic
dependency), §H.16.3 (the all-clear presumption — a compliance analogue of this standard: a return
that cannot fail is evidence of theatre), §H.19 (authorship of record).

---

**Related:** [ST-05 Decay and Review Intervals](st-05-decay-and-review-intervals.md) ·
[ST-07 Evidence and VERIFY](st-07-evidence-and-verify.md) ·
[ST-24 Page Prose Standard](st-24-page-prose-standard.md) ·
[HX-001 Harm Audit Rubric](../harms/hx-001-harm-audit-rubric.md) ·
[Archive Register §5](../00-governance-map/archive-register.md) ·
[Corrections Log](../00-governance-map/corrections-log.md) · [ML-2.3](../license/ml-2-3.md)

*Curated by Maher. Four required properties, four counterfeits, seven claim-card fields — and
zero falsifiers exercised by any external reader, which is this standard's own most honest
number.*
