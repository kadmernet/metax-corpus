---
doc_id: ST-16
title_en: Audience Tier and Register Standard
title_ar: معيار مستويات الجمهور والسجل الأسلوبي
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
domain_tags: [audience, tiers, register, micro-meta-macro, standards]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. The corpus contains almost no tier 1 writing, which §6 quantifies.
route: /standards/st-16/
---

# ST-16 — Audience Tier and Register Standard

> **Authority.** `operative-form`, tier 5. Governs the two front matter fields
> `audience_tier` and `depth` ([ST-02](st-02-front-matter-schema.md)). Prose form
> is [ST-24](st-24-page-prose-standard.md); summaries are
> [ST-09](st-09-summary-and-abstract-standard.md); accessibility is
> [ST-12](st-12-accessibility-implementation.md).

> **Disclosure first.** The corpus is written almost entirely at **tier 2–3** in
> the **meta** and **macro** registers. Of the instruments that a member of the
> public would actually arrive at — terms, privacy, demo notice, contact — only
> some are genuinely tier 1, and §6 counts them. An estate whose governing
> documents are addressed to specialists has, in effect, chosen its readership,
> and the choice is visible in these two fields.

---

## 1. Position

Two independent axes are routinely confused, and the corpus keeps them apart:

| Axis | Field | Asks |
|---|---|---|
| **Who is this for?** | `audience_tier` | What must the reader already know? |
| **At what altitude?** | `depth` | Is this about a mechanism, a system, or a principle? |

They are orthogonal. A **tier 1, macro** page is possible and valuable — a
plain-language statement of why the estate refuses advertising. A **tier 3, micro**
page is also possible — a specialist's account of one CSS token. Collapsing the
axes produces the standard failure of technical corpora: everything difficult is
also abstract, and everything accessible is also trivial.

## 2. Definitions

### 2.1 Audience tiers

| Tier | Reader | Assumed knowledge | Example |
|---|---|---|---|
| **1** | Any member of the public | **None.** No corpus vocabulary, no prior page | [MX-003 privacy](../corpus/mx-003-privacy-notice.md), [SITE-04 demo notice](../site/demo-notice.md) |
| **2** | A reader with a stake | Knows the estate exists; willing to follow one link | [MX-002 terms](../corpus/mx-002-terms-of-service.md), [MX-005 scope](../corpus/mx-005-scope-and-boundaries.md) |
| **3** | A practitioner or maintainer | Corpus vocabulary, precedence ladder, families | Standards, registries, rubrics |
| **4** | A machine reader | [GM-11](../00-governance-map/machine-reading-contract.md)'s five conditions | [ST-14](st-14-machine-surfaces-and-json-schemas.md) surfaces |

**Tier 1 is a hard constraint, not an aspiration.** It means: no undefined corpus
term, no reliance on having read another page, no precedence reasoning, and no
identifier used without its meaning given in the sentence.

### 2.2 Depth registers

| Register | Altitude | Characteristic move |
|---|---|---|
| **micro** | One mechanism, one rule | "Here is exactly what must happen" |
| **meta** | The system of rules | "Here is how these rules relate and where they fail" |
| **macro** | Principle and consequence | "Here is why this is the right constraint, and what it costs" |

### 2.3 The tier-1 test

> A page is tier 1 only if a reader who has **never seen this corpus** can act on
> it correctly after one reading, without following any link.

This is testable and most of the corpus fails it. A page that says "subordinate to
ML-2.3 (tier 1) and HX-000 (tier 1a, incorporated by §A.10)" is **not** tier 1,
whatever its front matter claims — and several pages labelled tier 1 open exactly
that way, including [MX-002](../corpus/mx-002-terms-of-service.md) and
[MX-003](../corpus/mx-003-privacy-notice.md).

## 3. The rules

| # | Rule | Rationale |
|---|---|---|
| **U1** | Declare both `audience_tier` and `depth` in front matter | [ST-02](st-02-front-matter-schema.md); machine readers rely on them |
| **U2** | A tier 1 page uses **no undefined corpus term** and requires **no prior page** | §2.3 |
| **U3** | A tier 1 page may **link** to specialist material but must not **depend** on it | A link is an offer; a dependency is a barrier |
| **U4** | Higher tiers may assume lower-tier content; never the reverse | Otherwise the ladder is decorative |
| **U5** | `depth` must match the page's actual altitude, not its subject's importance | Important subjects are not automatically macro |
| **U6** | Where an instrument must serve two tiers, **split the page**, do not average the register | An averaged register serves neither |
| **U7** | A reader-facing obligation must exist at tier 1 **somewhere**, even if its governing statement is tier 3 | A duty a lay reader cannot find is not a duty they can obey |

