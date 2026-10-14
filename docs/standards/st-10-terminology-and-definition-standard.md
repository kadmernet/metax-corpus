---
doc_id: ST-10
title_en: Terminology and Definition Standard
title_ar: معيار المصطلحات والتعريفات
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
domain_tags: [terminology, definitions, lexicon, one-term-one-meaning, standards]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. The standard's central rule — one term, one defining instrument — is breached by the corpus in at least four places named in §6.
route: /standards/st-10/
---

# ST-10 — Terminology and Definition Standard

> **Authority.** `operative-form`, tier 5. Governs how terms are defined across
> the corpus. The register of defined terms is
> [LEX-01](../lexicon/keyword-register.md); identifier grammar is
> [ST-01](st-01-identifier-and-url-grammar.md); front matter fields are
> [ST-02](st-02-front-matter-schema.md).

> **Disclosure first.** [LEX-01](../lexicon/keyword-register.md) holds **20 terms
> of a probable 100**, and holds **no Arabic entries** in a register whose
> authoritative language is Arabic. This standard therefore governs a register that
> covers a fifth of its subject in the wrong language. §6 names four terms the
> corpus defines in more than one place, which is the specific breach this standard
> exists to prevent.

---

## 1. Position

A governance corpus's terms do load-bearing work. "Governing", "record",
"designated", "notice", "condition", "covenant", "session" — each changes a
reader's obligations depending on which meaning applies. A corpus that lets a term
drift acquires a class of defect that no amount of careful drafting elsewhere can
compensate for, because the drift is **invisible within any single document**.

The standard's single rule, from which everything else follows:

> **One term, one meaning, one defining instrument.** Every other instrument
> *uses* the term and **links** to the definition; none redefines it.

### 1.1 Why local definitions are prohibited

A local definition — a term redefined inside one instrument "for the purposes of
this document" — is the most common and most respectable route to corpus-wide
incoherence. It reads as precision. It produces two meanings for one word, and a
reader who learned the term in one instrument carries the wrong meaning into the
other.

[MX-002 §2](../corpus/mx-002-terms-of-service.md) implements this rule
deliberately: it defines **nothing** locally, and every term in its table points
elsewhere. That is the pattern this standard generalises.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **defined term** | A word or phrase whose corpus meaning differs from, or is narrower than, ordinary usage |
| **defining instrument** | The single instrument that states a defined term's meaning |
| **use site** | Any other instrument that uses the term |
| **local definition** | A definition stated at a use site — **prohibited** (§1.1) |
| **confusable pair** | Two defined terms readers routinely conflate |
| **term of art imported** | A term borrowed from law or another field, whose imported meaning may not match |

### 2.1 What is not a defined term

Not every word needs defining, and over-definition is its own fault — a corpus that
defines "document" has spent a reader's attention for nothing. The test:

> A term requires definition only if a competent reader, using ordinary meaning,
> would reach a **different practical result** than the corpus intends.

"Governing" passes the test: ordinary usage would not tell a reader that a
`governing` instrument outranks an `operative-form` one. "Page" passes marginally:
[REG-02 §2](../registries/reg-02-page-registry.md) imposes five conditions
ordinary usage would not. "Document" fails and is not defined.

## 3. The rules

| # | Rule | Consequence of breach |
|---|---|---|
| **T1** | Each defined term has **exactly one** defining instrument | Two meanings; readers carry the wrong one |
| **T2** | Every use site **links** the term's first mention to the defining instrument | Reader cannot check the meaning — also [ST-08 §2.2](st-08-cross-reference-and-link-integrity.md) |
| **T3** | **No local definitions** (§1.1) | Silent divergence |
| **T4** | Every defined term is **registered** in [LEX-01](../lexicon/keyword-register.md) | Unregistered terms cannot be audited |
| **T5** | **Confusable pairs** are declared, with the distinction stated at both ends | Reader conflates them |
| **T6** | **Imported terms of art** are flagged, with the imported source and any divergence stated | Reader imports the wrong body of meaning |
| **T7** | A term's meaning changes only by **amendment with record**, never by re-use | Silent redefinition — worse than a silent edit |

