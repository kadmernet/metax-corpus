---
doc_id: "ST-07"
title_en: "Evidence, Citation and the VERIFY Tag"
title_ar: "الأدلة والاستشهاد ووسم التحقّق"
family: "standards"
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
domain_tags: ["standards", "evidence", "citation", "verification"]
route: "/method/epistemics/evidence-classes/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# ST-07 · Evidence, Citation and the VERIFY Tag

**What this standard governs.** What must support a claim before it may be published: the five
evidence classes E0–E4, the citation form, and the `[VERIFY]` tag that marks a claim the estate
believes and has not checked.

**Its place in the apparatus.** [ST-04](st-04-falsifiability-and-claim-cards.md) asks what would
refute a claim. [ST-05](st-05-decay-and-review-intervals.md) asks how long it survives. ST-07 asks
**what holds it up now** — and its most-used provision is the one permitting a claim to be
published with the honest answer *"nothing yet."*

---

## 1. Position

Every corpus has a gap between what it asserts and what it has verified. The only question is
whether the gap is **marked**.

This standard exists to make marking cheap enough that nobody is tempted to skip it. A rule
requiring full citation for every claim produces one of two outcomes: an unpublishable corpus, or
a corpus that cites loosely and calls it rigour. The `[VERIFY]` tag is the third option — publish,
mark, and track — and the tracking is [the Verification Log](../00-governance-map/verification-log.md),
which exists precisely so the tag cannot become a shrug.

