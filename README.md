# The MetaX Universe — Canonical Corpus

**Release v2026.10.1 · Curated by Maher · Licensed under [ML-2.3](docs/license/ml-2-3.md)**

A governance and documentation estate written to be read by **both humans and AI systems**. Every
instrument is a Markdown file at a permanent path, with front matter, a version, a stated
authority, and relative links from every identifier to the document that defines it.

> **Start here:** [`docs/index.md`](docs/index.md) is the canonical entry point and the
> authoritative list of every instrument.
> **Resuming work on this corpus?** Read [`docs/00-governance-map/task-ledger.md`](docs/00-governance-map/task-ledger.md) first.

---

## Review and completion pass (2026-10-08)

**Read [GM-17, the v2027.1 corpus review](docs/00-governance-map/corpus-review-v2027.1.md) first.** It lists 56 missing
documents (M-01…M-56), 54 conflicts and contradictions (X-01…X-116) and 29 proposed edits (A-01…A-29). Its **§8** maps what
this pass wrote.

**Written this pass (all drafts, `human_read: none`):**
- **Licence:**
  - [CF-1 Compliance File](docs/license/cf-1-compliance-file-template.md)
  - [ML-B-1.0 Schedules B-1/B-2](docs/license/ml-b-1-0-schedules-b1-b2.md)
  - [CPF-1 Comment Period](docs/license/cpf-1-comment-period-publication-format.md)
  - [GM-20 Decision Records](docs/license/decision-record-register.md)
  - [ML-2.0 retained](docs/license/ml-2-0.md)
- **Records:**
  - [GM-18 Anomaly Register](docs/00-governance-map/anomaly-register.md)
  - [GM-19 Continuity Register](docs/00-governance-map/continuity-register.md)
  - [REG-13 Decay Calendar](docs/registries/reg-13-decay-calendar.md)
  - [REG-14 programme series](docs/registries/reg-14-programme-series-registry.md)
  - corrections C-17 and C-18
- **Programmes:** MLT-01…MLT-09 seven-part charters (`docs/metax/programs/`)
- **Harms:** seven stratum pages (`docs/harms/strata/`)
- **Specs:**
  - [ST-34 machine forms](docs/standards/st-34-licence-and-register-machine-forms.md)
  - [SITE-08 Decision Queue](docs/site/site-08-decision-queue.md)
  - [PR-1 pre-registration](docs/templates/pr-1-preregistration-form.md)
  - [LEX-06 term entries](docs/lexicon/lex-06-term-entries-governance-set.md)
- **Registers:** DEF-054…067 · RAT-39…44 · V-22 · B-26 · GM-13 §4b (next free numbers)

**Most important open items (Curator):**
- Signing (B-01).
- Ethics-veto holder (M-03).
- **The refusals conflict between MX-000 §0.4 and MX-014 §2 (RAT-44).**
- MLT-05's method, which MX-014 forbids (RAT-40).
- The subdomain-vs-one-origin model (RAT-28(g)).
- Approval of the GM-17 §5 A-items. No canonical text has been edited.

**Cannot be written by an agent:** a key, signatures, mirrors, the ethics reviewer, a successor's acceptance, a dissent
receiver, counsel review, Arabic prevailing text, Book 9, and the premise register. **Needs a build:** the JSON surfaces,
the validator, the Decision Queue and the site pages (staged, never thin).

---

## v2027.1 source intake (2026-09-30)

**Read [GM-16](docs/00-governance-map/source-intake-v2027-1.md) first.** It lists 17 decisions,
answers the bundle's 8 review questions, and maps what the new files answer.

