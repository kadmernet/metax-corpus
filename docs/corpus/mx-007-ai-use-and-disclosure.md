---
doc_id: "MX-007"
title_en: "AI Use and Disclosure"
title_ar: "استخدام الذكاء الاصطناعي والإفصاح عنه"
family: "corpus"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 2
depth: 5
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["corpus", "ai", "disclosure", "authorship"]
route: "/about/policy/ai-policy/"
provenance_of_purpose: "specification"
authorship_note: "Drafted by an AI system. See §5."
hreflang: "en, ar"
---

# MX-007 · AI Use and Disclosure

**What this instrument governs.** Where AI systems may be used in producing this estate, what must
be disclosed when they are, and what may never be delegated to them.

**The disclosure this instrument owes before anything else.** **Substantially all of this corpus
was drafted by an AI system, including this instrument.** Its front matter carries
`authorship_note` for that reason, and §5 states what follows from it. A policy on AI disclosure
that concealed its own authorship would be self-refuting in the first sentence.

---

## 1. Position

Nearly every organisation now writes an AI policy, and nearly all of them are addressed outward —
to users, about a product. This one is addressed **inward**: it governs how the estate produces
its own instruments, because that is where the estate's AI use actually is.

The governing constraint is [ML-2.3 §H.19](../license/ml-2-3.md), **authorship of record**: an
assertion issued in the estate's name requires a recorded natural author. Its companion is §H.25,
**agent constraint**, and §H.29, **substitution disclosure** — what human activity was replaced, and
for whom.

Its published route is `/about/policy/ai-policy/`, shared with
[MX-023](mx-023-attention-and-human-sovereignty.md), and its enforcement surface is
[ST-02 §3.2](../standards/st-02-front-matter-schema.md)'s `authorship_note` field.

**The macro register.** The question this instrument exists to keep open is not whether AI writing
is good enough. It is what an institution is claiming when it publishes at volume. Under **HX‑09**
(labour displacement without transfer) and **HX‑19** (authorship of record), an estate that
publishes 385,000 words of agent-drafted prose under its own name is making a claim about what it
has **thought about** — and the gap between *published* and *thought about* is the thing this
policy is built to keep visible.

---

## 2. Definition — the four use classes

| Class | What the AI does | Disclosure |
|---|---|---|
| **A · Drafting** | Produces prose the estate then adopts | `authorship_note` on the instrument |
| **B · Transformation** | Reformats, summarises, translates existing estate text | Noted where the output is published |
| **C · Analysis** | Reads and reports — reconciliation, link-checking, defect-finding | Recorded in the register it feeds |
| **D · Generation at volume** | Produces routed pages from a specification | **Per-page disclosure**, plus §4's gate |

**Class D is the one with teeth**, because it is the only class where the estate could plausibly
publish more than it has read. A single agent-drafted instrument is reviewed by the Curator
sentence by sentence; 321 agent-drafted pages cannot be, and the honest response is a mechanism
rather than a promise.

### 2.1 What AI may never do

Five prohibitions, none subject to disclosure as a cure. Disclosure makes a permitted act
transparent; it does not make a prohibited act permissible.

**Decide anything reserved to the Curator.** The [open questions](../00-governance-map/open-questions-and-ratifications.md)
file exists because some determinations require the person who owns them. An agent may draft
options and state a recommendation; it may not choose.

**Issue a Part H Statement.** [ML-2.3 §H.16.4](../license/ml-2-3.md) requires a **natural person**.
A department cannot sign one and neither can a model.

