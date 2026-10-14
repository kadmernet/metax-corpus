---
doc_id: ST-18
title_en: Related Blocks and Exit Pairs Standard
title_ar: معيار كتل الروابط وأزواج الخروج
family: standards
version: v2026.10.1
status: published
authority: operative-form
prevailing_text: ar
audience_tier: 3
depth: micro
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [related, exit-pair, navigation, page-furniture, standards]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. The furniture this standard governs is the part of the page contract the estate most consistently satisfies in form and least verifies in substance.
route: /standards/st-18/
---

# ST-18 — Related Blocks and Exit Pairs Standard

> **Authority.** `operative-form`, tier 5. Governs the two furniture items
> [SITE-02](../site/page-contract.md) requires on every page: `.mx-related` (four
> groups, ≥ 8 links) and `.mx-exitpair` (exactly two actions). Link form is
> [ST-08](st-08-cross-reference-and-link-integrity.md); prose form is
> [ST-24](st-24-page-prose-standard.md).

> **Disclosure first.** Every page in this corpus carries both items, and **no
> page's related block has ever been checked for resolvability**
> ([ST-08 §3.1](st-08-cross-reference-and-link-integrity.md): L1 not implemented,
> never run). So the estate satisfies this standard's countable requirements —
> four groups, eight links, two actions — and cannot demonstrate that a single
> link works. Form compliance without integrity verification is the exact failure
> [RB-03](../rubrics/rb-03-instrument-quality-rubric.md) scores as a **2**.

---

## 1. Position

Related blocks exist to solve a problem the corpus created for itself.

[MX-004 §2.1](../corpus/mx-004-terms-of-top-levels.md) assigns every document to
**exactly one** pillar, with a four-rule tie-break. The partition is rigorous, and
[MX-004 §5](../corpus/mx-004-terms-of-top-levels.md) shows the consequence: correct
filing is sometimes **counter-intuitive**. The credential registry lives under
Records, not Learning, because records beat subject.

A reader looking in the intuitive place will not find it. The corpus's answer is
**not** to fudge the partition but to make navigation redundant: four related
groups per page, at least eight links, so a correctly-but-unintuitively filed
document is reachable from wherever a reader actually starts.

That is the design purpose. It follows that a related block is **load-bearing
navigation**, not decoration — which is why a stale link in one is a real fault and
not a cosmetic one.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **related block** | `.mx-related`: four labelled groups of links at the page foot |
| **group** | A set of links sharing a stated relationship to this page |
| **group label** | The stated relationship — the part that carries the information |
| **exit pair** | `.mx-exitpair`: exactly two actions a reader may take next |
| **action** | An instruction plus a destination, not merely a link |
| **decorative link** | A link present to meet a count — prohibited |

### 2.1 The group label does the work

Four groups of two links each is worthless if the groups are labelled "See also",
"More", "Related", "Other". The label must state **why** these links are grouped —
what relationship they bear to this page.

Compare:

| Weak | Strong |
|---|---|
| See also | **Where the gap is recorded** |
| More standards | **What is being scored against** |
| Related | **The four discoveries** |
| Other reading | **Why Q4 scores low** |

The strong labels tell a reader which group to open. That is the difference between
a related block and a footer.

### 2.2 An exit pair is two actions, not two links

An action has an **imperative** and a **consequence**:

> *"Run the cross-check. Falsifier §8(f) — compare every `designated: yes` to the
> designation list. Never done, needs no tools."*

That is an action. *"See also: designation list"* is a link. The exit pair is the
page's last content and the only place the corpus tells a reader what to **do**,
so it is held to the higher form.

## 3. The rules

| # | Rule | Rationale |
|---|---|---|
| **R1** | **Exactly four** groups. Not three, not five | A fixed shape is scannable; a variable one is not |
| **R2** | **≥ 8 links total**, ≥ 2 per group | Redundancy sufficient to defeat the partition problem (§1) |
| **R3** | Every group carries a **relationship label**, never a generic heading | §2.1 |
| **R4** | **No decorative links.** Every link is one a reader of *this* page may need | Padding to meet R2 destroys the signal R2 exists to create |
| **R5** | **Exactly two** exit actions | More than two is a menu; fewer is a dead end |
| **R6** | Each exit action has an **imperative and a consequence** | §2.2 |
| **R7** | At least one exit action must be **adverse** — pointing at a gap, a failure, or a falsifier the reader can run | §3.1 |
| **R8** | Related links are **relative paths** | [ST-08 §2.1](st-08-cross-reference-and-link-integrity.md); survives the portable archive ([MX-019 W5](../corpus/mx-019-sunset-and-wind-down.md)) |

