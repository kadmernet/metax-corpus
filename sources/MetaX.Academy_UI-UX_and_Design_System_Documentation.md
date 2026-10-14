# MetaX.Academy — UI/UX & Design System Documentation
**Corpus ref MX‑DESIGN‑001 · Release v2026.09.2 · Curated by Maher**
*Supersedes the component notes in v2026.08.12; extends the sitemap in v2026.09.1*

---

## Part 0 — The architectural correction this release forces

Everything you have just asked for — authentication, payment, per‑user dashboards that "infect all MetaX subdomains," per‑academy subdomains — collides head‑on with the Static Principle published at `metax.academy/about/static/`. That page currently claims "no database, no login wall, no client‑side fetch." As of this release that claim becomes false, and a false claim on a doctrine page is exactly the failure mode this universe exists to prevent. So the principle is not abandoned; it is **partitioned**, and the doctrine page is rewritten rather than quietly contradicted.

**The two‑plane model.** MetaX now runs two planes with a hard boundary between them.

The **Content Plane** (`metax.academy`, `toptech.`, `bcia.`, `academies.`, `library.`, `lexicon.`, `verify.`, and every `{academy}.metax.academy`) remains fully static, pre‑rendered, archivable, and crawlable. Every content page must render completely, correctly and legibly for an anonymous visitor with JavaScript disabled. No content page may gate its primary text behind a session.

The **Identity & Commerce Plane** (`auth.`, `pay.`, `me.`) is dynamic, stateful, non‑indexed, and never archived. It holds sessions, entitlements, payment intents and learner artefacts.

The boundary rule is one sentence and it is load‑bearing: **the content plane may be *decorated* by the identity plane but never *depends* on it.** Concretely, a signed‑in visitor on a series page sees the same HTML as an anonymous visitor, plus a hydrated identity bar and up to three inline entitlement chips injected by a single ~4 KB island script reading a short‑lived signed token. If that script fails, times out, or is blocked, the page is unchanged and unbroken. This is the only sanctioned exception to "no client‑side fetch," and `/about/static/` gains a new section, *Where the principle bends*, stating it explicitly with its date.

**Second correction, on gradients.** The existing identity is Ink and Paper — austere, print‑derived, deliberately unfashionable. Gradients can be added without destroying that, but only if they are confined to a defined layer. The rule adopted here: **gradients are chrome, never substrate.** They live in hero fields, section rules, badge fills, focus states and edge treatments. Body copy always sits on flat Paper or flat Ink. Any gradient that ever appears behind running text is a defect, logged as such. This gives you the modern surface you asked for while keeping the reading experience at AA contrast without heroics.

---

## Part 1 — Foundations

### 1.1 Mobile‑first, and what that actually constrains

Every component is authored at 360 px first and enhanced upward. No component may be designed at desktop and "made responsive" afterwards; the build lints for desktop‑only CSS that lacks a mobile counterpart.

| Token | Min width | Columns | Gutter | Container | Primary use |
|---|---|---|---|---|---|
| `xs` | 360 | 4 | 16 | 100% − 32 | Baseline phone |
| `sm` | 480 | 4 | 20 | 448 | Large phone |
| `md` | 768 | 8 | 24 | 720 | Tablet portrait |
| `lg` | 1024 | 12 | 24 | 960 | Tablet landscape / small laptop |
| `xl` | 1280 | 12 | 32 | 1180 | Desktop |
| `2xl` | 1600 | 12 | 32 | 1320 (capped) | Large desktop |

Reading measure is capped at 68 characters at all widths — the container may grow, the paragraph may not. Touch targets are minimum 44 × 44 px with 8 px separation. All primary actions on `xs` and `sm` sit within the bottom 40% thumb zone or in a sticky action bar; secondary and destructive actions never do.

Type is fluid via `clamp()` on a 1.200 minor‑third mobile scale expanding to 1.250 at `lg`. Display sizes are the only place letter‑spacing is negative. Latin family is a transitional serif for H1/H2 and a grotesque for UI; the Arabic pairing is a Naskh‑derived family with matching x‑height so bilingual pages do not visually jump between locales. Arabic never uses faux‑bold or faux‑italic; weight comes from the family or not at all.

