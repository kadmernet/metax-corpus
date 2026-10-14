---
doc_id: "LEX-06"
title_en: "LEX-06 · Term Entries, Governance Set 1 (t-{root}-NN)"
title_ar: "LEX-06 · مداخل المصطلحات، مجموعة الحوكمة ١ [AR-DRAFT]"
family: "lexicon"
version: "v2026.10.3"
status: "draft"
authority: "companion"
prevailing_text: "en"
audience_tier: 3
depth: 3
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-08"
domain_tags: ["lexicon", "term-entries", "governance", "LEX-02"]
route: "/library/lexicon/entries/governance/"
form: "LEX-02 nine-field entry"
human_read: "none"
conformance_state: "partial"
derived_from: "LEX-02 §2 (form); LEX-04 §3 (t-{root}-NN grammar); LEX-05 contested terms; defining instruments as cited per entry"
authorship_note: "The first entries written under the prescribed grammar (GM-17 M-31). Field 2 (Arabic, the authoritative form) is EMPTY on every entry and marked [AR-REQUIRED]. An agent-invented Arabic term would be presented as the prevailing text while being a guess, which is worse than a gap. Entries are therefore non-compliant with LEX-02 at field 2 by construction, as LEX-02's own disclosure anticipates."
hreflang: "en, ar"
---

# LEX-06 · Term Entries, Governance Set 1

> **Authority.** A **companion**. Each entry is **a pointer with guards** (LEX-02 §1). It names exactly one
> defining instrument and never states the operative meaning. Open the instrument.

> **Disclosure first.** Every field 2 is empty. **These entries have no authoritative form** (LEX-02 §2.2).
> Root slugs are English placeholders until Arabic roots are supplied. When the Arabic root is set, the
> identifier does not change (Rule 2), and a `root_ar` field is added instead.

---