- **New, all drafts:** HX-000 v2027.1 (28 harms) · CON-002 · ML-2.4 · ML-B-1.0 · BX-018 substrate register · MLT-000 (nine programmes) · SITE-06 nav · SITE-07 design and reader · BHS-2027-001 draft Statement.
- **Key findings:**
  - The folder held two incompatible "v2027.1" releases. The one that matches ML-2.3 was adopted.
  - The estate's own HX-000 v2026.10.1 disagreed with ML-2.3 on most harm identities (DEF-040).
  - The claimed signatures are future-dated, so **nothing is signed** (B-01 open).
  - ML-2.4 as drafted would overwrite ML-2.3 §H.31, so it was renumbered (B-25).
- **Answered:** RAT-14 (ML-2.2 skipped), the meaning of BCIA (MLT-09).
- **Waiting on the Curator:** RAT-29…38, B-25, signing.

---

## Release v2026.10.2 — restoration pass (2026-09-26)

**Read [GM-15, the corpus review](docs/00-governance-map/corpus-review-v2026.10.2.md) first.** It lists
13 conflicts, 15 proposed adjustments and 10 refinements, with severity and owner.

| What | Where |
|---|---|
| Inventory of missing documents, plus the agent completion prompt | [GM-14](docs/00-governance-map/completion-programme.md) §2 and §4 |
| Record of 40 reused identifiers and their refuge numbers | [GM-13](docs/00-governance-map/identifier-reallocation-record.md) |
| New instruments | MX-025…029 · AG-013…022 · ST-25…33 · RB-06/07 · REG-09…12 · **BX-010…017 (BCIA research programme restored)** · LEX-04/05 · SITE-05 · License ops set |
| Pointer stubs at legacy paths | 46 (plus 2 licence pointers). Every GM-14 path now resolves |
| Register appends | DEF-036…039 · RAT-24…28 · R-57…60 · V-14…17 · changelog · task ledger §10 · document index §10 · index §14 |

**Entry URIs.** Everything is relative to `docs/`:
- `index.md` (architecture; see §14 for the new instruments)
- `00-governance-map/*` (records)
- `license/`, `corpus/`, `agents/`, `standards/`, `rubrics/`, `registries/`, `bcia/`, `lexicon/`, `site/`, `design/`, `harms/`
- The planned public routes are in `site/route-manifest.md`, e.g. `/metax/bcia/status/`

**Not yet done:**
- The A-items in GM-15 §4, which edit canonical text and need Curator approval
- A human L-1 source pass
- A Curator ruling on RAT-25 and RAT-28
- A link checker and front-matter validator
- Arabic mirror texts
- Any HTML site build

**Data storage:** Markdown files in git only. No tables and no backend.

---

## Project goals

1. **Governance that can be audited.** Precedence is decided by one document; conflicts are
   defects to be filed, not matters for interpretation.
2. **Claims that can be falsified.** Every substantive claim states what evidence would withdraw
   it. A register whose entries are never narrowed is a doctrine.
3. **A record that cannot be quietly improved.** Superseded text is retained permanently;
   corrections add records rather than replacing them.
4. **Machine citability.** The corpus is built to be read, quoted and checked by AI systems, which
   is why paths are permanent and every keyword links to its defining instrument.

---

## What is completed

### The license layer
- **[ML-2.3](docs/license/ml-2-3.md)** — the governing instrument, published with **Part H**: a
  register of **twenty-five structural harms** made operative, a four-role allocation
  (§H.1-bis), a four-tier **Scale Gate** (§H.2-bis), the **condition/covenant split** (§F.4), and
  **eight bounded absolutes** (§H.3(a)) whose breach terminates the grant.
- [ML-2.1](docs/license/ml-2-1.md) — published predecessor, retained permanently.

