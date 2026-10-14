---
doc_id: BX-001
title_en: The Before Phase
title_ar: مرحلة ما قبل القراءة
family: bcia
version: v2026.10.1
status: published
authority: companion
prevailing_text: ar
audience_tier: 3
depth: meta
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [bcia, before, orientation, abstract, arrival]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000, class I-1, resting on gap 1. The phase this document describes is the one the corpus serves worst, per BX-000 §5.1.
route: /bcia/before/
---

# BX-001 — The Before Phase

> **Authority.** `companion`, tier 5a-adjacent. It **explains**; it does not bind.
> Phase B obligations are discharged by
> [ST-16](../standards/st-16-audience-tier-standard.md) and
> [ST-09](../standards/st-09-summary-and-abstract-standard.md), per
> [BX-000 §4.2](bx-000-bcia-charter.md).

> **Disclosure first.** [BX-000 §5.1](bx-000-bcia-charter.md) found that this
> corpus is **systematically weak at phase B**, because
> [ST-24](../standards/st-24-page-prose-standard.md)'s eight parts contain no slot
> for it. This document describes a phase the estate serves badly, and it inherits
> the weakness: a reader in phase B for *this page* is served by the two sentences
> above and nothing else.

---

## 1. Position

Phase B is everything that happens **before a reader commits**. It is short — often
under thirty seconds — and it is the phase in which a reader is lost for good.

The asymmetry that makes it matter:

| Phase | If the corpus fails | Recovery |
|---|---|---|
| **B** | Reader never opens the page, or opens the wrong one | **None** — the reader is gone and the corpus never knows |
| C | Reader is confused while reading | Re-read, follow a link |
| I | Reader absorbs claims and not limits | A later page may correct it |
| A | Reader acts on stale text | Version stamp may catch it |

Failures in C, I and A leave a reader **in the corpus** where a later page can
help. A phase B failure removes them. And the estate cannot detect it: it does not
measure arrivals ([REG-06 `DSET-R01`](../registries/reg-06-dataset-registry.md)),
so a reader deterred at phase B is indistinguishable from one who never existed.

## 2. What a reader is doing in phase B

Four questions, asked fast, usually from a related-block link or a route:

| # | Question | Answered by |
|---|---|---|
| **Q1** | *Is this about my problem?* | Title, first two lines |
| **Q2** | *Is this written for someone like me?* | `audience_tier`, register |
| **Q3** | *Does it bind, or merely describe?* | `authority` |
| **Q4** | *Is it current?* | `version`, next review date |

### 2.1 The corpus answers Q2–Q4 well and Q1 badly

Q2, Q3 and Q4 are front matter fields, present on every instrument and surfaced in
the page stamp. Strong.

**Q1 is the failure.** The eight-part recipe opens with **Position**, which states
where the instrument sits in the precedence ladder — a phase-I orientation. A
reader asking *"is this about my problem?"* gets an answer to *"how does this relate
to the other instruments?"*, which presupposes the commitment they have not yet
made.

### 2.2 The related block makes it worse

[ST-18 §1](../standards/st-18-related-blocks-and-exit-pairs.md) exists because
[MX-004](../corpus/mx-004-terms-of-top-levels.md)'s rigorous partition files
documents counter-intuitively — so eight links in four groups give a reader
redundant routes in.

But redundancy **increases phase B load**. A reader arriving from a related block
has been told the page is relevant to something and must now determine *what*. More
inbound routes mean more readers arriving with less context, and the landing
experience is Position.

So [ST-18](../standards/st-18-related-blocks-and-exit-pairs.md) solves a
findability problem by generating phase B traffic the pages are not built to
receive.

## 3. What phase B obligations actually are

| # | Obligation | Discharged by | State |
|---|---|---|---|
| **B1** | State the subject in the title | [ST-01](../standards/st-01-identifier-and-url-grammar.md) | **Met** |
| **B2** | State the audience | [ST-16](../standards/st-16-audience-tier-standard.md) `audience_tier` | **Met in field; §3.1** |
| **B3** | State the authority class | [ST-02](../standards/st-02-front-matter-schema.md) | **Met** |
| **B4** | State currency | version + review date | **Met** |
| **B5** | **Answer "is this my problem?" in the first two lines** | *(nothing)* | **Unmet** |
| **B6** | Make the page's scope boundary visible early | [ST-03](../standards/st-03-limits-and-bridge.md) Limits — **at §7** | **Unmet in position** |