Layout uses CSS logical properties throughout (`margin-inline-start`, not `margin-left`) so the Arabic RTL mirror is a `dir` attribute change, not a second stylesheet. Exceptions that never mirror: code blocks, terminal output, LTR identifiers such as `S042`, chart x‑axes representing time, and the credential identifier field.

### 1.2 The gradient system — one per brand

Each gradient is a three‑stop linear ramp defined once in `mx-tokens` as a custom property, with a mandated solid fallback for text and small surfaces.

| Brand / surface | Gradient name | Stops | Angle | Character |
|---|---|---|---|---|
| MetaX Hub | **Meridian** | `#2A2F36 → #7A5A2A → #B4884A` | 135° | Curator gold rising out of ink |
| TopTech | **Forge** | `#4A2E14 → #A5642A → #E3A857` | 120° | Brass, worked metal, warm |
| Ascent | **Ridge** | `#1E3A44 → #3C6E7F → #7FB2C0` | 150° | Cold steel, altitude |
| BCIA | **Nucleus** | `#241E3A → #4B3F72 → #8B7BB8` | 135° | Violet, laboratory, unresolved |
| Academies | **Kiln** | `#3A2216 → #9A5B3E → #D08F6A` | 120° | Clay, fired, built by hand |
| Credentials & Verify | **Seal** | `#12332B → #2E6F5E → #6FAE99` | 160° | Green, attested, closed |
| Library & Lexicon | **Slate** | `#1B2126 → #55606B → #97A3AC` | 180° | Neutral, archival |
| Auth | **Vault** | `#0A0C0F → #1C2530 → #33465C` | 90° | Cold, sober, unmistakable |
| Pay | **Ledger** | `#12242E → #1F4E5F → #2E7285` | 90° | Restrained, financial, no glow |
| Me (dashboard) | **Desk** | `#F6F4EF → #EFEAE0 → #E9E4D9` | 135° | Near‑flat paper; user content dominates |

Five rules govern their use. Gradients may not carry semantic meaning — semantic state is `mx-statusbadge` colour only (valid `#2E6F5E`, pending `#C98A17`, defect `#A33227`, frozen `#5A6472`), and no brand gradient may use a semantic hue as its dominant stop. Maximum two gradient surfaces are visible in any single viewport. `background-clip: text` is permitted only at display sizes ≥ 32 px and always ships a solid‑colour fallback. Any gradient adjacent to text must pass 4.5:1 against its *darkest and lightest* stop, tested at both, not at the midpoint. And Auth and Pay gradients are locked — an academy may not theme them, because a payment screen that looks different on every subdomain is a phishing surface.

Academy subdomains get a constrained sixth option: one hue chosen from a 12‑swatch wheel, from which the build derives a three‑stop ramp at fixed lightness values. They cannot supply arbitrary hex. This keeps a thousand academies visually distinct and structurally identical.

---

## Part 2 — Motion and attention

You asked for animation to draw attention to important elements. The risk is obvious: a corpus that rejects attention economics cannot itself run on attention mechanics. The resolution is a strict four‑tier hierarchy where motion earns its place by carrying information.

**T0 — Static.** Body copy, tables, source lists, legal text. Never animates. This is roughly 80% of the estate by page count and that ratio is a budget, not an accident.

**T1 — Entrance reveal.** One‑shot, on first viewport entry, 240 ms, 12 px translate plus opacity, staggered 40 ms across siblings, capped at six staggered items. Applied to `mx-archetypecard`, `mx-branchmatrix` cells, `mx-principlegrid`, `mx-seriescard` grids. Never replays on scroll‑back.

**T2 — State feedback.** 120–180 ms, responds to input: hover lift on cards (2 px, desktop pointer only), focus ring bloom, accordion expansion of `mx-lessonarc`, mega‑nav panel open, toast entry. Cursor‑following and parallax effects are prohibited estate‑wide.

**T3 — Persistent signal.** The only tier allowed to loop, and only four elements ever qualify: a `DEFECT` badge, a `GATED` badge on the BCIA Gateway, a revoked credential result on the verifier, and an expired‑decay chip past its review date. The loop is a 2.4 s opacity breath between 0.72 and 1.0 with no scale change, and it stops permanently after eight cycles or on any user interaction. Nothing celebratory loops. There is no confetti in this universe.

