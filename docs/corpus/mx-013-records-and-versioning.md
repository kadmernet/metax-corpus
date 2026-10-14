---
doc_id: "MX-013"
title_en: "Records, Versioning and Corrections"
title_ar: "السجلات والإصدارات والتصحيحات"
family: "corpus"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 3
depth: 5
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["corpus", "records", "versioning", "corrections", "permanence"]
route: "/library/record/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# MX-013 · Records, Versioning and Corrections

**What this instrument governs.** How the estate keeps its own history: what is versioned, what is
retained, what may never be deleted, and who is forbidden from deleting it.

**The rule it exists to make operative.** [MX-000 §0.8](mx-000-charter.md) forbids silent edits and
[§0.5.2](mx-000-charter.md#2-the-correction-obligation) places the correction obligation **beyond
the Curator**. MX-013 is the machinery: which register receives what, in which form, and with what
permanence.

---

## 1. Position

An institution's record of itself is the only thing that makes its other claims checkable. A
falsifier is worthless if the claim it attaches to can be quietly rewritten. A decay interval is
worthless if `last_reviewed` can be backdated. A defect register is worthless if entries can be
removed once resolved.

So this instrument sits beneath the whole epistemic apparatus —
[ST-04](../standards/st-04-falsifiability-and-claim-cards.md),
[ST-05](../standards/st-05-decay-and-review-intervals.md),
[ST-07](../standards/st-07-evidence-and-verify.md) — and supplies the property each of them
assumes: **that the past state of a claim remains retrievable.**

Published at `/library/record/`, the group hub whose five leaves are the estate's registers.

**The macro register.** Under **HX‑12** (harm to the record) and **HX‑25** (silence in the
record), the characteristic failure of a modern institution is not falsification but **quiet
revision** — text improved, the improvement obviously better, the previous version deleted because
nobody can imagine needing it. The result is an institution that appears always to have been
correct, which a successor inherits as **HX‑20**: a body of knowledge whose errors are invisible
and whose judgement therefore cannot be assessed. This instrument's whole content is the refusal of
that convenience.

---

## 2. Definition — the six registers and what each receives

| Register | Receives | Authority |
|---|---|---|
| [Changelog](../00-governance-map/changelog.md) | Releases, **with reasons** | record |
| [Corrections Log](../00-governance-map/corrections-log.md) | Claims found **wrong** | record |
| [Defect Register](../00-governance-map/defect-register.md) | Known shortfalls, with owners and dates | record |
| [Verification Log](../00-governance-map/verification-log.md) | `[VERIFY]` claims and **their age** | record |
| [Archive Register](../00-governance-map/archive-register.md) | Superseded text | record |
| [Version History](../license/version-history.md) | Licence versions and reasons | record |

**All six are `authority: record` and govern nothing.** Under
[GM-01 §1.2](../00-governance-map/precedence-and-conflict-rules.md) they sit **outside the
precedence ladder**, and the exclusion protects them: a record cannot create an obligation, and
equally **cannot be overridden**, because it makes no normative claim to override. No instrument at
any tier can make the Corrections Log stop having recorded that the estate was wrong.

### 2.1 Routing a change to the right register

The distinctions are routinely confused, and the wrong routing loses information.

| The situation | Register | Because |
|---|---|---|
| A claim was **wrong** | Corrections Log | It records errors, only errors |
| A shortfall is **known and published** | Defect Register | Not an error — a gap with an owner |
| A claim is **unchecked** | Verification Log | Not known wrong; not yet known |
| Text **no longer governs** | Archive Register | What it *used to say* |
| A decision **needs the Curator** | Open Questions | Needs a choice, not a check |
| A release **happened** | Changelog | With reasons, not diffs |

**The sharpest pair is Corrections and Verification.** A correction records *we said X and X is
false*. A `[VERIFY]` tag records *we say X and have not checked*. Routing an unchecked claim to
corrections asserts an error nobody has established; routing a known error to verification hides
it in a queue.

---

## 3. Mechanism — the four permanence rules

**Rule 1 — A correction adds a record; it never replaces one.** Where an instrument was wrong, the
wrong text stays retrievable with a non-governing banner and the correction points at it.

**Rule 2 — A published defect cannot be removed by the Curator.** [§0.5.2](mx-000-charter.md#2-the-correction-obligation).
Closed defects are **never deleted**: a register that removes resolved entries cannot be audited
for **how long a defect stayed open**, which is the only number revealing whether the correction
obligation is real.

**Rule 3 — Rejected corrections are published with reasons.** This is what stops the correction
queue becoming a black box, and it applies to machine-filed corrections identically
([GM-11 §3.2](../00-governance-map/machine-reading-contract.md)).

**Rule 4 — Superseded text is retained, and prefer retaining *in place*.** Moving a superseded
licence version into an archive directory **breaks every citation of it**. ML-2.1 and DS-01's
superseded sections are therefore retained where they are, with non-governing banners; the
[Archive Register](../00-governance-map/archive-register.md) records *that* they are superseded
rather than necessarily holding the bytes.

### 3.1 Versioning

Instruments version as `v{YYYY}.{MM}.{n}`. A version increments when **substance** changes; an
editorial fix does not increment it. The test, from
[Archive Register §2.1](../00-governance-map/archive-register.md): *would a party's conduct have
been assessed differently under the old text?* If no, it is editorial.

**Identifiers never version.** [ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md):
numbers are immortal from first assignment. `MX-013` is this instrument at every version it will
ever have.

---

## 4. Worked instance — one error, three registers, three treatments

The estate misspelt its own subject: **MacroLifeTach** for **MacroLifeTech**, propagated through
forty-six ledger entries, four instruments, and a published anchor slug.

**To the Corrections Log** → [C-13](../00-governance-map/corrections-log.md#c-13). What was
claimed, what is correct, how it was found — **by the Curator**, because no consistency check can
catch a name that is wrong everywhere. Rule 1: the entry *adds* a record.

**To the Defect Register** → [DEF-023](../00-governance-map/defect-register.md#def-023), open,
because the misspelling survives in the live build, `data.js`, the meta description and the search
index. The prose is fixed; the artefact is not.

**To the Archive Register** → **nothing.** A name spelt wrongly was never a different substantive
claim, so there is no superseded *text* to retain
([Archive Register §2.1](../00-governance-map/archive-register.md)).

**And the anchor was kept.** `#r-42--the-third-pillar-is-macrolifetach-not-bcia` remains beside the
corrected one. Deleting a published address to conceal a spelling error trades a cosmetic defect
for a **broken citation** — and under
[ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md) an anchor, once published, is an
identifier.

**What the instance demonstrates.** One error, four different correct treatments, and the
distinctions are not bureaucratic: each register answers a different question a future reader will
ask. Collapsing them into one "changes" file would lose the *how it was found*, the *still broken
in the build*, and the *deliberately retained anchor*.

---

## 5. Failure modes

**The improvement that erases.** Always innocent, always the same shape. Detected only by an
auditor who wanted the old words.

**Backdated review dates.** `last_reviewed` set to the write date without a review. Undetectable
from the front matter and it corrupts every staleness computation
([ST-05 §6](../standards/st-05-decay-and-review-intervals.md)).

**Closed defects pruned for readability.** Rule 2. It destroys the one metric that reveals whether
corrections actually happen.

**Retroactive archiving to tidy a contradiction.** Moving an inconvenient text to the archive with
no corrections entry — the register becoming the mechanism of the concealment it was built to
prevent. Every archive row must trace to a changelog release and, where the text was *wrong*, to a
corrections entry.

**The register that predates nothing.** [DEF-029](../00-governance-map/defect-register.md#def-029):
§0.8 was cited as authority for two releases before the Archive Register existed, so **two
superseded texts are already unretrievable** — MX‑NAV‑SPEC v2026.09.4 and the fourteen subdomain
page-spec rows. A rule cited as operative is not the same as a rule operating, and the gap is
invisible from inside the citation.

---

## 6. Limits

**Class: technical.** Nothing enforces any of this. No mechanism detects a deleted defect row, a
backdated review or a silently rewritten section. The content-integrity check would live in
[SENTINEL](../standards/st-13-static-build-and-sentinel.md)
([DEF-001](../00-governance-map/defect-register.md#def-001)). **The estate's record-keeping is
currently protected by intention alone.**

**Class: custodial, and it is the serious one.** The only custodian of this estate's record is the
estate, in one repository, on one provider.
[ML-2.3 §E.7](../license/ml-2-3.md) requires three independent mirrors, one content-addressed and
one outside the steward's control; **none exists**
([B-02](../00-governance-map/launch-blockers.md)). So the instrument forbidding the Curator from
deleting a record is enforced against a Curator who holds the only copy.

**Class: epistemic.** Archive coverage begins 2026‑10‑01 (§5). Everything superseded before that is
retained only where it happened to survive.

**Class: governance.** Rule 3 — rejected corrections published with reasons — has **never been
exercised**, because nothing is published and no external correction has been received.

---

## 7. Falsifier

1. **A superseded text that cannot be retrieved and appears in no archive row.** Expected for
   pre-October supersessions; a valid correction in every case after.
2. **A closed defect absent from the register**, falsifying Rule 2 in practice.
3. **A correction that replaced rather than added**, falsifying Rule 1.
4. **The four rules proving to cost more than they return** — if permanence makes the corpus so
   cluttered that readers cannot find current text. Watch the accumulation of anchor aliases and
   retained banners; the estate asserts this trade and has not tested it.
5. **Rule 3 never exercised after publication.** If no rejected correction is ever published, either
   none was rejected or the rule is decorative — and the estate should be able to say which.

---

## 8. Obligation

**For any editor:** route the change to the right register (§2.1) **in the same edit** as the
change. Add, never replace. Retain in place, never move. Increment the version only when substance
changed.

**For the Curator:** you cannot decline a valid correction, delete a published defect, or remove a
superseded claim. That is [§0.5.2](mx-000-charter.md#2-the-correction-obligation) and it is beyond
you by design.

**For the estate:** build the §E.7 mirrors. Until they exist, every permanence rule here is
enforced by the party the rules constrain, and §6's custodial limit is the largest unaddressed
weakness in the estate's record-keeping.

**For a reader:** if a claim you cite changes and you cannot find what it said before, that is a
defect and it is one this instrument exists to prevent. File at
`/library/record/corrections-log/`.

**Under ML-2.3:** §H.12 (harm to the record), §H.25 (silence in the record), §H.19 (authorship of
record), §H.20 (inheritance of unauditable systems), §H.26 (corpus hygiene), §H.27
(reversibility), §H.28 (custody and horizon), §E.5 (narrowing on falsification — recorded in
Archive Register Class D, currently **empty**), §E.7 (registry redundancy).

---

**Related:** [MX-000 §0.8](mx-000-charter.md) ·
[Corrections Log](../00-governance-map/corrections-log.md) ·
[Defect Register](../00-governance-map/defect-register.md) ·
[Archive Register](../00-governance-map/archive-register.md) ·
[Verification Log](../00-governance-map/verification-log.md) ·
[Changelog](../00-governance-map/changelog.md) ·
[SITE-03 Routing Law §6](../site/routing-law.md) ·
[ST-01 Identifier Grammar](../standards/st-01-identifier-and-url-grammar.md)

*Curated by Maher. Six registers, four permanence rules, one error routed four different ways —
and the only custodian of the whole record is the party the rules are written to constrain.*