### 3.1 B2 is met in the field and not in the page

`audience_tier: 3` appears in front matter. Front matter is **not rendered to a
reader** in most presentations, and the page stamp carries authority and dates but
not tier.

So the field satisfying B2 is one a practitioner reads and a lay reader never
sees — which is precisely backwards, since the reader who most needs to know *"this
is not written for you"* is the one who will not find the field.

[ST-16 §6](../standards/st-16-audience-tier-standard.md) already found that three
of four tier 1 claims fail their own test. This adds a second problem: even a
correct tier declaration is invisible where it matters.

### 3.2 B6 and the position of Limits

Every instrument carries a Limits section, and it is always **§7 or later** — after
Position, Definitions, Mechanism, Worked instance, Failure modes.

A reader in phase B wants to know what the page does **not** cover, which is the
fastest way to rule a page out. Putting it seventh means it is reached only by
readers who have already committed — and they are not the ones who needed it.

## 4. Mechanism — how a page could serve phase B

Three candidate remedies, with costs:

| Remedy | Serves | Cost |
|---|---|---|
| **R1 Mandatory abstract** before Position, ≤ 120 words, per [ST-09 §2.1](../standards/st-09-summary-and-abstract-standard.md) | Q1, B5 | Amends [ST-24](../standards/st-24-page-prose-standard.md), tier 5 — needs ratification ([BX-000/1](bx-000-bcia-charter.md)) |
| **R2 Tier and authority in the visible header**, not only front matter | Q2, Q3, B2 | Presentation change; no standard amended |
| **R3 One-line exclusions in the opening**, drawn from Limits | Q1, B6 | Authoring practice; no standard amended |

**R2 and R3 require no ratification.** R1 does, and is the one filed as a
ratification question.

### 4.1 Why the estate has not done R3 already

R3 costs one sentence per page and needs no permission. It has not been done
because the eight-part recipe is **complete as a checklist**: an author who writes
all eight parts has discharged [ST-24](../standards/st-24-page-prose-standard.md)
and has no prompt to add anything.

That is the mechanism by which a good standard produces a systematic gap — **the
checklist defines the work, and what is off the checklist is not neglected but
invisible.**

## 5. Worked instance

**Phase B for a real arrival.**

A licensee wants to know whether they may use estate material in a paid course.
They arrive at [MX-002 terms](../corpus/mx-002-terms-of-service.md) — a reasonable
guess.

| Q | What they get in 30 seconds | Served? |
|---|---|---|
| Q1 my problem? | Title "Terms of Service"; first lines are an authority note about tier 3 and ML-2.3 precedence | **No** — they cannot tell it will not answer them |
| Q2 for me? | `audience_tier: 1` in invisible front matter | **No** |
| Q3 binds? | Authority note says `governing` | **Yes** |
| Q4 current? | v2026.10.1, page stamp | **Yes** |

They commit, read, reach §8 — and the worked instance traces their exact question
to **`indeterminate`**, because three Scale Gate thresholds are unpublished.

**Terminal state: `blockage` — but at phase C, after the commitment.**

### 5.1 The finding

The reader spent the full reading cost of a governing instrument to learn their
question **cannot be answered by the estate at all**.

[MX-002 §8](../corpus/mx-002-terms-of-service.md) is *exemplary* at phases C, I and
A: it traces the question honestly, names the estate as the cause, and refuses to
manufacture a confident permission. The failure is entirely at phase B — nothing on
arrival said *"if your question is about reuse at scale, this page will not resolve
it."*

And R3 would have fixed it. One sentence in the opening:

> *This page does not decide reuse. [ML-2.3](../license/the-maher-license.md) does,
> and for use at scale the [Scale Gate](../license/scale-gate.md) thresholds are
> **unpublished**, so the analysis cannot currently be completed.*

Twenty-eight words. No standard amended, no ratification, no permission. It would
have saved the reader the entire reading, and it is the kind of thing the eight-part
recipe gives an author no occasion to write.

Filed per [ST-17 W6](../standards/st-17-worked-instance-standard.md):

> **Finding BX-001/1.** R3 — a one-line statement of what the page will **not**
> resolve, in the opening — requires no amendment to any standard and is the
> highest-value unmade change in the corpus's presentation. It should be adopted as
> authoring practice immediately, independently of the
> [BX-000/1](bx-000-bcia-charter.md) ratification question about mandatory
> abstracts.

