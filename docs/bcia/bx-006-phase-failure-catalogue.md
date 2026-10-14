---
doc_id: BX-006
title_en: Phase Failure Catalogue
title_ar: فهرس إخفاقات المراحل
family: bcia
version: v2026.10.1
status: published
authority: record
prevailing_text: ar
audience_tier: 3
depth: meta
evidence_class: semi-durable
review_interval_months: 6
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [bcia, failures, catalogue, remedies, free-fixes]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000, class I-1, resting on gap 1. Every failure catalogued here was found by the system that caused it.
route: /bcia/failures/
---

# BX-006 — Phase Failure Catalogue

> **This page will not resolve:** how often any of these failures actually harms a
> reader. Frequencies would need reader data, refused at
> [REG-06](../registries/reg-06-dataset-registry.md).

> **Authority.** A **record** — outside the precedence ladder
> ([GM-01](../00-governance-map/precedence-and-conflict-rules.md)). It reports;
> it creates no duty.

> **Disclosure first.** Of the **twelve** failures catalogued, **seven have
> remedies that are free** — no standard amended, no permission needed, no reader
> data. They are listed in [§5](#5-the-free-seven). That seven free remedies have
> gone unadopted across ~80 instruments is the single most actionable fact in the
> BCIA family, and §5.1 explains the mechanism that kept them invisible.

---

## 1. Position

[BX-001](bx-001-before-phase.md)–[BX-005](bx-005-phase-audit-method.md) each found
failures while examining their own phase. Scattered across five documents, they
cannot be compared, counted, or prioritised.

This record consolidates them. The value is **not** the list — each entry already
exists elsewhere — but the two things a consolidation makes visible:

1. **Which failures share a cause.** Three trace to one standard.
2. **Which remedies are free.** Seven of twelve, which nobody could see while they
   were distributed.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **phase failure** | The corpus failing a phase obligation ([BX-000 §2](bx-000-bcia-charter.md)) |
| **free remedy** | One requiring no standard amendment, no ratification, no reader data |
| **gated remedy** | One requiring ratification or a vacant role |
| **impossible remedy** | One requiring a refused capability |
| **cause cluster** | Failures sharing one origin |

## 3. The catalogue

| # | Failure | Phase | Source | Remedy | Class |
|---|---|---|---|---|---|
| **PF-1** | Opening answers "how does this relate?" not "is this my problem?" | B | [BX-001 §2.1](bx-001-before-phase.md) | One opening line stating what the page won't resolve | **Free** |
| **PF-2** | Audience tier invisible in the rendered page | B | [BX-001 §3.1](bx-001-before-phase.md) | Surface tier in the page stamp | **Free** |
| **PF-3** | Limits section at §7, unreachable before commitment | B, I | [BX-001 §3.2](bx-001-before-phase.md) | One-line exclusions in the opening | **Free** |
| **PF-4** | Related blocks generate context-free arrivals | B | [BX-001 §2.2](bx-001-before-phase.md) | *(none identified)* | **Unresolved** |
| **PF-5** | Fluency read as comprehension | C | [BX-002 §3.1](bx-002-contact-phase.md) | *(none — structural)* | **Unresolved** |
| **PF-6** | Disclosure amplifies trust in unverified claims | C | [BX-002 §3.1](bx-002-contact-phase.md) | *(none identified)* | **Unresolved** |
| **PF-7** | Terminal state buried in prose, invisible to scanning | C | [BX-002 §5.1](bx-002-contact-phase.md) | Tabulate or bold every terminal state | **Free** |
| **PF-8** | Eight relations offered where two integrate | I | [BX-003 §2.1](bx-003-internalisation-phase.md) | Limit in-body relations to two | **Free** |
| **PF-9** | Fragmenting device (related block) precedes integrating device (exit pair) | I | [BX-003 §5.1](bx-003-internalisation-phase.md) | Swap the order | **Free** |
| **PF-10** | Precedence-ladder tax on every page's first sentence | I | [BX-003 §3.1](bx-003-internalisation-phase.md) | *(none identified)* | **Unresolved** |
| **PF-11** | Returning reader cannot find defects filed against the page | A | [BX-004 §3.1](bx-004-after-phase.md) | Instruments link their own defects (P1) | **Free** |
| **PF-12** | Reader cannot be told a relied-on text changed | A | [BX-004 §2.2](bx-004-after-phase.md) | Corrections feed + "last corrected" stamp (P2, P3) | **Free** — but see §5.2 |

**Free: 7 (PF-1, 2, 3, 7, 8, 9, 11). Partly free: 1 (PF-12). Unresolved: 4.**

### 3.1 The cause clusters

| Cluster | Failures | Origin |
|---|---|---|
| **The eight-part recipe has no phase B slot** | PF-1, PF-3 | [ST-24](../standards/st-24-page-prose-standard.md) opens with Position |
| **[ST-18](../standards/st-18-related-blocks-and-exit-pairs.md)'s eight-link floor** | PF-4, PF-8, PF-9 | A findability remedy applied without phase distinction |
| **Front matter invisible to readers** | PF-2 | Presentation, not standard |
| **Asymmetric defect linkage** | PF-11 | [ST-08 L5](../standards/st-08-cross-reference-and-link-integrity.md) |
| **Genuinely structural** | PF-5, PF-6, PF-10 | No remedy identified |

**Three failures trace to [ST-18](../standards/st-18-related-blocks-and-exit-pairs.md)
alone.** That standard was written to solve one real problem — counter-intuitive
filing under [MX-004](../corpus/mx-004-terms-of-top-levels.md)'s partition — and
solved it with a device (eight links) that is correct for phase B and wrong for
phase I.

This is not a bad standard. It is a standard written **before the phase
distinction existed**, which is the ordinary way such things happen and the reason
a diagnostic like [BX-005](bx-005-phase-audit-method.md) is worth having.

## 4. Mechanism

### 4.1 Classifying a remedy

```
does it need a standard amended?         yes → GATED (ratification)
does it need a vacant role?              yes → GATED
does it need reader data?                yes → IMPOSSIBLE (REG-06 refusals)
otherwise                                    → FREE
```

### 4.2 Free does not mean easy at scale

A free remedy costs nothing **per page** and must be applied to ~80 pages. PF-1
(one opening line) is one sentence; across the corpus it is eighty sentences.

But five of the seven — PF-2, PF-7, PF-8, PF-9, PF-11 — are **practice changes for
new pages plus a mechanical pass on old ones**, and PF-9 is a single ordering rule
applied once in [SITE-02](../site/page-contract.md)'s furniture spec.

## 5. The free seven

| # | Remedy | Scope of work |
|---|---|---|
| **PF-1** | Opening line: what the page won't resolve | ~80 sentences |
| **PF-2** | Tier in the page stamp | Stamp template |
| **PF-3** | One-line exclusions in the opening | Merges with PF-1 |
| **PF-7** | Terminal state tabulated or bolded | ~40 worked instances |
| **PF-8** | Two in-body relations, not eight | Practice change |
| **PF-9** | Exit pair before related block | **One ordering rule** |
| **PF-11** | Instruments link their own defects | ~31 defect back-links |

### 5.1 Why seven free remedies went unadopted

Not laziness, and not oversight in the ordinary sense. Three mechanisms, each
documented elsewhere:

1. **Checklist completeness** ([BX-001 §4.1](bx-001-before-phase.md)). An author
   who writes all eight [ST-24](../standards/st-24-page-prose-standard.md) parts
   has discharged the standard. What is off the checklist is not neglected — it is
   **invisible**.
2. **The quality rubric is phase-blind**
   ([BX-005 §5.1](bx-005-phase-audit-method.md)).
   [RB-03](../rubrics/rb-03-instrument-quality-rubric.md)'s six dimensions measure
   phases C and A only, so pages failing at B and I **scored well**.
3. **Incapacity absorbing capability** ([BX-004 §4.1](bx-004-after-phase.md)).
   Having named a real refusal (no address list), the estate stopped asking what
   was possible without one — and PF-12's three pull-side remedies went unexamined.

Together these explain the whole pattern: **a corpus can be carefully written,
honestly self-assessed, and systematically blind, if its checklist and its rubric
share the same blind spot.**

### 5.2 PF-12 is the one that was misattributed

[BX-004 §5.1](bx-004-after-phase.md) found that the harm the estate attributes to
its address-list refusal is **substantially caused by PF-11**, which is free.

A reader who returns to a page they relied on — doing exactly what the pull model
asks — still cannot see a defect filed against it, because defects live in the
register and the page does not link them.

So PF-12 has been carrying blame for PF-11's failure. Until PF-11 is adopted, the
estate cannot honestly claim that its notification refusal is the cause of phase A
harm.

## 6. Failure modes of this catalogue

| # | Failure | Current state |
|---|---|---|
| F1 | **Consolidation read as new findings** | Every entry is sourced; none is new |
| F2 | **Free misclassified** | §4.1's gate is checkable per row |
| F3 | **Unresolved four abandoned** | PF-4, 5, 6, 10 have no remedy and are **listed rather than dropped** |
| F4 | **Catalogue treated as authority** | It is a `record`; creates no duty |
| F5 | **Self-found bias** | **Structural** — all twelve found by the causing system |
| F6 | **Free-at-scale underestimated** | §4.2 states the per-page arithmetic |

## 7. Limits

1. **Frequencies are unknown.** No failure here has a rate; all are structural
   claims (opening line).
2. **All twelve are self-found** by the system that produced the corpus
   ([MX-017 C1](../corpus/mx-017-conflicts-of-interest.md)).
3. **Four are unresolved** — PF-5 (fluency) and PF-6 (disclosure as trust
   amplifier) may be irreducible; PF-4 and PF-10 simply have no proposal.
4. **The free/gated classification is the agent's**, and an agent has an interest
   in remedies being free — free remedies are ones it can perform.
5. **Twelve is not a census.** The phase audit has run five times, all self-audits.
6. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** This catalogue is falsified if:
>
> - **(a)** a remedy classified **free** is shown to require an amendment,
>   ratification, a vacant role, or reader data (§4.1) — **checkable per row in
>   minutes**;
> - **(b)** a thirteenth phase failure is identified — **expected**, since twelve
>   came from five self-audits;
> - **(c)** PF-5, PF-6 or PF-10 is shown to have a remedy, contradicting §3's
>   `Unresolved`;
> - **(d)** §5.2 is wrong — PF-11's adoption is shown **not** to reduce the harm
>   attributed to PF-12;
> - **(e)** any cause cluster in §3.1 is shown to be a coincidence rather than a
>   shared origin.
>
> **(a) is the test a sceptical reader should run first.** If the free seven are
> not free, the catalogue's headline is wrong and the estate's inaction is
> explained. **(c) would be the most valuable outcome** — three structural failures
> currently have no proposal at all.

## 9. Obligation

None — this is a `record`. The bearing duties sit with the standards named in
[BX-000 §4.2](bx-000-bcia-charter.md). For navigation:

- Adopt the **free seven** (§5); none needs permission.
- Adopt **PF-11 before assessing PF-12** (§5.2) — the estate is currently crediting
  an unpaid cost to a principle.
- Keep PF-4, PF-5, PF-6 and PF-10 **listed as unresolved** rather than dropping
  them (F3).
- File the gated items as ratification questions:
  [BX-000/1](bx-000-bcia-charter.md) (mandatory abstracts),
  [BX-002/1](bx-002-contact-phase.md) (prominent terminal state),
  [BX-003/1](bx-003-internalisation-phase.md) (block ordering),
  [BX-005/1](bx-005-phase-audit-method.md) (RB-03 phase blindness).

---

### Related

**Sources of every entry** — [BX-001](bx-001-before-phase.md) ·
[BX-002](bx-002-contact-phase.md) · [BX-003](bx-003-internalisation-phase.md) ·
[BX-004](bx-004-after-phase.md)

**Standards in the cause clusters** —
[ST-24](../standards/st-24-page-prose-standard.md) ·
[ST-18](../standards/st-18-related-blocks-and-exit-pairs.md) ·
[ST-08](../standards/st-08-cross-reference-and-link-integrity.md) ·
[SITE-02](../site/page-contract.md)

**Why the failures were invisible** —
[RB-03](../rubrics/rb-03-instrument-quality-rubric.md) ·
[BX-005](bx-005-phase-audit-method.md) ·
[REG-07](../registries/reg-07-defect-classification-registry.md) ·
[AG-011](../agents/ag-011-agent-review-and-audit.md)

**Where these should be filed** —
[defect register](../00-governance-map/defect-register.md) ·
[open questions](../00-governance-map/open-questions-and-ratifications.md) ·
[task ledger](../00-governance-map/task-ledger.md) ·
[BX-000](bx-000-bcia-charter.md)

### Exit pair

1. **Test one "free" claim.** Falsifier §8(a) — pick any row marked Free and run
   §4.1's four gates. If one fails, the catalogue's headline is wrong.
2. **Solve an unresolved one.** PF-5, PF-6 and PF-10 have no remedy proposed.
   [§3](#3-the-catalogue) lists them rather than hiding them.

<!-- mx-pagestamp: BX-006 · v2026.10.1 · record · reviewed 2026-09-16 · next review 2026-12-16 -->
<!-- mx-demo: the published site is a demonstration; none of the seven free remedies has been adopted -->