### 3.1 U7 is the substantive rule

Most of this standard is bookkeeping. U7 is the rule with teeth:

> **If the corpus imposes a duty on a reader, the duty must be findable and
> comprehensible at tier 1, even though the governing text may be tier 3.**

[MX-002 §6](../corpus/mx-002-terms-of-service.md) lists six things a user may not
do. Item 3 is *"Breach the licence absolutes. §H.3(a) lists eight. Seven are
cumulative; (vii) developmental substitution is disjunctive — it bites on its
own."*

That sentence is **not tier 1**. A lay reader cannot act on it: they do not know
what an absolute is, what cumulative and disjunctive mean in this context, or what
developmental substitution is. The governing statement is properly in
[ML-2.3](../license/the-maher-license.md); U7 requires that a tier 1 rendering
exist somewhere — and it does not.

This is the clearest breach in this standard and it sits on the estate's most
reader-facing instrument.

### 3.2 U6 and the split

The temptation, when a page must serve both a lay reader and a practitioner, is a
middle register. The result reads as slightly technical to the first and slightly
vague to the second.

U6 requires a split instead: a tier 1 page stating the duty plainly, and a tier 3
page stating it precisely, with the tier 1 page linking **down** (offering) and the
tier 3 page linking **up** (locating). The corpus does this nowhere, and doing it
for the licence absolutes would discharge §3.1.

## 4. Mechanism

### 4.1 Assigning the fields

```
who must be able to act on this page?
  any member of the public       → tier 1 → apply the §2.3 test HONESTLY
  someone with a stake           → tier 2
  a maintainer                   → tier 3
  a machine                      → tier 4

what does the page do?
  states one mechanism           → micro
  relates rules, shows failure   → meta
  argues a principle and cost    → macro
```

### 4.2 The tier-1 audit

A page claiming tier 1 must survive four passes:

| # | Pass | Fails if |
|---|---|---|
| P1 | **Vocabulary** | Any corpus term appears undefined in the sentence that uses it |
| P2 | **Dependency** | Acting correctly requires having read another page |
| P3 | **Identifier** | An identifier appears without its meaning in-sentence |
| P4 | **Action** | A reader cannot say what to do after one reading |

P3 is the pass most corpus pages fail, because the corpus's own design claim —
every identifier links to its defining document
([ST-08 §2.2](st-08-cross-reference-and-link-integrity.md)) — encourages dense
identifier use. **A link satisfies ST-08 and fails P3**: a tier 1 reader should not
have to follow it.

### 4.3 The two standards pull against each other

Worth stating plainly, because it is a genuine conflict inside the corpus:

- [ST-08 T2/§2.2](st-08-cross-reference-and-link-integrity.md) requires every
  identifier's first mention to be **linked**.
- **U2/P3** requires a tier 1 page to carry an identifier's **meaning in the
  sentence**.

Both are satisfiable together — *"the licence ([ML-2.3](../license/the-maher-license.md)),
which sets the terms on which you may reuse anything here"* — but only by writing
more words. The conflict is resolved in favour of **both**, at the cost of length,
and not by exempting tier 1 pages from linking.

## 5. Worked instance

**Rewriting one obligation from tier 3 to tier 1.**

Source, [MX-002 §6](../corpus/mx-002-terms-of-service.md) item 3, as published:

> *Breach the licence absolutes. §H.3(a) lists eight. Seven are cumulative;
> (vii) developmental substitution is disjunctive — it bites on its own.*

Run the §4.2 passes: **P1 fails** (absolute, cumulative, disjunctive,
developmental substitution — four undefined terms). **P3 fails** (§H.3(a)
unexplained). **P4 fails** — a reader cannot say what to avoid.

A tier 1 rendering:

> **You must not use anything here in a way that replaces a person's own
> development.** If what you build lets someone skip the learning instead of
> supporting it, you may not use this material — and this one rule stands alone:
> breaking it is enough on its own, even if you have followed every other rule.
> Seven further hard limits exist and are set out in the
> [licence](../license/the-maher-license.md); all seven have to be respected
> together.

Check it: P1 — no undefined term. P2 — no prior page needed. P3 — no bare
identifier; the licence is named by what it is. P4 — the reader knows what to
avoid. **Passes.**

### 5.1 What the rewrite reveals

Three things, and the third is the most useful.

**It is longer.** Roughly three times the source. Tier 1 costs words, which is why
the 1200-word floor and the tier system interact: a tier 1 page reaches the floor
easily and a tier 3 page reaches it by adding substance.

**It loses precision.** "Replaces a person's own development" is not §H.3(a)(vii).
It is a serviceable gloss that a careful licensee would need to check against the
governing text. That loss is acceptable **only because** the tier 1 rendering
points at the licence — which is [ST-09](st-09-summary-and-abstract-standard.md)'s
territory, and means **every U7 tier 1 rendering of a governing duty is a summary**
and therefore owes S1–S5: subordination notice, link, named lossy elements, version
pin, staleness condition.

**That connection was not designed.** U7 and ST-09 were written independently, and
working the instance shows U7 cannot be discharged without ST-09 compliance. So the
rule as drafted is incomplete, and the completion is stated here:

> **U7, completed.** A tier 1 rendering of a governing duty is a summary within
> [ST-09 §2](st-09-summary-and-abstract-standard.md) and must carry S1–S5. The
> rewrite above does **not** yet carry S3 (named lossy elements), S4 (version pin),
> or S5 (staleness condition), and is therefore non-compliant as it stands.

The estate publishes the incomplete example rather than a polished one, because the
gap between "reads well at tier 1" and "compliant" is exactly what an author needs
to see.

## 6. The tier census

| Tier | Instruments | Genuinely passing §4.2? |
|---|---|---|
| **1** | [MX-002](../corpus/mx-002-terms-of-service.md), [MX-003](../corpus/mx-003-privacy-notice.md), [MX-006](../corpus/mx-006-contact-and-correspondence.md), [SITE-04](../site/demo-notice.md) | **Probably only SITE-04.** The other three open with precedence reasoning (P1, P3 failures) |
| **2** | ~10 — scope, top levels, conflicts, security, credentials, appeals | Mostly appropriate |
| **3** | ~60 — all standards, registries, rubrics, governance map | Appropriate |
| **4** | 0 — [ST-14](st-14-machine-surfaces-and-json-schemas.md) specifies nine surfaces, **none exists** | n/a |

| Register | Count |
|---|---|
| micro | ~8 |
| meta | ~45 |
| macro | ~20 |

### 6.1 What the census shows

- **Tier 1 is effectively one page.** Four are labelled; by the standard's own test
  three fail. The estate has written a corpus for practitioners and labelled part of
  it public.
- **`meta` dominates at roughly 60%.** The corpus is mostly *about its own system
  of rules*. That is defensible for a governance estate and is also how a corpus
  becomes unreadable to anyone outside it.
- **micro is thin (~8).** Few pages state one mechanism plainly. This correlates
  with the tier 1 shortage: lay readers need micro pages.
- **Tier 4 is empty.** Machine surfaces are specified and unbuilt, so
  [GM-11](../00-governance-map/machine-reading-contract.md)'s six owed signals are
  three delivered and none structured.

## 7. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Tier 1 claimed, not achieved** | **Actual** — three of four (§6) |
| F2 | **Averaged register** | Guarded by U6; the corpus splits nowhere, so untested |
| F3 | **Duty unfindable at tier 1** | **Actual** — U7 breached on the licence absolutes (§3.1) |
| F4 | **Depth inflated by subject importance** | Guarded by U5; `macro` is the flattering label |
| F5 | **Identifier density defeating tier 1** | **Systemic** — §4.3 |
| F6 | **Tier 1 rendering that is a non-compliant summary** | **Actual** — §5.1, including the example in this very standard |
| F7 | **No tier 4 content** | **Actual** — §6 |

## 8. Limits

1. **The §4.2 audit has been run on five pages**, informally, by the author. The
   census in §6 is therefore an estimate, and its tier 1 column is the author
   marking its own work down — more credible than marking it up, still not
   independent ([MX-017 C1](../corpus/mx-017-conflicts-of-interest.md)).
