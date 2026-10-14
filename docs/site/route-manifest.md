---
doc_id: "SITE-01"
title_en: "The Route Manifest"
title_ar: "بيان المسارات"
family: "site"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 4
depth: 5
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["site", "routing", "information-architecture", "navigation"]
supersedes: "MX-NAV-SPEC v2026.09.4 (route sections)"
derived_from: "MX-NAV-SPEC v2026.10.1 §§1–5"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# The Route Manifest

**What this instrument is.** The single canonical enumeration of every address the
`metax.academy` estate publishes, together with the law governing address formation. It is the
discharge of deferred task A-09 — *"write sitemap + route manifest + per-property page specs"* —
which was blocked from the moment it was written, because the estate did not know its own route
grammar, and is unblocked by
[MX‑NAV‑SPEC v2026.10.1](../../sources/MX-NAV-SPEC_v2026.10.1.md).

**What this instrument is not.** It is not a sitemap file. `sitemap.xml` is *generated* from this
manifest at build time and must never be hand-maintained ([§9](#9-generated-artefacts)). Nor is
it a navigation menu: the `MENU` array in `/js/site.js` is likewise generated from this manifest,
and where the two disagree **this document governs and the divergence is a defect**.

**Authority.** Governing for the shape of addresses. It does not govern what a page says — that
is [ST-24](../standards/st-24-page-prose-standard.md) — nor how a page is built, which is the
[Page Contract](page-contract.md). Where it conflicts with [ML-2.3](../license/ml-2-3.md), the
License prevails and the conflict is itself a defect to be filed under §E.9.

---

## 0. Why a route list is a governance instrument

A route list looks like an implementation detail. It is not, and the argument belongs before the
tables rather than after them.

**An address is a commitment.** When the estate publishes `/license/harms/stratum-v-reflexive/`
it asserts three things at once: that a stratum V exists, that it is reflexive, and that the
estate has something to say about it at a permanent location. A reader citing that URL in 2031
relies on all three. This is the property [MX-000 §0.8](../corpus/mx-000-charter.md) protects when
it forbids silent edits, extended from a document's *text* to its *address* — which is why the
estate treats a broken internal link as a correction event rather than a maintenance chore.

**The shape of the addresses is the shape of the argument.** A three-tier grammar asserts that
the estate's knowledge has three levels of generality: a pillar claims something about a domain,
a group hub about a method or family within it, a leaf about one object. That is a substantive
epistemological position and it is falsifiable in the ordinary way — if a leaf cannot be written
without repeating its hub, the tier was wrong. §2 therefore records what each tier is *for*, so
that a future editor can be told they have filed a page at the wrong altitude.

**A manifest is the only defence against silent scope drift.** Without a canonical enumeration an
estate grows by accretion: a page here, a section there, each locally justified, until nobody can
say how large the thing is or what it promised. The census in §4 is a number the estate can be
held to — 321 English routes, 45 group hubs, 266 leaves — published so that a reader can count
what exists against what was declared and find the gap.

**The macro register.** Everything above concerns this estate. The wider claim is this: the
dominant pattern of the machine-mediated web is the **addressless surface** — the feed, the
infinite scroll, the app view with no URL, the chat answer that exists once and is never
retrievable. Knowledge published that way cannot be cited, cannot be checked against its earlier
self, and cannot be inherited, which under [HX‑12 and HX‑20…HX‑25](../harms/) is not a stylistic
preference but a structural harm to the record and to the successor. This manifest's insistence
that **every claim carry a permanent, human-legible, hierarchically meaningful address** is the
estate's most concrete refusal of that pattern — and its cheapest, since directory routes cost
nothing but discipline.

---

## 1. Routing law

### 1.1 Shape

Directory routes with a trailing slash, each backed by `index.html`. **No `.html` in any
published URL.** Depth capped at three segments, plus the parametric exception at §6.

```
/                                   root hub                    (1)
/{pillar}/                          pillar hub                  (9)
/{pillar}/{group}/                  group hub                   (45)
/{pillar}/{group}/{leaf}/           leaf page                   (266)
/toptech/s/{S##}-{slug}/            parametric series
/toptech/s/{S##}-{slug}/c{NN}/      parametric course
```

**Why three tiers and not four.** A fourth level is technically free and epistemically expensive.
Each additional level asks the reader to hold one more distinction before reaching a claim, and
asks the author to justify a level of generality between "family of methods" and "one object"
that in practice does not exist. The parametric exception is the one place a fourth segment
appears, and it appears because a course genuinely is part of a series in a way no leaf is part
of another leaf.

### 1.2 Trailing slash is canonical

`/toptech/start` issues a 301 to `/toptech/start/`. `<link rel="canonical">` always carries the
slash. Cloudflare Pages resolves directory indexes natively; `trailingSlash: always` behaviour is
asserted through `_redirects`.

This is a duplicate-content rule and also a **citation rule**. Two addresses for one page mean
two citation forms in the wild, which means a future audit of who cited what cannot be performed
by exact match. One canonical form per page is the minimum condition for the estate's
machine-citability thesis to be testable at all.

### 1.3 Root-absolute asset paths — a build law

Every asset, script and internal link in every generated file **must** be root-absolute:
`/css/style.css`, `/js/site.js`, `/img/…`, `/toptech/start/diagnostic/`. Relative paths are a
**build failure**, not a style preference.

The source names this *"the single most common way this migration breaks,"* and the failure mode
earns the emphasis. `href="css/style.css"` resolves at depth 0 and fails silently at depths 1, 2
and 3. It does not fail in the build, does not fail in CI, and does not fail on the root hub —
the page most often open while working. It fails at depth, for the reader, with an unstyled page
and no error emitted anywhere; and under the estate's own no-JavaScript law the degraded state is
a page with no chrome at all. Recorded as
[DEF-026](../00-governance-map/defect-register.md#def-026) before a single depth‑1 page exists,
because a defect invisible to the person who causes it belongs in the register in advance.

### 1.4 `navKeyFor()` reads the first path segment

```js
function navKeyFor() {
  var seg = location.pathname.replace(/^\/+/, "").split("/");
  if (seg[0] === "ar") seg.shift();                 // Arabic mirror
  var k = seg[0] || "home";
  var KEYS = ["toptech","method","ascent","metax","academies",
              "credentials","library","license","about"];
  return KEYS.indexOf(k) > -1 ? k : "home";
}
```

Two properties are load-bearing. The `ar` shift means the Arabic mirror needs no separate nav
logic — parity achieved by one line rather than a duplicated code path, and a duplicated code
path is how mirrors drift. The `KEYS` whitelist means an unrecognised first segment falls back to
`home` rather than rendering a nav with nothing active, which is correct for `/search/`, `/404`
and any future off-manifest utility route.

### 1.5 Legacy redirects

| From | To |
|---|---|
| `/index.html` | `/` |
| `/toptech.html` | `/toptech/` |
| `/curriculum.html` | `/toptech/catalog/` |
| `/start-here.html` | `/toptech/start/diagnostic/` |
| `/macrolifetach.html` | `/metax/` |
| `/macrolifetech.html` | `/metax/` |
| `/bcia.html` | `/metax/bcia/` |
| `/bcia-status.html` | `/metax/bcia/status/` |
| `/community.html` | `/academies/` |
| `/academies.html` | `/academies/how-it-works/` |
| `/credentials.html` | `/credentials/` |
| `/verify.html` | `/credentials/verify/` |
| `/library.html` | `/library/` |
| `/lexicon.html` | `/library/lexicon/` |
| `/news.html` | `/library/news/` |
| `/news.html?cat=:c` | `/library/news/:c/` |
| `/detail.html` | `/toptech/catalog/series/` |
| `/article.html` | `/library/news/` |
| `/about.html` | `/about/` |
| `/contact.html` | `/about/legal/contact/` |
| `/privacy.html` | `/about/legal/privacy/` |
| `/terms.html` | `/about/legal/terms/` |
| `/about/demo-notice/` | `/about/universe/demo-notice/` |

All 301. **The misspelling survives in exactly one place, deliberately:**
`/macrolifetach.html` must keep naming the defective URL in order to retire it, and that is the
only sanctioned occurrence of *MacroLifeTach* anywhere in the estate
([C-13](../00-governance-map/corrections-log.md#c-13),
[DEF-023](../00-governance-map/defect-register.md#def-023)). Both spellings redirect, since the
correctly spelt flat file may also have been linked.

Note what this table *is*, at the meta register: a **record of the estate's own history of
addresses**, and the reason a 2026 citation still resolves in 2031. A redirect table pruned for
tidiness is a corpus that has quietly broken its own past. This table only ever grows.

### 1.6 Arabic mirror

Every route has an `/ar/` twin at the identical path. `<html lang="ar" dir="rtl">`, `hreflang`
pair on both, **status badges never mirrored**, numerals Western Arabic, gradients unchanged.

The operative sentence: *"The Arabic page is a translation of equal editorial standing and no
superior authority; a divergence is a defect."* This resolves an apparent tension with
`prevailing_text: "en"`, and the distinction must not be collapsed:

- **Prevailing text** is a conflict rule of last resort — if the two texts say different things,
  English governs.
- **Editorial standing** is a quality obligation — a divergence is a *filed defect*, not an
  accepted consequence of translation.

An estate treating its second language as courtesy translation commits the harm ML‑2.3 §H.22
names while formally complying with it. Reconciled at
[R-55](../00-governance-map/reconciliation-ledger.md#r-55--the-arabic-mirror-has-equal-standing);
shipping order is [RAT-22](../00-governance-map/open-questions-and-ratifications.md#rat-22).

---

## 2. The tier contract — what each altitude is for

| Tier | Route form | Claims something about | Word band | Fails when |
|---|---|---|---|---|
| Root | `/` | What the estate is and who it is for | 1400–1800 | It reads as a product page |
| Pillar hub | `/{pillar}/` | A domain, and why the estate treats it as one | 1400–1800 | It is a table of contents |
| Group hub | `/{pillar}/{group}/` | A method, family or apparatus | 1400–1800 | Its leaves could be its sections |
| Leaf | `/{pillar}/{group}/{leaf}/` | One object, operatively defined | ≥1200 | It repeats its hub, or needs sub-pages |
| Parametric | `/toptech/s/{S##}-{slug}/…` | One instance in an enumerable set | 1400 / 1200 | The set is not actually enumerable |

**The hub rule, as a rule an agent can fail.** A hub is *"a real page with its own thesis, not a
table of contents."* It carries all eight recipe sections **plus** a Map section describing every
child in two to three sentences. The Map is one section, not the page. A hub whose Position,
Definition, Mechanism, Worked instance, Failure modes, Limits, Falsifier and Obligation sections
could be deleted without loss has failed this contract — and the remedy is to delete the hub and
re-parent its children, never to pad it.

**The leaf rule.** A leaf is the altitude at which the estate makes a checkable claim about a
single object. Its diagnostic is the Falsifier section: if you cannot state the observation that
would show the page wrong, you are probably at hub altitude and should say so.

---

## 3. The nine pillars

| Key | Label | Arabic | Hub | Badge | Thesis |
|---|---|---|---|---|---|
| `toptech` | TopTech | توب‑تِك | `/toptech/` | — | Master the machine-mediated internet, learn where it fails, prepare for what replaces it |
| `method` | Method | المنهج | `/method/` | — | The academic apparatus: how a lesson is shaped, how a claim is tested, how a claim expires |
| `ascent` | Ascent | الصعود | `/ascent/` | research-preview | The ten-rung ladder from the computing substrate to the edge of silicon |
| `metax` | Meta-X | ميتا‑إكس | `/metax/` | research-preview | **MacroLifeTech** — the civilizational research umbrella. Nine programs, one of them BCIA |
| `academies` | Academies | الأكاديميات | `/academies/` | — | Found and teach your own academy, Applicant to Institution, on a public record |
| `credentials` | Credentials | الشهادات | `/credentials/` | — | The mastery ladder, the evidence it demands, the public verification that makes it checkable |
| `library` | Library | المكتبة | `/library/` | — | The stack, the standards, the bilingual lexicon, the open data, the corrections record |
| `license` | License | الرخصة | `/license/` | live | The Maher License 2.3 and the register of twenty-five structural harms it makes operative |
| `about` | About | عن ميتا‑إكس | `/about/` | — | The universe, its shared DNA, the curator, the policies, the honest state of the build |

**Three observations that belong in a governance instrument rather than a nav file.**

*First:* `license` is a **navigational pillar**. An estate giving its licence one of nine
top-level slots has made a claim about what it is, and every later argument about whether Part H
is compliance theatre will be measured against that slot. It is the cheapest credibility the
estate will ever buy and the easiest to spend badly.

*Second:* `method` is **an agent's proposal, disclosed as such** — *"`Method` as a ninth pillar is
my addition, not yours."* Adopted **provisionally**, because a route manifest is unusable without
a pillar count, and filed as
[RAT-19](../00-governance-map/open-questions-and-ratifications.md#rat-19). If folded, the cost is
bounded and known: 46 routes re-parent to `/toptech/method/…`, the breakpoint reverts to 1000px,
the redirect table gains 46 lines. **That cost is bounded only while the pages are unwritten**,
which makes RAT-19 the fastest-decaying open question the estate holds.

*Third:* "three pillars" is a **thesis, not a navigation fact**. The conceptual set — TopTech,
Academies, MacroLifeTech (Meta‑X) — survives and is routed at `/about/universe/pillars/`. The
navigational set is nine. Any instrument using the word "pillar" must say which it means
([C-16](../00-governance-map/corrections-log.md#c-16),
[DEF-028](../00-governance-map/defect-register.md#def-028)).

**Badge vocabulary — four values, no fifth.** `live` · `planned` · `research-preview` · `gated`.
Every badge renders a text label, never colour alone. A fifth value is a specification change
requiring a changelog line, because badge inflation is how a status system becomes decoration.

---

## 4. The census

| Pillar | Hub | Group hubs | Leaves | Subtotal |
|---|---:|---:|---:|---:|
| root | 1 | — | — | 1 |
| toptech | 1 | 6 | 29 | 36 |
| method | 1 | 6 | 39 | 46 |
| ascent | 1 | 3 | 20 | 24 |
| metax | 1 | 4 | 29 | 34 |
| academies | 1 | 5 | 32 | 38 |
| credentials | 1 | 5 | 22 | 28 |
| library | 1 | 6 | 29 | 36 |
| license | 1 | 5 | 34 | 40 |
| about | 1 | 5 | 29 | 35 |
| utility | — | — | 3 | 3 |
| **Total EN** | **10** | **45** | **266** | **321** |

Utility routes are `/search/`, `/404` and `/ar/`. The Arabic mirror doubles the total to **642
menu routes**, before §6's parametric families.

**The number the estate must say out loud.** At a 1200-word floor, 321 English routes is
**≈385,000 words**; with the mirror at equal standing, ≈770,000. The source states it
deliberately: *"worth stating out loud before work starts, because it is the real cost of 'no
missed details.'"*

This manifest adopts the census and refuses to treat the word figure as a plan. It is filed as
[RAT-21](../00-governance-map/open-questions-and-ratifications.md#rat-21), and the default posture
until the Curator rules is **staged publication** — ship pillar by pillar with unwritten routes
*absent* rather than thin. The badge vocabulary exists to express exactly that, and staging is
the only one of four available options that never requires publishing a page nobody wrote.

**The failure mode at this volume is not incompleteness.** It is **uniformity** — *"321 pages that
all sound like the same eight-section template."* The mitigation is structural and must be
instructed explicitly: **vary which section leads.** A standards page may open on Definition, a
harm page on the macro frame, a series page on the worked instance. Left unsaid, *"they will all
open on Position."* Carried into [ST-24](../standards/st-24-page-prose-standard.md) as a rule
rather than as advice.

---

## 5. Route tables by pillar

Group hubs in bold; leaves listed beneath.

### 5.1 `toptech` — 36 routes

| Route | Kind | Badge |
|---|---|---|
| `/toptech/` | pillar hub | — |
| **`/toptech/start/`** | group hub | — |
| `/toptech/start/diagnostic/` · `how-to-study/` · `prerequisites/` · `time-budget/` · `what-this-is-not/` | 5 leaves | — |
| **`/toptech/catalog/`** | group hub | live |
| `/toptech/catalog/series/` · `courses/` · `map/` · `decay/` · `changelog/` | 5 leaves | — |
| **`/toptech/branch-a/`** | group hub | live |
| `/toptech/branch-a/flagship-search/` · `flagship-attention/` · `stack/` · `surfaces/` · `archetypes/` | 5 leaves | — |
| **`/toptech/branch-b/`** | group hub | planned |
| `/toptech/branch-b/design/` · `development/` · `data-ai/` · `infrastructure/` · `security/` · `networks/` · `gate/` | 7 leaves | — |
| **`/toptech/branch-c/`** | group hub | planned |
| `/toptech/branch-c/academy-builder/` · `curriculum-design/` · `governance/` | 3 leaves | — |
| **`/toptech/gateways/`** | group hub | gated |
| `/toptech/gateways/ascent/` · `metax/` · `conditions/` | 3 leaves | — |

Branches D and E are **gateways, not branches** in the route grammar: they lead to `ascent` and
`metax`, which are pillars in their own right. A gateway route exists to state a gate condition,
not to host content — which is why `/toptech/gateways/conditions/` is a leaf and not a hub.

### 5.2 `method` — 46 routes

| Route | Kind | Badge |
|---|---|---|
| `/method/` | pillar hub | — |
| **`/method/architecture/`** | group hub | live |
| `arc/` · `cadence/` · `limits/` · `bridge/` · `capstone/` | 5 leaves | — |
| **`/method/rails/`** | group hub | live |
| `compliance/` · `accessibility/` · `decay/` · `falsifiability/` · `kill-criteria/` · `unit-economics/` | 6 leaves | — |
| **`/method/epistemics/`** | group hub | live |
| `evidence-classes/` · `decay-standard/` · `falsifier-grammar/` · `counterproductivity/` · `banned-claims/` · `open-problems/` | 6 leaves | — |
| **`/method/assessment/`** | group hub | planned |
| `scenario/` · `rubric/` · `viva/` · `review/` · `artefacts/` · `ai-disclosure/` | 6 leaves | — |
| **`/method/instruments/`** | group hub | planned |
| `prereg/` · `review/` · `decay-watch/` · `cohorts/` · `artefacts/` · `scenario-engine/` · `viva/` · `exchange/` · `passport/` · `bounty/` · `citations/` · `determinations/` | 12 leaves | — |
| **`/method/notation/`** | group hub | live |
| `symbols/` · `identifiers/` · `versioning/` · `research-ethics/` · `human-subject-exclusion/` | 5 leaves | — |

**Two deliberate near-duplicates.** `/method/assessment/rubric/` and `/credentials/review/rubric/`
both concern the frozen D1–D5 rubric; `/method/assessment/artefacts/` and
`/method/instruments/artefacts/` both concern the Artefact Register. These are **not**
redundancies to be collapsed. The Method route defines the instrument; the Credentials route
states how a candidate is judged by it. Each must open on a different section — Definition and
Mechanism respectively — and each must cite the other in its `Depends on` block. If either can be
written without referring to the other, one of them should not exist.

### 5.3 `ascent` — 24 routes

| Route | Kind | Badge |
|---|---|---|
| `/ascent/` | pillar hub | research-preview |
| **`/ascent/rungs/`** | group hub | research-preview |
| `s38-substrate/` · `s39-paradigms/` · `s40-mathematics/` · `s41-end-of-binary/` · `s42-multivalued/` · `s43-electron-to-cell/` · `s44-biological/` · `s45-embodied/` · `s46-networks/` · `s47-collective/` | 10 leaves · parametric | — |
| **`/ascent/reading/`** | group hub | research-preview |
| `blue/` · `green/` · `gold/` · `sources/` · `citation-rule/` | 5 leaves | — |
| **`/ascent/boundaries/`** | group hub | research-preview |
| `limits-of-silicon/` · `exclusions/` · `banned-claims/` · `passport/` · `status/` | 5 leaves | — |

Every route in this pillar carries `research-preview` and none may carry `live` until the rung
status table at `/ascent/boundaries/status/` says so. A pillar whose subject is the limits of
computation, badging itself confidently, has failed before its first page.

### 5.4 `metax` — 34 routes

| Route | Kind | Badge |
|---|---|---|
| `/metax/` | pillar hub | research-preview |
| **`/metax/umbrella/`** | group hub | research-preview |
| `what-it-is/` · `charter/` · `exclusions/` · `method/` · `publication/` | 5 leaves | — |
| **`/metax/programs/`** | group hub | research-preview |
| `agora/` · `mana/` · `metabolism/` · `soma/` · `paideia/` · `athar/` · `afaq/` · `mizan/` · `bcia/` | 9 leaves · parametric | — |
| **`/metax/bcia/`** | group hub | gated |
| `what-it-is/` · `series/` · `roadmap/` · `document-zero/` · `charter/` · `governance/` · `notation/` · `bibliography/` · `contribution/` · `gateway/` | 10 leaves | gateway: gated |
| **`/metax/bcia/status/`** | group hub | gated |
| `remediation/` · `audit/` · `protocol/` · `defects/` · `open-problems/` | 5 leaves | — |

**The name is MacroLifeTech.** Nav key `metax`, display label `Meta‑X`, prose name **MacroLifeTech
(Meta‑X)**. No page anywhere may render the old spelling
([C-13](../00-governance-map/corrections-log.md#c-13)).

**The route grammar here encodes a correction.** BCIA appears twice by design: as
`/metax/programs/bcia/`, one program among nine, and as `/metax/bcia/`, a group hub with its own
depth. The first is corrective — it is the route that makes the estate's earlier mis-levelling of
BCIA as a *pillar* visibly wrong
([R-42](../00-governance-map/reconciliation-ledger.md#r-42--the-third-pillar-is-macrolifetech-not-bcia)).
The second is a concession to reality: BCIA has more written about it than the other eight
programs combined, and pretending otherwise for symmetry would be its own dishonesty.
`/metax/programs/bcia/` must therefore be a genuine program page that links *up* to the umbrella
and *across* to `/metax/bcia/`, and must state in prose why it has a sibling the others lack.

**`/metax/bcia/status/` is a group hub, not a leaf, and this is the estate's most important
structural decision.** BCIA's honesty layer — remediation, critical audit, publication-readiness
protocol, defect register, scope limits and open problems — is given the same tier as BCIA's
content. A research program routing its own audit at the depth of its own claims has made a
checkable commitment. The demo strip may **never** be suppressed anywhere under `/metax/bcia/`.

### 5.5 `academies` — 38 routes

| Route | Kind | Badge |
|---|---|---|
| `/academies/` | pillar hub | — |
| **`/academies/how-it-works/`** | group hub | live |
| `principles/` · `path/` · `eligibility/` · `sandbox/` · `apply/` · `cost/` | 6 leaves | — |
| **`/academies/levels/`** | group hub | live |
| `l1-applicant/` · `l2-sandbox/` · `l3-provisional/` · `l4-chartered/` · `l5-institution/` | 5 leaves · parametric | — |
| **`/academies/requirements/`** | group hub | live |
| `r1-curator/` · `r2-thesis/` · `r3-curriculum/` · `r4-rubric/` · `r5-charter/` · `r6-technical/` · `r7-bilingual/` · `r8-legal/` · `r9-red-lines/` · `r10-audit/` · `r11-part-h/` | 11 leaves · parametric | — |
| **`/academies/operating/`** | group hub | live |
| `technical/` · `subdomain/` · `design/` · `moderation/` · `exchange/` · `revocation/` | 6 leaves | — |
| **`/academies/record/`** | group hub | live |
| `directory/` · `audits/` · `charters/` · `bounty/` | 4 leaves | — |

**`/academies/requirements/r11-part-h/` is where the License becomes operative on someone other
than the Curator.** Requirement 11 obliges a founding academy to publish its own Part H
Statement. The estate cannot demand that of others while `/license/statement/ours/` is
unpublished — which is why
[RAT-15](../00-governance-map/open-questions-and-ratifications.md#rat-15) gates this pillar as
surely as it gates the License pillar, and why the two routes must link each other directly.

### 5.6 `credentials` — 28 routes

| Route | Kind | Badge |
|---|---|---|
| `/credentials/` | pillar hub | — |
| **`/credentials/ladder/`** | group hub | live |
| `completion-marker/` · `practitioner/` · `professional/` · `master-fellow/` · `contributor/` | 5 leaves | — |
| **`/credentials/evidence/`** | group hub | live |
| `proof-ladder/` · `submission/` · `templates/` · `artefacts/` · `ai-disclosure/` | 5 leaves | — |
| **`/credentials/review/`** | group hub | live |
| `handbook/` · `rubric/` · `conflicts/` · `statistics/` · `appeals/` | 5 leaves | — |
| **`/credentials/lifecycle/`** | group hub | live |
| `renewal/` · `revocation/` · `integrity/` · `registry-spec/` | 4 leaves | — |
| **`/credentials/verify/`** | group hub | live |
| `lookup/` · `how-it-works/` · `limits/` · `revocations/` **(thin)** | 4 leaves | — |

Two routes here are structurally unusual and both deliberate.
`/credentials/ladder/completion-marker/` exists to say a completion marker is **not** a credential
— a route whose whole purpose is to refuse a claim the reader arrived expecting. And
`/credentials/verify/limits/`, "What It Does Not Prove," makes the verification system honest: a
verifier with no stated limit page is an authority claim wearing the costume of a lookup tool.
`/credentials/verify/revocations/` is declared **thin by nature**
([DEF‑2026‑043](../00-governance-map/defect-register.md#def-2026-043)).

### 5.7 `library` — 36 routes

| Route | Kind | Badge |
|---|---|---|
| `/library/` | pillar hub | — |
| **`/library/stack/`** | group hub | live |
| `layers/` · `two-plane/` · `data-tiers/` · `topology/` | 4 leaves | — |
| **`/library/standards/`** | group hub | live |
| `style-guide/` · `symbols/` · `decay/` · `falsifiability/` · `accessibility/` · `bilingual/` · `generation-prompt/` | 7 leaves | — |
| **`/library/lexicon/`** | group hub | live |
| `entries/` · `roots/` · `contested/` · `method/` | 4 leaves | — |
| **`/library/record/`** | group hub | live |
| `mx-instruments/` · `ag-instruments/` · `corrections-log/` · `verification-log/` · `errata/` | 5 leaves | — |
| **`/library/sources/`** | group hub | live |
| `bibliography/` · `citations/` · `downloads/` **(thin)** · `schemas/` **(thin)** | 4 leaves | — |
| **`/library/news/`** | group hub | live |
| `announcements/` · `curriculum/` · `research/` · `field-notes/` · `archive/` | 5 leaves · 4 parametric parents | — |

`/library/record/corrections-log/` is the published face of
[GM-07](../00-governance-map/corrections-log.md), and §1.6 designates it the filing address for
any English/Arabic divergence. It is therefore the one route in the estate that receives defects
from the routing law itself.

### 5.8 `license` — 40 routes

The largest pillar by leaf count, which is a statement of priorities and should be read as one.

| Route | Kind | Badge |
|---|---|---|
| `/license/` | pillar hub | live |
| **`/license/ml-2-3/`** | group hub | live |
| `part-0-preamble/` · `part-a-definitions/` · `part-b-grant/` · `part-c-conditions/` · `part-d-notices/` · `part-e-governance/` · `part-f-breach/` · `part-g-interpretation/` · `part-h-harms/` · `schedules/` · `ml-2-3.txt` | 10 leaves + plain-text mirror | — |
| **`/license/harms/`** | group hub | live |
| `stratum-i-cognitive/` · `stratum-ii-relational/` · `stratum-iii-economic/` · `stratum-iv-material/` · `stratum-v-reflexive/` · `stratum-vi-successor/` · `falsifiers/` | 7 leaves | — |
| **`/license/machinery/`** | group hub | live |
| `absolutes/` · `roles/` · `scale-gate/` · `breach/` · `cure/` · `riba/` | 6 leaves | — |
| **`/license/statement/`** | group hub | live |
| `form/` · `generator/` · `ours/` · `examples/` · `compatibility/` | 5 leaves | — |
| **`/license/falsification/`** | group hub | live |
| `objections/` · `withdrawals/` · `defects/` · `changelog/` · `ml-2-2/` · `open-questions/` | 6 leaves | — |

Plus the parametric harm family `/license/harms/hx-{nn}-{slug}/` — **25 routes**, eight-part form,
floor 1400 (§6.3).

**Three routes here are the estate's integrity expressed as addresses.**

`/license/falsification/` — an entire group hub for objections, withdrawals, defects and open
questions. A licence routing its own falsification at the same tier as its own machinery has made
the strongest available structural commitment to being wrong in public.

`/license/falsification/ml-2-2/` — **and it currently has nothing true to say.** ML‑2.2 does not
exist ([RAT-14](../00-governance-map/open-questions-and-ratifications.md#rat-14), ML‑D‑007). The
route must therefore be built to *state the gap*, not to display a document: it exists to record
that ML‑2.3 declares `supersedes: "ML-2.2"` and grants transition rights to a text the estate has
never held. Building it as an empty archive page would convert an honest defect into a quiet one.

`/license/statement/ours/` — MetaX's own Part H Statement. The source states the position without
softening: it *"still requires MetaX's own Part H Statement to mark HX‑01 and HX‑04 unremedied
because of the AdSense and Adsterra slots on the content plane,"* and warns that if the ads stay,
*"the honest text stays too, and it will sit two clicks from the licence you are asking people to
adopt."* Because the estate is a demo there is a clean window to remove the slots first
([C-14](../00-governance-map/corrections-log.md#c-14)). Either way the route ships; only its
disposition column is undecided.

### 5.9 `about` — 35 routes

| Route | Kind | Badge |
|---|---|---|
| `/about/` | pillar hub | — |
| **`/about/universe/`** | group hub | live |
| `what-it-is/` · `pillars/` · `dna/` · `curator/` · `demo-notice/` | 5 leaves | — |
| **`/about/policy/`** | group hub | live |
| `static-principle/` · `ai-policy/` · `governance/` · `accessibility/` · `security/` · `no-images/` | 6 leaves | — |
| **`/about/status/`** | group hub | live |
| `capacity/` · `defects/` · `determinations/` · `migration/` · `roadmap/` | 5 leaves | — |
| **`/about/access/`** | group hub | live |
| `pricing/` · `free/` · `identity/` · `entitlements/` · `refunds/` | 5 leaves | — |
| **`/about/legal/`** | group hub | live |
| `contact/` · `press/` · `privacy/` · `terms/` · `advertising/` · `cookies/` **(thin)** · `ip/` · `sitemap/` **(thin)** | 8 leaves | — |

**`/about/universe/demo-notice/` is a launch blocker, not a page** —
[B-20](../00-governance-map/launch-blockers.md),
[DEF-025](../00-governance-map/defect-register.md#def-025). The source's §0 prose names it
`/about/demo-notice/` while the `MENU` array places it at `/about/universe/demo-notice/`; **the
`MENU` position governs** and the short form is added to the redirect table as an alias. This is
a divergence *within* the supplied specification, recorded here rather than resolved silently.

**`/about/legal/advertising/` exists and must not be quiet.** An estate running ad networks while
publishing a harms register that names attention expropriation owes its reader an advertising
policy at a findable address, written in the register's own vocabulary rather than in a
compliance idiom. This is the route where HX‑01 and HX‑04 are either defended or conceded.

---

## 6. Parametric families

Parametric routes are generated from a data file, one route per record. They are the only routes
whose count this manifest does not fix, and each carries a **generation gate** — the condition
under which a record becomes a route.

| Family | Route form | Source | Count | Floor | Generation gate |
|---|---|---|---:|---:|---|
| Series | `/toptech/s/{S##}-{slug}/` | `catalog.json` | 47 planned | 1400 | One per series record |
| Course | `/toptech/s/{S##}-{slug}/c{NN}/` | `catalog.json` | ~250 | 1200 | **Only if the series is `live`** |
| Harm | `/license/harms/hx-{nn}-{slug}/` | HX-000 | 25 | 1400 | One per register harm |
| Rung | `/ascent/rungs/{s##}-{slug}/` | `catalog.json` | 10 | 1200 | Enumerated in §5.3 |
| Program | `/metax/programs/{slug}/` | fixed set | 9 | 1200 | Enumerated in §5.4 |
| Lexicon | `/library/lexicon/entries/{root}-{slug}/` | `lexicon.json` | variable | **600** | One per entry |
| Instrument | `/method/instruments/{slug}/` | fixed set | 12 | 1200 | Enumerated in §5.2 |
| Academy | `/academies/record/directory/{slug}/` | `academy.json` | variable | 1200 | Level ≥ L3 Provisional |
| News | `/library/news/{cat}/{slug}/` | `news.json` | variable | natural | One per article |

### 6.1 The series page

Required: eyebrow `SERIES · {S##}`, claim H1, one-sentence deck, status badge, branch, tier,
hours, decay class, thesis (150 w), why-now (200 w), the twelve course rows with the six-beat arc
per course, the Limits module summary, the Bridge lesson statement, the capstone contract, **the
pre-registered hypothesis and null**, the kill criterion, prerequisites, what this series will not
teach, evidence classes used, and the related-page block.

Two of those are unusual enough on a curriculum page to name. A **pre-registered hypothesis and
null** commits the series to a claim about its own effect before anyone enrols. A **kill
criterion** states in advance what result would cause the series to be withdrawn. Together they
make a curriculum falsifiable, which is the estate's entire methodological wager.

### 6.2 The course page, and the rule that suppresses it

Six lesson beats as sections — What, Why, How, Lab, Artifact, Scenario Assessment — each 180–260
words, plus artefact spec and rubric mapping.

**Generated only for series badged `live`.** For `planned` and `research-preview` series, courses
remain fragments on the series page and **no route is emitted**. The reason is the best sentence
in the specification: *"emitting a 1200-word page for an unwritten course is HX‑15 in miniature."*

This is the estate's own harms register operating as a build constraint. A route that exists
because the template could generate it, describing a course nobody designed, is compliance theatre
at page scale — and an estate that would not accept that from a licensee cannot ship 250
instances of it itself.

### 6.3 The harm page

Twenty-five routes, eight-part form: claim, reply, named critics, evidence, ethical mapping,
falsifier, obligation, in-this-estate. Floor 1400. Generated from [HX-000](../harms/) once the
v2026.10.1 re-version exists; until then these routes are **blocked, not thin**
([DEF-021](../00-governance-map/defect-register.md#def-021)). The `named critics` and
`in-this-estate` parts are what distinguish the register from advocacy: the first requires the
strongest objection stated by a real author who holds it, the second requires the estate to say
where it commits the harm itself.

### 6.4 The lexicon exception

Floor **600** — the one sanctioned exception in the estate, explained in a clause: *"a lexicon
entry that runs to 1200 words is an essay, not an entry."* Filed under
[DEF‑2026‑043](../00-governance-map/defect-register.md#def-2026-043).

---

## 7. Off-manifest routes and the dynamic plane

Three utility routes sit outside the pillar grammar: `/search/`, `/404`, `/ar/`.

`/search/` carries an unusual triple duty — search destination, **no-JavaScript fallback**, and
human-readable sitemap — listing every route as plain links grouped by pillar. `SEARCH_INDEX`
becomes generated: one entry per route from H1, deck and section titles, emitted to
`/data/search-index.json`, fetched lazily on first modal open
([DEF-027](../00-governance-map/defect-register.md#def-027),
[R-56](../00-governance-map/reconciliation-ledger.md#r-56--generated-search-and-the-no-js-sitemap)).

The **identity and commerce plane** is off-manifest by design — the plane boundary of MX‑ARCH‑001
expressed as an address space:

| Host | Purpose | Gradient | Motion |
|---|---|---|---|
| `auth.metax.academy/authorize` | Social sign-in only; provider names as text word-marks | `--grad-vault` | **None** |
| `pay.metax.academy/checkout/{sku}` | Binance Pay only, stated plainly | `--grad-ledger` | Static |
| `me.metax.academy` | Dashboard; 48px identity bar; deterministic SVG glyph from `SHA-256(usr_id+salt)` | Inherits viewed pillar | Minimal |
| `verify.metax.academy/c/{id}/` | Flat static credential records | `--grad-verify` | None |
| `hooks.metax.academy/v1/*` | Form endpoints for apply and appeal | — | — |
| `{slug}.metax.academy` | Academy sites inheriting `/css/style.css` unmodified | Per academy | Per DS |

Three design decisions here are governance decisions wearing design clothes. `auth.` uses
deliberately **the quietest gradient in the system**, so a phishing clone reaching for visual
excitement is visibly wrong. `me.` carries **no streaks and no leaderboards** — a direct refusal
of the engagement mechanics HX‑01 and HX‑03 name. And the dashboard borrows the gradient of the
pillar being viewed rather than owning one, because *"the dashboard is a lens, not a brand."*

---

## 8. Capacity

| Component | Files |
|---|---:|
| English menu routes | 321 |
| Arabic mirror | 321 |
| Series ×2 languages | 94 |
| Live courses ×2 | ~500 |
| Harms ×2 | 50 |
| Lexicon, news, programs, rungs, academies ×2 | ~400 |
| Assets, data, redirects | ~300 |
| **Total** | **≈2,000** |

Cloudflare Pages free-tier ceiling is 20,000 files. Headroom ≈18,000 — at ~40 files per new
series, roughly **450 further series**.

**The binding constraint has moved.** The ceiling is no longer it; **Workers requests at
100k/day** are the first tripwire.
[DEF‑2026‑041](../00-governance-map/defect-register.md#def-2026-041) stays open under its original
number, re-characterised as a request-rate constraint wearing a file-count constraint's
identifier. The 80% capacity meter still governs
([R-54](../00-governance-map/reconciliation-ledger.md#r-54--the-file-ceiling-is-no-longer-binding)).

---

## 9. Generated artefacts

Four artefacts derive from this manifest. Each must be emitted at build time, and a hand-edit is a
defect regardless of whether it happens to be correct.

| Artefact | Derived from | Failure if hand-written |
|---|---|---|
| `sitemap.xml` | §§4–6 | Drifts from the route set; search engines index a fiction |
| `/js/site.js` `MENU` | §§3, 5 | Nav shows routes that do not exist, or hides ones that do |
| `/data/search-index.json` | Every page's H1, deck, section titles | Search returns stale titles for changed pages |
| `_redirects` | §1.5 + every retired address | A dropped line silently breaks every citation of the old URL |

The principle generalises, and is why this section exists: a **derived artefact editable
independently of its source will diverge from it**, and the divergence will be found by a reader
rather than by the estate. Nine of the sixteen entries in the
[Corrections Log](../00-governance-map/corrections-log.md) are instances of exactly this class.
Where a divergence can be *removed* rather than *checked for*, removal is the correct remedy —
and generation removes it.

---

## 10. What this manifest does not decide

**Whether `Method` is a pillar.** Nine adopted provisionally;
[RAT-19](../00-governance-map/open-questions-and-ratifications.md#rat-19) is the Curator's, and it
decays — cheap today, expensive at a hundred written pages.

**When the estate leaves demo.** Every route ships with the `.mx-demo` strip until it does.
[RAT-20](../00-governance-map/open-questions-and-ratifications.md#rat-20).

**Whether ≈385,000 words get written.** The census is a shape, not a schedule.
[RAT-21](../00-governance-map/open-questions-and-ratifications.md#rat-21).

**When the Arabic mirror ships.** Parity specified, unbuilt.
[RAT-22](../00-governance-map/open-questions-and-ratifications.md#rat-22).

**The disposition of `/license/statement/ours/`.** The route exists; whether HX‑01 and HX‑04 read
*remedied* or *unremedied* depends on whether the ad slots survive.
[RAT-15](../00-governance-map/open-questions-and-ratifications.md#rat-15).

**What any page contains.** That is [ST-24](../standards/st-24-page-prose-standard.md) and the
[Page Contract](page-contract.md).

---

## 11. Falsifier

This manifest is wrong if any of the following is observed:

1. A published address on `metax.academy` appearing in no table here, and not a §6 parametric or
   §7 utility route.
2. A leaf whose page cannot be written without repeating its group hub — showing the three-tier
   grammar to be one tier too many for that family.
3. A group hub whose eight recipe sections are unwritable without padding — showing it to be a
   table of contents and its children to be its sections.
4. A route in `MENU` that 404s, or a route in these tables absent from `MENU`.
5. A relative asset path at depth ≥1 that nonetheless resolves — which would falsify §1.3's build
   law rather than confirm it.

Each is checkable by a build step; none is checkable by rereading this document. That asymmetry
is the point — a manifest whose correctness can only be established by rereading it has no
falsifier at all.

---

## 12. Obligation

For the **build agent**: root-absolute paths (§1.3), both `hreflang` tags and the trailing-slash
canonical (§1.2), the demo strip ([B-20](../00-governance-map/launch-blockers.md)). No route
emitted that is not in this manifest; no course route for a non-`live` series (§6.2).

For the **editor**: adding a route means adding it here first, at the correct tier per §2, with a
badge from the four permitted values and a changelog line at
[`changelog.md`](../00-governance-map/changelog.md). Retiring a route means adding a `_redirects`
line, never deleting an address.

For the **reader**: every address here is meant to be citable in five years. If one is not, that
is a defect, and you may file it at `/library/record/corrections-log/`, which exists for that
purpose and publishes rejected submissions with reasons.

---

**Related:** [Page Contract](page-contract.md) · [Routing Law](routing-law.md) ·
[ST-24 Page Prose Standard](../standards/st-24-page-prose-standard.md) ·
[DS-07 Navigation Geometry](../design/ds-07-navigation-geometry.md) ·
[DS-00 As-Built Token Layer](../design/ds-00-as-built-token-layer.md) ·
[Reconciliation Ledger Part 4](../00-governance-map/reconciliation-ledger.md) ·
[Defect Register](../00-governance-map/defect-register.md) · [ML-2.3](../license/ml-2-3.md)

*Curated by Maher. 321 English routes, 45 group hubs, 266 leaves, nine pillars — one of which is
an agent's disclosed proposal, and all of which are provisional until the estate leaves demo.
Derived from MX‑NAV‑SPEC v2026.10.1; this document governs where the two disagree, and the
disagreement is a defect.*
