---
doc_id: "ST-24"
title_en: "Page Prose Standard — the Eight-Part Recipe and the Three Registers"
title_ar: "معيار نصوص الصفحات — الوصفة الثمانية والمستويات الثلاثة"
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
domain_tags: ["standards", "writing", "epistemics", "editorial"]
derived_from: "MX-NAV-SPEC v2026.10.1 §7"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# ST-24 · Page Prose Standard

**What this standard governs.** What a page in the `metax.academy` estate must *say*, and at what
altitudes. The [Page Contract](../site/page-contract.md) governs the container; the
[Route Manifest](../site/route-manifest.md) governs the address; this standard governs the
argument.

**Why it exists.** At 321 English routes and a 1200-word floor, the estate owes ≈385,000 words. A
volume that large is not written by exhortation. It is written against a recipe, and the quality
of the recipe determines the quality of the corpus more than the diligence of any individual
author does. This document is that recipe, plus the rules that stop it becoming a mould.

---

## 1. Position — where this standard sits

This standard is the operative half of the estate's academic claim. The
[Charter](../corpus/mx-000-charter.md) asserts that MetaX publishes checkable knowledge;
[ST-05](st-05-decay-and-review-intervals.md) asserts that claims expire; the
[harms register](../harms/) asserts that a body of knowledge published without a record and
without a falsifier damages the successor. None of those assertions reaches a reader except
through a page, and a page reaches a reader only through its prose. ST-24 is therefore where the
estate's epistemology either becomes operative or reveals itself as posture.

The parent instrument is the [Page Contract](../site/page-contract.md), which is deliberately
silent about argument. That silence is this standard's remit, and the division is strict: if a
requirement can be checked by a build step, it belongs in the contract's §9 checklist. If it
requires reading, it belongs here.

---

## 2. Definition — the eight-part recipe

Eight sections, each a `.reveal` block with an `<h2 class="section-title">` carrying exactly one
`.gradient-text` span. Word bands are **targets, not caps**.

| # | Section | Words | What it must contain |
|---:|---|---|---|
| 1 | **Position** | 120–180 | Where this sits in the estate and what question it answers. Names the parent hub in prose. |
| 2 | **Definition** | 150–220 | The term or object defined *operatively* — what would count as an instance, what would not. |
| 3 | **Mechanism** | 200–300 | How it works, in causal order. The academic core of the page. |
| 4 | **Worked instance** | 180–260 | One concrete case carried end to end. Named, dated, specific. |
| 5 | **Failure modes** | 150–220 | How it goes wrong in practice, with the signature by which you would notice. |
| 6 | **Limits** | 120–180 | What this page does not cover and cannot decide. Maps to a limit class. |
| 7 | **Falsifier** | 80–140 | The observation that would show this page's claim wrong. Stated as a test. |
| 8 | **Obligation** | 100–160 | What follows for the reader — duty, artefact or next gate. Cites an identifier. |

**Floors.** Leaf ≥1200. Hub 1400–1800, because a hub adds a **Map** section describing every
child in two to three sentences. Series 1400. Course 1200. Harm 1400. Lexicon entry 600.

### 2.1 The four sections that make a page checkable

Sections 1 through 5 are what a competent technical writer produces without instruction. Sections
**2, 6, 7 and 8** are the ones this standard exists to force, and each is a specific defence
against a specific failure.

**Definition, stated operatively.** Not "what the term means" but *what would count as an
instance, and what would not*. A definition that cannot exclude anything has not defined
anything, and the test is mechanical: name one thing a reader would plausibly think is an
instance and explain why it is not. Most encyclopaedic prose fails this and is not noticeably
worse for it — which is exactly why the requirement must be explicit here.

**Limits, mapped to a class.** Every Limits section names one of four classes — **epistemic**
(the knowledge is not available), **technical** (the capability does not exist), **ethical** (it
would be wrong), **economic** (nobody will pay for it). The classification is the point: an
epistemic limit and an economic limit are both "we don't do this," and conflating them lets an
estate present a business decision as a boundary of knowledge.

**Falsifier, stated as a test.** One sentence minimum, phrased as an observation. Not "this may
be wrong" but "if X is observed, this page is wrong." A page without a falsifier is not
necessarily false; it is *unfalsifiable*, which is a different and worse property for a document
claiming academic standing. [Falsifier grammar](../../docs/site/route-manifest.md) is routed at
`/method/epistemics/falsifier-grammar/`, and the estate's own falsifiers are collected at
`/license/harms/falsifiers/`.

