---
doc_id: "ST-06"
title_en: "The Objections Standard"
title_ar: "معيار الاعتراضات"
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
domain_tags: ["standards", "objections", "criticism", "epistemics"]
route: "/license/falsification/objections/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# ST-06 · The Objections Standard

**What this standard governs.** How this estate handles the strongest available argument against
each of its own positions: where the objection must be stated, who must state it, and what counts
as an answer.

**The rule that makes it more than a gesture.** An objection is stated **in the voice of someone
who holds it**, at its strongest, *before* the reply. A position that has never been written down
in its opponent's own terms has not been tested — it has been summarised by the party it
threatens.

---

## 1. Position

[ST-04](st-04-falsifiability-and-claim-cards.md) requires every claim to state the observation
that would refute it. That handles **empirical** exposure. It does nothing about **argumentative**
exposure, which is the more common way a governance position fails: not refuted by evidence, but
outreasoned by an objection nobody in the estate had honestly confronted.

ST-06 is the other half of that apparatus. Published at `/license/falsification/objections/` —
inside the group hub the licence devotes to its own falsification, alongside withdrawals, defects
and open questions.

Its siblings: [MX-016](../corpus/mx-016-appeals-and-due-process.md) handles a grievance about a
**decision**; the [Corrections Log](../00-governance-map/corrections-log.md) handles a claim found
**wrong**; this standard handles a **disagreement about a position** that may be perfectly
informed and still opposed.

**The macro register.** An institution publishing at volume acquires an asymmetry: it has the
platform, the vocabulary, the identifiers and the last word. Under **HX‑06** (erosion of the
deliberative commons) the harm is not censorship but **crowding** — the institution's framing
becomes the only framing available, and dissent has to be conducted in terms the institution
chose. Steel-manning an objection **in the objector's own vocabulary** is the cheapest structural
correction, and it costs the author precisely what it is worth: the discomfort of writing the best
case against themselves.

---

## 2. Definition — what a stated objection must contain

Four properties, all required. Three of them are about *whose* words are used.

**1. Attributable.** A named holder — a person, a school of thought, a discipline. *"Some would
argue"* is the author arguing with themselves. If no one actually holds it, it is not an objection;
it is a rhetorical convenience.

**2. In the objector's vocabulary.** Stated in the terms the objector would use, not translated
into the estate's. Translating an objection into the framework it attacks is how it gets answered
without being met.

**3. At its strongest available form.** Not the weakest version that is easy to answer. Where
several versions exist, the strongest is stated — and if the estate cannot answer the strongest, §4
applies.

**4. Prior to the reply.** The objection is written first, in full, and can be read on its own. A
reply woven through an objection prevents a reader from assessing the objection independently.

### 2.1 The four counterfeits

Each passes casual reading. The estate names them because it has committed at least two.

**The straw objection.** *"Critics say governance documents are boring."* Answerable, unheld, and
its presence suggests the real objection was avoided.

**The pre-answered objection.** Stated with its refutation embedded — *"one might object X, though
this ignores Y."* Property 4 forbids it.

**The objection to a weaker claim.** The estate states a strong position, then answers an objection
to a moderate version of it.

**The deferred objection.** *"This is addressed in the Limits section."* A limit is what a position
does not cover; an objection is an argument that the position is **wrong where it does cover**.
Different things.

---

## 3. Mechanism — the record

```
OBJECTION   [stated in full, in the objector's terms]
HELD BY     [named person, school, or discipline]
STRENGTH    [strong | partial | weak] — the estate's own assessment
REPLY       [or: "no adequate reply — see disposition"]
DISPOSITION [answered | narrowed | conceded | open]
RECORDED    [date]
```

### 3.1 The four dispositions, and why two of them are the point

**`answered`** — the estate believes the objection fails, and says why.

**`narrowed`** — the objection is partly right, and **the estate's position has changed in
consequence.** Under [ML-2.3 §E.5](../license/ml-2-3.md) a narrowing is recorded in
[Archive Register Class D](../00-governance-map/archive-register.md), which is **currently empty.**

**`conceded`** — the objection is right and the position is withdrawn.

**`open`** — the objection stands unanswered and the estate is publishing it anyway.

**`open` is the disposition this whole standard exists to make available.** An estate that can only
publish objections it has defeated has a rhetorical device, not a standard. The ability to write
*"this is the best argument against our position and we do not have an answer"* is what
distinguishes the two, and it is the reason the objections route sits under
`/license/falsification/` rather than in an FAQ.

**A register with no `narrowed` or `conceded` entries is presumptively decorative** — the same
structure as [§H.16.3](../license/ml-2-3.md)'s all-clear presumption, and the same reasoning: a
process in which the institution always wins is not a process.

---

## 4. Worked instance — the strongest objection to this estate's method

Written to the standard, because a standard about steel-manning that did not steel-man itself would
be self-refuting.

