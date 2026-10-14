---
doc_id: BX-008
title_en: BCIA and Machine Readers
title_ar: BCIA والقراء الآليون
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
domain_tags: [bcia, machine-readers, ai, phases, retrieval]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000, class I-1. The page describes how machine readers encounter this corpus, written by one — which makes §5 introspection, the least reliable evidence class available.
route: /bcia/machine-readers/
---

# BX-008 — BCIA and Machine Readers

> **This page will not resolve:** how any specific AI system actually processes
> this corpus. It reasons from one system's structure, disclosed as introspection
> ([§7.2](#7-limits)).

> **Authority.** `companion`. The binding machine-reading duties are
> [GM-11](../00-governance-map/machine-reading-contract.md) and
> [ST-14](../standards/st-14-machine-surfaces-and-json-schemas.md).

> **Disclosure first.** [GM-11](../00-governance-map/machine-reading-contract.md)
> sets five conditions on a machine reader and six signals the corpus owes —
> **three delivered**. [ST-14](../standards/st-14-machine-surfaces-and-json-schemas.md)
> specifies nine surfaces, **refuses three**, and **none exists**. So this page
> describes the phases of a reader the corpus has not yet built for.

---

## 1. Position

[BX-000](bx-000-bcia-charter.md)'s four phases were derived from human reading.
Machine readers traverse them too, and **differently enough that the corpus's
phase remedies land in the wrong places**.

The corpus already recognises a machine audience:
[ST-16 §2.1](../standards/st-16-audience-tier-standard.md) defines **tier 4** as a
machine reader bound by
[GM-11](../00-governance-map/machine-reading-contract.md)'s five conditions. It
records that tier 4 content is **empty** — nine surfaces specified, none built.

So the corpus has a named audience, a contract for it, and nothing addressed to it.

### 1.1 Why this is urgent rather than theoretical

[MX-018 D5](../corpus/mx-018-third-party-dependencies.md) records that an AI
system authored essentially this entire corpus. That system read the corpus to
write it. **The corpus's most active reader to date has been a machine**, and
nothing in the estate was designed for that.

## 2. How the phases differ for a machine

| Phase | Human | Machine |
|---|---|---|
| **B** Before | Decides whether to read; seconds; can be deterred | **Retrieval.** A matcher selects the page. No deterrence, no judgement |
| **C** Contact | Reads linearly; fluency risk | **Ingestion.** Often partial — a section, not a page |
| **I** Internalisation | Relates to one or two held things | **Context assembly.** Relates to whatever else was retrieved, which may be arbitrary |
| **A** After | Acts, may return | **No return.** No session memory ([AG-006](../agents/ag-006-agent-session-and-state.md)) |

### 2.1 Phase B inverts

For a human, phase B is where a reader is **lost** — deterred, or arriving at the
wrong page ([BX-001 §1](bx-001-before-phase.md)).

For a machine, phase B is **retrieval**, and the failure is opposite: the machine
is **not deterred by anything**. It does not read the disclosure block and decline.
It takes what matched.

Consequence: every phase B remedy in
[BX-006](bx-006-phase-failure-catalogue.md) — PF-1's opening line, PF-2's visible
tier, PF-3's early exclusions — is **useless against a machine reader**, because
all three work by helping a reader *decide not to proceed*, and a retrieval system
has already proceeded.

What works instead is **structure**: fields a matcher can filter on, which is
precisely [ST-14](../standards/st-14-machine-surfaces-and-json-schemas.md)'s nine
surfaces, none of which exists.

### 2.2 Phase C fragments

A human reads a page. A machine frequently ingests a **fragment** — a matched
section, a table, a heading and its paragraph.

This defeats the eight-part recipe's central property. The parts work as a
sequence: Mechanism is qualified by Limits, the Worked instance is qualified by its
terminal state, claims are qualified by Falsifier. **A fragment arrives
unqualified.**

Worked example of the risk: a machine retrieving
[MX-002 §5](../corpus/mx-002-terms-of-service.md) — *"May read, quote, reuse"* —
without §5's first line deferring entirely to
[ML-2.3](../license/the-maher-license.md), and without §8's trace to
`indeterminate`.

The corpus's defence is **in-section self-qualification**: each section carrying
enough of its own limit that a fragment is not misleading alone. This corpus does
that unevenly and has never made it a rule.

### 2.3 Phase A does not exist

A machine reader has no After. No return, no correction discovery, no staleness
check on a later date ([AG-006](../agents/ag-006-agent-session-and-state.md) gap
5).

Every phase A mechanism the corpus has — next review date in the stamp, the
corrections log, version stamps — **assumes a returning reader**. A machine never
returns; a *new instance* arrives with no knowledge that a prior one read anything.

So for machine readers the corpus's entire phase A apparatus is inert, and the
whole burden shifts to **phase C**: whatever qualification the fragment carries at
ingestion is all the qualification there will ever be.

## 3. What the corpus owes a machine reader

| # | Obligation | [GM-11](../00-governance-map/machine-reading-contract.md) signal? | State |
|---|---|---|---|
| **M1** | Authority class machine-readable | Yes | **Met** — front matter |
| **M2** | Version and currency machine-readable | Yes | **Met** |
| **M3** | Summary content marked subordinate | Yes ([ST-09 §4.2](../standards/st-09-summary-and-abstract-standard.md)) | **Met in prose, not in structure** |
| **M4** | Evidence class per claim | Owed | **Unmet** — E-classes are prose |
| **M5** | Section-level self-qualification | Owed | **Unmet** — §2.2 |
| **M6** | Defect linkage per instrument | Owed | **Unmet** — PF-11 |

Three of six delivered, matching
[GM-11](../00-governance-map/machine-reading-contract.md)'s own count.

### 3.1 M4 is the one that matters most

[ST-07](../standards/st-07-evidence-and-verify.md) classes claims E0–E4, and the
corpus uses them constantly — *"this claim is E0"*, *"E1 at best"*.

They are **prose**. A machine ingesting a claim gets the claim; it gets the
evidence class only if the sentence happens to be in the fragment.

So the corpus's principal honesty mechanism — labelling how well-supported each
claim is — is **the mechanism least likely to survive machine ingestion**, because
it is carried in sentences adjacent to claims rather than attached to them.

## 4. Mechanism — writing for a fragment

```
for each section, ask:
  if ONLY this section were retrieved, would it mislead?
     yes → add the qualifying clause INSIDE the section
  does the section state a claim?
     yes → state its evidence class IN the section, not elsewhere
  does the section state a permission or an obligation?
     yes → name the governing instrument IN the section
```

This is a **practice**, not a duty — BCIA creates none
([BX-000 §1.1](bx-000-bcia-charter.md)). But unlike most of
[BX-006](bx-006-phase-failure-catalogue.md)'s remedies it is **free** under
[BX-006 §4.1](bx-006-phase-failure-catalogue.md)'s gates: no standard amended, no
ratification, no reader data.

## 5. Worked instance

**Testing fragment-safety on three sections of one page.**

Take [REG-05 credential registry](../registries/reg-05-credential-registry.md),
whose central fact is that **no credential has been issued and none currently can
be**.

| Fragment retrieved | Misleading alone? |
|---|---|
| §2 "A credential is… seven conditions" | **Yes.** Reads as a live credentialling scheme. Nothing in §2 says none has been issued |
| §3.3 "Until stage 2 can be staffed, the estate must not issue credentials" | **No** — self-qualifying |
| §5 "The register contains no rows" | **No** — self-qualifying |

**Terminal state: `result` — one of three fragments misleads.**

### 5.1 The finding

§2 is a **definition section**, and definition sections are systematically the
most fragment-unsafe part of the eight-part recipe.

The reason is structural. [ST-24](../standards/st-24-page-prose-standard.md)'s
Definition part states **what a thing is**, and the qualification — that the thing
does not exist here, or cannot operate — lives in Mechanism, Limits, or the
disclosure block. A definition is written in the present indicative
(*"a credential is…"*) and reads, alone, as a description of something operating.

This is not confined to REG-05. Across the corpus, Definition sections describe
processes that [DEF-031](../00-governance-map/defect-register.md) establishes
**cannot run**: [MX-016](../corpus/mx-016-appeals-and-due-process.md)'s three
appeal stages, [RB-05](../rubrics/rb-05-harm-review-gate.md)'s review gate,
[AG-011](../agents/ag-011-agent-review-and-audit.md)'s four review levels. Each
definition is accurate; each is fragment-unsafe; and a machine reader retrieving
any of them learns that the estate has an appeals process.

Filed per [ST-17 W6](../standards/st-17-worked-instance-standard.md):

> **Finding BX-008/1.** Definition sections are the corpus's most fragment-unsafe
> part, because they state what a thing **is** while the fact that it does not
> operate lives elsewhere on the page. The free remedy is one clause inside each
> Definition section that describes an inoperative process — *"…; no such review has
> ever occurred"*. This affects an estimated dozen instruments and requires no
> amendment. Filed as practice, and as an addition to
> [BX-006](bx-006-phase-failure-catalogue.md)'s free list.

### 5.2 Why this was invisible

[BX-005](bx-005-phase-audit-method.md)'s sixteen questions audit a **page**. Every
one of them assumes the whole page is read.

There is no question in the phase audit that asks *"would this section mislead
alone?"*, because the audit was derived from human phases where fragmentation does
not occur. So the corpus's own diagnostic is **structurally unable to find
fragment-unsafety** — the same shape as
[BX-005 §5.1](bx-005-phase-audit-method.md)'s finding that
[RB-03](../rubrics/rb-03-instrument-quality-rubric.md) cannot see phases B and I.

**Three times now**, an assessment instrument in this estate has been found blind
to a class of failure it was not built to see. That is a pattern, and it suggests
the right response is not another instrument but a standing expectation: **every
diagnostic here has a blind spot, and finding it is more valuable than applying
it.**

## 6. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Phase B remedies useless against retrieval** | **Actual** — §2.1 |
| F2 | **Fragment arrives unqualified** | **Actual** — §2.2, §5 |
| F3 | **Evidence class lost in ingestion** | **Actual** — §3.1 |
| F4 | **Phase A apparatus inert for machines** | **Structural** — §2.3 |
| F5 | **Definition sections describe inoperative processes** | **Actual, ~12 instruments** — §5.1 |
| F6 | **Phase audit cannot detect fragment-unsafety** | **Actual** — §5.2 |
| F7 | **No machine surfaces exist** | **Actual** — [ST-14](../standards/st-14-machine-surfaces-and-json-schemas.md) |

## 7. Limits

1. **No machine reader's behaviour has been observed.** Retrieval and
   fragmentation are described from general structure, not measurement.
2. **§5 is introspection.** An AI system describing how AI systems read is the
   least reliable evidence available — worse than self-report, since the system
   cannot observe its own retrieval. **E0.**
3. **Nine machine surfaces remain unbuilt**, so M4–M6 have no delivery mechanism
   even if adopted.
4. **The four-phase mapping to machine behaviour is asserted.**
5. **"~12 instruments" in §5.1 is an estimate**, prohibited as a precise figure
   under [AG-003 O3](../agents/ag-003-agent-output-standards.md) and stated as an
   estimate accordingly.
6. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** a machine reader is shown to be deterred at phase B by prose
>   disclosure — which would restore PF-1, PF-2 and PF-3 for machine audiences
>   (§2.1);
> - **(b)** a Definition section is shown to be fragment-safe without an internal
>   qualifying clause (§5.1);
> - **(c)** [BX-005](bx-005-phase-audit-method.md)'s sixteen questions are shown to
>   detect fragment-unsafety — **checkable in two minutes** against BX-005 §2, and
>   would defeat §5.2;
> - **(d)** a machine reader is shown to return to a page and detect a correction
>   (§2.3);
> - **(e)** the three-blind-diagnostics pattern in §5.2 is shown to be coincidence.
>
> **(c) is cheapest.** **(b) is the most useful**: if one Definition section is
> genuinely safe alone, the remedy is narrower than §5.1 claims.

## 9. Obligation

None — a companion. For navigation:

- Adopt the §4 fragment practice; it is **free** under
  [BX-006 §4.1](bx-006-phase-failure-catalogue.md)'s gates.
- Add **BX-008/1** to [BX-006](bx-006-phase-failure-catalogue.md)'s free list
  (§5.1) — a qualifying clause in every Definition section describing an
  inoperative process.
- State evidence classes **inside** the section carrying the claim (M4, §3.1).
- Build the [ST-14](../standards/st-14-machine-surfaces-and-json-schemas.md)
  surfaces, or record tier 4 as deferred rather than planned.
- Treat §5.2's pattern as standing: **look for each diagnostic's blind spot before
  trusting its output.**

---

### Related

**Binding machine-reading duties** —
[GM-11](../00-governance-map/machine-reading-contract.md) ·
[ST-14](../standards/st-14-machine-surfaces-and-json-schemas.md) ·
[ST-16](../standards/st-16-audience-tier-standard.md) ·
[ST-09](../standards/st-09-summary-and-abstract-standard.md)

**The phases reinterpreted** — [BX-000](bx-000-bcia-charter.md) ·
[BX-001](bx-001-before-phase.md) · [BX-004](bx-004-after-phase.md) ·
[BX-005](bx-005-phase-audit-method.md)

**Why the machine reader matters here** —
[MX-018](../corpus/mx-018-third-party-dependencies.md) ·
[AG-006](../agents/ag-006-agent-session-and-state.md) ·
[MX-007](../corpus/mx-007-ai-use-and-disclosure.md) ·
[AG-002](../agents/ag-002-agent-disclosure-obligations.md)

**The fragment-unsafe pages** —
[REG-05](../registries/reg-05-credential-registry.md) ·
[MX-016](../corpus/mx-016-appeals-and-due-process.md) ·
[RB-05](../rubrics/rb-05-harm-review-gate.md) ·
[AG-011](../agents/ag-011-agent-review-and-audit.md)

### Exit pair

1. **Retrieve one section and judge it.** Read
   [REG-05 §2](../registries/reg-05-credential-registry.md) alone. §5 says it
   reads as a live credentialling scheme; falsifier §8(b) is yours.
2. **Watch the pattern, not the page.**
   [§5.2](#52-why-this-was-invisible) — three diagnostics in this estate have now
   been found blind to what they were not built to see.

<!-- mx-pagestamp: BX-008 · v2026.10.1 · companion · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; none of the nine machine surfaces exists -->
