---
doc_id: MX-017
title_en: Conflicts of Interest
title_ar: تعارض المصالح
family: corpus
version: v2026.10.1
status: published
authority: governing
prevailing_text: ar
audience_tier: 2
depth: macro
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: yes
last_reviewed: 2026-09-16
domain_tags: [conflicts, interest, independence, disclosure, self-review]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000 at the instruction of the person whose conflicts it governs.
provenance_of_purpose: Required by MX-008, MX-016 and RB-05, each of which presumes an unconflicted decider; absent until v2026.10.1.
route: /conflicts-of-interest/
---

# MX-017 — Conflicts of Interest

> **Authority.** `governing`, tier 3. Presumed by
> [MX-008](mx-008-moderation-and-enforcement.md),
> [MX-016](mx-016-appeals-and-due-process.md) and
> [RB-05](../rubrics/rb-05-harm-review-gate.md), each of which requires a decider
> who is not an interested party.

> **Disclosure first.** In this estate the conflict is **total and structural, not
> occasional**. One person is author, publisher, assessor, appeal decider, defect
> classifier, severity rater, and the only party with an interest in the outcome of
> each of those acts
> ([REG-08](../registries/reg-08-role-and-authority-registry.md)). This instrument
> cannot resolve that. What it can do is refuse to let it be described as anything
> smaller, and specify what is owed when a conflict cannot be removed. That is
> §5, and it is the only operative part.

---

## 1. Position

A conflicts policy in a normal institution allocates decisions away from
interested parties. This estate has nowhere to allocate them to.

That produces a choice between two dishonest options and one uncomfortable one:

- **Option A** — write a standard policy with recusal provisions. Reads well;
  every provision is inoperable; the estate would be publishing procedure it
  cannot run, which is exactly the fault pattern of
  [DEF-031](../00-governance-map/defect-register.md).
- **Option B** — declare conflicts irrelevant because the estate is small and
  the curator well-intentioned. This is the argument
  [REG-08 §2.2](../registries/reg-08-role-and-authority-registry.md) rejects:
  independence is a property of the arrangement, not of character.
- **Option C** — state that the conflict is unresolved, specify what the estate
  owes a reader **in place of** independence, and make each substitute checkable.

This instrument takes C. A reader should understand that C is **worse than
independence** and is being offered because independence is unavailable, not
because disclosure is equivalent to it.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **interest** | Anything the decider gains or loses by the decision going one way |
| **conflict** | A decision where the decider holds an interest |
| **structural conflict** | A conflict arising from the arrangement of roles, present in every instance of a decision class |
| **occasional conflict** | A conflict arising from the facts of one matter |
| **recusal** | Transferring the decision to an unconflicted decider |
| **substitute** | What is owed when recusal is impossible (§5) |

### 2.1 Interests need not be financial

The estate holds **no** financial interest: no revenue, no advertising
([MX-009](mx-009-advertising-and-commercial.md)), no affiliate income
([ST-23](../standards/st-23-affiliate-and-referral.md)), no payments
([MX-021](mx-021-payments-and-commerce.md)). A policy limited to financial
interests would find nothing to report, and would be useless.

The interests that actually operate here are **reputational and dispositional**:

| Interest | Pulls toward |
|---|---|
| Wanting the corpus to appear complete | Understating gaps; calling a partial series complete |
| Wanting one's own work to pass review | Passing it ([RB-05](../rubrics/rb-05-harm-review-gate.md)) |
| Wanting a defect to be cheap | Rating severity by fix cost, not reader effect ([REG-07 §2.2](../registries/reg-07-defect-classification-registry.md)) |
| Wanting a clock not to run | Classifying a notice as an enquiry ([MX-006 F6](mx-006-contact-and-correspondence.md)) |
| Wanting to avoid rewriting four instruments | Leaving DEF-031 open rather than narrowing the specifications |
| Wanting a decision upheld | Deciding one's own appeal ([MX-016](mx-016-appeals-and-due-process.md)) |

Six interests, all live, none financial. This table is the substance of the
instrument; everything else is machinery around it.

## 3. The structural conflicts, enumerated

| # | Decision class | Decider | Interest | Recusal possible? |
|---|---|---|---|---|
| C1 | Whether published work meets the estate's standards | Curator = author | Reputational | **No** — no reviewer |
| C2 | Harm review gate outcome | Curator = author | Reputational | **No** — Harm Reviewer vacant |
| C3 | Defect class and severity | Curator = cause of the defect | Dispositional | **No** — one classifier |
| C4 | Appeal outcome, stage 2 | Curator = original decider | Direct | **No** — vacant; consequence is no credentials ([REG-05](../registries/reg-05-credential-registry.md)) |
| C5 | Whether an objection is `open` or answered | Curator = objected-to party | Reputational | **No** — [ST-06](../standards/st-06-objections-standard.md) |
| C6 | Ratifying text the curator authored | Curator = author | Direct | **No** — Ratifying Authority vacant |
| C7 | Classifying incoming correspondence | Curator = bound party | Direct | **No** |
| C8 | Whether the estate's own scope covers a subject | Curator = would do the work | Dispositional | **No** — [MX-005 §7.3](mx-005-scope-and-boundaries.md) |
| C9 | Archive attestation | Curator = keeper | Reputational | **No** — Records Keeper vacant |