```
OBJECTION   The whole apparatus is elaborate self-flattery. A governance corpus that
            publishes its own defect register, corrections log and unremedied harms has
            discovered that confession is cheaper than reform. Every unflattering
            disclosure buys credibility while the underlying conduct — behavioural ad
            networks on the content plane, an inaccessible interface, no working build —
            continues unchanged. The estate has 33 defects, 16 corrections, 23 open
            questions, three harms it admits committing, and zero duties ever narrowed.
            Its output is documents about documents. Judged by what it has actually
            built rather than what it has written about building, it is a demo with
            ad slots and a very large amount of prose. The confession apparatus is not
            evidence of integrity; it is the product.
HELD BY     The standard critique of institutional ethics-washing — Sarah Bell and
            others on "ethics theatre"; the same objection made against corporate
            responsibility reporting generally, and against AI ethics boards specifically.
STRENGTH    strong
REPLY       Partial, and the estate does not claim more. Three points hold. First,
            the mechanism is falsifiable in a way ethics-washing is not: the estate
            published the exact test — zero narrowings means doctrine, not register —
            and that number is public, checkable, and currently zero. Second, the
            disclosures have costs the confession thesis does not predict: refusing to
            reconstruct ML-2.2 leaves a permanent gap on the face of the Tier 1
            instrument, and RB-05 returns RETURNED against the estate's own work.
            Third, several commitments are structural rather than declarative —
            forbidden schema columns, an append-only redirect record, the correction
            obligation placed beyond the Curator — and structural commitments cost
            something to reverse.
            What the reply does NOT establish: that the conduct will change. On the
            objection's central point — that confession has so far substituted for
            reform — the estate has no answer, because the ad slots are still running
            and the reduced-motion block is still unshipped.
DISPOSITION open
RECORDED    2026-10-01
```

**Why this is filed `open` rather than `answered`.** The objection's core claim is about **what
happens next**, and the estate cannot answer it with a document. It is answered by removing the ad
slots, shipping three lines of CSS, and recording the first narrowing — or it is not answered at
all. **Publishing the objection as open is the only honest disposition available today**, and it is
precisely the case §3.1 was built to accommodate.

---

## 5. Failure modes

**The objection nobody holds.** §2.1's straw. Signature: no attributable holder.

**Steel-manning as performance.** A strong objection stated well, filed `answered`, with a reply
that does not engage its strongest part. Harder to detect than a straw objection and more
damaging, because it looks like exactly what this standard requires.

**`open` never used.** If every objection resolves to `answered`, the standard has become the
rhetorical device it was built to prevent.

**The objection answered by a limit.** §2.1's fourth counterfeit.

**Objections curated for answerability.** Selecting which objections to state by how well they can
be replied to. The control is that the objections route is **open to filing by anyone**, and
rejected filings are published with reasons
([MX-013 Rule 3](../corpus/mx-013-records-and-versioning.md)).

---

## 6. Limits

**Class: structural.** The estate selects, states and assesses the objections against itself. Even
performed honestly, that is an author grading their own opponent. The only real correction is
external filing, and **no external objection has ever been filed** because nothing is published.

**Class: epistemic.** `STRENGTH` is the estate's own judgement. An objection the estate cannot
perceive as strong will be recorded as partial, and nothing in the standard detects that.

**Class: practical.** **One objection is on the record** — §4's. A standard with a single worked
instance, authored by its subject, is a specification rather than a practice.

**Class: reflexive.** §4's objection applies to this standard. A standard requiring the estate to
publish the best case against itself is itself the kind of disclosure the objection identifies as
cheap. The estate cannot escape that circle by writing more; only by the conduct §4's reply admits
it has not yet changed.

---

## 7. Falsifier

1. **An objection stated to all four properties that is nonetheless not the strongest form** —
   showing §2 insufficient to prevent the subtler counterfeit.
2. **Every objection resolving to `answered` over a year**, showing the disposition set
   decorative. Checkable, and **the estate's current single entry is `open`**, which is the one
   piece of evidence pointing the other way.
3. **External objections, once invited, proving systematically stronger than the estate's
   self-generated ones** — falsifying §2's premise that an author can state the case against
   themselves at full strength. **The estate expects this to fire** and says so.
4. **Class D remaining empty after external objections are filed.** That is §4's objection
   vindicated, and it would falsify the estate's claim to operate a register rather than a
   doctrine.

---

## 8. Obligation

**For any author of a substantive position:** state the strongest objection, attribute it, use the
objector's vocabulary, place it before your reply. Where you have no adequate reply, file `open` —
that is a permitted and respectable outcome, and using it is what makes the `answered` entries
worth anything.

**For the estate:** invite external objections at publication, publish rejected filings with
reasons, and record the first `narrowed` disposition when it comes. **Class D is empty and §4's
objection is open**; both are answered by conduct, not by further documents.

**For a reader:** the objection in §4 is the estate's own best case against itself, filed unanswered
on its central point. If you can strengthen it, that is more useful to this corpus than agreement,
and the route is `/license/falsification/objections/`.

**Under ML-2.3:** §H.06 (erosion of the deliberative commons), §H.15 (compliance theatre — §4's
objection is its direct application to this estate), §H.17 (non-theatre), §E.5 (narrowing on
demonstrated falsification), §H.19 (authorship of record).

---

**Related:** [ST-04 Falsifiability and Claim Cards](st-04-falsifiability-and-claim-cards.md) ·
[ST-07 Evidence and VERIFY](st-07-evidence-and-verify.md) ·
[MX-016 Appeals and Due Process](../corpus/mx-016-appeals-and-due-process.md) ·
[Corrections Log](../00-governance-map/corrections-log.md) ·
[Archive Register §5](../00-governance-map/archive-register.md) ·
[HX-002 Harm → Instrument Map](../harms/hx-002-harm-instrument-map.md) · [ML-2.3](../license/ml-2-3.md)

*Curated by Maher. Four required properties, four counterfeits, four dispositions — and the
estate's own strongest objection to itself is filed `open`, because the reply that would close it
is conduct rather than prose.*
