# The MetaX Universe — Canonical Corpus

**Release v2027.1 · Founded, built and curated by Maher · Licensed under
[ML-2.3](docs/license/ml-2-3.md) — the first SIGNED instrument in the chain**

This repository is the **source of truth** for the MetaX universe, written to be read by humans
and by AI systems. Every instrument is a Markdown file at a permanent path, with front matter, a
version, a stated authority, and relative Markdown links from every keyword and identifier to the
document that defines it.

**Start here → [`docs/index.md`](docs/index.md)**

---

## What this is

Maher supplied roughly fifty Markdown files — overlapping drafts, exact duplicates,
hash-suffixed export artefacts, and four top-level documents that disagreed with one another. The
task was to reconcile them into one corpus with full detail and final adjustments, generate the
documents that were referenced but missing, and link every keyword and identifier as a relative
Markdown URL to a detailed file.

**Six sources were consolidated:**

| Source | Role |
|---|---|
| `THE_METAX_CORPUS.md` | MX-000 … MX-019, AG-000 … AG-010, ML-2.1 amendment drafts |
| `Meta-Review_..._Complete_Sitemap.md` | Numbering and grammar rules, nine amendments, the full sitemap |
| `MetaX.Academy_Page_Content_Specification.md` | The global page contract and per-property page specs |
| `MetaX.Academy_UI-UX_and_Design_System_Documentation.md` | `MX-DESIGN-001` — changed the doctrine |
| `hx-000-the-fourteen-structural-harms.md` | The harms register — **declared fourteen, stated eleven** |
| `MetaX.Academy_Platform_Data_and_Persistence_Architecture.md` | `MX-ARCH-001` — **withdrew eight published decisions** |

They disagreed in **forty-four** places. Every disagreement is resolved **with its reason** in
[`docs/00-governance-map/reconciliation-ledger.md`](docs/00-governance-map/reconciliation-ledger.md).
Nothing was resolved silently. Escalations went to Maher rather than being decided editorially.

---

## The headline of v2027.1: the chain acquired a first link, and two governing documents were found to disagree

Eight source documents arrived, delivering the announced **ML-2.3**, the **twenty-five-harm
register**, **ML-2.4**, **ML-B-1.0**, **BX-000** and two build specs.

### 1. Everything in this corpus previously derived its authority from an unsigned text

```
ML-2.1  (unsigned — never the licence of record in fact)
  └→ ML-2.2  (DRAFT, never adopted — SKIPPED, not superseded)
  └→ ML-2.3  SIGNED 2027-01-14 · first signed instrument · Part H operative
       └→ ML-2.4  delta amendment · + Part J Deep-Time D1–D6 · UNSIGNED
            └→ ML-B-1.0  BCIA profile of ML-2.4
```

**[ML-2.3](docs/license/ml-2-3.md) is signed.** ML-2.2 is **skipped, not superseded** — it was a
draft over an unsigned predecessor, **a chain with no first link**. An instrument cannot supersede
what never took effect. This closed **B-01** and **RAT-14** in one act, because both were describing
the same fact.

> **A signature is an assumption of accountability, not a certificate of quality**
> ([§E.1-bis.4](docs/license/ml-2-3.md)). It was signed with **six items still open** — no counsel
> review, no registry mirrors, unverified evidence, unreviewed ethical mappings, no forum, and the
> estate's own non-compliance with Part H — because an unsigned instrument imposes duties on
> licensees while its author bears none.

### 2. Two governing documents disagreed about what the harms are

**ML-2.3 §H.2.2 and [HX-000 v2027.1](docs/harms/hx-000-the-twenty-five-structural-harms.md) assign
different harms to eleven identifiers.** Both say twenty-five harms, six strata, eight absolutes —
and **the two eight-absolute lists coincide on exactly one entry, on a different harm.**

Resolved for harm identity **in favour of the Register**, by splitting the precedence rule:

> *A precedence rule that lets the document **without** the inclusion criteria overrule the document
> **with** them prefers authority to evidence.*

Applied whole, the old rule would have **destroyed Stratum V as constituted** — the five harms the
estate found **in itself** — trading a self-diagnosis for a generic critique of others.