**Named animations.** `mx-reveal` (T1 base). `mx-countup` — computed statistics in `mx-metastrip` count from zero over 900 ms, easing out, with the final value present in the DOM from the start so it is correct without JS. `mx-bridge-draw` — on a series page, an SVG line draws from the Limits panel to the Bridge card over 600 ms, making the pedagogical dependency physically visible. `mx-limits-unfold` — the four limit classes stagger open, epistemic first, economic last, in the order MetaX considers them binding. `mx-ladder-climb` — Ascent rungs illuminate sequentially on entry, 80 ms apart, stopping at the visitor's current rung if the identity bar reports one. `mx-verify-stamp` — the verification result lands with a 180 ms scale‑from‑1.04 and a single subtle shadow settle; this is the one moment in the estate designed to feel consequential. `mx-gate-lock` — a gated card's border draws closed rather than pulsing.

**Reduced motion.** `prefers-reduced-motion: reduce` is honoured absolutely, not softened. T1 becomes instant opacity 1. T2 becomes instant state change. T3 becomes a static high‑contrast outline plus a text label — the information survives, the motion does not. `mx-countup` prints the final number immediately. `mx-bridge-draw` renders the completed line.

**Performance contract.** Only `transform` and `opacity` are animated. No scroll‑linked layout animation. Cumulative Layout Shift target 0.00, hard ceiling 0.05. INP under 200 ms at p75 on a mid‑tier Android device on 4G. Total animation CSS under 6 KB. Any component that cannot meet this ships without motion.

---

## Part 3 — Responsive behaviour of the named components

The mega‑nav is the hardest case. Below `md` it is a full‑screen drawer opening from the inline‑end edge, pillar‑first: seven pillar rows, each expanding in place to reveal its sections, with `mx-statusbadge` preserved at every level because status is structural and must not be a desktop luxury. The utility bar (Start Here · Verify · Search · EN/ع) becomes a fixed four‑icon row at the drawer's foot, always reachable by thumb. At `lg` and above it becomes the seven‑pillar horizontal bar with drop panels capped at four columns by seven links, opening on 120 ms fade with no slide.

`mx-branchmatrix` stacks to five full‑width cards on `xs`, becomes a 2 × 3 grid at `md`, and resolves to the true five‑column matrix at `lg`. `mx-facetedtable` — used by the catalog, the directory and the record — renders as a card list on `xs` with the three highest‑value fields visible and the rest behind a disclosure, converts to a horizontally scrollable table with a sticky first column at `md`, and becomes a full table with column sorting at `lg`; the facet rail is a bottom sheet on mobile and a persistent inline‑start rail on desktop. `mx-lessonarc` is a six‑step accordion on mobile with one beat open at a time, and a two‑column stepper with a persistent progress rail on desktop. `mx-ladder` stays vertical at every breakpoint — the Ascent is a climb and rotating it horizontally would be a lie about the content — but gains an inline‑start progress rail and rung annotations at `lg`. `mx-leveltable` for the five academy levels flips from a table to five stacked level cards below `md`, each carrying its entry criteria, rights, obligations and downgrade triggers as labelled pairs. `mx-limitspanel` and `mx-defectcard`, the two highest‑fidelity components, are single‑column everywhere; they are never compressed into a grid, at any width.

---

## Part 4 — `auth.metax.academy`

**Purpose.** One authentication authority for the entire estate, including every academy subdomain. No academy ever collects a MetaX credential.

**Design posture.** Deliberately austere and deliberately *identical everywhere*. Single column, 400 px maximum, Vault gradient field, no mega‑nav, no footer links except a single "Return to metax.academy," no advertising slot, no marketing copy of any kind. The visual sameness is a security feature: a user who sees a colourful, branded, academy‑themed login screen is being phished, and the docs say so in plain words on `/how-we-protect-you/`.

**Flow.** Standard authorization‑code with PKCE. A relying subdomain redirects to `https://auth.metax.academy/authorize` with its registered `client_id`, a `redirect_uri` drawn from the allowlist, `state`, `nonce` and a code challenge. On success the user returns to `https://{sub}.metax.academy/auth/callback`, which exchanges the code server‑side at the edge and sets a host‑scoped session cookie plus a short‑lived signed identity token (10 minutes, silently refreshed) readable by the island script on the content plane. The session cookie is never scoped to `.metax.academy` wildcard; each host holds its own, and cross‑host continuity comes from a silent re‑authorize against the auth host's own first‑party session. This is what makes `me` "infect" all subdomains without a shared cookie that any single compromised academy could steal.