Routed at `/method/epistemics/evidence-classes/`. Its enforcement surfaces are
[SITE-02 §9](../site/page-contract.md) line 13 (no number without a date or `data-count-src`) and
[ST-24 §8](st-24-page-prose-standard.md) (every claim carries a citation or an explicit mark as the
estate's own position).

---

## 2. Definition — the five evidence classes

| Class | Means | Publishable? |
|---|---|---|
| **E4** | Independently replicated, or a primary source the reader can retrieve | Yes |
| **E3** | Single credible primary source, cited and retrievable | Yes |
| **E2** | Secondary source, or the estate's own direct observation of an artefact | Yes, with provenance |
| **E1** | Reasoned position with an internal test; no external study | Yes, **marked as the estate's own** |
| **E0** | Assertion. No source, no test | **No** — either find E1+ or delete the sentence |

**E0 is the only unpublishable class**, and the boundary between E0 and E1 is the one that matters:
an E1 claim has a **test** — an argument that could be shown inconsistent. An E0 claim has
confidence.

### 2.1 E1 is legitimate and under-used

The estate's most common failure is not fabricating E3 citations. It is dressing an E1 position in
the grammar of established fact.

[ST-24 §8](st-24-page-prose-standard.md) gives the remedy and calls it under-used:

> *"the estate's own position, unsupported by external evidence"* is an honest sentence.

Two live instances, both load-bearing.
[ST-04's own claim card](st-04-falsifiability-and-claim-cards.md) declares `EVIDENCE E1` and admits
its Popperian lineage is *ancestry, not authority*.
[MX-023 §6](../corpus/mx-023-attention-and-human-sovereignty.md) declares that its position on
engagement optimisation *"rests substantially on a normative claim about autonomy rather than on
measured outcomes."* Neither is weaker for saying so; both are **checkable** in a way an
unmarked assertion is not.

### 2.2 E2 requires provenance of purpose

Direct observation of an artefact is E2 — and after
[C-14](../00-governance-map/corrections-log.md#c-14) it additionally requires
`provenance_of_purpose`: `demo`, `staging` or `production`.

The estate published **nine E2 claims** about its own live code — ad networks, no-JS render, flat
routes, nine animations. Every one accurate. All nine described a **prototype** and read as findings
about the estate ([DEF-024](../00-governance-map/defect-register.md#def-024)). The lesson is now
carried in three standards because it generalises:

> Reading an artefact tells you what is there. It cannot tell you what the artefact is **for**.

An E2 observation without provenance of purpose is not a false statement. It is an **unlabelled**
one — and no consistency check raises it.

---

## 3. Mechanism — the citation form

```
[claim] ([source], [date]) — E{n}
```

Three requirements, each closing a specific failure.

**Retrievable.** A citation a reader cannot follow is a gesture of authority. A dead link is a
defect and belongs in [the register](../00-governance-map/defect-register.md).

**Dated.** Undated citations are how a 2019 figure becomes a 2026 claim. This is the same principle
as [ST-05 §1](st-05-decay-and-review-intervals.md)'s macro frame — the undated claim is the
dominant pattern of the machine-mediated web, and it is refusable at almost no cost.

**Numbers carry a date or a `data-count-src`.** Every number, without exception. A typed count is a
claim with no falsifier, and [the defect register](../00-governance-map/defect-register.md) records
that a typed count which *undercounts defects* is the specific failure it exists to prevent. The
`data-count-src` attribute points at the JSON path the figure is computed from, so the number is
rendered from the same artefact an auditor would read.

### 3.1 The `[VERIFY]` tag

**What it is:** a marker on a claim the estate **believes true**, has published, and has **not
independently checked**. A statement carrying it may be relied on at the reader's discretion and
may not be cited as verified by this estate.

**What it is not** — four boundaries, each routing elsewhere:

| Not a… | Because | Belongs in |
|---|---|---|
| Placeholder | A placeholder has no content | `[BRACKETS]`, e.g. `[STEWARD NAME]` |
| Defect | A defect is a known shortfall; this is unknown correctness | [Defect Register](../00-governance-map/defect-register.md) |
| Open question | That needs a **decision**; this needs a **check** | [Open Questions](../00-governance-map/open-questions-and-ratifications.md) |
| Correction | That records something found **wrong**; this is not yet known either way | [Corrections Log](../00-governance-map/corrections-log.md) |

**The third boundary is the sharpest.** `[VERIFY]` asks *is this so?* An open question asks *what
shall we do?* Confusing them sends a factual question to the Curator's desk to await a decision
nobody needs to make.

**Two hard rules.** A tag on a claim the author **doubts** is a defect wearing a verification
marker — the test is that the estate must believe the claim true. And **a tag without a row in
[the Verification Log](../00-governance-map/verification-log.md) is invisible**; the row is added in
the same edit as the tag.

---

## 4. Worked instance — three claims from ST-22

[ST-22](st-22-platform-and-persistence.md) §5 renders six platform capacity figures. Each needed a
class before it could be published.

**"Cloudflare Pages imposes a 20,000-file ceiling."** Retrievable from the provider's published
terms → **E3**, cited with the date `2026-10-01`. And tagged `[VERIFY]` as
[V-07](../00-governance-map/verification-log.md), because the estate has **not re-read the terms
page** — the figure came from a source document, not from checking. That distinction is the whole
reason the tag exists.

**"The estate plans ≈2,000 files including assets."** The estate's own arithmetic over its own
route census → **E1**, marked as the estate's own computation, no external source possible.

**"Requests at 100k/day are the first tripwire."** An inference *from* the two figures above → **E1
resting on E3**, and it inherits the weaker parent's uncertainty. If V-07 resolves against the
20,000 figure, this claim moves too.

**What the instance shows.** Three sentences in one table, three different evidential situations,
and only the middle one is fully within the estate's knowledge. A reader who cannot see that
distinction cannot weight the table — and the six-figure table would look uniformly authoritative
without the classes.

---

## 5. Failure modes

**E0 in the grammar of E3.** The characteristic failure: a confident sentence with no source and
no test. *"Most learners abandon self-directed courses in the first fortnight."* Plausible,
unsourced, unfalsifiable as written.

**The tag as an escape hatch.** `[VERIFY]` on a claim the author suspects is wrong. §3.1's belief
test is the control.

**Tag inflation.** Marking everything unverified, making the log unreadable and the marker
meaningless. Thirteen open tags is manageable; a hundred and thirty would not be.

**Silent resolution.** A claim verified and the tag removed with no closure entry. The verification
leaves no trace, and a future reader cannot distinguish a checked claim from an unmarked one — which
is why [the log's §6](../00-governance-map/verification-log.md) specifies a closure format and
retains closed entries permanently.

**Citation laundering.** Citing a secondary source that cites a primary one, at the primary's
apparent strength. That is E2 presented as E3, and the fix is to read the primary or drop a class.

**The estate's live failure, stated plainly.** **Thirteen `[VERIFY]` claims are open and none has
ever been closed** ([DEF-030](../00-governance-map/defect-register.md#def-030)). Four are checkable
in minutes — a pricing page, an `rsync`, a link checker, nine RTL labels measured — and all four
were identified *while writing the instruments citing them*, then deferred. That is how a
verification queue becomes a graveyard, and publishing a log that exposes it does not discharge it.

---

## 6. Limits

**Class: technical.** No mechanism enforces evidence classes, dates or `data-count-src`. The check
would live in [SENTINEL](st-13-static-build-and-sentinel.md), which does not run
([DEF-001](../00-governance-map/defect-register.md#def-001)). So this standard is enforced by
whoever remembers it — and the tag sweep that would populate the Verification Log automatically
does not exist either, meaning the log's completeness depends on authors remembering to add rows.

**Class: epistemic.** Five classes is coarse, and the E2/E3 boundary is genuinely blurry: the
estate's own observation of its own artefact is more reliable than a weak secondary source and is
classed lower. The scheme prefers a rule that is applied to a rule that is right.

**Class: governance.** Four rows in the log name **Counsel** or **a qualified scholar** as
resolver, and the estate has engaged neither. Those cannot close by internal diligence at any
level — honest rather than negligent, and not to be mistaken for a moving queue.

---

## 7. Falsifier

This standard is wrong if:

1. **A claim needs a class the five do not offer** — under-inclusive. Candidate: a claim resting on
   a source the estate holds but may not republish.
2. **Two authors classify the same claim differently** using §2, showing the classes too vague to
   be a procedure. The E2/E3 boundary is where this will surface first.
3. **`[VERIFY]` proves to be a permanent state rather than a queue.** If the log still reads *none
   closed* in twelve months, the tag is a licence to publish unverified claims rather than a
   commitment to check them, and §3.1 should be narrowed to forbid publication instead. **This
   falsifier is currently the closest to firing** and the estate names it as such.
4. **Marked E1 claims prove no more reliable than unmarked assertions**, falsifying §2.1's premise
   that marking improves anything.

---

## 8. Obligation

**For any author:** every substantive claim carries a class. No number without a date or
`data-count-src`. Where the honest class is E1, **say so in the prose** — the sentence *"the
estate's own position, unsupported by external evidence"* is available and under-used. Delete E0
sentences rather than softening them.

**For any author adding a `[VERIFY]` tag:** add the log row in the same edit.

**For the estate:** close V-07, V-08, V-10 and V-13 — the four that cost minutes — before the next
release. Failing to close items that cheap, while publishing a log whose purpose is to expose
exactly that, is **HX‑15** committed by the mechanism built to prevent it.

**For a reader:** any claim carrying `[VERIFY]` may not be cited as verified by this estate, and
under [GM-11 §2](../00-governance-map/machine-reading-contract.md) condition 3 the tag must be
preserved verbatim in any quotation.

**Under ML-2.3:** §H.2 (epistemic dependency), §H.4 (optimisation disclosure), §H.17
(non-theatre), §H.19 (authorship of record), §E.5 (narrowing on demonstrated falsification).

---

**Related:** [ST-04 Falsifiability and Claim Cards](st-04-falsifiability-and-claim-cards.md) ·
[ST-05 Decay and Review Intervals](st-05-decay-and-review-intervals.md) ·
[ST-02 Front-Matter Schema](st-02-front-matter-schema.md) ·
[Verification Log](../00-governance-map/verification-log.md) ·
[ST-24 Page Prose Standard](st-24-page-prose-standard.md) ·
[Machine Reading Contract](../00-governance-map/machine-reading-contract.md)

*Curated by Maher. Five evidence classes, one unpublishable, four boundaries around the
`[VERIFY]` tag — and thirteen tags open with none ever closed, which is the number that will
decide whether the tag is a queue or an excuse.*
