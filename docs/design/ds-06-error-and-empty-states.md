---
doc_id: "DS-06"
title_en: "Error, Empty and Degraded States"
title_ar: "حالات الخطأ والفراغ والتدهور"
family: "design-system"
version: "v2026.09.2"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 3
evidence_class: "semi-durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.1"
derived_from: ["MX-DESIGN-001 Part 10"]
last_reviewed: "2026-08-30"
domain_tags: ["design", "accessibility", "analytics"]
ai_disclosure_url: "../corpus/mx-007-ai-use-and-disclosure.md"
hreflang: "en, ar"
---

# DS-06 — Error, Empty and Degraded States

**Governs:** what the estate says when something is missing, broken, or unavailable — including
when MetaX itself is the thing that is degraded.

These are the states an institution reveals itself in. A corpus can be careful on its doctrine
pages and still tell a reader, on a 404, that the reader did something wrong.

---

## §6.1 Error pages — the fixed order

Every error page states four things, **in this order**:

1. **What happened**
2. **What it means**
3. **What the visitor can do**
4. **Who to contact**

**Without apology inflation.** One "sorry" at most, and only where MetaX is actually at fault. A
page that opens with three sentences of regret has delayed the information the reader came for,
and repeated apology reads as a substitute for a fix.

The order is normative because it is the order of decreasing usefulness. A reader who leaves after
one line should have received the most valuable line.

### §6.1.1 Never blame the user

`auth./error` *"explains failure classes in plain language and never blames the user."* This
generalises to the estate: no error copy attributes cause to the reader unless the reader can act
on the attribution. "Your code has expired — request a new one" is actionable. "You entered an
invalid code" is an accusation with no next step.

---

## §6.2 The 404 routes intelligently

A 404 in this estate is usually not a typo — it is a **superseded identifier**, because identifiers
here are immortal and content is versioned
([ST-01](../standards/st-01-identifier-and-url-grammar.md)).

So: **an unknown `/s/{id}/` looks up the identifier and offers the archived or superseded page if
one exists.**

| Case | Behaviour |
|---|---|
| Identifier exists, content archived | Offer the archived page, with its supersession date |
| Identifier exists, superseded by another | Offer the successor **and** the archived original |
| Identifier exists, never published | State that plainly. Do **not** imply it is coming |
| Identifier is `PREVIEW` or `PENDING INGESTION` | State the status and link the registry row |
| Identifier does not exist | Ordinary 404 with search |

The fourth row matters more than it looks. Book 7, 8 and 10 chapters are `[PENDING INGESTION]`
and Book 9 carries `[GAP IN SOURCE]`
([REG-03](../registries/reg-03-book-registry.md)). A reader arriving at one of those must be told
which of the two it is, because "not ingested yet" and "the source itself is incomplete" are
different facts about MetaX, and only one of them is a promise.

---

## §6.3 Empty states

**In `me.`:** written as **invitations with a single action** — never as scolding, and never
implying the reader is behind.

There is a specific temptation to refuse here. An empty dashboard is the natural place to put
motivational pressure, and pressure is what
[Charter §0.4.1](../corpus/mx-000-charter.md#1-attention-economic-mechanics) refuses. "You haven't
submitted an artefact yet" is a scold; "Choose a series to begin" is an invitation. The difference
is whether the sentence is about the reader's past or their next step.

**On the content plane:** an empty registry, catalog facet or search result states the fact and
does not manufacture a suggestion. Zero results is information.

---

## §6.4 Degraded states — when MetaX is the failure

### §6.4.1 Degraded mode

Under [AG-000 §A.6](../agents/ag-000-agent-constitution.md#a6-degraded-mode-and-prompter-succession),
the [Determination Queue](ds-04-academic-features.md#12--the-determination-queue) at
`/about/governance/queue/` **displays the degraded banner and the reduced authority ceiling.**

This is unusual and deliberate: the estate publishes its own reduced capacity on the page where
governance decisions are tracked, rather than letting service targets slip silently. The
escalation timer *"turns amber then red in public when a target is missed"* — including when the
reason is that the Curator is unavailable.

### §6.4.2 Missed decay reviews

A page past its review date says so **on its own face**, not only in the Decay Watch aggregate
([ST-05](../standards/st-05-decay-and-review-intervals.md)). The chip is one of the four T3
looping elements ([DS-02 §1](ds-02-motion-and-attention.md#t3--persistent-signal)).

### §6.4.3 Untranslated pages

A page with no Arabic mirror renders the **honest untranslated notice with a target date**. **No
language toggle resolves silently to a homepage** — a silent redirect tells a bilingual reader
that the estate has parity when it does not
([B-09](../00-governance-map/launch-blockers.md#b-09--arabic-parity-is-claimed-but-not-built--soft-blocker)).

### §6.4.4 The island failing

Nothing. By contract, an island failure produces **no visible state at all**: no error, no retry
prompt, no degraded banner. The page is the page an anonymous visitor sees
([ST-19 §3.4](../standards/st-19-two-plane-architecture.md#34-failure-transparency-and-how-it-is-proved)).

This is the one place in this document where the correct error state is **silence** — because the
identity bar is decoration, and announcing the absence of decoration would make it load-bearing.

---

## §6.5 Analytics posture

| Rule | |
|---|---|
| Aggregate, **cookieless** | |
| **No per-user tracking on the content plane** | |
| **No third-party tags anywhere** in the estate | Including `auth.` and `pay.` |
| Metrics collected are **published** on the accessibility and integrity pages | *"So the measurement itself is inspectable"* |

The last row is the one that costs something. Publishing which metrics MetaX collects means a
reader can check that the list has not grown — and that the estate is not quietly measuring
engagement while refusing to optimise for it.

---

## §6.6 Conformance

| Rule | Enforced by | Failure |
|---|---|---|
| Four-part error structure, in order | Template gate on every error route | Build failure |
| 404 identifier lookup resolves archived/superseded pages | Route test against the registries | Build failure |
| No third-party tag on any host | Network-request audit at build | Build failure |
| Untranslated notice present where a mirror is absent | Bilingual gate | Build failure |
| Island failure produces no visible state | Island-disabled differential build | Build failure |
| Published metrics list matches metrics collected | Manual review at each release | Public defect |

---

**Related:** [DS-02 Motion and Attention](ds-02-motion-and-attention.md) ·
[ST-19 Two-Plane Architecture](../standards/st-19-two-plane-architecture.md) ·
[ST-05 Decay and Review Intervals](../standards/st-05-decay-and-review-intervals.md) ·
[MX-010 Accessibility](../corpus/mx-010-accessibility.md) ·
[AG-000 §A.6](../agents/ag-000-agent-constitution.md#a6-degraded-mode-and-prompter-succession) ·
[REG-03 Book Registry](../registries/reg-03-book-registry.md)

*Curated by Maher. An institution is legible in its failure states. These are written so that a
reader who arrives at a broken page learns something true about MetaX rather than something
soothing.*