**Callback registry.** `clients.json` holds one record per relying host: client id, display name, exact redirect URIs, allowed scopes, logo, and charter status. Academy subdomains are auto‑registered at charter grant with the fixed URI `https://{slug}.metax.academy/auth/callback` and a scope ceiling of `profile openid entitlements:read`. Wildcard redirect URIs are rejected at registration. Custom‑domain academies at Chartered level register a second exact URI after domain verification.

**Methods, in order of preference.** Passkeys first, presented as the default and not as an advanced option. Email one‑time code as the universal fallback. Recovery codes issued once at enrolment, shown once, downloadable as a printable card. TOTP for reviewers, academy curators and anyone holding a P3 credential. No SMS. No social login — a third‑party identity provider inside a corpus about provenance would be an unforced contradiction.

**Anti‑phishing.** At first enrolment the user picks a safety glyph from the `mx-glyph` set and a two‑word phrase. Both are shown on the authorization screen *before* any credential entry, on every subsequent sign‑in. The screen also prints the requesting client's display name and charter status from `clients.json`, so a sandbox academy cannot present itself as a chartered one.

**Screens and their copy intent.** `/authorize` states plainly which site is asking and for what. `/signin` leads with the passkey button. `/otp` shows the code's expiry as a countdown that is informational, never pressuring. `/consent` lists scopes in human sentences ("See which courses you have access to"), not scope strings. `/devices` lists active sessions with device, location approximation, last use, and a single revoke control per row plus revoke‑all. `/recover` is deliberately slow and states the delay honestly. `/error` explains failure classes in plain language and never blames the user. `/signout` confirms which sessions ended.

---

## Part 5 — `pay.metax.academy`

**Purpose.** All commerce in the universe, for MetaX itself and on behalf of chartered academies. Binance Pay is the first and currently the only method; the interface is built method‑agnostic from day one so adding a second processor is a configuration change, not a redesign.

**Design posture.** Ledger gradient, sober, near‑monochrome, generous whitespace, no imagery. The estate's no‑dark‑patterns rule is enforced hardest here: no countdown timers on prices, no fake scarcity, no strike‑through anchoring, no pre‑ticked boxes, no upsell interstitial between payment and receipt, and no "are you sure you want to miss out" on cancel. Cancellation is a primary‑weight link, not a grey whisper.

**Flow.** A content‑plane page carries a static price and a single link to `https://pay.metax.academy/checkout/{sku}`. The pay host creates an intent, displays the order summary, and on confirmation redirects to the Binance Pay checkout. Binance returns the user to `https://pay.metax.academy/return/{intent}` while the authoritative state change arrives independently via a signed webhook — the return URL is treated as a hint, never as proof of payment. On webhook confirmation an entitlement record is written, and the user is redirected to `https://me.metax.academy/entitlements/?new={intent}`. If the webhook is slow, `/processing/{intent}` polls with an honest message and an explicit "you may close this page; your receipt will be emailed" statement.

**Screens.** `/checkout/{sku}`, `/methods`, `/confirm/{intent}`, `/processing/{intent}`, `/receipt/{id}` (permanent, static, individually addressable, printable), `/failed/{intent}` with a plain diagnosis and a retry that reuses the intent, `/refunds` stating the policy before purchase rather than after, `/entitlements` redirecting to `me`, and `/invoices` for academy payouts.

**Currency and volatility.** Prices are declared in a single fiat display currency and settled in the crypto amount quoted at intent creation, with the quote's validity window stated on screen. The receipt records both the fiat display figure and the settled amount and asset, because a receipt that records only the crypto amount is useless for accounting a year later.

**Riba constraint.** MX‑000 refuses Core Riba instruments, and that refusal has direct UI consequences: no interest‑bearing instalments, no financing partners, no late fees computed as a percentage of an outstanding balance, and no buy‑now‑pay‑later integrations. Permitted patterns are single payment, zero‑markup split payment where the total never exceeds the single‑payment price, sponsored seats, and needs‑based waivers. The pricing page must show that split payment costs exactly the same as paying at once — that equality is the compliance evidence, displayed rather than asserted. I should note plainly that I am not a lawyer, a financial adviser, or a scholar of Islamic finance; the structural rule is clear, but before launch this should be reviewed by someone qualified in each of those three domains, and jurisdictional availability of crypto payment rails varies considerably and will need its own check.

