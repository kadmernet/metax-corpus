---
doc_id: "ST-05"
title_en: "Decay Classes and Review Intervals"
title_ar: "أصناف التلاشي وفترات المراجعة"
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
domain_tags: ["standards", "decay", "epistemics", "review"]
route: "/method/epistemics/decay-standard/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# ST-05 · Decay Classes and Review Intervals

**What this standard governs.** How fast a claim in this estate goes stale, how that is declared,
and what the estate owes a reader when a review date passes.

**The claim it rests on.** A technical claim has a **half-life**, and publishing it without one is
a defect. Not because the claim is wrong, but because a reader cannot weight it: an undated,
un-classed assertion about a platform limit and a durable statement of principle look identical on
a page, and only one of them will still be true next year.

---

## 1. Position

This is the operative half of the estate's epistemology. [ST-04](st-04-falsifiability-and-claim-cards.md)
requires every substantive claim to state what would refute it; ST-05 requires it to state **how
long it is expected to survive**. The two together are what distinguish a claim from an assertion,
and both are enforced through [ST-02](st-02-front-matter-schema.md)'s `evidence_class` and
`review_interval_months` fields.

Published at `/method/epistemics/decay-standard/`, and it is the reason
[SITE-02 §2](../site/page-contract.md) puts the evidence class and review date in the
`.mx-pagestamp` on **every page** rather than in a colophon.

**The macro frame.** The dominant publishing pattern of the machine-mediated web is the **undated
claim**. Content is published without a date, revised without a record, and ranked by systems that
reward freshness *signals* over actual currency — so a 2019 tutorial carrying a 2026 "updated"
stamp outranks a correct 2024 one. The result is a body of technical knowledge a reader cannot
date, which under **HX‑12** is damage to the record and under **HX‑14** is temporal foreclosure.
A decay interval on the face of every page is a refusal of that pattern, and it is refusable at
almost no cost — which is what makes its absence elsewhere a choice rather than a constraint.

---

## 2. Definition — the three classes

| Class | Interval | What it means | Typical subject |
|---|---:|---|---|
| **durable** | 12 months | Change requires a change of position or principle | Charter, licence, this standard, ST-01 |
| **semi-durable** | 6 months | Changes as the estate's own structure changes | Route manifest, DS-07, designation list |
| **perishable** | 3 months | Changes without the estate acting at all | Defect register, ST-22's platform limits, the demo notice |

**The class is chosen by asking one question:** *what would make this wrong, and does it require
anyone to act?*

If only a change of the estate's own position could falsify it → **durable**. If a change to the
estate's structure would → **semi-durable**. If it can become false while nobody touches
anything → **perishable**.

### 2.1 Why `perishable` is the honest default for anything observed

The class most often mis-assigned is `perishable`, and the failure is always in the same direction:
authors mark observations `durable` because the *observation* felt solid.

