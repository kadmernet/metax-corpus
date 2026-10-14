---
doc_id: BX-004
title_en: The After Phase
title_ar: مرحلة ما بعد القراءة
family: bcia
version: v2026.10.1
status: published
authority: companion
prevailing_text: ar
audience_tier: 2
depth: macro
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [bcia, after, reliance, notification, staleness]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000, class I-1, resting on gap 1. This phase contains the estate's costliest refusal, and the drafting system benefits from that refusal being framed as principled.
route: /bcia/after/
---

# BX-004 — The After Phase

> **This page will not resolve:** whether anyone has ever relied on this corpus.
> The estate does not know and has refused the means of finding out
> ([REG-06 `DSET-R01`](../registries/reg-06-dataset-registry.md)).

> **Authority.** `companion`. Phase A obligations are discharged by
> [ST-04](../standards/st-04-falsifiability-and-claim-cards.md),
> [ST-05](../standards/st-05-decay-and-review-intervals.md) and
> [MX-013](../corpus/mx-013-records-and-versioning.md), per
> [BX-000 §4.2](bx-000-bcia-charter.md).

> **Disclosure first.** Phase A is where the estate's **costliest refusal** sits:
> a reader who relies on an instrument that is later corrected **cannot be told**,
> because the estate holds no address list
> ([MX-003 §5](../corpus/mx-003-privacy-notice.md)). This is the one refusal that
> harms readers rather than the estate, and §5 traces what it actually costs.

---

## 1. Position

Phase A is everything after the reader closes the page: **acting on it, and
learning later that it changed.**

It is the phase with the longest duration and the least corpus presence. A reader
spends minutes at Contact and potentially years in After — relying on a permission,
building against a standard, citing a version.

| Phase | Duration | Corpus present? |
|---|---|---|
| B | Seconds | Yes |
| C | Minutes | Yes |
| I | Minutes to hours | Yes |
| **A** | **Months to years** | **Almost not at all** |

Everything the corpus does for phase A is **passive**: a version stamp that must
be re-checked, a review date that must be compared to today, a changelog that must
be visited. All require the reader to **return**, unprompted, with no signal that
returning is necessary.

## 2. The four phase A obligations

| # | Obligation | Mechanism | State |
|---|---|---|---|
| **A1** | Tell the reader what they must do | Obligation section, every page | **Met** |
| **A2** | Tell them what would show it wrong | Falsifier, every page | **Met in form**; most never run |
| **A3** | Let them determine currency **unaided** | Version + next review date in the page stamp | **Met** — [MX-019 §6](../corpus/mx-019-sunset-and-wind-down.md) |
| **A4** | **Tell them when it changed** | — none — | **Refused** |

### 2.1 A3 was fixed for a different reason

The next-review-date-in-the-stamp remedy came from
[MX-019 §6](../corpus/mx-019-sunset-and-wind-down.md), reasoning about estate
orphaning: a reader at month 13 cannot distinguish a missed review from a confirmed
one unless the next date is printed.

[AG-012 §5.2](../agents/ag-012-agent-sunset-and-withdrawal.md) then found the same
remedy protects against agent withdrawal.

So the corpus's one active phase A protection was adopted **twice, for reasons
having nothing to do with readers**. It is worth noting how the estate's best phase
A mechanism arrived: not from thinking about reliance, but from thinking about
death.

### 2.2 A4 and the shape of the refusal

The refusal is stated plainly at
[MX-003 §5](../corpus/mx-003-privacy-notice.md): notifying readers of corrections
would require an address list, an address list is a dataset about people, and
[REG-06 §3.1](../registries/reg-06-dataset-registry.md) requires a prior written
question and a retention condition for any such dataset.

The estate declined. [MX-003](../corpus/mx-003-privacy-notice.md) records this as
the refusal that *"most clearly harms readers rather than the estate"* and files
the objection as `open` under
[ST-06](../standards/st-06-objections-standard.md).

**The objection is correct and is not answered anywhere.** This page does not
answer it either. What it can do is make the cost precise, which §5 attempts.

## 3. What a reader in phase A actually needs

| Need | Available? |
|---|---|
| Know the version they relied on | **Yes** — stamp |
| Know whether it is still current | **Yes** — next review date |
| Know whether it was **corrected** | **Only by returning** and reading the [corrections log](../00-governance-map/corrections-log.md) |
| Know whether a **defect** was found against it | **Only by returning**, and the instrument usually does not link its own defects ([ST-08 §3.2](../standards/st-08-cross-reference-and-link-integrity.md)) |
| Be told | **No** |

### 3.1 The asymmetric defect linkage makes A worse