### 3.1 R7 is the rule with content

The other seven rules are shape. R7 requires that **one of the two exits point
somewhere unflattering**: a falsifier the reader can run, a defect, an unmet
obligation, a gap.

The reason is structural. Every page in this corpus is written by the party it
describes ([MX-017 C1](../corpus/mx-017-conflicts-of-interest.md)). A page whose
two exits both lead deeper into the estate's own reasoning offers the reader no
route to disagreement. R7 forces the author to hand the reader a tool against the
page.

It is also [MX-017](../corpus/mx-017-conflicts-of-interest.md)'s substitute **S4**
(outsider falsifiability) implemented at the level of page furniture: the exit pair
is where S4 becomes a concrete instruction rather than a principle.

### 3.2 The four canonical group shapes

Not mandatory, but these four relationships cover most pages and are recommended
as a default set:

| Group | Contains |
|---|---|
| **What governs this** | Instruments above it in the precedence ladder |
| **What this governs, or what applies it** | Instruments below, or operative forms |
| **Where its faults are recorded** | Defects, blockers, objections, verification items |
| **Siblings** | Same-family instruments a reader may have wanted instead |

The third is the one usually omitted, and it is the one
[ST-08 §3.2](st-08-cross-reference-and-link-integrity.md) identifies as widely
breached: defects are filed **in the register** naming an instrument, and the
instrument does not link back. The "where its faults are recorded" group is the
fix, applied at the page rather than the register.

## 4. Mechanism

### 4.1 Building a related block

```
1. what governs this page?            → group 1
2. what applies or depends on it?     → group 2
3. what is filed against it?          → group 3   ← usually skipped
4. what might the reader have meant?  → group 4
label each group by the RELATIONSHIP  (R3)
≥ 2 links per group, ≥ 8 total        (R2)
strike any link a reader of THIS page would not need  (R4)
if striking drops below 8 → the page is under-connected; find real links,
                            do NOT restore the padding
```

The last line matters. If honest pruning leaves fewer than eight links, the
correct response is to find genuine relationships, or to accept that the page is
isolated and record it — not to reinstate decorative links to satisfy a count.

### 4.2 Building an exit pair

```
1. what is the single most useful thing a reader can DO with this page?  → action 1
2. what is the most useful thing that would UNDERMINE it?                → action 2 (R7)
each: imperative + destination + one clause of consequence               (R6)
exactly two                                                              (R5)
```

### 4.3 The checks

| # | Check | Detects | Status |
|---|---|---|---|
| **E1** | Four groups present, ≥ 8 links, ≥ 2 per group | R1, R2 | Specified; **not implemented** |
| **E2** | Exactly two exit actions | R5 | Specified; **not implemented** |
| **E3** | Group labels not in a generic blocklist ("See also", "More", "Related") | R3 | Specified; **not implemented** |
| **E4** | All related links resolve | R8 + [ST-08 L1](st-08-cross-reference-and-link-integrity.md) | Specified; **not implemented** |
| **E5** | At least one exit action links to a defect, objection, or falsifier | R7 | Specified; **not mechanisable reliably** |

Five checks, **zero implemented** ([DEF-001](../00-governance-map/defect-register.md)).
E1, E2 and E3 are trivially mechanisable — counting and a blocklist — and their
absence is the clearest case in the corpus of a cheap check going unbuilt.

## 5. Worked instance

**Auditing one page's furniture against all eight rules.**

Case: [REG-05 credential registry](../registries/reg-05-credential-registry.md).
Chosen because it is a `record` with an unusual shape (empty register), so its
related block cannot rely on the canonical governs/governed structure.

