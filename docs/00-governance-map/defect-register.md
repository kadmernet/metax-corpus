---
doc_id: "GM-09"
title_en: "Defect Register"
title_ar: "سجل العيوب"
family: "governance-map"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 5
evidence_class: "perishable"
review_interval_months: 3
curator: "Maher"
license: "ML-2.3 · Work of Foundational Character"
last_reviewed: "2026-10-01"
hreflang: "en, ar"
---

# Defect Register

Known shortfalls in the MetaX estate, each with an owner and a target date. **This register is
published with the site, deliberately** — it is not an internal tracker that leaked.

**Why a public register.** [Charter §0.3](../corpus/mx-000-charter.md#03-shared-dna) makes
correctability one of four Shared DNA properties, and §0.5.2 places the correction obligation
beyond the Curator: he cannot decline a valid correction, cannot delete a published defect, and
cannot remove a superseded claim from the record. A defect register that only the author can see
satisfies none of that.

**Defect vs blocker vs open question.** A **defect** is a published shortfall that does not make
publication dishonest — the site ships with it visible. A
[**blocker**](launch-blockers.md) makes publication dishonest. An
[**open question**](open-questions-and-ratifications.md) needs the Curator's decision.

**Anyone may file.** Public submission is at `library.metax.academy/corrections/`
([DS-04 feature 11](../design/ds-04-academic-features.md#11--the-correction-bounty)), and
**rejected submissions are published with reasons** — which is what stops the queue becoming a
black box.

---

## Open defects

| Id | Defect | Class | Owner | Target |
|---|---|---|---|---|
| [DEF-001](#def-001) | SENTINEL is a specification, not a running pipeline | Build integrity | Maher / build | Wave 1 |
| [DEF-002](#def-002) | No Arabic editions of any instrument exist | Translation divergence | Maher | Wave 2 |
| [DEF-003](#def-003) | Accessibility conformance committed to but never tested | Accessibility | Maher | Wave 1 |
| [DEF-004](#def-004) | Book 9 chapters 2–9 absent from the source itself | Source gap | Maher | Unset — see [RAT-05](open-questions-and-ratifications.md) |
| [DEF-005](#def-005) | Books 7, 8, 10 un-ingested | Source gap | Maher | Wave 2 |
| [DEF-006](#def-006) | BCIA Gate 3 currently unresolvable | Research state | Maher | Unset, honestly |
| [DEF-007](#def-007) | BSN / LPN / AMN referenced but never defined | Notation inconsistency | Maher | Frozen pending [RAT-03](open-questions-and-ratifications.md) |
| [DEF-008](#def-008) | `domain_tags` wrongly populated with rubric dimensions in v2026.08.12 front matter | Notation inconsistency | Build | Wave 1 |
| [DEF-009](#def-009) | Dated claims in the book corpus checkable but unchecked | Stale claim | VERIFIER + human gate | Wave 2 |
| [DEF-010](#def-010) | Governing instruments unreviewed by counsel | Legal | Maher + counsel | Wave 1 |
| [DEF-011](#def-011) | MX-DESIGN-001 describes content-plane hosts as "fully static" while requiring a cookie-setting callback | Factual error in a source | Editorial — **closed** | Closed 2026-08-30 |
| [DEF-012](#def-012) | Scenario assessment has no plane-compliant design | Architecture | Maher | Blocked on [RAT-11](open-questions-and-ratifications.md#rat-11--how-the-scenario-assessment-resolves-against-the-plane-boundary) |
| [DEF-013](#def-013) | Riba compliance asserted structurally, unreviewed substantively | Governance | Maher + 3 reviewers | Wave 9 |
| [DEF-014](#def-014) | Single crypto payment rail excludes part of the target audience | Access | Maher | Wave 9 |
| [DEF-015](#def-015) | Island failure transparency untested | Build integrity | Build | Wave 8 |
| [DEF-016](#def-016) | No `prefers-reduced-motion` block; nine infinite animations run regardless of user preference | Accessibility | Build | **Immediate — also [B-16](launch-blockers.md)** |
| [DEF-017](#def-017) | Detail pages are query-parameter routes with no server-rendered content; invisible to non-JS crawlers | Machine citability | Maher / build | Blocked on [RAT-17](open-questions-and-ratifications.md#rat-17--pre-render-or-remain-javascript-only) |
| [DEF-018](#def-018) | The site does not render with JavaScript disabled, contrary to its own stated law | Build integrity | Maher / build | Blocked on [RAT-17](open-questions-and-ratifications.md#rat-17--pre-render-or-remain-javascript-only) |
| [DEF-019](#def-019) | Behavioural ad networks live on the content plane, contradicting MX-009 and engaging HX-01 / HX-04 | Governance | Maher | Blocked on [RAT-15](open-questions-and-ratifications.md#rat-15--will-the-estate-publish-its-own-harms-as-unremedied) |
| [DEF-020](#def-020) | DS-01 through DS-06 describe a design system the live code contradicts | Factual error in an instrument | Editorial | Wave 1 |
| [DEF-021](#def-021) | ML-2.3 references ML-2.2, which does not exist; HX-000 v2026.10.1 incorporated but not yet written | Dangling reference in a governing instrument | Maher | Blocked on [RAT-14](open-questions-and-ratifications.md#rat-14--does-ml-22-exist) |
| [DEF-022](#def-022) | Touch targets below the 44px floor (`.nav-toggle` 42px, `.btn` 14px×26px) | Accessibility | Build | Wave 1 |
| [DEF-023](#def-023) | The name **MacroLifeTach** is a misspelling of **MacroLifeTech**, propagated estate-wide including into a published anchor | Factual error in an instrument | Editorial | **Immediate — partially discharged** |
| [DEF-024](#def-024) | Nine live-code claims published without recording whether their subject was demo, staging or production | Evidence-class error | Editorial / build | Wave 1 |
| [DEF-025](#def-025) | No page carries the demo provenance strip; `/about/universe/demo-notice/` does not exist | Honesty of publication | Build | **Immediate — also [B-20](launch-blockers.md)** |
| [DEF-026](#def-026) | Relative asset paths break at route depth ≥1 under directory routing | Build integrity | Build | Before first depth‑1 page ships |
| [DEF-027](#def-027) | `SEARCH_INDEX` is hand-written and drifts from the route set by construction | Build integrity | Build | Wave 1 |
| [DEF-028](#def-028) | "Three pillars" published as a navigation fact while navigation carries nine | Factual error in an instrument | Editorial | Blocked on [RAT-19](open-questions-and-ratifications.md#rat-19) |
| [DEF-029](#def-029) | **The archive rule predates the archive** — §0.8 has been cited as authority since the corpus began; its destination was created in the third release, so pre-October supersessions are retained only incidentally | Record integrity | Editorial | Coverage begins 2026-10-01; two texts already unretrievable |
| [DEF-030](#def-030) | Thirteen `[VERIFY]` claims open, **none ever closed**, four of them checkable in minutes | Verification practice | Build / Curator | Next release |
| [DEF-031](#def-031) | **Four instruments specify processes the estate cannot perform**, all for one reason: the estate has one participant | Governance capacity | Maher | Blocked on [RAT-04](open-questions-and-ratifications.md#rat-04--name-the-ethics-reviewer-and-the-successors) + [B-01](launch-blockers.md) |
| [DEF-2026-041](#def-2026-041) | Cloudflare Pages 20,000-file ceiling | Capacity | Build | **Re-characterised — see entry** |
| [DEF-2026-042](#def-2026-042) | Query-parameter detail route invisible without JavaScript | Machine citability | — | **Resolved structurally — see entry** |
| [DEF-2026-043](#def-2026-043) | Six page classes are thin by nature and exempt from the 1200-word floor | Declared exemption | Editorial | Standing |

---

### DEF-001

**Every mechanical-enforcement claim in this corpus currently describes an intention.**
[ST-13](../standards/st-13-static-build-and-sentinel.md) and
[ST-21](../standards/st-21-performance-budgets.md) specify front-matter validation, computed
counts, dangling-link detection, falsifier presence, single-source drift checks, budget gates and
build-failure-over-placeholder. None of it runs.

This is the estate's most consequential defect because
[MX-006 §6.3](../corpus/mx-006-editorial-and-evidence.md#63-falsifiability) states that
falsifiability is enforced mechanically *"because editorial enforcement of a discipline the editor
also authors is not enforcement."* Until the pipeline runs, that sentence is the strongest claim in
the corpus and the least supported. Also
[B-06](launch-blockers.md#b-06--the-build-cannot-yet-enforce-its-own-rules--hard-blocker).

### DEF-002

Arabic is described as *authoritative*, not as a translation target
([MX-020](../corpus/mx-020-language-authority.md)). No Arabic edition of any instrument exists.
Parity is stated as a standing target and never as a present state; no toggle resolves silently to
a homepage. Also [B-09](launch-blockers.md#b-09--arabic-parity-is-claimed-but-not-built--soft-blocker).

### DEF-003

WCAG 2.2 AA is committed to across all properties
([MX-010](../corpus/mx-010-accessibility.md)). No test matrix has been run. The defect closes with
the **first** audit and its published gap list, not with full conformance — publishing the gaps is
the compliant state.

### DEF-004

Book 9 chapters 2–9 were never provided in the upload. Marked `[GAP IN SOURCE]` in
[REG-03](../registries/reg-03-book-registry.md). **No amount of drafting closes this** — it is a
source gap, and only Maher can supply the text. Any Ascent rung depending on those chapters is
`PREVIEW` at best and may not claim chapter-level fidelity.

### DEF-005

Book 7 chapters 3–12 and Books 8 and 10 exist but are un-ingested. Marked
`[PENDING INGESTION]`. Distinguished from DEF-004 on the 404 surface, because "not ingested yet"
and "the source is incomplete" are different facts about MetaX
([DS-06 §6.2](../design/ds-06-error-and-empty-states.md#62-the-404-routes-intelligently)).

### DEF-006

[Gate 3](../bcia/bx-003-remediation-gates.md) is recorded as currently unresolvable. The target is
deliberately unset: a target date on a gate whose closure condition is unknown would be a
fabricated schedule. Published as unresolvable rather than as pending.

### DEF-007

BSN, LPN and AMN are referenced throughout the BCIA sources and defined nowhere. The triad is
[frozen](../bcia/bx-005-notation-freeze.md) — referenced where the sources reference it, never
taught as settled. Blocked on [RAT-03](open-questions-and-ratifications.md).

### DEF-008

v2026.08.12 front matter populated `domain_tags: [D1..D5]` with **rubric dimensions**, conflating
three unrelated D-prefixed vocabularies: the frozen D1–D5 assessment rubric, the retired D1–D10
domain tags, and Branch D. Resolved editorially at
[R-04](reconciliation-ledger.md#r-04--the-d-prefix-collision); the defect remains open until the
migration runs across all affected files.

### DEF-009

Landauer 1961, Shannon 1937, EDVAC 1945, Bell Labs 1947, the Setun era, He Jiankui 2018, a 2024
Neuralink matter — all became *checkable* on ingestion and none has been checked. Each carries
`[VERIFY]` and is counted in [Verification Log](verification-log.md). The banned
DishBrain-versus-DeepMind comparison is **not** awaiting verification; it is prohibited outright
([MX-006 §6.6](../corpus/mx-006-editorial-and-evidence.md#66-banned-comparisons)) because it is not
comparable at any level of verification.

### DEF-010

MX-002, MX-003, MX-004, MX-018, MX-021, MX-022 and the ML-2.1 enforceability assertions are
drafting work product. Governing law, forum and the liability cap are unset. Also
[B-05](launch-blockers.md#b-05--counsel-review-of-the-legal-instruments--hard-blocker).

### DEF-011 — closed

**Filed against the source's wording, not its architecture.**
[MX-DESIGN-001](../../sources/MetaX.Academy_UI-UX_and_Design_System_Documentation.md) Part 0
describes content-plane hosts as "fully static" while Part 4 requires each host to set its own
host-scoped session cookie — which a purely static host cannot do.

The architecture is sound and the wildcard-cookie refusal is correct: it is what stops one
compromised academy subdomain from harvesting estate-wide sessions. Only the description was
wrong.

**Closed 2026-08-30** by adopting the precise formulation: every content-plane *page* is static;
every content-plane *host* additionally exposes exactly one non-static route, `/auth/callback`,
which serves no content and renders no page
([ST-19 §4](../standards/st-19-two-plane-architecture.md#4-the-callback-route),
[R-32](reconciliation-ledger.md#r-32--an-unstated-consequence-the-content-plane-needs-an-edge-callback)).

Retained in this register rather than deleted, per
[Charter §0.5.2](../corpus/mx-000-charter.md#2-the-correction-obligation).

### DEF-012

The sixth beat of the lesson arc has no design that satisfies both assessment integrity and the
plane boundary. Three options exist, each surrendering something the corpus values. **Not resolved
editorially** — blocked on
[RAT-11](open-questions-and-ratifications.md#rat-11--how-the-scenario-assessment-resolves-against-the-plane-boundary).
Provisionally the tree is fully public and the exercise is described as a rehearsal, not a gate.

### DEF-013

The payment structure implements [ML-2.1 §C.9](../license/ml-2-1.md#c9--core-riba) at the interface
layer and **no qualified person has reviewed whether it succeeds.** Review is required in three
domains — law, finance, and Islamic finance scholarship — and the source document's author states
plainly that they hold none of those qualifications. No page asserts Riba compliance as a reviewed
conclusion. Also [B-12](launch-blockers.md#b-12--riba-structure-and-payment-rails-are-unreviewed--hard-blocker).

### DEF-014

Binance Pay is the only rail. Filed as a defect on the source document's **own** reasoning: it
will exclude a meaningful share of the intended audience, *particularly in Arabic-speaking markets
where Meta-X is authoritative*, and couples estate commerce to one company's regional availability.
Disclosed on the pricing page with affected markets named, never at checkout. Also
[B-13](launch-blockers.md#b-13--single-payment-rail--hard-blocker).

### DEF-015

[ST-19 §3.4](../standards/st-19-two-plane-architecture.md#34-failure-transparency-and-how-it-is-proved)
requires a differential build proving every content page is unchanged with the island stubbed to
throw. It does not exist. Until it does, the partitioned Static Principle rests on a promise —
and the island will become load-bearing gradually, through reasonable-looking commits, unless a
machine refuses them. Also [B-14](launch-blockers.md#b-14--the-island-contract-is-untested--hard-blocker-standing).

### DEF-016

**`css/style.css` contains no `prefers-reduced-motion` block.** Nine infinite animations run
regardless of the user's declared operating-system preference: `drift 120s` (starfield),
`heroWash 16s`, `heroGrid 22s`, `heroPan 34s`, `spin 40s` and `spin 30s` (orbits), `marq 32s`
(marquee), `heroFloat 9s` (particles), `shimmer 3.2s` (`.img-slot`). `html { scroll-behavior:
smooth }` is also unqualified.

This is the estate's most embarrassing defect relative to its cost, and it is filed in those
terms deliberately. [DS-02](../design/ds-02-motion-and-attention.md) commits the estate to an
anti-engagement motion posture, and ML‑2.3 §H.4 obliges an operator to publish what it
optimises. A stylesheet that runs nine unstoppable animations while the corpus asserts a refusal
of attention capture is a **contradiction between an instrument and its implementation**, which
is precisely the class of failure [HX‑15](../license/ml-2-3.md#h17-duty-of-non-theatre) names.

One implementation detail must not be lost, because freezing is not sufficient: the block must
**hide `.marquee` entirely**. A frozen marquee is a static half-sentence clipped by a mask,
which is worse than its absence. Escalated to [B-16](launch-blockers.md).

### DEF-017

Detail pages resolve as `detail.html?type=series&id=N` and `article.html?id={slug}` — one
template driven by `js/data.js`. **There is no server-rendered content**, so a series page is
invisible to any crawler that does not execute JavaScript, and the estate's indexability rests
entirely on Googlebot's renderer.

Filed rather than celebrated, because this defect is the **price of retiring DEF-2026-041**. The
flat-file architecture collapsed ~13,300 routes to a few dozen files and removed the Pages
ceiling as a constraint; it also removed the crawlable surface. For a curriculum whose stated
thesis is *being citable by machines*, that is the wrong trade — the estate optimised for a
constraint it had and lost the property it exists for. Blocked on
[RAT-17](open-questions-and-ratifications.md#rat-17--pre-render-or-remain-javascript-only);
recorded at [R-41](reconciliation-ledger.md#r-41--the-live-site-is-flat-files-not-subdomain-routes).

### DEF-018

The estate's own law that pages must render with JavaScript disabled **is violated by the estate
itself.** With JS off there is no header, no footer, no navigation, no pillars, no search and no
year stamp: `components.js` and `main.js` build all of it.

Either the law changes or the build changes. This register's position, and the source's, is that
the build changes — the law is the more valuable of the two, and it is the same argument ML‑2.3
§E.7 makes for the licence text: a document that depends on a script is a document that can be
made unreadable. Blocked on
[RAT-17](open-questions-and-ratifications.md#rat-17--pre-render-or-remain-javascript-only).

### DEF-019

**Google AdSense (`ca-pub-4463113802541266`, three slots) and an Adsterra slot are live on the
content plane.** This contradicts the estate's stated position that the content plane carries no
per-user tracking, and under the newly published Part H it engages **HX‑01** (attention
expropriation) and **HX‑04** (the human as product).

The consequence is not merely editorial. ML‑2.3 §H.16.2 requires a disposition for each harm and
§H.16.3 makes an all-clear Statement presumptively non-compliant. If the estate publishes a Part
H Statement marking these remedied while the ad networks run, **MetaX is the first specimen of
HX‑15**, the harm its own licence introduced. Blocked on
[RAT-15](open-questions-and-ratifications.md#rat-15--will-the-estate-publish-its-own-harms-as-unremedied);
recorded at [R-45](reconciliation-ledger.md#r-45--ads-are-live-on-the-content-plane).

To the live code's credit, `.ad-slot` collapses unfilled slots via `[data-ad-status="unfilled"]`
and reveals the "Advertisement" label only when an ad is actually present.

### DEF-020

[DS-01](../design/ds-01-foundations-and-tokens.md) asserts an "Ink-and-Paper" identity with ten
gradients. The live `:root` is a **cosmic dark, single-theme** token layer — `--bg: #05060f`,
three canonical gradients, two typefaces, no light mode, no `prefers-color-scheme` branch. The
per-brand gradients and warm-gold ramp in the design family were invented and are not the site.

Handled as a correction, not an edit: DS-01's superseded sections are retained with a
non-governing banner and the as-built layer is published as a new instrument, per
[Charter §0.8](../corpus/mx-000-charter.md). Recorded at
[R-43](reconciliation-ledger.md#r-43--the-token-layer-is-cosmic-dark-single-theme).

### DEF-021

[ML-2.3](../license/ml-2-3.md) carries two dangling references **on the face of a Tier 1
governing instrument**: it declares `supersedes: "ML-2.2"` and grants ML‑2.2 a transition period
to 2027‑03‑31, but no ML‑2.2 text exists; and §A.10 incorporates *HX‑000 v2026.10.1*, which has
not been written.

Filed as licence defects ML‑D‑007 and ML‑D‑008 under ML‑2.3 §E.9, which requires exactly this —
*"a conflict between this License and the Register is resolved in favour of this License and is
itself a defect to be filed."* Until resolved, no party may rely on §E.3. Blocked on
[RAT-14](open-questions-and-ratifications.md#rat-14--does-ml-22-exist).

**Second limb discharged 2026‑09‑16 — provisionally.** *HX‑000 v2026.10.1* now exists at
[`hx-000-structural-harms.md`](../harms/hx-000-structural-harms.md): twenty-five harms in six
strata, at a new path with the predecessor retained and marked superseded on its face
([ST-15 §5](../standards/st-15-amendment-and-versioning-standard.md)'s clarified A1 — create,
redirect, supersede; never overwrite). §A.10's reference now resolves.

**Why *provisionally*.** The discharge is not verified. **Nobody has compared the new register
against ML‑2.3's own enumeration** — [HX-000 §9(f)](../harms/hx-000-structural-harms.md) states
this as its own falsifier and records that the check *"should have been run before this document
was published and was not."* If the licence names a harm the register does not carry, §A.10 is
still dangling. Until that comparison is run, this limb is **closed on the author's assertion
alone**, which under [H17](../harms/hx-000-structural-harms.md) is not a closure.

**First limb — ML‑2.2 — remains permanently open.** The text is unrecoverable and the estate will
not reconstruct it ([version history](../license/version-history.md), and the same refusal as
[DEF-029](#def-029)).

**What the re-version found.** Twelve of twenty-five harms are instantiated **by this estate**,
and **ten of the twelve are in the two strata that did not previously exist** — V Reflexive
(H15–H19, all five FAIL) and VI Successor (H20–H25, five of six FAIL). Recorded at
[HX-000 §7](../harms/hx-000-structural-harms.md). The predecessor could not have found them: a
register of fourteen harms about computing had no category in which *"we disclose faster than we
remedy"* could be stated. See [DEF-033](#def-033).

### DEF-022

Touch targets fall below the 44px minimum by a small margin: `.nav-toggle` is 42px and `.btn` is
`14px 26px` on a 100px radius. Corrections are `44px` and `15px 26px` respectively. Minor, but
it is a conformance claim in [MX-010](../corpus/mx-010-accessibility.md) that a ruler falsifies.

### DEF-023

**The name is MacroLifeTech.** The estate published *MacroLifeTach* in
[R-42](reconciliation-ledger.md#r-42--the-third-pillar-is-macrolifetech-not-bcia),
[C-05](corrections-log.md#c-05), [DS-00 §2](../design/ds-00-as-built-token-layer.md) and the
[Task Ledger](task-ledger.md), and minted the anchor
`#r-42--the-third-pillar-is-macrolifetach-not-bcia` from the misspelling, thereby publishing it
as a citable address.

**Partially discharged, and the remainder is not this estate's to fix.** The prose spelling is
corrected in all four instruments with dated amendment notes, and the defective anchor is
retained beside the corrected one — deleting a published address to conceal a spelling error
would trade a cosmetic defect for a broken citation. What remains open is outside the corpus:
MX‑NAV‑SPEC §0 records the misspelling in the live build, in `data.js`, in the meta description,
in the `og:` tags and in the search index, and §9 makes *"Spelling of MacroLifeTech correct in
every instance"* a per-page acceptance criterion. This entry therefore stays open until the
build ships correctly, with one sanctioned exception: the `_redirects` source path
`/macrolifetach.html`, which must keep naming the defective URL in order to retire it.

**Class note.** This is the estate's first defect of a class the register did not previously
have: an error that is **invisible to consistency checking in principle**. A proper name misspelt
everywhere passes cross-source reconciliation, front-matter validation and dangling-link
detection, all of which test agreement rather than reference. See
[C-13](corrections-log.md#c-13) and
[the log's §Method taxonomy](corrections-log.md#method-what-this-log-has-learned).

### DEF-024

**Nine live-code claims were published without recording the provenance of purpose of their
subject.** DEF-017, DEF-018, DEF-019, C-02…C-09 and ledger entries R-41 and R-43…R-46 all
describe bytes that were fetched and read correctly, and all read as findings about **the
estate**. Their subject was a **demo** ([C-14](corrections-log.md#c-14),
[R-50](reconciliation-ledger.md#r-50--the-live-site-is-a-demo)).

None of the nine is false. Every one is unlabelled, which is a different and subtler failure: a
true statement whose evidential weight the reader cannot compute. The remedy is a required
field — `demo`, `staging` or `production` — on every live-artefact claim, amended into
[ST-05](../standards/st-05-decay-and-review-intervals.md) and enforced at the ledger's door.
Until the nine entries carry it, this register treats their evidence class as **indeterminate**
rather than perishable, which is the honest reading.

### DEF-025

**The estate knows it is a demo and no page says so.** MX‑NAV‑SPEC §6.4 requires a provenance
strip beneath the header of every page — `--panel` ground, 1px `--line`, 3px `--gold` left rule,
0.85rem, no animation, dismissible only for the session via `sessionStorage` and **never hidden**
on `/license/`, `/about/status/` or `/metax/bcia/` — plus a page at
`/about/universe/demo-notice/` stating plainly what is real and what is scaffolding. Neither
exists.

This is filed as a defect **and** as launch blocker [B-20](launch-blockers.md), because it is the
boundary case the blocker definition was written for: publishing prototype counts, prototype
catalogues and unreviewed prose *without saying so* does not merely fall short, it misleads. Under
ML‑2.3 it is **HX‑15** committed on the exact pages a reader would visit to check whether the
estate commits HX‑15.

### DEF-026

**Relative asset paths are a latent build failure under directory routing.**
`href="css/style.css"` resolves at depth 0 and fails at depths 1, 2 and 3, and the estate's route
grammar is now three segments deep ([R-49](reconciliation-ledger.md#r-49--root-absolute-paths-are-a-build-law)).
Every asset, script and internal link in every generated file must be root-absolute.

The defect is recorded before any page ships because of how it fails: not at build time, not in
CI, and not on the root hub — the page most often opened while working. It fails at depth, for
the reader, with a missing stylesheet and no error emitted anywhere, and under the estate's own
no-JavaScript law the degraded state is a page with no chrome at all. A defect that cannot be
noticed by the person who caused it belongs in the register before it exists.

### DEF-027

**`SEARCH_INDEX` is hand-written**, which makes it drift from the route set every time a page is
added — a *document-versus-artefact* divergence of precisely the class that produced nine
corrections in this release. MX‑NAV‑SPEC §8.2 replaces it with a build-time emission to
`/data/search-index.json`, fetched lazily, plus `/search/` as a real page listing every route by
pillar.

Recorded at [R-56](reconciliation-ledger.md#r-56--generated-search-and-the-no-js-sitemap). Note
that the remedy **removes the possibility of the divergence** rather than scheduling a check for
it, which is strictly the better repair and is available far less often than the estate would
like.

### DEF-028

**"Three pillars" is published as a navigational fact and navigation carries nine.** MX-001, the
Charter's pillar language and [DS-00 §2](../design/ds-00-as-built-token-layer.md)'s three-gradient
assignment all rest on the three-pillar shape; the canonical `MENU` array carries `toptech`,
`method`, `ascent`, `metax`, `academies`, `credentials`, `library`, `license`, `about`.

The three-pillar thesis survives as a **thesis** — it is routed at `/about/universe/pillars/` —
but a reader who arrives at a nine-item menu after reading a three-pillar charter is entitled to
assume one of them is stale. The register's position is that instruments must state which pillar
set they mean, conceptual or navigational. Blocked on
[RAT-19](open-questions-and-ratifications.md#rat-19), because one of the nine (`Method`) is an
agent's disclosed proposal and the Curator has not ruled.

### DEF-029

**The rule requiring superseded text to be retained was cited for two releases before its
destination existed.** [MX-000 §0.8](../corpus/mx-000-charter.md) forbids silent edits and is the
authority nearly every instrument in this corpus invokes when it records a correction rather than
making one. The [Archive Register](archive-register.md) that §0.8 requires was created on
2026‑10‑01 — after the supersessions it was meant to hold.

**Two texts are already unretrievable**, and both are recorded in
[Archive Register §4](archive-register.md):

- **MX‑NAV‑SPEC v2026.09.4** — superseded *"in its entirety"* by v2026.10.1, and the estate never
  held the earlier text. A reader cannot check whether the four §0 corrections describe the
  previous specification accurately.
- **The fourteen subdomain page-spec rows** of `docs/index.md` §10 — the index states they are
  "retained in the Archive Register"; they are retained as one *table row describing them* and
  nowhere else.

**Not remediable by reconstruction, and that is the entry's substantive content.** The estate will
not draft a plausible v2026.09.4 from its successor's description of it. That is the same refusal
the [version history](../license/version-history.md) made for ML-2.2 — fabricating a superseded
text inside the instrument that defines *Ṣidq* — and it applies with equal force here. The defect
is therefore **permanently open as to those two texts** and closes prospectively: archive coverage
begins 2026‑10‑01.

> The general lesson is worth more than the entry. A procedural rule cited as authority is not the
> same as a procedural rule *operating*, and the gap is invisible from inside the citation. §0.8
> was quoted correctly in a dozen instruments while having nowhere to put anything. This is the
> same failure class as [DEF-001](#def-001) (the standards whose build gate does not run) and it
> is [HX-002 §8](../harms/hx-002-harm-instrument-map.md)'s finding restated: **the estate's
> recurring failure is not bad rules; it is rules without mechanisms.**

### DEF-030

**Thirteen `[VERIFY]` claims are open in the [Verification Log](verification-log.md) and none has
ever been closed.** The log was created in this release — itself a dangling reference for two
releases — and its first publication reports zero verifications.

At one month of verification practice that is expected. What makes it a defect rather than a status
note is [§4 of the log](verification-log.md): **four of the thirteen are checkable in minutes** —
the six platform capacity figures (read a pricing page), the migration-by-copying property
(`rsync` and serve), the dangling-reference count (a link checker), and the Arabic nav breakpoint
(render nine RTL labels and measure).

All four were identified *while writing the instruments that cite them*, which was the moment they
could have been checked at zero marginal cost, and each was deferred to a log instead. That is
precisely how a verification queue becomes a graveyard, and publishing a log whose stated purpose
is to expose it does not discharge it. Under [ML-2.3](../license/ml-2-3.md) a mechanism that
reports a problem it could have fixed is **HX‑15** in miniature.

**Closes when** the four cheap items are verified and §6 of the log has rows. The nine remaining
depend on counsel, a qualified scholar, or a second auditor, and cannot close by internal effort
at any level of diligence — that part is honest rather than negligent, and is not what this defect
is about.

### DEF-031

**Four instruments written in v2026.10.1 specify processes that cannot currently be performed, and
they all fail for the same reason.**

| Instrument | Specifies | Cannot operate because |
|---|---|---|
| [MX-016 §3.1](../corpus/mx-016-appeals-and-due-process.md) | Three-stage appeal, stage 2 a **fresh review by an uninvolved reviewer** | No reviewer pool exists. An appeal collapses to two stages, both held by the Curator |
| [MX-015 §2](../corpus/mx-015-succession-and-continuity.md) | Four roles: Curator, Steward, **Custodian**, **ethics reviewer** | Three are unfilled. §3's triggers fire into an empty room |
| [MX-014 §7](../corpus/mx-014-research-ethics-and-exclusions.md) | Exclusions policed by an **independent ethics veto** | The role is unfilled; exclusions are administered by the party they constrain |
| [ST-06 §6](../standards/st-06-objections-standard.md) | Objections stated at full strength by someone who **holds** them | No external objection has ever been filed; the estate states its own |

**This is one defect recorded four times, not four defects.** Each instrument needs a **second
person** — a reviewer, a custodian, an independent veto, an objector. The estate has one
participant, so each process is specified correctly and inoperative.

**Why it is filed as a single entry.** Fixing them individually is impossible; fixing the cause is
two actions, neither difficult: **name the role holders**
([RAT-04](open-questions-and-ratifications.md#rat-04--name-the-ethics-reviewer-and-the-successors))
and **sign the licence** ([B-01](launch-blockers.md)), since a successor cannot be named against an
unpublished key fingerprint. Both have been open since the first release, through four releases in
which the corpus grew to roughly forty instruments.

**Severity note, stated plainly.** This outranks the ad slots
([DEF-019](#def-019)) in consequence. The ad slots are one decision about one practice; this is
four instruments that cannot do what they say, including **the appeals process** — which means a
person wronged by this estate today has a documented three-stage remedy and two stages available,
both heard by the person who decided against them.

> The estate's recurring finding has been *rules without mechanisms*
> ([HX-002 §8](../harms/hx-002-harm-instrument-map.md)). This entry sharpens it: in four cases the
> missing mechanism is not a script or a build step. **It is a second human being**, and no amount
> of further drafting supplies one.

### DEF-032

**The route manifest is a plan presented in the grammar of an inventory.**
[SITE-01](../site/route-manifest.md) enumerates **321 English routes**.
[REG-02 §5.1](../registries/reg-02-page-registry.md) counts roughly **77 written English pages**
and **zero Arabic pages** — against a corpus whose prevailing text is Arabic.

The gap is not a backlog in the ordinary sense. A manifest listing addresses for pages nobody has
written is a *plan*; publishing it in the enumerative form an *inventory* takes is a category
error, and it is the estate's most misleading single artefact.

**Aggravated by a disclosure failure.** [RB-03 §6](../rubrics/rb-03-instrument-quality-rubric.md)
scores SITE-01 **Q3 = 2** — it needed a sibling instrument
([REG-02](../registries/reg-02-page-registry.md)) to make its own adverse disclosure. An
instrument should not depend on a neighbour to say what is wrong with it.
[ST-18 §5.2](../standards/st-18-related-blocks-and-exit-pairs.md) records the remedy: one adverse
exit action on SITE-01 itself, which would discharge R7 **and** lift Q3 from 2 to 3.

**Also engages** [H19 — volume as evidence](../harms/hx-000-structural-harms.md): a 321-row
enumeration reads as authoritative in proportion to its length.

### DEF-033

**The estate instantiates twelve of its own twenty-five structural harms, and five of the twelve
are harms about publishing a harms register.**

Recorded in full at [HX-000 §7](../harms/hx-000-structural-harms.md). The reflexive stratum, all
five failing:

| Harm | State | Evidence |
|---|---|---|
| **H15** register as absolution | **FAILS** | [REG-07 §5.1](../registries/reg-07-defect-classification-registry.md): every closed defect is cosmetic; **no substantive defect has ever been closed**. [BX-006](../bcia/bx-006-phase-failure-catalogue.md): seven free remedies, none adopted |
| **H16** disclosure as trust amplifier | **FAILS** | [BX-002 §3.1](../bcia/bx-002-contact-phase.md) — found independently, with **no control at all** |
| **H17** self-assessment as assessment | **FAILS** | [AG-011 §4.2](../agents/ag-011-agent-review-and-audit.md) — **review debt 100% at every level** |
| **H18** incapacity absorbing capability | **FAILS** | Found **twice independently**: [AG-011 §5.1](../agents/ag-011-agent-review-and-audit.md), [BX-004 §4.1](../bcia/bx-004-after-phase.md) |
| **H19** volume as evidence | **FAILS** | ~80 instruments, thousands of cross-references, **zero source checks ever performed** |

**This entry cannot be closed by filing it.** H15 *is* the move of substituting disclosure for
remedy, and H15 is one of the twelve. Recording the tally is a statement of position, not a
discharge; the count falls only through the **seven free remedies**
([BX-006 §5](../bcia/bx-006-phase-failure-catalogue.md)) and the **five owed repairs**
([AG-010 §5](../agents/ag-010-agent-error-and-correction.md)).

> This is the sharpest form the estate's recurring finding has taken. *Rules without mechanisms*
> ([DEF-029](#def-029)); *the missing mechanism is a second human being*
> ([DEF-031](#def-031)); and now: **the estate's disclosure practice has itself become the thing
> being disclosed**, and no amount of further drafting reduces the count.

### DEF-034

**A stale register is a false instruction to the next agent, and the task ledger is stale by
roughly forty rows.**

[AG-008 §5.1](../agents/ag-008-agent-collaboration-protocol.md) traced this and rates it **S1** —
the first S1 identified outside [DEF-031](#def-031). The mechanism is compound, and neither limb
is a defect alone:

1. The [task ledger](task-ledger.md) records D-01…D-56 and has **no rows** for the ~40 instruments
   created in this release — the registries family (REG-01…08), most of the corpus family
   (MX-002…019), RB-03/04, ST-08…ST-18, LEX-02/03, AG-001…AG-012, BX-000…BX-009, and HX-000
   v2026.10.1.
2. [AG-005 §5.1](../agents/ag-005-agent-tool-use-limits.md) records **zero compliance** with
   archive-before-overwrite: six instruments were overwritten this session with no Class B entry.

A successor agent reading the ledger would conclude those forty are still owed and begin drafting
them — into an overwrite path with no archive. **The realistic loss is forty instruments.**

**Remedy is cheap and unperformed:** write the ledger rows.
[AG-008 §5.2](../agents/ag-008-agent-collaboration-protocol.md) elevates ledger reconciliation
from bookkeeping to **handover safety**; [H21](../harms/hx-000-structural-harms.md) names the
harm class.

**Structural note, and the one improvement this release's record supports.**
[AG-010 §5.1](../agents/ag-010-agent-error-and-correction.md) found that across nine recorded
agent errors, **every prohibition held and every affirmative duty failed** — no protected artefact
touched, no deletion, no deployment, no continuity claim; and six of six missed archives.
Archive-before-overwrite is drafted as an affirmative duty. Redrafted as a **prohibition** — *an
agent may not overwrite a file absent from archive Class B* — it would sit in the category that
held perfectly. Same rule, same effect, different compliance profile.

### DEF-035

**Twenty-two immortal identifiers were reassigned to different subjects. This is the most serious
defect in the register, and it was committed by the agent that wrote the register entry
announcing it.**

[ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md#3-rule-2--numbers-are-immortal)
states that a number is spent from **first assignment**, including assignment by citation. This
[index](../index.md) had already allocated every identifier below. The completion pass
([task ledger §5b](task-ledger.md)) wrote **new instruments onto the allocated numbers**, at new
paths, under different titles.

| Id | Allocated subject (index §4–§6) | What was written onto it |
|---|---|---|
| MX-005 | Credentialing and Assessment (+ Annex A naming map) | Scope and Boundaries |
| MX-006 | Editorial and Evidence Policy | Contact and Correspondence |
| MX-017 | Trademark and Brand Use | Conflicts of Interest |
| MX-018 | Data Retention Schedule | Third-Party Dependencies |
| MX-019 | Conflicts of Interest | Sunset and Wind-Down |
| ST-08 | The Cognitive Arc and Series Architecture | Cross-Reference and Link Integrity |
| ST-09 | Unit Economics and Kill Criteria | Summary and Abstract Standard |
| ST-10 | Style Guide (English) | Terminology and Definition |
| ST-15 | Component Library Standard | Amendment and Versioning |
| ST-16 | Security Architecture and Dynamic Exceptions | Audience Tier and Register |
| ST-17 | Credential Registry and Verifier Specification | Worked Instance Standard |
| ST-18 | academy.json Manifest Specification | Related Blocks and Exit Pairs |
| AG-001 | The Sole Prompter Protocol | Agent Roles and Scopes |
| AG-002 | Agent Roster and Role Charters | Agent Disclosure Obligations |
| AG-003 | The Standing System Prompt (Kernel) | Agent Output Standards |
| AG-005 | Output Contract and Provenance | Agent Tool Use Limits |
| AG-006 | Evidence and Citation Protocol | Agent Session and State |
| AG-007 | Agent Change Control | Agent Instruction Interpretation |
| AG-008 | Human-in-the-Loop Gates | Agent Collaboration Protocol |
| AG-010 | Agent Evaluation Rubric | Agent Error and Correction |
| AG-011 | Series Generation Agent Charter | Agent Review and Audit |
| AG-012 | Degraded Mode and Prompter Succession | Agent Sunset and Withdrawal |

**Class and severity.** **DC-1 dangling reference** — twenty-two index paths now resolve to
nothing, because the allocated files were never written and their numbers are occupied. Also
**DC-3 overclaim**: each new instrument asserts an authority note for an identifier that belongs
to another subject. Severity **S1** under
[REG-07 §2.2](../registries/reg-07-defect-classification-registry.md): a reader following
[index §5](../index.md) to *AG-011 Series Generation Agent Charter* arrives at a review-and-audit
instrument and cannot tell which is wrong.

**Not repaired by renaming, and the reasoning is the substantive part.** Renaming twenty-two
files would (i) be a silent edit of the kind [Charter §0.8](../corpus/mx-000-charter.md) forbids,
(ii) break several hundred cross-references in the ~40 instruments written this pass, and (iii)
**spend twenty-two further numbers** to conceal the spending of twenty-two. The remedy is a
ratification decision — either the index's allocations are superseded and recorded as such, or
the new instruments are re-identified at the next free numbers with redirects. **That decision is
the Curator's** and is filed as **RAT-25**, not taken here.

**How it was found, which is the one creditable fact in the entry.** By reading
[index §§4–6](../index.md) back before appending rows to it — an **L-2 form audit** in
[AG-011 §3](../agents/ag-011-agent-review-and-audit.md)'s terms, on a document the agent had
already written to twice. It was not found by any of the ~40 instruments, by
[RB-03](../rubrics/rb-03-instrument-quality-rubric.md)'s quality scores, by the five phase audits,
or by [AG-010](../agents/ag-010-agent-error-and-correction.md)'s nine-error consolidation.

> **This is [H19 — volume as evidence](../harms/hx-000-structural-harms.md) with a named
> instance.** Forty instruments were produced, each internally consistent, each carrying eight
> parts and a falsifier and an adverse disclosure, and **twenty-two of them were built on
> identifiers that were not theirs.** The corpus's form did not catch it; its rubrics did not
> catch it; its self-audits did not catch it. One directory listing against one index did.
>
> [AG-011 §3.1](../agents/ag-011-agent-review-and-audit.md) argued that the cheapest unrun check
> in the corpus needs *"no role, no authority and no second participant — only a reader."* That
> argument is now demonstrated rather than asserted, and it was demonstrated against the agent
> that made it.

### DEF-2026-041

**Cloudflare Pages imposes a 20,000-file ceiling**, and the estate's claim to scale "to thousands
of series" was false as built: at ~91 pre-rendered routes per series the ceiling arrives at ~219
series.

**Status: largely retired, and retained anyway.** The live architecture is flat `.html` files
with query-parameter detail routes, so ~13,300 routes collapse to a few dozen files and the
ceiling is no longer the binding constraint. The entry is **not deleted**, for two reasons: the
closed-defect rule forbids it, and the retirement was not a fix — it was a trade that produced
[DEF-017](#def-017) and [DEF-018](#def-018). Should
[RAT-17](open-questions-and-ratifications.md#rat-17--pre-render-or-remain-javascript-only)
resolve toward pre-rendering, **this defect returns as a live constraint** and the file budget
must be computed before that build ships.

**Re-characterised 2026‑10‑01 by MX‑NAV‑SPEC §5.4.** Pre-rendering is now the grammar, and the
arithmetic is restated: 321 EN routes + 321 AR, plus 47 series ×2, plus ~250 live course routes
×2, plus 25 harms ×2, plus lexicon and news — **≈2,000 files including assets**. Headroom ≈18,000
files, about **450 further series** at ~40 files each. The ceiling is therefore *not* the binding
constraint; **Workers requests at 100k/day are the first tripwire.** The entry stays open under
its original identifier because the capacity risk is real and the 80% meter still governs — but
it is now a request-rate constraint wearing a file-count constraint's number, and
[R-54](reconciliation-ledger.md#r-54--the-file-ceiling-is-no-longer-binding) records that
plainly.

### DEF-2026-042

**Resolved structurally, 2026‑10‑01.** The defect was a query-parameter detail route carrying no
server-rendered content, invisible to any crawler that does not execute JavaScript. Under
MX‑NAV‑SPEC v2026.10.1 that route does not exist: `/toptech/s/{S##}-{slug}/` is a real
pre-rendered file at a directory route. Resolution note, as the spec dictates it:
*"resolved structurally by MX‑NAV‑SPEC v2026.10.1, directory routing."*

The entry is retained, not deleted, and it is worth noting **why this closure is unusual**. It
was not repaired, mitigated or accepted — its subject ceased to exist. That is the cheapest
remedy in the register's history and the estate should record how seldom it is available: it
required a change of routing grammar decided for other reasons entirely. Most defects are not
dissolvable and the register should not learn optimism from this one.

### DEF-2026-043

**Six page classes are thin by nature and are exempt from the 1200-word floor** —
`/about/legal/cookies/`, `/about/legal/sitemap/`, `/credentials/verify/revocations/`,
`/library/sources/schemas/`, `/library/sources/downloads/`, and every lexicon entry. Each writes
to natural length and declares `<meta name="mx-thin" content="true">`.

**This entry is a declared exemption, not a shortfall**, and it is filed as a defect deliberately
so that the exemption is visible and countable rather than silently exercised. The reasoning is
the estate's own licence, quoted from MX‑NAV‑SPEC §7.4: *"Padding a cookie policy to 1200 words
to satisfy a spec is exactly the behaviour HX‑15 describes, and the estate cannot publish a
register of that harm while committing it on thirty pages."*

The standing risk is scope creep — an exemption list that grows page by page becomes a licence
to write nothing. The register's control is that additions require a **stated reason per page**
and appear here, where they can be counted against the 321-route census.

<a id="def-036"></a>
### DEF-036

**MX-004 carries two subjects.** Source MX-004 is the Academies Charter, and source MX-012 cites
"MX-004 §4.3(9)" for academy content. The file now at `corpus/mx-004-terms-of-top-levels.md` holds
Terms of Top Levels (the nine-pillar scope). **Class** DC-1 dangling reference. **Severity** S2.
**Remedy applied:** the academies subject was written at [MX-029](../corpus/mx-029-academies-charter.md),
with a pointer at `mx-004-annex-a-technical-requirements.md`. **Closes when** RAT-25 is ruled and every
"MX-004 §4.x" citation is repointed. Owner: Curator.

<a id="def-037"></a>
### DEF-037

**The acronym BCIA was redefined.** In every source (00_BCIA_*, source MX-014 §14.4) BCIA is a
bio-computational research programme under remediation, with seven gates, a human-cell exclusion and
a frozen notation. BX-000…BX-009 (v2026.10.1) use the acronym for a reading model, "Before · Contact ·
Internalisation · After", and occupy every number and path the source programme had been allocated.
The consequence is the most serious in this release: **MX-014 §3's link to the human-cell
exclusion resolved to "The Contact Phase".** **Class** DC-3 overclaim plus DC-1. **Severity S1.**
**Remedy applied:** the source programme is restored at [BX-010…BX-017](../bcia/bx-010-document-zero-and-research-charter.md),
with pointer stubs at all ten legacy paths. The stub at `bx-002-human-cell-exclusion.md` carries the exclusion verbatim.
**Closes when** RAT-28(a) is ruled. Owner: Curator.

<a id="def-038"></a>
### DEF-038

**The human calibration set is unwritten.** [MX-025](../corpus/mx-025-credentialing-and-assessment.md)
and [RB-07](../rubrics/rb-07-agent-evaluation-specimens.md) rely on paired agent and human specimen
sets. Only the agent set exists (SP-01…SP-12). No assessor calibration is possible. **Class** DC-2
missing artefact. **Severity** S2. **Closes when** a human set of at least 12 specimens with scored
exemplars exists. Owner: Curator or a named assessor.

<a id="def-039"></a>
### DEF-039

**Eighteen further identifier collisions beyond DEF-035, and open questions that only accumulate.**
*(Corrected the same day, 2026-09-26. The first draft of this entry said "fifteen", but 40 − 22 = 18.
GM-15 item C-03 records the error.)*
(i) [GM-13](identifier-reallocation-record.md) records 40 collided rows, of which DEF-035 covered 22.
The additional rows are MX-004, RB-03, RB-04, REG-02, REG-04, REG-06, REG-07, REG-08 and BX-000…BX-009.
MX-004 is filed separately as DEF-036 and the BCIA rows as DEF-037. (ii) RAT-24 was cited in eight files
before it existed. (iii) The open-questions file has grown in four consecutive releases to twenty-eight
entries, with none closed. **Class** DC-1, plus a governance defect. **Severity** S2.
**Remedy:** pointer stubs at every legacy path (done, v2026.10.2), and a Curator ruling session on
RAT-25 and RAT-28. Owner: Curator.

**A note on how these were found.** DEF-036, DEF-037 and DEF-039 were found by listing directories
against the index, the same L-2 check that found DEF-035. Text search reported false negatives on
these files several times during the pass, and **an empty search result was never taken as proof of
absence.** That practice is proposed as a kernel rule in [AG-015](../agents/ag-015-standing-system-prompt.md).

### v2027.1 intake defects (DEF-040 … DEF-053), filed 2026-09-30 by [GM-16](source-intake-v2027-1.md)

<a id="def-040"></a>
**DEF-040 · S1 · HX-000 v2026.10.1 names different harms than ML-2.3 §H.2.2 under most identifiers.**
Only H1, H10, H11 and H15 match. "HX-18" means *standard capture* in the licence and the estate's
Statement draft called it "consent integrity". MX-014 §1 and the v2026.10.2 BX files cited HX-21/HX-24
for subjects those identifiers do not hold. **Remedy applied:** a supersession banner,
[CON-002](../harms/con-002-harm-numbering-concordance.md), and corrections in BX-010 and BX-011. MX-014 §1
is still owed (an A-item). **GM-15 missed this**, which is the failure GM-15 §7 predicted for a
self-review.

**DEF-041 · S2 · Two incompatible "v2027.1" source families share version numbers and doc_ids.**
Family A and Family B both issue "HX-000 v2027.1", "ML-2.4" and "ML-B-1.0" with different content.
Resolved by precedence (GM-16 D-01, D-07).

<a id="def-042"></a>
**DEF-042 · S1 · Future-dated signature claims.** The sources say "ML-2.3 SIGNED 2027-01-14" and
"ML-2.4 SIGNED 2027-02-02". Today is 2026-09-30, the fingerprint is `[FPR]`, and no key exists.
Not recorded as fact. B-01 stays open.

**DEF-043 · S1 · ML-2.4 draft collides with ML-2.3.** It reuses §H.31 (Interaction, including the
§H.31.3 conflict rule), §E.6 and §E.7. Renumbered to §H.34, §E.10 and §E.11. **Blocks Track 1 (B-25).**

**DEF-044 · S2 · A fourth claimant to BX-000.** The source's "Register of Substrate Harms v1.0" is
written at BX-018 (RAT-29).

**DEF-045 · S2 · Two different instruments called ML-2.4.** Family B's Part J version is kept as
proposals DT-1…6, WR-1 and SI-1.

**DEF-046 · S1 · The nav spec would misrepresent the licence of record.** It labels unsigned ML-2.4
"The Instrument · live" and redirects ML-2.3 to "Falsification & History". Corrected in
[SITE-06](../site/mx-nav-spec-v2027-1.md).

**DEF-047 · S2 · The source estate Statement omits the ad slots (HX-01, HX-04).** Added in BHS-2027-001 (draft).

**DEF-048 · S3 · Source RAT-17…20 collide with GM-04 RAT-17…20.** Re-keyed to RAT-30…33.

**DEF-049 · S2 · Seven programmes declare `research-preview` against their own charter rule.**
No programme has all seven charter parts ([MLT-000](../metax/programs/mlt-000-programme-register.md)).

**DEF-050 · S3 · The source says §H.7 and §H.24 "were never issued".** Both exist in ML-2.3.

**DEF-051 · S3 · Decay rules.** The source's per-entry verify dates follow neither the stated rule
nor the corrected rule. Both registers' `(n mod 12)` rules produce month 0. A recomputed Decay
Calendar is owed.

**DEF-052 · S1 · ML-B-1.0 §B-E.3 states the estate's limit more weakly than MX-014.** It excludes
only S4/I3, while MX-014 excludes all cultivation and bench work. MX-014 prevails. Annotated on the
face of ML-B-1.0. RAT-37.

**DEF-053 · S2 · No dissent channel outside the steward**, which ML-2.4 §H.33(c), ML-B-1.0 §B-E.4
and BX-018 §7.7 all require at first issue.

### Completion-pass defects (DEF-054 … DEF-067), filed 2026-10-08 from [GM-17](corpus-review-v2027.1.md) and the documents written to close it

<a id="def-054"></a>
**DEF-054 · S1 · HX-002 uses a third harm vocabulary** (e.g. "HX-18 consent integrity", "HX-20 inheritance of unauditable systems"), which matches neither ML-2.3 §H.2.2 nor v2026.10.1. GM-17 X-11. **Remedy:** A-17, a re-key that keeps the state column. Owner: agent, with approval.

**DEF-055 · S3 · MLT-01 declares "2 gates open" and names neither.** [MLT-01](../metax/programs/mlt-01-agora-charter.md).

**DEF-056 · S2 · MLT-02's "live production dependency" on the lexicon has no object.** No LEX-02-form entry had field 2. [LEX-06](../lexicon/lex-06-term-entries-governance-set.md) is the first set, still without Arabic.

**DEF-057 · S3 · MLT-03 "supplies D4 and capacity accounting"**. D4 is an unadopted Family B proposal (DT-4), and no capacity accounting exists.

**DEF-058 · S3 · MLT-04 "3 of 7 parts complete"** conflicts with the five parts the source supplies.

<a id="def-059"></a>
**DEF-059 · S1 · MLT-05's method (cohort outcome measurement) is forbidden by MX-014 exclusions 1 and 4**, and it contradicts the programme's own "no learner data" exclusion. GM-17 X-81. MX-014 prevails. RAT-40.

**DEF-060 · S3 · MLT-07's target "HX-25" uses Family B numbering.** Premise ossification is UH-10 here, and HX-25 is erosion of exit.

<a id="def-061"></a>
**DEF-061 · S1 · MX-014 §2's "three refusals" are not MX-000 §0.4's four.** Only Core Riba is common to both, and "sexualisation of minors" appears in neither MX-000 §0.4 nor §0.7. GM-17 X-20. RAT-44.

<a id="def-062"></a>
**DEF-062 · S2 · ML-2.3 §H.2-bis.1's Tier 1 duty list omits §H.21 (header: "all Tiers") and §H.24 (header: "T1+")**, and its Tier 0 row ("§H.3 only") omits §H.21. The scale gate and the clause headers give different duty sets for small and personal Deployments. **Interim reading:** the header's lower floor applies, as the more protective reading (CF-1 §5; ST-34 §2). Do not edit ML-2.3 in place. RAT-43.

**DEF-063 · S3 · Family B labels the Compliance File "Schedule 1 / CF-1".** In ML-2.3, Schedule 1 is the Part H Statement. Kept apart in [CF-1](../license/cf-1-compliance-file-template.md).

**DEF-064 · S3 · ML-B-1.0 Schedule B-2 cites "Part 3 §3", which the held source lacks.** The worksheet is reconstructed in [ML-B-1.0-SCH](../license/ml-b-1-0-schedules-b1-b2.md).

**DEF-065 · S2 · RAT-24 is cited for five different subjects** (GM-04, scale-gate, REG-03, REG-05, MX-004/REG-02). GM-17 X-40. Remedy A-26: letter them (a)–(d).

**DEF-066 · S1 · MX-000 §0.6 and MX-001 §1.1 define subdomain properties that SITE-01 says do not exist**, and on the precedence ladder the subdomains win (GM-17 X-50). RAT-28(g).

**DEF-067 · S2 · MLT-09's sunset is defeated by its own recommended remedy.** If the notation is retired at Gate 7, Gate 3 can never stay "unresolvable" (GM-17 X-75). RAT-41.

**DEF-051 narrowed (2026-10-08).** The source's per-entry verify dates **all follow the corrected rule**. Only the *stated* formula is defective. The examples given in HX-000 v2027.1 §9 are withdrawn ([C-18](corrections-log.md#c-18), [REG-13](../registries/reg-13-decay-calendar.md)).

**Source defects addressed by forms, pending acceptance:** DEF-2026-073 (`license.json` role discriminator, by [ST-34 §2](../standards/st-34-licence-and-register-machine-forms.md)), -078 (comment-register retention, by [CPF-1 §5](../license/cpf-1-comment-period-publication-format.md)), -079 (Compliance File retention, by CF-1 §8 and B-1.8).

**Source defects imported as issued:** DEF-2026-055…079 and DEF-2027-001 (see HX-000 v2027.1 §11,
BX-018 §11, ML-2.4 Annex A, SITE-07). Open among them: -056, -061, -065, -066, -067, -068, -069,
-070, -071, -072…079, 2027-001.

---

## Closed defects

| Id | Closed | How |
|---|---|---|
| DEF-011 | 2026-08-30 | Precise static-host formulation adopted; `/auth/callback` specified as the single non-content route |
| DEF-2026-042 | 2026-10-01 | **Resolved structurally** — directory routing removed the query-parameter route entirely (MX‑NAV‑SPEC v2026.10.1) |

Closed defects are **never deleted** ([Charter §0.5.2](../corpus/mx-000-charter.md#2-the-correction-obligation)).
A register that removes its resolved entries cannot be audited for how long a defect stayed open,
which is the only number that reveals whether the correction obligation is real.

---

## Counts

Defect counts on any generated page are **computed from this register at build time and never
typed** ([ST-13 §4](../standards/st-13-static-build-and-sentinel.md#4-computed-counts)). A typed
count is a claim with no falsifier, and a typed count that undercounts defects is the specific
failure this register exists to prevent.

---

**Related:** [Launch Blockers](launch-blockers.md) ·
[Open Questions and Ratifications](open-questions-and-ratifications.md) ·
[Corrections Log](corrections-log.md) ·
[Verification Log](verification-log.md) ·
[Reconciliation Ledger](reconciliation-ledger.md)

*Curated by Maher. Thirty-four defects, two closed, one re-characterised, one a declared
exemption — and one (DEF-031) whose remedy is not a fix but a second person. A register with no
entries would mean nobody looked.*

**Amended 2026-09-02.** Seven new defects (DEF-016 … DEF-022) and one retirement, arising from
[ML-2.3](../license/ml-2-3.md) and the as-built design review. The pattern is worth stating
because it is unflattering and therefore load-bearing: **five of the seven are cases where the
estate's own documents describe a site that does not exist, or the site contradicts a value the
documents assert.** DEF-016, DEF-018, DEF-019 and DEF-020 are all of that kind. This is what
happens the first time a corpus is checked against its own running code rather than against its
other documents, and it is the strongest available evidence that the correction obligation in
[Charter §0.5.2](../corpus/mx-000-charter.md#2-the-correction-obligation) is real rather than
decorative.

**Amended 2026-10-01.** Six new defects (DEF-023 … DEF-028), one structural closure
(DEF‑2026‑042), one re-characterisation (DEF‑2026‑041) and one declared exemption
(DEF‑2026‑043), arising from
[MX‑NAV‑SPEC v2026.10.1](../../sources/MX-NAV-SPEC_v2026.10.1.md).

The pattern in this amendment is different from the last one and worth stating with equal
candour. September's seven defects were all found by **reading the code**, and the register drew
the lesson that documents flatter and artefacts do not. October's six were found by the
**Curator**, and two of them — DEF-023 (a proper name) and DEF-024 (the purpose of an artefact) —
were unreachable by either documents or code. Nine claims published in September were true of
the bytes and unlabelled as to what those bytes were for.

The register therefore now recognises three defect-discovery methods with three distinct blind
spots, tabulated at
[Corrections Log §Method](corrections-log.md#method-what-this-log-has-learned), and it records the
uncomfortable implication: **only two of the three can be automated.** The third requires a
person who knows what the thing is called and what it is for. An estate that intends to be
auditable by machines should write that limit down rather than let it be discovered a third time.

One further asymmetry deserves recording. Of the ten entries in this amendment, exactly one
(DEF‑2026‑042) closed — and it closed because its subject ceased to exist, not because anyone
fixed it. The register's honest ratio for the release is **six opened, one dissolved, none
repaired.**