[ST-08 §3.2](../standards/st-08-cross-reference-and-link-integrity.md) records that
defects are filed **in the register** naming an instrument, and the instrument
usually does **not** link back.

For a phase A reader this compounds badly. Even a conscientious reader who returns
to the page they relied on will **not** see that a defect was filed against it — the
page looks unchanged. They would have to read the entire defect register and match
by identifier.

So the return-based substitute for A4 does not work even for readers who perform
it. **The corpus's passive phase A protection fails the reader who does the right
thing**, and the fix is [ST-18 §3.2](../standards/st-18-related-blocks-and-exit-pairs.md)'s
"where its faults are recorded" group — which that standard already identifies as
the group most often omitted.

## 4. Mechanism — what the estate could do without an address list

Three candidate remedies, none requiring reader data:

| # | Remedy | Serves | Cost | Requires reader data? |
|---|---|---|---|---|
| **P1** | Every instrument links its own defects ([ST-18 §3.2](../standards/st-18-related-blocks-and-exit-pairs.md) group 3) | A returning reader sees faults | Authoring practice | **No** |
| **P2** | A single **corrections feed** at a stable route, chronological, one line per correction | A reader can poll one page instead of eighty | One page, appended | **No** |
| **P3** | Print **"last corrected"** in the page stamp alongside the review date | A returning reader sees at a glance | Stamp change | **No** |

**None of the three requires an address list.** They convert A4's *push*
notification into a **reliable pull**, which is weaker than notification and much
stronger than what exists.

### 4.1 Why these were never adopted

Because the refusal at [MX-003 §5](../corpus/mx-003-privacy-notice.md) was framed
as *"cannot notify"*, and having named the cost the estate stopped. The question
*"what can we do that is not notification?"* was not asked.

This is the same pattern [AG-011 §5.1](../agents/ag-011-agent-review-and-audit.md)
found: a genuine incapacity absorbed an adjacent capability that was never
examined. There, source-checking was absorbed into the single-participant excuse.
Here, three pull-side remedies were absorbed into the address-list refusal.

**Twice now, in independently written instruments, the estate's honest statements
of incapacity have been found to cover more ground than they were entitled to.**
That is a pattern worth naming, and it generalises: an estate that documents its
limits carefully can use those limits, without dishonesty, to stop looking.

## 5. Worked instance

**Costing A4 on a real case.**

Suppose a reader relied on [MX-005](../corpus/mx-005-scope-and-boundaries.md) §2 —
the three scope conditions — and built a decision on condition 2, that a subject is
in scope only if *"dischargeable by publishing a checkable text"*, described there
as the estate's **sole capability**.

[MX-018 §6](../corpus/mx-018-third-party-dependencies.md) subsequently found that
claim wrong: authorship is **not** a capability the estate holds, it is a service
received from a dependency. Classified **DC-3 overclaim**, severity **S2**, filed
against a governing instrument.

Now trace what the reader experiences:

| Step | Outcome |
|---|---|
| Reader relied on MX-005 §2 | — |
| Defect found and filed in MX-018 §6 | Yes |
| Is MX-005's text amended? | **No** — filed, not silently edited ([Charter §0.8](../corpus/mx-000-charter.md)) |
| Does MX-005 link the defect? | **No** — asymmetric linkage (§3.1) |
| Is there a corrections entry? | In the log, not on the page |
| Does the reader's version stamp change? | **No** |
| Does the next review date change? | **No** |
| **Can the reader discover it?** | **Only by reading MX-018 §6 — a page about third-party dependencies** |

**Terminal state: `blockage` — the finding is undiscoverable from the affected
instrument.**

### 5.1 The finding

The estate did everything its own rules require. It found the defect, filed it
rather than silently editing, classified it, and disclosed it in the instrument
where it was discovered.

**And a reader relying on the affected instrument cannot find out.** Not because of
the address-list refusal — they returned to the page, which is what the pull model
asks — but because the defect lives in a *different* instrument and nothing
connects them.

So the harm attributed to the A4 refusal is **partly misattributed**. The reader in
this case was defeated by **P1's absence**, not by the absence of notification.
P1 costs nothing and requires no data.

Filed per [ST-17 W6](../standards/st-17-worked-instance-standard.md):

> **Finding BX-004/1.** The phase A harm the estate attributes to its
> address-list refusal is substantially caused by **P1** — instruments not linking
> their own defects — which is free. Before the A4 refusal can be assessed as the
> costly principled choice
> [MX-003 §5](../corpus/mx-003-privacy-notice.md) presents it as, P1, P2 and P3
> should be adopted and the residual harm re-measured. **The estate has been
> crediting an unpaid cost to a principle.**