| Rule | Finding | Status |
|---|---|---|
| **R1** four groups | "Assessment", "Due process", "Refusals that constrain design", "Siblings" | **Pass** |
| **R2** ≥ 8 links, ≥ 2 per group | 16 links, 4 per group | **Pass** |
| **R3** relationship labels | Three are relationships; **"Siblings"** is a family fact, not a relationship to *this* page | **Marginal** |
| **R4** no decorative links | [MX-014](../corpus/mx-014-research-ethics-and-exclusions.md) under "Refusals" — does a reader of the credential registry need research ethics? **Yes**: REG-05 §2.1 refuses ranking, and the hard exclusions are where that reasoning lives | **Pass** |
| **R5** exactly two exits | Two | **Pass** |
| **R6** imperative + consequence | "Falsify the emptiness. Produce one credential…"; "Attack the real blocker. Read MX-016 §3…" | **Pass** |
| **R7** ≥ 1 adverse exit | **Both** are adverse — one invites falsification, one points at the blocking vacancy | **Pass, doubly** |
| **R8** relative paths | All `../` | **Pass** |
| **E4** links resolve | **Unverified** — L1 has never run | **Unknown** |

**Terminal state: `result` with one marginal and one unknown.**

### 5.1 What the audit exposed

**R3 is satisfiable by a label that carries no information.** "Siblings" appears in
nearly every related block in this corpus, including this page's. It is not in the
E3 blocklist — it is not "See also" — and it states a **filing fact** rather than a
relationship the reader can use. A reader does not open "Siblings" because they
know what it offers; they open it because they have run out of options.

So R3 as drafted is under-specified. The rule requires a "relationship label" and
does not require that the relationship be **to this page**. Stated as a
clarification, in-text, per [ST-17 W6](st-17-worked-instance-standard.md):

> **R3, clarified.** A group label must state the relationship between the linked
> instruments **and this page**. A label stating a property of the linked
> instruments alone ("Siblings", "Other standards", "Registries") is
> non-compliant. The compliant form names what those instruments do *for a reader
> of this page* — e.g. "Registries a reader may have wanted instead".

This is a substantive amendment to the standard made in the act of first
publication, and it puts **most related blocks in this corpus into breach of R3**,
including the one below. Filed rather than retro-fitted silently.

### 5.2 The counter-instance ST-17 W5 requires

The audit above largely passed, so a failing case is owed.

[SITE-01 route manifest](../site/route-manifest.md): its related block is
structurally fine and its exit pair, per
[RB-03 §6](../rubrics/rb-03-instrument-quality-rubric.md), sits on a page scored
**Q3 = 2** — an instrument that needed a *sibling*
([REG-02](../registries/reg-02-page-registry.md)) to make its adverse disclosure
that most of its 321 routes have no page.

Under **R7**, SITE-01's exit pair should have pointed at exactly that. An adverse
exit on SITE-01 reading *"Count the pages behind these routes — most do not exist"*
would have discharged R7 **and** raised the page's Q3 from 2 to 3, because the
disclosure would be on the instrument that owes it rather than on a neighbour.

That connection was not designed: R7 (page furniture) and
[RB-03](../rubrics/rb-03-instrument-quality-rubric.md) Q3 (disclosure quality) were
written independently, and the audit shows **R7 is a mechanism for discharging Q3**.
A well-built exit pair is not decoration at the bottom of a page; it is where an
instrument's self-criticism becomes actionable. That is the strongest available
argument for R7 and it emerged from the counter-instance, not from the design.

## 6. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Padding to meet the count** | Guarded by R4; **unverifiable** — only the author knows why a link is there |
| F2 | **Generic group labels** | Guarded by R3 + E3 blocklist |
| F3 | **Uninformative label passing R3** | **Actual** — "Siblings", §5.1; now non-compliant |
| F4 | **Both exits self-serving** | Guarded by R7; the temptation on an unflattering page |
| F5 | **Stale related links** | **Unknown at scale** — E4 never run |
| F6 | **Exit pair as two links** | Guarded by R6 |
| F7 | **Fault group omitted** | **Widespread** — §3.2 group 3 is the one skipped |
| F8 | **Absolute paths** | Would break the portable archive ([MX-019](../corpus/mx-019-sunset-and-wind-down.md)) |

## 7. Limits

1. **No check runs.** Five specified, zero implemented — and E1–E3 are
   counting exercises. This is the cheapest unbuilt check set in the corpus
   ([ST-13](st-13-static-build-and-sentinel.md)).
2. **E4 unverified means the whole standard is formal.** The estate can prove it
   has eight links per page and cannot prove one of them works.
