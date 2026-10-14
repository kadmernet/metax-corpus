---
doc_id: "MX-015"
title_en: "Succession and Institutional Continuity"
title_ar: "الخلافة والاستمرارية المؤسسية"
family: "corpus"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 4
depth: 5
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["corpus", "succession", "continuity", "custody"]
route: "/about/policy/governance/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# MX-015 · Succession and Institutional Continuity

**What this instrument governs.** What happens to this estate when the Curator stops — by choice,
by incapacity, or by death.

**Why it is written now, before anything is at stake.** A succession instrument drafted during a
succession is drafted by whoever is holding the credentials. The only time it can be written
honestly is while its author has nothing to gain from its terms, and that time is now: the estate
has no revenue, no learners, no credential holders and one participant.

---

## 1. Position

Every claim of permanence this estate makes is a claim about **after Maher**. Addresses citable in
2031 ([SITE-03](../site/routing-law.md)). Superseded text retained permanently
([MX-013](mx-013-records-and-versioning.md)). A licence whose registry outlives its steward
([§E.7](../license/ml-2-3.md)). Instruments written for a successor who inherits the corpus rather
than a product.

None of that survives a bus. MX-015 is the instrument that decides whether those are commitments or
decorations, and it is the only one whose subject is the estate's own **mortality**.

Published at `/about/policy/governance/`. Its siblings are
[MX-024](mx-024-infrastructure-and-migration.md) on the infrastructure the successor inherits and
[Steward Succession](../license/steward-succession.md), which is §E.8 in operational form.

**The macro register.** Under **HX‑23** (custody without horizon) and **HX‑20** (inheritance of
unauditable systems), the ordinary fate of a one-person body of knowledge is not destruction but
**orphaning**: the domain lapses, the repository stays private, the payment method expires, and a
corpus that was publicly readable becomes unreachable without anyone deciding it should. That is
the estate's most likely failure mode — more likely than being wrong, refuted, or abandoned — and
it is the failure this instrument exists to make expensive.

---

## 2. Definition — the four roles and what each may do

