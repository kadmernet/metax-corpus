---
doc_id: REG-05
title_en: Credential Registry
title_ar: سجل الشهادات
family: registries
version: v2026.10.1
status: published
authority: record
prevailing_text: ar
audience_tier: 2
depth: meta
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [credentials, assessment, proof, registry, verification]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. No credential has been issued; the register is empty of holders by design and by fact.
route: /registries/credentials/
---

# REG-05 — Credential Registry

> **Authority note.** A **record**. The rules of assessment are
> [RB-01 D1–D5](../rubrics/rb-01-d1-d5-rubric.md) and
> [RB-02 proof ladder](../rubrics/rb-02-proof-ladder.md), both tier 5. Appeals are
> [MX-016](../corpus/mx-016-appeals-and-due-process.md). This page records issued
> credentials and nothing else.

> **Disclosure first.** **Zero credentials have been issued.** The register is
> published empty. An empty credential registry is more informative than a missing
> one: it tells a prospective holder that the machinery has never been exercised,
> that no precedent exists, and that they would be the first — which are exactly
> the facts a person deciding whether to invest effort needs, and exactly the facts
> that a silent absence conceals.

---

## 1. Position

A credential is a **claim the estate makes to third parties about a person**. That
makes it categorically different from everything else in the corpus:

- A page that is wrong misinforms a reader who can check it.
- A **credential** that is wrong misinforms an employer, a school, or a
  counterparty about someone who cannot easily correct the record.

Consequently the estate's posture on credentials is **restrictive by design**. The
governing constraint is [RB-02](../rubrics/rb-02-proof-ladder.md): the proof level
is **printed on the credential itself**, and level **P0 is uncreditable** — it
cannot appear on any issued credential at all. A credential that does not say how
strongly it was proved is, in this estate, a forgery of its own authority.

## 2. Definition

A **credential** is an issued, revocable, publicly verifiable statement that a
named holder demonstrated stated competences at a stated proof level, satisfying
**seven** conditions:

1. **Named competences**, each traceable to a `D`-dimension in
   [RB-01](../rubrics/rb-01-d1-d5-rubric.md) (D1–D5).
2. **Per-dimension scores** on the 0–4 scale, printed individually. **No total
   score** — RB-01 refuses composites, and the credential inherits that refusal.
3. **Proof level** P1, P2, or P3 from [RB-02](../rubrics/rb-02-proof-ladder.md),
   printed on the face. **Never P0.**
4. **Rubric version**, frozen per cohort. The version assessed under is the
   version printed, permanently, even after the rubric changes.
5. **Assessor identity**, and whether the assessor was human, machine, or mixed —
   disclosed per [MX-007](../corpus/mx-007-ai-use-and-disclosure.md).
6. **Verification route**, resolvable by a third party with no account.
7. **Revocation state**, and if revoked, the date and the ground.

A statement lacking any of (1)–(7) is not a credential. It may be a letter, a
receipt, or an opinion, and it must not be described in credential language.

### 2.1 What the estate refuses to certify

| Refusal | Reason |
|---|---|
| Completion without demonstration | Attendance is not competence |
| Aggregate scores | RB-01 §3 — a total hides a failing dimension |
| Anything at P0 | RB-02 — self-report alone is uncreditable |
| Ranking of holders against each other | Cohort ranking converts assessment into competition and drives the harms in [HX stratum I](../harms/hx-000-the-fourteen-structural-harms.md) |
| Permanent credentials with no review | Competence decays; so must the claim |
| Credentials to entities, rather than persons | The subject of a competence claim is a person |

### 2.2 Revocability

Every credential is revocable on **four** grounds and no others:

1. **Assessment error** — the estate scored wrongly. Revocation plus correction.
2. **Fraud by the holder** — the demonstration was not theirs.
3. **Withdrawal of the competence claim** — the estate no longer believes the
   dimension measures what it claimed. Revocation without fault to the holder, and
   the record must say so explicitly.
4. **Holder request.**

Ground 3 is unusual and deliberate. If the estate discovers that D3 does not
measure what it said, holders of D3 claims are carrying a statement the estate no
longer stands behind. Leaving it in place would be more comfortable for everyone
and would make the estate a party to a claim it knows is unsupported.

## 3. Mechanism

### 3.1 Issue path

```
cohort opened          →  rubric version FROZEN
candidate demonstrates →  evidence captured at a proof level (P1/P2/P3)
assessment             →  per-dimension scores D1..D5, no total
assessor recorded      →  human / machine / mixed
credential minted      →  identifier assigned [immortal]
row written here       →  verification route live
```

