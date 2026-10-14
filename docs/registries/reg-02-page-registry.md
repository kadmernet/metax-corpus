---
doc_id: REG-02
title_en: Page Registry
title_ar: سجل الصفحات
family: registries
version: v2026.10.1
status: published
authority: record
prevailing_text: ar
audience_tier: 3
depth: meta
evidence_class: perishable
review_interval_months: 3
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [pages, registry, routes, census]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. The census below is a claim about the estate that the estate cannot presently verify mechanically.
route: /registries/pages/
---

# REG-02 — Page Registry

> **Authority note.** A **record**. Outside the precedence ladder
> ([GM-01](../00-governance-map/precedence-and-conflict-rules.md)). It reports; it
> does not rule. The address law is [SITE-03](../site/routing-law.md); the address
> list is [SITE-01](../site/route-manifest.md); the page form is
> [SITE-02](../site/page-contract.md) and [ST-24](../standards/st-24-page-prose-standard.md).

> **Disclosure first.** [SITE-01](../site/route-manifest.md) enumerates **321
> English routes**. This register accounts for **far fewer written pages**. The gap
> is not a backlog in the ordinary sense — a route manifest that lists addresses
> for pages nobody has written is a *plan* presented in the grammar of an
> *inventory*. That category error is the single most misleading feature of the
> estate and is recorded as [DEF-032](../00-governance-map/defect-register.md).

---

## 1. Position

Four instruments touch a page, and a reader must keep them apart:

| Instrument | Tier | Answers |
|---|---|---|
| [SITE-03](../site/routing-law.md) | 7 | *May this address exist?* |
| [SITE-01](../site/route-manifest.md) | 7 | *Which addresses are planned?* |
| [ST-24](../standards/st-24-page-prose-standard.md) | 5 | *What must the prose do?* |
| **REG-02** (this) | — (record) | *Which pages have actually been written, and in what state?* |

Note the ordering trap restated: **ST-24 is tier 5 and SITE-01 is tier 7**. The
standard governing page *content* outranks the manifest governing page
*addresses*. A page may therefore be correctly addressed and still be
non-compliant, and the non-compliance is the more serious fault.

## 2. Definition

A **page** is a single addressable document intended for a reader, satisfying:

1. one route, root-absolute, well-formed under SITE-03's seven conditions;
2. front matter complete per [ST-02](../standards/st-02-front-matter-schema.md) —
   18 required fields, plus applicable conditionals;
3. prose in the eight-part recipe of ST-24, in a declared register (micro / meta /
   macro);
4. a page stamp, a related block of four groups totalling ≥ 8 links, and an exit
   pair of exactly two actions (SITE-02);
5. ≥ 1200 words, unless it falls in one of the **six thin-by-nature exemptions**
   declared by the nav spec §0(4).

An artefact failing (2) is **draft**. Failing (3) or (4) is **non-compliant**.
Failing (5) without exemption is **thin**. Failing (1) is **unpublishable** — it
has no address, so it is not a page at all.

### 2.1 State vocabulary

| State | Meaning | Reader-visible? |
|---|---|---|
| `written` | Full text, compliant with (1)–(5) | Yes |
| `thin` | Full text, under the word floor, no exemption | Yes, with notice |
| `exempt-thin` | Under floor, within one of the six exemptions | Yes |
| `non-compliant` | Text exists; SITE-02 furniture missing | Yes, with notice |
| `draft` | Text exists; front matter incomplete | **No** |
| `stub` | Route reserved; heading and disclosure only | Yes, labelled |
| `planned` | Route in SITE-01; nothing written | **No** — must 404 or be absent |
| `withdrawn` | Was published; removed under MX-008 | Route redirects per SITE-03 |

The critical rule: **`planned` is not a publication state.** A planned route must
not resolve to an empty page dressed as content. Under
[ST-04](../standards/st-04-falsifiability-and-claim-cards.md) an empty page with a
confident title is a counterfeit claim of coverage.

## 3. Mechanism

### 3.1 How a page enters this register

```
route reserved (SITE-01)     →  state: planned      [no row here]
front matter drafted         →  state: draft        [row created, not public]
prose complete, ST-24 form   →  state: written      [row public]
SITE-02 furniture added      →  compliance flag set
word count checked           →  thin flag set or cleared
page stamp written           →  date recorded
```

A row is created at **draft**, not at **written**. This is deliberate: the
register's value depends on showing work in progress, and a register that only
admits finished work systematically understates how much is unfinished.

### 3.2 The census method