| Role | Held by | May |
|---|---|---|
| **Curator** | Maher | Everything not reserved by [§0.5](mx-000-charter.md#05-powers-placed-beyond-the-curator) |
| **Steward** | The Curator, or a named successor | Issue determinations; maintain the registry |
| **Custodian** | A named person or institution | Hold the keys, the domain and the mirrors. **May not alter content** |
| **Ethics reviewer** | A named third party | Veto under [§0.5](mx-000-charter.md#05-powers-placed-beyond-the-curator) |

**The Custodian/Steward separation is the instrument's central device.** A Custodian can keep the
estate *reachable* without being able to change what it says; a Steward can interpret it without
holding the infrastructure. Concentrating both is how a successor becomes a new author — and the
estate's whole claim is that the corpus is inheritable rather than authorial.

**Three of these four roles are currently unfilled.** `[VERIFY]`
([V-04](../00-governance-map/verification-log.md),
[RAT-04](../00-governance-map/open-questions-and-ratifications.md#rat-04--name-the-ethics-reviewer-and-the-successors)).
The estate has a Curator and nobody else, which means §3's triggers currently fire into an empty
room.

---

## 3. Mechanism — the three triggers

**Trigger 1 — Planned handover.** The Curator names a successor Steward in writing, signed against
the published key fingerprint, with a dated effective point. Published as a determination.

**Trigger 2 — Incapacity.** No signed activity for **180 consecutive days** and no response to the
Custodian's dated notice. The Custodian then publishes the notice and the non-response, and the
Steward role passes to the named successor.

**Trigger 3 — Death.** Immediate passage to the named successor, on the Custodian's publication of
the fact.

### 3.1 What a successor inherits, and in what order

Order matters, and it is the same order as
[MX-024's migration doctrine](mx-024-infrastructure-and-migration.md): **the record moves before
the features.**

1. **`mx_governance` and the six registers.** Determinations, defects, corrections, archive,
   verification, changelog.
2. **The static content plane** — copyable by `rsync` under
   [MX-024 Property 1](mx-024-infrastructure-and-migration.md).
3. **The licence, its registry and the three §E.7 mirrors.**
4. **Credentials**, then identity, then commerce.

**A successor inheriting mid-transfer and forced to choose takes the record.** The courseware can be
rewritten; the corrections log cannot.

### 3.2 What a successor may never do

Five things, and they are the reason this instrument is not merely a handover plan:

**Delete a published defect, decline a valid correction, or remove a superseded claim.**
[§0.5.2](mx-000-charter.md#2-the-correction-obligation) binds the successor exactly as it binds
Maher.

**Amend §0.4's three refusals or §0.5's reserved powers toward weakness.** Unamendable in that
direction by anyone, ever.

**Issue a determination that entrenches their own advantage.** [§G.5](../license/ml-2-1.md#g5-humility-clause),
which runs against the Steward and is outside precedence entirely.

**Renumber an identifier.** [ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md).
A successor tidying the numbering breaks every citation the estate ever earned.

**Represent the corpus as their own authorship.** [§H.19](../license/ml-2-3.md). The corrections
log records who found what; a successor inherits the record including its attributions.

---

## 4. Worked instance — the estate dies tonight

The honest walk-through, because a succession instrument that cannot be tested against the present
is aspirational.

**What survives.** The Git repository, if someone has a clone. The published Markdown, if anyone
mirrored it. Nothing else with certainty.

**What fails immediately.** The domain lapses at its next renewal, and **every permanent address in
[SITE-03](../site/routing-law.md) breaks** — the whole citation-durability claim depends on one
registrar relationship with **no mitigation at all**
([MX-024 §3.4](mx-024-infrastructure-and-migration.md)). The §E.7 mirrors do not exist
([B-02](../00-governance-map/launch-blockers.md)), so the licence's canonical text has one
custodian. The three unfilled roles mean triggers 2 and 3 pass the Steward role **to nobody**.

**What that means for the corpus.** It becomes a repository someone might find — not an estate.
Readable by whoever has a copy, unreachable at its published addresses, unmaintained, and with no
party empowered to correct it. **Orphaned, exactly as §1 predicts**, without anyone having decided
it should be.

**The instructive part.** This instrument is well-specified and **currently inoperative.** Its four
roles are one role. Its three triggers fire into an empty room. Its inheritance order presumes
mirrors that do not exist. The gap between a written succession plan and an operating one is three
names and a registrar arrangement — none of which is difficult, and all of which have gone
unaddressed through four releases while the corpus grew to thirty instruments.

**That is the estate's characteristic failure arriving in the one place it is fatal.** Elsewhere
*rules without mechanisms* produces a defect. Here it produces an orphan.

---

## 5. Failure modes

**The unnamed successor.** The live condition. A succession instrument with no successor is a
document about a plan.

**The Custodian who is also the Steward.** Convenient, and it dissolves §2's central separation —
the successor becomes a new author with the keys.

**The 180-day trigger firing wrongly.** A Curator on sabbatical, uncontactable, and the estate
transfers. The Custodian's **dated notice and published non-response** are the protection, and the
window is deliberately long.

**Succession by credential capture.** Whoever holds the domain and the signing key becomes the
estate in practice, regardless of what this instrument says. The only defence is that the
§E.7 mirrors are **outside the steward's operational control** — and they do not exist.

**The successor who improves the record.** Tidying identifiers, pruning closed defects, rewriting
superseded sections into agreement. Each individually reasonable; the aggregate is an estate that
appears always to have been correct. §3.2's five prohibitions exist against exactly this.

---

## 6. Limits

**Class: practical, and it is decisive.** Three of four roles are unfilled, the mirrors do not
exist, and the domain dependency is unmitigated. **This instrument specifies a succession the
estate cannot currently perform.**

**Class: legal.** Whether any of this binds a successor is unreviewed in every jurisdiction —
`counsel_reviewed: false`,
[RAT-07](../00-governance-map/open-questions-and-ratifications.md#rat-07--jurisdiction-governing-law-and-the-liability-cap)
and [RAT-18](../00-governance-map/open-questions-and-ratifications.md#rat-18). A succession plan
that is a moral instrument rather than an enforceable one should be read as such.

**Class: custodial.** §E.7's redundancy requirement is the instrument's precondition and
[B-02](../00-governance-map/launch-blockers.md) is open. Until mirrors exist, continuity depends on
one repository held by the party whose absence triggers the plan.

**Class: economic.** A Custodian holding a domain and three mirrors incurs recurring cost. The
estate has no revenue and no endowment, and this instrument does not solve who pays after the
Curator stops — which is the question most likely to decide the estate's actual fate.

---

## 7. Falsifier

1. **A trigger fires and the estate does not transfer** — falsifying §3 as operative. **Currently
   guaranteed to fire this way**, since no successor is named.
2. **A successor performing one of §3.2's five prohibitions** without any mechanism resisting it,
   showing the prohibitions moral rather than structural.
3. **The Custodian/Steward separation proving unworkable** at this scale, forcing concentration —
   which would falsify §2's central device rather than the instrument.
4. **The corpus surviving the Curator's absence without this instrument** — if a clone, a mirror
   and a motivated reader are sufficient, then MX-015 is ceremony and the real continuity mechanism
   is **publication itself.** The estate considers this partly true and is not certain how much.

---

## 8. Obligation

**For the Curator, and these are the estate's most overdue items.** Name the successor Steward, the
Custodian and the ethics reviewer
([RAT-04](../00-governance-map/open-questions-and-ratifications.md#rat-04--name-the-ethics-reviewer-and-the-successors)).
Build the three §E.7 mirrors, one content-addressed and one outside operational control
([B-02](../00-governance-map/launch-blockers.md)). Arrange the domain so it does not lapse on a
single unpaid invoice. **Sign the licence** —
[B-01](../00-governance-map/launch-blockers.md) — because an unsigned instrument cannot name a
successor against a key fingerprint.

None of the four is difficult. All four have been open since the first release, and §4 states what
they cost if they stay open.

**For a successor:** take the record first (§3.1). Read §3.2 before changing anything. You inherit
a corpus including its errors, its attributions and its unflattering findings — **and the record of
who found them is part of what you inherit**, not a draft you may improve.

**Under ML-2.3:** §E.7 (registry continuity), §E.8 (anti-capture and steward succession), §G.5
(the humility clause, binding a successor), §H.19 (authorship of record), §H.20 (chain of
responsibility), §H.23 (custody without horizon), §H.25 (silence in the record), §H.28 (custody
and horizon).

---

**Related:** [MX-000 §0.5](mx-000-charter.md#05-powers-placed-beyond-the-curator) ·
[MX-024 Infrastructure and Migration](mx-024-infrastructure-and-migration.md) ·
[MX-013 Records and Versioning](mx-013-records-and-versioning.md) ·
[Steward Succession](../license/steward-succession.md) ·
[Registry and Mirrors](../license/registry-and-mirrors.md) ·
[Launch Blockers B-01, B-02](../00-governance-map/launch-blockers.md) ·
[SITE-03 Routing Law](../site/routing-law.md)

*Curated by Maher. Four roles of which three are unfilled, three triggers that currently fire into
an empty room, and one domain name on which every permanent address in this estate depends — which
is what the estate's most-repeated permanence claim actually rests on tonight.*
