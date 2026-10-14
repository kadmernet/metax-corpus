---
doc_id: "GM-01"
title_en: "Precedence and Conflict Rules"
title_ar: "قواعد الأولوية وتعارض النصوص"
family: "governance-map"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 5
evidence_class: "durable"
curator: "Maher"
license: "ML-2.3 · Work of Foundational Character"
last_reviewed: "2026-10-01"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# Precedence and Conflict Rules

A corpus with a hundred instruments and one author will contain contradictions. The
question is not whether they occur but whether they are resolved by a published rule or
by whoever is reading at the time. This document is that rule.

---

## 1. The precedence ladder

Where two instruments in this corpus conflict, the higher tier governs. Within a tier,
[§2](#2-same-tier-conflicts) applies.

| Tier | Instrument class | Examples |
|---:|---|---|
| 1 | **Maher's License** | [ML-2.3](../license/ml-2-3.md), including **Part H**, Part G and §C.9 |
| 1a | **The Register incorporated by §A.10** | [HX-000](../harms/) — see §1.1 |
| 2 | **The Charter** | [MX-000](../corpus/mx-000-charter.md) — §0.4 and §0.5 are unamendable toward weakness |
| 3 | **Corpus instruments** | [MX-001](../corpus/mx-001-about-metax.md) … [MX-024](../corpus/mx-024-infrastructure-and-migration.md) |
| 4 | **Agent instruments** | [AG-000](../agents/ag-000-agent-constitution.md) … [AG-012](../agents/ag-012-degraded-mode-and-succession.md) |
| 5 | **Standards and rubrics** | [ST-01](../standards/st-01-identifier-and-url-grammar.md) … [ST-24](../standards/st-24-page-prose-standard.md), [RB-01](../rubrics/rb-01-d1-d5-rubric.md) … [RB-05](../rubrics/rb-05-harm-review-gate.md), [HX-001](../harms/hx-001-harm-audit-rubric.md) |
| 5a | **Design system** | [DS-00](../design/ds-00-as-built-token-layer.md) governing; DS-01…[DS-07](../design/ds-07-navigation-geometry.md) |
| 6 | **Registries** | [REG-01](../registries/reg-01-series-registry.md) … [REG-08](../registries/reg-08-processors-keys-mirrors.md) |
| 7 | **Site specifications** | [SITE-01](../site/route-manifest.md), [SITE-02](../site/page-contract.md), [SITE-03](../site/routing-law.md), [SITE-04](../site/demo-notice.md) |
| 8 | **Published pages and generated artefacts** | Anything the build emits |
| — | **Records** | Outside the ladder entirely — see §1.2 |

Two clarifications that matter more than the ladder itself.

**The License is above the Charter and says so.** [MX-000 §0.1](../corpus/mx-000-charter.md#01-founding-statement)
states that where the Charter and the License conflict, the License governs, and that any
inconsistent Charter provision is void from the moment of inconsistency rather than from
its discovery. That is not a courtesy to the License; it is what makes the Charter
falsifiable.

**A lower tier may be stricter, never laxer.** A standard may impose a requirement the
corpus does not mention. It may not relieve anyone of a corpus requirement. A registry may
record more fields than a standard requires; it may not record a value a standard forbids.

### 1.1 Tier 1a — the Register, and why it needed its own rung

[ML-2.3 §A.10](../license/ml-2-3.md) incorporates **HX-000** by reference. An incorporated text is
part of the instrument incorporating it, which would put the Register at tier 1 — nearly right, and
wrong in one case, so the ladder states the case rather than leaving it to inference.

**§E.9 resolves it:** *"a conflict between this License and the Register is resolved in favour of
this License and is itself a defect to be filed."* Tier 1a records that outcome — the Register
governs everything below and yields to the licence text above.

The distinction is not academic. The Register **describes** twenty-five harms; only §H.3(a)'s eight
absolutes **prohibit**. A reader treating the Register as tier 1 in full may conclude that naming a
harm forbids it, which is the commonest misreading of Part H and the one
[the enforceability table §6.3](../license/enforceability-two-track-table.md) exists to correct.

**The Register does not currently exist at its cited path**
([DEF-021](defect-register.md#def-021), ML‑D‑008), so tier 1a points at an absent document and no
party may rely on it. Stated here because a ladder with a phantom rung is worse than one admitting
the rung is empty.

### 1.2 Records are outside the ladder

Six instruments carry `authority: "record"` and **govern nothing**:
[Document Index](document-index.md), [Verification Log](verification-log.md),
[Archive Register](archive-register.md), [Changelog](changelog.md),
[Corrections Log](corrections-log.md),
[License Version History](../license/version-history.md).

They are evidence *about* the corpus, and the exclusion cuts both ways. **A record cannot create an
obligation** — a changelog entry describing a duty does not impose it. **And a record cannot be
overridden**, because it makes no normative claim to override: no instrument at any tier can make
the Corrections Log stop having recorded that the estate was wrong.

That second half is the protection. If records sat inside the ladder, a tier‑1 amendment could in
principle purge them. [MX-000 §0.5.2](../corpus/mx-000-charter.md#2-the-correction-obligation)
places the correction obligation beyond the Curator, and §1.2 is the precedence-layer expression of
the same idea: **the estate's record of its own errors is not a governable object.**

### 1.3 Ordering consequence of the site layer

Tier 7 previously named `route-manifest-fixed.md` and `page-spec-hub.md`, describing eight content
subdomains and a route grammar the estate does not have ([C-04](corrections-log.md#c-04), C-15).
Superseded and archived at [Archive Register B-04/B-05](archive-register.md).

Note the ordering, since it inverts easily: **SITE-01 is tier 7 and ST-24 is tier 5.** Where the
route manifest and the prose standard conflict about what a page must contain, **the standard
governs.** The manifest governs *addresses* and says so on its own face.

---

## 2. Same-tier conflicts

Within a tier, in order:

1. **The more specific instrument governs the specific case**, and the general instrument
   continues to govern everything else.
2. **The later release governs**, where both texts are in the same release family and the
   later one addresses the same question. Release order is fixed by
   [Changelog](changelog.md).
3. **The prohibition governs the permission.** Where one text permits and another forbids
   the same conduct, the conduct is forbidden until the conflict is resolved. This rule is
   deliberately asymmetric: the cost of an unnecessary refusal is delay, and the cost of an
   unauthorised permission is a breach of the Charter.
4. **If none of the above resolves it, the conflict is a defect.** It is filed in the
   [Defect Register](defect-register.md), escalated under
   [AG-004](../agents/ag-004-refusal-and-escalation-register.md), and decided by Maher. No
   agent and no editor resolves a same-tier conflict by choosing.

---

## 3. Summaries never govern

Several documents in this corpus restate a rule that is operative somewhere else. Restating
is permitted; drifting is not. Every summary carries three things:

- a conspicuous notice that it is a summary and creates no obligation absent from the source;
- a link to the governing text;
- an explicit conflict rule resolving to that text.

The pattern was adopted because exact textual mirroring between two instruments is a known
drafting failure: two copies of a normative sentence drift at the first amendment, and the
drift is invisible until somebody exploits it. The canonical instance is
[MX-002 §2.6](../corpus/mx-002-terms-of-service.md#26-machine-reading-and-ai-training),
which summarises [ML-2.1 §C.10](../license/ml-2-1.md#c10--machine-learning-model-training-and-synthetic-derivation)
and is mechanically checked against it by
[SENTINEL](../standards/st-13-static-build-and-sentinel.md#5-single-source-checks).

**Single-source pairs currently under mechanical check:**

| Summary | Governing text | Check |
|---|---|---|
| [MX-002 §2.6](../corpus/mx-002-terms-of-service.md#26-machine-reading-and-ai-training) | [ML-2.1 §C.10](../license/ml-2-1.md#c10--machine-learning-model-training-and-synthetic-derivation) | Build fails if the summary asserts an obligation absent from §C.10 |
| [MX-012](../corpus/mx-012-licensing-and-reuse.md) | [ML-2.1](../license/ml-2-1.md), [Designation List](../license/designation-list.md) | Build fails on a designation not in the List |
| [MX-007](../corpus/mx-007-ai-use-and-disclosure.md) | [AG-000](../agents/ag-000-agent-constitution.md), [AG-009](../agents/ag-009-prohibited-actions.md) | Build fails if a public refusal is missing from the agent instruments |
| [Hub governance page](../site/route-manifest.md) | [MX-000](../corpus/mx-000-charter.md), [MX-016](../corpus/mx-016-appeals-and-due-process.md) | Current state only; history lives in the Record |
| [SITE-04 §2](../site/demo-notice.md) "what is real" | [Document Index](document-index.md) | Must not claim an instrument exists that the index marks REFERENCED |
| [MX-023 §3.6](../corpus/mx-023-attention-and-human-sovereignty.md) | [MX-009](../corpus/mx-009-advertising-and-commercial.md), [ML-2.3 Part H](../license/ml-2-3.md) | Fails if the advertising disposition diverges from [HX-002](../harms/hx-002-harm-instrument-map.md) |
| [ST-22 §4.2](../standards/st-22-platform-and-persistence.md) forbidden columns | [ML-2.3 §C.9](../license/ml-2-3.md), [ST-23 §3.3](../standards/st-23-affiliate-and-referral.md) | Fails if a schema declares a column either text forbids |

**None of these checks runs.** [SENTINEL](../standards/st-13-static-build-and-sentinel.md) is a
specification, not a pipeline ([DEF-001](defect-register.md#def-001)), so every row above is a
*specified* check and an *unperformed* one. The table is kept in the present tense because that is
what it will mean when the build runs, and the gap is disclosed here rather than by the absence of
a build.

---

## 4. Language authority

Precedence between an authoritative text and a translation is not decided here. It is
decided by [MX-020 Language Authority](../corpus/mx-020-language-authority.md), which has
four limbs: Arabic governs the Meta-X and BCIA book libraries and the Lexicon; English
governs the License and the MX instruments, subject to a mandatory-consumer-law carve-out;
every instrument states its own prevailing text on its face; and a divergence between an
authoritative text and its translation is a defect rather than a matter for interpretation.

Every document in this corpus carries `prevailing_text` in its front matter. That field, not
a global assumption, is the operative statement for that document.

---

## 5. What is outside precedence entirely

Four things are not subject to the ladder because they cannot be traded away by any
instrument at any tier:

1. **[Charter §0.4](../corpus/mx-000-charter.md#04-the-three-refusals) — the three refusals.**
   Laboratory instruction in biology; Core Riba; the sexualisation of minors. No research
   exception, no artistic exception, no contextual reframing, no amendment toward weakness.
2. **[ML-2.1 §C.9](../license/ml-2-1.md#c9--absolute-prohibition-of-core-riba) — Core Riba.**
   Non-severable by private agreement; reformable by a court only to the narrowest
   enforceable form, and surviving in every forum as a limit on representation.
3. **[Charter §0.5](../corpus/mx-000-charter.md#05-powers-placed-beyond-the-curator) — the
   powers beyond the Curator.** The ethics veto, unilateral revocation, and unilateral
   amendment of the succession instrument.
5. **[ML-2.3 §H.3(a)(i)–(viii)](../license/ml-2-3.md) — the eight absolutes.** They bind at
   **every scale including Tier 0 private use**, and the [Scale Gate](../license/scale-gate.md)
   allocates investigative duties only — never permission. Under §F.4 they are **conditions**, so
   breach terminates the grant automatically rather than sounding in contract.
   **(vii) developmental substitution is disjunctive** — any single limb suffices, unlike the
   cumulative §C.9.2 model — and reading it as cumulative is the error most likely to be made in
   good faith.
6. **[ML-2.3 §H.16.3](../license/ml-2-3.md) — the all-clear presumption.** A Part H Statement
   recording nothing partially remedied or unremedied is presumptively non-compliant and is
   evidence of HX‑15. It sits outside precedence because it is an **evidential** rule no instrument
   can trade away: no lower tier can make a clean return respectable, and the estate cannot exempt
   itself — which is why its own Statement is
   [NOT YET ISSUED](../license/part-h-statement.md) rather than issued clean.
7. **[MX-000 §0.5.2](../corpus/mx-000-charter.md#2-the-correction-obligation) — the correction
   obligation.** §1.2 is its precedence-layer expression.
8. **[ML-2.1 §G.5](../license/ml-2-1.md#g5-humility-clause) — the humility clause.** A
   determination issued in bad faith, to suppress dissent, or to entrench the Steward's
   advantage is void. This clause protects the corpus against its own author, which is the
   only reason the rest of the corpus is credible.

---

## 6. Filing a conflict

Anyone may file. The route is the corrections address in
[MX-001 §1.7](../corpus/mx-001-about-metax.md#17-contact-and-recourse). A filing needs three
things: the two texts quoted verbatim with their paths and versions, the conduct or decision
that turns on the difference, and the resolution you believe is correct. Filings receive a
reasoned reply, and the reply is published in the
[Corrections Log](corrections-log.md) whether or not the filing succeeded.

A conflict report is never treated as an attack on the corpus. It is the corpus working.