**Accessibility of money.** Every price is text, never an image. Currency symbols carry `aria-label`. Amount fields use `inputmode="decimal"`. Arabic locale renders numerals per the user's locale preference with the Latin‑numeral equivalent available, because financial ambiguity across numeral systems is a real error source.

---

## Part 6 — `me.metax.academy`

**Purpose.** The single profile and dashboard, and the source of the identity overlay that appears across the whole estate.

**The MetaX Bar.** A 48 px bar injected at the top of every content‑plane page by the island script when a valid identity token exists. It shows the user's glyph and name, current path, one contextual chip (for example "You have access to this series" or "Rung 4 of 10"), and a link to `me`. Anonymous visitors see nothing — no login prompt, no dismissible banner, no space reserved that would cause layout shift. The bar is `position: sticky` on desktop and static on mobile, where vertical space is scarcer than convenience.

**Dashboard sections.** *Path* shows the chosen archetype and the six‑to‑eight selected series with artefact‑based progress. *Artefacts* is the working portfolio. *Credentials* lists held credentials with proof rung and verification links. *Entitlements* lists purchased and granted access with source and expiry. *Reviews* appears for those with reviewer standing. *Academy* appears for founders and links to their subdomain's admin. *Decay Watch* lists claims in the user's completed material that have passed review date. *Settings*, *Data* (export, deletion, and the honest note that public credential records revoke rather than delete), *Devices*, and *Digest*.

**Progress is measured in artefacts, not minutes.** There is no video‑percentage bar, because a percentage of a video watched is not evidence of anything. A series shows courses with an artefact submitted, an artefact reviewed, and a capstone pre‑registered — three binary states, no fabricated continuum.

**Anti‑engagement commitments, stated in the UI itself.** No streaks. No leaderboards. No infinite feed. No notification badges with counts designed to itch. Notifications are a weekly digest, off by default for everything except credential status changes, review deadlines and decay alerts. This is written on `/me/digest/` as a commitment with a falsifier: if MetaX ever ships a streak counter, that page becomes a published defect.

---

## Part 7 — Academy subdomains

Each chartered academy receives `{slug}.metax.academy`, provisioned at charter grant, static, on the shared component library, driven by its `academy.json` manifest. The manifest supplies name, curator, level, accent hue index, language set, curriculum index and audit history; the build derives the theme ramp, routes, and directory entry from it.

Four things an academy cannot change: the `mx-statusbadge` colour semantics, the shape and copy of `mx-limitspanel` and the Bridge card, the footer standing strip showing level and last audit date, and anything on `auth` or `pay`. Sandbox academies carry a persistent, non‑dismissible banner and are excluded from search indexing. Provisional academies carry a lighter standing notice. Chartered academies may add a verified custom domain, which changes the URL but not a single component.

The academy admin surface lives at `me.metax.academy/academy/{slug}/`, not on the academy's own subdomain, which keeps the academy subdomain entirely static and keeps all privileged operations behind one audited plane.

---

## Part 8 — Certification surfaces

A certification is three artefacts that must never disagree. The **record** is the permanent static page at `verify.metax.academy/c/{id}/`, carrying JSON‑LD, the plain‑language assertion, the proof rung, the evidence hash, reviewer signatures and revocation status. The **document** is a printable A4/Letter PDF generated at issuance, bilingual, with the assertion in both Arabic and English, the short verification code, a QR to the record, the proof rung rendered as a four‑segment indicator with the earned segments filled, and — critically — a line stating what the credential does *not* assert. The **share card** is a build‑generated OG image using the Seal gradient, showing credential type, rung and code only, never the holder's photo.

Revoked credentials do not vanish. The record page remains, the status flips to a T3 defect state, the ground for revocation is stated, and the PDF's QR resolves to the same honest page. A verification system that can quietly delete is not a verification system.

---

## Part 9 — Twelve additional academic features