**Nine decision classes, nine unrecusable conflicts.** The count is the honest
headline and is stated before any mitigation is described.

## 4. Mechanism

### 4.1 Where recusal is possible, it is mandatory

None of C1–C9 currently permits it. If a second participant joins, the
**recusal-first rule** applies immediately and without amendment: any decision in
C1–C9 transfers to the unconflicted party, and the transfer is logged.

This is drafted now, while it cannot operate, specifically so that acquiring a
second person does not require a governance change to take effect. Writing it
later would allow the conflict to persist through a drafting delay.

### 4.2 Where recusal is impossible

The substitutes in §5 apply. They are **cumulative**, not alternatives: all four
are owed on every conflicted decision.

### 4.3 What is never permitted

- Deciding a conflicted matter **without disclosing** the conflict.
- Describing a self-review as independent.
- Using the absence of an alternative decider as a reason not to record the
  conflict.
- Treating a disclosure as curing the conflict. It does not; it makes the conflict
  legible.

## 5. The four substitutes

Owed on every decision in C1–C9.

### S1 — Disclose the conflict at the point of decision

Not in a policy, not in a register: **on the page where the decision appears.**
Every instrument in this corpus carries an `authorship_note` disclosing AI
drafting, and instruments recording estate self-assessment state that they are
self-assessed. That is S1 operating.

**Check:** find a published estate self-assessment that does not say it is one.

### S2 — State the direction of the interest

Disclosure without direction is nearly useless. "There is a conflict" tells a
reader to be careful; "the interest pulls toward understating the gap" tells them
**which way to discount**.

§2.1's table is the estate's compliance with S2, and it is the least common of the
four substitutes in practice.

**Check:** find a conflicted decision where the direction of pull is not stated
anywhere.

### S3 — Publish the adverse alternative

Where a conflicted decision could reasonably have gone the other way, publish the
other way's reasoning. Examples actually in the corpus:

- [MX-005 §5](mx-005-scope-and-boundaries.md) publishes the argument that the
  estate's own enforceability table should be withdrawn on the same grounds it
  refuses a licence comparison.
- [REG-06 §5.1](../registries/reg-06-dataset-registry.md) publishes that a reader
  may reasonably think the estate's refusal to test its own licence premise is
  wrong.
- [MX-011 §9.3](mx-011-security-and-disclosure.md) publishes that both available
  options on the access-practice question are unsatisfactory.

**Check:** find a conflicted decision with no adverse alternative published.

### S4 — Make the decision falsifiable by an outsider

The decision must come with a test a reader can run without the estate's
cooperation. This is [ST-04](../standards/st-04-falsifiability-and-claim-cards.md)
applied to conflicts: a conflicted decision that only the decider can check is
indistinguishable from a decision made for the interest.

**Check:** find a conflicted decision whose only verification route runs through
the estate.

### 5.1 The honest assessment of the substitutes

| Substitute | Applied? | Quality |
|---|---|---|
| S1 disclose | **Widely** | Good — front matter carries it corpus-wide |
| S2 direction | **Partially** | Weak — usually the conflict is named without a direction |
| S3 adverse alternative | **Sometimes** | Uneven — strong in a few places, absent in most |
| S4 outsider falsifier | **Widely** | Good in form; several falsifiers are **unrunnable** ([MX-011 §8a](mx-011-security-and-disclosure.md)) |

Two of four substitutes are applied well, one poorly, one in form but not always
in substance. **Four substitutes applied at roughly half strength do not equal one
independent reviewer**, and no arithmetic here should suggest otherwise.

## 6. Worked instance

**C3 traced: the estate classifies a defect it caused.**

[DEF-031](../00-governance-map/defect-register.md) records that four instruments
specify processes the estate cannot run. Who classified it? The curator. Whose
conduct caused it? The curator's. Which severity did it receive? S2 for three
instances, S1 for one.

Now apply the substitutes and see where they hold:

| Substitute | Applied here? |
|---|---|
| **S1** disclose | **Yes** — the defect register states one participant and one classifier |
| **S2** direction | **Yes** — the interest pulls toward *lower* severity, because higher severity means rewriting four instruments |
| **S3** adverse alternative | **Yes, in part** — [REG-07 §4](../registries/reg-07-defect-classification-registry.md) publishes that DEF-031 has **two** legitimate remedies pointing opposite ways, one of which (narrowing four specifications) is the one the curator would least like |
| **S4** outsider falsifier | **Yes** — a reader can read MX-016, MX-015, MX-014 and ST-06 and judge for themselves whether those processes can run with one person. **This requires no access and no cooperation** |

So on this decision all four substitutes engage, and S4 engages strongly: the
underlying facts are entirely public, so a reader can second-guess the severity
without the estate's help.