The counts in §5 are produced by hand: directory listing, then file-by-file
inspection of front matter. They are **evidence class E1** under
[ST-07](../standards/st-07-evidence-and-verify.md) — checkable by a reader in
minutes — but they are *not* E3 (machine-reproduced), because
[ST-13 SENTINEL](../standards/st-13-static-build-and-sentinel.md) does not run.

Consequence, stated plainly: **every number below may be stale the moment it is
written.** The review interval is therefore set to **3 months**
(`evidence_class: perishable`), the shortest the estate uses.

### 3.3 Compliance arithmetic

For any population of pages *P*:

- **address correctness** = |{p ∈ P : route well-formed}| / |P|
- **form correctness** = |{p ∈ P : ST-24 eight parts present}| / |P|
- **furniture correctness** = |{p ∈ P : SITE-02 items 1–4 present}| / |P|
- **floor compliance** = |{p ∈ P : words ≥ 1200 ∨ exempt}| / |P|

The estate publishes all four rather than a single "compliance score", for the
same reason [RB-01](../rubrics/rb-01-d1-d5-rubric.md) refuses a total: a composite
lets a strong dimension conceal a failing one.

## 4. Worked instance

**One page, audited fully.** Take
[`/standards/st-24/`](../standards/st-24-page-prose-standard.md).

| Test | Result | Evidence |
|---|---|---|
| Route well-formed (SITE-03 × 7) | Pass | root-absolute, lowercase, no extension, trailing slash, unique, stable, in SITE-01 |
| Front matter 18 required | Pass | inspect head of file |
| Conditional fields applicable | Pass | `authorship_note` present as required for AI-drafted text |
| ST-24 eight parts | Pass | Position, Definition, Mechanism, Worked instance, Failure modes, Limits, Falsifier, Obligation |
| Register declared | Pass | `depth: meta` |
| Page stamp | Pass | trailing comment |
| Related block ≥ 8 links, 4 groups | Pass | 4 groups |
| Exit pair exactly 2 | Pass | 2 actions |
| Word floor ≥ 1200 | Pass | — |
| **Overall** | **`written`** | — |

Now the counter-instance. Take the **Arabic counterpart** of the same page,
`/ar/standards/st-24/`. It appears in SITE-01. It does not exist. Its state is
`planned`. And because `prevailing_text: ar`, the *governing* text of ST-24 is the
one that has not been written, while the *published* text is the subordinate one.
This is not a minor asymmetry; it means that across the estate the prevailing text
is largely **absent** — recorded at
[MX-020 §5](../corpus/mx-020-language-authority.md) and
[ST-11 §7](../standards/st-11-arabic-authoring.md).

## 5. The census

### 5.1 By family (English pages actually written)

| Family | Written | Draft | Stub | Planned (SITE-01) | Notes |
|---|---|---|---|---|---|
| Corpus `MX-` | 16 | 0 | 0 | ~25 | MX-002…006, 011, 017–019 absent |
| Standards `ST-` | 18 | 0 | 0 | ~25 | ST-08…10, 15–18 absent |
| Harms `HX-` | 3 | 1 | 0 | 26+ | HX-000 draft at append-point |
| Design `DS-` | 8 | 0 | 0 | ~10 | — |
| Rubrics `RB-` | 3 | 0 | 0 | 6 | RB-03, RB-04 absent |
| Agents `AG-` | 3 | 0 | 0 | 13 | 10 absent |
| Registries `REG-` | 3 | 0 | 0 | 8 | this batch |
| Site `SITE-` | 4 | 0 | 0 | 4 | complete |
| Governance map `GM-` | 12 | 0 | 0 | 13 | — |
| Licence `ML-` companions | 6 | 0 | 0 | ~8 | Part H statement unissued |
| Lexicon `LEX-` | 1 | 0 | 0 | 4 | entry standard absent |
| BCIA `BX-` | 0 | 0 | 0 | 10 | **entirely absent** |
| **Total (EN)** | **~77** | **1** | **0** | **321** | |

### 5.2 By language

| Language | Written | Planned | Prevailing? |
|---|---|---|---|
| English | ~77 | 321 | No — subordinate text |
| Arabic | **0** | 321 | **Yes — and absent** |

### 5.3 Compliance rates over written English pages

| Measure | Rate | Basis |
|---|---|---|
| Address correctness | high, unverified | no SENTINEL |
| ST-24 form correctness | high for pages authored since ST-24 | pages predating ST-24 unaudited |
| SITE-02 furniture | **partial** — three acceptance criteria are failed estate-wide | [SITE-02 §6](../site/page-contract.md) |
| Word floor | met by most; exemptions not individually recorded | — |

No percentage is stated where the denominator has not been counted by hand. A
precise-looking figure with an uncounted denominator is worse than an admitted
gap.

