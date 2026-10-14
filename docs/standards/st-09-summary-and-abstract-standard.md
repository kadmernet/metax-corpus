---
doc_id: ST-09
title_en: Summary and Abstract Standard
title_ar: معيار الملخصات والخلاصات
family: standards
version: v2026.10.1
status: published
authority: operative-form
prevailing_text: ar
audience_tier: 3
depth: meta
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: no
last_reviewed: 2026-09-16
domain_tags: [summaries, abstracts, authority, machine-reading, standards]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000 — a class of reader that consumes summaries more readily than full texts, which is the risk this standard exists to manage.
route: /standards/st-09/
---

# ST-09 — Summary and Abstract Standard

> **Authority.** `operative-form`, tier 5. Governs the **form of every summary** in
> the corpus. The rule it implements is
> [GM-01 §3](../00-governance-map/precedence-and-conflict-rules.md): **summaries
> never govern.** Machine-facing surfaces are
> [ST-14](st-14-machine-surfaces-and-json-schemas.md); the reading contract is
> [GM-11](../00-governance-map/machine-reading-contract.md).

> **Disclosure first.** The estate publishes at least one document that is
> functionally a summary and is easy to mistake for governing text:
> [MX-012 licensing and reuse](../corpus/mx-012-licensing-and-reuse.md), which
> summarises [ML-2.3](../license/the-maher-license.md) and **governs nothing**. Its
> own title does not say so. This standard exists because that pattern — an
> accurate, readable, non-governing summary of a hard instrument — is the most
> likely route by which a reader ends up relying on the wrong text.

---

## 1. Position

A summary is a **convenience with a failure mode**: it is read instead of the
thing it summarises, by exactly the readers least equipped to notice the
difference.

Three properties make this acute in a governance corpus:

1. **Summaries are more readable than governing text**, so they win attention.
2. **Governing text is long because precision requires it** — [ML-2.3](../license/the-maher-license.md)
   has 25 harms, 8 absolutes, and a condition/covenant split; no honest summary
   preserves all of it.
3. **Machine readers prefer structured brevity.** An AI system given both a
   summary and a 90,000-byte instrument will often use the summary, which is a
   real and current risk given [MX-018 D5](../corpus/mx-018-third-party-dependencies.md).

So the standard's approach is not to forbid summaries but to make them **loudly
subordinate**: every summary must announce its own inadequacy at the top, name
what it drops, and point at what governs.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **summary** | A shorter restatement of another instrument, intended to be read in its place |
| **abstract** | A ≤ 120-word statement of what an instrument does, intended to help a reader decide whether to read it |
| **digest** | A structured extraction (tables, lists) of an instrument's provisions |
| **lossy element** | Anything the source states that the summary does not |
| **governing text** | The instrument that actually binds — never the summary |

### 2.1 Abstract ≠ summary

| | Abstract | Summary |
|---|---|---|
| Purpose | Decide whether to read | Read instead of |
| Length | ≤ 120 words | Unbounded |
| May state obligations? | **No** — may only name their subject | Yes, with §3's furniture |
| Risk | Low | **High** |
| Required on every page? | Encouraged | No |

The distinction is load-bearing. An abstract that states an obligation has become
a summary and acquires all of §3's duties. "This instrument governs advertising"
is an abstract. "This instrument prohibits sponsored content" is a summary.

## 3. The five required elements of a summary

Cumulative. A summary missing any one is non-compliant and must not be published.

| # | Element | Form |
|---|---|---|
| **S1** | **Subordination notice**, at the top, before any substance | "This is a summary. It governs nothing. [Instrument X] governs." |
| **S2** | **Link to the governing text**, in the notice itself | Relative path, per [ST-08](st-08-cross-reference-and-link-integrity.md) |
| **S3** | **Named lossy elements** — what this summary drops | A list, not "some details omitted" |
| **S4** | **Version pinning** — the version summarised | `doc_id` + version; a summary of an unnamed version is useless |
| **S5** | **Staleness condition** — when this summary becomes wrong | "Void when [X] changes version" |

