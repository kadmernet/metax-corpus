---
doc_id: REG-04
title_en: Media Registry
title_ar: سجل الوسائط
family: registries
version: v2026.10.1
status: published
authority: record
prevailing_text: ar
audience_tier: 3
depth: meta
evidence_class: semi-durable
review_interval_months: 6
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [media, images, provenance, registry, accessibility]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. Four images supplied to the estate remain unexamined and are registered in that state.
route: /registries/media/
---

# REG-04 — Media Registry

> **Authority note.** A **record**, outside the precedence ladder
> ([GM-01](../00-governance-map/precedence-and-conflict-rules.md)). Accessibility
> duties for media are governed by [MX-010](../corpus/mx-010-accessibility.md) and
> [ST-12](../standards/st-12-accessibility-implementation.md); AI-generation
> disclosure by [MX-007](../corpus/mx-007-ai-use-and-disclosure.md); licensing by
> [ML-2.3](../license/the-maher-license.md). This page records provenance and state.

> **Disclosure first.** The register's most important rows are the ones marked
> **`unexamined`**. Four image files were supplied to the estate and have never
> been opened, described, or given alternative text. They are recorded here in
> that exact state rather than omitted, because an unexamined asset that nobody
> has written down is indistinguishable from an asset that does not exist — and
> the two have very different consequences.

---

## 1. Position

Media is where three duties collide and where corpora usually fail quietly:

| Duty | Source | Tier |
|---|---|---|
| Every non-decorative image has a text equivalent | [MX-010](../corpus/mx-010-accessibility.md) | 3 |
| Implementation pattern for that equivalent | [ST-12](../standards/st-12-accessibility-implementation.md) | 5 |
| Synthetic media is disclosed as synthetic | [MX-007](../corpus/mx-007-ai-use-and-disclosure.md) | 3 |
| Provenance is recorded and retrievable | [GM-12](../00-governance-map/archive-register.md) | — record |

Prose failures are visible: a bad sentence looks bad. Media failures are
**invisible to the author** — a missing `alt` attribute reads perfectly to the
person who can see the picture. The register exists because self-inspection does
not catch this class of fault.

## 2. Definition

A **media asset** is any non-text file intended to be served to a reader: raster
image, vector diagram, audio, video, font subset, downloadable data file.

Each asset carries **six** recorded properties. All six are mandatory; a row
missing any is `incomplete`:

1. **Identifier** — stable, assigned once, immortal per
   [ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md).
2. **Provenance** — one of `original` · `supplied` · `licensed-third-party` ·
   `ai-generated` · `unknown`.
3. **Rights basis** — the specific permission relied on, not a vague claim.
4. **Text equivalent** — `alt` text, or a declaration of `decorative`, or a long
   description route.
5. **Examination state** — `examined` · `unexamined`. An asset is `examined` only
   when a human or system has actually inspected its content and written a
   description.
6. **Placement** — the routes where it appears, or `unplaced`.

### 2.1 The `unknown` provenance is not permitted for publication

An asset whose provenance is `unknown` may be **registered** but must not be
**published**. This is stricter than copyright prudence requires and is deliberate:
under [ML-2.3 §H](../license/the-maher-license.md) the estate holds itself to
accounting for what it puts in front of a reader. "We found it" is not an account.

### 2.2 Decorative is a claim, not a default

Marking an asset `decorative` asserts that **no information is lost** when it is
not rendered. That is a falsifiable claim about content, and a reader who can
identify information conveyed only by the image has falsified it. `decorative` is
therefore never the correct treatment for a chart, a diagram, a screenshot, a
photograph of a person, or any image whose caption would be non-trivial.

## 3. Mechanism

### 3.1 Intake

```
asset arrives  →  identifier assigned        [immortal]
               →  provenance recorded        [must not be `unknown` to proceed]
               →  content EXAMINED           [human or system inspection]
               →  text equivalent written    [alt / decorative / long-desc]
               →  rights basis stated
               →  placement recorded
               →  publishable
```

The gate is **examination**. An asset cannot skip from intake to publication, and
the register's `unexamined` state exists precisely to make skipping visible.

### 3.2 Synthetic media

Any asset with provenance `ai-generated` must additionally carry:

- the **fact** of generation, visible to the reader at the point of use — not
  buried in a registry;
- a statement of **what the image depicts versus what it evidences**. A generated
  illustration of a mechanism is a diagram; it is never evidence that the
  mechanism exists. Treating it as evidence is the counterfeit
  [ST-04 §3](../standards/st-04-falsifiability-and-claim-cards.md) names.

The estate additionally **refuses** three uses of synthetic media outright, per
[MX-007 §3](../corpus/mx-007-ai-use-and-disclosure.md):