## 6. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Q1 unanswered on arrival** | **Systemic** — §2.1 |
| F2 | **Tier invisible to the reader who needs it** | **Actual** — §3.1 |
| F3 | **Limits reached only after commitment** | **Systemic** — §3.2 |
| F4 | **Related blocks generating unserved arrivals** | **Actual** — §2.2 |
| F5 | **Checklist completeness hiding the gap** | **Actual** — §4.1 |
| F6 | **Phase B failures undetectable** | **Structural** — §1; the estate cannot measure arrivals |

## 7. Limits

1. **Phase B failure is undetectable here.** Every claim about how readers behave
   on arrival is **E0** and will remain so
   ([REG-06](../registries/reg-06-dataset-registry.md)).
2. **The four questions of §2 are asserted**, not observed.
3. **This page does not implement R3 on itself** beyond its disclosure block — a
   partial demonstration of the very gap it describes.
4. **R1 requires ratification** and the Ratifying Authority is vacant
   ([REG-08](../registries/reg-08-role-and-authority-registry.md)).
5. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** a reader is shown to answer Q1 reliably from the current opening of a
>   corpus page — **only a reader can run this**;
> - **(b)** adding R3 to a page is shown to make no difference to a reader's ability
>   to rule it out;
> - **(c)** a fifth phase-B question is identified beyond Q1–Q4;
> - **(d)** the Limits section's position is shown not to matter (§3.2);
> - **(e)** §5.1's claim that R3 needs no amendment is wrong — i.e. a standard
>   forbids an opening line of that kind.
>
> **(e) is checkable in minutes** against
> [ST-24](../standards/st-24-page-prose-standard.md) and
> [SITE-02](../site/page-contract.md), and the estate asserts nothing forbids it —
> which means the remedy has been available throughout and simply was not written.

## 9. Obligation

**On an author (practice, not binding — this is a companion):**
- Adopt **R3**: one opening line saying what the page will **not** resolve (§5.1).
- Make tier and authority visible in the rendered page, not only in front matter
  (R2, §3.1).
- Treat an inbound related-block link as a phase B arrival with no context (§2.2).
- Remember the checklist does not prompt this (§4.1).

**On the estate:**
- Adopt **finding BX-001/1** as practice now; it needs no ratification.
- Pursue [BX-000/1](bx-000-bcia-charter.md) — mandatory abstracts — through the
  ratification route (R1).
- Keep all phase B claims labelled **E0** (§7.1).

---

### Related

**Standards that discharge phase B** —
[ST-16](../standards/st-16-audience-tier-standard.md) ·
[ST-09](../standards/st-09-summary-and-abstract-standard.md) ·
[ST-02](../standards/st-02-front-matter-schema.md) ·
[ST-03](../standards/st-03-limits-and-bridge.md)

**Why arrivals are unserved** —
[ST-24](../standards/st-24-page-prose-standard.md) ·
[ST-18](../standards/st-18-related-blocks-and-exit-pairs.md) ·
[MX-004](../corpus/mx-004-terms-of-top-levels.md) ·
[SITE-02](../site/page-contract.md)

**The instance that failed at B** —
[MX-002](../corpus/mx-002-terms-of-service.md) ·
[scale gate](../license/scale-gate.md) ·
[ML-2.3](../license/the-maher-license.md) ·
[MX-012](../corpus/mx-012-licensing-and-reuse.md)

**Why the failure is invisible** —
[REG-06](../registries/reg-06-dataset-registry.md) ·
[MX-023](../corpus/mx-023-attention-and-human-sovereignty.md) ·
[RB-04](../rubrics/rb-04-reader-comprehension-rubric.md) ·
[BX-000](bx-000-bcia-charter.md)

### Exit pair

1. **Write one sentence.** Finding BX-001/1 — add to any page an opening line
   saying what it will not resolve. It needs no permission and has never been done.
2. **See the cost of not having it.**
   [MX-002 §8](../corpus/mx-002-terms-of-service.md) — a reader reads a governing
   instrument in full to learn their question is unanswerable.

<!-- mx-pagestamp: BX-001 · v2026.10.1 · companion · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; the phase described here is the one the corpus serves worst -->
