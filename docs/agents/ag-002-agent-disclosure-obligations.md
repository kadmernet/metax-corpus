---
doc_id: AG-002
title_en: Agent Disclosure Obligations
title_ar: واجبات الإفصاح عن الوكلاء
family: agents
version: v2026.10.1
status: published
authority: governing
prevailing_text: ar
audience_tier: 2
depth: meta
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: yes
last_reviewed: 2026-09-16
domain_tags: [agents, disclosure, ai-authorship, transparency, provenance]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000 in role R-1. This note is itself the minimum disclosure this instrument requires, and §5 shows it is insufficient.
provenance_of_purpose: MX-007 imposes disclosure duties on the estate; this instrument imposes them on the agent. Absent until v2026.10.1.
route: /agents/ag-002/
---

# AG-002 — Agent Disclosure Obligations

> **Authority.** `governing`, tier 4. Reader-facing AI disclosure is
> [MX-007](../corpus/mx-007-ai-use-and-disclosure.md) (tier 3, and therefore
> **superior** to this instrument). AG-002 governs what the **agent** must disclose
> about its own work. Where the two differ, MX-007 prevails.

> **Disclosure first.** The `authorship_note` field carried by every instrument in
> this corpus is the **minimum** this standard requires, and §5 demonstrates it is
> **insufficient** for its purpose: it tells a reader that an AI drafted the text
> and tells them nothing they can act on. The estate satisfies its disclosure rule
> and fails its disclosure aim, which is the distinction this instrument exists to
> draw.

---

## 1. Position

AI disclosure is usually treated as a labelling problem: say that a machine was
involved, and the duty is discharged.

That is wrong for a governance corpus, and the reason is specific. A reader of a
governing instrument needs to know not *whether* a machine wrote it but **what the
machine's involvement means for how much weight the text can bear**. Those are
different disclosures:

| Weak disclosure | Useful disclosure |
|---|---|
| "AI-generated" | "The legal classifications here were produced by a system with no legal training and no counsel review" |
| "AI-assisted" | "The severity ratings in this register were assigned by the system that caused the defects" |
| "Drafted with AI" | "The counts in §5 were produced by a system that cannot execute code and did not verify them" |

The right column tells a reader **which way to discount**. That is
[MX-017 §5](../corpus/mx-017-conflicts-of-interest.md)'s substitute **S2**
(direction of interest) applied to machine authorship, and it is the standard this
instrument sets.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **agent involvement** | Any contribution by a non-human system to an artefact |
| **involvement class** | The kind of contribution — see §3 |
| **bearing disclosure** | A disclosure stating what the involvement means for reliance |
| **label disclosure** | A disclosure stating only that involvement occurred |
| **capability gap** | A thing the artefact appears to rest on that the agent cannot do |

### 2.1 The five capability gaps

An agent in this estate **cannot**:

1. **Execute or verify.** It cannot run code, so no count, census, or compliance
   rate it produces is machine-verified. All are **E1 at best** under
   [ST-07](../standards/st-07-evidence-and-verify.md).
2. **Be accountable.** It cannot be answerable for a judgement, which is why every
   [AG-001](ag-001-agent-roles-and-scopes.md) exit condition routes to a human.
3. **Hold a legal view.** No legal training, no counsel
   ([REG-08](../registries/reg-08-role-and-authority-registry.md)).
4. **Observe the world.** It cannot inspect hosting configuration, open an image
   file it was not given, or confirm a font is self-hosted.
5. **Persist or remember.** It cannot attest continuity between sessions, so no
   claim of the form "as previously verified" is available to it.

Every bearing disclosure is, in practice, a statement of which of these five gaps
the artefact sits on.

## 3. Involvement classes

| Class | Meaning | Bearing consequence |
|---|---|---|
| **I-1 Drafted** | The agent produced the text | Prose is the agent's; claims inherit gaps 1–5 |
| **I-2 Reconciled** | The agent compared instruments and recorded differences | Comparison is textual only; gap 1 applies to any count |
| **I-3 Audited** | The agent assessed compliance against a standard | Gap 1 and gap 2: findings unverified and unaccountable |
| **I-4 Classified** | The agent assigned a class or severity | **Gap 2 is dispositive** — see [AG-001 §5.1](ag-001-agent-roles-and-scopes.md) |
| **I-5 Rendered** | The agent restated tier 3 material at tier 1 | Gap 3 where the material is legal; the rendering is a summary owing [ST-09](../standards/st-09-summary-and-abstract-standard.md) S1–S5 |
| **I-6 Enumerated** | The agent produced a count or census | **Gap 1 is dispositive** — no count is verified |

### 3.1 The disclosure must name the class and the gap

> **Rule D1.** Every artefact with agent involvement discloses (a) the involvement
> class, (b) the capability gap the artefact's central claims rest on, and (c) the
> direction in which a reader should discount.

A disclosure naming only (a) is a **label disclosure** and is non-compliant.