## 6. Failure modes

| # | Failure | Mechanism | Current state |
|---|---|---|---|
| F1 | **Planned-as-published** — a manifest route resolving to a confident empty page | Static generator emits a shell for every manifest entry | **Prevented by absence** — no site is built; would recur on first build |
| F2 | **Census drift** — counts here diverge from the tree | Manual census, no automation | **Certain over time**; mitigated only by the 3-month interval |
| F3 | **Draft leakage** — an incomplete page becomes reachable | Missing `status` gate in build | Unguarded |
| F4 | **Furniture rot** — related-block links go stale as pages move | Append-only redirects not applied to inbound links | **Occurring** — one stale anchor retained knowingly (R-42) |
| F5 | **Exemption abuse** — thin pages claimed under the six exemptions without naming which | No field records *which* exemption | **Live** — the exemption claimed is nowhere recorded per page |
| F6 | **Prevailing-text illusion** — reader assumes the English page governs | `prevailing_text: ar` in front matter, Arabic absent | **Systemic** |

F5 deserves a note. The nav spec grants six thin-by-nature exemptions. Nothing in
[ST-02](../standards/st-02-front-matter-schema.md) requires a page to *name* the
exemption it relies on. An unnamed exemption is unfalsifiable, and an
unfalsifiable exemption is not an exemption but a loophole. Filed as a
ratification question: **RAT-24**.

## 7. Limits

1. **This is a hand census.** Its accuracy decays continuously and it has no
   machine witness.
2. **Word counts are not recorded per page.** The floor is therefore asserted, not
   demonstrated, for most rows.
3. **The Arabic column is a single zero.** Everything the estate says about
   bilingual authority is, at the level of pages, currently aspiration.
4. **No page has a recorded *reader*.** The register knows what exists; it knows
   nothing about whether anyone read it, and the estate deliberately declines to
   instrument that ([MX-023 §2 refusals](../corpus/mx-023-attention-and-human-sovereignty.md)).
   This is a limit accepted on purpose, not a defect.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** a written English page exists in a family whose §5.1 count does not
>   include it;
> - **(b)** any route in SITE-01 resolves, on a built site, to a page this register
>   marks `planned`;
> - **(c)** an Arabic page exists — §5.2 claims zero, and one counter-example
>   destroys the row;
> - **(d)** a page marked `written` is shown to lack any of the eight ST-24 parts.
>
> (a) and (c) are checkable by directory listing in under two minutes. (d) is
> checkable by reading one page. The estate has performed (d) on exactly one page
> (§4) and generalised — which is precisely the inferential vice
> [ST-07](../standards/st-07-evidence-and-verify.md) classes as E1-presented-as-E3.

## 9. Obligation

No obligation arises from this record. The bearing obligations:

- Build no page for a `planned` route — [SITE-03](../site/routing-law.md).
- Meet the eight-part recipe — [ST-24](../standards/st-24-page-prose-standard.md).
- Carry complete front matter — [ST-02](../standards/st-02-front-matter-schema.md).
- Publish failures rather than round them away —
  [MX-013 §3](../corpus/mx-013-records-and-versioning.md).
- Do not instrument readers to improve these numbers —
  [MX-023](../corpus/mx-023-attention-and-human-sovereignty.md).

---

### Related

**Address and form** — [SITE-01](../site/route-manifest.md) ·
[SITE-02](../site/page-contract.md) · [SITE-03](../site/routing-law.md) ·
[ST-24](../standards/st-24-page-prose-standard.md)

**Language** — [MX-020](../corpus/mx-020-language-authority.md) ·
[ST-11](../standards/st-11-arabic-authoring.md) ·
[LEX-01](../lexicon/keyword-register.md)

**Records** — [GM-02](../00-governance-map/document-index.md) ·
[GM-08](../00-governance-map/verification-log.md) ·
[MX-013](../corpus/mx-013-records-and-versioning.md) ·
[changelog](../00-governance-map/changelog.md)

**Siblings** — [REG-01](reg-01-series-registry.md) ·
[REG-03](reg-03-book-registry.md) · [REG-05](reg-05-credential-registry.md) ·
[REG-07](reg-07-defect-classification-registry.md)

### Exit pair

1. **Falsify row 5.2.** List any Arabic page in the estate. If one exists, this
   register is wrong and must be corrected.
2. **Read the page law.** [SITE-02](../site/page-contract.md) states the twenty
   acceptance criteria this register merely counts.

<!-- mx-pagestamp: REG-02 · v2026.10.1 · record · reviewed 2026-09-16 · next review 2026-12-16 -->
<!-- mx-demo: the published site is a demonstration; counts describe the repository, not a live build -->