**Obligation, citing an identifier.** The section must cite an `ML-2.3 §`, an `MX-` instrument or
a Method standard by identifier — not by name, not by description. The reason is the lattice
requirement of the [Page Contract §3](../site/page-contract.md): an obligation that cites nothing
is advice, and advice does not connect a page to the estate's governance.

---

## 3. Mechanism — the three registers

Every page must operate at three altitudes. The source's sentence is the clearest statement of
this standard's purpose: *"an agent producing only the middle one has produced a manual rather
than an academy page."*

| Register | Asks | Lives in |
|---|---|---|
| **Micro** | How does this work, concretely? | Sections 3 and 4 |
| **Meta** | What kind of knowledge is this? How does it decay? How could it be wrong? Who is answerable? | Sections 6, 7 and 8 |
| **Macro** | What does this do to attention, to labour, to the record, to the successor? | Section 1, and at least one paragraph of section 5 |

### 3.1 Why the macro register is mandatory and not decorative

A page about, say, `sitemap.xml` generation can be written entirely in the micro register and be
perfectly correct. The estate requires more, and the requirement is not stylistic ambition.

The four macro questions — attention, labour, the record, the successor — are the four axes of the
[harms register](../harms/), and the register is only operative if the estate's own pages are
written with it in mind. A curriculum that teaches search optimisation without asking what
optimisation does to the record is teaching a technique and concealing its cost. That is not a
hypothetical failure: it is the ordinary state of technical education, and correcting it is a
substantial part of why this estate exists.

The discipline is bounded, deliberately. One paragraph of section 5 and the framing of section 1 —
not an essay bolted onto every page. A macro register that consumes half of every page becomes
sermon, and sermon is the failure mode on the opposite side of the one this section guards
against.

### 3.2 The variation rule

**Vary which section leads.** A standards page may open on Definition. A harm page opens on the
macro frame. A series page opens on the worked instance. A page refusing a claim — like
`/credentials/ladder/completion-marker/` — may open on Limits.

The source states the reason and the consequence of omitting it: at 321 pages the failure mode
*"is not incompleteness but uniformity,"* and agents told only the recipe *"will all open on
Position."* This is written as a rule rather than as advice because it is the one requirement in
this standard that cannot be checked mechanically and will therefore be the first to erode.

---

## 4. Worked instance — the same object at three altitudes

Take `/method/rails/decay/`, the Decay-Awareness Rail.

**Micro.** Every claim in a lesson carries an evidence class and a review interval. `perishable`
claims — pricing, platform behaviour, API surfaces — carry a three-month interval; `semi-durable`
six; `durable` twelve. The rail is implemented as a front-matter field plus a build check that
flags any claim past its interval. A lesson failing the check does not publish.