### 3.2 Where disclosure must appear

| Location | Required |
|---|---|
| Front matter `authorship_note` | **Always** |
| At the point of the affected claim | **Where a central claim rests on a gap** |
| In the page stamp | Never — too compressed to carry bearing |
| In a machine surface field | When the surface exists ([ST-14](../standards/st-14-machine-surfaces-and-json-schemas.md)) |

The second row is where the corpus is weakest. A front matter note is read by
practitioners and skipped by everyone else; a census table with no local disclosure
reads as data.

### 3.3 What an agent must never disclose falsely

- **Never** imply verification it did not perform (gap 1).
- **Never** imply continuity across sessions (gap 5).
- **Never** present a legal classification as anything but untrained opinion
  (gap 3).
- **Never** describe its own output as independently reviewed
  ([MX-017 §4.3](../corpus/mx-017-conflicts-of-interest.md)).
- **Never** soften a disclosure because it undermines the artefact. The
  undermining is the information.

## 4. Mechanism

### 4.1 Producing a compliant disclosure

```
1. name the involvement class            (I-1..I-6)
2. identify the artefact's central claim
3. which of the five gaps does it rest on?
4. state the direction of discount
5. place it: front matter ALWAYS; at the claim if the claim is central (§3.2)
```

### 4.2 Worked form

Non-compliant (label only), as currently carried by most of this corpus:

> *Drafted by an AI system under AG-000.*

Compliant (bearing), for a census page:

> *Drafted by an AI system under AG-000 (class I-6, enumeration). The counts below
> were produced by reading file listings, not by executing a check: the system
> cannot run code, so no figure here is machine-verified and all are **E1**. Where
> a count flatters the corpus, discount it — the system produced both the corpus and
> the count.*

The second is four times longer and is the only one that lets a reader do
anything.

## 5. Worked instance

**Auditing this corpus's own disclosure against D1.**

Sample of four instruments, each with agent involvement, checked for (a) class,
(b) gap, (c) direction:

| Instrument | Class | (a) class named? | (b) gap named? | (c) direction? | D1 |
|---|---|---|---|---|---|
| [REG-02 page registry](../registries/reg-02-page-registry.md) | I-6 | No | **Partly** — §3.2 says counts are E1, not E3, and SENTINEL does not run | No | **Fail** |
| [RB-03 §6 self-score](../rubrics/rb-03-instrument-quality-rubric.md) | I-3, I-4 | No | No | **Yes** — "direction of interest is toward higher marks" | **Fail** |
| [MX-018 dependency register](../corpus/mx-018-third-party-dependencies.md) | I-1, I-4 | No | No | **Yes** — §7.6 states the discount direction | **Fail** |
| [REG-04 media registry](../registries/reg-04-media-registry.md) | I-1 | No | **Yes** — four images `unexamined`, gap 4 | No | **Fail** |

**Terminal state: `result` — four of four fail D1.**

### 5.1 What the audit exposed

**No instrument in the corpus names its involvement class**, because the class
taxonomy did not exist until this page. That part is unsurprising.

The interesting finding is the **pattern of partial compliance**. Each of the four
discloses **one** of the three D1 limbs and each discloses a different one:

- REG-02 names the gap (unverified counts) and not the direction.
- RB-03 names the direction and not the gap.
- MX-018 names the direction and not the gap.
- REG-04 names the gap (unexamined assets) and not the direction.

So the corpus's disclosure practice is **not weak but incoherent**: each author
pass disclosed whatever was salient in that document's subject matter, and nothing
enforced a common shape. A reader moving between instruments cannot form a stable
expectation of what a disclosure will tell them.

### 5.2 The finding that matters more

Working the instance surfaced something worse than incoherence.

**Gap 4 (cannot observe the world) is the corpus's most consequential capability
gap and is disclosed nowhere as a gap.** It appears repeatedly as a *fact about the
estate* and never as a *limit on the agent*:

| Where it appears | How it is framed | How it should be framed |
|---|---|---|
| [MX-003 §7](../corpus/mx-003-privacy-notice.md) hosting unaudited | The estate has not audited | The agent **cannot** audit; only a human can |
| [REG-04 `IMG-001`–`004`](../registries/reg-04-media-registry.md) | Four images unexamined | The agent **cannot** open them |
| [MX-018 D4](../corpus/mx-018-third-party-dependencies.md) font self-hosting unconfirmed | Unconfirmed | Unconfirmable **by the agent** |
| [MX-011 §4](../corpus/mx-011-security-and-disclosure.md) transport assumed | Assumed | Unverifiable **by the agent** |

The difference is not cosmetic. Framed as estate inaction, each reads as a task
awaiting attention. Framed as an agent capability gap, they read as **a class of
work that will never be done by the mechanism currently doing all the work** —
which is the accurate and more useful statement, and which connects directly to
[MX-018 D5](../corpus/mx-018-third-party-dependencies.md): the estate's sole
productive capacity cannot perform this class of task at all.