The freeze at step 1 is what makes a credential meaningful years later. Without
it, "scored 3 on D2" is uninterpretable, because D2 may since have changed
meaning. The frozen version is therefore printed, not linked to "current".

### 3.2 Verification without accounts

Verification must work for a third party who has no relationship with the estate:
no login, no email, no tracking. This follows from
[MX-022 identity and sessions](../corpus/mx-022-identity-and-sessions.md) and from
[MX-023](../corpus/mx-023-attention-and-human-sovereignty.md)'s refusals — the
estate does not learn who is checking a credential. The consequence is that
verification reveals only what the holder consented to publish, and the estate
cannot offer "private verification" as a feature because it has no mechanism to
authenticate a verifier.

### 3.3 Appeals

An assessment is appealable through the three stages of
[MX-016](../corpus/mx-016-appeals-and-due-process.md). **Stage 2 is currently
unstaffable** — it requires a reviewer independent of the original assessor and
the estate has one participant
([DEF-031](../00-governance-map/defect-register.md)). Therefore:

> **Operative consequence.** Until stage 2 can be staffed, the estate **must not
> issue credentials**. Issuing an unappealable competence claim about a person is
> not a procedural shortcoming; it is the substance of the guarantee failing. This
> is the binding reason §5 is empty — not lack of demand.

## 4. Worked instance

**The blocking chain, followed to the end.**

Suppose a candidate demonstrates competence today at P2 (independent
observation), scoring D1=3, D2=3, D3=2, D4=4, D5=2. Every input exists: the rubric
is written, the ladder is written, the scores are computable, the identifier is
assignable.

Now walk the issue path and find where it stops:

| Step | Available? |
|---|---|
| Rubric version freeze | Yes — RB-01 v2026.10.1 |
| Proof level assignment | Yes — P2 defined |
| Per-dimension scoring | Yes |
| Assessor disclosure | Yes — would read `mixed`, AI-assisted |
| Identifier assignment | Yes |
| Verification route | Yes — static page, no account |
| **Appeal availability (MX-016 stage 2)** | **No — unstaffable** |

Six of seven work. The seventh is not a technical gap but a structural one: there
is nobody who is not the assessor. And under §3.3 that single absence is
dispositive, because the guarantee that makes a credential safe for the *holder*
is the one thing missing.

Note what the estate declines to do here. The convenient move would be to issue
the credential with a note that appeals are "temporarily limited". That converts
a structural incapacity into fine print, and it shifts the cost from the estate
(which cannot staff a role) to the holder (who loses a remedy). The estate does
not have the standing to make that trade on the holder's behalf.

## 5. The register

| ID | Holder | Competences | Scores (D1–D5) | Proof level | Rubric version | Assessor | Issued | Verify | State |
|---|---|---|---|---|---|---|---|---|---|
| — | — | — | — | — | — | — | — | — | — |

**The register contains no rows.** This is the true and intended state. See §3.3
for the reason and [B-01](../00-governance-map/launch-blockers.md) /
[RAT-04](../00-governance-map/open-questions-and-ratifications.md) for the
conditions under which it may gain its first.

### 5.1 Reserved identifier space

Per [ST-01](../standards/st-01-identifier-and-url-grammar.md), credential
identifiers take the form `CRED-` + zero-padded ordinal, assigned in issue order.
**`CRED-0001` is unassigned.** No identifier has been spent — unlike `S3` in
[REG-01](reg-01-series-registry.md), no careless citation has burnt a credential
number, which matters more here because a burnt credential number in a
verification route would be permanently unresolvable.

### 5.2 Statements that are *not* credentials

The estate has produced none of the following, and lists them so that none can be
mistaken for a credential later:

- No letters of competence.
- No completion certificates.
- No badges, points, streaks, or levels. Gamified progress markers are refused
  under [MX-023 §2](../corpus/mx-023-attention-and-human-sovereignty.md) as
  engagement instruments dressed as assessment.
- No endorsements of third parties.

## 6. Failure modes

