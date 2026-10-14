---
doc_id: MX-006
title_en: Contact and Correspondence
title_ar: الاتصال والمراسلات
family: corpus
version: v2026.10.1
status: published
authority: governing
prevailing_text: ar
audience_tier: 1
depth: micro
evidence_class: perishable
review_interval_months: 3
curator: Maher
license: ML-2.3
designated: yes
last_reviewed: 2026-09-16
domain_tags: [contact, correspondence, notice, reporting, response]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. The response commitments below are made by one person with no cover.
provenance_of_purpose: Required by MX-002, MX-003, MX-008, MX-016 and ML-2.3 §F.4, each of which assumes a working channel; absent until v2026.10.1.
route: /contact/
---

# MX-006 — Contact and Correspondence

> **Authority.** `governing`, tier 3. Five instruments depend on a working
> channel: [MX-002](mx-002-terms-of-service.md),
> [MX-003](mx-003-privacy-notice.md),
> [MX-008](mx-008-moderation-and-enforcement.md),
> [MX-016](mx-016-appeals-and-due-process.md), and
> [ML-2.3 §F.4](../license/the-maher-license.md), whose 30- and 90-day cure
> periods **run from notice** and therefore cannot operate without one.

> **Disclosure first.** Correspondence is received and answered by **one person**,
> who is also the author of everything you might write about, the assessor of any
> work, and the decider of any appeal
> ([REG-08](../registries/reg-08-role-and-authority-registry.md)). There is no
> cover for absence, no escalation above the curator, and no independent recipient.
> Every response time below is a commitment without redundancy, and §7 states what
> happens when the one person is unavailable: **nothing happens.**

---

## 1. Position

This is the smallest instrument in the corpus and the one most other instruments
lean on. That asymmetry is the whole problem.

A cure period that runs from notice requires a notice mechanism whose receipt can
be established. A defect report duty requires somewhere to report. An appeal
requires a filing address. The estate wrote all three duties before writing this
page, which is recorded in `provenance_of_purpose` and is a straightforward
ordering failure: **the obligations preceded the channel by the estate's entire
prior life.**

## 2. Definitions

| Term | Meaning | Why it matters |
|---|---|---|
| **notice** | A communication that starts a period running under a governing instrument | [ML-2.3 §F.4](../license/the-maher-license.md) cure clocks |
| **report** | A communication asserting a defect, harm, or breach | [MX-013 §4](mx-013-records-and-versioning.md) filing duty |
| **appeal** | A communication contesting a decision | [MX-016](mx-016-appeals-and-due-process.md) |
| **enquiry** | Anything else | No period runs |
| **receipt** | The estate's acknowledgement that a communication arrived | §4.2 |

### 2.1 Notice is not the same as an enquiry

The classes have different consequences and a sender should say which they intend.
A message that does not say is treated as an **enquiry**, which starts no clock.
This default protects the sender from nothing and the estate from a great deal,
and the estate says so rather than presenting it as neutral drafting.

A sender who intends **notice** should write the word *notice* and cite the
provision relied on. The estate will not reclassify a message upward on the
sender's behalf.

## 3. The channels

| Channel | Address | Accepts | Receipt issued? |
|---|---|---|---|
| **Public record** | The [defect register](../00-governance-map/defect-register.md) and repository history | Reports of any kind, permanently visible | **Yes — by publication** |
| **Curator** | As published at `/contact/` on the live site | Notice, report, appeal, enquiry | §4.2 — **best efforts only** |
| **Contact form** | **none** | — | — |
| **Telephone** | **none** | — | — |
| **Postal address** | **none published** | — | — |
| **Social channels** | **none** | — | — |

### 3.1 Why there is no form

A contact form is a collection mechanism. It requires storage, a retention
condition, and a prior written question under
[REG-06 §3.1](../registries/reg-06-dataset-registry.md). The estate has no
justified dataset for correspondents and would have to open one.

The consequence is a real cost to a sender: there is no structured intake, no
ticket number, and no status view. The estate's substitute is the **public
record** — a report filed publicly cannot be lost, ignored without trace, or
denied. That is a weaker convenience and a stronger accountability, and a sender
choosing between channels should understand the trade rather than have it chosen
for them.

### 3.2 Why the public record is listed first

It is the only channel whose receipt is **self-proving**. A report in the public
record is timestamped by the record itself and cannot be silently discarded. For
anything a sender might later need to establish, the public record is the better
channel, and it is listed first for that reason rather than as a deflection.

## 4. Mechanism

### 4.1 Classification on arrival

```
message arrives
  → does it say "notice" and cite a provision?   yes → NOTICE, clock starts
  → does it assert a defect, harm, or breach?    yes → REPORT, filing duty engages
  → does it contest a decision?                  yes → APPEAL, MX-016 stages
  → otherwise                                         ENQUIRY, no clock
```

