---
doc_id: "MX-012"
title_en: "Licensing and Reuse"
title_ar: "الترخيص وإعادة الاستخدام"
family: "corpus"
version: "v2026.10.1"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 2
depth: 5
evidence_class: "semi-durable"
review_interval_months: 6
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-01"
domain_tags: ["corpus", "licensing", "reuse", "attribution"]
route: "/about/legal/ip/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# MX-012 · Licensing and Reuse

**What this instrument governs.** What a reader may do with the material in this estate: which
licence applies to what, what attribution is required, and which reuses need nothing from anyone.

**What it is not.** It is not the licence. [ML-2.3](../license/ml-2-3.md) is, and this instrument
is a **summary that creates no obligation absent from it**. Under
[GM-01 §3](../00-governance-map/precedence-and-conflict-rules.md) **summaries never govern**; where
this page and ML-2.3 differ, the licence governs and the difference is a defect filed under §E.9.

---

## 1. Position

A governance corpus that publishes a demanding licence and leaves a reader unable to work out what
they may do has produced a restriction, not a licence. Most readers will never open ML-2.3 — Parts
0 and A through H, five schedules, twenty-five harms — and their practical understanding of their
own permissions will come from a page like this one.

That makes this instrument's **accuracy** more consequential than its authority. It governs nothing
and it is what most people will rely on.

Published at `/about/legal/ip/`. Its companions are
[the plain-language companion](../license/ml-2-1-plain-language.md), expressly non-operative, and
[the enforceability table](../license/enforceability-two-track-table.md), which states what the
estate would actually enforce.

**The macro register.** Under **HX‑08** (intermediation rent) and **HX‑12** (harm to the record),
the modern licensing failure is not restriction but **uncertainty**: terms so complex that a
prospective user's cheapest response is to walk away. The material goes unused, the estate learns
nothing, and the refusal arrives as silence. A licence that produces silence has failed whatever
its terms say — which is why
[the enforceability table §1](../license/enforceability-two-track-table.md) exists and why this
instrument leads with permissions rather than conditions.

---

## 2. Definition — what is licensed how

| Material | Licence | Designated? |
|---|---|---|
| The MX, AG, ST, RB, DS, SITE and GM instruments | **ML-2.3** | Per [the Designation List](../license/designation-list.md) |
| [ML-2.3](../license/ml-2-3.md) and its schedules | ML-2.3; **all versions designated** | Yes |
| [HX-000](../harms/) and the harms apparatus | ML-2.3; HX-000 and HX-001 designated | Yes |
| Course, lesson and capstone material | ML-2.3, **not designated** | No |
| Site templates, components, CSS, build scripts | ML-2.3, not designated | No |
| Machine artefacts — `catalog.json`, `credentials.json`, `lexicon.json`, `status.json` | ML-2.3, not designated | No — they are *renderings* |
| The registers: changelog, corrections, defects, archive, verification | ML-2.3; protected by [MX-013](mx-013-records-and-versioning.md) rather than Part G | No |
| Third-party quotations inside the corpus | **Their own terms.** Nothing here relicenses them | — |