**But note what the substitutes did not prevent.** The interest identified in S2
— avoiding the rewrite — points at exactly the outcome that obtained: DEF-031 is
`open` with the remedy recorded as *acquire a second participant*, which is the
remedy that requires nothing of the curator's existing text. The alternative
remedy, narrowing four instruments to promise only what one person can deliver, is
recorded as legitimate and **has not been done**.

Disclosure worked. It did not change the decision. That is the accurate account of
what §5 buys, and this instrument would be misleading if it ended on a stronger
note.

## 7. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Disclosure treated as cure** | Prohibited by §4.3; **the temptation is constant** |
| F2 | **Direction omitted** | **Occurring** — S2 is the weakest substitute (§5.1) |
| F3 | **Adverse alternative omitted where inconvenient** | **Likely**; unverifiable from outside by construction |
| F4 | **Falsifier present but unrunnable** | **Occurring** — e.g. [MX-011](mx-011-security-and-disclosure.md) integrity test |
| F5 | **Conflict normalised** | **Occurring** — nine unrecusable classes, dating from inception |
| F6 | **Recusal rule dormant then forgotten** | §4.1 drafted to be self-executing; **no watcher** |
| F7 | **Policy read as resolving the conflict** | Guarded by §1's Option-C framing |

## 8. Limits

1. **No conflict in C1–C9 can be recused.** Everything here is mitigation.
2. **The substitutes are self-administered.** The party owing S1–S4 is the
   conflicted party, so compliance with the conflicts policy is itself a
   conflicted decision. This regress has no bottom and is not closed by adding
   documents.
3. **S2 and S3 are applied unevenly** and the unevenness is invisible from outside
   (F3).
4. **This instrument was written by the conflicted party's own agent**, at the
   conflicted party's instruction, and the agent is barred from every role that
   could review it ([REG-08 §3.3](../registries/reg-08-role-and-authority-registry.md)).
5. **No Arabic text**, while `prevailing_text: ar`.

## 9. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** a decision in classes C1–C9 is published without S1 disclosure;
> - **(b)** a self-review is described anywhere in the corpus as independent;
> - **(c)** a conflicted decision is published with **no** direction of interest
>   stated, which §5's S2 requires — the estate expects this to fire, and §5.1
>   concedes it;
> - **(d)** a second participant joins and a C1–C9 decision is still taken by the
>   conflicted party;
> - **(e)** a conflict is shown to exist that is absent from §3's enumeration of
>   nine.
>
> **(c) is expected to fire** and is published in that expectation. **(e) is the
> more valuable test**: nine classes were enumerated by the conflicted party, who
> has an interest in the list being short.

## 10. Obligation

**On the estate:**
- Disclose at the point of decision, never only in a policy (S1, §4.3).
- State the **direction** of every interest (S2) — the weakest current practice
  and the one most owed.
- Publish the adverse alternative wherever a conflicted decision could have gone
  the other way (S3).
- Provide an outsider-runnable falsifier, and repair the ones that are currently
  unrunnable (S4, F4).
- Never describe a self-review as independent (§4.3).
- On acquiring a second participant, transfer C1–C9 decisions **immediately**;
  §4.1 requires no amendment.
- Record any addition to §3's nine classes as a correction, not a quiet edit.

**On a reader:**
- Discount the estate's self-assessments **in the direction §2.1 states**.
- Run falsifier §9(e): find a tenth conflict class. The list was written by the
  interested party.

---

### Related

**Instruments presuming independence** — [MX-008](mx-008-moderation-and-enforcement.md) ·
[MX-016](mx-016-appeals-and-due-process.md) ·
[RB-05](../rubrics/rb-05-harm-review-gate.md) ·
[ST-06](../standards/st-06-objections-standard.md)

**The structural cause** — [REG-08](../registries/reg-08-role-and-authority-registry.md) ·
[DEF-031](../00-governance-map/defect-register.md) ·
[MX-015](mx-015-succession-and-continuity.md) ·
[MX-005 Annex A](mx-005-scope-and-boundaries.md)

**Disclosure machinery** — [ST-02](../standards/st-02-front-matter-schema.md) ·
[ST-04](../standards/st-04-falsifiability-and-claim-cards.md) ·
[ST-07](../standards/st-07-evidence-and-verify.md) ·
[MX-007](mx-007-ai-use-and-disclosure.md)

**Adverse alternatives already published** — [MX-005 §5](mx-005-scope-and-boundaries.md) ·
[REG-06 §5.1](../registries/reg-06-dataset-registry.md) ·
[MX-011 §9](mx-011-security-and-disclosure.md) ·
[REG-07 §5.2](../registries/reg-07-defect-classification-registry.md)

### Exit pair

1. **Find the tenth conflict.** §3 lists nine, enumerated by the interested party.
   Falsifier §9(e) is the most useful thing a reader can do with this page.
2. **See a substitute fail.** [§6](#6-worked-instance) — all four substitutes
   engaged on DEF-031 and the decision still went the way the interest pointed.

<!-- mx-pagestamp: MX-017 · v2026.10.1 · governing · tier 3 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the live site is a demonstration; every decision class listed here is currently unrecusable -->