**1. The Pre‑Registration Desk** (`me.metax.academy/prereg/`, public mirror at `toptech.metax.academy/prereg/{id}/`). Before a capstone begins, the learner files a hypothesis, an explicit null, a decision rule and a stopping condition. The filing is hashed and timestamped, and it publishes automatically when the capstone concludes — whatever the result. The UI deliberately makes editing after the start impossible rather than merely discouraged; the edit control is replaced by an "amend with public diff" control. Failure mode it prevents: the retrofitted success story, which is the single most common lie in professional education.

**2. Adversarial Review Exchange** (`me.metax.academy/reviews/`). A reciprocity market: you receive one structured critique for each one you deliver, scored against the frozen D1–D5 rubric. Reviewers are calibrated against gold‑standard artefacts quarterly, and inter‑reviewer agreement is published in the Integrity Report. The UI shows the rubric dimensions as a five‑axis form, forces a stated weakness before a stated strength, and refuses submission of a review under 120 words. Anonymous by default, de‑anonymised on mutual consent.

**3. Decay Watch** (`library.metax.academy/decay/` and a personal view in `me`). Every claim in the estate carries a class and a review date. This surface lists what is overdue, by pillar, with a public count on the hub's honesty strip. Learners subscribe per series and receive a digest line when material they have completed expires. The uncomfortable feature is the point: MetaX publishes its own staleness.

**4. Time‑Boxed Asynchronous Cohorts** (`toptech.metax.academy/cohorts/`). Ninety‑day capstone cohorts with a fixed open and a fixed permanent close. No live video requirement, no timezone tyranny — the cadence is weekly artefact drops and peer critique windows. When a cohort closes it becomes a read‑only public archive including the post‑mortems, so cohort N+1 learns from cohort N's failures. The UI shows a cohort's calendar as a single vertical spine with three states per week: due, delivered, reviewed.

**5. The Artefact Vault** (`me.metax.academy/artefacts/`). Version‑controlled, content‑hashed storage for capstone evidence. Each artefact gets a permanent citable identifier and an optional public URL. Because the hash is recorded in the credential record, evidence cannot be swapped after certification. Supports documents, datasets, repositories by reference, and recorded walkthroughs. Storage quotas are stated in plain numbers on the pricing page.

**6. Deterministic Scenario Assessment** (`/s/{id}/c/{nn}/scenario/`). The sixth beat of the lesson arc, built as a seeded branching scenario with a fixed decision tree and published scoring logic. No language model participates in scoring. The learner can, after completion, open the full tree and see every path not taken and its consequence — the debrief is the actual teaching, and the assessment is the pretext.

**7. The Mastery Viva** (`me.metax.academy/viva/`). The P3 rung's oral defence: a scheduled sixty‑minute examination by two calibrated reviewers, with a published question bank of domain areas but not questions. The transcript is published with holder consent; the outcome is published regardless. This is the operational meaning of "mastery is judgment under scrutiny," and until it existed that sentence was a slogan.

**8. The Citation Ledger** (`library.metax.academy/citations/`). Every source in the estate, monitored for link rot, retraction and version drift, with an archived snapshot recorded at citation time. Each source shows a health state, and any lesson citing a retracted source is automatically flagged as a defect on its own page within one build cycle. Learners see source health inline as a small state marker next to each citation.

**9. The Bridge Passport** (`me.metax.academy/passport/`). A cumulative record of which Limits modules and Bridge lessons a learner has completed, rendered as a ladder. It is not decorative: Ascent rung entry and any future Branch E access are gated on specific passport entries, so the passport is the mechanism that makes the Limits‑before‑Bridge doctrine binding rather than advisory.

**10. Academy Exchange** (`academies.metax.academy/exchange/`). Chartered academies publish modules against a shared schema, and cross‑credit recognition is expressed as explicit equivalence mappings, each requiring both curators' signatures and a stated basis. The UI shows a mapping as a two‑column comparison of learning outcomes with the delta highlighted, so recognition is always inspectable rather than mutual back‑scratching.

**11. The Correction Bounty** (`library.metax.academy/corrections/`). Public defect submission against any page in the estate. Accepted corrections are credited by name in the changelog and on the corrected page's stamp, and contributors accumulate a Corrections standing visible on their profile. The ledger publishes rejected submissions too, with reasons, which is what stops the queue becoming a black box. Categories: factual error, stale claim, broken citation, accessibility defect, notation inconsistency, translation divergence.

