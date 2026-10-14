---
doc_id: MX-011
title_en: Security and Vulnerability Disclosure
title_ar: الأمن والإفصاح عن الثغرات
family: corpus
version: v2026.10.1
status: published
authority: governing
prevailing_text: ar
audience_tier: 2
depth: meta
evidence_class: semi-durable
review_interval_months: 6
curator: Maher
license: ML-2.3
designated: yes
last_reviewed: 2026-09-16
domain_tags: [security, disclosure, vulnerability, static, threat-model]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. No security review has been performed by any party.
provenance_of_purpose: Cited by MX-024 and ST-22 since inception; absent until v2026.10.1.
route: /security/
---

# MX-011 — Security and Vulnerability Disclosure

> **Authority.** `governing`, tier 3. Platform constraints are
> [ST-22](../standards/st-22-platform-and-persistence.md) and
> [MX-024](mx-024-infrastructure-and-migration.md); the reporting channel is
> [MX-006](mx-006-contact-and-correspondence.md); data holdings are
> [REG-06](../registries/reg-06-dataset-registry.md).

> **Disclosure first.** **No security review has ever been performed** — not by the
> estate, not by a third party, not automatically. The threat model in §3 is
> reasoned, not tested. The estate's principal security property is **not having
> much to attack**: no accounts, no user data, no server-side logic. That is a real
> property and it is also a description of an estate that has not yet built the
> things that get attacked.

---

## 1. Position

Security instruments usually describe controls. This one mostly describes
**absences**, and the honest framing is that the estate's security posture is a
consequence of its incapacity rather than of its diligence.

Two claims a reader should keep apart:

- **"There is little to steal."** True, and verifiable: no accounts, no personal
  data ([MX-003](mx-003-privacy-notice.md)), no payment path active
  ([MX-021](mx-021-payments-and-commerce.md)).
- **"The estate is secure."** Not established. Nobody has looked.

The second does not follow from the first. A static site with nothing to steal can
still be defaced, have its integrity compromised, or serve altered governing text
— and **integrity, not confidentiality, is this estate's primary security
interest**, because the whole value of a governance corpus is that its text is
what it says it is.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **integrity compromise** | Published text differs from the text the estate authored and recorded |
| **availability loss** | The service is unreachable. **Not promised** ([MX-002 §4.1](mx-002-terms-of-service.md)) |
| **confidentiality breach** | Disclosure of data that should not be disclosed. Scope is narrow — see §3.2 |
| **supply-chain compromise** | A third-party asset serves altered or hostile content |
| **vulnerability** | A condition permitting any of the above |

### 2.1 Why integrity ranks first

If an attacker alters [ML-2.3](../license/the-maher-license.md) — changing a cure
period, removing an absolute from §H.3(a), softening a harm — a reader could
rely on text the estate never wrote, in a document whose entire function is to be
relied on. No confidentiality loss the estate could suffer compares, because the
estate holds almost nothing confidential.

This ordering drives §4: the controls that matter most are the ones that make
**text tampering detectable**, and the estate's are weak.

## 3. Threat model

### 3.1 In the model

| # | Threat | Impact | Current control |
|---|---|---|---|
| T1 | **Governing text altered at rest** (repository or host) | Severe — readers rely on false text | Git history; **no signed commits, no published digests** |
| T2 | **Governing text altered in transit** | Severe | Transport encryption (assumed, **unverified**) |
| T3 | **Supply-chain compromise** of a third-party asset (font, CDN) | Moderate to severe | **None** — asset not confirmed self-hosted ([REG-04](../registries/reg-04-media-registry.md)) |
| T4 | **Defacement** | Moderate; reputational | Host access controls (**unaudited**) |
| T5 | **Availability loss** | Low — not promised | None, by design |
| T6 | **Reader data exposure** | Low if §3.2 holds; **unknown** | [MX-003 §7](mx-003-privacy-notice.md) — the unaudited layer |
| T7 | **Curator account compromise** | Severe — enables T1 and T4 | Unstated; **single account, no published practice** |
| T8 | **Silent history rewrite** | Severe — defeats the no-silent-edits rule | Git history is rewritable by the account holder |

### 3.2 Out of the model

- **User account attacks** — no accounts exist.
- **Payment fraud** — no payment path active.
- **Injection against a database** — no server-side query path is reachable by a
  reader.
- **Session hijacking** — sessions are not identities
  ([MX-022](mx-022-identity-and-sessions.md)).

These are genuinely out of the model, and each becomes in-model the moment the
corresponding capability is built. The review trigger is therefore **capability
acquisition, not the calendar** — the same rule as
[MX-005 §4.3](mx-005-scope-and-boundaries.md).

### 3.3 T8 deserves its own paragraph

