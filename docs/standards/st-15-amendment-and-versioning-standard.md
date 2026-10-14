---
doc_id: ST-15
title_en: Amendment and Versioning Standard
title_ar: معيار التعديل والإصدارات
family: standards
version: v2026.10.1
status: published
authority: operative-form
prevailing_text: ar
audience_tier: 3
depth: meta
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [amendment, versioning, supersession, records, standards]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. The standard's own central requirement — retrievable superseded text — is already breached and unrecoverable for ML-2.2.
route: /standards/st-15/
---

# ST-15 — Amendment and Versioning Standard

> **Authority.** `operative-form`, tier 5. Governs **how an instrument changes**.
> The duty to record is [MX-013](../corpus/mx-013-records-and-versioning.md); the
> prohibition on silent edits is [Charter §0.8](../corpus/mx-000-charter.md);
> retention is [GM-12](../00-governance-map/archive-register.md); identifiers are
> immortal per [ST-01 Rule 2](st-01-identifier-and-url-grammar.md).

> **Disclosure first.** The estate has already lost a superseded governing text:
> **ML-2.2 is absent and declared unrecoverable**
> ([version history](../license/version-history.md)), a gap classified
> `declared-permanent` rather than `open` because no remedy exists. This standard
> is therefore written by an estate that has already committed the worst breach the
> standard prohibits, and it says so at the top rather than in a limits section.

---

## 1. Position

The user instruction that governs this whole corpus is: **latest document details,
not new documents with versions.** That is a versioning policy, and it has a
precise meaning worth stating in a standard:

> An instrument is **refreshed at its permanent path**. A new version does not get
> a new address. There is no `-v2`, no `-rev2`, no `/terms-2026/`.

This single rule produces most of §3, and it has a cost that must be paid
explicitly: **if the current version occupies the only address, the previous
version must be retrievable somewhere else, or it is gone.** That cost is where
the estate has already failed.

### 1.1 Two things versioning must do at once

| Duty | Serves | Mechanism |
|---|---|---|
| **A single current address** | The reader who wants what applies now | Permanent path, version in front matter |
| **Retrievable history** | The reader who relied on an earlier version | Archive + changelog + supersession fields |

Duty A is easy and the estate does it. Duty B is laborious, invisible, and the one
that decays. A corpus that does A without B looks tidier and quietly strands
everyone who acted on last year's text.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **amendment** | Any change to a published instrument |
| **substantive amendment** | One that changes what a reader may, must, or must not do |
| **editorial amendment** | One that does not — spelling, formatting, link repair |
| **supersession** | Replacement of an instrument by a different instrument |
| **re-version** | Replacement of a version by a later version **at the same path** |
| **superseded governing text** | The text that governed before; conditional front matter field per [ST-02](st-02-front-matter-schema.md) |

### 2.1 Version string form

`vYYYY.MM.P` — year, month, patch within month. So `v2026.10.1`.

Three consequences:

1. Versions are **dated**, so staleness is visible without consulting a register.
2. Two amendments in one month are distinguished by patch, not by day, so the
   string does not imply more precision than the record holds.
3. **The version string is not semantic.** It does not encode whether the change
   was substantive. That is recorded separately (§3), because a reader must not
   have to infer significance from a number.

### 2.2 Re-version is not supersession

| | Re-version | Supersession |
|---|---|---|
| Path | Unchanged | New instrument, new path |
| Identifier | Unchanged — immortal | New identifier; old one retired, never reused |
| Front matter | `version` updated | `supersedes` on the new, `superseded_governing_text` on the old |
| Old text's status | Archived | `status: superseded`, retained in place |

Confusing the two is how history is lost. A re-version that *should* have been a
supersession overwrites a text that a reader may still be bound by; a supersession
that *should* have been a re-version fragments one instrument across two
addresses, defeating §1.

## 3. The seven rules

