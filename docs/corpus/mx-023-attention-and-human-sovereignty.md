---
doc_id: "MX-023"
title_en: "Attention and Human Sovereignty"
title_ar: "الانتباه والسيادة الإنسانية"
family: "corpus"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 3
depth: 5
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["corpus", "attention", "autonomy", "design-ethics"]
route: "/about/policy/ai-policy/"
required_by: "ML-2.3 Part H, Stratum I"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# MX-023 · Attention and Human Sovereignty

**What this instrument is.** The estate's position on the reader's attention: what MetaX may ask
of it, what it may never do to obtain it, and what the estate owes a reader who wants to stop.

**Why it is a corpus instrument and not a design guideline.** [DS-02](../design/ds-02-motion-and-attention.md)
states which animations are permitted. That is a consequence. The premise — that a reader's
attention is theirs and that an institution addressing them has duties to it — is a claim about
persons, which puts it in the corpus. ML-2.3 Part H Stratum I made the instrument necessary:
HX‑01, HX‑02 and HX‑03 impose duties that must land somewhere in the estate's own doctrine, not
only in its licence.

**Numbering note.** MX-023 was allocated for this instrument in v2026.09.4, which pushed the
architecture source's proposed "MX-022 Infrastructure & Migration" to
[MX-024](mx-024-infrastructure-and-migration.md) — numbers are immortal from first assignment
([ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md#3-rule-2--numbers-are-immortal)).

---

## 1. Position

Every other instrument in this corpus governs what the estate **publishes**. This one governs how
the estate **addresses a person**, and the two are not the same subject.

An institution can publish accurate, well-sourced, falsifiable material and still treat its
readers as a resource — by measuring their return rather than their learning, by making leaving
harder than staying, by designing the page so that the next action is chosen for them. Nothing in
[ST-04](../standards/st-04-falsifiability-and-claim-cards.md) or
[ST-07](../standards/st-07-evidence-and-verify.md) would catch that, because those standards
examine claims and this failure is in the *frame around* the claims.

Its parent is [MX-000 §0.3](mx-000-charter.md#03-shared-dna), which makes correctability one of
four Shared DNA properties; its siblings are [MX-009](mx-009-advertising-and-commercial.md) on
advertising and [MX-007](mx-007-ai-use-and-disclosure.md) on AI disclosure. Its published route is
`/about/policy/ai-policy/`, and it is cited by every duty in
[HX-002 Stratum I](../harms/hx-002-harm-instrument-map.md).

**The macro frame, which is the reason this instrument is written at all.** The dominant business
model of the machine-mediated internet is the conversion of human attention into inventory, and
its dominant design literature is the study of how to obtain attention that would not have been
given freely. That literature is not fringe: it is the operating manual of the largest
information systems ever built, and a curriculum that teaches those systems without a position on
this is teaching techniques and concealing their cost. **TopTech exists to teach the
machine-mediated internet. It cannot do that honestly from inside the attention economy's
assumptions**, and MX-023 is where the estate states the assumptions it rejects.

---

## 2. Definition — what "sovereignty over attention" means here

**The claim.** A person's attention is theirs. An institution may **ask** for it by making
something worth attending to, and may not **take** it by exploiting the gap between what a person
would choose deliberately and what they can be induced to do reflexively.

That gap is the operative concept and it needs a test rather than a sentiment. The estate uses
this one:

> **The reflective-endorsement test.** Would the reader, told plainly what the design was doing
> and why, endorse it? If yes, the design asks. If no, it takes.

Four applications, to show the test excluding things:

| Design | Test | Verdict |
|---|---|---|
| A page whose lead sentence states what you will be able to check | Told plainly, a reader endorses it | **Asks** |
| Two exit actions — one deeper, one sideways | Endorsed: it serves both real intentions | **Asks** |
| An autoplaying next lesson with a five-second countdown | *"We start the next one before you decide, because most people don't stop it"* | **Takes** |
| A streak counter | *"We show consecutive days so that breaking it feels like a loss"* | **Takes** |

**What the test is not.** It is not consent, and the difference matters. A reader can consent to a
streak counter; the test asks whether they would endorse the *mechanism's purpose* once stated,
and a mechanism that works by exploiting loss aversion does not survive being described. This is
why [ML-2.3 §H.18](../license/ml-2-3.md) treats consent integrity separately: consent obtained at
a moment when a person cannot practically refuse is not the same as endorsement.

**What sovereignty does not mean.** It does not mean the estate must be dull, or that difficulty
is disrespectful, or that a reader should never be surprised. A hard course that demands sustained
attention is not a violation — it is the thing being asked for. The distinction is between
**demanding attention for the work** and **capturing attention for the platform.**

---

## 3. Mechanism — the six refusals

The estate's position is operative through six specific refusals. Each is checkable, each is
implemented somewhere in the corpus, and each has a cost the estate accepts.

### 3.1 No engagement metric governs any decision

No page, series or feature is evaluated by time-on-site, sessions, return rate, streak length or
completion velocity. The permitted measures concern **whether learning happened and whether claims
held**: assessment outcomes, artefact quality, correction submissions, falsifications accepted.

This is the deepest of the six and the reason is structural rather than moral. An engagement metric
is not a neutral instrument that can be used well; it is an **objective function**, and once a
team is held to one, every subsequent design decision is quietly resolved in its favour. Under
[ML-2.3 §H.4](../license/ml-2-3.md) an optimisation must be disclosed as the objective function
actually in use — and the estate's answer must remain sayable in public.

**The cost:** the estate cannot tell whether it is growing in the way institutions normally
measure. It accepts operating with less information about itself than its competitors have about
themselves.

### 3.2 No streaks, no leaderboards, no variable reward

`me.metax.academy` carries no streak counter, no leaderboard, no ranking, no badge issued for
consecutive activity. Progress is shown as **state, not momentum**: what is complete, what is
open, what has expired.

Variable-ratio reward is the most reliable compulsion mechanism known and it is trivially cheap to
implement. It is refused because it works — it produces returning users who did not decide to
return, which is precisely HX‑03.

**Consistency check the estate applies to itself:** having refused this mechanic for learners, it
may not adopt it for referrers, which is why [ST-23](../standards/st-23-affiliate-and-referral.md)
excludes leaderboards from the affiliate program by schema.

### 3.3 The exit is as easy as the entrance

Two actions at the foot of every page, one deeper and one sideways —
[SITE-02 §4](../site/page-contract.md). **No third action, no newsletter capture, no urgency
copy.** No interstitial on leaving, no confirmation dialogue on unsubscribing, no dark-pattern
asymmetry between signing up and signing off.

Account deletion is a single action with a stated retention period
([MX-018](mx-018-data-retention.md)). A person may take their artefacts and credentials with them.

**The cost:** measurably fewer newsletter subscribers. Accepted, on the reasoning that a
subscriber acquired by making leaving awkward is a subscriber who did not choose.

### 3.4 Nothing moves that the reader did not start

The five-tier motion system reserves **T‑3 (signal)** and leaves it unused. Ambient motion is
decorative, marked `aria-hidden`, and must be suppressible by `prefers-reduced-motion`.

**This refusal is currently violated by the estate itself.** Nine infinite ambient animations run
with no `prefers-reduced-motion` block ([DEF-016](../00-governance-map/defect-register.md#def-016),
[B-16](../00-governance-map/launch-blockers.md)). Animation that continues over an expressed user
preference is compulsion at small scale, and the preference exists precisely so the system need not
guess — the reader has already answered. Stated here rather than in a footnote, because an
instrument that lists its violations only in the defect register is asking to be read selectively.

### 3.5 No claim on attention outside the page

No push notification. No re-engagement email. No "you haven't visited in a while." The estate
communicates on **transactional** grounds — an assessment result, a credential expiry, a
correction to something the reader submitted — and on no other.

The distinction is whether the message serves an intention the reader already had. An assessment
result does; a reminder that a course is waiting does not, and it is an attempt to reach into a
person's day to produce a return they did not plan.

### 3.6 Advertising is disclosed, bounded, and currently the estate's own failure

[MX-009](mx-009-advertising-and-commercial.md) states the position. The estate's practice
contradicts it: Google AdSense (three slots) and Adsterra run **on the content plane**
([DEF-019](../00-governance-map/defect-register.md#def-019)).

This is recorded in [HX-002](../harms/hx-002-harm-instrument-map.md) as an outright **FAILS** on
HX‑01 and HX‑04, not a partial. Behavioural ad networks are the exact mechanism those harms name,
and the estate's five other refusals do not offset it — treating good conduct elsewhere as
compensation for a live harm is the substitution HX‑15 describes.

**The decision is the Curator's** and it is currently cheap: because the site is a demo, the slots
can be removed before the estate's [Part H Statement](../license/part-h-statement.md) is ever
issued, which would let HX‑01 and HX‑04 read *remedied*
([RAT-15](../00-governance-map/open-questions-and-ratifications.md#rat-15)). That window closes on
publication.

---

## 4. Worked instance — designing the placement diagnostic

`/toptech/start/diagnostic/` is the estate's highest-stakes attention surface: a first-time
reader, deciding whether to commit months. Every mechanism this instrument refuses would work
there.

**What an engagement-optimised version would do.** Open with a single question to create
commitment before cost is known. Show a progress bar that accelerates near the end. Withhold the
result behind an email address. Present the recommendation as a scarce opportunity with a
time-limited enrolment window. Every one of those is standard practice and each measurably
increases completion.

**What this instrument requires instead.** The diagnostic states its length and purpose before the
first question — *"eleven questions, about nine minutes, and you can stop at any point without
losing your answers."* The progress indicator is linear and honest. The result is shown
immediately, **without an email address**, and includes the outcome a marketer would suppress:
*"on these answers, TopTech is not the right starting point for you, and here is what is."* There
is no enrolment deadline because there is no scarcity — it is a static site.

**Applying the §2 test:** told plainly *"we state the length up front so you can decline, and we
show your result even when it advises against us,"* a reader endorses it. Told *"we withhold your
result until you give us an email because most people comply at that point,"* they do not.

**The honest cost.** Fewer completed diagnostics, fewer captured addresses, and some readers
correctly advised elsewhere. The estate accepts all three, and the third is not a cost at all
except on a metric this instrument refuses.

---

## 5. Failure modes

**Sovereignty invoked to justify neglect.** "We don't do engagement" becoming cover for a
confusing interface or an unanswered question. Refusing to capture attention is not the same as
refusing to serve it, and this is the failure most likely to be committed by someone who has read
this instrument approvingly.

**The metric that arrives as a diagnostic.** *"We're only measuring completion to find where
learners get stuck"* — a true and reasonable sentence. The mechanism of §3.1 is that measurement
becomes optimisation without anyone deciding it should, so the estate's rule is that a measure
introduced for diagnosis must have a stated expiry and a named owner, or it will still be there in
three years shaping decisions.

**Difficulty as a proxy for rigour.** An unnecessarily hard interface, unexplained notation, or
prose written to signal seriousness. This wastes attention rather than capturing it, which is a
different failure with the same victim.

**The estate's actual pattern, named plainly.** Four of the six refusals are implemented and two
are violated by the live build — the animations (§3.4) and the ads (§3.6). This is the recurring
shape of the whole corpus, recorded in
[HX-002 §8](../harms/hx-002-harm-instrument-map.md): **good rules, missing mechanisms.** A
doctrine whose violations are all in the same two places should suspect that the doctrine is
easier to write than the build is to fix.

---

## 6. Limits

**Class: ethical.** The reflective-endorsement test of §2 is the estate's own construction, not a
settled standard. It has a known weakness: a reader can endorse something bad for them, and the
test then licenses it. It is used because the alternatives are worse — a paternalistic standard
lets the estate decide what a reader should want, and a pure consent standard licenses anything
disclosed.

**Class: epistemic.** This instrument asserts that engagement optimisation harms readers. The
empirical literature is real but contested, and the estate's position rests substantially on a
normative claim about autonomy rather than on measured outcomes. Marked as the estate's own
position under [ST-24 §8](../standards/st-24-page-prose-standard.md) rather than presented as
established.

**Class: economic.** Every refusal has a revenue or growth cost, and §§3.1–3.5 accept them
unquantified. Whether an institution can be built this way is untested — the estate has no
learners, no revenue and no credential holders. This instrument is a commitment made before it has
been expensive.

**Class: religious.** The *Ḥifẓ al-ʿAql* extension — from intoxicants to attention-engineering —
is published as **contested** and awaits scholarly review
([RAT-16](../00-governance-map/open-questions-and-ratifications.md#rat-16)). The duties in §3 rest
on the secular evidence and the autonomy argument independently, and do not require the extension
to hold.

---

## 7. Falsifier

This instrument is wrong if:

1. **An estate applying all six refusals produces measurably worse learning outcomes** than one
   using engagement mechanics — which would show the refusals to cost the reader rather than serve
   them. Testable, and untested.
2. **The reflective-endorsement test licenses a mechanism the estate would refuse on other
   grounds**, showing §2's test to be under-inclusive.
3. **Readers, told plainly what a refused mechanism does, endorse it anyway at scale.** Streaks
   are the candidate: many people report wanting them. If that endorsement is robust under full
   disclosure, §3.2 is wrong as written and should be narrowed to variable-ratio reward alone.

Falsifier 3 is the live one, and the estate should say what would follow: under
[ML-2.3 §E.5](../license/ml-2-3.md) a demonstrated falsification obliges the steward to narrow or
withdraw the corresponding duty. §3.2 would narrow, and the narrowing would be recorded in
[the version history](../license/version-history.md) — where the count of withdrawals is currently
**zero**, which is the number that will show whether this corpus is a register or a doctrine.

---

## 8. Obligation

**For the estate:** ship the `prefers-reduced-motion` block (§3.4) and decide the advertising
question (§3.6). Those are the two live violations, and both are named in the
[Part H Statement](../license/part-h-statement.md) as *unremedied* if they survive.

**For a designer working in this estate:** apply §2's test to any mechanism that would produce a
return, a completion or a click the reader had not planned. Where the test is close, the
mechanism does not ship — a doctrine of attention that resolves its own hard cases in favour of
the institution is not operating.

**For an academy chartered under [MX-004](mx-004-terms-of-top-levels.md):** §§3.1–3.5 are
inherited. An academy may not add streaks, push notifications or engagement metrics to a MetaX
subdomain, and Requirement 11 obliges its own Part H Statement to record Stratum I dispositions.

**Under ML-2.3:** HX‑01, HX‑02, HX‑03 (Stratum I), §H.4 (optimisation disclosure), §H.18 (consent
integrity), §H.24 (developmental default), §H.3(a)(vii) (developmental substitution — disjunctive,
and the reason §§3.1–3.2 bind absolutely where the users are people whose faculties are still
forming).

---

**Related:** [MX-009 Advertising and Commercial](mx-009-advertising-and-commercial.md) ·
[MX-007 AI Use and Disclosure](mx-007-ai-use-and-disclosure.md) ·
[MX-024 Infrastructure and Migration](mx-024-infrastructure-and-migration.md) ·
[DS-02 Motion and Attention](../design/ds-02-motion-and-attention.md) ·
[HX-002 Harm → Instrument Map](../harms/hx-002-harm-instrument-map.md) ·
[SITE-02 Page Contract](../site/page-contract.md) · [ML-2.3](../license/ml-2-3.md)

*Curated by Maher. Six refusals, four implemented, two violated by the estate's own build — and
the count of duties this corpus has narrowed under §E.5 stands at zero.*
