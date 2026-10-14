---
doc_id: "ST-01"
title_en: "Identifier, Naming and URL Grammar"
title_ar: "قواعد المعرّفات والتسمية والعناوين"
family: "standards"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 4
depth: 5
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: true
last_reviewed: "2026-10-01"
domain_tags: ["standards", "identifiers", "naming", "notation"]
route: "/method/notation/identifiers/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# ST-01 · Identifier, Naming and URL Grammar

**What this standard governs.** Every identifier the estate mints: what the prefixes mean, how
numbers are allocated, and the rules that make an identifier permanently citable. It is
**designated** as a Work of Foundational Character ([DL-1 row 11](../license/designation-list.md))
because a corpus whose identifiers can be reassigned cannot be cited at all.

**Its relation to the routing law.** ST-01 governs the **identifier**; [SITE-03](../site/routing-law.md)
governs the **address**. `MX-023` is an identifier; `/about/policy/ai-policy/` is where the
instrument bearing it is published. The two are deliberately independent — an instrument may be
re-routed without being renumbered, and must never be renumbered at all.

---

## 1. Position

An identifier is the smallest unit of citability in this estate, and every durability claim the
corpus makes decomposes into claims about identifiers. `ML-2.3 §H.3(a)(vii)` must mean the same
thing in 2031 as today. `DEF-021` must still name the same defect after four hundred more are
filed. `HX-15` must not silently become a different harm.

This standard exists because the alternative is not chaos but something worse: **plausible drift.**
Identifiers reassigned one at a time, each reassignment locally sensible, until a body of citations
in the wild points at documents that no longer say what they said. Nobody notices, because every
individual citation resolves to *something*.

Its published route is `/method/notation/identifiers/` and its sibling is
[ST-02 Front-Matter Schema](st-02-front-matter-schema.md), which governs the fields an identified
document must carry.

---

## 2. Definition — the prefix registry

Every identifier is `{PREFIX}-{NUMBER}` or `{PREFIX}-{NUMBER}{SUFFIX}`. The prefix is closed:
adding one is an amendment to this standard requiring a changelog line.

| Prefix | Family | Number form | Example |
|---|---|---|---|
| `ML-` | The licence and its schedules | Version, or `S{n}` / `D-{nnn}` | `ML-2.3`, `ML-S1`, `ML-D-007` |
| `MX-` | Corpus instruments | `000`–`999` | `MX-024` |
| `HX-` | Harms register and its apparatus | `000`–`999` for documents; `01`–`25` for harms | `HX-002`, `HX-15` |
| `AG-` | Agent instruments | `000`–`999` | `AG-004` |
| `ST-` | Standards | `01`–`99` | `ST-24` |
| `RB-` | Rubrics | `01`–`99` | `RB-05` |
| `DS-` | Design system | `00`–`99` | `DS-07` |
| `REG-` | Registries | `01`–`99` | `REG-03` |
| `BX-` | BCIA program instruments | `000`–`999` | `BX-005` |
| `GM-` | Governance map | `01`–`99` | `GM-12` |
| `SITE-` | Site layer | `01`–`99` | `SITE-01` |
| `DEF-` | Defects | `001`–`999`, or `{YEAR}-{nnn}` | `DEF-029`, `DEF-2026-041` |
| `B-` | Launch blockers | `01`–`99` | `B-20` |
| `R-` | Reconciliation entries | `01`–`999` | `R-56` |
| `C-` | Corrections | `01`–`999` | `C-13` |
| `RAT-` | Ratifications / open questions | `01`–`99` | `RAT-23` |
| `V-` | Verification tags | `01`–`999` | `V-13` |
| `S` | Course series | `S01`–`S99` | `S38` |
| `usr_` | User records | `usr_{ULID}` | `usr_01J...` |

### 2.1 The two dual-numbered prefixes, and why they are not defects

**`HX-`** carries two number spaces. `HX-000`, `HX-001`, `HX-002` are **documents**; `HX-01`
through `HX-25` are **harms inside** `HX-000`. The three-digit and two-digit forms are what
distinguish them, and the collision is tolerable only because the padding differs. This is
recorded as a **known weakness** of the scheme rather than defended: a reader encountering `HX-02`
must know whether a harm or a document is meant, and the answer is *harm*, because documents are
always three digits. Any future document beyond `HX-999` or harm beyond `HX-99` breaks it.