| # | Rule | Rationale |
|---|---|---|
| **A1** | Amend **at the permanent path**. No version-suffixed paths | §1; [ST-01 Rule 2](st-01-identifier-and-url-grammar.md) |
| **A2** | **Classify** every amendment as substantive or editorial, in the record | A reader must not infer it from a version string (§2.1) |
| **A3** | **Archive the superseded text before** publishing the new one | The only protection of duty B (§1.1) |
| **A4** | Log **every** amendment in the [changelog](../00-governance-map/changelog.md); log substantive ones additionally in the [corrections log](../00-governance-map/corrections-log.md) | [Charter §0.8](../corpus/mx-000-charter.md) |
| **A5** | State **what changed and why**, not that something changed | "Updated" is not a record |
| **A6** | Where an instrument is incorporated by another, **check the incorporating text** before amending | [ML-2.3 §A.10](../license/the-maher-license.md) incorporates HX-000 — amending HX-000 changes the licence |
| **A7** | **Never** amend to remove a disclosed defect without a corrections entry explaining the removal | Otherwise the defect register shrinks silently |

### 3.1 A3 is the rule that has failed

Archive-before-publish is the whole of duty B. Its failure mode is silent: the new
text publishes fine, and the loss is discovered only when someone wants the old
one.

Current state per [GM-12](../00-governance-map/archive-register.md):

| Class | Contents | State |
|---|---|---|
| A | Current texts | Held |
| B | Superseded texts | **Two unretrievable** ([DEF-029](../00-governance-map/defect-register.md)); ML-2.2 **permanently lost** |
| C | Records and ledgers | Held |
| D | Withdrawn duties | **Empty** — suspicious ([REG-07 §3.2](../registries/reg-07-defect-classification-registry.md)) |

So A3 has a known failure rate greater than zero in a corpus with very few
supersessions. That is a poor record on a small sample.

### 3.2 A6 and incorporation by reference

[ML-2.3 §A.10](../license/the-maher-license.md) incorporates
[HX-000](../harms/hx-000-the-fourteen-structural-harms.md), placing it at **tier
1a** above the Charter. Therefore:

> **Amending HX-000 amends the licence's operative content without amending the
> licence's text.**

This is the most consequential versioning hazard in the corpus and it has no
guard. The pending re-version of HX-000 from fourteen harms to twenty-five is
exactly such an amendment: it will change what Tier 1 governs, while
[ML-2.3](../license/the-maher-license.md)'s own version string stays at 2.3.

A6 therefore requires that an amendment to an incorporated document record, in
**both** documents, that the incorporating instrument's operative content changed.
Nothing enforces this.

### 3.3 A7 and the shrinking register

A defect register that only grows is credible. One that shrinks without
explanation is not distinguishable from one being tidied. A7 requires that any
removal — a defect closed, re-characterised, or withdrawn — carries a corrections
entry stating which and why. The estate's register currently records
[DEF-2026-042 closed and -041 re-characterised](../00-governance-map/defect-register.md)
with entries, which is A7 operating correctly.

## 4. Mechanism

### 4.1 Amendment sequence

```
1. classify: substantive or editorial              (A2)
2. check incorporation: who incorporates this?     (A6)
3. ARCHIVE the current text                        (A3)  ← the step that fails
4. publish the new text at the same path           (A1)
5. update `version`, `last_reviewed`               (ST-02)
6. if supersession: set `supersedes` /
   `superseded_governing_text`                     (§2.2)
7. changelog entry: what and why                   (A4, A5)
8. if substantive: corrections log entry           (A4)
9. if it removes a disclosed defect: explain       (A7)
```

Step 3 is placed before step 4 deliberately. Archiving after publication is the
same as not archiving, because the text to archive is already gone.

### 4.2 What "latest details, not new versions" forbids

| Forbidden | Why |
|---|---|
| `mx-002-terms-of-service-v2.md` | Two addresses for one instrument; A1 |
| `/terms/2026/` | Same |
| A "current" page redirecting to a dated page | Reader cannot cite a stable address |
| Keeping both live with no `status` | Reader cannot tell which governs |
| Deleting the old text | A3; duty B |

### 4.3 The check