**Designation is not a compliment.** It means [Part G](../license/ml-2-1.md#part-g--the-charter-layer)
applies — the charter layer, with its supremacy and its Charter Conformity Determinations. A
designated Work is **more demanding to adopt**, not better. `designated: false` on lesson material
is deliberate: a course should be reusable without accepting a charter layer.

---

## 3. Mechanism — what you may do

### 3.1 Without asking, and without conditions beyond attribution

**Read, quote, cite, link, archive, mirror, translate for private use, index, and use in a machine
reading** under [GM-11](../00-governance-map/machine-reading-contract.md).

**Quote at length.** No word limit. The estate would rather be quoted accurately at length than
paraphrased briefly.

**Mirror the whole corpus.** Actively encouraged — [§E.7](../license/ml-2-3.md) requires three
independent mirrors of the licence and **the estate has none**
([B-02](../00-governance-map/launch-blockers.md)). A reader who mirrors this corpus is repairing a
launch blocker on the estate's behalf.

**Criticise, refute, fork the argument.** `/license/falsification/objections/` is open and
[ST-06](../standards/st-06-objections-standard.md) states how an objection is recorded. The estate
has no interest in a licence that discourages disagreement.

### 3.2 Attribution — what is actually required

```
[Title], [doc_id] [version], MetaX.Academy, curated by Maher.
Licensed under the Maher License 2.3.
SPDX-License-Identifier: LicenseRef-ML-2.3
```

**Three requirements and one prohibition.** Name the instrument and its `doc_id`. Give the
**version** — the corpus versions instruments and a citation without one is unresolvable in five
years. Identify the licence.

**And do not misattribute.** [§H.19](../license/ml-2-3.md) cuts both ways: you may not present the
estate's text as your own, **and you may not present your own as the estate's.** The second matters
more here — a modified instrument circulated under an unmodified identifier corrupts the citation
graph the whole corpus depends on.

### 3.3 Modification and derivation

**Permitted**, under two conditions.

**Change the identifier.** A modified `MX-013` is not `MX-013`.
[ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md) makes identifiers immortal
*within* this estate, and a derivative asserting the same `doc_id` breaks that outside it. Use your
own prefix.

**State what you changed.** Not a diff — a statement. *"Derived from MX-013 v2026.10.1; §3 Rule 4
replaced; the archive requirement removed."* A reader must be able to tell which text they hold.

**For designated Works, Part G additionally applies** — the charter conditions of §G.2 and the
derived-licence floor of §E.6. This is the case where reading ML-2.3 itself is unavoidable, and
this summary says so rather than paraphrasing a charter layer.

---

## 4. Worked instance — three reuses, one estate

A reader wants to use [ST-05](../standards/st-05-decay-and-review-intervals.md), the decay standard.

**Reuse A — quoting the three classes in a blog post.** Nothing needed beyond §3.2's attribution.
No permission, no notice to the estate, no length limit. ST-05 is not designated, so Part G does
not arise.

**Reuse B — adopting the three classes in their own documentation.** Permitted under §3.3. They
change the identifier — their own prefix, not `ST-05` — and state the derivation. Nothing else is
required and the estate is not notified.

**Reuse C — adopting [HX-001](../harms/hx-001-harm-audit-rubric.md), the harm audit rubric,
commercially at scale.** Different, and the difference is the point. HX-001 **is designated**
([DL-2 row 15](../license/designation-list.md)), so Part G applies: §G.2's charter conditions bind,
the Work may be the subject of a Charter Conformity Determination, and §6-bis's stronger
attribution regime applies. **Reading ML-2.3 is now unavoidable** and this summary is insufficient.

**Additionally, at Tier 1 or above**, [§H.16](../license/ml-2-3.md) obliges them to publish their
own Part H Statement, using [the Schedule 1 form](../license/part-h-statement.md), which is itself
designated. **That is the estate's most demanding licensing consequence** and the one a reader is
least likely to discover from a summary — stated here plainly for exactly that reason.

---

## 5. Failure modes

**This summary drifting from the licence.** The failure this instrument is most exposed to.
[GM-01 §3](../00-governance-map/precedence-and-conflict-rules.md) lists MX-012 as a single-source
pair checked against ML-2.3 and the Designation List — and **that check does not run**
([DEF-001](../00-governance-map/defect-register.md#def-001)), so the drift protection is presently
a specification.

**Designation assumed from importance.** A reader concluding that a Work matters, therefore Part G
applies. Only [the Designation List](../license/designation-list.md) decides, and it is **still
unratified** ([RAT-06](../00-governance-map/open-questions-and-ratifications.md#rat-06--ratify-the-designation-list)),
so every designation is asserted rather than settled.

**Derivative under the same identifier.** §3.3. The commonest real reuse error, and it damages the
citation graph rather than the estate.

**Attribution without version.** Unresolvable once the instrument moves.

**Relicensing third-party quotations.** Nothing here relicenses material quoted from elsewhere. A
reader reusing a quotation needs its source's terms.

---

## 6. Limits

**Class: authority.** This instrument **governs nothing.** If it is wrong, ML-2.3 still binds and a
reader who relied on this page was misled by a summary — which is why §5 puts drift first.

**Class: legal.** `counsel_reviewed: false`. ML-2.3 has never been reviewed by a lawyer in any
jurisdiction (ML‑D‑010,
[RAT-18](../00-governance-map/open-questions-and-ratifications.md#rat-18)), and its two central
devices — the condition/covenant split and the Scale Gate — are untested. **A reader adopting this
licence for anything consequential should obtain their own advice**, and the estate says so rather
than implying the instrument is settled.

**Class: unresolved.** ML-2.3 declares `supersedes: "ML-2.2"` and **no ML-2.2 exists**
(ML‑D‑007, [RAT-14](../00-governance-map/open-questions-and-ratifications.md#rat-14--does-ml-22-exist)).
**No party may rely on §E.3's transition provision.** If you hold a grant under an earlier version,
the estate's published position is that **no party is disadvantaged by relying on ML-2.1's terms**
until this resolves.

**Class: practical.** Nobody has adopted ML-2.3. No determination has issued, no compatibility
question has been decided, and the interpretive record is empty — so every clause's meaning rests
on its text alone.

---

## 7. Falsifier

1. **A reuse this instrument permits that ML-2.3 forbids**, or the reverse. A drift defect, and the
   likeliest failure given §5.
2. **A prospective adopter unable to determine their permissions from §§2–3** and abandoning the
   material. That is §1's silent refusal; it falsifies this instrument's purpose rather than its
   accuracy, and **the estate cannot currently detect it.**
3. **The designation boundary proving unusable** — if readers routinely cannot tell whether Part G
   applies, the two-tier structure is too subtle to operate.
4. **Nobody adopting the licence at all.** After a year of publication that would falsify not this
   summary but the estate's premise that a demanding ethical licence can be adopted. The estate
   would rather learn that from adoption data than from silence.

---

## 8. Obligation

**For a reader:** attribute with the version. Change the identifier if you modify. Read ML-2.3
itself if the Work is designated or if you operate at Tier 1 or above — this summary is not
sufficient for either, and §4's reuse C shows why.

**For the estate:** run the single-source check against ML-2.3 and the Designation List
([ST-13 §2.4](../standards/st-13-static-build-and-sentinel.md)); **ratify the Designation List**
(RAT-06) so designations stop being asserted; resolve the ML-2.2 gap (RAT-14); obtain counsel review
before representing ML-2.3 as binding on any third party.

**For anyone mirroring this corpus:** you are welcome, and you are doing something the estate needs
— §E.7 requires three independent mirrors and there are none.

**Under ML-2.3:** §C.10 (machine learning and synthetic derivation, which this summary does not
displace), §E.3 (transition — currently unusable), §E.6 (derived-licence floor), §E.9 (conflicts
between licence and register are defects), §H.19 (authorship of record), §6-bis (attribution
integrity for foundational Works), Part G (the charter layer).

---

**Related:** [ML-2.3](../license/ml-2-3.md) ·
[Designation List](../license/designation-list.md) ·
[Two-Track Enforceability Table](../license/enforceability-two-track-table.md) ·
[Plain-Language Companion](../license/ml-2-1-plain-language.md) ·
[License Version History](../license/version-history.md) ·
[Part H Statement](../license/part-h-statement.md) ·
[Machine Reading Contract](../00-governance-map/machine-reading-contract.md) ·
[MX-017 Trademark and Brand Use](mx-017-trademark-and-brand.md)

*Curated by Maher. A summary that governs nothing and is what most readers will rely on — which is
why its first named failure mode is drifting from the instrument it summarises, and why that check
does not yet run.*