### 3.1 S3 is the substance

"Some details omitted" is not compliance. S3 requires the summary to name the
elements a reader would need and will not find. A worked example for a summary of
ML-2.3:

> **This summary drops:** the condition/covenant split of §F.4 (four automatic, 19
> curable at 30/90 days); the disjunctive character of absolute (vii); the Scale
> Gate tiers of §H.2-bis; the all-clear presumption of §H.16.3; and 20 of the 25
> harms by name.

A reader who sees that list knows what they are missing. A reader who sees "some
details omitted" believes they are missing trim.

### 3.2 S5 and version rot

A summary is correct only against one version. Without S5 a summary of v2026.09
persists next to a v2026.10 instrument, and nothing on its face says so. S5's
staleness condition makes the summary self-invalidating rather than quietly wrong
— the same principle as the review-date visibility argued at
[MX-019 §6](../corpus/mx-019-sunset-and-wind-down.md).

### 3.3 What a summary must never do

- **Never** paraphrase an absolute. The eight absolutes of
  [§H.3(a)](../license/the-maher-license.md) must be quoted or omitted — never
  restated, because a paraphrase of an absolute creates a second, non-identical
  absolute.
- **Never** simplify a disjunctive/cumulative distinction. Absolute (vii) is
  disjunctive; every other absolute is cumulative. A summary that presents all
  eight uniformly has altered the licence's operation.
- **Never** state a number that appears in the source without the source's
  qualification (the unpublished Scale Gate thresholds, for instance, must not be
  summarised as though determinate).
- **Never** carry a title that reads as governing. See §6.

## 4. Mechanism

### 4.1 Compliance check

```
is it shorter than its source and meant to be read instead?   no  → not a summary
                                                              yes → S1..S5 required
does it state an obligation?                                  yes → it is a summary,
                                                                     not an abstract
does it paraphrase an absolute?                               yes → REFUSE publication
does it name its lossy elements specifically?                 no  → non-compliant
```

### 4.2 Machine-facing summaries

[ST-14](st-14-machine-surfaces-and-json-schemas.md) specifies nine machine
surfaces, **refuses three**, and none exists. Where a machine surface carries a
summary field, S1–S5 apply in structured form: an `authority` field reading
`summary`, a `governs` field naming the instrument, a `lossy` array, a
`summarised_version` string, and a `void_when` condition.

The refusal in ST-14 that matters here: **the estate refuses to publish a machine
surface that presents summary content without a subordination field.** A machine
reader given an unmarked summary has no way to discover it is not governing, and
[GM-11](../00-governance-map/machine-reading-contract.md) places that duty on the
corpus, not the reader.

### 4.3 The estate's own worst case

[MX-012](../corpus/mx-012-licensing-and-reuse.md) is a summary of ML-2.3 occupying
a `governing`-looking slot in the corpus family, titled "Licensing and Reuse".
Its own text states it governs nothing. Its **title and family do not.**

Under §3 it requires S1–S5. What it should carry, and does not carry in the
required form, is a title that discloses its character — and the estate cannot
rename the file, because the route is published and identifiers are immortal
([ST-01 Rule 2](st-01-identifier-and-url-grammar.md)).

So the remedy available is **S1 stated at maximum prominence**, above everything
else on the page, and a `title_en` amended to read as a summary while the path
stays fixed. That is a small change to one field and it is owed.

## 5. Worked instance

**Writing a compliant one-paragraph summary of [ML-2.3 §F.4](../license/the-maher-license.md),
then checking it.**