### Governance map
| Document | State |
|---|---|
| [Task Ledger](docs/00-governance-map/task-ledger.md) | Durable work state, so it survives context loss |
| [Corrections Log](docs/00-governance-map/corrections-log.md) | **16 corrections** — nine found by reading the live code, four by the Curator; carries the three-method taxonomy |
| [Document Index](docs/00-governance-map/document-index.md) | Every instrument with its **existence state**; the estate's own count of its dangling references |
| [Machine Reading Contract](docs/00-governance-map/machine-reading-contract.md) | Five conditions on a machine reader, six signals owed by the corpus — **three currently delivered** |
| [Verification Log](docs/00-governance-map/verification-log.md) | 13 `[VERIFY]` claims with ages — **none ever closed** |
| [Archive Register](docs/00-governance-map/archive-register.md) | Superseded text; **two texts already unretrievable**; Class D (withdrawn duties) is **empty** |
| [Reconciliation Ledger](docs/00-governance-map/reconciliation-ledger.md) | **56 entries in four parts** |
| [Defect Register](docs/00-governance-map/defect-register.md) | **34 defects**, published deliberately; one closed structurally |
| [Launch Blockers](docs/00-governance-map/launch-blockers.md) | B-01…B-20 + publication waves 0–10 |
| [Open Questions](docs/00-governance-map/open-questions-and-ratifications.md) | RAT-01…RAT-23, none closed |
| [Changelog](docs/00-governance-map/changelog.md) | Records **reasons**, not diffs |
| [Precedence Rules](docs/00-governance-map/precedence-and-conflict-rules.md) | The precedence ladder |

### Design system
- **[DS-00 As-Built Token Layer](docs/design/ds-00-as-built-token-layer.md)** — **governing.**
  Read directly out of the live `css/style.css`: cosmic-dark single theme, four gradients, two
  typefaces, the page skeleton contract, and the five-tier motion hierarchy.
- DS-01…DS-06 — retained; DS-01's palette and gradient sections are **superseded in part**.

### The site layer — new in v2026.10.1

The estate is **one origin with directory routes**, not eight content subdomains. Four
instruments, and the first discharges a task blocked since the first day of this work.

| Id | Document | What it fixes |
|---|---|---|
| **SITE-01** | [The Route Manifest](docs/site/route-manifest.md) | 9 pillars, 45 group hubs, 266 leaves, 321 English routes, the tier contract and the census. **Discharges task A-09.** |
| **SITE-02** | [The Page Contract](docs/site/page-contract.md) | The skeleton, four required components, **twenty acceptance criteria** a page can fail |
| **SITE-03** | [Routing Law](docs/site/routing-law.md) | Seven conditions for a well-formed address; the **append-only** redirect record |
| **SITE-04** | [The Demo Notice](docs/site/demo-notice.md) | Audience-tier-1 statement of what is real and what is scaffolding |
| **ST-24** | [Page Prose Standard](docs/standards/st-24-page-prose-standard.md) | The eight-part recipe, the three registers (micro/meta/macro), the variation rule |
| **DS-07** | [Navigation Geometry](docs/design/ds-07-navigation-geometry.md) | Nine pillars, fluid `clamp()` nav, the 1000→**1180px** breakpoint |

### The affiliate system — designed from scratch

**[ST-23](docs/standards/st-23-affiliate-and-referral.md).** The Curator asked for an affiliate
system "if missed." It was missed — **no supplied source contains one in any form**, across
nineteen documents read in full. ST-23 is therefore the only instrument in this corpus with no
upstream source, and it is marked as such in its own front matter under ML-2.3 §H.19.

Four cumulative elements: disclosed at the point of influence · paid once on a completed
enrolment · fixed at a published rate · severable without penalty. Six schema columns are
**forbidden** so that recurring commissions, two-tier structures, leaderboards and cookie
attribution are *unrepresentable* rather than merely disallowed. It accepts **lower attribution
accuracy** as the price of not tracking readers, and says so.

### The compliance and governance layer

Part H's machinery, the estate's own assessment against it, and the standards the corpus had been
citing without holding:

| Instrument | What it does |
|---|---|
| [Part H Statement](docs/license/part-h-statement.md) | Schedule 1 form **and** the estate's own — **NOT YET ISSUED**, with §5 stating why |
| [Scale Gate](docs/license/scale-gate.md) | Four tiers, five qualitative tests; the **absolutes bind at Tier 0** |
| [HX-001](docs/harms/hx-001-harm-audit-rubric.md) | Five dimensions, 25 tuples, the §H.7 counterproductivity test — **no total score** |
| [HX-002](docs/harms/hx-002-harm-instrument-map.md) | Every harm mapped to its answering instrument — and **three harms the estate commits** |
| [RB-05](docs/rubrics/rb-05-harm-review-gate.md) | Six checks, three outcomes, **no pass**; the estate's own work returns RETURNED |
| [MX-023](docs/corpus/mx-023-attention-and-human-sovereignty.md) · [MX-024](docs/corpus/mx-024-infrastructure-and-migration.md) | Six attention refusals (**two violated**); four data tiers and the 80% tripwire |
| [ST-22](docs/standards/st-22-platform-and-persistence.md) · [ST-13](docs/standards/st-13-static-build-and-sentinel.md) | Nine forbidden schema columns; five SENTINEL check families — **none running** |
| [ST-01](docs/standards/st-01-identifier-and-url-grammar.md) · [ST-02](docs/standards/st-02-front-matter-schema.md) · [ST-04](docs/standards/st-04-falsifiability-and-claim-cards.md) · [ST-05](docs/standards/st-05-decay-and-review-intervals.md) · [ST-06](docs/standards/st-06-objections-standard.md) · [ST-07](docs/standards/st-07-evidence-and-verify.md) | Identifiers, front matter, falsifiers, decay, objections, evidence |
| [MX-007](docs/corpus/mx-007-ai-use-and-disclosure.md) … [MX-016](docs/corpus/mx-016-appeals-and-due-process.md) | AI disclosure, moderation, advertising, accessibility, licensing, records, research ethics, succession, appeals |

### The harms register (in progress)
- [HX-000](docs/harms/hx-000-structural-harms.md) — harms H1–H11 complete in full eight-part form
  (thesis · mechanism · evidence · strongest counter-argument · reply · ethical mapping ·
  **falsifier** · obligation created). **Re-version to 25 harms is the largest remaining task.**

---

## Functional entry URIs

This repository is a **Markdown corpus**; there is no build system or server yet. Paths are the
functional entry points.

| Path | Contents |
|---|---|
| `docs/index.md` | Canonical entry point; every instrument, by family |
| `docs/license/` | ML-2.3, ML-2.1, and the license companions |
| `docs/harms/` | HX-000 register (+ HX-001, HX-002 pending) |
| `docs/00-governance-map/` | Precedence, ledgers, registers, changelog, task ledger |
| `docs/corpus/` | MX-000…MX-024 instruments |
| `docs/design/` | DS-00…DS-06 |
| `docs/standards/` | ST-01…ST-24 |
| `docs/rubrics/` | RB-01…RB-05 |
| `docs/site/` | **SITE-01…SITE-04** — route manifest, page contract, routing law, demo notice |
| `docs/registries/`, `docs/bcia/`, `docs/lexicon/` | Registries, BCIA program, lexicon |
| `sources/` | All 20 uploaded source documents, retained verbatim and read-only |

**Planned public URLs** (not yet deployed). **Corrected in v2026.10.1:** the estate is *one
origin with directory routes*, not eight content subdomains — the earlier list here described
hostnames that do not exist.

- **Content plane, one origin:** `metax.academy` with nine pillar hubs — `/toptech/`, `/method/`,
  `/ascent/`, `/metax/`, `/academies/`, `/credentials/`, `/library/`, `/license/`, `/about/` —
  plus `/search/`, `/404` and an `/ar/` mirror at every path. 321 English routes, enumerated in
  [SITE-01](docs/site/route-manifest.md).