1. synthetic images of identifiable real people;
2. synthetic images presented as photographic documentation of an event;
3. synthetic charts — a chart must be rendered from data, never drawn to look like
   it was.

### 3.3 Text equivalents

| Asset kind | Required equivalent | Insufficient |
|---|---|---|
| Chart / graph | The data, or a route to it | "Chart showing results" |
| Diagram of a process | The process in prose | "Diagram" |
| Screenshot of an interface | The interface state and the relevant text | "Screenshot" |
| Photograph illustrating a concept | What is depicted, and why it is here | filename |
| Pure ornament | `decorative` declaration | empty `alt` with no declaration |

The pattern: the equivalent must carry the **information**, not the **fact that an
image exists**. "Chart showing results" tells a non-seeing reader only that they
are missing something.

## 4. Worked instance

**The four unexamined images, traced honestly.**

Four image files were supplied to the estate alongside the design and licence
documents. What is known about them is: they exist, they were supplied, and they
were supplied in a context concerning site design. What is **not** known: what
they depict, whether they contain text, whether they contain identifiable people,
whether they are original to the supplier, or whether any of them is a chart whose
data would be needed for a text equivalent.

Walk the §3.1 gate with them:

| Step | Status |
|---|---|
| Identifier assigned | Done — `IMG-001`…`IMG-004` (now immortal) |
| Provenance | `supplied` — known |
| Content examined | **No** |
| Text equivalent | **Impossible until examined** |
| Rights basis | **Undetermined** — supplier's own rights unstated |
| Placement | `unplaced` |
| Publishable | **No** |

The instructive part is that the blockage is **not** accessibility and **not**
rights. Those are downstream. The blockage is step 3, an act of inspection that
would take minutes and has not happened. This is the smallest possible unit of
estate failure: a cheap step, not taken, blocking four assets and one section of a
design document.

Contrast an asset that passed. `IMG-005`, the estate's own navigation geometry
sketch referenced by [DS-07](../design/ds-07-navigation-geometry.md): original,
examined, equivalent written as prose describing the breakpoint behaviour
(1000→1180px), rights basis `original work of the curator`, placed at one route.
Six properties, six answers, publishable. That is what a complete row looks like,
and the estate has very few of them.

## 5. The register

Provenance: `original` · `supplied` · `licensed-third-party` · `ai-generated` · `unknown`.
Examination: `examined` · `unexamined`.

| ID | Kind | Provenance | Rights basis | Text equivalent | Examined | Placement | Publishable |
|---|---|---|---|---|---|---|---|
| `IMG-001` | image | `supplied` | **undetermined** | **none** | `unexamined` | `unplaced` | **No** |
| `IMG-002` | image | `supplied` | **undetermined** | **none** | `unexamined` | `unplaced` | **No** |
| `IMG-003` | image | `supplied` | **undetermined** | **none** | `unexamined` | `unplaced` | **No** |
| `IMG-004` | image | `supplied` | **undetermined** | **none** | `unexamined` | `unplaced` | **No** |
| `IMG-005` | diagram | `original` | curator's own work | prose in DS-07 §3 | `examined` | `/design/ds-07/` | Yes |
| `FNT-001` | font subset | `licensed-third-party` | web font licence, terms not archived | n/a | `examined` | tokens layer | **Conditional** — see §5.1 |

### 5.1 Row notes

- **`IMG-001`…`IMG-004`** — Four assets, one blocking step. Filed as a task, not a
  defect, because nothing incorrect has been published; the fault is omission.
  If any is ever placed without examination, it becomes a defect immediately.
- **`IMG-005`** — The only fully compliant row in the register. One of six.
- **`FNT-001`** — The licence **terms are not archived**. The estate is relying on
  a permission it cannot produce. Under
  [GM-12](../00-governance-map/archive-register.md) Class B this is an
  unretrievable provenance record, and it is the same failure class as the two
  texts already logged at
  [DEF-029](../00-governance-map/defect-register.md). Marked `Conditional`:
  currently in use, not defensible if challenged.

### 5.2 What the register does not contain

- **No audio.** None exists. If audio is ever published, transcripts are required
  by [MX-010](../corpus/mx-010-accessibility.md), not optional.
- **No video.** Same, plus captions.
- **No AI-generated imagery.** The estate has generated none. Should it, §3.2
  applies and the disclosure must be at the point of use.
- **No charts.** Consistent with §3.2(3): the estate has data it has not plotted
  rather than plots it cannot substantiate.

## 6. Failure modes