### 3.1 T6 and the imported-legal-term problem

The corpus imports several terms from legal usage: **condition**, **covenant**,
**notice**, **cure**, **material**, **good faith**. Each carries a body of meaning
the estate has **not** adopted wholesale and cannot authoritatively interpret,
because there is no counsel
([REG-08](../registries/reg-08-role-and-authority-registry.md)).

So T6 requires each such term to state:

1. the field it is imported from;
2. the corpus meaning;
3. **whether the corpus meaning is narrower, wider, or uncertain** relative to the
   imported one.

For all six terms above, limb 3 currently reads **uncertain**, and that is the
honest entry. The [enforceability two-track table](../license/enforceability-two-track-table.md)
depends on the condition/covenant distinction holding its legal sense; whether it
does is the exposure named at
[REG-08 §4](../registries/reg-08-role-and-authority-registry.md).

### 3.2 T7 is stricter than the no-silent-edits rule

[Charter §0.8](../corpus/mx-000-charter.md) forbids silent edits to text. T7 forbids
something harder to detect: **a term's meaning shifting through accumulated use
without any single edit being wrong.** If "record" is used in three new instruments
in a slightly broader sense, no edit is silent and the definition has moved.

Detection requires comparing a term's use sites against its definition — check
**M3** in §4.2, unimplemented.

## 4. Mechanism

### 4.1 Introducing a term

```
does ordinary meaning give the intended result?   yes → do not define (§2.1)
is it already defined somewhere?                  yes → LINK, do not redefine (T3)
                                                  no  → choose the defining instrument:
                                                        the one whose SUBJECT owns it
register in LEX-01                                (T4)
is it imported from another field?                yes → flag with divergence (T6)
is it confusable with an existing term?           yes → declare the pair (T5)
```

The defining instrument is the one whose **subject** owns the term, not the first
one to use it. "Session" is defined by
[MX-022](../corpus/mx-022-identity-and-sessions.md), not by
[MX-003](../corpus/mx-003-privacy-notice.md), which uses it first in reading order.

### 4.2 The three checks

| # | Check | Detects |
|---|---|---|
| **M1** | Every LEX-01 term has exactly one defining instrument | T1 breach |
| **M2** | Every first use of a registered term at a use site is linked | T2 breach |
| **M3** | A term's use sites are consistent with its definition | **T7 drift** |

| Check | Specified | Implemented | Run |
|---|---|---|---|
| M1 | Yes | **No** | **No** |
| M2 | Yes | **No** | **No** |
| M3 | Yes | **No** — and **not mechanisable** | **No** |

M3 is the important row: drift detection requires **reading**, not matching. It
cannot be automated by string comparison, so it is the one check in this corpus
that a runner would not fix. It needs a reviewer, and there is one participant
([DEF-031](../00-governance-map/defect-register.md)).

## 5. Worked instance

**Following one term that is defined twice.**

Take **"designated"**. It appears as a required front matter field —
`designated: yes|no` ([ST-02](st-02-front-matter-schema.md)) — and it appears as a
licence concept in the [designation list](../license/designation-list.md), where
DL-2 records four rows added and two close calls excluded.

Are these the same term?

| Sense | Where | Meaning |
|---|---|---|
| **A — front matter** | [ST-02](st-02-front-matter-schema.md) | Whether this instrument is designated under the licence |
| **B — licence** | [designation list](../license/designation-list.md) | The act of the curator placing a work under ML-2.3's designation regime |

They are *related* and not *identical*: A is a **property of a document**, B is an
**act with criteria**. A reader who learns sense A from front matter and then reads
the designation list will assume the field records the outcome of the B process —
which it should, and nothing verifies that it does. There is no check that
`designated: yes` in front matter corresponds to a row in the designation list.

Apply the standard:

| Rule | Status |
|---|---|
| T1 one defining instrument | **Breached.** Two instruments state a meaning |
| T4 registered in LEX-01 | Registered once, in one sense |
| T5 confusable pair declared | **No** — and this is a confusable pair with itself |
| M1 check | Would catch it; unimplemented |

**The remedy shape** matters here and illustrates something the standard did not
anticipate. The right fix is *not* to pick one instrument and delete the other
definition. The two senses are both needed. The correct fix is to **split the term**:
`designated` (the act, licence) and `designation_recorded` (the document property,
front matter), with T5 declaring them a pair.

But renaming a front matter field breaks every instrument that carries it — roughly
eighty files — and [ST-02](st-02-front-matter-schema.md)'s field names are part of
a published schema that machine readers are invited to rely on
([GM-11](../00-governance-map/machine-reading-contract.md)).

So the estate faces the terminology equivalent of
[MX-004 §3.1](../corpus/mx-004-terms-of-top-levels.md)'s frozen-mistake problem:
**the immortality that protects readers also preserves an ambiguity.** The
available remedy is the weaker one — declare the confusable pair under T5, state
the distinction at both ends, and add the missing cross-check between the field and
the designation list. Filed rather than fixed silently.

## 6. Failure modes and the four known breaches

| # | Failure | Current state |
|---|---|---|
| F1 | **Two defining instruments** (T1) | **Four known**, below |
| F2 | **Unlinked first use** (T2) | Widespread; unaudited |
| F3 | **Local definition** (T3) | Guarded; [MX-002](../corpus/mx-002-terms-of-service.md) is the model |
| F4 | **Unregistered term** (T4) | **~80 terms unregistered** — LEX-01 holds 20 of ~100 |
| F5 | **Undeclared confusable pair** (T5) | LEX-01 declares 4; more exist |
| F6 | **Imported term unflagged** (T6) | Six legal imports, all `uncertain` (§3.1) |
| F7 | **Meaning drift** (T7) | **Undetectable** — M3 needs a reader (§4.2) |

### 6.1 The four T1 breaches

| Term | Sense A | Sense B | Remedy shape |
|---|---|---|---|
| **designated** | Front matter property ([ST-02](st-02-front-matter-schema.md)) | Licence act ([designation list](../license/designation-list.md)) | Split + T5 pair (§5) |
| **record** | Authority class, `authority: record` ([GM-01](../00-governance-map/precedence-and-conflict-rules.md)) | An entry in a register ([MX-013](../corpus/mx-013-records-and-versioning.md)) | T5 pair; both senses needed |
| **notice** | A communication starting a clock ([MX-006 §2](../corpus/mx-006-contact-and-correspondence.md)) | A reader-facing disclosure banner ([SITE-04](../site/demo-notice.md), "demo notice") | T5 pair; second sense should be renamed *disclosure* |
| **condition** | Licence provision terminating automatically ([§F.4](../license/the-maher-license.md)) | A prerequisite in a general sense (used throughout) | Flag under T6; the licence sense must always be qualified |

**"Notice" is the dangerous one.** One sense starts a 30- or 90-day cure clock;
the other is a banner at the top of a page. A reader who sees "demo notice" and
then reads that "the period runs from notice" has every reason to conflate them.
The remedy — rename the banner sense to *disclosure* — is cheap, affects few
files, and is owed.

## 7. Limits

1. **LEX-01 holds 20 of ~100 terms.** Four fifths of the corpus's defined
   vocabulary is unregistered, so T4 is breached at scale and M1 would have little
   to check.
2. **No Arabic entries** in LEX-01, while `prevailing_text: ar`. The authoritative
   vocabulary of the corpus does not exist
   ([MX-020](../corpus/mx-020-language-authority.md),
   [ST-11](st-11-arabic-authoring.md)). For a terminology standard this is not a
   backlog — a term's authoritative meaning is stated in a language the corpus has
   never written.