| # | Field | Content |
|---|---|---|
||**t-signed-01 · signed**||
| 1 | Term (EN) | signed |
| 2 | Term (AR) | **[AR-REQUIRED]** |
| 3 | Defining instrument | [REG-12 §2](../registries/reg-12-processors-keys-mirrors.md) (key and fingerprint) and [B-01](../00-governance-map/launch-blockers.md) |
| 4 | Orientation | Whether an instrument bears a verifiable signature against a published key |
| 5 | **Not** | **Not** a date in a source document. "SIGNED 2027-01-14 against [FPR]" is not signed (DEF-042) |
| 6 | Confusable pair | *ratified*. Ratified = adopted by the Curator. Signed = cryptographically attested. Either can exist without the other |
||**t-canonical-01 · canonical**||
| 1 | Term (EN) | canonical (status) |
| 2 | Term (AR) | **[AR-REQUIRED]** |
| 3 | Defining instrument | [ST-02](../standards/st-02-front-matter-schema.md) `status` enum |
| 4 | Orientation | A front-matter status value for a document currently in force in its role |
| 5 | **Not** | **Not** "read by a human". `canonical` with `human_read: none` is the corpus's characteristic state (UH-03). **Not** `published` (not an ST-02 value, X-30) |
| 9 | Superseded sense | "live" and "published" in the 00_* sources (CT-09) |
||**t-governing-01 · governing**||
| 1 | Term (EN) | governing (authority) |
| 2 | Term (AR) | **[AR-REQUIRED]** |
| 3 | Defining instrument | [GM-01 §1](../00-governance-map/precedence-and-conflict-rules.md) (the ladder) |
| 4 | Orientation | An `authority` value: the document's text binds within its tier |
| 5 | **Not** | **Not** "in force". A governing draft is not in force. Strings such as "governing on ratification only" are not ST-02 values (X-31) |
| 6 | Confusable pair | *record*: outside the ladder, binds nothing |
||**t-record-01 · record**||
| 1 | Term (EN) | record (authority) |
| 2 | Term (AR) | **[AR-REQUIRED]** |
| 3 | Defining instrument | [GM-01 §1.2](../00-governance-map/precedence-and-conflict-rules.md) |
| 4 | Orientation | A document that records facts and decisions, and sits outside precedence |
| 5 | **Not** | **Not** a governing instrument. A record that "decides" has exceeded its class |
||**t-refusal-01 · refusal (Charter)**||
| 1 | Term (EN) | refusal |
| 2 | Term (AR) | **[AR-REQUIRED]** |
| 3 | Defining instrument | [MX-000 §0.4](../corpus/mx-000-charter.md) |
| 4 | Orientation | What the estate will not do, placed outside precedence |
| 5 | **Not** | **Not** "MX-014 exclusion". **Contested:** MX-014 §2 lists three refusals that differ from MX-000 §0.4's four (GM-17 X-20, RAT-44) |
| 6 | Confusable pair | *absolute* (licence, §H.3) · *refusal A-n* (ML-B-1.0, BX-018) · *exclusion* (MX-014 §3). Four words, four instruments |
||**t-absolute-01 · absolute**||
| 1 | Term (EN) | absolute |
| 2 | Term (AR) | **[AR-REQUIRED]** |
| 3 | Defining instrument | [ML-2.3 §H.3(a)](../license/ml-2-3.md) |
| 4 | Orientation | A Part H prohibition whose breach is a condition breach, at every tier |
| 5 | **Not** | **Not** any strongly worded duty. §H.3(b): "These eight are exhaustive" |
| 7 | Imported from | — |
||**t-falsifier-01 · falsifier**||
| 1 | Term (EN) | falsifier |
| 2 | Term (AR) | **[AR-REQUIRED]** |
| 3 | Defining instrument | [ST-04 §2](../standards/st-04-falsifiability-and-claim-cards.md) |
| 4 | Orientation | The observation that would show a claim wrong |
| 5 | **Not** | **Not** a caveat. Under ML-2.3 §H.2.4 a falsifier may excuse a duty and never impose one |
| 7 | Imported from | Philosophy of science (Popper). **Narrower**: the four properties of ST-04 |
||**t-gate-01 · gate**||
| 1 | Term (EN) | gate |
| 2 | Term (AR) | **[AR-REQUIRED]** |
| 3 | Defining instrument | **None single. Contested** ([LEX-05 CT-14](contested-terms.md)) |
| 4 | Orientation | Always qualify: Substrate Gate G0–GX (ML-B-1.0), remediation gate 1–7 (BX-012), or Scale Gate tier (ML-2.3 §H.2-bis) |
| 5 | **Not** | A bare "gate" in new text is a defect |
||**t-steward-01 · steward**||
| 1 | Term (EN) | steward |
| 2 | Term (AR) | **[AR-REQUIRED]** (*amānah* is the principle, not the role) |
| 3 | Defining instrument | [ML-2.3 §E.8](../license/ml-2-3.md) |
| 4 | Orientation | The party that governs a licence or register |
| 5 | **Not** | **Not** an owner (BCIA remediation gate 5). **Not** a Custodian (BX-018 §1: custody attaches to the holding) |
||**t-designated-01 · designated**||
| 1 | Term (EN) | designated |
| 2 | Term (AR) | **[AR-REQUIRED]** |
| 3 | Defining instrument | [Designation list](../license/designation-list.md) (Works of Foundational Character) |
| 4 | Orientation | Listed as a Work of Foundational Character |
| 5 | **Not** | **Not** the front-matter field `designated: false`, which only records it. **No agent-drafted document asserts its own designation** |

## Count

10 entries (computed). 10 of 10 lack field 2.

## Falsifier

An entry here is defective if it states an operative meaning that a reader could act on without opening field 3.

---

**Related:** [LEX-01](keyword-register.md) · [LEX-02](lexicon-entry-standard.md) · [LEX-03](term-set-governance.md) · [LEX-04](metax-grammar.md) · [LEX-05](contested-terms.md)
