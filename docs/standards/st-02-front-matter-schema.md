---
doc_id: "ST-02"
title_en: "Front-Matter Schema"
title_ar: "مخطّط البيانات الأمامية"
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
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["standards", "front-matter", "metadata", "machine-reading"]
route: "/library/sources/schemas/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# ST-02 · Front-Matter Schema

**What this standard governs.** The YAML block at the head of every instrument: which fields are
required, what values are permitted, and what each field commits its author to.

**Why front matter is governance and not metadata.** Every field in this schema is a **claim the
estate can be held to.** `evidence_class: durable` asserts the content will not decay for a year.
`authority: governing` asserts the text binds. `counsel_reviewed: false` admits nobody qualified
has read it. The block is the machine-readable surface of the estate's honesty, and
[GM-11 §3](../00-governance-map/machine-reading-contract.md) makes six of these fields the signals
a machine reader may rely on.

---

## 1. Position

Front matter is where this corpus is most obviously written for machines. A human reader gets the
same information from the prose; a machine reader gets it in one parse, before reading anything —
which is what lets it resolve authority *before* content, as
[the Machine Reading Contract §2](../00-governance-map/machine-reading-contract.md) requires.

Its sibling is [ST-01](st-01-identifier-and-url-grammar.md), which governs the `doc_id` this
schema requires, and [ST-05](st-05-decay-and-review-intervals.md), which defines the decay classes
the `evidence_class` field selects from. Its published route is `/library/sources/schemas/`, which
is declared **thin by nature** under
[DEF‑2026‑043](../00-governance-map/defect-register.md#def-2026-043) — a schema page padded to
1,200 words would be padding.

---

## 2. Definition — required fields

Eighteen fields are required on every instrument. A missing required field is a build failure.

| Field | Type | Permitted values |
|---|---|---|
| `doc_id` | string | An identifier valid under [ST-01 §2](st-01-identifier-and-url-grammar.md) |
| `title_en` | string | — |
| `title_ar` | string | Arabic; required even where no Arabic edition exists |
| `family` | enum | `license` · `corpus` · `harms` · `agents` · `standards` · `rubrics` · `design` · `registries` · `bcia` · `site` · `governance-map` · `lexicon` |
| `version` | string | `v{YYYY}.{MM}.{n}` |
| `status` | enum | `canonical` · `draft` · `superseded` · `withdrawn` |
| `authority` | enum | `governing` · `operative-form` · `companion` · `record` |
| `prevailing_text` | enum | `en` · `ar` |
| `audience_tier` | int 1–5 | 1 general reader … 5 governance reader |
| `depth` | int 1–5 | Treatment depth |
| `evidence_class` | enum | `durable` · `semi-durable` · `perishable` |
| `review_interval_months` | int | 12 / 6 / 3, matching the evidence class |
| `curator` | string | `Maher` |
| `license` | string | The governing licence version |
| `designated` | bool | Whether it is a Work of Foundational Character |
| `last_reviewed` | ISO date | — |
| `domain_tags` | array | Free, lower-case |
| `hreflang` | string | `en, ar` |

### 2.1 The four fields most often wrong

**`authority` is not `status`.** `status: canonical` says the text is current; `authority: record`
says it binds nobody. The [License Version History](../license/version-history.md) is both —
current *and* non-binding. Conflating them produces the error
[GM-11 §5](../00-governance-map/machine-reading-contract.md) calls **authority flattening**:
treating everything in `docs/` as equally governing.

**`evidence_class` must match `review_interval_months`.** `durable` → 12, `semi-durable` → 6,
`perishable` → 3. A `perishable` document with a twelve-month interval is asserting that it decays
fast and need not be checked, which is incoherent.

**`title_ar` is required even with no Arabic edition.** Zero Arabic pages exist
([DEF-002](../00-governance-map/defect-register.md#def-002)). The field is required anyway, because
an instrument that cannot state its own Arabic title has not been thought about bilingually — and
ML-2.3 §H.22 makes parity a duty rather than an aspiration.

**`designated` is a legal claim, not a compliment.** `true` invokes Part G supremacy. It must match
[the Designation List](../license/designation-list.md) exactly, and a mismatch is a defect in both
documents.

---

## 3. Conditional fields

Required when their condition holds; forbidden otherwise.

| Field | Required when | Values |
|---|---|---|
| `provenance_of_purpose` | The document describes or relies on a live artefact | `production` · `staging` · `demo` · `specification` · `record` |
| `counsel_reviewed` | The document makes an enforceability claim | bool |
| `supersedes` | It replaces an earlier text | array of strings |
| `superseded_governing_text` | Its governing licence changed | string |
| `derived_from` | It is substantially derived from a source | string |
| `incorporated_by` | A higher instrument incorporates it | string |
| `authorship_note` | Authorship is mixed or agent-originated | string |
| `route` | It has a published address | A [SITE-03](../site/routing-law.md)-valid route |
| `ratification` | It awaits the Curator | `PENDING — RAT-nn` |
| `statement_status` | It is a Part H Statement | e.g. `NOT YET ISSUED` |
| `ai_disclosure_url` | AI systems contributed materially | URL |

### 3.1 `provenance_of_purpose` exists because of a failure

Added in v2026.10.1 after the estate published **nine claims about its own live code without
recording what that code was for.** Every claim was true of the bytes read. All nine read as
findings about the estate. Their subject was a **demo**
([C-14](../00-governance-map/corrections-log.md#c-14),
[DEF-024](../00-governance-map/defect-register.md#def-024)).

The general lesson, which is the most valuable sentence in this standard:

> Reading an artefact tells you what is there. It cannot tell you what the artefact is **for**.

None of the nine was false; all nine were **unlabelled**, which is the subtler defect and the one
no consistency check raises. A field is the only remedy, because the missing information was never
in the artefact.

### 3.2 `authorship_note` and §H.19

ML-2.3 §H.19 requires a recorded natural author for assertions issued in the estate's name.
Applied honestly it has produced three uncomfortable declarations:

- **HX-000** — harms H1–H11 are the documentation agent's; Strata V and VI arrived with the
  Curator's ML-2.3 text ([C-11](../00-governance-map/corrections-log.md#c-11)).
- **[ST-23](st-23-affiliate-and-referral.md)** — `authorship_note: "Designed from scratch. No
  supplied source contains an affiliate system."`
- **`Method` as a ninth pillar** — *"my addition, not yours"* in the nav spec's own words
  ([RAT-19](../00-governance-map/open-questions-and-ratifications.md#rat-19)).

**A duty that never embarrasses its holder is not operating.** The field's value is measured by how
often it produces an admission nobody wanted to make.

---

## 4. Worked instance — reading ST-22's block

[ST-22](st-22-platform-and-persistence.md) declares `evidence_class: perishable`,
`review_interval_months: 3`, `provenance_of_purpose: specification`.

**What a machine reader may conclude.** The content decays in three months. `last_reviewed:
2026-10-01` plus a three-month interval means it is stale after 2027‑01‑01 and must be **reported
as stale** rather than quoted as current. `specification` means it describes an intended system,
not a running one — so its four data tiers and six databases are a design, and no row has ever
been written.

**Why `perishable` rather than `durable`.** Its §5 renders six third-party platform limits. Those
change without notice, and a persistence standard written as though platform limits were durable is
a standard that will be quietly wrong within a year. The field is what makes that reasoning
machine-visible.

**The inference the block prevents.** Without `provenance_of_purpose: specification`, a reader
encountering "six D1 databases" would reasonably conclude they exist. They do not. One field
prevents a false conclusion that the prose alone left available — which is what a schema is for.

---

## 5. Failure modes

**Copy-paste inheritance.** The commonest failure. A new instrument copies a neighbour's block and
keeps its `evidence_class`, `last_reviewed` and `designated`. Signature: a cluster of instruments
sharing an implausibly identical review date.

**`durable` by default.** `durable` is the least demanding class — twelve-month review — so an
author under time pressure selects it. A perishable claim marked durable is a promise not to check
something that changes.

**`last_reviewed` set to the write date without a review.** Writing is not reviewing. This is
undetectable from the block and corrodes the whole apparatus, since every staleness computation
depends on the field meaning what it says.

**`authority: governing` as a status symbol.** Applied to companions and records because it sounds
more serious. Every misapplication makes the ladder in
[GM-01](../00-governance-map/precedence-and-conflict-rules.md) less usable.

**Conditional fields omitted where they would be unflattering.** `counsel_reviewed: false` and
`authorship_note` are precisely the fields an author is tempted to leave off. §3 makes them
required-when-applicable for that reason.

---

## 6. Limits

**Class: technical, and it is the binding one.** **No validator runs.** The front-matter check
would live in [SENTINEL](st-13-static-build-and-sentinel.md)
([DEF-001](../00-governance-map/defect-register.md#def-001)), so every requirement here is
currently enforced by whoever remembers it. The estate has already recorded what that produces:
[DEF-008](../00-governance-map/defect-register.md#def-008) — `domain_tags` populated with rubric
dimensions across the v2026.08.12 instruments, undetected until read by hand.

This standard is therefore a specification of what the blocks *should* contain, and the corpus's
actual conformance is unmeasured.

**Class: epistemic.** The schema cannot detect a field that is well-formed and untrue. A document
claiming `evidence_class: durable` about volatile content parses cleanly.

**Class: governance.** `designated` must match the Designation List, and the list is itself
**unratified** ([RAT-06](../00-governance-map/open-questions-and-ratifications.md#rat-06--ratify-the-designation-list)),
so every `designated: true` in the corpus is asserted rather than settled.

---

## 7. Falsifier

This schema is wrong if:

1. **An instrument requires a field the schema does not define** — under-inclusive. Candidate:
   nothing currently records *who* reviewed at `last_reviewed`, only the date.
2. **A required field is genuinely inapplicable to some instrument class**, showing §2's
   eighteen-field floor too high. `title_ar` is the candidate for a machine-only artefact.
3. **Two authors reading §2 produce incompatible blocks for the same document**, showing the
   permitted values too vague.
4. **The estate's own conformance proves poor when measured**, which would falsify not the schema
   but the estate's claim to be following it. This is the likeliest of the four and is currently
   **unmeasurable** by §6's own admission.

---

## 8. Obligation

**For any author:** eighteen required fields, plus every applicable conditional. Set
`last_reviewed` only when a review actually happened. Choose `evidence_class` by asking *what would
make this wrong, and how fast* — not by copying a neighbour.

**For any author describing a live artefact:** `provenance_of_purpose` is required. Nine claims
published without it in one release, none false, all unlabelled.

**For the estate:** build the validator. Until it runs, this standard and
[ST-01](st-01-identifier-and-url-grammar.md) are habits, and
[GM-11](../00-governance-map/machine-reading-contract.md) promises machine readers six signals of
which the corpus reliably delivers three.

**Under ML-2.3:** §H.19 (authorship of record — `authorship_note`), §H.4 (optimisation
disclosure), §H.26 (corpus hygiene), §H.22 (language parity — `title_ar`, `hreflang`), §H.29
(substitution disclosure — `ai_disclosure_url`).

---

**Related:** [ST-01 Identifier and URL Grammar](st-01-identifier-and-url-grammar.md) ·
[ST-05 Decay and Review Intervals](st-05-decay-and-review-intervals.md) ·
[ST-13 Static Build and SENTINEL](st-13-static-build-and-sentinel.md) ·
[Machine Reading Contract](../00-governance-map/machine-reading-contract.md) ·
[Precedence and Conflict Rules](../00-governance-map/precedence-and-conflict-rules.md) ·
[Designation List](../license/designation-list.md)

*Curated by Maher. Eighteen required fields, eleven conditional, and no validator — so this
standard describes what the corpus should look like and cannot yet tell you whether it does.*