3. **M3 (drift) is not mechanisable** and requires a second reader (§4.2).
4. **Six imported legal terms all read `uncertain`** on divergence, because there
   is no counsel (§3.1).
5. **Two of the four T1 breaches cannot be cleanly fixed**, because the ambiguous
   names are embedded in a published schema or published routes (§5).
6. **The §2.1 test is judgement, not a rule.** Whether "ordinary meaning gives a
   different practical result" is itself a judgement by the party who chose the
   term.

## 8. Falsifier

> **IF FALSE.** This standard is falsified if:
>
> - **(a)** a defined term is shown to have two defining instruments beyond the
>   four in §6.1 — the estate expects this and lists four as a starting point, not
>   a census;
> - **(b)** a local definition is found at a use site (T3);
> - **(c)** a term is used in a sense inconsistent with its defining instrument
>   (T7 drift) — **the most valuable test and the only one requiring a reader**;
> - **(d)** an imported legal term is used without its T6 flag;
> - **(e)** a LEX-01 term is shown to be absent from every instrument — a
>   registered term nobody uses;
> - **(f)** `designated: yes` appears in front matter with no corresponding row in
>   the [designation list](../license/designation-list.md) — **this cross-check has
>   never been run** (§5).
>
> **(f) is runnable today** by a reader with a directory listing and one register,
> and the estate has not run it. **(c) is the test that matters most** and cannot
> be automated, which is why it has never been performed.

## 9. Obligation

**On an author:**
- Do not define a term that ordinary meaning already handles (§2.1).
- **Never** define locally; link instead (T3).
- Link the first use of every defined term (T2, [ST-08 §2.2](st-08-cross-reference-and-link-integrity.md)).
- Register every new defined term in [LEX-01](../lexicon/keyword-register.md) (T4).
- Flag imported terms with their divergence, including `uncertain` (T6).
- Declare confusable pairs at **both** ends (T5).
- Change a meaning only by amendment with record (T7).

**On the estate:**
- Register the ~80 missing terms (§7.1).
- Rename the banner sense of **notice** to *disclosure* (§6.1) — cheap and owed.
- Declare T5 pairs for `designated`, `record`, `notice`, `condition`.
- Run falsifier §8(f): reconcile front matter `designated` against the
  designation list.
- State that M3 drift detection requires a second reader and is therefore not
  performed (§4.2).

---

### Related

**The register governed** — [LEX-01](../lexicon/keyword-register.md) ·
[ST-11](st-11-arabic-authoring.md) ·
[MX-020](../corpus/mx-020-language-authority.md) ·
[GM-11](../00-governance-map/machine-reading-contract.md)

**Where terms are stated** — [ST-02](st-02-front-matter-schema.md) ·
[GM-01 precedence](../00-governance-map/precedence-and-conflict-rules.md) ·
[MX-013](../corpus/mx-013-records-and-versioning.md) ·
[MX-006](../corpus/mx-006-contact-and-correspondence.md)

**Imported legal terms** — [ML-2.3](../license/the-maher-license.md) ·
[enforceability two-track table](../license/enforceability-two-track-table.md) ·
[designation list](../license/designation-list.md) ·
[REG-08](../registries/reg-08-role-and-authority-registry.md)

**Checks and their absence** — [ST-08](st-08-cross-reference-and-link-integrity.md) ·
[ST-13](st-13-static-build-and-sentinel.md) ·
[DEF-001](../00-governance-map/defect-register.md) ·
[REG-07](../registries/reg-07-defect-classification-registry.md)

### Exit pair

1. **Run the cross-check.** Falsifier §8(f) — compare every `designated: yes` to
   the [designation list](../license/designation-list.md). Never done, needs no
   tools.
2. **See the dangerous pair.** [§6.1](#61-the-four-t1-breaches) — "notice" means
   both a cure-clock trigger and a page banner.

<!-- mx-pagestamp: ST-10 · v2026.10.1 · operative-form · tier 5 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; LEX-01 registers 20 of an estimated 100 defined terms -->
