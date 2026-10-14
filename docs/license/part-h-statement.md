---
doc_id: "ML-S1"
title_en: "The Part H Statement — Schedule 1 Form and the Estate's Own Statement"
title_ar: "بيان الجزء ح — نموذج الملحق الأول وبيان المؤسسة نفسها"
family: "license"
version: "v2026.10.1"
status: "canonical"
authority: "operative-form"
prevailing_text: "en"
audience_tier: 5
depth: 5
evidence_class: "semi-durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["license", "compliance", "harms", "disclosure"]
route: "/license/statement/form/"
derived_from: "ML-2.3 §H.16 and Schedule 1"
provenance_of_purpose: "specification"
statement_status: "NOT YET ISSUED — see §5"
hreflang: "en, ar"
---

# The Part H Statement

**What this instrument is.** Two things in one file, deliberately. §§1–4 are the **Schedule 1
form** any licensee at Tier 1 or above must complete under
[ML-2.3 §H.16](ml-2-3.md#h16-part-h-statement). §5 is **MetaX's own Statement**, which is not yet
issued and states plainly why.

**Why the form and the estate's own answer sit in the same document.** Because a compliance form
published without its author's completed copy is an instrument that asks of others what it has not
asked of itself. ML-2.3 §E.8(a)–(b) forbid the steward from charging for compliance or granting
unpublished exemptions, and a steward who simply *omits* its own Statement has granted itself the
exemption §E.8(b) says does not exist. Keeping both here makes the omission impossible to
overlook.

---

## 1. Who must issue a Statement, and when

| Tier | Threshold (§H.2-bis) | Statement required |
|---|---|---|
| **Tier 0** | Personal, non-public, no third-party users | No |
| **Tier 1** | Small — public but below the published user and revenue thresholds | **Yes**, short form (§2) |
| **Tier 2** | Substantial | **Yes**, full form (§3) |
| **Tier 3** | Systemic | **Yes**, full form plus the §H.21 proportionality analysis |

**Timing.** Within ninety days of first exceeding a tier threshold, and annually thereafter.
Republished within thirty days of any material change in disposition.

**Publication.** At a stable public URL, in the licensee's prevailing language, with a
machine-readable mirror. A Statement that cannot be retrieved by a person who was not given the
link has not been published.

**The four roles (§H.1-bis)** must each be named or expressly declared absent: **Author** (who
made the artefact), **Integrator** (who assembled it into a system), **Operator** (who runs it),
**Commissioner** (who asked for it and benefits). A single natural or legal person may hold more
than one role; no role may be left blank.

---

## 2. The short form (Tier 1)

```
PART H STATEMENT — ML-2.3 §H.16
Issued by:            [legal name]
Accountable person:   [natural person, §H.16.4 — not a department]
Artefact / system:    [name, version, public URL]
Tier claimed:         1 (Small)
Tier basis:           [the measured figures, with their date]
Roles:    Author:        [name or "absent, and why"]
          Integrator:    [ ]
          Operator:      [ ]
          Commissioner:  [ ]
Period covered:       [dates]
Next review:          [date]

DISPOSITIONS — one line per harm, HX-01 … HX-25
  HX-nn  [remedied | partially remedied | unremedied | not engaged]
         Reason: [one sentence]
         Review: [date, required unless "not engaged"]

DECLARATION
  I have read HX-000 in full. The dispositions above are my own assessment and not
  a supplier's assurance. I understand that a Statement recording no unremedied or
  partially remedied harm is presumptively non-compliant under §H.16.3.
  Signed: [natural person] Date: [ ]
```

**`not engaged` is the only disposition that needs no review date**, and it is the one most likely
to be abused. It means the harm's mechanism is structurally absent — not that it is small, not
that it is managed. A static document with no telemetry may honestly mark HX‑01 *not engaged*. A
product with an engagement metric may not, whatever its intentions.

---

## 3. The full form (Tiers 2 and 3)

Everything in §2, plus the following for **every** harm not marked `not engaged`.

| Field | What it requires |
|---|---|
| **Mechanism as instantiated** | How this harm arises *in this system specifically*, not the register's general statement |
| **Measurement** | What is measured, how often, by whom. "Not measured" is an acceptable and informative answer |
| **The counterproductivity test (§H.7)** | Whether the remedy has made the harm worse, and how you would know |
| **Optimisation disclosure (§H.4)** | What the system optimises for, stated as the objective function actually in use |
| **Substitution disclosure (§H.29)** | What human activity this replaces, and for whom |
| **Reversibility (§H.27)** | Whether the deployment can be withdrawn, at what notice, and what would be lost |
| **Chain of responsibility (§H.20)** | Which of the four roles can actually change this, and whether they agreed to |

**Tier 3 additionally requires the §H.21 proportionality analysis**: for each imposed burden, who
bears it, whether they chose it, and what alternative was available to them. §H.21 exists because
a systemic deployment distributes its costs to people who never agreed to the trade, and a
Statement that omits them is a Statement written for the deployer's own comfort.

---

## 4. The §H.16.3 presumption, and how not to fail it

> An all-clear Statement is presumptively non-compliant and is itself evidence of **HX‑15**
> (compliance theatre).

This is the clause that makes the whole instrument work, and it inverts the ordinary incentive of
a compliance form. Every other disclosure regime rewards a clean return. This one treats a clean
return as a red flag, on the reasoning that twenty-five structural harms cannot all be absent from
any real deployment, and a party reporting otherwise has either not looked or has decided what the
answer should be before looking.

**Three consequences a licensee should understand before drafting.**

**An honest Statement is unflattering by construction.** If yours is not, revise your reading of
the register rather than your Statement. The most common error is treating "we did not intend
this" as a remedy; the register is about *structure*, and structural harm is indifferent to
intent.

**"Partially remedied" is the most useful disposition and the least used.** It states that a
mechanism is present, that something has been done, and that the something is insufficient. That
is the true state of most remediation most of the time, and a form that pushes drafters toward the
two extremes produces less information than one that makes the middle respectable.

**A review date is a commitment, not a formality.** A Statement whose review dates have all passed
is worse evidence of good faith than no Statement, because it demonstrates that the process was
performed once and abandoned.

---

## 5. MetaX's own Statement

**Status: NOT YET ISSUED.**

The estate does not hold a completed Statement, and this section records why rather than leaving
the omission to be inferred from an absence.

### 5.1 What blocks it

Two things, and only one of them is a decision.

**First, HX-000 does not yet exist at v2026.10.1.** ML-2.3 §A.10 incorporates a twenty-five-harm
register; the estate holds eleven harms in full form and fourteen unwritten
([DEF-021](../00-governance-map/defect-register.md#def-021), ML‑D‑008). A Statement recording
dispositions against harms whose text has not been published would be an assessment against a
document nobody can read. That is a sequencing constraint, not a judgement, and it resolves when
the register is completed.

**Second, and this is the decision: the ad slots.** Google AdSense (`ca-pub-4463113802541266`,
three slots) and an Adsterra slot run on the content plane
([DEF-019](../00-governance-map/defect-register.md#def-019)). On the present evidence the estate's
dispositions would have to read:

| Harm | Disposition the evidence supports | Why |
|---|---|---|
| **HX‑01** attention expropriation | **unremedied** | Behavioural ad networks on the content plane are the mechanism the harm names |
| **HX‑04** the human as product | **unremedied** | Ad delivery makes the reader the transacted party |
| **HX‑10** material and infrastructural cost | **partially remedied** | Static estate, no images, small payloads — but third-party ad scripts are not accounted for |
| **HX‑18** consent integrity | **partially remedied** | Cookie disclosure exists; consent at the point of influence does not |
| **HX‑02** epistemic dependency | **partially remedied** | Falsifiers and evidence classes are published; the build that enforces them does not run ([DEF-001](../00-governance-map/defect-register.md#def-001)) |
| **HX‑12** harm to the record | **partially remedied** | Permanent addresses, append-only redirects, retained supersessions — against zero Arabic pages and an unbuilt archive |

### 5.2 The decision the demo status has changed

Until this release the question was *how does the estate confess HX‑01 and HX‑04*. It is now a
different question, and better.

Because the live site is a **demo** ([C-14](../00-governance-map/corrections-log.md#c-14),
[R-50](../00-governance-map/reconciliation-ledger.md#r-50--the-live-site-is-a-demo)), there is a
window in which the ad slots can be removed **before this Statement is ever issued** — which would
let HX‑01 and HX‑04 honestly read *remedied* rather than *unremedied*. MX‑NAV‑SPEC §10 puts it
directly: *"you have a clean window to remove the ad slots before the statement is ever
published,"* and warns that if they stay, *"the honest text stays too, and it will sit two clicks
from the licence you are asking people to adopt."*

That window closes on publication, and it does not reopen. This is
[RAT-15](../00-governance-map/open-questions-and-ratifications.md#rat-15) and
[B-19](../00-governance-map/launch-blockers.md), and no editor may decide it.

### 5.3 The one thing this section will not do

It will not publish an all-clear Statement, and it will not delay indefinitely to avoid publishing
an unflattering one.

Both failures are named in the register the estate wrote. An all-clear return makes MetaX the
first specimen of **HX‑15** — the harm its own licence introduced — and indefinite delay is the
same harm by omission, since a duty deferred until convenient is a duty the deployer controls. The
honest options are two: remove the conduct, or publish the disposition. There is no third.

**What the estate commits to here, in advance of the decision:** this Statement will be issued
within thirty days of HX-000 v2026.10.1's publication, whatever the ad decision is by then, and it
will name a natural person under §H.16.4. If the slots remain, the Statement says *unremedied*
with a reason and a review date.

### 5.4 BHS-2027-001: draft second-cycle Statement *(added 2026-09-30; NOT ISSUED)*

**The §5.1 blocker is cleared.** A twenty-five-harm register now exists, and
[HX-000 v2027.1](../harms/hx-000-register-v2027-1.md) holds 28. **Correction to the §5.1 table:**
four of its harm labels are wrong against ML-2.3 §H.2.2. HX-02 is *cognitive offloading*, not
"epistemic dependency". HX-10 is *extractive materiality*. HX-12 is *digital amnesia*, not "harm to
the record". **HX-18 is *standard capture*, not "consent integrity"**, which is HX-16. The table above
is kept as published (DEF-040). The draft below uses ML-2.3 names.

**A nil return was considered and rejected.** One source proposes a "Nil Return BHS-2026-001"
("mostly not applicable, no holdings"). That is acceptable for the **substrate** register, since the
estate holds no substrate (BX-018 §13). It is **not** acceptable for HX-000, because the estate
operates a deployment that instantiates harms.

| Harm | Draft disposition | Basis | Review date |
|---|---|---|---|
| **HX-01** Attention expropriation | **Unremedied** | AdSense and Adsterra on the content plane (REG-12 P-02/P-03) | on the RAT-15 decision |
| **HX-04** The human as product | **Unremedied** | Behavioural ad profiling by the same processors | same |
| HX-28 Steward dependence | **Unremedied**, structural | One curator. No succession acceptance, no dissent channel | 2027-05 |
| HX-25 Erosion of exit | Unremedied | Third-party identity providers on the identity plane | 2027-02 |
| HX-19 Ethical enclosure | Unremedied | Arabic mirror unreviewed; Anglophone evidence base | 2027-08 |
| HX-13 Exclusion by default | Partially remedied | Known accessibility gaps, published (MX-010) | 2027-02 |
| HX-10 Extractive materiality | Partially remedied | Static estate, but inherited accounting gaps and unmeasured AI-authorship energy | 2027-11 |
| HX-18 Standard capture | Unremedied | No external check that this licence is not a barrier | 2027-07 |
| HX-03 Epistemic collapse | Partially remedied | Provenance and AI disclosure published; bibliography unverified | 2027-04 |
| HX-15 Compliance theatre | **Unremedied** | Disclosures outpace remedies (REG-07 §5.1; DEF-039) | 2027-04 |
| *all others* | *not yet assessed* | No assessment has been performed. Marking them "not applicable" without one would be HX-15 | — |

**Accountable person (§H.16.4):** *[unnamed: Curator to name]*. **Issue:** only the Curator can
issue this. Thirty days from the publication of HX-000 v2027.1 as adopted is the commitment above.

---

## 6. Failure modes of the form itself

**The supplier's assurance laundered as a disposition.** A licensee marks HX‑07 remedied because a
vendor's compliance page says so. §2's declaration exists to block this: the dispositions are the
signer's own assessment, and a vendor assurance is evidence, not a disposition.

**The departmental signature.** §H.16.4 requires a **natural person**. "Compliance Team" is not a
person and cannot be asked a question in five years.

**`not engaged` as a default.** The disposition that requires no review date will attract the
drafter who wants to be finished. §2 states the test: mechanism structurally absent, not merely
small or managed.

**Optimisation disclosure written as a mission statement.** §H.4 asks for the **objective function
actually in use** — the metric a team is held to. "We optimise for learner outcomes" is a mission
statement. "We optimise for weekly active sessions" is a disclosure.

**The Statement nobody can find.** Published at a URL circulated on request only, or behind a
login. §1's retrievability test applies.

---

## 7. Falsifier

This instrument is wrong if a licensee can complete §§2–3 fully and honestly while operating a
system that plainly instantiates several harms — which would show the form to be satisfiable
without being informative. The estate's own §5 is the first test case, and it is a genuine one:
the form's value depends on whether MetaX can complete it without either flattering itself or
performing self-criticism. Both failures are visible in the text, which is why §5 shows its
working rather than only its conclusion.

---

## 8. Obligation

**For the licensee:** read HX-000 in full before drafting. A Statement drafted from the register's
summary table is a Statement drafted from a summary, and [GM-01 §3](../00-governance-map/precedence-and-conflict-rules.md)
holds that summaries never govern.

**For the estate:** issue §5 within thirty days of HX-000 v2026.10.1, name a natural person, and
publish the unremedied harms with reasons and review dates if the conduct producing them survives.

**Cited by:** [ML-2.3 §H.16](ml-2-3.md) · Academy Requirement 11 at
`/academies/requirements/r11-part-h/` — which obliges every founding academy to publish one of
these, and which the estate cannot demand while §5 stands unissued.

---

**Related:** [ML-2.3](ml-2-3.md) · [Scale Gate Worksheet](scale-gate.md) ·
[HX-000 The Register](../harms/) · [HX-001 Harm Audit Rubric](../harms/hx-001-harm-audit-rubric.md) ·
[RB-05 Harm Review Gate](../rubrics/rb-05-harm-review-gate.md) ·
[Open Questions](../00-governance-map/open-questions-and-ratifications.md#rat-15)

*Curated by Maher. A compliance form published together with its author's own unissued copy, so
that the omission is on the record rather than in the gap between documents.*
