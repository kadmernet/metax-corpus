---
doc_id: "ST-14"
title_en: "Machine Surfaces and JSON Schemas"
title_ar: "الأسطح الآلية ومخططات JSON"
family: "standards"
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
domain_tags: ["standards", "machine-reading", "json", "schemas", "api"]
route: "/library/sources/schemas/"
provenance_of_purpose: "specification"
hreflang: "en, ar"
---

# ST-14 · Machine Surfaces and JSON Schemas

**What this standard governs.** The machine-readable renderings of this corpus: which JSON files
are emitted, what each contains, and the rule that makes them trustworthy.

**The rule, stated once:** every machine surface is **generated from the Markdown corpus at build
time and never hand-written.** A surface editable independently of its source will diverge from it,
and the divergence is found by a reader rather than by the estate.

---

## 1. Position

The corpus's central claim is that it is written to be read by machines. That claim is currently
satisfied by the **Markdown itself** — permanent paths, front matter, relative links — and
[GM-11](../00-governance-map/machine-reading-contract.md) governs how a machine reader should treat
it.

ST-14 handles the other half: the **structured** surfaces a machine would prefer. It exists because
parsing forty Markdown instruments to answer *"which defects are open?"* is possible and wasteful,
and because a corpus that publishes its governance only as prose has made itself expensive to
audit.