**Meta.** This is a *procedural* claim, not an empirical one: the estate is asserting that its own
process has a property. Its evidence class is `durable`, because the procedure changes rarely.
Its falsifier is specific and cheap to run: if a page past its review interval is found published
and unflagged, the rail is not operating. Answerability sits with the build owner, named under
ML‑2.3 §H.19 — and note that the estate's own build pipeline does not currently run
([DEF-001](../00-governance-map/defect-register.md#def-001)), which means this rail is at present
an intention rather than a mechanism, and the page must say so.

**Macro.** The dominant publishing pattern of the machine-mediated web is the undated claim.
Content is published without a date, revised without a record, and surfaced by ranking systems
that reward freshness signals over actual currency — so a 2019 tutorial with a 2026 "updated"
stamp outranks a correct 2024 one. The consequence is a body of technical knowledge that cannot
be dated by the reader, which under HX‑12 is damage to the record and under HX‑20…HX‑25 damage to
the successor, who inherits a corpus they cannot audit. A decay interval published on the face of
every page is a refusal of that pattern, and it is refusable at almost no cost — which is what
makes its absence elsewhere a choice rather than a constraint.

That is one object, three altitudes, roughly 300 words. The recipe is not onerous once the habit
exists; it is onerous to *acquire*, which is why it is specified rather than assumed.

---

## 5. Failure modes

**Padding to reach the floor.** The most likely failure and the most damaging. From §0 of the
source: *"An agent that pads a page to hit a count has produced a worse artifact than an agent
that reported the page as thin."* Its signature is recognisable — sentences restating the
preceding sentence in different words, lists whose items differ only in phrasing, a Limits section
that says the page cannot decide things nobody asked it to decide. A padded page also destroys the
one number the estate can be held to, because a 1200-word count stops meaning anything once it
can be met by dilution.

**The bulleted page.** Prose and paragraphs, not bullet lists. Lists are permitted only for
genuine enumerations — the eleven academy requirements, the eight absolutes, the six rails — and
then each item runs **two sentences or more**. A page of bullets is a page whose author has
declined to state the relations between the items, and relations are the entire content of an
argument. This is the failure mode most likely to be produced by an agent, because bullets are
locally easier and globally empty.

**Micro-only.** Correct, useful, and a manual. Signature: no evidence class in the prose, no
falsifier that could fail, a Limits section listing features rather than boundaries of knowledge.

**Sermon.** The opposite failure, and the estate is more at risk of it than most because it holds
a harms register. Signature: the macro register colonising sections 2 through 4, moral vocabulary
substituting for mechanism, and a worked instance that is an illustration of a thesis rather than
a case that could have come out differently.

**The uncited number.** A statistic with no date and no `data-count-src`. Its signature is
confidence — "most developers," "the majority of sites," "roughly 40%" — and its cost is that a
reader cannot check it, which converts a factual claim into an authority claim.

**Marketing verbs.** *Unlock, supercharge, revolutionise, empower, seamless, cutting-edge,
game-changing* — forbidden outright. Also: no exclamation marks. Declarative sentences. Second
person for learners, third person for governance. The prohibition is not fastidiousness: these
verbs work by promising an outcome without specifying a mechanism, which is precisely the move
sections 2, 3 and 7 exist to prevent.

---

## 6. Limits

**Class: epistemic.** This standard cannot make a page true. Eight well-formed sections can carry
a wrong claim, and the falsifier requirement helps only if the falsifier is honest — a
deliberately unfalsifiable falsifier ("this page is wrong if the estate's entire method is wrong")
satisfies the letter and defeats the purpose.

**Class: technical.** Almost nothing here is machine-checkable. Section presence and word count
are; register coverage, definitional adequacy, falsifier honesty and the variation rule are not.
The [Page Contract §9](../site/page-contract.md) checklist deliberately contains only the
checkable subset, and this standard's compliance therefore rests on review rather than on build.

**Class: ethical.** This standard does not decide who writes. At ≈385,000 words the authorship
question is
[RAT-21](../00-governance-map/open-questions-and-ratifications.md#rat-21), and ML‑2.3 §H.19 and
§H.25 both bear on it. A recipe good enough to produce publishable prose at volume is also a
recipe good enough to produce prose nobody thought about, and this document cannot tell the
difference.

**Class: economic.** It sets no schedule and budgets no cost.

---

## 7. Falsifier

This standard is wrong if either of the following is observed.

**A page that satisfies all eight sections, all three registers and the variation rule is
nonetheless not worth publishing.** That would show the recipe to be insufficient rather than
merely necessary, and the correct response would be to add a section, not to raise the floor.

**Or: a page that omits a section is nonetheless clearly better for the omission.** The estate
should watch section 4 in particular. A page defining a notation convention may have no
non-trivial worked instance, and forcing one produces an invented example — which is padding
wearing the costume of rigour. If that pattern recurs across more than a handful of pages,
section 4 should become conditional, and the change belongs in the changelog rather than in
quiet local exceptions.

---

## 8. Obligation

**For the author or agent:** eight sections, three registers, a lead section chosen for the page
rather than the template. Where the floor cannot be met honestly, declare
`<meta name="mx-thin" content="true">`, write to natural length, and file under
[DEF‑2026‑043](../00-governance-map/defect-register.md#def-2026-043) with a stated reason per page.
Never pad. Every number carries a date or a `data-count-src`; every status carries a gate
condition and a review date; every claim carries either a citation or an explicit mark as the
estate's own position — that third option is legitimate and under-used, and *"the estate's own
position, unsupported by external evidence"* is an honest sentence.

**For the reviewer:** read for the meta and macro registers first. They are the two an agent
omits, they are the two a build cannot detect, and their absence is what turns an academy into a
manual.

**For the estate:** the six thin-by-nature classes are named and closed —
`/about/legal/cookies/`, `/about/legal/sitemap/`, `/credentials/verify/revocations/`,
`/library/sources/schemas/`, `/library/sources/downloads/`, and every lexicon entry. Adding a
seventh requires a stated reason in the defect register, because the estate cannot publish a
register naming compliance theatre *"while committing it on thirty pages"* — and it equally cannot
let the exemption list grow until the floor means nothing.

---

**Related:** [Page Contract](../site/page-contract.md) ·
[Route Manifest](../site/route-manifest.md) ·
[ST-05 Decay and Review Intervals](st-05-decay-and-review-intervals.md) ·
[HX-000 Structural Harms](../harms/) · [ML-2.3](../license/ml-2-3.md) ·
[Defect Register](../00-governance-map/defect-register.md)

*Curated by Maher. Eight sections, three registers, one variation rule — and the variation rule is
the only one that cannot be checked, which is why it will be the first to go.*
