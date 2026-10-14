---
doc_id: "SITE-08"
title_en: "SITE-08 · The Decision Queue: Specification"
title_ar: "SITE-08 · طابور القرارات [AR-DRAFT]"
family: "site"
version: "v2026.10.3"
status: "draft"
authority: "operative-form"
prevailing_text: "en"
audience_tier: 3
depth: 4
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-08"
domain_tags: ["site", "decision-queue", "governance", "accountability", "service-targets", "static"]
route: "/about/governance/queue/"
human_read: "none"
conformance_state: "unmet"
derived_from: "MX-001 §1.2 ('Determination Queue … the one that costs something'); LEX-05 CT-08 (rename to Decision Queue); UI-UX source §12; GM-04; ML-2.3 §H.2-bis.4 (determinations); ST-14; ST-19"
authorship_note: "Drafted by an AI system under AG-000 to close GM-17 M-24. Names follow the LEX-05 CT-08 recommendation (Decision Queue), pending RAT-28(f). Service targets are proposals: the figures are the Curator's to set."
hreflang: "en, ar"
---

# SITE-08 · The Decision Queue

> **Authority.** An **operative form** (tier 7) for one surface. [MX-001 §1.2](../corpus/mx-001-about-metax.md)
> requires the surface to exist "as a condition of publishing anything else". It links to a pointer
> stub (`page-spec-hub.md`). This file is the specification that link lacked.

> **Disclosure first.**
> - (1) **Name.** MX-001 calls it the *Determination* Queue. ML-2.1 Part D uses "Determination" narrowly, for a compatibility or conformity ruling. LEX-05 CT-08 recommends **Decision Queue** for the broad surface, and this file uses that name. The ruling is RAT-28(f).
> - (2) **The service targets in §4 are placeholders** proposed by an agent. MX-001 makes the Curator's own performance falsifiable by a stranger, so **only the Curator can set the figures he will be measured against.** An agent setting them would be HX-18 in miniature.
> - (3) If built today, the queue would hold **at least 44 open Curator questions** (RAT-01…38 and RAT-B-01…06, less those answered), most past any plausible target. Every item would turn red on the first build. **That is the honest outcome, and the specification forbids softening it** (§6).

---

## 1. What the queue holds

Every matter awaiting a decision by a named natural person, of these classes:

| Class | Source | Example |
|---|---|---|
| `ratification` | GM-04 RAT-nn, RAT-B-nn | RAT-29 BX-000 holder |
| `blocker` | GM-05 B-nn | B-01 sign ML-2.3 |
| `licence-determination` | ML-2.3 §H.2-bis.4, `/determinations/` | A Licensee's tier request |
| `objection` | ST-06 | An objection to an instrument |
| `comment-period` | CPF-1 | Unanswered comments at close |
| `correction-request` | GM-07 | A filed correction awaiting acceptance or rejection |
| `ethics-review` | MX-000 §0.5.1 | *(no holder; see §5)* |
| `appeal` | MX-025 | A credential decision appealed |

**Excluded:** anything concerning a person's private data. An appeal appears as `appeal · id · dates · state`, with no name and no content, unless the appellant opts in.

## 2. Row model

```json
{"id": "RAT-29", "class": "ratification", "title": "Final holder of BX-000",
 "opened": "2026-09-30", "decider": "Maher", "target_days": null,
 "age_days": 8, "state": "open|decided|declined|withdrawn",
 "timer": "none|green|amber|red", "intervals_survived": 0,
 "source_instrument": "GM-04", "anchor": "/library/record/open-questions/#rat-29",
 "decided_on": null, "decision_record": null}
```

- `age_days` and `intervals_survived` are **computed at build time**, never typed.
- `decision_record` links a [GM-20](../license/decision-record-register.md) row where the decision amends an instrument.

## 3. Rendering

- **Static.** Generated from the governance-map Markdown at build. No JavaScript is required to read it (ST-19). Also emitted as `/data/queue.json` with the ST-14 envelope.
- Sorted by **age, oldest first**. Not by importance, which would let the decider choose what is seen.
- Each row shows id, class, title, age in days, intervals survived, timer and decider.
- Counts shown at the head: open · red · amber · decided in the last 90 days · median age.

## 4. Timers *(placeholders; the Curator sets the figures, RAT-42)*

| Class | Green until | Amber until | Red after |
|---|---|---|---|
| `licence-determination` | *[C: e.g. 30 days]* | *[C]* | *[C]* |
| `objection`, `correction-request` | *[C: e.g. 30]* | *[C]* | *[C]* |
| `ratification`, `blocker` | *[C: e.g. 90]* | *[C]* | *[C]* |
| `comment-period` | 30 days after close (CPF-1 §6) | — | after 30 |

**Until the Curator sets figures, the timer shows `none`, and the page head says so in one sentence.** A
queue with no targets is a list, not an accountability mechanism, and it must not look like one.

## 5. The class that has no decider

`ethics-review` rows show the decider as **"unheld (M-03)"**, and the timer is **red from opening**. A
decision that structurally cannot be made is shown as overdue from the start. It is never shown as pending.

## 6. Prohibitions

1. **No item may be removed** except by decision, decline or withdrawal, and each of those is recorded. A declined item stays visible with its reason.
2. **No timer may be paused**, reset or re-based by editing an item.
3. **No re-classing** an item to a class with a longer target.
4. **No colour, wording or ordering change that makes a red item less visible.**
5. **No engagement telemetry** on the page (MX-023, ST-14 §2.1).

## 7. Falsifier

The queue has failed if a stranger can find a pending decision in GM-04, GM-05, the CPF-1 registers
or `/determinations/` that is not on the queue. It has also failed if any red item turns green without
a recorded decision.

## 8. Build dependency

The queue needs the build (M-32, DEF-001). **Until there is a build, the queue does not exist**, and
MX-001 §1.2's "four things, continuously, as a condition of publishing anything else" is unmet for
this surface. That is a launch condition, proposed as **B-26**.

---

**Related:** [MX-001 §1.2](../corpus/mx-001-about-metax.md) · [Open questions](../00-governance-map/open-questions-and-ratifications.md) · [Launch Blockers](../00-governance-map/launch-blockers.md) ·
[CPF-1](../license/cpf-1-comment-period-publication-format.md) · [GM-20](../license/decision-record-register.md) · [LEX-05 CT-08](../lexicon/contested-terms.md) · [ST-14](../standards/st-14-machine-surfaces-and-json-schemas.md)