> **This is a summary. It governs nothing.**
> [ML-2.3](../license/the-maher-license.md) v2.3 governs.
> **In outline:** breaches of the licence fall into two kinds. Four are
> *conditions*: breaching one terminates the licence automatically, with no notice
> and no cure period. Nineteen are *covenants*: breaching one is curable, within
> 30 or 90 days depending on the covenant, and the period runs **from notice**.
> **This summary drops:** which four provisions are conditions; which covenants
> carry 30 days and which 90; the interaction with the eight absolutes of §H.3(a);
> and the §H.16.3 all-clear presumption.
> **Void when** ML-2.3 changes version.

Check it against §3:

| Element | Present? |
|---|---|
| S1 subordination notice, at top | Yes, first line |
| S2 link in the notice | Yes |
| S3 lossy elements named specifically | Yes — four named, not "details" |
| S4 version pinned | Yes — v2.3 |
| S5 staleness condition | Yes |
| §3.3 no absolute paraphrased | Yes — absolutes referred to, not restated |

Compliant. Note three things about the result.

**First, it is longer than an incompliant summary would be**, and most of the
added length is S3. That is the correct trade: the list of omissions is more
useful to a reader deciding whether to open the licence than another sentence of
paraphrase.

**Second, it is still dangerous.** A reader who stops here knows that cure periods
exist and does **not** know whether *their* breach is a condition or a covenant —
which is the only question that matters in practice. A compliant summary is not a
safe summary; it is an honestly labelled one.

**Third, it exposes a hole in the source.** Writing S3 forced an enumeration of
what §F.4 leaves undetermined, and one item — *the period runs from notice* —
cannot be applied at all, because [MX-006 §5](../corpus/mx-006-contact-and-correspondence.md)
establishes that the estate usually cannot serve notice on a licensee. So the
nineteen covenants are practically unenforceable, and **a compliant summary of
§F.4 is more revealing about that defect than §F.4 itself.** That is an argument
for writing summaries carefully rather than for avoiding them.

## 6. Failure modes

| # | Failure | Mechanism | Current state |
|---|---|---|---|
| F1 | **Summary read as governing** | Readability advantage | **Live** — [MX-012](../corpus/mx-012-licensing-and-reuse.md), §4.3 |
| F2 | **"Some details omitted"** | S3 satisfied in form only | Prohibited by §3.1; unaudited |
| F3 | **Version-rotted summary** | S5 absent | No summary currently carries an S5 condition |
| F4 | **Absolute paraphrased** | Compression pressure | Prohibited by §3.3; **the most damaging single breach available** |
| F5 | **Machine surface without subordination field** | Structured brevity | Prevented by non-existence; will recur at first build ([ST-14](st-14-machine-surfaces-and-json-schemas.md)) |
| F6 | **Abstract drifts into summary** | An obligation stated in 120 words | Guarded by §2.1 |
| F7 | **Title implies authority** | Naming predates the standard | **Actual** — §4.3, unfixable by rename |

## 7. Limits

1. **No summary in the corpus currently carries all of S1–S5.** This standard is
   published in breach of itself by every existing summary, and the breaches are
   listed rather than corrected in the same act
   ([Charter §0.8](../corpus/mx-000-charter.md) forbids silent repair).
2. **No check runs.** S1–S5 compliance is a text property a script could verify;
   [ST-13 SENTINEL](st-13-static-build-and-sentinel.md) does not run
   ([DEF-001](../00-governance-map/defect-register.md)).
3. **F7 is unfixable by renaming**, because routes are permanent
   ([SITE-03](../site/routing-law.md)). Only prominence and `title_en` can be
   changed.
4. **The 120-word abstract bound is asserted**, not derived.
5. **This standard cannot reach summaries made by others.** A third party
   summarising ML-2.3 is bound by the licence, not by ST-09 —
   [MX-002 §6.2](../corpus/mx-002-terms-of-service.md) prohibits stripping
   disclosure, which is the nearest applicable duty and is weaker.
6. **No Arabic text**, while `prevailing_text: ar`. A summary standard in the
   subordinate language, governing summaries of instruments whose prevailing text
   does not exist, is a compounded version of the problem in
   [MX-020](../corpus/mx-020-language-authority.md).