| # | Failure | Mechanism | Current state |
|---|---|---|---|
| F1 | **Unappealable issue** | Credential issued while stage 2 unstaffed | **Prevented** — by refusing to issue |
| F2 | **Composite creep** | A "total" or "overall" appearing on a credential face | Prevented by §2(2); untested, nothing issued |
| F3 | **Rubric drift** | Old credential reinterpreted under a new rubric | Prevented by the freeze; untested |
| F4 | **P0 leakage** | Self-reported work credited | Prevented by §2(3) |
| F5 | **Verification requiring an account** | Convenience feature added | Prevented by §3.2; pressure will recur |
| F6 | **Silent non-revocation** | Estate stops believing a dimension, leaves credentials standing | **Untested** — ground 3 has never been exercised |
| F7 | **Ranking pressure** | Demand for comparability between holders | Refused in §2.1; demand not yet encountered |

Every entry in the "current state" column reads *prevented* or *untested*, and the
reason is the same: **nothing has been issued.** A control that has never been
under load is a specification, not a control. This register should be read as a
description of intended behaviour with an honest zero in the evidence column.

## 7. Limits

1. **No credential exists, so no claim here is empirically supported.** The entire
   document is **E0** under [ST-07](../standards/st-07-evidence-and-verify.md)
   except its statements about what other instruments say, which are E1.
2. **Stage 2 is unstaffable and no date exists for fixing it.** The remedy is
   naming role holders (RAT-04), which requires a second person.
3. **No Arabic text**, while `prevailing_text: ar`. For a document that would bind
   the estate's statements about real people, the absence of the prevailing text is
   more serious than elsewhere in the corpus.
4. **The estate cannot verify identity** without violating its own session
   refusals, which means fraud ground (2) is, in practice, detectable only by
   inspection of the work itself. That is a genuine limit on what a credential
   from this estate can mean, and it should be stated on the credential face —
   currently §2's seven conditions do **not** require it. Filed with **RAT-24**.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** any credential, certificate, badge, or letter of competence has been
>   issued by the estate and is absent from §5;
> - **(b)** any issued credential shows a total or composite score;
> - **(c)** any issued credential omits its proof level or its frozen rubric
>   version;
> - **(d)** any verification route requires an account, an email, or accepts a
>   tracking parameter.
>
> (a) is the load-bearing test and is trivially checkable: **one** issued document
> anywhere falsifies the register's central claim of emptiness. The estate asserts
> zero and invites the counter-example.

## 9. Obligation

None from the record itself. Bearing duties, all of which currently resolve to
*do not issue*:

- Do not issue while [MX-016](../corpus/mx-016-appeals-and-due-process.md) stage 2
  is unstaffable.
- Print per-dimension scores and never a total —
  [RB-01](../rubrics/rb-01-d1-d5-rubric.md).
- Print the proof level; refuse P0 — [RB-02](../rubrics/rb-02-proof-ladder.md).
- Freeze and print the rubric version.
- Disclose assessor composition — [MX-007](../corpus/mx-007-ai-use-and-disclosure.md).
- Verify without identifying the verifier —
  [MX-022](../corpus/mx-022-identity-and-sessions.md).
- Revoke on ground 3 even when it costs the estate credibility — §2.2.

---

### Related

**Assessment** — [RB-01](../rubrics/rb-01-d1-d5-rubric.md) ·
[RB-02](../rubrics/rb-02-proof-ladder.md) ·
[RB-05](../rubrics/rb-05-harm-review-gate.md) ·
[ST-07](../standards/st-07-evidence-and-verify.md)

**Due process** — [MX-016](../corpus/mx-016-appeals-and-due-process.md) ·
[MX-008](../corpus/mx-008-moderation-and-enforcement.md) ·
[MX-015](../corpus/mx-015-succession-and-continuity.md) ·
[DEF-031](../00-governance-map/defect-register.md)

**Refusals that constrain design** — [MX-023](../corpus/mx-023-attention-and-human-sovereignty.md) ·
[MX-022](../corpus/mx-022-identity-and-sessions.md) ·
[MX-014](../corpus/mx-014-research-ethics-and-exclusions.md)

**Siblings** — [REG-01](reg-01-series-registry.md) ·
[REG-02](reg-02-page-registry.md) · [REG-08](reg-08-role-and-authority-registry.md)

### Exit pair

1. **Falsify the emptiness.** Produce one credential issued by this estate. If you
   can, §8(a) has fired and the register is false.
2. **Attack the real blocker.** Read
   [MX-016 §3](../corpus/mx-016-appeals-and-due-process.md) on stage 2; nothing
   here moves until that role has a holder.

<!-- mx-pagestamp: REG-05 · v2026.10.1 · record · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; no credential has been issued or can currently be issued -->