**12. The Determination Queue** (`metax.academy/about/governance/queue/`). Every pending governance decision — charter applications, appeals, ethics reviews, licence determinations — visible as an anonymised queue with filing date, class, service‑level target, and an escalation timer that turns amber then red in public when a target is missed. Under AG‑000 §A.6 degraded mode, the queue displays the degraded banner and the reduced authority ceiling. Governance that can be watched is governance that can be held to account, and this is the feature that makes the Curator's own performance falsifiable.

Two further slots are reserved and deliberately unspecified — an Arabic Translation Bench and an Open Problem Claims register — so that the roadmap has stated capacity for growth rather than presenting itself as complete.

---

## Part 10 — Cross‑cutting standards

**Accessibility.** WCAG 2.2 AA is the floor, and gradient surfaces are tested against both extreme stops rather than the midpoint. Focus indicators are a 2 px accent ring plus a 1 px inverse offset ring, visible on every background including gradients. All state conveyed by colour is duplicated in text or glyph. Every animation has a reduced‑motion equivalent that preserves the information. Forms on `auth` and `pay` are tested with screen readers in both locales, because those are the two surfaces where a failure has material consequence.

**Performance budgets, enforced at build.** HTML ≤ 60 KB, CSS ≤ 40 KB estate‑wide (a single shared file), JS ≤ 12 KB on the content plane and ≤ 60 KB on the identity plane, fonts ≤ 180 KB subset per locale with `font-display: swap` and metric‑compatible fallbacks. LCP under 1.8 s on 4G mid‑tier. A page exceeding budget fails the build; there is no override flag.

**Error and empty states.** Every error page states what happened, what it means, what the visitor can do, and who to contact, in that order, without apology inflation. Empty states in `me` are written as invitations with a single action, never as scolding. The 404 routes intelligently: an unknown `/s/{id}/` looks up the identifier and offers the archived or superseded page if one exists.

**Analytics posture.** Aggregate, cookieless, no per‑user tracking on the content plane, no third‑party tags anywhere, and the metrics collected are published on the accessibility and integrity pages so the measurement itself is inspectable.

---

## Part 11 — Documents this release obliges you to change

Adding identity and money to the corpus is a governance event, not a design event. The following must be amended before launch, and the design work should not ship ahead of them: `/about/static/` gains the two‑plane model and *Where the principle bends*; MX‑003 Privacy adds Class 4 (authentication and payment data) to the classification canon; MX‑002 Terms adds purchase, entitlement and refund terms; MX‑011 Security adds session, key and webhook handling; MX‑018 Retention adds payment record periods with their statutory basis; MX‑008 Moderation extends to academy subdomains; and two new instruments are required — **MX‑020 Payments & Commerce** and **MX‑021 Identity & Sessions**. On the agent side, AG‑000 must be amended to place all payment mutation, session revocation and entitlement changes in the absolute‑refusal set, since these are exactly the operations an agent must never perform even under a valid Curator prompt.

---

## Part 12 — Build order

Ship the token layer and the gradient system first, because every later decision inherits from it. Then the responsive chrome — utility bar, mega‑nav drawer, footer, page stamp — at mobile fidelity before desktop. Then the status spine, since badges are structural and cannot be retrofitted. Then `auth`, alone, with nothing depending on it, so it can be penetration‑tested in isolation. Then `me` with the identity bar and the island contract, proving the content plane still renders perfectly with the island disabled. Then `pay`, last of the three planes, because a payment surface built before its identity foundation is stable is a liability. Then the academy subdomain template. Then the twelve features, in the order 1, 3, 9, 2, 11, 5, 6, 4, 8, 12, 7, 10 — pre‑registration, decay watch and the passport first because they make existing doctrine binding, and the viva and the exchange last because they require human capacity that does not yet exist.

**One thing to decide before any of this is drawn.** Crypto‑only payment via a single processor is a real access constraint — it will exclude a meaningful share of the audience this curriculum is written for, particularly in the Arabic‑speaking markets where Meta‑X is authoritative, and it couples the universe's commerce to one company's regional availability and terms. The design here is method‑agnostic precisely so that constraint is temporary, but I would treat "second payment method" as a launch‑blocking item rather than a roadmap item, and I would state the current limitation on the pricing page rather than let visitors discover it at checkout.