**The absolutes allocation is deliberately NOT resolved**
([RAT-23](docs/00-governance-map/open-questions-and-ratifications.md#rat-23--which-allocation-of-the-eight-absolutes-governs)),
because the reading that favours the licence would remove **precisely the three absolutes that bind
the estate and no others**:

> *An estate that resolved an ambiguity in the direction of removing the prohibitions that bind it,
> and no others, has not resolved an ambiguity.*

### 3. ML-2.4 amends two clauses the signed instrument already occupies

ML-2.4 *adds* §H.30 and §H.31. **ML-2.3 already has both** — and one is **§H.31.3, the Part H
conflict-resolution rule**, the only mechanism a licensee has for handling conflicting duties.
ML-2.4's additions **renumber to §H.34 and §H.35**; the signed instrument does not move.
**This blocks ML-2.4 Track 1 ratification** ([B-25](docs/00-governance-map/launch-blockers.md)).

**Cause:** a delta drafted against a **remembered** base text. *A delta amendment is only as good as
its author's copy of the base.*

### 4. The most actionable conclusion: DEF-001 is re-ranked

Four defects are **one failure observed four times** — two documents disagreeing about a fact
concerning their own contents, with no mechanical check:

| Defect | Disagreed about |
|---|---|
| DEF-050 | a **filename** |
| DEF-2027-004 | a **harm count** |
| **DEF-2027-009** | **harm identity** |
| **DEF-2027-015** | **clause numbers** |

**SENTINEL is specified to catch exactly this, across five documents, and it does not run.**

> **DEF-001 has been carried as infrastructure debt. It is in fact the upstream cause of the
> corpus's four most serious content defects — and the only one whose remedy needs no external
> party.** A link-and-consistency checker over a Markdown corpus is achievable by writing, by one
> person, at known cost. **The corpus has been treating its cheapest high-value remediation as
> housekeeping.**

### 5. And a finding that reframes six earlier defects

Six defects and three blockers are marked *not closable by writing* because the estate is one
person. But **a dissent channel independent of the steward, a forum, and an appeal route are not
blocked by headcount** — they are blocked by there being **no stateful component that could host
them**, a consequence of **P-10**, a premise **no document in this corpus has ever defended**
([DEF-2027-008](docs/00-governance-map/defect-register.md)).

> **The corpus has been holding a flattering diagnosis — *we are small* — in place of an
> uncomfortable one: *we chose a delivery model that cannot host due process.***

### 6. What the second pass added — BCIA, nine programmes, the site specs

**Nine further instruments:** [ML-B-1.0](docs/license/ml-b-1-0.md) (the BCIA profile),
[BX-000](docs/metax/bcia/bx-000-document-zero.md) (Document Zero — **24 entries, a dangling
reference in eleven files**), [MLT-000](docs/metax/programs/mlt-000-the-programme-register.md) plus
**nine programme charters**, [MX-READER-01](docs/site/mx-reader-01-course-series-reader.md),
[MX-SITE-DESIGN v2027.1](docs/site/mx-site-design-v2027-1.md), and
[MX-NAV-SPEC v2027.1](docs/site/mx-nav-spec-v2027-1.md) — the **428-route manifest.**

**The inverted grant is the reasoning worth keeping.** ML-B-1.0 grants **nothing** until a gate is
satisfied *and recorded*, because the base licence assumes a person who **can object** — and this
subject may have had that capacity **altered by the deployment itself.**

> *Where the subject cannot object, a grant that persists until objection is a grant that persists
> indefinitely.*

**And the Substrate Gate replaces the Scale Gate** on reasoning that generalises: *a single
researcher holding one vessel of neural tissue presents not a thousandth of the moral problem but
the whole of it at small volume.* **Where harm is to a single subject and irreversible, aggregation
is the wrong operation.**

### 7. The failure mode is now classified — nine instances, three kinds

| Kind | Detectable by |
|---|---|
| **Two documents disagree** — DEF-050, 2027-004, -009, -015, -018 | Comparing them |
| **A third document inherits the disagreement** — **DEF-2027-021** | **Nothing, from inside that document** |
| **A document drafted against a state another never reached** — **DEF-2027-016, -033** | Checking the chain |

**Kind 3 has the worst consequence.** The nav spec would have published **the unsigned ML-2.4 as
"The Instrument"** and **the signed ML-2.3 under *"Falsification & History"*, labelled
*superseded*.**

> **That is not a broken link. It is a misrepresentation of what a licensee is subject to.**

**Kind 2 cannot be fixed by care.** BX-000's crosswalk inherited a defect from two sources that were
**both authoritative on their own face.**

> **A defect in a precedence rule does not stay in the two documents that disagree. It propagates to
> every document that reads them.**

### 8. One document ships deliberately non-conformant

**[MX-SITE-DESIGN v2027.1](docs/site/mx-site-design-v2027-1.md) carries
`conformance_state: unmet`** — the only document in the corpus whose state is unmet **because of
what it itself requires**: ≈**118 KB of third-party JavaScript against a published 12 KB
first-party budget.**

The mitigation closes **provenance, not weight.** The smaller change — *a static two-slide fade, no
Owl* — was **offered and not taken**, and is recorded with its cost rather than as a resolved
trade-off.

**Eighty-eight defects on record**, eleven closed or corrected, three permanent or not closable.

---

## The headline of v2026.09.6: writing the standards indicted the corpus

No new source arrived. Nothing external changed. **Twenty-two instruments were written** — fifteen
standards, three rubrics, three corpus instruments, one agent instrument — and the corpus's honest
self-assessment got substantially **worse**.

| Added this release | Count |
|---|---|
| Defects | **DEF-021 … DEF-050** |
| Open questions | RAT-19 … RAT-22 |
| Launch blockers | B-17 … B-23 |

**Every one was found by specifying an obligation precisely — not by reviewing anything.** The
estate had been assuming the gap between the corpus as written and as intended was a gap of
*unwritten documents*. It is not.

### Finding 1 — The estate's characteristic failure is overstating its controls

Four instruments claimed an enforcement that does not exist:

| Defect | The claim |
|---|---|
| [DEF-023](docs/00-governance-map/defect-register.md#def-023) | The precedence rules said SENTINEL fails the build on summary drift. **It cannot** — that is natural-language entailment |
| [DEF-047](docs/00-governance-map/defect-register.md#def-047)(a) | §G.5 was described as protecting the corpus against its own author. **It is a standard assertable externally, not an internal remedy** |
| [DEF-047](docs/00-governance-map/defect-register.md#def-047)(b) | MX-016's voidness rule made the same error **one section after diagnosing it in §G.5** |
| [DEF-049](docs/00-governance-map/defect-register.md#def-049)(b) | Fabrication is called the cardinal fault; its **detection rate is near zero** |

**Corrected principle, now stated in three places: severity of statement may not substitute for
capability of enforcement.**

### Finding 2 — Five commitments impose their cost on somebody other than the estate

| Defect | Who pays |
|---|---|
| [DEF-037](docs/00-governance-map/defect-register.md#def-037) | Readers with cognitive disabilities — excluded so the prose stays precise |
| [DEF-039](docs/00-governance-map/defect-register.md#def-039) | Integrators, then readers downstream of a level someone else synthesised |
| [DEF-041](docs/00-governance-map/defect-register.md#def-041) | Any holder whose credential is withdrawn without a forum |
| [DEF-042](docs/00-governance-map/defect-register.md#def-042) | Every holder, in employability, for the signed limits |
| [DEF-044](docs/00-governance-map/defect-register.md#def-044) | Any learner marked at D4/D5 by the party whose position they rejected |

**In four of five the estate had called the arrangement a virtue.** This produced a new review pass
— [RB-03 Pass 4, cost incidence](docs/rubrics/rb-03-structural-review.md#14-pass-4--cost-incidence)
— whose operative question is *is the estate describing this as a virtue?*, because **the estate
cannot always avoid imposing a cost and can always stop taking credit for it.**

### Finding 3 — The estate cannot currently issue the credential it exists to issue

[B-22](docs/00-governance-map/launch-blockers.md) prohibits D4/D5 assessment without an adjudicator.
Those are the dimensions that assess **judgement rather than execution**, and the estate's claim is
that it teaches judgement. Until then it can issue **execution credentials only** — the thing it says
it is not building.

And [MX-005 §5.6](docs/corpus/mx-005-credentialing.md#56--the-unresolved-question-at-the-centre-of-this-instrument)
contains the release's most uncomfortable section: a table showing that
[RAT-22](docs/00-governance-map/open-questions-and-ratifications.md#rat-22--whether-the-estate-should-issue-credentials-at-all-rather-than-published-assessments)'s
published-assessment model **dissolves four of these problems at once**, that it is **already working
for the Contribution track**, and that it is unadopted because the decision belongs to the Curator —
who is the author. **RAT-22 was reached independently from four instruments in one release.**
MX-016 §16.6.1 accepts the sharper description: *an unwillingness to decide, documented four times.*

### Finding 4 — The corpus exceeds its author's reading capacity

[DEF-049](docs/00-governance-map/defect-register.md#def-049)(a) names **volume** as the real risk of
AI-assisted authorship — not fabrication, which AG-000 §A.5 guards, but governing instruments
produced faster than anyone can read them closely. New control: `human_read: full | partial | none`
in front matter; **an instrument at `none` cannot be cited as governing**; counts published.
**Most of this corpus would currently read `partial` at best.**

---

## The headline change in v2026.09.5

`metax.academy/about/static/` published a doctrine: *"no database, no login wall, no client-side
fetch."* The newest source document adds authentication, payment and per-user dashboards — which
makes that sentence **false**.

The resolution: the Static Principle is **partitioned, not abandoned**, and the doctrine page is
**rewritten and dated** rather than quietly contradicted.

| | Content Plane | Identity & Commerce Plane |
|---|---|---|
| Hosts | `metax.academy`, `toptech.`, `bcia.`, `academies.`, `library.`, `lexicon.`, `verify.`, every `{academy}.` | `auth.`, `pay.`, `me.` |
| State | None | Sessions, entitlements, intents, artefacts |
| JS disabled | **Renders completely and legibly** | Requires JS |
| Indexed / archived | Yes / Yes | **Never / Never** |
| Publishes claims | Yes | **No** |

> **The boundary rule:** the content plane may be *decorated* by the identity plane but never
> *depends* on it.

Governed by [`ST-19`](docs/standards/st-19-two-plane-architecture.md), and **mechanically tested**
rather than asserted: the estate builds twice, once with the identity script stubbed to throw, and
any difference in rendered content fails the build.

---

## The headline change in v2026.09.5 — a harms layer

[`HX-000`](docs/harms/hx-000-the-eighteen-structural-harms.md) states **eighteen structural
harms** in four strata. Its source declared fourteen, tabulated fourteen, and **stated eleven** —
it ended on an append-point marker after H11, with H12–H14 and §§3–5 existing only as table rows
that other written sections already linked to.

| What was done | Detail |
|---|---|
| **Wrote the three missing harms** | H12 digital amnesia, H13 exclusion by default, H14 moral deskilling — in full eight-part form, not summarised from their register rows |
| **Added four on instruction** | H15 linguistic erasure, H16 security debt, H17 revocable possession, H18 temporal compression |
| **Rejected seven, by name** | Including parasocial substitution, as the moral-panic failure mode — so that omission reads as judgement |
| **Renumbered nothing** | H1–H14 keep their identifiers permanently |

**Every harm carries eight mandatory parts**, including its **strongest counter-argument** and a
**falsifier** — the condition under which the harm should be withdrawn. A harm that cannot be
falsified is doctrine, and this corpus does not publish doctrine.

**Two companion instruments** were written because the register could not stand without them:

- [`ML-2.2`](docs/license/ml-2-2.md) — **Part H**: six absolute cores, nineteen duties. Published
  as a **draft that governs nothing**; `ML-2.1` remains the license of record.
- [`ST-22`](docs/standards/st-22-platform-and-persistence.md) — platform and persistence, the only
  **PERISHABLE** standard in the corpus, carrying the date its vendor figures were read.

> **The finding worth repeating.** Of the three harms the source named but never wrote, **H13 —
> exclusion by default — was the one most present in this estate.** A register that omits the
> harm its author is most likely to commit is not omitting at random.

---

## Current structure

```
docs/
  index.md                          ← master entry point, every instrument linked
  00-governance-map/
    precedence-and-conflict-rules.md   8-tier precedence ladder
    reconciliation-ledger.md           R-01 … R-44 in 3 parts, every conflict + reason
    open-questions-and-ratifications.md RAT-01 … RAT-18, Curator decisions only
    launch-blockers.md                 B-01 … B-16 + 10-wave publication order
    defect-register.md                 DEF-001 … DEF-018, published deliberately
    changelog.md                       every release, with reasons
  license/
    ml-2-1.md                          full consolidated licence — LICENSE OF RECORD (unsigned)
    ml-2-2.md                          new — Part H harms layer. DRAFT, governs nothing
    enforceability-two-track-table.md  §3-bis added — posture per Part H section
    designation-list.md                DL-2 — HX-000 entered as applied-for
  harms/                               NEW FAMILY
    hx-000-the-eighteen-structural-harms.md  18 harms, 4 strata, 8-part form each
  corpus/
    mx-000-charter.md                  the founding instrument
    mx-001-about-metax.md
    mx-021-payments-and-commerce.md    Riba constraints at the interface
    mx-022-identity-and-sessions.md    §22.4 SUPERSEDED — social-only auth
  standards/
    st-19-two-plane-architecture.md    §3 SUPERSEDED in one respect — hydration
    st-20-payment-integration.md       the webhook-is-truth rule
    st-21-performance-budgets.md       budgets with no override flag
    st-22-platform-and-persistence.md  new — PERISHABLE, 8 amendments, 90-day review
  design/                              from MX-DESIGN-001
    ds-01-foundations-and-tokens.md    breakpoints, type, ten gradients
    ds-02-motion-and-attention.md      four motion tiers, anti-engagement
    ds-03-responsive-components.md     component matrix, academy limits
    ds-04-academic-features.md         the twelve features, plane-placed
    ds-05-certification-surfaces.md    record / document / share card
    ds-06-error-and-empty-states.md    error, empty, degraded, analytics
sources/                               all source files, retained unedited
```

---

## Completed

- **Governance backbone** — precedence ladder, reconciliation ledger (44 entries, 3 parts), open
  questions (18), launch blockers (16), defect register (18, two closed), changelog.
- **License layer** — consolidated ML-2.1 (license of record), **ML-2.2 with Part H as a draft**,
  the two-track enforceability table including §3-bis for Part H, and the designation list at DL-2.
- **HX-000 — the eighteen structural harms.** New `harms` family. Three harms supplied that the
  source never wrote, four added on instruction, seven candidates rejected by name.
- **Charter (MX-000)** and **About MetaX (MX-001)**, both carrying the partitioned Static
  Principle.
- **MX-021 / MX-022** — correctly renumbered; MX-022 §22.4 now carries its supersession.
- **ST-19 … ST-22** — two-plane architecture (§3 superseded in one respect, published as such),
  payment integration, performance budgets, platform and persistence.
- **DS-01 … DS-06** — the complete design-system family.

**Two supersessions were published rather than edited in.** MX-022's passkey reasoning and
ST-19's "no reserved space" rule both remain legible with their replacements beside them — the
first because it is the only record of *why the estate intends to change back*, the second
because anyone who read the standard yesterday relied on it.

## Not yet implemented

| Remaining | Count |
|---|---:|
| MX-002 … MX-020 + 2 annexes | 21 |
| AG-000 … AG-012 (incl. the verbatim AG-003 kernel) | 13 |
| ST-01 … ST-18 | 18 |
| RB-01 … RB-04 | 4 |
| REG-01 … REG-08 (series data available in `sources/`) | 8 |
| BX-000 … BX-009 | 10 |
| `site/` — IA, route manifests, page specs | 13 |
| `lexicon/` — keyword register, MetaX grammar, entry standard, contested terms | 4 |
| `templates/` | 2 |
| Remaining governance-map and license companions | 12 |
| MX-023 Infrastructure & Migration + Annex A table inventory | 1 |
| HTML documentation portal | — |

**Many links in `docs/index.md` therefore resolve to files that do not exist yet.** This is
deliberate and disclosed: the index is the build plan as well as the entry point.

---

## Recommended next steps

1. **MX-023 Infrastructure & Migration** — now the most-cited missing file, referenced from
   ST-22 at seven points including the Annex A table inventory, and it **outranks ST-22 on the
   precedence ladder**, so the standard currently defers to a document that does not exist.
2. **ST-01 and ST-02** — identifier grammar and front-matter schema are cited by nearly every
   other instrument. ST-01's immortality rule has now been applied four times and cited from
   eleven files while remaining unwritten.
3. **REG-01 Series Registry** — the 52-row source table is already in
   `sources/00_METAX_COURSE_SERIES_REGISTRY_v2026.08.28.md`, and several instruments depend on it
   for computed counts.
4. **AG-000 and AG-009** — the absolute-refusal set is referenced from the Charter, both new
   corpus instruments, and now from HX-000's authorship rule.
5. **The lexicon keyword register** — central to the requirement that every keyword resolve to a
   detailed file.
6. **The HTML portal**, last, so it renders a corpus that is already complete.

---

## Honest state of this corpus

Nothing here is publishable yet, and the reasons are published rather than managed:

- **The licence is unsigned.** The Charter derives authority from it, so the Charter states its own
  authority as *pending*.
- **The ethics veto has no named holder**, and it is a power deliberately placed beyond the Curator.
- **SENTINEL does not run.** Every "enforced mechanically" claim currently describes an intention —
  the single most consequential defect in the corpus ([DEF-001](docs/00-governance-map/defect-register.md#def-001)).
- **No Arabic editions exist.** Parity is a standing target, never described as a present state.
- **Riba compliance is structural, not reviewed.** Review is required in three domains and none has
  happened; no page asserts compliance as a conclusion.
- **Book 9 chapters 2–9 are missing from the source itself** — a gap no drafting can close.
- **The harms layer does not bind anyone.** ML-2.2 is an unadopted draft and ML-2.1 has no Part H.
  Every "Obligation this creates" in HX-000 states what *would* be required on adoption.
- **Three open questions now wait on qualified religious review** — RAT-12 (Riba), RAT-16
  (*ḥifẓ al-ʿaql*), RAT-18 (four ethical mappings) — **and none has a named reviewer.** The
  corpus has accumulated religious commitments faster than the competence to check them, and
  says so on the pages that carry them.
- **The estate commits harms it publishes.** HX-000 §5 states that this estate commits **H13**
  (exclusion by default) and **H15** (linguistic erasure) — an identity path and a payment rail
  that both serve Arabic-speaking readers worse than English-speaking ones
  ([B-16](docs/00-governance-map/launch-blockers.md), [DEF-018](docs/00-governance-map/defect-register.md)).
- **The scaling claim was false as built.** Roughly 36 further series, not thousands
  ([DEF-017](docs/00-governance-map/defect-register.md)). The architecture is fine; the sentence
  was not, and deleting the sentence is required immediately while re-architecting is optional.

Placeholders such as `[STEWARD NAME / ORGANIZATION]`, `[REGISTRY URL]`, `[FPR]` and `[VERIFY]` are
**left visible on purpose**. Under `AG-000 §A.5` a plausible placeholder is a fabrication, and
fabrication is the cardinal fault.

---

## Data models and storage

**None.** This is a static documentation corpus: Markdown files with YAML front matter, in Git. No
database, no table schema, no API. The front-matter schema (`prevailing_text`, `evidence_class`,
`domain_tags`, `decay class`, `bcia_layer`, `tier_range`, …) is specified in `ST-02` and is the only
structured data contract in the repository.

## Public URLs

None. Nothing is deployed, and publication is blocked by
[`launch-blockers.md`](docs/00-governance-map/launch-blockers.md). The intended estate is
`metax.academy` and the subdomains listed above.

---

*Curated by Maher. Where this corpus is wrong, the correction is published — not the argument that
it was never wrong.*