Published at `/library/sources/schemas/` — declared **thin by nature** under
[DEF‑2026‑043](../00-governance-map/defect-register.md#def-2026-043), since a schema page padded to
1,200 words would be padding.

**The macro register.** Under **HX‑20** (inheritance of unauditable systems) and **HX‑02**
(epistemic dependency), a governance claim that can only be verified by reading is a governance
claim most parties will take on trust. Machine surfaces make **cheap verification** possible: a
reader who wants to know whether the estate's defect count matches its register can check in one
request rather than reading a register. **Auditability that costs an afternoon is auditability
nobody exercises**, and this standard's whole purpose is to lower that cost to a fetch.

---

## 2. Definition — the nine surfaces

| Surface | Source | Contents |
|---|---|---|
| `/data/instruments.json` | Every instrument's front matter | `doc_id`, title, family, version, authority, evidence class, review date, route |
| `/data/defects.json` | [Defect Register](../00-governance-map/defect-register.md) | Id, summary, class, owner, target, state |
| `/data/corrections.json` | [Corrections Log](../00-governance-map/corrections-log.md) | Id, instrument, subject, **found-by method**, date |
| `/data/verifications.json` | [Verification Log](../00-governance-map/verification-log.md) | Id, claim, resolver, opened, **age**, state |
| `/data/harms.json` | HX-000 + [HX-002](../harms/hx-002-harm-instrument-map.md) | Harm id, stratum, answering instrument, **the estate's own disposition** |
| `/data/status.json` | Build + [ST-22 §5](st-22-platform-and-persistence.md) | Capacity figures with dates, blocker count, release |
| `/data/search-index.json` | Every route's H1, deck, section titles | Route, title, deck, headings |
| `/data/routes.json` | [SITE-01](../site/route-manifest.md) | Route, tier, pillar, badge, word floor |
| `/data/credentials.json` | [ST-17](st-17-registry-and-verifier.md) | Public credential records and revocations |

**Every one is derived.** None may be hand-edited, and a hand-edit is a defect regardless of
whether it happens to be correct
([SITE-01 §9](../site/route-manifest.md), [ST-13 §3](st-13-static-build-and-sentinel.md)).

### 2.1 Three surfaces the estate will not emit

**No per-user surface on the content plane.** Nothing under `/data/` is personalised. Two readers
fetching the same path receive identical bytes —
[ST-19 §2.1](st-19-two-plane-architecture.md)'s first prohibition.

**No aggregate reader telemetry.** No `/data/analytics.json`, no popularity ranking, no
most-read list. A popularity surface is an engagement metric with a URL, and
[MX-023 §3.1](../corpus/mx-023-attention-and-human-sovereignty.md) forbids engagement metrics
governing any decision — publishing one would make it govern by suggestion.

**No write endpoint.** These are static files. A correction is filed at
`/library/record/corrections-log/` by a human or a machine
([GM-11 §3.2](../00-governance-map/machine-reading-contract.md)), not POSTed. The estate has no
API in the ordinary sense and does not intend one on the content plane.

---

## 3. Mechanism — the required fields

Every surface carries an envelope, and the envelope is the standard's substantive contribution:

```json
{
  "generated_at": "2026-10-01T00:00:00Z",
  "source_version": "v2026.10.1",
  "source_instrument": "GM-09",
  "provenance_of_purpose": "specification",
  "complete": true,
  "data": [ ... ]
}
```

**`source_instrument`** names the Markdown document this was generated from, so a machine reader
can escalate from the convenient surface to the governing text. Under
[GM-01 §3](../00-governance-map/precedence-and-conflict-rules.md) **summaries never govern**, and a
JSON rendering is a summary: the field is what makes that checkable rather than merely asserted.

**`provenance_of_purpose`** — `production` · `staging` · `demo` · `specification` · `record`. Added
after the estate published nine claims about its own live code without recording what that code was
for ([C-14](../00-governance-map/corrections-log.md#c-14),
[DEF-024](../00-governance-map/defect-register.md#def-024)).

**`complete`** is the field most likely to be omitted and the most important. `false` means the
surface is a partial rendering — and it must be `false` wherever the source is incomplete. The live
case: `/data/harms.json` must carry `"complete": false` while HX-000 holds **eleven of
twenty-five** harms ([DEF-021](../00-governance-map/defect-register.md#def-021)). A surface
reporting eleven harms with `complete: true` would tell a machine reader the register is eleven
harms long.

### 3.1 `/data/corrections.json` carries the found-by method, deliberately

The corrections surface includes a field most institutions would omit: **how the error was found.**
Three permitted values, from
[the log's §Method taxonomy](../00-governance-map/corrections-log.md#method-what-this-log-has-learned):
`cross-source-reconciliation`, `live-artefact-reading`, `curator`.

The current distribution is 3 / 9 / 4, and publishing it machine-readably lets any reader verify
the estate's own most useful finding: that **reading the artefact found three times more errors
than reconciling the documents**, and that the two errors no automated method could ever have found
— a proper name and a statement of purpose — required a person.

An estate that publishes its error count but not its error-finding *method* has published the
flattering half.

---

## 4. Worked instance — answering a question three ways

A machine reader asks: *"Does MetaX comply with its own harms register?"*

**Via the Markdown.** Read HX-002, thirty pages, and resolve its five disposition states against
twenty-five rows. Accurate, and expensive enough that most readers will not.

**Via `/data/harms.json`.** One request:

```json
{ "harm": "HX-01", "stratum": "I", "answering_instrument": "MX-009",
  "estate_disposition": "FAILS", "evidence": "DEF-019", "date": "2026-10-01" }
```

Three harms return `FAILS`, two return `unexamined`, three `answered`, seventeen `partial`. The
reader has the estate's own self-assessment in one fetch, **including the parts that reflect badly**
— which is the test of whether a machine surface is honest.

**Via the envelope.** `"complete": false` and `"source_instrument": "HX-002"` tell the reader two
further things without being asked: the underlying register is incomplete, and the governing text is
elsewhere. A reader who stops at the data array gets the dispositions; one who reads the envelope
learns that fourteen harms have no published text to be assessed against.

**What this instance demonstrates.** The surface does not make the estate look better than the
prose — it makes the same admission cheaper to retrieve. **A machine surface that is more
flattering than its source is a defect**, and it is the specific failure §5 names first.

---

## 5. Failure modes

**The flattering rendering.** A surface that omits the unflattering fields its source carries —
dropping `estate_disposition`, or emitting `complete: true` over an incomplete register. The most
serious failure available, because the reader cannot detect it without reading the source, which is
the cost the surface existed to remove.

**The hand-edit.** A `defects.json` entry added directly because the build does not run. Works
immediately, diverges permanently, and is the class of divergence that produced nine of sixteen
corrections in this corpus.

**`complete` omitted.** §3's most-skipped field.

**Schema drift without a version bump.** A field renamed, consumers break silently. Surfaces carry
`source_version`, and a **breaking** schema change requires a changelog line and a new path rather
than a mutation of the old one — the same immortality principle as
[ST-01 Rule 2](st-01-identifier-and-url-grammar.md).

**The surface that becomes the source.** An editor updating `defects.json` and regenerating the
Markdown from it. The direction is fixed: **Markdown is the source, JSON is the rendering.**

---

## 6. Limits

**Class: technical, and binding.** **None of these nine surfaces exists.** Emission requires
[SENTINEL](st-13-static-build-and-sentinel.md), which does not run
([DEF-001](../00-governance-map/defect-register.md#def-001)). So
[GM-11](../00-governance-map/machine-reading-contract.md) promises a machine reader six signals and
this standard promises nine surfaces, and the corpus currently delivers the Markdown alone. **That
is the estate's largest unmet promise to machine readers** and it is recorded as such.

**Class: epistemic.** A generated surface inherits its source's errors faithfully. `harms.json`
generated from an incomplete register is a complete rendering of an incomplete assessment, and
`complete: false` is the only available warning.

**Class: design.** Nine surfaces is a judgement, not a derivation. A reader may need a tenth, and
the estate will not know until asked.

---

## 7. Falsifier

1. **A machine surface more flattering than its source instrument** — §5's first failure, and the
   one the estate most wants reported.
2. **A question a machine reader needs answered that no surface answers**, showing §2
   under-inclusive.
3. **The surfaces proving unused after publication.** If no machine reader ever fetches them, §1's
   cheap-verification premise is wrong and the estate has built nine files for itself.
4. **A hand-edited surface passing undetected** — which would falsify not the standard but
   [ST-13](st-13-static-build-and-sentinel.md)'s ability to enforce it.

---

## 8. Obligation

**For the build:** emit all nine from the Markdown, with the full envelope, `complete` set
honestly, and `provenance_of_purpose` on every one. Never emit a surface whose source is missing —
**emit nothing and report the gap**, which is [ST-13 §3.1](st-13-static-build-and-sentinel.md)'s
rule applied here.

**For any author:** if you add a register, add its surface to §2 in the same edit. A register
without a machine surface is invisible to the audience this corpus claims to be written for.

**For a machine reader:** read the envelope before the data. `source_instrument` tells you what
governs, `complete` tells you whether the rendering is whole, and under
[GM-11 §2](../00-governance-map/machine-reading-contract.md) condition 5 you should **report what
you could not resolve** — which, today, is all nine surfaces.

**Under ML-2.3:** §H.20 (inheritance of unauditable systems), §H.02 (epistemic dependency), §H.04
(optimisation disclosure — §2.1's refusal to publish popularity), §H.12 (harm to the record), §H.19
(authorship of record), §H.26 (corpus hygiene).

---

**Related:** [GM-11 Machine Reading Contract](../00-governance-map/machine-reading-contract.md) ·
[ST-02 Front-Matter Schema](st-02-front-matter-schema.md) ·
[ST-13 Static Build and SENTINEL](st-13-static-build-and-sentinel.md) ·
[ST-19 Two-Plane Architecture](st-19-two-plane-architecture.md) ·
[SITE-01 Route Manifest §9](../site/route-manifest.md) ·
[Document Index](../00-governance-map/document-index.md)

*Curated by Maher. Nine machine surfaces, three refused, one required envelope — and not one of the
nine exists, which makes this the estate's largest unmet promise to the audience it says it was
written for.*