**`DEF-`** carries `DEF-{nnn}` and `DEF-{YEAR}-{nnn}`. The year-prefixed form is inherited from
the pre-corpus defect log and **survives because it was published**. `DEF-2026-041` cannot become
`DEF-031` under Rule 2 below, so the estate carries two forms permanently rather than tidying one
away. Recorded at [Archive Register C-02](../00-governance-map/archive-register.md).

---

## 3. Rule 1 — identifiers are allocated from a high-water mark

A new identifier takes the **next free number** in its family, recorded in the
[Task Ledger §7](../00-governance-map/task-ledger.md) high-water table. Never a gap-fill, never a
number chosen for meaning.

**Gap-filling is forbidden**, and this is the non-obvious half of the rule. If `DEF-014` is closed
and deleted from the open table, `DEF-014` is **not** available for reuse. A gap in a sequence is
information: it says something was there. Filling it makes two different subjects share one
address across time, which is the precise failure Rule 2 exists to prevent.

---

## 4. Rule 2 — numbers are immortal from first assignment

**Once published, an identifier's referent never changes.** Not on supersession, not on
supersession of the whole family, not to correct an ordering error, not to close a gap.

This is the most-cited rule in the corpus and it has been exercised four times:

| Collision | Requested | Resolution | Recorded |
|---|---|---|---|
| Payments and Identity | `MX-020`, `MX-021` | `MX-020` was Language Authority → **MX-021**, **MX-022** | [R-25](../00-governance-map/reconciliation-ledger.md#r-25--the-mx-020-numbering-collision) |
| Infrastructure and Migration | `MX-022` | Already Identity → **MX-024**, MX-023 having gone to Attention | [index §4](../index.md) |
| The file-ceiling defect | renumber to `DEF-031` | **Refused.** Re-characterised under `DEF-2026-041` | [DEF-2026-041](../00-governance-map/defect-register.md#def-2026-041) |
| The `MacroLifeTach` anchor | delete the defective slug | **Refused.** Retained beside the corrected one | [C-13](../00-governance-map/corrections-log.md#c-13) |

**The fourth row is the rule's hardest case and the clearest.** The anchor
`#r-42--the-third-pillar-is-macrolifetach-not-bcia` was minted from a misspelling and published.
Deleting it would trade a cosmetic defect for a broken citation, so both anchors now exist and the
defective one carries no authority. An estate willing to keep a misspelling visible in order to
keep a citation resolving has understood what Rule 2 is for.

**Redundancy is permitted; renumbering is not.** [Designation List §6](../license/designation-list.md)
records rows 1 and 14 both designating the licence — deliberate, so that a reader searching for
Part H finds an entry rather than inferring one. Neither row may now be renumbered, and the
redundancy is documented so a future editor does not "tidy" it into a defect.

---

## 5. Rule 3 — slug grammar

Every published slug: **lower-case, hyphen-separated, ASCII.** No underscores, no camel case, no
percent-encoding, no trailing hyphens. Filenames carry the identifier first:
`mx-024-infrastructure-and-migration.md`, `st-01-identifier-and-url-grammar.md`.

**Arabic content lives at `/ar/…` with English slugs.** Percent-encoded non-ASCII paths are legal
and technically fine, and the estate declines them: they are unreadable in a citation, break when
copied through systems that normalise differently, and make the two language mirrors structurally
incomparable. **Parity is easier to audit when both trees have identical shapes** — which is what
[SITE-03 §2](../site/routing-law.md) requires and what ML-2.3 §H.22 makes a duty.

**Case-sensitivity is a real hazard, not a style note.** Platform rule matching is case-sensitive,
so `/Method/` is a 404 and not an alias of `/method/`. On case-insensitive infrastructure both
resolve and the canonical tag disagrees with the address the reader is on — so the same corpus
behaves differently depending on where it is hosted. That is a portability defect wearing a
formatting question's clothes.

---

## 6. Rule 4 — the anchor grammar

Section anchors are generated from headings, lower-cased, non-alphanumerics to hyphens. Once
published, **an anchor is an identifier** and Rule 2 applies to it in full.

The consequence is uncomfortable and is stated rather than avoided: **a heading cannot be reworded
freely once its anchor is cited.** Rewording changes the anchor and breaks every citation. The
permitted move is to add an explicit `<a id="...">` preserving the old anchor beside the new one —
exactly the mechanism R-42 now uses. The estate therefore accumulates anchor aliases, and that
accumulation is the cost of citability rather than untidiness.

---

## 7. Worked instance — allocating MX-024

The architecture source proposed *"MX-022 Infrastructure & Migration."*

**Step 1 — check the high-water mark.** `MX-022` is Identity and Sessions, published. Rule 2:
unavailable.

**Step 2 — check the next free number.** `MX-023` had been allocated to Attention and Human
Sovereignty, required by ML-2.3 Part H Stratum I. Also unavailable.

**Step 3 — allocate.** `MX-024`.

**Step 4 — record the collision, not just the outcome.** A note in
[`docs/index.md` §4](../index.md) states what was requested, what was allocated, and why — because
a future reader encountering the architecture source will find "MX-022" and needs to resolve it
without guessing.

**What was not done.** The source was not amended to say MX-024, and MX-022 was not renumbered to
free the slot. Both would have been tidier and both would have destroyed the record of the
collision. **The estate's numbering is deliberately less tidy than it could be**, and every
untidiness in it is a preserved citation.

---

## 8. Failure modes

**The tidy renumbering.** The characteristic failure: an editor notices MX-023 and MX-024 are out
of thematic order and reorders them. Every external citation now points at the wrong instrument,
and nothing detects it because both resolve.

**Gap-filling after a closure.** `DEF-014` closes, the row is removed from the open table, and the
next defect takes 014. Two subjects, one address, across time.

**Meaningful numbers.** Reserving `MX-100` for "future commerce instruments." A number that
carries meaning acquires a constituency that resists reallocation, and the meaning is always
obsolete before the number is used.

**Silent anchor drift.** Rewording a heading for clarity. §6's failure, invisible until an external
citation breaks.

**Prefix invention.** Minting `SEC-` for security documents because none of the existing prefixes
feels right. The prefix table is closed for exactly this reason: two prefixes for one family is how
a corpus becomes two corpora.

---

## 9. Limits

**Class: technical.** No mechanism enforces any of this. The identifier validator would live in
[SENTINEL](st-13-static-build-and-sentinel.md), which does not run
([DEF-001](../00-governance-map/defect-register.md#def-001)). Every rule here is currently enforced
by whoever remembers it — which is, precisely, the estate's recurring failure recorded at
[HX-002 §8](../harms/hx-002-harm-instrument-map.md).

**Class: epistemic.** §2.1's `HX-` dual space works only while padding distinguishes the two, and
the standard does not know how many harms or harm-documents the register will eventually hold.

**Class: governance.** Rule 2 protects citations and makes the corpus permanently less legible than
a renumbered one would be. That trade is asserted, not demonstrated: the estate has no external
citations yet, so the rule currently costs tidiness and buys nothing measurable.

---

## 10. Falsifier

This standard is wrong if:

1. **An identifier is found whose referent changed after publication** — a Rule 2 breach, and the
   most serious available.
2. **Two published identifiers in one family share a number.**
3. **A slug conforming to §5 nonetheless fails to resolve on the target platform**, falsifying the
   ASCII/lower-case grammar as sufficient.
4. **The `HX-` dual number space produces a genuine ambiguity** in a real citation, falsifying
   §2.1's padding defence.
5. **Rule 2's cost exceeds its benefit at scale** — if anchor aliases and out-of-order numbering
   make the corpus materially harder to use than the citations are worth. Testable only once
   external citations exist.

---

## 11. Obligation

**For any author minting an identifier:** take the next free number from the
[Task Ledger §7](../00-governance-map/task-ledger.md) table and **update the table in the same
edit.** An allocated-but-unrecorded number is the mechanism by which the next author creates a
collision.

**For any editor rewording a heading:** preserve the old anchor with an explicit `<a id>`. This is
not optional and it is not tidy.

**For anyone tempted to renumber:** the collision record is worth more than the ordering. File the
collision, allocate forward, and leave the untidiness in place.

**Under ML-2.3:** §H.12 (harm to the record), §H.19 (authorship of record), §H.26 (corpus
hygiene), §H.25 (silence in the record — a renumbering with no record is exactly that), §H.20
(inheritance of unauditable systems — a successor inheriting drifted identifiers inherits a corpus
whose citations cannot be checked).

---

**Related:** [ST-02 Front-Matter Schema](st-02-front-matter-schema.md) ·
[SITE-03 Routing Law](../site/routing-law.md) ·
[SITE-01 Route Manifest](../site/route-manifest.md) ·
[Task Ledger §7](../00-governance-map/task-ledger.md) ·
[Archive Register](../00-governance-map/archive-register.md) ·
[Document Index](../00-governance-map/document-index.md) · [ML-2.3](../license/ml-2-3.md)

*Curated by Maher. Nineteen prefixes, four rules, two dual-numbered families kept as known
weaknesses — and a misspelt anchor retained on purpose, because a broken citation is the worse
defect.*