| # | Check | Detects | Status |
|---|---|---|---|
| **V1** | Every `version` change has a changelog entry | A4 breach | Specified; **not implemented** |
| **V2** | Every substantive change has a corrections entry | A4 breach | Specified; **not implemented** |
| **V3** | Every superseded text is retrievable in [GM-12](../00-governance-map/archive-register.md) Class B | **A3 breach** | Specified; **not implemented** |
| **V4** | Every amendment to an incorporated document is recorded in the incorporating one | A6 breach | Specified; **not implemented** |

Four checks, none implemented ([DEF-001](../00-governance-map/defect-register.md)).
**V3 is the one that would have caught the ML-2.2 loss** at the moment it
occurred, when recovery was still possible.

## 5. Worked instance

**The pending HX-000 re-version, traced before it happens.**

[HX-000](../harms/hx-000-the-fourteen-structural-harms.md) currently exists as a
draft: titled "The Fourteen Structural Harms", complete through H1–H11, ending at
an append-point, with obligation blocks linking `../license/ml-2-2.md` — a
**nonexistent** file. [ML-2.3](../license/the-maher-license.md) governs
**twenty-five** harms in six strata and incorporates HX-000 by §A.10.

Run §4.1 in advance:

| Step | What it requires here |
|---|---|
| 1. Classify | **Substantive.** Fourteen harms become twenty-five; this changes what the licence governs |
| 2. Incorporation check (A6) | **ML-2.3 incorporates it.** So this amendment changes Tier 1's operative content. Both documents must record that |
| 3. Archive (A3) | **The fourteen-harm draft must be archived first.** It is the text that has stood while the licence pointed at it |
| 4. Publish at same path | Here a judgement is forced — see below |
| 5. Version / reviewed | `v2026.10.1` |
| 6. Supersession fields | Not a supersession: same instrument, same identifier. `HX-000` is immortal |
| 7–8. Logs | Changelog + corrections, stating fourteen → twenty-five and why |
| 9. Defect removal (A7) | Closes [DEF-021](../00-governance-map/defect-register.md); the corrections entry must say so |

**The judgement at step 4.** The existing file is at
`hx-000-the-fourteen-structural-harms.md`. The path **names a claim that will
become false** — fourteen. Under A1 the amendment belongs at the permanent path;
under [ST-01 Rule 2](st-01-identifier-and-url-grammar.md) the *identifier* `HX-000`
is immortal but a *path* is not an identifier; under
[SITE-03](../site/routing-law.md) a path change requires an append-only redirect.

So the correct handling is: **publish at a new path (`hx-000-structural-harms.md`),
record a redirect from the old path, and keep the identifier.** That is not a
breach of A1 — A1 forbids version-suffixed paths, not the correction of a path
whose wording states a superseded fact.

**What this instance exposes.** A1 as drafted does not distinguish *version
suffixing* (forbidden) from *path correction* (sometimes required). Writing the
worked instance surfaced the ambiguity, and the estate's choice is to state the
distinction here rather than leave the next author to guess:

> **A1, clarified.** A path may change only to remove a statement of fact that has
> become false, never to encode a version. Every such change requires an
> append-only redirect and a changelog entry.

That clarification is itself a substantive amendment to this standard, made in the
same act as its first publication, and it is logged as such.

## 6. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Superseded text lost** | **Actual** — ML-2.2 permanent; two more in Class B (§3.1) |
| F2 | **Amendment unclassified** | A2 relies on the author; unaudited |
| F3 | **"Updated" as a record** | Prohibited by A5; the commonest temptation |
| F4 | **Incorporated document amended silently** | **Live** — the HX-000 re-version (§5); no guard |
| F5 | **Defect register shrinks silently** | Guarded by A7; currently honoured |
| F6 | **Version-suffixed path** | Forbidden by A1; not observed |
| F7 | **Path frozen with a false name** | **Actual** — "fourteen" in a twenty-five-harm corpus (§5) |
| F8 | **Archive-after-publish** | The way A3 fails; step ordering in §4.1 is the only guard |

## 7. Limits

1. **A3 has already failed irrecoverably** for ML-2.2 and twice more in Class B.
   The standard cannot repair what is gone; `declared-permanent` is the honest
   disposition ([REG-07 §2.3](../registries/reg-07-defect-classification-registry.md)).
