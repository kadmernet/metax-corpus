---
doc_id: BX-003
title_en: The Internalisation Phase
title_ar: مرحلة الاستيعاب
family: bcia
version: v2026.10.1
status: published
authority: companion
prevailing_text: ar
audience_tier: 3
depth: macro
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [bcia, internalisation, integration, cross-reference, transfer]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000, class I-1, resting on gap 1. Internalisation is the phase where the corpus's density helps and its size hurts, and the drafting system caused both.
route: /bcia/internalisation/
---

# BX-003 — The Internalisation Phase

> **This page will not resolve:** how many instruments a reader can hold
> simultaneously. That is a question about human memory the estate has not
> researched ([§7.3](#7-limits)).

> **Authority.** `companion`. Phase I obligations are discharged by
> [ST-17](../standards/st-17-worked-instance-standard.md),
> [ST-18](../standards/st-18-related-blocks-and-exit-pairs.md) and
> [ST-08](../standards/st-08-cross-reference-and-link-integrity.md), per
> [BX-000 §4.2](bx-000-bcia-charter.md).

> **Disclosure first.** Internalisation is where this corpus's **size becomes a
> hostile property**. Roughly eighty instruments, each linking to at least eight
> others, produce a graph no reader can hold. The estate has optimised heavily for
> *findability* ([ST-18](../standards/st-18-related-blocks-and-exit-pairs.md)) and
> not at all for **integration**, and §5 shows the two are in tension.

---

## 1. Position

Phase I is the reader **relating what they have just read to what they already
hold**. It is the phase in which reading becomes knowledge, and it is the only
phase whose difficulty **increases as the corpus grows**.

| Phase | Effect of corpus growth |
|---|---|
| **B** Before | Slightly worse — more pages to choose among |
| **C** Contact | **Neutral** — one page is one page |
| **I** Internalisation | **Much worse** — more relations to hold |
| **A** After | Slightly worse — more to keep current |

That asymmetry is the whole subject. Every instrument added to this corpus makes
Contact no harder and Internalisation harder for every reader of every other page.

### 1.1 The estate has been optimising the wrong phase

[ST-18 §1](../standards/st-18-related-blocks-and-exit-pairs.md) is explicit: four
related groups and eight links exist because
[MX-004](../corpus/mx-004-terms-of-top-levels.md)'s rigorous partition files
documents counter-intuitively, so **navigation must be redundant**.

That serves **findability** — getting a reader to the right page. It is a phase B
remedy, and [BX-001 §2.2](bx-001-before-phase.md) already recorded that it
*increases* phase B load by generating context-free arrivals.

It does something worse at phase I: **eight outbound links per page is eight
invitations to leave before integrating.** A reader following related links depth-first
accumulates open threads and integrates none.

## 2. What internalisation requires

| # | Requirement | Served by |
|---|---|---|
| **I1** | A concrete case to attach the abstraction to | [ST-17](../standards/st-17-worked-instance-standard.md) worked instance |
| **I2** | The boundary — what this is **not** | [ST-03](../standards/st-03-limits-and-bridge.md), [ST-10 field 5](../lexicon/lexicon-entry-standard.md) |
| **I3** | Relation to one or two things already held | **Not served** — §2.1 |
| **I4** | A transfer opportunity — apply it elsewhere | [RB-04 C5](../rubrics/rb-04-reader-comprehension-rubric.md) |

### 2.1 I3 is unserved and the related block is why

I3 asks for **one or two** relations. The related block supplies **eight**.

Eight is not a larger amount of the same good. A reader given two relations
integrates them; a reader given eight chooses none, or follows the first and
abandons the page. The related block is sized for a reader who is **navigating**,
not one who is **integrating**, and those are different readers in different
phases.

So [ST-18 R2](../standards/st-18-related-blocks-and-exit-pairs.md)'s eight-link
floor — a phase B/findability remedy — actively obstructs phase I. Two standards
pulling against each other, exactly as
[ST-16 §4.3](../standards/st-16-audience-tier-standard.md) found for
[ST-08](../standards/st-08-cross-reference-and-link-integrity.md) versus tier 1
plainness.

### 2.2 The exit pair is the phase I instrument

[ST-18 R5](../standards/st-18-related-blocks-and-exit-pairs.md) requires **exactly
two** exit actions, and [R7](../standards/st-18-related-blocks-and-exit-pairs.md)
requires at least one to be adverse.

**Two** is the I3 number. The exit pair, not the related block, is the corpus's
integration device — and it was designed as a call to action, not as a memory aid.
A reader who takes nothing from a page but its two exits has retained the right
quantity of relation.

That is a stronger justification for R5's exactly-two rule than
[ST-18](../standards/st-18-related-blocks-and-exit-pairs.md) offers: it reasons
that *"more than two is a menu; fewer is a dead end"*, which is about choice
paralysis. The phase I reason is better — two is what integrates.

## 3. The density problem

| Corpus property | Phase I effect |
|---|---|
| ~80 instruments | Exceeds what any reader holds |
| ≥ 8 links per page | ~640+ edges; no reader maps them |
| Nine pillars, 45 hubs | A structure that must itself be learned |
| Precedence ladder, 8 tiers + records outside | Must be held to read any authority note |
| 19 identifier prefixes | Must be held to parse any cross-reference |

### 3.1 The precedence ladder is a phase I tax on every page

Every instrument opens with an authority note referencing tiers. A reader cannot
parse *"`governing`, tier 4, subordinate to tier 1a incorporated by §A.10"* without
holding the ladder.

That is an **eight-item structure required to read the first sentence of any
page.** It is taught in
[GM-01](../00-governance-map/precedence-and-conflict-rules.md) and assumed
everywhere.

The estate's own [ST-16](../standards/st-16-audience-tier-standard.md) identified
this at tier 1 — three of four tier 1 claims fail because they open with precedence
reasoning. BX-003 records the tier 3 version: even practitioners pay the tax on
every page, and the corpus has never considered whether the authority note could
carry its meaning without the ladder.

## 4. Mechanism — auditing a page at phase I

```
I1: is there a concrete case? does it TRACE or illustrate?
I2: is the boundary stated, and early enough to matter?
I3: does the page relate itself to ONE or TWO things — or to eight?
I4: does the exit pair offer a transfer, or only a reference?
```

## 5. Worked instance

**Testing I3 on a real reading path.**

A reader has just finished [AG-010](../agents/ag-010-agent-error-and-correction.md)
and understood its central finding: prohibitions on an agent hold, affirmative
duties do not.

Now count what the page offers for integration:

| Device | Count | Serves I3? |
|---|---|---|
| Related block | **16 links, 4 groups** | **No** — far past two |
| Exit pair | **2 actions** | **Yes** |
| In-text cross-references | ~40 | No — these serve C, not I |

The reader who uses the **exit pair** goes to
[§5.1](../agents/ag-010-agent-error-and-correction.md) and re-reads the one
generalisation. Integration succeeds.

The reader who uses the **related block** faces sixteen choices, opens
[AG-001](../agents/ag-001-agent-roles-and-scopes.md), and now holds two partially
integrated instruments. Repeat twice and they hold four fragments and no finding.

**Terminal state: `result` — the exit pair integrates; the related block
fragments.**

### 5.1 The finding

The corpus contains two devices at the foot of every page, and **they serve
opposite phases**:

| Device | Phase | Optimal size | Actual |
|---|---|---|---|
| Related block | B (findability) | Many | 8+ ✔ |
| Exit pair | I (integration) | Two | 2 ✔ |

Both are correctly sized **for their own phase**. The failure is that they are
**presented together, unlabelled by phase**, so a reader cannot tell which one they
should be using.

A reader who has finished reading and wants to *consolidate* should use the exit
pair and ignore the related block. A reader who has finished and wants to *go
elsewhere* should do the reverse. Nothing on any page says so, and the related
block appears **first** — so the device that fragments is encountered before the
device that integrates.

Filed per [ST-17 W6](../standards/st-17-worked-instance-standard.md):

> **Finding BX-003/1.** The exit pair should precede the related block, or the two
> should be labelled by purpose — *"to consolidate"* and *"to go elsewhere"*. The
> current order presents the fragmenting device first. This is an ordering change to
> [SITE-02](../site/page-contract.md) page furniture and
> [ST-18](../standards/st-18-related-blocks-and-exit-pairs.md), filed as a
> ratification question rather than made here
> ([BX-000 §1.1](bx-000-bcia-charter.md)).

The change costs nothing — no content, no new rule, an ordering swap — and it
addresses the phase the corpus has never optimised.

## 6. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Eight relations offered where two integrate** | **Structural** — §2.1 |
| F2 | **Fragmenting device presented first** | **Actual** — §5.1 |
| F3 | **Depth-first link following** | Unmeasurable; likely |
| F4 | **Precedence-ladder tax on every page** | **Actual** — §3.1 |
| F5 | **Corpus growth degrading phase I for all prior pages** | **Structural and accelerating** — §1 |
| F6 | **Boundary stated too late** | Inherited from [BX-001 §3.2](bx-001-before-phase.md) — Limits at §7 |

F5 deserves emphasis. **This session added roughly forty instruments.** Under §1,
that made phase I worse for every reader of every pre-existing page, and no
instrument in the corpus records growth as having a cost.

## 7. Limits

1. **Phase I is unobservable here** — no reader data
   ([REG-06](../registries/reg-06-dataset-registry.md)).
2. **The four requirements I1–I4 are asserted**, not derived.
3. **No memory or comprehension literature was surveyed** — the same gap
   [RB-04 §6.5](../rubrics/rb-04-reader-comprehension-rubric.md) and
   [BX-000 §7.3](bx-000-bcia-charter.md) record. "Two integrates, eight fragments"
   is **E0**.
4. **§5 traced one reading path**, imagined by the author.
5. **The drafting system caused F5** and is assessing it
   ([MX-017 C1](../corpus/mx-017-conflicts-of-interest.md)); the direction of
   interest is toward treating volume as costless.
6. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** readers given eight related links integrate as well as those given two
>   — which would destroy §2.1 and §5.1 together;
> - **(b)** the exit pair is shown to be used for navigation rather than
>   consolidation;
> - **(c)** the authority note is shown to be parseable without holding the
>   precedence ladder (§3.1);
> - **(d)** corpus growth is shown **not** to degrade phase I for existing pages
>   (F5);
> - **(e)** a fifth internalisation requirement is identified.
>
> **(c) is runnable in minutes**: hand any authority note in this corpus to someone
> who has not read
> [GM-01](../00-governance-map/precedence-and-conflict-rules.md) and ask what it
> means. **(a) and (d) need readers the estate refuses to observe**, so the two
> claims this page rests on most heavily are permanently **E0**.

## 9. Obligation

**On an author (practice; this is a companion):**
- Offer **one or two** relations in the body, not eight (I3, §2.1).
- Treat the **exit pair as the integration device** and write it accordingly
  (§2.2).
- State the boundary early enough to be reached (I2, F6).
- Make the worked instance a trace, not an illustration (I1).

**On the estate:**
- File **BX-003/1**: put the exit pair before the related block, or label both by
  purpose (§5.1). Costless and unaddressed.
- **Record corpus growth as having a phase I cost** (F5) — no instrument does, and
  forty were added this session.
- Run falsifier §8(c) on the authority note; it is minutes.
- Keep "two integrates, eight fragments" labelled **E0** (§7.3).

---

### Related

**Standards discharging phase I** —
[ST-17](../standards/st-17-worked-instance-standard.md) ·
[ST-18](../standards/st-18-related-blocks-and-exit-pairs.md) ·
[ST-08](../standards/st-08-cross-reference-and-link-integrity.md) ·
[ST-03](../standards/st-03-limits-and-bridge.md)

**Structures a reader must hold** —
[GM-01 precedence](../00-governance-map/precedence-and-conflict-rules.md) ·
[MX-004](../corpus/mx-004-terms-of-top-levels.md) ·
[ST-01](../standards/st-01-identifier-and-url-grammar.md) ·
[LEX-01](../lexicon/keyword-register.md)

**The path traced in §5** —
[AG-010](../agents/ag-010-agent-error-and-correction.md) ·
[AG-001](../agents/ag-001-agent-roles-and-scopes.md) ·
[AG-005](../agents/ag-005-agent-tool-use-limits.md) ·
[RB-04](../rubrics/rb-04-reader-comprehension-rubric.md)

**Adjacent phases** — [BX-000](bx-000-bcia-charter.md) ·
[BX-001](bx-001-before-phase.md) · [BX-002](bx-002-contact-phase.md) ·
[BX-004](bx-004-after-phase.md)

### Exit pair

1. **Swap two blocks.** Finding BX-003/1 — putting the exit pair before the related
   block costs nothing and stops the fragmenting device being encountered first.
2. **Measure the tax.** Falsifier §8(c) — show any authority note to someone who
   has not read the precedence ladder and see what survives.

<!-- mx-pagestamp: BX-003 · v2026.10.1 · companion · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; ~40 instruments added this session degraded this phase for every existing page -->