**A claim about a live system is never durable.** It decays the moment the code changes. The estate
learned this expensively — the [Corrections Log §Method](../00-governance-map/corrections-log.md#method-what-this-log-has-learned)
records that it *"has been writing them as though they were durable,"* and the remedy adopted there
is a standing obligation restated in §4 below.

---

## 3. Mechanism — what a passed review date means

**A document past its review date is `stale`.** It is not withdrawn, not non-governing, and not
presumed wrong. It is **flagged**, and three obligations follow.

**On the page.** The `.mx-pagestamp` renders the stale state visibly. A reader must not have to
compute `last_reviewed + review_interval_months` themselves.

**For a machine reader.** [GM-11 §3](../00-governance-map/machine-reading-contract.md) makes this
one of six signals a machine reader may rely on, and staleness is **arithmetic a machine does and a
human usually does not** — one of the few places a machine reader should outperform. Condition 3 of
that contract requires the stale state be preserved in any quotation.

**For the reviewer.** A review either records movement or **records that there was none**, with
the date. That second half is the load-bearing part: a review producing no change must still be
recorded, because an unrecorded review is indistinguishable from a skipped one.

### 3.1 The review that changes nothing is still a review

The estate's cadence rule, inherited from the
[Open Questions](../00-governance-map/open-questions-and-ratifications.md) file: *"Each review
either records movement or records that there was none, with the date."*

This is not bureaucracy. It is the only way to distinguish **checked and unchanged** from
**not checked** — and those two states look identical in every corpus that does not insist on the
distinction. A reader encountering a two-year-old durable instrument needs to know whether it has
been re-read twice and confirmed, or written once and forgotten.

---

## 4. Provenance of purpose — the amendment this standard acquired

**Every claim about a live artefact must record `demo`, `staging` or `production` alongside its
date.**

This was added in v2026.10.1 following
[C-14](../00-governance-map/corrections-log.md#c-14) and filed as
[DEF-024](../00-governance-map/defect-register.md#def-024). The estate had published **nine claims
about its own running code** — ad networks live, no JavaScript render, flat-file routes, nine
ambient animations — every one true of the bytes read, every one written as a finding about *the
estate*. The subject was a **prototype**.

**Why this belongs in the decay standard rather than only in the schema.** Provenance of purpose is
a **decay parameter**, not merely a label. A claim about a demo decays differently from a claim
about production: the demo's copy is *scheduled to be replaced*, so a finding about it has a known
expiry that a production finding does not. Mislabelling the two therefore corrupts the interval,
not just the description.

The lesson the standard now carries on its face:

> Reading an artefact tells you what is there. It cannot tell you what the artefact is **for**.

Nine claims. None false. All nine unlabelled — which is the subtler defect and the one no
consistency check will ever raise.

---

## 5. Worked instance — three claims about the same subject

Take the estate's advertising arrangements.

**Claim A: "Behavioural advertising engages HX‑01 and HX‑04."** A statement about how the harms
register applies to a practice. Only a change of position or a narrowing under §E.5 could falsify
it. → **`durable`, 12 months.**

**Claim B: "Ad slots run on the content plane, contradicting MX-009."** A statement about the
estate's own structure. It becomes false the moment the Curator removes the slots — an act by the
estate. → **`semi-durable`, 6 months**, and `provenance_of_purpose: demo`, because the observed
artefact is a prototype.

**Claim C: "AdSense publisher `ca-pub-4463113802541266`, three slots, plus one Adsterra slot."** A
statement about a third party's configuration. It can become false without anyone at MetaX acting
— a network changes its tag format, a slot is disabled upstream. → **`perishable`, 3 months.**

**What the worked instance shows.** One subject, three claims, three classes. A document asserting
all three at `durable` — which is what the estate's earlier defect entries effectively did — is
making a twelve-month promise about a third party's configuration it does not control. The class
is not a property of the topic. It is a property of **what would have to happen for the sentence to
become false**.

---

## 6. Failure modes

**`durable` as the path of least resistance.** Twelve-month review is the least demanding
commitment, so it is what an author under pressure selects. Signature: a corpus where nearly
everything is durable and the review queue is permanently empty.

**The write date entered as the review date.** Writing is not reviewing. Undetectable from the
front matter, and it corrodes every staleness computation downstream.

**Silent staleness.** A perishable document eighteen months past review, rendering as though
current, because nothing computes the arithmetic. This is the estate's live condition —
[ST-22 §7](st-22-platform-and-persistence.md) says so of its own capacity figures.

**Class inherited by copy-paste.** A new instrument copies a neighbour's block, including its class
and review date. [ST-02 §5](st-02-front-matter-schema.md) names the same failure.

**Interval/class mismatch.** `perishable` with a twelve-month interval — an assertion that
something decays fast and need not be checked.

**Treating stale as wrong.** The inverse failure, and it matters because it makes the flag
expensive. A stale durable instrument is very probably still correct; the flag says *nobody has
confirmed it*, not *do not rely on it*. An estate that treats staleness as invalidity will stop
flagging.

---

## 7. Limits

**Class: technical, and it is binding.** **No mechanism computes staleness.** The check would live
in [SENTINEL](st-13-static-build-and-sentinel.md), which does not run
([DEF-001](../00-governance-map/defect-register.md#def-001)). So this standard's central operative
requirement — that a passed review date be visible — is currently unenforced, and the
`.mx-pagestamp` that would render it exists in [SITE-02](../site/page-contract.md) and on no page.

**Class: epistemic.** Three classes is a coarse instrument. Real half-lives are continuous, and
the estate has no evidence that twelve/six/three months are the right cut points — they are
asserted from judgement. A claim decaying in six weeks has no home here.

**Class: governance.** The standard cannot make reviews happen. Thirteen `[VERIFY]` claims are open
and **none has ever been closed** ([DEF-030](../00-governance-map/defect-register.md#def-030)),
which is the best available evidence that intervals declared are not intervals honoured.

---

## 8. Falsifier

This standard is wrong if:

1. **A claim's real half-life falls outside all three classes** in a way that matters — showing the
   three-class model under-inclusive rather than merely coarse.
2. **Two competent authors assign different classes to the same claim** using §2's test, showing
   the test too vague to be a procedure.
3. **Stale flags prove to be ignored in practice** once rendered, showing the mechanism social
   rather than epistemic.
4. **The estate's own review cadence stays empty for a year** while intervals are declared
   throughout the corpus. That would falsify not the classes but the estate's claim to operate
   them — and it is the falsifier currently closest to firing.

---

## 9. Obligation

**For any author:** choose the class by §2's test, not by convenience. Set `last_reviewed` only
when a review happened. Where the claim concerns a live artefact, record
`provenance_of_purpose` (§4).

**For any reviewer:** record the review even when nothing changed, with the date. A review with no
record did not happen.

**For the estate:** build the staleness computation. Until it runs, every `review_interval_months`
in the corpus is a promise with no mechanism — which is
[HX-002 §8](../harms/hx-002-harm-instrument-map.md)'s recurring finding, arriving again.

**For a machine reader:** compute `last_reviewed + review_interval_months` and **report a stale
document as stale**, per [GM-11 §5](../00-governance-map/machine-reading-contract.md). The estate
does not yet do this for you, and the arithmetic is the cheapest correction anyone can make to
this corpus.

**Under ML-2.3:** §H.12 (harm to the record), §H.14 (temporal foreclosure), §H.4 (optimisation
disclosure), §E.5 (narrowing or withdrawal on falsification — the mechanism a review may trigger),
§H.26 (corpus hygiene).

---

**Related:** [ST-04 Falsifiability and Claim Cards](st-04-falsifiability-and-claim-cards.md) ·
[ST-02 Front-Matter Schema](st-02-front-matter-schema.md) ·
[ST-07 Evidence and VERIFY](st-07-evidence-and-verify.md) ·
[SITE-02 Page Contract](../site/page-contract.md) ·
[Verification Log](../00-governance-map/verification-log.md) ·
[Machine Reading Contract](../00-governance-map/machine-reading-contract.md)

*Curated by Maher. Three classes, three intervals, one amendment forced by nine unlabelled claims
— and no mechanism yet computes any of it, which makes every interval in this corpus a promise
rather than a check.*