The estate's central governance commitment is **no silent edits**
([Charter §0.8](mx-000-charter.md)). That commitment is enforced by a git history
that the curator can rewrite. There is no external witness, no signed tag, no
published commit digest, and no third-party mirror.

So the estate's strongest claim about itself rests on an unwitnessed record held
by the only person with an interest in its contents. The estate is not aware of
any rewrite, and its awareness is not evidence. This is the most serious
unmitigated item in this instrument and the cheapest to fix — a published digest
per release, or a mirror, would convert an unfalsifiable claim into a checkable
one.

## 4. Controls, stated honestly

| Control | Present? | Notes |
|---|---|---|
| No server-side application code | **Yes** | Static files only; largest single reduction in attack surface |
| No user accounts | **Yes** | |
| No personal data at rest (by design) | **Yes, unverified** | [MX-003 §7](mx-003-privacy-notice.md) |
| Transport encryption | **Assumed** | Not verified as enforced, with no downgrade path |
| Signed commits | **No** | T1, T8 unmitigated |
| Published content digests per release | **No** | T1, T2 undetectable by a reader |
| Independent mirror | **No** | T8 unmitigated |
| Self-hosted assets confirmed | **No** | T3 |
| Dependency inventory | **Partial** | [REG-04](../registries/reg-04-media-registry.md); font licence unarchived |
| Automated checks | **No** | [ST-13 SENTINEL](../standards/st-13-static-build-and-sentinel.md) specified, not running ([DEF-001](../00-governance-map/defect-register.md)) |
| Access review for the hosting account | **No** | T7 |
| Security review by any party | **No** | — |

**Seven rows read "No".** A controls table with seven absences is published
because the alternative is a table listing only what exists, which would read as
adequate.

## 5. Vulnerability disclosure

### 5.1 How to report

Use the channels in [MX-006](mx-006-contact-and-correspondence.md). A security
report is a **report** under [MX-006 §4.1](mx-006-contact-and-correspondence.md),
so the filing duty engages: **it will be filed in the
[defect register](../00-governance-map/defect-register.md) whether or not the
estate agrees.**

| Property | Commitment |
|---|---|
| Acknowledgement | 14 days ([MX-006 §4.2](mx-006-contact-and-correspondence.md)) |
| Identification required? | **No.** Anonymous reports accepted on identical terms |
| Confidentiality asked of the reporter? | **No** — see §5.2 |
| Bounty | **None.** The estate has no funds; [MX-021](mx-021-payments-and-commerce.md) is inactive |
| Legal threat against good-faith reporters | **None.** The estate undertakes not to pursue a good-faith reporter |
| Publication of the report | **Yes**, in the defect register |

### 5.2 The estate does not ask for embargo

Most disclosure policies request a private window. This one does not, for a
reason specific to its situation: **the estate cannot commit to fixing anything on
a schedule.** One participant, no cover ([MX-006 §7](mx-006-contact-and-correspondence.md)).
Requesting an embargo the estate cannot repay with a timely fix asks a reporter to
hold a finding indefinitely for nothing.

A reporter is therefore free to publish immediately. The estate prefers to be
publicly embarrassed on a real finding than to hold a secret it cannot act on.

**The cost of this position:** a reader is exposed between disclosure and fix, and
that exposure is the estate's fault rather than the reporter's. The estate accepts
that ordering because the alternative — an embargo it cannot honour — shifts the
same risk onto the reader while also concealing it.

### 5.3 What the estate will do on a valid report

1. File it (always).
2. Classify it under [REG-07](../registries/reg-07-defect-classification-registry.md) —
   most security findings will be **DC-4 unenforced obligation** or **DC-2
   unoperable process**, with severity by reader effect.
3. If it touches governing text integrity, treat it as **S1** and enter
   [launch blockers](../00-governance-map/launch-blockers.md).
4. Publish the fix, or publish the reason there is none.

Step 4's second branch is the realistic one for several of §4's absences.

## 6. Worked instance

**T1 traced to the point where a reader is helpless.**

Suppose an attacker changes one number in [ML-2.3](../license/the-maher-license.md)
§F.4 — the 30-day cure period becomes 3 days — in the published site only.

Can a reader detect it?

| Method available to a reader | Works? |
|---|---|
| Compare against a published digest | **No** — none published |
| Compare against a signed release | **No** — no signing |
| Compare against an independent mirror | **No** — none exists |
| Compare against the repository | **Partially** — if the reader knows the repository and the attacker altered only the host |
| Notice the version stamp changed | **No** — an attacker would not change it |
| Notice internal inconsistency | **Sometimes** — the [enforceability table](../license/enforceability-two-track-table.md) also states the period, so a careful cross-reader might spot a mismatch |