2. **All four checks are unimplemented** (§4.3). V3 would have prevented §7.1.
3. **A6 has no enforcement**, and the single most consequential amendment in the
   corpus's future is an A6 case (§5).
4. **Class D is empty** (§3.1), which on this estate's history is more likely an
   omission than a fact.
5. **The A1 clarification in §5 was discovered while writing**, meaning the rule
   set was incomplete at first draft and may still be.
6. **No Arabic text**, while `prevailing_text: ar` — so the authoritative version
   of the versioning standard does not exist, and cannot be compared against for
   drift.

## 8. Falsifier

> **IF FALSE.** This standard is falsified if:
>
> - **(a)** a superseded governing text is unretrievable — **fires now**, three
>   times (§3.1);
> - **(b)** a `version` change appears with no changelog entry;
> - **(c)** a substantive change appears with no corrections entry;
> - **(d)** an incorporated document is amended without the incorporating
>   instrument recording it (A6);
> - **(e)** a version-suffixed path exists anywhere in the corpus (A1);
> - **(f)** a disclosed defect vanishes from the register with no explanation (A7).
>
> **(a) fires immediately and permanently.** The estate publishes a standard whose
> primary falsifier is already satisfied, because the alternative — narrowing the
> rule until the existing loss no longer breaches it — would make the standard
> agree with the estate's conduct instead of judging it.
>
> **(b), (c), (e) and (f) are reader-runnable** against the published changelog and
> registers, with no tools and no access.

## 9. Obligation

**On an author:**
- Amend at the permanent path; never version-suffix (A1, §5 clarified).
- **Archive before publishing** (A3, §4.1 step 3).
- Classify every amendment (A2) and state **what and why** (A5).
- Check who incorporates the document before amending it (A6).
- Log every amendment; substantive ones twice (A4).
- Explain any removal from the defect register (A7).

**On the estate:**
- Implement **V3** first; it is the check whose absence caused the permanent loss
  (§4.3, [ST-13](st-13-static-build-and-sentinel.md)).
- On the HX-000 re-version: archive the fourteen-harm draft, record the redirect,
  and note in **both** HX-000 and ML-2.3 that Tier 1's operative content changed
  (§5).
- Populate [GM-12](../00-governance-map/archive-register.md) Class D rather than
  leaving it empty (§3.1).
- Keep `declared-permanent` on ML-2.2; do not reconstruct a lost governing text and
  present it as the original ([REG-07 §3.2](../registries/reg-07-defect-classification-registry.md)).

---

### Related

**Records and permanence** — [MX-013](../corpus/mx-013-records-and-versioning.md) ·
[GM-12 archive register](../00-governance-map/archive-register.md) ·
[MX-000 Charter](../corpus/mx-000-charter.md) ·
[changelog](../00-governance-map/changelog.md)

**Identifiers and paths** — [ST-01](st-01-identifier-and-url-grammar.md) ·
[SITE-03](../site/routing-law.md) · [ST-02](st-02-front-matter-schema.md) ·
[ST-08](st-08-cross-reference-and-link-integrity.md)

**The incorporation hazard** — [ML-2.3](../license/the-maher-license.md) ·
[HX-000 draft](../harms/hx-000-the-fourteen-structural-harms.md) ·
[version history](../license/version-history.md) ·
[precedence](../00-governance-map/precedence-and-conflict-rules.md)

**What failed** — [DEF-021](../00-governance-map/defect-register.md) ·
[DEF-029](../00-governance-map/defect-register.md) ·
[REG-07](../registries/reg-07-defect-classification-registry.md) ·
[MX-019](../corpus/mx-019-sunset-and-wind-down.md)

### Exit pair

1. **Run the cheap checks.** Falsifiers §8(b), (c), (e), (f) need only the
   published [changelog](../00-governance-map/changelog.md) and registers.
2. **Read the loss this standard could not prevent.**
   [version history](../license/version-history.md) — ML-2.2 is gone and the gap is
   declared, not reconstructed.

<!-- mx-pagestamp: ST-15 · v2026.10.1 · operative-form · tier 5 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; none of this standard's four checks is implemented -->