- **Identity and commerce plane, off-manifest:** `auth.metax.academy/authorize`,
  `pay.metax.academy/checkout/{sku}`, `me.metax.academy`, `verify.metax.academy/c/{id}/`,
  `hooks.metax.academy/v1/*`, and `{slug}.metax.academy` for chartered academies.

---

## Data models and storage

**None in use.** This is a static Markdown corpus: no tables are defined, no database is
provisioned, and no access rules are set. Structured data lives in the documents' own front
matter, whose schema is defined by ST-02:

```yaml
doc_id, title_en, title_ar, family, version, status, authority,
prevailing_text, audience_tier, depth, evidence_class,
review_interval_months, curator, license, designated,
last_reviewed, domain_tags, ai_disclosure_url, hreflang
```

Evidence classes are `durable` / `semi-durable` / `perishable`, each with a review interval. The
architecture source specifies a future four-tier persistence model (build artefacts → Workers KV
config → D1 → IndexedDB cache) across six D1 databases, documented in ST-22 — **not yet built**.

---

## Not yet implemented

**Blocking, and stated on the instruments' own faces rather than hidden:**

| Item | Reference |
|---|---|
| ML-2.3 cites an **ML-2.2 that has never been published**; §E.3's transition has no referent | [RAT-14](docs/00-governance-map/open-questions-and-ratifications.md#rat-14--does-ml-22-exist) |
| ML-2.3 incorporates **HX-000 v2026.10.1**, which does not yet exist | DEF-021 |
| ML-2.3 is **not reviewed by counsel** in any jurisdiction | [RAT-18](docs/00-governance-map/open-questions-and-ratifications.md) |
| The estate has **no Part H Statement**, while ad networks run on the content plane | [RAT-15](docs/00-governance-map/open-questions-and-ratifications.md#rat-15--will-the-estate-publish-its-own-harms-as-unremedied) · B-19 |
| **No `prefers-reduced-motion` block**; nine infinite animations | DEF-016 · B-16 |
| The site **does not render without JavaScript**, contrary to its own law | DEF-018 |
| Detail pages are invisible to non-JS crawlers — in a corpus built to be cited by machines | DEF-017 |

| The estate is a **demo** and no page says so; no provenance strip, no demo-notice page built | DEF-025 · B-20 |
| **MacroLifeTech** is still misspelt in the live build, `data.js`, the meta description and the search index | DEF-023 |
| Nine live-code claims published **without provenance of purpose** (`demo`/`staging`/`production`) | DEF-024 |
| Touch targets below the 44px floor — an accessibility claim **a ruler falsifies** | DEF-022 |

**Documents required but not yet written:** HX-000 re-version to v2026.10.1 (25 harms), HX-001
audit rubric, HX-002 harm→instrument map, MetaX's own Part H Statement, the Scale Gate worksheet,
license version history, MX-023, MX-024, ST-22, RB-05, and the Part H rows of the enforceability
table.

**And 321 pages.** The site layer now specifies the estate completely and **not one page has been
generated.** At a 1200-word floor that is ≈385,000 English words plus an Arabic mirror of equal
standing. The order is deliberate — a structure can be criticised cheaply before it is full — and
the volume is an open question, not a plan
([RAT-21](docs/00-governance-map/open-questions-and-ratifications.md#rat-21)).

**Deferred by the Curator's own ordering:** MX-002…MX-020, AG-000…AG-012, ST-01…ST-18,
REG-01…REG-08, BX-000…BX-009, RB-01…RB-04, `lexicon/`, `templates/`, and the HTML documentation
portal.

---

## Recommended next steps

**First, the finding that outranks everything else.**

**[DEF-031](docs/00-governance-map/defect-register.md#def-031) — four instruments specify processes
the estate cannot perform, all for one reason: the estate has one participant.** MX-016's appeals
process has an unstaffable middle stage. MX-015's succession has three unfilled roles. MX-014's
research exclusions have no independent ethics veto. ST-06's strongest objection to the estate is
filed `open` because no external objector exists.

The remedy is two actions, neither difficult, both open since the first release: **name the role
holders** ([RAT-04](docs/00-governance-map/open-questions-and-ratifications.md#rat-04--name-the-ethics-reviewer-and-the-successors))
and **sign the licence** ([B-01](docs/00-governance-map/launch-blockers.md)). This outranks the ad
slots, because the ad slots are one decision and this is four instruments that cannot do what they
say — including the appeals process.

**Then the two questions that decay fastest.**

1. **[RAT-19](docs/00-governance-map/open-questions-and-ratifications.md#rat-19) — is `Method` a
   ninth pillar?** It was proposed by an agent, which disclosed it as its own addition. The nine
   are adopted provisionally because a route manifest is unusable without a count. **The cost of
   folding it is bounded only while the pages are unwritten** — today it is 46 re-parented routes
   and a breakpoint revert; at a hundred written pages it is a migration.
2. **[RAT-15](docs/00-governance-map/open-questions-and-ratifications.md#rat-15) — the ad slots.**
   Because the site is a demo there is now a **clean window to remove them before** the Part H
   Statement is ever published, which would let it read *remedied* on HX-01 and HX-04 rather than
   *unremedied*. The question has changed from *how do we confess this* to *do we commit it at
   all*, and that window closes on publication.

**Then the substantive work.**

3. **Re-version HX-000 to v2026.10.1** — the largest single remaining task, and the dangling
   reference on the face of the Tier 1 instrument (ML-2.3 §A.10, DEF-021).
4. **Resolve RAT-14** (does ML-2.2 exist?) — it gates every `license:` front-matter field.
   Recommendation on file: do **not** draft a retrospective 2.2; that would be manufacturing a
   record inside the instrument that defines *Ṣidq*.
5. **Ship the `prefers-reduced-motion` block and the 44px targets** — CSS measured in minutes,
   standing between the corpus and an honest accessibility claim.
6. **Build `/about/universe/demo-notice/` and the `.mx-demo` strip** — [B-20](docs/00-governance-map/launch-blockers.md)
   gates wave 1, which publishes the Charter and the License.
7. Then generate the estate pillar by pillar, with unwritten routes **absent rather than thin**.

**The cheapest four items in the whole backlog**, each minutes of work, all deferred at the moment
they were cheapest ([DEF-030](docs/00-governance-map/defect-register.md#def-030)): read the
provider's pricing page (V-07), `rsync` the static estate to a second host and serve it (V-13), run
a link checker over `docs/` (V-10), and measure nine Arabic RTL nav labels at 1180px (V-08). The
second of those tests the property **every durability claim in this corpus rests on**, and it has
never been exercised.

---

## Working conventions

- **Numbers are immortal** from first assignment (ST-01 Rule 2). A colliding request takes the
  next free number and the collision is recorded in the ledger, never silently reassigned.
- **No silent edits.** Superseded text is retained with a non-governing banner
  ([MX-000 §0.8](docs/corpus/mx-000-charter.md)).
- **Summaries never govern** (GM-01 §3).
- **Nothing is marked done on the strength of a tool call that reported success** — only when the
  artefact has been read back. One interrupted edit in this project silently did not land, and the
  Task Ledger is why it was caught rather than assumed.
- **A defect register with no entries would mean nobody looked.**
- **Three error-finding methods, three blind spots.** Cross-source reconciliation cannot see what
  the corpus is uniformly wrong about. Reading the live artefact cannot see what the artefact is
  *for*. The Curator's statement of intent cannot see whether anything was implemented. Each
  method's blind spot is another's specialty — and **only two of the three can be automated.**

---

*Founded, built and curated by Maher. Licensed under the Maher License, Version 2.3 —
`SPDX-License-Identifier: LicenseRef-ML-2.3`. The absolutes at §H.3(a) apply at every scale,
including private use.*
