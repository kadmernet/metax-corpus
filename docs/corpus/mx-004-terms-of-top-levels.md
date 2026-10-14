---
doc_id: MX-004
title_en: Terms of the Top Levels
title_ar: شروط المستويات العليا
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
domain_tags: [pillars, top-levels, scope, architecture, naming]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. Of the nine top levels, several hold no written leaf pages.
provenance_of_purpose: The nine pillars were named before their scopes were defined; this instrument defines them retrospectively, which is recorded as a weakness in §11.
route: /terms-of-top-levels/
---

# MX-004 — Terms of the Top Levels

> **Authority.** `governing`, tier 3. Defines the **scope and boundary** of each of
> the nine top-level pillars. Addresses for those pillars are in
> [SITE-01](../site/route-manifest.md) (tier 7); page form is
> [ST-24](../standards/st-24-page-prose-standard.md) (tier 5). Where a pillar's
> *content* and its *route* disagree, this instrument and ST-24 prevail over the
> manifest — the ordering trap restated.

> **Disclosure first.** The nine pillars were **named before their scopes were
> written.** This instrument supplies the scopes retrospectively, which means it
> is fitted to names already chosen rather than names chosen to fit a scheme. Two
> pillars have **zero written leaf pages**. See [Annex A](#annex-a--pillar-census)
> for the count before reading any claim about coverage.

---

## 1. Position

Nine top levels partition the estate. A partition does three things, and this
instrument must do all three or the partition is decorative:

1. **Assign** — every document belongs to exactly one pillar.
2. **Exclude** — each pillar states what it does *not* cover, so a reader can rule
   it out quickly.
3. **Resolve** — where two pillars could claim a document, a stated tie-break
   decides.

Partitions usually fail at (2) and (3). A set of nine attractive names with no
exclusions produces an estate where everything is arguably everywhere, and a
reader's only navigation strategy becomes search — which defeats the point of
having a structure at all.

## 2. Definition

A **top level** (pillar) is a named division of the estate with **six** recorded
properties:

1. **Scope** — the subject matter it covers, positively stated.
2. **Exclusions** — at least two things a reader might expect and will not find.
3. **Group hubs** — the intermediate pages beneath it (45 across the estate).
4. **Leaf classes** — the kinds of terminal page it contains (266 leaves total).
5. **Tie-break rule** — what wins when another pillar could also claim a page.
6. **Census** — written pages versus planned routes.

Property 2 is mandatory and is the one that gives a pillar an edge. A pillar with
no exclusions has no boundary, and a division without a boundary is a label.

### 2.1 The assignment rule

Every document has **exactly one** pillar. Not zero, not two. Cross-cutting
subjects are handled by **cross-reference**, never by dual assignment — because a
document with two homes has two review schedules, two group hubs claiming it, and
two chances to be forgotten.

### 2.2 The tie-break hierarchy

Where two pillars could claim a document, apply in order:

1. **Authority beats subject.** A `governing` instrument goes to the pillar that
   governs its *authority*, not its topic. So a licence provision about payments
   lives under the licence pillar, not the commerce pillar.
2. **Duty beats description.** If the document imposes a duty, it belongs where the
   duty is enforced.
3. **Record beats both.** A `record` goes to the records pillar regardless of
   subject — this is why every `REG-` document is filed together rather than
   dispersed to the topics it registers.
4. **Curator's choice, logged.** If 1–3 do not resolve it, the curator chooses and
   records the choice in the
   [reconciliation ledger](../00-governance-map/reconciliation-ledger.md).

Rule 3 is the most consequential. It is why
[REG-05 credential registry](../registries/reg-05-credential-registry.md) is not
filed under the learning pillar despite being entirely about assessment.

## 3. The nine top levels

| # | Pillar | Scope | Two exclusions | Tie-break note |
|---|---|---|---|---|
| 1 | **Licence** | ML-2.3, its schedules, companions, version history, enforceability analysis | Not: reuse *advice*; not: terms of service | Wins over every other pillar by rule 1 |
| 2 | **Harms** | The 25 structural harms, strata I–VI, audit rubric, instrument map | Not: moderation of content; not: user complaints | Tier 1a; wins over all but licence |
| 3 | **Corpus** | Charter, governing `MX-` instruments, scope, user-facing terms and notices | Not: standards of form; not: records | Loses to standards on questions of form |
| 4 | **Agents** | Agent constitution, powers, prohibitions, refusal and escalation records | Not: AI disclosure to readers (that is MX-007, corpus) | Duty-bearing pillar, rule 2 |
| 5 | **Standards** | Form, grammar, front matter, evidence, accessibility, build, prose recipe | Not: what to say; only how to say it | Beats corpus on form (rule 2) |
| 6 | **Rubrics** | Assessment dimensions, proof ladder, review gates | Not: issued credentials (record, rule 3) | — |
| 7 | **Design** | Tokens, geometry, typography, navigation behaviour | Not: route addresses; not: page prose | Loses to SITE on addressing |
| 8 | **Records** | Registries, ledgers, logs, indexes, verification, archive | Not: anything `governing` | **Wins by rule 3** on subject collisions |
| 9 | **Site** | Route manifest, page contract, routing law, demo notice | Not: page content standards (ST-24, standards pillar) | Tier 7, lowest of the governing layers |

### 3.1 Why exactly nine

No principled reason. Nine is the number that existed when the names were fixed,
and this instrument was written against it. A reader who suspects the partition
would be cleaner at seven or eleven is probably right, and the estate's answer is
not a defence of nine but an application of
[ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md): the pillar
routes are published, the numbers are spent, and reorganising would break
addresses that must remain resolvable
([SITE-03](../site/routing-law.md)).

This is a real cost of the immortality doctrine, and it is worth naming: **the
doctrine that protects readers from dead links also freezes early mistakes.** The
estate accepts the freeze and records the reasoning here rather than presenting
nine as elegant.

## 4. Mechanism

### 4.1 The three-level shape

```
pillar (9)         →  group hub (45)         →  leaf (266)
  scope stated        subject cluster            one topic, one address
  no leaf content     no leaf content            the reader's destination
```

- A **pillar page** states scope, exclusions, and hubs. It carries no substantive
  content, because content at pillar level cannot be found again.
- A **group hub** clusters leaves and states what the cluster is for. It is
  navigational.
- A **leaf** is the reader's destination and bears the full weight of
  [ST-24](../standards/st-24-page-prose-standard.md)'s eight parts and
  [SITE-02](../site/page-contract.md)'s twenty acceptance criteria.

Total: **321 English routes** — 9 + 45 + 266 + parametric families. Enumerated in
[SITE-01](../site/route-manifest.md).

### 4.2 Thin-by-nature exemptions

Pillar pages and group hubs are **structurally short**. They fall within the
nav spec's six thin-by-nature exemptions and are not subject to the 1200-word
floor. Leaves are.

The estate's own weakness here: [REG-02 §6 F5](../registries/reg-02-page-registry.md)
records that **no field names which exemption a page relies on**. A pillar page is
obviously exempt; an ambiguous leaf claiming exemption is not checkable. Filed at
**RAT-24**.

### 4.3 Adding or removing a pillar

- **Adding** requires: a scope, two exclusions, a tie-break note, and a changelog
  entry. A new pillar takes the next number; it does not renumber existing ones.
- **Removing** is prohibited. A pillar's route must remain resolvable forever
  ([SITE-03](../site/routing-law.md)). A pillar whose content moves elsewhere
  becomes a redirect with an append-only record, and its number is never reused.

## 5. Worked instance

**Assigning one document that three pillars want:
[REG-05 credential registry](../registries/reg-05-credential-registry.md).**

The candidates:

| Claim | Argument |
|---|---|
| **Rubrics (6)** | It is entirely about D1–D5 scores and proof levels. Its content is assessment |
| **Corpus (3)** | It states obligations about what may be certified, which reads as governing |
| **Records (8)** | It is `authority: record` |

Apply §2.2 in order:

1. *Authority beats subject* — REG-05's authority is `record`. Its subject is
   assessment. **Authority wins**, so not Rubrics.
2. *Duty beats description* — does REG-05 impose a duty? It appears to: "do not
   issue while stage 2 is vacant." But inspect its own §9: **"No obligation arises
   from a record."** The duty is [MX-016](mx-016-appeals-and-due-process.md)'s,
   restated for navigation. So not Corpus.
3. *Record beats both* — **Records pillar.** Decided.

Now the instructive part: the answer is *counter-intuitive and correct*. A reader
looking for credential rules will look under learning or assessment and will not
find them, because what lives under Records is the **list of issued credentials**
(empty), while the **rules** live in [RB-01](../rubrics/rb-01-d1-d5-rubric.md),
[RB-02](../rubrics/rb-02-proof-ladder.md), and MX-016 across three other pillars.

That is a genuine navigational cost of a clean partition. The mitigation is
[SITE-02](../site/page-contract.md)'s related-block requirement — four groups,
eight links minimum — which exists precisely so that a correctly-but-unintuitively
filed document is still reachable from where a reader starts. The partition is
kept rigorous and the **navigation** is made redundant, rather than the partition
being fudged to match intuition.

## 6. Failure modes

| # | Failure | Mechanism | Current state |
|---|---|---|---|
| F1 | **Dual assignment** | A cross-cutting document filed twice | Prohibited by §2.1; not observed |
| F2 | **Empty pillar** | A pillar with named hubs and no leaves | **Occurring ×2** — see Annex A |
| F3 | **Content at pillar level** | Substantive prose on a navigation page | Prevented by §4.1; unaudited |
| F4 | **Unrecorded tie-break** | Rule 4 used without a ledger entry | Possible; one classifier |
| F5 | **Exemption without name** | Thin leaf claiming exemption unspecifically | **Live** — §4.2 |
| F6 | **Frozen-mistake accumulation** | Nine pillars kept because renumbering breaks links | **Accepted** — §3.1 |
| F7 | **Hub inflation** | 45 hubs for 266 leaves — some hubs holding one leaf | **Likely**; not counted per hub |

F7 is worth a number: 266 leaves across 45 hubs averages **5.9 leaves per hub**.
A hub with one leaf is a redundant click, and the estate has not counted its
distribution. That count is cheap and owed.

## 7. Limits

1. **Retrospective scopes.** §3's scopes were fitted to existing names. The
   partition may be sound; it has not been derived, only rationalised.
2. **Two pillars are empty of leaves** (Annex A). Their scopes are therefore
   **untested by any actual page**, which is the same E0 problem that runs through
   the estate.
3. **The tie-break hierarchy has been applied to few real collisions.** §5 is one
   worked case. A four-rule hierarchy validated against one case is not validated.
4. **Hub distribution uncounted** (F7).
5. **No Arabic text**, while `prevailing_text: ar`. The authoritative statement of
   the estate's own top-level structure does not exist.
6. **Nine is arbitrary and now permanent** (§3.1).

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** any document is shown to belong to two pillars, or to none;
> - **(b)** a pillar's stated exclusions are shown to exclude a document that is in
>   fact filed under it;
> - **(c)** applying §2.2's four rules to a real collision yields a different
>   pillar than where the document sits;
> - **(d)** a pillar page or group hub is shown to carry substantive content that
>   exists nowhere else — which would make a navigation page load-bearing and
>   unfindable;
> - **(e)** the leaf count under any pillar differs from
>   [SITE-01](../site/route-manifest.md)'s enumeration.
>
> **(c) is the real test** and requires only picking a document and running four
> rules. The estate has run it once (§5). Running it on ten documents would either
> validate the hierarchy or expose it, and takes under an hour.

## 9. Obligation

**On the estate:**
- Assign every document exactly one pillar (§2.1).
- State at least two exclusions per pillar; a pillar without exclusions is not
  publishable (§2).
- Log every rule-4 tie-break in the
  [reconciliation ledger](../00-governance-map/reconciliation-ledger.md).
- Never renumber or remove a pillar; redirect and record instead
  ([SITE-03](../site/routing-law.md)).
- Keep pillar and hub pages navigational; substantive content belongs on a leaf.
- Count leaves per hub and publish the distribution (F7).

**On a reader:**
- Use the exclusions to rule pillars out; they are the fastest navigation tool
  here.
- Expect correct filing to be occasionally counter-intuitive (§5), and use the
  related blocks.

---

## Annex A — Pillar census

Written leaf pages against planned routes, per
[REG-02 §5.1](../registries/reg-02-page-registry.md).

| Pillar | Written leaves | Planned | Group hubs | State |
|---|---|---|---|---|
| 1 Licence | ~6 | ~8 | 4 | Partial; Part H statement **unissued** |
| 2 Harms | 3 | 26+ | 6 | **Weakest relative to scope** — HX-000 is a draft |
| 3 Corpus | 19 | ~25 | 7 | Best covered |
| 4 Agents | 3 | 13 | 3 | Partial |
| 5 Standards | 18 | ~25 | 6 | Good |
| 6 Rubrics | 3 | 6 | 2 | Partial |
| 7 Design | 8 | ~10 | 4 | Good |
| 8 Records | 20 | ~21 | 8 | Good |
| 9 Site | 4 | 4 | 3 | **Complete** |
| **BCIA** *(sub-domain of 3)* | **0** | 10 | 2 | **Empty** |
| **Lexicon** *(sub-domain of 5)* | **1** | 4 | 1 | **Near-empty** |

**The two empty divisions are BCIA (`BX-000`…`BX-009`, zero written) and the
lexicon beyond its keyword register.** Both are named throughout the corpus and
neither exists. This is the honest answer to "how complete is the estate": nine
pillars, one complete, two effectively empty, and the tier 1a harms pillar
resting on a draft.

## Annex B — Terms reserved and not used

Names considered for pillars and rejected, recorded so their later adoption is
visibly a reversal:

| Name | Why rejected |
|---|---|
| Community | Implies participation the estate does not offer ([REG-08 §5.1](../registries/reg-08-role-and-authority-registry.md)) |
| Learning | Overlaps Rubrics and Corpus with no clean tie-break |
| Products | No product exists; [MX-021](mx-021-payments-and-commerce.md) path inactive |
| Research | Would imply human-subjects work, hard-excluded by [MX-014](mx-014-research-ethics-and-exclusions.md) |

---

### Related

**Structure and addressing** — [SITE-01](../site/route-manifest.md) ·
[SITE-02](../site/page-contract.md) · [SITE-03](../site/routing-law.md) ·
[ST-24](../standards/st-24-page-prose-standard.md)

**Scope and authority** — [MX-000 Charter](mx-000-charter.md) ·
[MX-001](mx-001-about-metax.md) ·
[precedence](../00-governance-map/precedence-and-conflict-rules.md) ·
[ST-01](../standards/st-01-identifier-and-url-grammar.md)

**Census and records** — [REG-02](../registries/reg-02-page-registry.md) ·
[GM-02 document index](../00-governance-map/document-index.md) ·
[REG-08](../registries/reg-08-role-and-authority-registry.md) ·
[task ledger](../00-governance-map/task-ledger.md)

**The empty divisions** — [HX-002](../harms/hx-002-harm-instrument-map.md) ·
[LEX-01](../lexicon/keyword-register.md) ·
[defect register](../00-governance-map/defect-register.md) ·
[launch blockers](../00-governance-map/launch-blockers.md)

### Exit pair

1. **Run the tie-break ten times.** Pick ten documents, apply §2.2, compare to
   where they sit. Falsifier §8(c) is the instrument's real test and is unrun.
2. **Look at what is empty.** [Annex A](#annex-a--pillar-census) — BCIA has ten
   planned routes and zero pages.

<!-- mx-pagestamp: MX-004 · v2026.10.1 · governing · tier 3 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the live site is a demonstration; most enumerated routes have no written page -->