The last row is the estate's only real integrity control, and it is **accidental**:
the corpus's heavy cross-referencing means a single altered fact contradicts its
restatements elsewhere. Redundancy is acting as a tamper-evidence mechanism that
nobody designed.

That is worth noticing, and it is not a substitute for a digest. The reasoning is
the same as
[ST-07](../standards/st-07-evidence-and-verify.md)'s: an accidental property
nobody tested is **E0**. A published digest per release would be **E3** and costs
almost nothing. The gap between those two is the whole of this instrument's
outstanding work.

## 7. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Integrity compromise undetectable by readers** | **Actual** — §6 |
| F2 | **Silent history rewrite** | **Unmitigated** — §3.3 |
| F3 | **Posture confused with review** — absence of attack surface read as evidence of security | Guarded by §1; the confusion is easy to make |
| F4 | **Out-of-model threat becomes in-model on a build** | Trigger is capability acquisition; **no watcher** |
| F5 | **Supply-chain asset unverified** | **Actual** — T3 |
| F6 | **No fix capacity** | **Actual** — §5.2 is built around it |
| F7 | **Transport assumed** | Unverified |

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** any published governing text differs from the recorded text — the
>   central test, and **currently unrunnable by a reader** for want of a digest;
> - **(b)** any request is made to a third-party domain the reader did not choose
>   (also [MX-003 §10(e)](mx-003-privacy-notice.md));
> - **(c)** a security report is shown to have been received and not filed;
> - **(d)** the estate is shown to have pursued a good-faith reporter;
> - **(e)** a security review is shown to have occurred — which would **improve**
>   the estate's position and falsify this page's central disclosure.
>
> That **(a) cannot currently be run** is the most important sentence in this
> instrument. The estate's own falsifier is blocked by the estate's own missing
> control.

## 9. Limits

1. **No security review by anyone.** Everything in §3 is reasoned.
2. **No published digests, no signing, no mirror** — so T1, T2 and T8 are
   undetectable from outside (§6, §8a).
3. **Single account, unpublished access practice** (T7). The estate does not state
   whether multi-factor authentication is in use, because stating it would be an
   unverifiable claim about a private configuration — and not stating it leaves
   T7 wholly unaddressed. Both options are unsatisfactory; the estate has chosen
   silence over an unverifiable assurance and records the choice here.
4. **Transport security assumed, not verified.**
5. **No fix capacity or schedule** (§5.2).
6. **No Arabic text**, while `prevailing_text: ar`.

## 10. Obligation

**On the estate:**
- Publish a content digest per release. This is the single cheapest act that would
  make §8(a) runnable, and it is owed.
- Confirm all assets are self-hosted, or disclose the third party at the point of
  use (T3).
- File every security report, agreed or not (§5.3).
- Never pursue a good-faith reporter (§5.1).
- Do not ask for an embargo the estate cannot repay with a fix (§5.2).
- Re-run the threat model on **capability acquisition**, not at the interval (§3.2).
- Treat integrity of governing text as S1 (§5.3).

**On a reporter:**
- Report by any channel in [MX-006](mx-006-contact-and-correspondence.md);
  anonymity is fine.
- Publish when you choose; no embargo is requested (§5.2).

---

### Related

**Platform and data** — [ST-22](../standards/st-22-platform-and-persistence.md) ·
[MX-024](mx-024-infrastructure-and-migration.md) ·
[REG-06](../registries/reg-06-dataset-registry.md) ·
[MX-003](mx-003-privacy-notice.md)

**Integrity of the record** — [MX-000 Charter](mx-000-charter.md) ·
[MX-013](mx-013-records-and-versioning.md) ·
[GM-12 archive register](../00-governance-map/archive-register.md) ·
[changelog](../00-governance-map/changelog.md)

**Reporting** — [MX-006](mx-006-contact-and-correspondence.md) ·
[defect register](../00-governance-map/defect-register.md) ·
[REG-07](../registries/reg-07-defect-classification-registry.md) ·
[launch blockers](../00-governance-map/launch-blockers.md)

**Absent controls** — [ST-13](../standards/st-13-static-build-and-sentinel.md) ·
[REG-04](../registries/reg-04-media-registry.md) ·
[GM-08 verification log](../00-governance-map/verification-log.md) ·
[REG-08](../registries/reg-08-role-and-authority-registry.md)

### Exit pair

1. **Demand the digest.** Until a per-release content digest exists, no reader can
   verify that the licence they are reading is the licence the estate wrote.
2. **Read the unmitigated one.** [§3.3](#33-t8-deserves-its-own-paragraph) — the
   no-silent-edits rule rests on an unwitnessed history.

<!-- mx-pagestamp: MX-011 · v2026.10.1 · governing · tier 3 · reviewed 2026-09-16 · next review 2027-03-16 -->
<!-- mx-demo: the live site is a demonstration; no security review has been performed -->