### 4.2 Response commitments

| Class | Acknowledge within | Substantive response within | Published? |
|---|---|---|---|
| **Notice** | 7 days | Per the governing provision's own period | Only if it results in a correction or defect |
| **Report** | 14 days | **Filed in the defect register regardless of agreement** | **Yes — always** |
| **Appeal** | 14 days | [MX-016](mx-016-appeals-and-due-process.md) stage periods | Outcome published |
| **Enquiry** | No commitment | No commitment | No |

The report row is the load-bearing one. A report is **filed whether or not the
estate agrees with it.** Disagreement is recorded as a disposition
(`re-characterised`, or `open` with the estate's reasoning), never as a reason not
to file. This follows [Charter §0.8](mx-000-charter.md): the alternative is an
estate that only records the faults it concedes.

### 4.3 What the estate will not do

- **Will not** treat silence as resolution. An unanswered report remains open in
  the record.
- **Will not** require identification to accept a report. Anonymous reports are
  filed on the same terms; an anonymous reporter simply cannot be told the outcome
  directly and must read the register.
- **Will not** ask a reporter to keep a report confidential.
- **Will not** retain correspondence beyond what the record requires
  ([REG-06](../registries/reg-06-dataset-registry.md)).

### 4.4 Correspondence is not retained as a dataset

The estate keeps **the record of what was decided**, in public registers. It does
not maintain a correspondence archive, a sender list, or a history per sender.
A sender who needs a durable copy of their own communication should keep it; the
estate's durable artefact is the register entry, not the message.

## 5. Worked instance

**A licensee receives a cure notice — and the clock problem appears.**

Suppose the estate believes a licensee has breached one of the nineteen curable
covenants under [§F.4](../license/the-maher-license.md). The cure period is 30 or
90 days and **runs from notice**. Trace it:

| Step | State |
|---|---|
| Estate identifies the breach | Possible |
| Estate must give notice | Requires an address for the licensee |
| Does the estate hold licensee addresses? | **No** — no registration, no accounts, no dataset ([REG-06](../registries/reg-06-dataset-registry.md)) |
| Can notice be given? | **Only if the licensee has contacted the estate first** |
| If not, does the clock start? | **No** |
| So can the covenant be enforced? | **In practice, no** |

This is a genuine structural hole and it is not small: **nineteen of twenty-three
Part H obligations are curable covenants whose remedy depends on a notice the
estate usually cannot serve.** The four automatic conditions are unaffected —
they terminate without notice — which means the estate's *enforceable* licence is
effectively the four conditions and the eight absolutes, not the twenty-three
provisions the text describes.

**What the estate does about it.** It publishes the hole rather than the
impression of enforcement. Two candidate remedies exist and both have costs:

- **Publish notice in the public record**, treating publication as constructive
  notice. Cheap, and of doubtful effect against a licensee who never reads it —
  and its validity is a legal question the estate cannot answer without counsel
  ([MX-005 Annex A row 6](mx-005-scope-and-boundaries.md)).
- **Require registration for licensees at scale**, using the
  [scale gate](../license/scale-gate.md) tiers. This would create exactly the
  dataset the estate refuses, for exactly the population where enforcement
  matters most.

The estate has adopted **neither** and records the non-decision as an open
question rather than presenting the second as obviously correct. A reader should
note that the refusal in [MX-003](mx-003-privacy-notice.md) and the enforceability
of [ML-2.3](../license/the-maher-license.md) are in genuine tension here, and the
estate has resolved it in favour of the refusal by default rather than by
decision.

## 6. Failure modes

| # | Failure | Mechanism | Current state |
|---|---|---|---|
| F1 | **Notice unservable** | No licensee addresses | **Actual** — §5 |
| F2 | **Single point of failure** | One recipient, no cover | **Actual** — §7 |
| F3 | **Unfiled report** | Estate disagrees and does not file | Prohibited by §4.2; **unverifiable from outside** |
| F4 | **Acknowledgement drift** | 7/14-day commitments quietly missed | No published response-time record exists |
| F5 | **Class inflation by sender** | Every message styled as "notice" | Tolerable; classification is the estate's under §4.1 |
| F6 | **Class deflation by estate** | A notice treated as an enquiry to avoid a clock | **The serious risk.** Same person classifies and is bound |
| F7 | **Anonymous report untraceable to outcome** | Reporter cannot be told | Accepted; mitigated by publication |

F6 is the one a reader should weigh. The estate classifies incoming mail, and
classification determines whether a clock runs against the estate. There is no
independent classifier and no audit. The only control is that **reports are
published**, so a deflected report leaves a gap between a sender's copy and the
register — checkable by the sender, by nobody else.

## 7. The availability problem

> **Stated without mitigation.**

There is one recipient. If that person is ill, travelling, or unreachable:

- acknowledgements in §4.2 are missed;
- reports are not filed on time;
- appeals do not progress;
- notices are not classified, so clocks that should run do not.

There is **no deputy, no shared mailbox, no escalation path, and no automated
acknowledgement.** [MX-015](mx-015-succession-and-continuity.md) specifies
succession triggers for permanent absence and says nothing useful about a fortnight
of unavailability, which is the far likelier event.

This is the practical face of [DEF-031](../00-governance-map/defect-register.md).
The remedy is not a document. The 3-month review interval (`perishable`) is set on
this instrument specifically because the estate expects these commitments to be
breached and wants the breach reviewed often rather than annually.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** a report is shown to have been received and **not** filed in the
>   [defect register](../00-governance-map/defect-register.md) — the single
>   most important test on this page;
> - **(b)** a communication expressly styled as notice, citing a provision, was
>   classified as an enquiry;
> - **(c)** any correspondence is shown to be retained as a dataset contrary to
>   §4.4;
> - **(d)** an acknowledgement commitment in §4.2 was missed without the miss being
>   recorded;
> - **(e)** a licensee is shown to have been served notice by a means not described
>   in §3 — which would mean the estate holds contact data it has not disclosed.
>
> **(a) and (b) can only be run by a sender**, who holds the other half of the
> evidence. The estate cannot falsify itself on either and depends on
> correspondents to do it. That dependency is stated rather than hidden behind an
> internal-audit claim the estate cannot make.

## 9. Limits

1. **One recipient, no cover** (§7).
2. **Notice is unservable to licensees the estate has never heard from** (§5),
   which defeats nineteen of twenty-three Part H covenants in practice.
3. **No response-time record is published**, so §4.2's commitments are unmeasured.
   Publishing a simple log of acknowledged-within dates would make F4 checkable and
   is not done.
4. **The estate classifies mail that binds the estate** (F6), with no independent
   check.
5. **No Arabic channel.** Correspondence in Arabic would be received and answered
   in a language the estate publishes nothing in
   ([MX-020](mx-020-language-authority.md)) — despite Arabic being the prevailing
   text of every instrument. A correspondent writing in the estate's own
   authoritative language is worse served than one writing in the subordinate one.
6. **No counsel**, so the constructive-notice option in §5 cannot be evaluated.

## 10. Obligation

**On the estate:**
- File every report, regardless of agreement (§4.2).
- Classify honestly; do not deflect a notice into an enquiry (§4.1, F6).
- Never require identification to accept a report (§4.3).
- Do not retain correspondence as a dataset (§4.4,
  [REG-06](../registries/reg-06-dataset-registry.md)).
- Publish a response-time record so §4.2 becomes measurable (§9.3, owed).
- Resolve the §5 notice hole by decision rather than by default, and record the
  decision.
- Review at 3 months, not 12 (§7).

**On a sender:**
- Say which class your message is, and cite the provision if it is notice (§2.1).
- Prefer the **public record** for anything you may need to establish later (§3.2).
- Keep your own copy; the estate keeps the register entry, not your message (§4.4).
- Run falsifier §8(a) or §8(b) if the estate's conduct diverges from this page —
  you hold evidence the estate does not.

---

### Related

**Instruments that depend on this channel** — [MX-002](mx-002-terms-of-service.md) ·
[MX-003](mx-003-privacy-notice.md) · [MX-008](mx-008-moderation-and-enforcement.md) ·
[MX-016](mx-016-appeals-and-due-process.md)

**The notice problem** — [ML-2.3](../license/the-maher-license.md) ·
[enforceability two-track table](../license/enforceability-two-track-table.md) ·
[scale gate](../license/scale-gate.md) ·
[MX-005 Annex A](mx-005-scope-and-boundaries.md)

**Records a sender can rely on** — [defect register](../00-governance-map/defect-register.md) ·
[corrections log](../00-governance-map/corrections-log.md) ·
[changelog](../00-governance-map/changelog.md) ·
[REG-07](../registries/reg-07-defect-classification-registry.md)

**Why there is one recipient** — [REG-08](../registries/reg-08-role-and-authority-registry.md) ·
[DEF-031](../00-governance-map/defect-register.md) ·
[MX-015](mx-015-succession-and-continuity.md) ·
[launch blockers](../00-governance-map/launch-blockers.md)

### Exit pair

1. **Use the self-proving channel.** File your report in the public record; §3.2
   explains why it is stronger than writing to one person.
2. **Read the hole this page cannot close.** [§5](#5-worked-instance) — nineteen
   curable covenants with no servable notice.

<!-- mx-pagestamp: MX-006 · v2026.10.1 · governing · tier 3 · reviewed 2026-09-16 · next review 2026-12-16 -->
<!-- mx-demo: the live site is a demonstration; the published contact address is the only active channel -->
