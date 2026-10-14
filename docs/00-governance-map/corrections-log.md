---
doc_id: "GM-07"
title_en: "Corrections Log"
title_ar: "سجل التصحيحات"
family: "governance-map"
version: "v2026.09.4"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 5
depth: 3
evidence_class: "durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3 · Work of Foundational Character"
last_reviewed: "2026-09-02"
domain_tags: ["governance", "corrections", "provenance"]
hreflang: "en, ar"
---

# Corrections Log

Every claim this estate has published and later found to be **wrong**, with what was said, what
is true, how it was found, and what changed as a result.

**Why this file exists separately from the ledger.** The
[Reconciliation Ledger](reconciliation-ledger.md) records how sources were reconciled — mostly a
record of decisions. This file records **errors**, and only errors. The distinction matters
because a reconciliation ledger read alone flatters its author: every entry is a problem
competently handled. This file is the same estate's record of being mistaken, and it is
deliberately harder to read.

**The rule.** Superseded text is never deleted ([MX-000 §0.8](../corpus/mx-000-charter.md)) and
a published defect cannot be removed by the Curator
([§0.5.2](../corpus/mx-000-charter.md#2-the-correction-obligation)). A correction therefore
**adds** a record; it never replaces one. Where an instrument was wrong, the wrong text stays
retrievable with a non-governing banner, and the correction points at it.

**How to read an entry.** `Claimed` is what the estate said, quoted where possible. `Correct`
is what is true. `Found by` matters most — a corpus whose errors are all found by its author is
a corpus with a weak error-finding mechanism.

---

## Index

| Id | Instrument corrected | Subject | Found by | Date |
|---|---|---|---|---|
| [C-01](#c-01) | MX-DESIGN-001 | "Fully static" content hosts vs a cookie-setting callback | Internal reconciliation | 2026-08-30 |
| [C-02](#c-02) | DS-01 | Design identity: Ink-and-Paper vs cosmic dark | **Fetching the live site** | 2026-09-02 |
| [C-03](#c-03) | DS-01 … DS-06, MX-DESIGN-001 | Invented per-brand gradients and palette | **Fetching the live site** | 2026-09-02 |
| [C-04](#c-04) | MX-DESIGN-001, MX-ARCH-001 | Eight content subdomains and a route grammar that do not exist | **Fetching the live site** | 2026-09-02 |
| [C-05](#c-05) | MX-DESIGN-001, BCIA family | BCIA mis-levelled as a pillar | **Fetching the live site** | 2026-09-02 |
| [C-06](#c-06) | MX-DESIGN-001 | Motion hierarchy understated by a whole tier | **Fetching the live site** | 2026-09-02 |
| [C-07](#c-07) | MX-009, ST-19 | "No per-user tracking on the content plane" — ad networks are live | **Fetching the live site** | 2026-09-02 |
| [C-08](#c-08) | MX-001, ST-13 | "Renders without JavaScript" — the site does not | **Fetching the live site** | 2026-09-02 |
| [C-09](#c-09) | DEF-2026-041 | The 20,000-file ceiling as a binding constraint | **Fetching the live site** | 2026-09-02 |
| [C-10](#c-10) | HX-000 (draft) | The harm/duty citation-collision rule | Upstream repair in ML-2.3 | 2026-09-02 |
| [C-11](#c-11) | HX-000 (draft) | Scope: fourteen harms | Upstream extension in ML-2.3 | 2026-09-02 |
| [C-12](#c-12) | ML-2.3 (transcription) | Cyrillic fragment in §H.18(b) | Reading the supplied text | 2026-09-02 |
| [C-13](#c-13) | R-42, C-05, DS-00, GM-10, MX-DESIGN-001 | **MacroLifeTach** → **MacroLifeTech** — a name misspelt estate-wide | Curator, via MX‑NAV‑SPEC v2026.10.1 §0 | 2026-10-01 |
| [C-14](#c-14) | C-07, C-08, C-09, DEF-017…DEF-019, R-41, R-44…R-46, DS-00 | The live site is a **demo**; its code was cited as production fact | Curator, via MX‑NAV‑SPEC v2026.10.1 §0 | 2026-10-01 |
| [C-15](#c-15) | R-41, MX-ARCH-001, A-09 | Flat `.html` files recorded as the estate's route grammar; the grammar is **directory routes** | MX‑NAV‑SPEC v2026.10.1 §1 | 2026-10-01 |
| [C-16](#c-16) | MX-001, MX-000 § pillars, DS-00 §2, index | "Three pillars" used as a navigational fact; navigation has **nine** | MX‑NAV‑SPEC v2026.10.1 §3 | 2026-10-01 |
| [C-17](#c-17) | BX-000 (reading model, v2026.10.1) | "The first BCIA document"; BCIA had "zero written instruments" | Cross-source reconciliation (GM-15 C-12, written late) | 2026-10-08 |
| [C-18](#c-18) | DEF-051, GM-17 X-104, HX-000 v2027.1 §9 | "The source's per-entry verify dates follow neither rule" | **Recomputing the arithmetic** (REG-13) | 2026-10-08 |

**Nine of sixteen corrections in this log were found by one method: fetching the live site and
reading the actual code instead of the estate's documents about it.** Four more — C-13 through
C-16 — were found by a *third* method that neither documents nor code can supply: the Curator
stating what the artefact is *for*. That is discussed in
[§Method](#method-what-this-log-has-learned) below, which has been amended in consequence.

---

<a id="c-01"></a>
## C-01 — "Fully static" content hosts

**Claimed.** MX-DESIGN-001 described content-plane hosts as *"fully static."*

**Correct.** The content plane requires one non-content route, `/auth/callback`, which sets a
cookie. "Fully static" was therefore false as an unqualified claim.

**Correction.** The Static Principle was **partitioned** rather than abandoned: content pages
are static; one enumerated callback route is not. Recorded at
[R-26](reconciliation-ledger.md) and closed as
[DEF-011](defect-register.md#def-011) on 2026-08-30.

**Found by.** Internal reconciliation of two sources against each other.

---

<a id="c-02"></a>
## C-02 — The design identity is cosmic dark, not Ink-and-Paper

**Claimed.** [DS-01](../design/ds-01-foundations-and-tokens.md) asserts an *"Ink-and-Paper"*
visual identity with ten gradients, and a light-mode-first palette.

**Correct.** The live `:root` in `css/style.css` is a **cosmic dark, single-theme** token layer.
There is no light mode, no `prefers-color-scheme` branch, and `<meta name="theme-color">` is
`#05060f` on every page. The grounds are `--bg: #05060f`, `--bg-2: #090b1a`, `--bg-3: #0d1024`;
text is `--text: #eef1ff`, `--muted: #a6adcf`, `--dim: #6f77a3`.

**Correction.** DS-01's palette and identity sections are marked **non-governing** and retained.
The as-built token layer is published as a new instrument (DS-00) rather than by rewriting DS-01,
per Charter §0.8. Recorded at [R-43](reconciliation-ledger.md#r-43--the-token-layer-is-cosmic-dark-single-theme),
filed as [DEF-020](defect-register.md#def-020).

**Found by.** Fetching `css/style.css` from the live site and reading `:root`.

---

<a id="c-03"></a>
## C-03 — The per-brand gradients were invented

**Claimed.** A warm-gold "Meridian" palette, a "Vault" brand gradient, and per-brand gradient
assignments across the design family.

**Correct.** The system has **exactly four** declared gradients — `--grad-aurora`, `--grad-solar`,
`--grad-nebula`, `--grad-text` — plus six named stops. `--emerald: #3ee6b0` is declared and
unused. The site's colour language is violet→cyan cosmic; the warm-gold ramp is not in it.

**Correction.** The invented gradients are **discarded wholesale**. The correct method is to
assign the three existing gradients by pillar and extend the same ramp in the same syntax where
the identity plane genuinely needs new hues (`--grad-verify` using the unused emerald,
`--grad-vault`, `--grad-ledger`). New brands select from the set or extend it in its own syntax;
they never invent a new colour language.

**Found by.** Fetching `css/style.css`.

> This entry is the clearest case in the log of the characteristic failure mode of documentation
> written *about* a system rather than *from* it: the invented palette was internally coherent,
> plausibly argued, and had no relationship to the artefact.

---

<a id="c-04"></a>
## C-04 — There are no content subdomains

**Claimed.** Eight content subdomains (`toptech.`, `bcia.`, `academies.`, `library.`, `lexicon.`
and others) and a route grammar `toptech.metax.academy/s/{S###}-{slug}/`.

**Correct.** The site is **flat `.html` files on one origin**: `toptech.html`, `community.html`,
`macrolifetach.html`, `curriculum.html`, `ascent.html`, `credentials.html`, `verify.html`,
`library.html`, `lexicon.html`, `news.html`, `about.html`. Detail pages are
`detail.html?type=series&id=N` and `article.html?id={slug}`, driven by `js/data.js`. The route
grammar does not exist.

**Correction.** Recorded at [R-41](reconciliation-ledger.md#r-41--the-live-site-is-flat-files-not-subdomain-routes).
Deferred task A-09 (sitemap and route manifest) **cannot be written as specified** and is
re-scoped in the [Task Ledger](task-ledger.md) rather than deleted, because deleting a task is
how a premise change becomes invisible.

**Found by.** Fetching `index.html` and `js/site.js`.

---

<a id="c-05"></a>
## C-05 — BCIA is a program, not a pillar

**Claimed.** BCIA as the third pillar of the estate, with its own subdomain and a pillar-level
instrument set.

**Correct.** The third pillar is **MacroLifeTech (Meta-X)**. BCIA is one program inside it —
routed at `/metax/bcia/` — one of nine, alongside Agora, Maʿnā, Metabolism, Soma, Paideia,
Athar, Āfāq and Mīzān.

**Correction.** The BX-000…BX-009 family survives, re-levelled as a **program** instrument set.
`bcia.metax.academy` is not a hostname the estate has. Recorded at
[R-42](reconciliation-ledger.md#r-42--the-third-pillar-is-macrolifetech-not-bcia); deferred task
A-08 re-scoped accordingly.

**Spelling amended 2026‑10‑01.** This entry originally read *MacroLifeTach*. See
[C-13](#c-13).

**Found by.** Fetching `index.html` and reading the actual pillar cards.

> A hierarchy error is worse than a detail error, because every instrument written beneath the
> wrong level inherits it. This correction invalidates a level of the estate's own architecture
> diagram, and it was found in a stylesheet-level review that was not looking for it.

---

<a id="c-06"></a>
## C-06 — The motion system was understated by a whole tier

**Claimed.** A four-tier motion hierarchy with *"T0 static, ~80% of pages."*

**Correct.** The system is **ambiently animated by default**. A fifth tier sits below the
others — T-A, ambient: `drift 120s`, `heroWash 16s`, `heroGrid 22s`, `heroPan 34s`, `spin 40s`
and `30s`, `marq 32s`, `heroFloat 9s`, `shimmer 3.2s` — present on hub, pillar and section
pages, and absent only on `auth.`, `pay.`, `verify.` record pages and `license.`.

**Correction.** The hierarchy is restated as five tiers (T-A ambient, T-1 entrance, T-2 feedback,
T-3 signal — reserved and currently unused). This correction is what exposed
[DEF-016](defect-register.md#def-016): nine infinite animations with no `prefers-reduced-motion`
escape, now hard blocker [B-16](launch-blockers.md).

**Found by.** Fetching `css/style.css` and counting the `@keyframes` blocks with
`animation-iteration-count: infinite`.

---

<a id="c-07"></a>
## C-07 — Ad networks are live on the content plane

**Claimed.** No per-user tracking on the content plane; the content plane holds no identity and
is unobservable by construction.

**Correct.** Google AdSense (`ca-pub-4463113802541266`, three slots) and an Adsterra slot are
**live on the content plane**.

**Correction.** This is the most consequential entry in this log, because it is not a
documentation error — it is a **claim contradicted by the estate's own running conduct**, and the
newly published Part H makes it operative rather than merely embarrassing. It engages
[HX-01](../license/ml-2-3.md#h4-optimisation-disclosure) (attention expropriation) and
**HX-04** (the human as product). Under ML-2.3 §H.16.2 the estate must record a disposition for
each; under §H.16.3 an all-clear Statement is presumptively non-compliant and evidence of
**HX-15, compliance theatre**.

Recorded at [R-45](reconciliation-ledger.md#r-45--ads-are-live-on-the-content-plane), filed as
[DEF-019](defect-register.md#def-019), escalated to [B-19](launch-blockers.md), and referred to
the Curator as [RAT-15](open-questions-and-ratifications.md#rat-15--will-the-estate-publish-its-own-harms-as-unremedied).
**No editor may resolve it.** The only two honest outcomes are removing the networks or
publishing the harms as unremedied.

One thing the live code does right, recorded so the entry is not one-sided: `.ad-slot` collapses
unfilled slots via `[data-ad-status="unfilled"]` and reveals the "Advertisement" label only when
an ad is actually present.

**Found by.** Fetching `index.html`.

---

<a id="c-08"></a>
## C-08 — The site does not render without JavaScript

**Claimed.** Pages must render with JavaScript disabled — stated as a law of the estate.

**Correct.** With JavaScript off the live site has **no header, no footer, no navigation, no
pillars, no search and no year stamp**. `components.js` and `main.js` build all of it.

**Correction.** The law is retained and the **build** is what must change — the law is the more
valuable of the two, and it is the same argument ML-2.3 §E.7 makes for the licence text itself: a
document that depends on a script is a document that can be made unreadable. Filed as
[DEF-018](defect-register.md#def-018), recorded at
[R-46](reconciliation-ledger.md#r-46--the-no-javascript-law-is-violated-by-the-estate-itself),
referred as [RAT-17](open-questions-and-ratifications.md#rat-17--pre-render-or-remain-javascript-only).

**Found by.** Fetching the live site and disabling script execution.

---

<a id="c-09"></a>
## C-09 — The file-ceiling defect was largely retired, and that is not a fix

**Claimed.** [DEF-2026-041](defect-register.md#def-2026-041): the Cloudflare Pages 20,000-file
ceiling binds the estate at ~219 series, so the claim of scaling "to thousands of series" was
false as built.

**Correct.** Under the as-built flat-file architecture, ~13,300 routes collapse to a few dozen
files. The ceiling is **not** the binding constraint.

**Correction.** The defect is marked largely retired and **retained**, because the retirement was
not a repair — it was a **trade**. The same architecture that removed the ceiling removed the
crawlable surface, producing [DEF-017](defect-register.md#def-017) and
[DEF-018](defect-register.md#def-018). If
[RAT-17](open-questions-and-ratifications.md#rat-17--pre-render-or-remain-javascript-only)
resolves toward pre-rendering, **DEF-2026-041 returns as a live constraint** and the file budget
must be computed before that build ships.

**Found by.** Fetching the live site; the correction to the correction is this log's own analysis.

> Recorded because a corrections log that only records claims found *too optimistic* is
> half a log. This entry corrects a claim that was too **pessimistic**, and then declines to
> celebrate it.

---

<a id="c-10"></a>
## C-10 — The harm/duty citation-collision rule is withdrawn

**Claimed.** The draft harms register identified a real citation hazard — harms `H12`, `H13`,
`H14` colliding with duties `§H.12`, `§H.13`, `§H.14` — and proposed a disambiguation convention:
`HX-000 H{n}` for harms, `ML-2.x §H.{n}` for clauses.

**Correct.** The hazard was real; the proposed remedy was the weaker of the two available.
ML-2.3 repairs it **at the source** by renaming every harm to the `HX-{nn}` form.

**Correction.** The estate's convention is **withdrawn** and must not be carried into HX-000
v2026.10.1. Canonical forms are now `HX-14` for a harm and `ML-2.3 §H.14` for a duty — which
refer to different subjects (moral deskilling; material accounting), exactly the confusion the
rename removes. Recorded at
[R-40](reconciliation-ledger.md#r-40--the-harm-identifier-collision-is-repaired-upstream).

**Found by.** Upstream repair, reading the ML-2.3 changelog.

> A convention that must be remembered is a defect. Distinct identifiers cannot collide.

---

<a id="c-11"></a>
## C-11 — The register's scope was fourteen harms

**Claimed.** *The Fourteen Structural Harms of Computing, Networking and Technological Order* —
fourteen harms in four strata, five of them carrying bounded absolutes.

**Correct.** ML-2.3 incorporates a **twenty-five** harm register in six strata with **eight**
absolutes, titled *The Structural Harms of…* — the word "Fourteen" is gone from the title.

**Correction.** HX-000 is **re-versioned, not merely completed**. The eleven drafted harms are
retained and re-based to `HX-{nn}`; HX-12/13/14 are completed; Strata V (Reflexive, HX-15…HX-19)
and VI (Successor, HX-20…HX-25) are added. Recorded at
[R-39](reconciliation-ledger.md#r-39--the-register-grows-from-fourteen-to-twenty-five), tracked
as task N-01 in the [Task Ledger](task-ledger.md).

**Authorship must be split in the corrected document.** Harms H1–H11 were drafted by this
estate's documentation agent; the eleven harms of Strata V and VI arrived with the ML-2.3 text
from a different drafting agent. ML-2.3 §H.19 requires a recorded natural author for assertions
issued in the estate's name, and presenting two voices as one would breach the *Ṣidq* the
register asserts. HX-000 v2026.10.1 carries an authorship note.

**Found by.** Reading the supplied ML-2.3 text against the draft in progress.

---

<a id="c-12"></a>
## C-12 — A Cyrillic fragment in ML-2.3 §H.18(b)

**Claimed.** The supplied ML-2.3 text reads, at §H.18(b): *"Consent obtained at a moment when the
person cannot pract**ически** refuse…"* — a Cyrillic transcription fault in an operative clause.

**Correct.** The intended word is *practically*.

**Correction.** Corrected in the published instrument and logged here rather than edited
silently, per Charter §0.8. The correction is non-substantive: no reading of the Cyrillic
fragment produces a different obligation. It is logged anyway, because the threshold for this log
is *"the published text was not what it should have been,"* not *"the meaning changed."* A log
that only records consequential errors trains its keeper to judge consequence before recording.

**Found by.** Reading the supplied text closely enough to publish it.

---

<a id="c-13"></a>
## C-13 — The name is MacroLifeTech, not MacroLifeTach

**Claimed.** The third pillar of the MetaX universe is **MacroLifeTach (Meta‑X)**. The estate
asserted this in [R-42](reconciliation-ledger.md#r-42--the-third-pillar-is-macrolifetech-not-bcia),
in [C-05](#c-05), in the gradient-assignment table of
[DS-00 §2](../design/ds-00-as-built-token-layer.md), in the
[Task Ledger](task-ledger.md), and in the anchor slug
`#r-42--the-third-pillar-is-macrolifetach-not-bcia`, which was minted from the misspelling and
circulated as a citable address.

**Correct.** The name is **MacroLifeTech**. The nav key is `metax`, the hub route is `/metax/`,
the display label is `Meta‑X`, and the expanded name written in prose is
**MacroLifeTech (Meta‑X)**.
[MX‑NAV‑SPEC v2026.10.1 §0](../../sources/MX-NAV-SPEC_v2026.10.1.md) rules every occurrence of
the old spelling a defect — in the live build, in `data.js`, in the meta description, in the
`og:` tags, in the search index, and expressly *"in every prior specification,"* which includes
this corpus. The single sanctioned survival is the redirect source `/macrolifetach.html`, which
must continue to name the defective URL in order to retire it.

**Correction.** The prose spelling is amended in R-42, C-05, DS-00 §2 and the Task Ledger, each
carrying a dated amendment note rather than a silent replacement. The defective anchor is
**retained alongside** the corrected one in R-42, because deleting a published address to hide a
spelling error would trade a cosmetic defect for a broken citation, and
[MX-000 §0.8](../corpus/mx-000-charter.md) forbids the silent removal either way. Filed as
[DEF-023](defect-register.md#def-023) and reconciled at
[R-47](reconciliation-ledger.md#r-47--the-name-is-macrolifetech).

**Found by.** The Curator, in the §0 corrections of a navigation specification — not by any
check this estate operates.

> This is the cheapest error in the log and the most instructive. Every mechanism the estate is
> proud of — cross-source reconciliation, live-code verification, front-matter validation,
> dangling-link detection — is a **consistency** mechanism, and a name misspelt consistently
> everywhere passes all of them. Forty-six ledger entries and nine code-derived corrections
> propagated the error faithfully; the estate's own instruments could not have caught it, because
> to catch it you must know the referent, and no document in the corpus is the referent. The
> proper name of a thing is held only by the person who named it. That is a structural limit on
> what a documentation corpus can audit about itself, and it is recorded here as a limit rather
> than as a slip.

---

<a id="c-14"></a>
## C-14 — The live site is a demo, and the estate cited it as production

**Claimed.** Throughout the v2026.09.4 release, the estate treated the fetched live build as
**the production system**. C-07 records that "ad networks are live." C-08 records that "the site
does not render without JavaScript." DEF-017, DEF-018 and DEF-019 are written as production
defects; R-44, R-45 and R-46 as findings of fact about a running estate; and
[DS-00](../design/ds-00-as-built-token-layer.md) opens by asserting that the as-built code
**governs** the design layer in its entirety.

**Correct.** [MX‑NAV‑SPEC v2026.10.1 §0](../../sources/MX-NAV-SPEC_v2026.10.1.md) states plainly:
*"The live site is a demo."* The consequence the spec draws is precise and it is not a general
retraction — *"the anchor set I told agents was immutable is not immutable; it was inventory of a
prototype. Live copy, live counts, live series descriptions and the live `FLAGSHIPS` array are
all placeholder-grade and must be rewritten, not preserved. What survives from the live build is
the token layer, the component vocabulary and the chrome mechanics — the design system, not the
content."*

**Correction.** The estate now distinguishes two classes of live-code finding, and the
distinction is load-bearing:

1. **Design-layer findings survive with full authority.** The token layer, the component
   vocabulary, the chrome mechanics, the five-tier motion system, the script load order and the
   `.img-slot` no-image regime are what the demo was built to establish. DS-00 stands. So do
   R-43, R-44 and the reduced-motion blocker [B-16](launch-blockers.md), because a missing
   `prefers-reduced-motion` block is a defect *in the design system itself*, which the demo
   faithfully carries into production.
2. **Content-layer and posture findings are demoted to findings about a prototype.** The ad
   slots (C-07, DEF-019, R-45), the no-JavaScript render failure (C-08, DEF-017, DEF-018,
   R-46), the flat-file route grammar (R-41) and the copy, counts and `FLAGSHIPS` inventory
   describe **scaffolding**, not a shipped posture. They are not withdrawn — a defect observed
   in a prototype that is scheduled to become production remains a defect — but their evidence
   class falls from a statement about the estate to a statement about the estate's current
   scaffolding, and each acquires a remediation window that a production defect would not have.

The practical gain is stated in the spec's own §10 and the estate adopts it: because the site is
a demo, there is *"a clean window to remove the ad slots before the statement is ever
published,"* which would let MetaX's own Part H Statement read **remedied** on HX‑01 and HX‑04
rather than *unremedied*. That converts [RAT-15](open-questions-and-ratifications.md) from a
question about how to confess a harm into a question about whether to commit it, and it is the
first time in this release that a correction has *widened* the Curator's options.

The obligation running the other way is new and it is immediate: every generated page must carry
the demo provenance strip of §6.4, undismissable on `/license/`, `/about/status/` and
`/metax/bcia/`, and `/about/universe/demo-notice/` must exist and say plainly what is real and
what is scaffolding. An estate that knows it is a demo and does not say so on the page is
committing HX‑15 in the one place a reader would look to check.

**Found by.** The Curator. No document and no fetch could have supplied it: the code of a
prototype and the code of a production system are byte-identical in every respect except
intention.

> C-14 is the deepest correction in this log, because it does not correct a fact — every fact in
> C-07, C-08 and DEF-017…019 remains true of the bytes that were read. It corrects the
> **authority** the estate granted those facts. The method that produced nine corrections by
> reading code turns out to have a blind spot exactly congruent with its strength: reading the
> artefact tells you what is there and cannot tell you what it is *for*. The estate replaced
> documentary self-flattery with a naive empiricism, and naive empiricism about a prototype
> produces a register of confident findings about a rehearsal. Provenance of purpose is now a
> required field of any live-code claim: see the amendment to
> [ST-05](../standards/st-05-decay-and-review-intervals.md) proposed in
> [§Method](#method-what-this-log-has-learned).

---

<a id="c-15"></a>
## C-15 — Flat files were recorded as the route grammar; the grammar is directory routes

**Claimed.** [R-41](reconciliation-ledger.md) records, correctly as observation, that the live
site is *"flat `.html` files on one origin"* — `toptech.html`, `curriculum.html`, `bcia.html`,
`news.html?cat=` — and on that basis retired the subdomain route grammar of MX-ARCH-001 and
re-scoped deferred task A-09.

**Correct.** The flat files are the demo's inventory (see [C-14](#c-14)), not the estate's
grammar. The canonical grammar is **directory routes with a trailing slash, each backed by
`index.html`, no `.html` in any published URL**, capped at three segments plus a parametric
series/course exception:

```
/                                   root hub
/{pillar}/                          pillar hub          (9)
/{pillar}/{group}/                  group hub           (45)
/{pillar}/{group}/{leaf}/           leaf page           (266)
/toptech/s/{S##}-{slug}/            parametric series
/toptech/s/{S##}-{slug}/c{NN}/      parametric course
```

**Correction.** Three things follow, and only the first is cosmetic. First, every anchor
citation of the form `a.html#b` in the corpus becomes the route `/a/b/`. Second, group headings
that existed only as `<h6>` labels inside a mega-panel are now **addressable pages**, which is
what produces the estate's third tier and its 45 group hubs. Third — and this is the one that
breaks builds — **relative asset paths are now a build failure**: `href="css/style.css"`
resolves at depth 0 and silently fails at depths 1, 2 and 3, so every asset, script and internal
link in every generated file must be root-absolute. Recorded at
[R-48](reconciliation-ledger.md#r-48--anchors-become-routes) and
[R-49](reconciliation-ledger.md#r-49--root-absolute-paths-are-a-build-law), and the deferred task
A-09 is unblocked and re-scoped in the [Task Ledger](task-ledger.md).

One defect closes structurally rather than by repair.
[DEF‑2026‑042](defect-register.md) — the query-parameter detail route invisible without
JavaScript — does not survive the migration, because `/toptech/s/{S##}-{slug}/` is a real
pre-rendered file. It moves to `resolved` with the note *"resolved structurally by
MX‑NAV‑SPEC v2026.10.1, directory routing."* A defect closed by making its subject nonexistent
is the cheapest possible remedy and the estate should record how rarely that is available.

**Found by.** MX‑NAV‑SPEC v2026.10.1 §1, read against R-41.

---

<a id="c-16"></a>
## C-16 — "Three pillars" is a thesis, not a navigation fact

**Claimed.** The estate speaks throughout of **three pillars** — TopTech, Academies/Community,
MacroLifeTech (Meta‑X) — and DS-00 §2 assigns exactly three gradients on that basis, one per
pillar card on the hub.

**Correct.** Navigation has **nine** top-level pillars: `toptech`, `method`, `ascent`, `metax`,
`academies`, `credentials`, `library`, `license`, `about`. The three-pillar thesis survives as a
thesis — the nav spec itself routes it at `/about/universe/pillars/` — but it is not the shape of
the estate's navigation, and a reader arriving at a nine-item menu after reading a three-pillar
charter is entitled to think one of them is out of date.

**Correction.** The estate now separates the **conceptual** pillar set (three: what the universe
is about) from the **navigational** pillar set (nine: how it is addressed), and requires any
instrument using the word "pillar" to say which it means. Two consequences are structural.
DS-00 §2's three-gradient assignment is under-specified for nine surfaces and is re-derived in
[DS-02](../design/) as a nine-way assignment reusing the existing ramp — not by inventing six
gradients, which is precisely the error C-03 corrected. And `Method` as a pillar is, in the
spec's own words, *"my addition, not yours"* — an agent-proposed ninth pillar assembling the arc,
the rails, the epistemics and the twelve instruments that were previously scattered as anchors.
That proposal is a governance question, not a design detail: it is filed as
[RAT-19](open-questions-and-ratifications.md#rat-19) for the Curator, with the spec's own
recommendation (keep the nine, move the breakpoint to 1180px) recorded and **not** adopted on the
agent's own authority.

**Found by.** MX‑NAV‑SPEC v2026.10.1 §3, read against MX-001 and DS-00.

---

<a id="c-17"></a>
## C-17 · BX-000 was not "the first BCIA document"

**Claimed.** BX-000 (v2026.10.1, the reading model) presents itself as the first BCIA document and says
BCIA had "zero written instruments" before it (bx-000 l.33–38).

**Correct.** At least five BCIA documents preceded it:
- 00_BCIA_PUBLIC_STATUS v2026.08.12
- 00_BCIA_TAXONOMY_OBSERVED v2026.08.14
- 00_BCIA_FRONT_MATTER_MIGRATION v2026.08.14
- 00_BCIA_STATUS_PAGE_PATCH v2026.08.14
- source MX-014 §14 (the human-cell exclusion, the seven gates and the ethics veto)

All are held in `sources/`. They are now restored at BX-010…BX-017. BX-000's claim was made
about an acronym it had redefined (DEF-037). It was true of the reading model and false of BCIA.

**Correction.** The claim stays in BX-000 with this entry as its correction. Nothing is deleted. A
non-governing banner is owed on BX-000 once RAT-29 decides the identifier's final holder.

**Found by.** Cross-source reconciliation, in GM-15 (item C-12). **GM-15 promised this entry and it was not
written for two releases** (GM-17 M-21, X-115). That delay is itself the lesson: a promised correction
that nobody files is a correction that did not happen.

---

<a id="c-18"></a>
## C-18 · The HX-000 verify dates *do* follow the corrected decay rule

**Claimed.** DEF-051, HX-000 v2027.1 §9 and GM-17 X-104 say that the source's per-entry verify
dates "follow neither the stated rule nor the corrected rule". They cite HX-05 (2027-06) and HX-25 (2027-02) as examples.

**Correct.** Every one of the 28 HX dates follows the **corrected** rule, `2027-01 + (((n − 1) mod 12) + 1)` months:
- n = 5 gives 2027-06.
- n = 12 gives 2028-01.
- n = 13 gives 2027-02.
- n = 24 gives 2028-01.
- n = 25 gives 2027-02.
- n = 28 gives 2027-05.

The dates differ from the source's *stated* rule `(n mod 12)` only at n = 12 and n = 24, where that rule produces month zero. The source therefore stated the wrong rule and applied the right one. For BX-018, the dates that could be checked (BX-01 and BX-13 at 2027-07) also follow the corrected rule offset from 2027-06.

**Correction.** DEF-051 is narrowed: the defect is the *stated* rule, not the dates. The examples
cited in HX-000 v2027.1 §9 are withdrawn. [REG-13](../registries/reg-13-decay-calendar.md) holds the computed calendar.

**Found by.** Doing the arithmetic, which the original finding had not done. This is the same
failure as GM-13's "thirty-seven" and DEF-039's "fifteen": a numerical claim written without being computed.

---

<a id="method-what-this-log-has-learned"></a>
## Method: what this log has learned

Sixteen entries is enough to see a pattern, and the pattern is the most useful thing in this file.

**1. Nine of sixteen corrections came from one method.** Fetching the live site and reading
`index.html`, `css/style.css`, `js/components.js` and `js/site.js` produced C-02 through C-09.
No amount of reconciling documents against each other found any of them, and Parts 1 and 2 of the
Reconciliation Ledger — thirty-seven entries of careful cross-source work — found one (C-01).

The estate's documents were **internally consistent and externally wrong**. That is the
characteristic failure of a governance corpus: it audits its own coherence, which is the property
it can check cheaply, and mistakes coherence for accuracy.

**2. The errors were not random.** They ran in one direction — the documents described a more
ambitious, more principled, more architecturally elaborate system than the one running. Invented
subdomains, invented gradients, a pillar that was a program, a static-rendering law nobody
implemented, an anti-tracking claim with ad networks underneath it. Documentation drift favours
the flattering reading, and it does so without anyone intending it.

**3. The corpus's own instruments caught nothing.** ST-13's dangling-link detection, front-matter
validation and single-source drift checks would not have caught one of these, because all nine
are *document-versus-code* divergences and
[DEF-001](defect-register.md#def-001) records that the pipeline does not run anyway.

**4. Three methods, three blind spots — and the third method is a person.** C-13 through C-16
were found by neither documents nor code. They came from the Curator saying what the artefact is
named, what it is for, and what shape it is meant to take. This completes a taxonomy the log can
now state:

| Method | Finds | Structurally cannot find |
|---|---|---|
| Cross-source reconciliation | Contradictions between instruments | Anything the corpus is uniformly wrong about (C-13) |
| Reading the live artefact | Divergence between document and code | What the code is *for* — demo vs production (C-14) |
| The Curator's statement of intent | Referent, purpose, intended shape | Whether the estate has actually implemented any of it |

Each method's blind spot is another method's specialty, which is the only reason the set works;
and no automated check can occupy the third row, because its input is a person's intention. An
estate that plans to be audited by machines should write that row down explicitly rather than
assume it away, and — the harder discipline — should record which of the three produced each
claim it publishes.

**Standing obligation arising from this log.** A claim about the live system is not durable
evidence. It decays the moment the code changes, which makes every such claim
**perishable** under [ST-05](../standards/st-05-decay-and-review-intervals.md), and the estate has
been writing them as though they were durable. The remedy is a build-time check that reads the
artefact rather than the document — proposed as the standing extension to ST-13, and the reason
[B-16](launch-blockers.md) and B-17 are written as tests rather than as intentions.

**Second standing obligation, arising from C-14.** Every claim about the live system must now
record the artefact's **provenance of purpose** — `demo`, `staging` or `production` — alongside
its date. A finding whose subject is a prototype and whose text reads as a finding about the
estate is not a false statement; it is an unlabelled one, and the estate published nine of them
in a single release. ST-05 is amended to require the field, and no live-code claim may be
admitted to the Reconciliation Ledger without it.

---

**Related:** [Defect Register](defect-register.md) ·
[Launch Blockers](launch-blockers.md) ·
[Open Questions and Ratifications](open-questions-and-ratifications.md) ·
[Reconciliation Ledger](reconciliation-ledger.md) ·
[Task Ledger](task-ledger.md) ·
[Changelog](changelog.md)

*Curated by Maher. Sixteen corrections. Nine found by reading the code instead of the documents;
four found by the Curator telling the estate what its own subject is called and what it is for.
The log's most important entry is no longer a correction but the taxonomy in §Method: three
methods of error-finding, three blind spots, and only two of them automatable.*