2. **U7 is breached on the most important duty in the corpus** and the remedy (a
   tier 1 licence page) does not exist.
3. **No check runs.** P1–P4 are judgement passes; P3 could be partly mechanised and
   is not ([ST-13](st-13-static-build-and-sentinel.md)).
4. **U6 has never been exercised**; no page has been split.
5. **Tier 4 is empty**, so the fourth tier is a specification with no instance.
6. **No Arabic text**, while `prevailing_text: ar`. Tiering an audience for a corpus
   whose authoritative language is unwritten assigns tiers in the wrong language
   ([MX-020](../corpus/mx-020-language-authority.md)).

## 9. Falsifier

> **IF FALSE.** This standard is falsified if:
>
> - **(a)** a page declaring `audience_tier: 1` fails any of P1–P4 — **fires now**,
>   three times (§6);
> - **(b)** a reader-facing duty exists with no tier 1 rendering anywhere (U7) —
>   **fires now** on the licence absolutes;
> - **(c)** a tier 1 rendering of a governing duty lacks S1–S5 (§5.1) — **fires now**,
>   including on this standard's own §5 example;
> - **(d)** a page's `depth` is shown to misdescribe its altitude (U5);
> - **(e)** a lower-tier page is shown to depend on a higher-tier one (U4).
>
> **(a) and (b) are runnable by any lay reader**, and a lay reader is the only
> competent judge of (a): the author cannot un-know the vocabulary. That makes this
> one of the few standards in the corpus whose primary falsifier **must** be run by
> an outsider to mean anything.

## 10. Obligation

**On an author:**
- Declare both fields (U1).
- Apply the §2.3 test honestly before claiming tier 1; **if in doubt, it is tier 2**.
- Give an identifier's meaning in-sentence at tier 1, **and** link it (§4.3).
- Split rather than average when two audiences must be served (U6).
- Match `depth` to altitude, not to importance (U5).
- Treat any tier 1 rendering of a governing duty as a summary owing S1–S5
  ([ST-09](st-09-summary-and-abstract-standard.md), §5.1).

**On the estate:**
- Write a **tier 1 licence page** rendering the eight absolutes plainly, with
  S1–S5. This discharges U7 and is the single largest gap this standard exposes.
- Re-audit the four tier 1 claims and **downgrade the three that fail** rather than
  rewriting the front matter to look compliant.
- Add micro pages; ~8 is too few to serve a lay reader (§6.1).
- Ask a lay reader to run §9(a); the author cannot.

---

### Related

**Form and prose** — [ST-24](st-24-page-prose-standard.md) ·
[ST-09](st-09-summary-and-abstract-standard.md) ·
[SITE-02](../site/page-contract.md) · [ST-02](st-02-front-matter-schema.md)

**Reader-facing instruments** — [MX-002](../corpus/mx-002-terms-of-service.md) ·
[MX-003](../corpus/mx-003-privacy-notice.md) ·
[MX-006](../corpus/mx-006-contact-and-correspondence.md) ·
[SITE-04](../site/demo-notice.md)

**The duty needing a tier 1 rendering** — [ML-2.3](../license/the-maher-license.md) ·
[MX-012](../corpus/mx-012-licensing-and-reuse.md) ·
[scale gate](../license/scale-gate.md) ·
[HX-000 draft](../harms/hx-000-the-fourteen-structural-harms.md)

**Machine and comprehension** — [GM-11](../00-governance-map/machine-reading-contract.md) ·
[ST-14](st-14-machine-surfaces-and-json-schemas.md) ·
[RB-04](../rubrics/rb-04-reader-comprehension-rubric.md) ·
[ST-12](st-12-accessibility-implementation.md)

### Exit pair

1. **Judge a tier 1 claim.** Open [MX-003](../corpus/mx-003-privacy-notice.md) as
   someone who has never seen this corpus and run P1–P4. Only you can.
2. **Read the duty with no plain rendering.**
   [ML-2.3 §H.3(a)](../license/the-maher-license.md) — eight absolutes, one
   disjunctive, and no tier 1 page anywhere.

<!-- mx-pagestamp: ST-16 · v2026.10.1 · operative-form · tier 5 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; by this standard's own test the corpus has roughly one genuine tier 1 page -->