## 8. Falsifier

> **IF FALSE.** This standard is falsified if:
>
> - **(a)** a published summary lacks any of S1–S5 — **this fires now** on every
>   existing summary, §7.1;
> - **(b)** a summary paraphrases one of the eight absolutes of §H.3(a);
> - **(c)** a summary states a number without the source's qualification;
> - **(d)** a machine surface publishes summary content with no subordination
>   field;
> - **(e)** an abstract is shown to state an obligation (§2.1);
> - **(f)** a reader is shown to have relied on a summary in preference to
>   governing text — which would show S1's prominence is insufficient and that the
>   whole approach of *labelling rather than forbidding* has failed.
>
> **(f) is the test of the standard's core design choice and the estate cannot run
> it**: it would require knowing what readers read, which
> [REG-06 `DSET-R01`](../registries/reg-06-dataset-registry.md) refuses. So ST-09's
> central premise — that a loud label is sufficient protection — is **E0** and will
> remain so. A reader who thinks summaries should simply be forbidden in a
> governance corpus has an argument the estate cannot refute with evidence.

## 9. Obligation

**On an author:**
- Never publish a summary without all five of S1–S5 (§3).
- Name lossy elements **specifically** (§3.1).
- Quote or omit absolutes; never paraphrase them (§3.3).
- Pin the version and state the staleness condition (S4, S5).
- Keep abstracts ≤ 120 words and free of obligations (§2.1).
- Treat writing S3 as a diagnostic on the source — §5 found a defect that way.

**On the estate:**
- Bring [MX-012](../corpus/mx-012-licensing-and-reuse.md) into S1–S5 compliance and
  amend its `title_en` to disclose its character (§4.3) — owed.
- Never publish a machine surface carrying summary content without a
  subordination field ([ST-14](st-14-machine-surfaces-and-json-schemas.md), §4.2).
- State plainly that the label-not-forbid approach is **E0** (§8f).
- Implement the S1–S5 check when a runner exists
  ([ST-13](st-13-static-build-and-sentinel.md)).

---

### Related

**The rule this implements** — [GM-01 precedence](../00-governance-map/precedence-and-conflict-rules.md) ·
[GM-11 machine reading contract](../00-governance-map/machine-reading-contract.md) ·
[ST-14](st-14-machine-surfaces-and-json-schemas.md) ·
[ST-04](st-04-falsifiability-and-claim-cards.md)

**The corpus's own summary** — [MX-012](../corpus/mx-012-licensing-and-reuse.md) ·
[ML-2.3](../license/the-maher-license.md) ·
[enforceability two-track table](../license/enforceability-two-track-table.md) ·
[scale gate](../license/scale-gate.md)

**Form and checking** — [ST-24](st-24-page-prose-standard.md) ·
[ST-08](st-08-cross-reference-and-link-integrity.md) ·
[ST-13](st-13-static-build-and-sentinel.md) ·
[SITE-02](../site/page-contract.md)

**Why the premise is untestable** — [REG-06](../registries/reg-06-dataset-registry.md) ·
[MX-023](../corpus/mx-023-attention-and-human-sovereignty.md) ·
[RB-04](../rubrics/rb-04-reader-comprehension-rubric.md) ·
[ST-07](st-07-evidence-and-verify.md)

### Exit pair

1. **Audit one summary.** Open [MX-012](../corpus/mx-012-licensing-and-reuse.md)
   and check it against S1–S5. Falsifier §8(a) predicts it fails.
2. **Read the text a summary cannot carry.**
   [ML-2.3 §H.3(a)](../license/the-maher-license.md) — eight absolutes, one of them
   disjunctive, none of which may be paraphrased.

<!-- mx-pagestamp: ST-09 · v2026.10.1 · operative-form · tier 5 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; no existing summary in the corpus is S1–S5 compliant -->