| # | Failure | Mechanism | Current state |
|---|---|---|---|
| F1 | **Publication before examination** | Asset placed because it "looks fine" | Prevented only by the §3.1 gate being honoured manually |
| F2 | **Equivalent names the medium, not the content** | "Diagram of architecture" | **Latent** — the estate's few equivalents are prose, but no audit has run |
| F3 | **Decorative overclaim** | Informative image marked decorative to skip work | Not observed; nothing to observe with 1 placed image |
| F4 | **Rights amnesia** | Permission relied on, terms not kept | **Occurring** — `FNT-001` |
| F5 | **Synthetic passed as documentary** | Generated illustration cited as evidence | Not observed; refused by §3.2 |
| F6 | **Unexamined accumulation** | Assets pile up faster than they are inspected | **Occurring** — 4 of 6 rows |
| F7 | **Orphan placement** | Asset served from a route absent from the register | Unverifiable — no build exists |

Note the ratio in F6: **two thirds of the register is unexamined.** A register in
that state cannot support any general claim about the estate's media compliance,
and none is made.

## 7. Limits

1. **No automated media audit.** [ST-13 SENTINEL](../standards/st-13-static-build-and-sentinel.md)
   specifies checks for missing `alt` attributes; it does not run
   ([DEF-001](../00-governance-map/defect-register.md)). Every property in §5 is
   hand-recorded.
2. **No file hashes.** Rows identify assets by identifier and description, not by
   content digest. An asset could be **substituted** without the register
   noticing. For a provenance record this is a serious weakness, and the remedy
   (record a digest per asset) is cheap and not done.
3. **Accessibility of equivalents is untested with assistive technology.**
   [ST-12 §4](../standards/st-12-accessibility-implementation.md) records that of
   nine tests, three have been run and two failed. No screen-reader pass has
   touched media.
4. **`FNT-001` is in use on an unarchived permission.** The honest description is
   that the estate is currently non-compliant with its own §2.1 spirit while
   remaining formally within it, because provenance is `licensed-third-party`
   rather than `unknown`. That distinction is thinner than the estate would like.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** any asset is served from a published route and is absent from §5;
> - **(b)** any asset marked `unexamined` is shown to have a text equivalent
>   somewhere in the estate — which would mean it was examined and the register
>   was not updated;
> - **(c)** any asset marked `decorative` is shown to convey information not
>   otherwise present on its page;
> - **(d)** `IMG-005`'s text equivalent is shown to omit information the diagram
>   conveys.
>
> (d) is the sharpest test, because it is the estate's one compliant row. If the
> single asset the estate has done properly turns out to have an inadequate
> equivalent, the method in §3.3 is wrong and not merely under-applied. No one has
> performed (d). It requires one reader, one page, and no tools.

## 9. Obligation

No obligation arises from a record. Bearing duties:

- Do not publish an `unexamined` asset — the gate in §3.1.
- Write equivalents that carry information, not existence —
  [MX-010](../corpus/mx-010-accessibility.md), [ST-12](../standards/st-12-accessibility-implementation.md).
- Disclose synthetic media at the point of use —
  [MX-007](../corpus/mx-007-ai-use-and-disclosure.md).
- Keep the permission you rely on — [GM-12](../00-governance-map/archive-register.md).
- Never draw a chart; render it from data — §3.2(3).

---

### Related

**Accessibility** — [MX-010](../corpus/mx-010-accessibility.md) ·
[ST-12](../standards/st-12-accessibility-implementation.md) ·
[SITE-02](../site/page-contract.md) · [RB-05](../rubrics/rb-05-harm-review-gate.md)

**Provenance and disclosure** — [MX-007](../corpus/mx-007-ai-use-and-disclosure.md) ·
[GM-12](../00-governance-map/archive-register.md) ·
[MX-013](../corpus/mx-013-records-and-versioning.md) ·
[ST-07](../standards/st-07-evidence-and-verify.md)

**Design placement** — [DS-07](../design/ds-07-navigation-geometry.md) ·
[DS-00](../design/ds-00-as-built-token-layer.md) ·
[ST-21 performance budgets](../standards/st-21-performance-budgets.md)

**Siblings** — [REG-02](reg-02-page-registry.md) ·
[REG-03](reg-03-book-registry.md) · [REG-06](reg-06-dataset-registry.md)

### Exit pair

1. **Examine four files.** The block on `IMG-001`…`IMG-004` is one act of
   inspection. Perform it and four rows change state.
2. **Test the one good row.** Read [DS-07](../design/ds-07-navigation-geometry.md)
   §3 without looking at the diagram. If you cannot reconstruct the breakpoint
   behaviour, falsifier §8(d) has fired.

<!-- mx-pagestamp: REG-04 · v2026.10.1 · record · reviewed 2026-09-16 · next review 2027-03-16 -->
<!-- mx-demo: the published site is a demonstration; no media asset is served from a live build -->