3. **R3 as first drafted was under-specified** and the clarification in §5.1 puts
   most existing blocks in breach.
4. **R4 is unverifiable from outside.** Whether a link is decorative depends on the
   author's reason for including it.
5. **The counts — four, eight, two — are asserted**, inherited from
   [SITE-02](../site/page-contract.md)'s acceptance criteria, and not derived from
   any observation of reader behaviour. The estate cannot observe reader behaviour
   ([REG-06 `DSET-R01`](../registries/reg-06-dataset-registry.md)), so these numbers
   are **E0** and will remain so.
6. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** This standard is falsified if:
>
> - **(a)** a page has other than four related groups, or fewer than eight links
>   (R1, R2) — **countable by any reader in seconds**;
> - **(b)** a group label states a property of the linked instruments rather than
>   their relationship to the page (R3 as clarified) — **fires now, widely**,
>   including on this page (§5.1);
> - **(c)** a page has other than exactly two exit actions (R5);
> - **(d)** neither exit action is adverse (R7);
> - **(e)** any related link fails to resolve (R8, E4) — **the estate cannot
>   predict the result**, having never run L1;
> - **(f)** a link is shown to exist only to satisfy the count (R4).
>
> **(a), (b), (c) and (d) are all runnable by a reader on a single page with no
> tools**, which makes this the most easily falsified standard in the corpus — by
> design. Furniture rules should be checkable by counting.

## 9. Obligation

**On an author:**
- Exactly four groups, ≥ 8 links, ≥ 2 per group (R1, R2).
- Label by the relationship **to this page** (R3 as clarified in §5.1).
- Include the **"where its faults are recorded"** group (§3.2); it is the one
  omitted, and its omission is a disclosure failure
  ([RB-03](../rubrics/rb-03-instrument-quality-rubric.md) Q3).
- Strike decorative links even if the count drops; then find real ones (R4, §4.1).
- Exactly two exit actions, each with an imperative and a consequence (R5, R6).
- Make at least one exit **adverse** (R7) — it discharges
  [MX-017](../corpus/mx-017-conflicts-of-interest.md) S4 and lifts Q3.
- Relative paths only (R8).

**On the estate:**
- Implement **E1, E2, E3** — counting and a blocklist, the cheapest checks in the
  corpus (§7.1).
- Run [ST-08 L1](st-08-cross-reference-and-link-integrity.md) so E4 becomes
  answerable; until then this standard is formal only.
- Bring existing group labels into R3-as-clarified compliance, and log it as an
  amendment rather than a tidy-up (§5.1).
- Keep the four/eight/two counts labelled **E0** (§7.5).

---

### Related

**The contract requiring this furniture** — [SITE-02](../site/page-contract.md) ·
[ST-24](st-24-page-prose-standard.md) ·
[SITE-01](../site/route-manifest.md) ·
[ST-16](st-16-audience-tier-standard.md)

**Link integrity this depends on** — [ST-08](st-08-cross-reference-and-link-integrity.md) ·
[ST-13](st-13-static-build-and-sentinel.md) ·
[DEF-001](../00-governance-map/defect-register.md) ·
[MX-019](../corpus/mx-019-sunset-and-wind-down.md)

**Why an adverse exit is owed** — [MX-017](../corpus/mx-017-conflicts-of-interest.md) ·
[RB-03](../rubrics/rb-03-instrument-quality-rubric.md) ·
[ST-06](st-06-objections-standard.md) ·
[ST-04](st-04-falsifiability-and-claim-cards.md)

**Standards a reader of this page may have wanted instead** —
[ST-17](st-17-worked-instance-standard.md) ·
[ST-09](st-09-summary-and-abstract-standard.md) ·
[ST-10](st-10-terminology-and-definition-standard.md) ·
[ST-15](st-15-amendment-and-versioning-standard.md)

### Exit pair

1. **Count this page's furniture.** Four groups, eight links, two actions —
   falsifiers §8(a) and (c) take seconds and need nothing.
2. **Catch this page in breach.** §5.1 clarified R3 so that labels naming a
   property rather than a relationship fail. The fourth group above was rewritten
   to comply; check whether the other three do.

<!-- mx-pagestamp: ST-18 · v2026.10.1 · operative-form · tier 5 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; no related link in the corpus has been verified to resolve -->