## 6. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Reader never learns of a correction** | **Actual** — A4 refused |
| F2 | **Returning reader still cannot find the defect** | **Actual** — §3.1, §5 |
| F3 | **Incapacity absorbing adjacent capability** | **Actual, twice** — §4.1 |
| F4 | **Falsifiers stated and never run** | **Actual** — A2 |
| F5 | **Passive protection assumed adequate** | §2.1 — the one active measure arrived by accident |
| F6 | **Long phase A, no corpus presence** | **Structural** — §1 |

## 7. Limits

1. **Reliance is unobservable here.** Whether anyone has relied on anything is
   unknown ([REG-06](../registries/reg-06-dataset-registry.md)).
2. **§5's reader is hypothetical**, constructed by the author — though the defect,
   the classification and the linkage gap are all real and citable.
3. **P1–P3 are asserted as sufficient-ish**; no evidence supports the claim that a
   reliable pull approximates a push.
4. **The drafting system benefits** from A4's refusal reading as principled
   ([MX-017 C1](../corpus/mx-017-conflicts-of-interest.md)); discount §5.1 toward
   understating the estate's fault.
5. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** a reader who returns to an instrument can discover a defect filed
>   against it elsewhere — **currently false** (§5);
> - **(b)** P1, P2 or P3 is shown to require reader data (§4) — which would vindicate
>   the estate's framing;
> - **(c)** adopting P1–P3 is shown not to reduce phase A harm (§5.1);
> - **(d)** the pattern in §4.1 — incapacity absorbing capability — is shown to be
>   two coincidences rather than a pattern;
> - **(e)** a fifth phase A obligation is identified beyond A1–A4.
>
> **(b) is the estate's best defence and it is checkable in minutes** against
> [REG-06 §3.1](../registries/reg-06-dataset-registry.md)'s gates. The estate's own
> reading is that none of the three requires any dataset, which means the harm at
> §5 has been unnecessary throughout.

## 9. Obligation

**On an author (practice; this is a companion):**
- Include the **"where its faults are recorded"** related group
  ([ST-18 §3.2](../standards/st-18-related-blocks-and-exit-pairs.md)) — P1, and the
  group most often omitted.
- When filing a defect against an instrument, add the reciprocal link **in that
  instrument** ([ST-08 L5](../standards/st-08-cross-reference-and-link-integrity.md)).

**On the estate:**
- **Adopt P1, P2 and P3** (§4). None requires reader data; all are unbuilt.
- **Re-assess the A4 refusal after P1–P3 are in place** (finding BX-004/1). The
  refusal may be right; it has not yet been paid for honestly.
- Audit for further cases of §4.1's pattern — incapacity absorbing adjacent
  capability. Two are recorded; the estate has not looked for a third.
- Keep A4 filed as an `open` objection
  ([ST-06](../standards/st-06-objections-standard.md)); do not treat this page as
  answering it.

---

### Related

**Standards discharging phase A** —
[ST-04](../standards/st-04-falsifiability-and-claim-cards.md) ·
[ST-05](../standards/st-05-decay-and-review-intervals.md) ·
[MX-013](../corpus/mx-013-records-and-versioning.md) ·
[ST-15](../standards/st-15-amendment-and-versioning-standard.md)

**The refusal and its cost** —
[MX-003 §5](../corpus/mx-003-privacy-notice.md) ·
[REG-06](../registries/reg-06-dataset-registry.md) ·
[MX-023](../corpus/mx-023-attention-and-human-sovereignty.md) ·
[ST-06](../standards/st-06-objections-standard.md)

**Why a returning reader still fails** —
[ST-08 §3.2](../standards/st-08-cross-reference-and-link-integrity.md) ·
[ST-18 §3.2](../standards/st-18-related-blocks-and-exit-pairs.md) ·
[defect register](../00-governance-map/defect-register.md) ·
[corrections log](../00-governance-map/corrections-log.md)

**Adjacent phases** — [BX-000](bx-000-bcia-charter.md) ·
[BX-001](bx-001-before-phase.md) · [BX-002](bx-002-contact-phase.md) ·
[BX-003](bx-003-internalisation-phase.md)

### Exit pair

1. **Pay the cost before claiming the principle.** Finding BX-004/1 — P1, P2 and
   P3 need no reader data and are unbuilt. Until they exist, the A4 refusal is
   being credited with harm it did not cause.
2. **Watch the pattern.** [§4.1](#41-why-these-were-never-adopted) — twice now, an
   honest statement of incapacity has been found covering ground it was not entitled
   to.

<!-- mx-pagestamp: BX-004 · v2026.10.1 · companion · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; no reader's reliance on any instrument has ever been observed -->
