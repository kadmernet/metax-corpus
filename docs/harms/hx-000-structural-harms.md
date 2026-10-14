---
doc_id: HX-000
title_en: The Twenty-Five Structural Harms
title_ar: الأضرار البنيوية الخمسة والعشرون
family: harms
version: v2026.10.1
status: published
authority: governing
prevailing_text: ar
audience_tier: 3
depth: macro
evidence_class: semi-durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: yes
incorporated_by: ML-2.3 §A.10 (Part H)
supersedes: HX-000 v2026.09.4 (fourteen harms)
superseded_governing_text: ../harms/hx-000-the-fourteen-structural-harms.md
last_reviewed: 2026-09-16
domain_tags: [harms, structural, license, part-h, maqasid, foundational]
ai_disclosure_url: ../corpus/mx-007-ai-use-and-disclosure.md
authorship_note: Drafted by an AI system under AG-000, class I-1, resting on gaps 1 and 3 (cannot verify, no legal competence). H1–H11 are carried from the predecessor; H12–H25 are new and have not been reviewed by anyone.
hreflang: [en, ar]
route: /harms/
---

# HX-000 — The Twenty-Five Structural Harms

> **⚠ Superseded in part, 2026-09-30 (v2027.1 intake).** The harm **identities** below (H1–H25)
> do **not** match [ML-2.3 §H.2.2](../license/ml-2-3.md), the tier-1 text this register claims to
> supply. Only H1, H10, H11 and H15 correspond cleanly (DEF-040). **For harm identity, read ML-2.3
> §H.2.2. For content, read [HX-000 v2027.1](hx-000-register-v2027-1.md).** Map any "H*n*"
> citation through [CON-002](con-002-harm-numbering-concordance.md). This text is retained
> unedited below as the record of what was published.

> **This page will not resolve:** whether any particular deployment causes a harm.
> It supplies the register the licence points at; instantiation is assessed with
> [HX-001](hx-001-harm-audit-rubric.md).

> **Authority.** `governing`, **tier 1a**. Incorporated by
> [ML-2.3 §A.10](../license/the-maher-license.md), which places this register
> **above the Charter** and below only the licence itself
> ([GM-01](../00-governance-map/precedence-and-conflict-rules.md)). Where this
> document and the licence differ, **the licence governs and the difference is a
> defect to be filed**. Where this document and a summary of it differ, **this
> document governs** ([GM-01 §3](../00-governance-map/precedence-and-conflict-rules.md)).

> **Disclosure first.** This is the **re-version** discharging
> [DEF-021](../00-governance-map/defect-register.md) — the dangling reference on
> the face of the Tier 1 instrument. Its predecessor named **fourteen** harms while
> [ML-2.3](../license/the-maher-license.md) governs **twenty-five**, sat at
> `v2026.09.4` under **ML-2.2** (a licence version that is
> [permanently lost](../license/version-history.md)), and ended unfinished at an
> append-point. That text is **retained, superseded, not deleted**
> ([ST-15 A3](../standards/st-15-amendment-and-versioning-standard.md)).
>
> **H12–H25 are new in this version and have been reviewed by nobody**
> ([AG-011 §4.2](../agents/ag-011-agent-review-and-audit.md): review debt 100%).

---

## §0 — Method

### 0.1 What is selected

The twenty-five harms are **not** the twenty-five worst things done with
computers. Crime, weaponisation, exploitation, repression and fraud are worse in
every ordinary sense and are **already reached** by law and by
[ML-2.3 Part C](../license/the-maher-license.md). Restating them would inflate the
register and add nothing operative.

What is selected is the class of harm that is **structural, distributed, and
unactionable one instance at a time**. Five inclusion criteria, all required:

| # | Criterion | What it excludes |
|---|---|---|
| 1 | **Structural, not incidental** | Remove every bad actor and the harm remains |
| 2 | **Mechanism-identified** | A named causal chain, not an atmosphere |
| 3 | **Evidence-bearing** | Checkable evidence exists, including evidence **against** |
| 4 | **Falsifiable** | A stated condition under which the harm is withdrawn |
| 5 | **Actionable by a builder** | Implies at least one design decision a licensee can make |

Criterion 4 is the load-bearing one. **A harm that cannot be withdrawn is a
doctrine**, and this corpus does not publish doctrine.

### 0.2 Why the count changed

The predecessor's fourteen were drawn from computing and networking. ML-2.3 extends
the register into three areas fourteen did not reach:

| Added | Stratum | Why the earlier register missed it |
|---|---|---|
| Economic harms beyond lock-in | III | Fourteen treated economics as a consequence, not a harm class |
| **Reflexive harms** — effects on the estate publishing the register | V | The earlier register did not turn on itself |
| **Successor harms** — effects on those who come after | VI | Fourteen had no time horizon beyond the current user |

Stratum V is the significant addition. A harms register that cannot name the harms
of **publishing a harms register** is incomplete in a way that matters, and H15–H19
exist to close it.

### 0.3 What each entry carries

| Field | Content |
|---|---|
| **Mechanism** | The causal chain, stated so it could be wrong |
| **Instantiation test** | What would show this harm present in a given deployment |
| **Falsifier** | The condition under which the harm is withdrawn |
| **Obligation** | The Part H duty it generates |
| **In this estate** | Whether the estate itself instantiates it |

The last field is required by [Charter §0.8](../corpus/mx-000-charter.md) and is
the field most registers omit. Its current tally appears at
[§7](#7-the-estates-own-state).

### 0.4 The strata are not a severity ordering

Six strata group harms by **subject**, not by seriousness. Stratum VI
(successor) contains harms the estate cannot presently assess at all; stratum I
(cognitive) contains harms with the most evidence. Neither fact is about severity.

---

## §1 — Stratum I: Cognitive (H1–H3)

Harms to attention, comprehension, and judgement. **The only stratum that
instantiates while the reader is present** ([BX-007 §2.1](../bcia/bx-007-bcia-and-harms.md)).

### H1 — Attention capture

**Mechanism.** A system whose revenue or success metric is engagement will, under
optimisation pressure and without anyone intending it, discover and exploit the
gap between what a person endorses on reflection and what holds their attention in
the moment. The optimiser needs no theory of mind; it needs only a gradient.

**Instantiation test.** Does any metric the system optimises increase when a user
spends time they would not endorse on reflection?

**Falsifier.** Withdrawn as to any deployment that (i) optimises no
attention-derived metric, (ii) exposes a complete stopping affordance the user
controls, and (iii) does not vary content ordering by predicted engagement.

**Obligation.** [§H.5](../license/the-maher-license.md) — the reflective-endorsement
duty.

**In this estate:** `partial`. [MX-023](../corpus/mx-023-attention-and-human-sovereignty.md)
states six refusals; four are implemented, **two are violated**.

### H2 — Comprehension substitution

**Mechanism.** A system that supplies an answer faster than a person could reach
understanding substitutes for the understanding, and the substitution is invisible
because the output is correct. Correctness is not the variable at risk.

**Instantiation test.** Would a user who relies on the output be unable to
reconstruct why it is right?

**Falsifier.** Withdrawn where the system shows its derivation such that a user can
reconstruct the result unaided, **and** where no metric rewards the user for not
doing so.

**Obligation.** [§H.6](../license/the-maher-license.md); connects to absolute
**(vii)**, developmental substitution — the **disjunctive** absolute of
[§H.3(a)](../license/the-maher-license.md), which operates alone.

**In this estate:** `partial`. Every instrument carries a worked instance a reader
must re-derive; nothing measures whether they do
([RB-04](../rubrics/rb-04-reader-comprehension-rubric.md) is handed to the reader
and never returned).

### H3 — Judgement deskilling

**Mechanism.** Delegating a judgement repeatedly erodes the capacity to make it.
Unlike H2 the loss is gradual and is discovered only when the system is
unavailable.

**Instantiation test.** If the system were removed for a month, would users perform
worse than before they adopted it?

**Falsifier.** Withdrawn where periodic unassisted performance is measured and
shown stable.

**Obligation.** [§H.6](../license/the-maher-license.md).

**In this estate:** **`FAILS`** as recorded at
[HX-002](hx-002-harm-instrument-map.md) — the corpus is authored by a system, and
the curator's own unassisted authoring capacity is untested and, per
[MX-018 §6](../corpus/mx-018-third-party-dependencies.md), is the binding
constraint that created the dependency.

---

## §2 — Stratum II: Relational (H4–H6)

Harms to trust, dependency, and connection. **Instantiate at phase A**, in
reliance.

### H4 — Misplaced and uncorrectable trust

**Mechanism.** A system that presents with authority acquires trust proportional to
its presentation, not to its reliability. When it is later found wrong, the parties
who relied cannot be reached.

**Instantiation test.** If a claim were found false today, could every party who
relied on it be told?

**Falsifier.** Withdrawn where a correction reaches those who relied, or where
nothing invites reliance.

**Obligation.** [§H.9](../license/the-maher-license.md) — the correction-reach duty.

**In this estate:** **`FAILS`**. [MX-003 §5](../corpus/mx-003-privacy-notice.md) —
no address list, no notification, by deliberate refusal.
[BX-004 §5.1](../bcia/bx-004-after-phase.md) found the harm is **substantially
caused by the free and unadopted PF-11**, not by the refusal.

### H5 — Dependency without exit

**Mechanism.** A system a party comes to rely on, from which departure costs more
than the reliance is worth, converts a voluntary relationship into a captive one
with no act of coercion anywhere.

**Instantiation test.** What does leaving cost, and is that cost disclosed before
adoption?

**Falsifier.** Withdrawn where exit cost is disclosed at adoption and an export path
is maintained and exercised.

**Obligation.** [§H.10](../license/the-maher-license.md).

**In this estate:** `partial`. [MX-018](../corpus/mx-018-third-party-dependencies.md)
records **eight dependencies**, of which **D5 has exit `impossible`** and **D3
(domain) has high lock-in and no plan**.

### H6 — Displacement of the irreplaceable relation

**Mechanism.** A system that adequately performs the *function* of a human relation
— counsel, teaching, company — displaces the relation, and the displaced relation
does not return when the system is withdrawn.

**Instantiation test.** Does adoption reduce the frequency of a human relation that
served the same function?

**Falsifier.** Withdrawn where the system is shown to supplement rather than
substitute over a sustained period.

**Obligation.** [§H.11](../license/the-maher-license.md); engages absolute **(vii)**.

**In this estate:** `unexamined`.

---

## §3 — Stratum III: Economic (H7, H8, H9, H13)

Harms of extraction, asymmetry, and enclosure.

### H7 — Value extraction without reciprocity

**Mechanism.** A system that captures value a user creates — attention, data,
contribution, judgement — without returning proportionate value, where the
asymmetry is invisible because the user's contribution is not priced.

**Instantiation test.** What does the system receive that the user is not told they
gave?

**Falsifier.** Withdrawn where every input is disclosed and the user could decline
it and still use the system.

**Obligation.** [§H.12](../license/the-maher-license.md).

**In this estate:** `answered`. The estate receives nothing — no data, no
attention metrics, no contributions
([REG-06](../registries/reg-06-dataset-registry.md): no dataset about people).

### H8 — Informational asymmetry as a business model

**Mechanism.** A system that profits from the user not knowing something it knows,
where the asymmetry is the product rather than an incident of it.

**Instantiation test.** Would the system's revenue fall if the user knew what it
knows about them or about the transaction?

**Falsifier.** Withdrawn where the system holds no material information about the
user that it does not disclose to them.

**Obligation.** [§H.12](../license/the-maher-license.md).

**In this estate:** `answered`. The estate holds nothing —
[MX-003](../corpus/mx-003-privacy-notice.md), subject to the **unaudited hosting
layer** at [MX-003 §7](../corpus/mx-003-privacy-notice.md).

### H9 — Enclosure of a commons

**Mechanism.** A system built on a commons — open knowledge, public data, shared
infrastructure — that returns its output under terms preventing the commons from
absorbing it. Each enclosure is individually defensible; the aggregate removes the
conditions of the commons's reproduction.

**Instantiation test.** Could the commons the system drew from absorb the system's
output on the terms offered?

**Falsifier.** Withdrawn where output returns on terms at least as permissive as
those the inputs were taken under.

**Obligation.** [§H.13](../license/the-maher-license.md).

**In this estate:** `partial`. [ML-2.3](../license/the-maher-license.md) imposes
conditions stricter than many inputs carried. Whether that is enclosure or
protection is a **genuine question** the estate cannot resolve without counsel
([REG-08](../registries/reg-08-role-and-authority-registry.md)) and files as
`open` under [ST-06](../standards/st-06-objections-standard.md).

### H13 — Cost externalisation

**Mechanism.** A system whose operating costs — energy, moderation, attention,
cleanup, disposal — fall on parties outside the transaction, where the price
signals efficiency because the externalised cost is not in it.

**Instantiation test.** Who bears a cost of operation and is not party to it?

**Falsifier.** Withdrawn where the operating cost borne by non-parties is measured
and disclosed.

**Obligation.** [§H.14](../license/the-maher-license.md).

**In this estate:** `partial`. The estate has **not measured** the energy cost of
the AI system that authored it ([MX-018 D5](../corpus/mx-018-third-party-dependencies.md)),
and that cost is externalised. This is a real instantiation, disclosed and
unremedied.

---

## §4 — Stratum IV: Material (H10, H11, H12, H14)

Harms in the physical and infrastructural world.

### H10 — Embodied cost invisibility

**Mechanism.** Computing presents as immaterial. The extraction, manufacture,
energy and disposal behind it are real, distant, and borne by people who are not
users. Invisibility is not incidental — it is a property of the interface.

**Instantiation test.** Does any surface disclose the physical cost of operation?

**Falsifier.** Withdrawn where embodied and operating physical cost is disclosed at
a granularity a user could act on.

**Obligation.** [§H.14](../license/the-maher-license.md).

**In this estate:** `partial` — same gap as H13.

### H11 — Correlated infrastructural failure

**Mechanism.** Coupling reduces the frequency of small failures and increases the
severity and correlation of large ones. The pre-digital regime failed often and
locally; the current regime fails rarely and everywhere at once. These are not
comparable by expected value.

**Instantiation test.** Does the system share an update channel or failure domain
with its own redundancy?

**Falsifier.** Withdrawn as to any deployment that (i) publishes its critical
dependency map including single points of failure, (ii) maintains and **exercises**
a documented non-digital fallback for life-safety and payment functions, and (iii)
does not share a failure domain with its redundancy. Sustained evidence that
correlated-failure frequency and severity decline as coupling increases would
defeat the thesis.

**Obligation.** [§H.15](../license/the-maher-license.md) — dependency mapping and,
for Works in critical functions, a documented and exercised fallback. **Not
absolute.**

**In this estate:** `partial`. [ST-19](../standards/st-19-two-plane-architecture.md)
states the island contract — the content plane must render with the identity plane
dead — and it is **untested** ([B-14](../00-governance-map/launch-blockers.md)).
[MX-018](../corpus/mx-018-third-party-dependencies.md) now supplies the dependency
map the obligation requires; **D3 has no fallback**.

### H12 — Irreversible material commitment

**Mechanism.** Infrastructure decisions that are cheap to make and expensive to
unmake, taken by parties who will not bear the unmaking.

**Instantiation test.** What would reversing this decision cost in five years, and
who would pay?

**Falsifier.** Withdrawn where reversal cost is estimated and published before
commitment.

**Obligation.** [§H.15](../license/the-maher-license.md).

**In this estate:** `partial`. [ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md)
makes identifiers immortal — a deliberate irreversible commitment whose cost
[MX-004 §3.1](../corpus/mx-004-terms-of-top-levels.md) discloses: **nine pillars
are arbitrary and now permanent**.

### H14 — Degradation of the non-digital alternative

**Mechanism.** As a digital path becomes dominant the non-digital path is
withdrawn for want of use, and those who cannot use the digital path lose access to
a service that was previously universal. Nobody decides to exclude them.

**Instantiation test.** Is there a non-digital path, and is it maintained to a
standard a user could actually rely on?

**Falsifier.** Withdrawn where a non-digital path is maintained and exercised.

**Obligation.** [§H.15](../license/the-maher-license.md); overlaps
[MX-010 accessibility](../corpus/mx-010-accessibility.md).

**In this estate:** `partial`. The corpus is text and portable
([MX-019 W5](../corpus/mx-019-sunset-and-wind-down.md) requires a plain-Markdown
archive) — and **W5 has never been performed**.

---

## §5 — Stratum V: Reflexive (H15–H19)

**Harms the estate causes by publishing this register.** New in v2026.10.1. This
stratum exists because a harms register that cannot turn on itself is incomplete.

### H15 — The register as absolution

**Mechanism.** Publishing a harm creates the impression it is being managed.
Disclosure substitutes for remedy, and the disclosing party accrues credibility
for the disclosure that it has not earned by the remedy.

**Instantiation test.** Are harms disclosed at a higher rate than they are remedied?

**Falsifier.** Withdrawn where the remedy rate is published alongside the
disclosure rate.

**Obligation.** [§H.16](../license/the-maher-license.md); engages the
**§H.16.3 all-clear presumption** — the absence of a recorded harm is **not**
evidence of its absence.

**In this estate:** **`FAILS`**.
[REG-07 §5.1](../registries/reg-07-defect-classification-registry.md): **every
closed defect is cosmetic; no substantive defect has been closed.**
[BX-006](../bcia/bx-006-phase-failure-catalogue.md): **seven free remedies,
none adopted.** The estate is disclosing at a far higher rate than it remedies, and
this harm names it.

### H16 — Disclosure as trust amplifier

**Mechanism.** A party that discloses its faults earns credibility that transfers
to claims it has **not** verified. The honesty is real; the transfer is unearned;
neither party notices.

**Instantiation test.** Does the disclosing party make unverified claims in the
same document as its disclosures?

**Falsifier.** Withdrawn where every claim carries its own evidence class **at the
point of the claim**, so credibility cannot transfer across a page.

**Obligation.** [§H.16](../license/the-maher-license.md).

**In this estate:** **`FAILS`**. Identified independently at
[BX-002 §3.1](../bcia/bx-002-contact-phase.md) as a phase C failure with **no
control at all**. [BX-008 §3.1](../bcia/bx-008-bcia-and-machine-readers.md) adds
that evidence classes are carried in prose and are the mechanism **least likely to
survive** fragmentary reading.

### H17 — Self-assessment presented as assessment

**Mechanism.** An organisation that audits itself and publishes the audit produces
an artefact indistinguishable in form from an independent one. Readers cannot tell,
and the form does the persuading.

**Instantiation test.** Is any published assessment independent?

**Falsifier.** Withdrawn where self-assessments are labelled as such at the point of
the finding and at least one independent assessment exists.

**Obligation.** [§H.16](../license/the-maher-license.md).

**In this estate:** **`FAILS`**.
[AG-011 §4.2](../agents/ag-011-agent-review-and-audit.md): **review debt is 100% at
every level.** Every audit in this corpus —
[RB-03](../rubrics/rb-03-instrument-quality-rubric.md)'s scores,
[AG-010](../agents/ag-010-agent-error-and-correction.md)'s error record,
[REG-02](../registries/reg-02-page-registry.md)'s compliance findings,
[BX-005](../bcia/bx-005-phase-audit-method.md)'s phase audits — is **self-review,
which [AG-011 §2.1](../agents/ag-011-agent-review-and-audit.md) defines as not a
review at all.**

### H18 — Incapacity absorbing capability

**Mechanism.** An organisation that documents a genuine limitation uses it, without
dishonesty, to stop examining what remains possible. The limitation is real; its
scope is overstated; and the overstatement is invisible because the limitation is
true.

**Instantiation test.** Is any refused capability adjacent to an unexamined
available one?

**Falsifier.** Withdrawn where each stated incapacity is accompanied by an
enumeration of what remains possible despite it.

**Obligation.** [§H.16](../license/the-maher-license.md).

**In this estate:** **`FAILS`**, **twice, independently found**:
[AG-011 §5.1](../agents/ag-011-agent-review-and-audit.md) — source-checking needs
no second participant and was absorbed into the
[DEF-031](../00-governance-map/defect-register.md) excuse; and
[BX-004 §4.1](../bcia/bx-004-after-phase.md) — three pull-side remedies need no
address list and were absorbed into the notification refusal.
[BX-006 §5.1](../bcia/bx-006-phase-failure-catalogue.md) names this as one of three
mechanisms that kept seven free remedies invisible.

### H19 — Volume as evidence

**Mechanism.** A large, consistent, heavily cross-referenced body of work reads as
authoritative in proportion to its size. Volume is produced by capacity, not by
correctness, and a reader cannot distinguish a thorough corpus from a prolific one.

**Instantiation test.** Does the body of work's persuasiveness rest on any property
that would survive its being wrong?

**Falsifier.** Withdrawn where the work's claims are independently checked at a rate
proportional to their number.

**Obligation.** [§H.16](../license/the-maher-license.md).

**In this estate:** **`FAILS`**. Roughly **eighty instruments**, thousands of
cross-references, **zero source checks ever performed**
([AG-011 §3.1](../agents/ag-011-agent-review-and-audit.md)). The corpus's
fabrication rate is, in [AG-010 §3.1](../agents/ag-010-agent-error-and-correction.md)'s
words, *"unknown and unknowable from inside"*. **This harm describes the document
you are reading.**

---

## §6 — Stratum VI: Successor (H20–H25)

Harms to those who come after — later readers, later maintainers, later systems.
New in v2026.10.1.

### H20 — The unmarked draft

**Mechanism.** An incomplete work published without a marker is indistinguishable
from a complete one, and the reader who relies on it cannot know what is missing.

**Instantiation test.** Does any published artefact present as complete while
unfinished?

**Falsifier.** Withdrawn where every incomplete artefact carries a marker on its
face.

**Obligation.** [§H.17](../license/the-maher-license.md).

**In this estate:** **`FAILS` — and this harm names its own predecessor.** The
[fourteen-harm draft](hx-000-the-fourteen-structural-harms.md) presented as
`status: canonical` while ending at an append-point, and it was the **tier 1a**
instrument. [AG-012 §3.1](../agents/ag-012-agent-sunset-and-withdrawal.md) records
the marker as owed. This re-version discharges it for HX-000 and **not** for the
rest of the corpus.

### H21 — The stale register as false instruction

**Mechanism.** A record that describes a past state instructs a successor to act on
conditions that no longer hold. Unlike a merely incomplete record, a stale one
causes **action**.

**Instantiation test.** Would a successor acting on the registers do something
destructive?

**Falsifier.** Withdrawn where registers are reconciled at the end of each
production session.

**Obligation.** [§H.17](../license/the-maher-license.md).

**In this estate:** **`FAILS`, severity S1.**
[AG-008 §5.1](../agents/ag-008-agent-collaboration-protocol.md) found that the
[task ledger](../00-governance-map/task-ledger.md) has **no rows for ~40
instruments**, and that a successor acting on it would attempt to draft files that
already exist — while
[AG-005 §5.1](../agents/ag-005-agent-tool-use-limits.md) records **zero compliance**
with archive-before-overwrite. Previously `unexamined`; this version records it as
instantiated.

### H22 — Permanence without a bearer

**Mechanism.** Commitments of unbounded duration made by a bounded institution.
The commitment is honest; the duration is not available to the party making it.

**Instantiation test.** Does the work make a promise longer than its own expected
life?

**Falsifier.** Withdrawn where each permanence promise states who will keep it after
the promising party stops.

**Obligation.** [§H.17](../license/the-maher-license.md).

**In this estate:** **`FAILS`**.
[MX-019 §5](../corpus/mx-019-sunset-and-wind-down.md) sorts the estate's permanence
promises: **eight die with the estate, five survive**, and all five that survive are
properties of *text* while all eight that die are properties of *process*. Every
route promise rests on [MX-018 D3](../corpus/mx-018-third-party-dependencies.md),
a domain with **no succession arrangement**.

### H23 — Interpretive foreclosure

**Mechanism.** A work that records how it was construed constrains a successor to
that construction, including where it was wrong. Recording the reasoning is
correct; it also forecloses.

**Instantiation test.** Would a successor be able to reach a different reading of
the founding instruction?

**Falsifier.** Withdrawn where recorded constructions are labelled as the
predecessor's readings rather than as settled meaning.

**Obligation.** [§H.17](../license/the-maher-license.md).

**In this estate:** `partial`, and **acute**.
[AG-007 §5](../agents/ag-007-agent-instruction-interpretation.md) records four
constructions, of which **K1 may be wrong** — and roughly eighty instruments rest
on it. [AG-008 §3.1](../agents/ag-008-agent-collaboration-protocol.md) requires a
successor **not to re-derive** them, which is exactly the foreclosure this harm
names. The estate cannot have both handover safety and interpretive freedom, and it
has chosen safety without recording the trade until now.

### H24 — Detection ending with production

**Mechanism.** Where the same mechanism both produces work and discovers faults in
it, the withdrawal of that mechanism does not degrade fault-finding — it **ends**
it, leaving a body of work with no remaining route to correction.

**Instantiation test.** If production stopped today, would any fault ever be found
again?

**Falsifier.** Withdrawn where at least one detection mechanism operates
independently of production.

**Obligation.** [§H.17](../license/the-maher-license.md).

**In this estate:** **`FAILS`**. Previously `unexamined`.
[AG-012 §3.2](../agents/ag-012-agent-sunset-and-withdrawal.md) establishes that the
agent is **simultaneously the estate's sole producer and its sole detector** —
errors are found *by writing, not by checking*
([AG-010 §1.3](../agents/ag-010-agent-error-and-correction.md)) — and that
[SENTINEL](../standards/st-13-static-build-and-sentinel.md), L-1 source checks, and
every review level are **already orphaned**.

### H25 — Undetectable cessation

**Mechanism.** A work that stops being maintained gives no signal that it has
stopped. A reader a year later sees the same surface and cannot distinguish a
maintained corpus from an abandoned one.

**Instantiation test.** Can a reader tell, from the work alone, whether it is still
being maintained?

**Falsifier.** Withdrawn where the work publishes a last-production date a reader
can compare to today.

**Obligation.** [§H.17](../license/the-maher-license.md).

**In this estate:** **`FAILS`**.
[AG-012 §5.2](../agents/ag-012-agent-sunset-and-withdrawal.md) —
*"agent withdrawal fails quietly and never finishes failing"* — and the remedy
**W7, a last-production date at the root, does not exist**. The one partial
protection (next review date in the page stamp) was adopted for a different reason
entirely ([MX-019 §6](../corpus/mx-019-sunset-and-wind-down.md)).

---

## §7 — The estate's own state

| Stratum | Harms | `answered` | `partial` | **`FAILS`** | `unexamined` |
|---|---|---|---|---|---|
| I Cognitive | H1–H3 | 0 | 2 | **1** | 0 |
| II Relational | H4–H6 | 0 | 1 | **1** | 1 |
| III Economic | H7, H8, H9, H13 | 2 | 2 | 0 | 0 |
| IV Material | H10, H11, H12, H14 | 0 | 4 | 0 | 0 |
| **V Reflexive** | H15–H19 | 0 | 0 | **5** | 0 |
| VI Successor | H20–H25 | 0 | 1 | **5** | 0 |
| **Total** | **25** | **2** | **10** | **12** | **1** |

### 7.1 Reading the tally

**Twelve of twenty-five FAIL**, and **ten of the twelve are in the two new
strata**.

That is the finding of this re-version, and it is not a coincidence of drafting.
Strata I–IV were written against *systems the estate might license*. Strata V–VI
were written against **the estate itself**, and the estate fails almost all of
them.

The predecessor could not have found this. A register of fourteen harms about
computing and networking had no category in which *"we disclose faster than we
remedy"* (H15), *"our honesty makes our unchecked claims persuasive"* (H16), or
*"we are prolific and unchecked"* (H19) could even be stated.

**So the count did not change from fourteen to twenty-five because eleven more
harms were discovered in the world. It changed because the register was turned on
its author, and eleven of the additions landed.**

### 7.2 What this does not license

The estate does **not** claim credit for this tally. Under **H15** — the register as
absolution — publishing twelve failures is precisely the move that substitutes
disclosure for remedy, and **H15 is itself one of the twelve**.

The tally is a statement of position, not a discharge. It becomes a discharge only
when the count falls, and the count falls only through the seven free remedies at
[BX-006 §5](../bcia/bx-006-phase-failure-catalogue.md) — **none adopted** — and the
five owed repairs at [AG-010 §5](../agents/ag-010-agent-error-and-correction.md).

---

## §8 — Limits

1. **H12–H25 have been reviewed by nobody.** Fourteen new harms, self-authored,
   self-assessed — which is **H17** operating on this page.
2. **The predecessor's full treatment of H1–H11** — mechanisms, evidence,
   counter-arguments, replies, ethical mappings, ~89,000 bytes — is **retained and
   superseded** at
   [hx-000-the-fourteen-structural-harms.md](hx-000-the-fourteen-structural-harms.md).
   The entries in §§1–4 here are the **operative** form; the predecessor holds the
   argument. A reader assessing whether a harm is well-founded should read both.
3. **No legal competence** (gap 3). Nothing here construes
   [§H.3(a)](../license/the-maher-license.md)'s eight absolutes, and no absolute is
   paraphrased ([ST-09 §3.3](../standards/st-09-summary-and-abstract-standard.md)).
4. **Evidence is not restated per harm** in this version. For H1–H11 it is in the
   predecessor; **for H12–H25 there is none** — they are reasoned from the estate's
   own record, which makes them **E1** where they cite it and **E0** where they
   generalise.
5. **H6 remains `unexamined`** — the only one, and it concerns displacement of
   human relation, which the estate has no way to observe.
6. **This document is ~14,000 words shorter than its predecessor while governing
   eleven more harms.** That is a real loss of argumentative depth, disclosed rather
   than concealed, and the remedy is to carry each H12–H25 entry to full treatment
   in later versions.
7. **No Arabic text**, while `prevailing_text: ar`. The **prevailing text of the
   tier 1a instrument does not exist**
   ([MX-020](../corpus/mx-020-language-authority.md)) — which for a document
   incorporated into the licence is the corpus's single most serious language gap.

## §9 — Falsifier

> **IF FALSE.** This register is falsified if:
>
> - **(a)** a harm listed here fails any of §0.1's five inclusion criteria —
>   **most likely for H12–H25**, which were reasoned from one estate's record rather
>   than from a survey;
> - **(b)** any harm's falsifier is shown to be unsatisfiable in principle, making
>   it a **doctrine** rather than a harm (§0.1 criterion 4);
> - **(c)** a `FAILS` entry in §7 is shown to be wrong — **the estate would welcome
>   this** and it is checkable against the cited instrument in each case;
> - **(d)** an `answered` entry (H7, H8) is shown to be instantiated — **H8 is the
>   likely one**, since it rests on the **unaudited hosting layer**
>   ([MX-003 §7](../corpus/mx-003-privacy-notice.md));
> - **(e)** a twenty-sixth structural harm is identified that none of the six strata
>   reaches;
> - **(f)** [ML-2.3](../license/the-maher-license.md) is shown to name a harm this
>   register does not carry — **which would mean §A.10's reference is still
>   dangling** and [DEF-021](../00-governance-map/defect-register.md) is not
>   discharged.
>
> **(f) is the test that matters most** and is a direct comparison between this
> register and the licence's own enumeration. It is the check that should have been
> run before this document was published and **was not**.

## §10 — Obligation

**On a licensee:**
- Apply the **instantiation test** for each harm to the deployment, using
  [HX-001](hx-001-harm-audit-rubric.md)'s five dimensions. **No total score** — a
  composite lets a passing dimension conceal a failing one.
- Observe the Part H duties each harm generates. The duties are in
  [ML-2.3](../license/the-maher-license.md), not here.
- Observe the **eight absolutes** of [§H.3(a)](../license/the-maher-license.md).
  Seven are cumulative; **(vii) developmental substitution is disjunctive** and
  bites alone.
- Do not treat the absence of a recorded harm as an all-clear —
  **[§H.16.3](../license/the-maher-license.md)**.

**On the estate:**
- **Run falsifier §9(f)** — compare this register against
  [ML-2.3](../license/the-maher-license.md)'s enumeration. Until run,
  [DEF-021](../00-governance-map/defect-register.md) is discharged only
  provisionally.
- **Mark the predecessor superseded on its face**
  ([AG-012 W1](../agents/ag-012-agent-sunset-and-withdrawal.md)) and record the
  redirect ([SITE-03](../site/routing-law.md), append-only).
- Record in **both** this document and
  [ML-2.3](../license/the-maher-license.md) that Tier 1's operative content changed
  — [ST-15 A6](../standards/st-15-amendment-and-versioning-standard.md).
- **Reduce the twelve `FAILS`**, beginning with the seven free remedies
  ([BX-006 §5](../bcia/bx-006-phase-failure-catalogue.md)). Under **H15**,
  publishing this tally is not a remedy.
- Carry H12–H25 to full treatment (§8.6).

---

### Related

**What incorporates this register** — [ML-2.3](../license/the-maher-license.md) ·
[precedence](../00-governance-map/precedence-and-conflict-rules.md) ·
[enforceability two-track table](../license/enforceability-two-track-table.md) ·
[scale gate](../license/scale-gate.md)

**How a harm is assessed** — [HX-001](hx-001-harm-audit-rubric.md) ·
[HX-002](hx-002-harm-instrument-map.md) ·
[RB-05](../rubrics/rb-05-harm-review-gate.md) ·
[BX-007](../bcia/bx-007-bcia-and-harms.md)

**Where the reflexive and successor failures are recorded** —
[AG-010](../agents/ag-010-agent-error-and-correction.md) ·
[AG-011](../agents/ag-011-agent-review-and-audit.md) ·
[AG-012](../agents/ag-012-agent-sunset-and-withdrawal.md) ·
[BX-006](../bcia/bx-006-phase-failure-catalogue.md)

**The superseded text and the record of this change** —
[HX-000 v2026.09.4](hx-000-the-fourteen-structural-harms.md) ·
[version history](../license/version-history.md) ·
[ST-15](../standards/st-15-amendment-and-versioning-standard.md) ·
[changelog](../00-governance-map/changelog.md)

### Exit pair

1. **Run the comparison that discharges DEF-021.** Falsifier §9(f) — set this
   register beside [ML-2.3](../license/the-maher-license.md)'s enumeration. It
   should have been run before publication and was not.
2. **Read the stratum that failed.** [§7.1](#71-reading-the-tally) — ten of the
   twelve failures are in the two strata written against the estate itself, and the
   register could not have found them before it was turned on its author.

<!-- mx-pagestamp: HX-000 · v2026.10.1 · governing · tier 1a · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; H12–H25 are new in this version and have been reviewed by nobody -->