**Fabricate a source, a citation, a superseded text or a version.** This is the estate's cardinal
fault. It is why [the version history §3](../license/version-history.md) refuses to reconstruct
ML-2.2 and why [DEF-029](../00-governance-map/defect-register.md#def-029) refuses to reconstruct
the lost nav spec — *"fabricating a record inside the instrument that defines Ṣidq."*

**Resolve a same-tier conflict by choosing.**
[GM-01 §2](../00-governance-map/precedence-and-conflict-rules.md) rule 4: an unresolvable conflict
is a defect to be filed, never a preference to be exercised.

**Enlarge the estate on its own authority.** An agent may propose structure and must label the
proposal as its own. `Method` as a ninth pillar is the live case — *"my addition, not yours"* —
adopted provisionally and filed as
[RAT-19](../00-governance-map/open-questions-and-ratifications.md#rat-19).

---

## 3. Mechanism — the disclosure form

```
authorship_note: "[what the AI produced] · [what a human did] · [what remains unreviewed]"
```

Three parts, and the **third is the one that carries information**. "Drafted by an AI system,
reviewed by the Curator" tells a reader nothing about depth. "Drafted by an AI system; the Curator
supplied the source material and has not reviewed §§4–7" tells them where to be sceptical.

**Three live instances, each of which cost something:**

**HX-000** — harms H1–H11 are the documentation agent's; Strata V and VI arrived with the
Curator's ML-2.3 text. Disclosed at [C-11](../00-governance-map/corrections-log.md#c-11), because
§H.19 *"won't let me present two voices as one."*

**[ST-23](../standards/st-23-affiliate-and-referral.md)** — `"Designed from scratch. No supplied
source contains an affiliate system."` The only instrument in the corpus with **no upstream
source**, which is why [RAT-23](../00-governance-map/open-questions-and-ratifications.md#rat-23)
asks whether an agent-designed commercial instrument should govern by default.

**The nav spec's ninth pillar** — proposed by an agent, labelled as such, with the cost of refusing
it stated.

**A duty that never embarrasses its holder is not operating.** The field's value is measured by how
often it produces an admission nobody wanted to make.

---

## 4. The volume gate

Class D — generation at scale — is permitted only under four conditions. They exist because
[RAT-21](../00-governance-map/open-questions-and-ratifications.md#rat-21) asks whether ≈385,000
English words plus an Arabic mirror can honestly be published under the estate's name, and this
section is the part of the answer that does not require the Curator.

**1. The specification precedes the generation.** A page is generated against
[ST-24](../standards/st-24-page-prose-standard.md)'s eight-part recipe and
[SITE-02](../site/page-contract.md)'s twenty acceptance lines, not free-written. A specification is
reviewable in a way that 321 pages are not.

**2. No page is emitted for content that does not exist.** *"Emitting a 1,200-word page for an
unwritten course is HX‑15 in miniature"* ([SITE-01 §6.2](../site/route-manifest.md)). Course routes
are generated **only** for series badged `live`.

**3. Nothing is padded to a floor.** *"An agent that pads a page to hit a count has produced a
worse artifact than an agent that reported the page as thin."* Six page classes are exempt by name
under [DEF‑2026‑043](../00-governance-map/defect-register.md#def-2026-043).

**4. Per-page disclosure, and the count is published.** A reader may see how much of what they are
reading was agent-drafted, at the page and in aggregate.

### 4.1 What the gate cannot do

It cannot detect **uniformity**. The failure mode at volume *"is not incompleteness but
uniformity — 321 pages that all sound like the same eight-section template,"* and no automated
check finds it. ST-24 §3.2's variation rule is the mitigation and is explicitly **the one
requirement that cannot be checked mechanically and will therefore be the first to erode.**

Nor can it answer RAT-21's real question: whether an estate that publishes 770,000 agent-drafted
words has *thought about* them. That is the Curator's, and this instrument's honest contribution is
to keep the question visible rather than to settle it.

---

## 5. This instrument's own disclosure

**Drafted by an AI system.** So were MX-009, MX-010, MX-023, MX-024, ST-01, ST-02, ST-04, ST-05,
ST-07, ST-13, ST-22, ST-23, ST-24, SITE-01 through SITE-04, DS-07, HX-001, HX-002, RB-05, the
licence companions, and the four governance-map instruments written this session.

**What a human did.** The Curator supplied every source document, the licence text including all
of Part H, the site design, the navigation specification, and the four §0 corrections that
invalidated a release of the estate's own work. He also supplied the two corrections no machine
could have produced: **the name of the estate's own subject**, and **the fact that the live site is
a demo** ([C-13](../00-governance-map/corrections-log.md#c-13),
[C-14](../00-governance-map/corrections-log.md#c-14)).

**What remains unreviewed.** Most of it, clause by clause. `counsel_reviewed: false` appears
throughout, and the [Verification Log](../00-governance-map/verification-log.md) carries thirteen
open claims with none closed.

**The reflexive limit, stated because it is real rather than as a formality.** An agent specifying
how agents may be used is not a disinterested party. This is the same limit
[GM-11 §6](../00-governance-map/machine-reading-contract.md) records about the machine-reading
contract, and a reader should weight §§2–4 accordingly. **The estate would rather that scepticism
than its absence.**

---

## 6. Failure modes

**Disclosure without depth.** "AI-assisted" on everything, which conveys nothing. §3's three-part
form exists to force the third part.

**The specification that launders the output.** Generating against a spec and treating the spec's
review as review of the pages. A reviewed specification plus unreviewed output is unreviewed
output with an audit trail.

**Fabrication under pressure to complete.** An agent asked to finish a document with a missing
source will produce something plausible. The estate has refused this twice —
ML-2.2 and the lost nav spec — and **both refusals left visible gaps**, which is what refusal
looks like when it is real.

**Recommendation presented as determination.** An agent stating a preference in the register's
voice rather than as its own recommendation. The nav spec's *"I would keep the nine and move the
breakpoint"* is the correct form: recommendation, labelled, unexecuted.

**The uniformity nobody notices.** §4.1. The failure that arrives only at volume and that this
instrument cannot detect.

---

## 7. Limits

**Class: reflexive.** §5. An AI-drafted policy on AI use, specified by the party it constrains.

**Class: technical.** No mechanism enforces disclosure. `authorship_note` is checked by
[SENTINEL](../standards/st-13-static-build-and-sentinel.md), which does not run
([DEF-001](../00-governance-map/defect-register.md#def-001)), so §3 is honoured by whoever
remembers it.

**Class: epistemic.** The estate cannot measure what §4 is for. There is no test distinguishing a
page an institution has *thought about* from one it has merely published, and this instrument
substitutes procedure for that missing test.

**Class: governance.** §2.1's five prohibitions bind an agent that intends to comply. They are not
enforceable against one that does not, and the estate's protection is that every instrument names
a human curator and every determination is public.

---

## 8. Falsifier

1. **An agent-drafted instrument indistinguishable in quality from a human-drafted one, where the
   disclosure changed no reader's assessment** — falsifying disclosure's value rather than its
   honesty.
2. **§4's four conditions satisfied by a generation run that nonetheless produces 321 uniform
   pages** — falsifying the gate as sufficient. **The likeliest**, since §4.1 admits the gate
   cannot see uniformity.
3. **A prohibited act in §2.1 occurring and being detected by something other than self-report** —
   which would show the estate has an enforcement mechanism it does not believe it has.
4. **The estate publishing at volume and no reader caring about authorship**, falsifying §1's
   premise that the *published / thought about* gap matters.

---

## 9. Obligation

**For any agent working on this estate:** disclose in the three-part form. Label proposals as your
own. Refuse the five prohibitions in §2.1 even where refusal leaves a visible gap — **especially**
then, because the visible gap is the evidence the refusal happened.

**For the Curator:** RAT-21 is yours, and it decays. The disclosure apparatus here is the part that
does not require you; the question of whether 770,000 agent-drafted words may be published under
the estate's name does.

**For a reader:** assume AI drafting throughout unless an instrument says otherwise, and read
`authorship_note` where present. The estate's position is that this is compatible with the corpus
being trustworthy **only because** every claim carries a falsifier, every instrument names a human
curator, and the correction route is open to anyone — including to machines
([GM-11 §3.2](../00-governance-map/machine-reading-contract.md)).

**Under ML-2.3:** §H.19 (authorship of record), §H.25 (agent constraint), §H.29 (substitution
disclosure), §H.09 (labour displacement without transfer), §H.15 (compliance theatre — §4's
conditions 2 and 3 are its direct application), §C.10 (machine learning and synthetic derivation,
which this instrument does not displace).

---

**Related:** [MX-023 Attention and Human Sovereignty](mx-023-attention-and-human-sovereignty.md) ·
[ST-02 Front-Matter Schema](../standards/st-02-front-matter-schema.md) ·
[ST-24 Page Prose Standard](../standards/st-24-page-prose-standard.md) ·
[SITE-01 Route Manifest](../site/route-manifest.md) ·
[Machine Reading Contract](../00-governance-map/machine-reading-contract.md) ·
[RAT-21](../00-governance-map/open-questions-and-ratifications.md#rat-21) ·
[RAT-23](../00-governance-map/open-questions-and-ratifications.md#rat-23)

*Curated by Maher. Four use classes, five prohibitions, one volume gate that cannot see the failure
it most needs to catch — and this instrument was drafted by the kind of system it governs, which
is stated in its front matter rather than discovered by a reader.*