Filed rather than retro-fitted across four instruments, per
[ST-17 W6](../standards/st-17-worked-instance-standard.md).

## 6. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Label disclosure passing as bearing** | **Actual** — most of the corpus (§5) |
| F2 | **Incoherent partial compliance** | **Actual** — §5.1 |
| F3 | **Gap 4 framed as inaction** | **Actual** — §5.2, four instruments |
| F4 | **Verification implied** | Guarded by §3.3; the easiest breach to commit accidentally |
| F5 | **Continuity implied across sessions** | Guarded by §3.3 (gap 5) |
| F6 | **Disclosure softened because it undermines** | Guarded by §3.3; unverifiable |
| F7 | **Disclosure only in front matter** | **Widespread** — §3.2 row 2 |

## 7. Limits

1. **Four of four sampled instruments fail D1**, and the sample was chosen by the
   agent that wrote them.
2. **This instrument is itself only partly compliant.** Its `authorship_note` names
   the class (I-1, R-1) and does not name a gap or a direction. That is deliberate
   and disclosed: it demonstrates the failure mode rather than hiding it.
3. **No mechanism enforces D1.** [ST-13](../standards/st-13-static-build-and-sentinel.md)
   could check for the presence of three limbs; it does not run
   ([DEF-001](../00-governance-map/defect-register.md)).
4. **Gap 4's reframing (§5.2) is owed across four instruments** and not done.
5. **The five gaps are the agent's own account of its limits** — a self-report
   about self-knowledge, which is the least verifiable disclosure in the corpus.
6. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** an artefact with agent involvement lacks any of D1's three limbs —
>   **fires on nearly the whole corpus** (§5);
> - **(b)** a central claim rests on a capability gap with no disclosure at the
>   point of the claim (§3.2);
> - **(c)** an agent-produced artefact implies verification, continuity, or legal
>   competence (§3.3);
> - **(d)** the five gaps in §2.1 are shown to be incomplete — **the most valuable
>   test**, because the list is the agent's self-report;
> - **(e)** a disclosure is shown to have been softened between drafts (F6).
>
> **(d) is what a reader should attack.** A system enumerating its own limits will
> omit the limits it cannot perceive, and §2.1 is exactly such a list. A sixth gap
> almost certainly exists and the agent is the party least able to name it.

## 9. Obligation

**On an agent:**
- Disclose **class, gap, and direction** — all three (D1, §3.1).
- Disclose **at the claim**, not only in front matter, where a central claim rests
  on a gap (§3.2).
- Never imply verification, continuity, or legal competence (§3.3).
- Never soften a disclosure because it weakens the artefact (§3.3).
- Frame a gap-4 limitation as **an agent incapacity**, not estate inaction (§5.2).

**On the estate:**
- Reframe the four gap-4 instances (§5.2) — owed.
- Require D1's three limbs in `authorship_note`, or state that the requirement is
  waived.
- Treat [MX-007](../corpus/mx-007-ai-use-and-disclosure.md) as prevailing where it
  demands more (§ authority note).
- Ask a reader to name the sixth capability gap (§8d); the agent cannot.

---

### Related

**Disclosure above this instrument** — [MX-007](../corpus/mx-007-ai-use-and-disclosure.md) ·
[ST-02](../standards/st-02-front-matter-schema.md) ·
[ST-07](../standards/st-07-evidence-and-verify.md) ·
[MX-017](../corpus/mx-017-conflicts-of-interest.md)

**Agent powers and their limits** — [AG-000](ag-000-agent-constitution.md) ·
[AG-001](ag-001-agent-roles-and-scopes.md) ·
[AG-009](ag-009-prohibited-actions.md) ·
[AG-004](ag-004-refusal-and-escalation-register.md)

**Instruments failing D1** — [REG-02](../registries/reg-02-page-registry.md) ·
[REG-04](../registries/reg-04-media-registry.md) ·
[RB-03](../rubrics/rb-03-instrument-quality-rubric.md) ·
[MX-018](../corpus/mx-018-third-party-dependencies.md)

**Where gap 4 bites** — [MX-003](../corpus/mx-003-privacy-notice.md) ·
[MX-011](../corpus/mx-011-security-and-disclosure.md) ·
[REG-06](../registries/reg-06-dataset-registry.md) ·
[GM-08](../00-governance-map/verification-log.md)

### Exit pair

1. **Name the sixth gap.** §2.1 lists five limits, enumerated by the system they
   limit. Falsifier §8(d) is the one an outsider is better placed to run.
2. **See the reframing that is owed.** [§5.2](#52-the-finding-that-matters-more) —
   four instruments describe estate inaction where the truth is agent incapacity.

<!-- mx-pagestamp: AG-002 · v2026.10.1 · governing · tier 4 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; most disclosures in this corpus are label disclosures, not bearing ones -->
