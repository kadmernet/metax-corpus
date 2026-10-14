---
doc_id: ST-08
title_en: Cross-Reference and Link Integrity Standard
title_ar: معيار الإحالات وسلامة الروابط
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
domain_tags: [cross-reference, links, integrity, relative-paths, standards]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. The standard specifies checks that no runner performs.
route: /standards/st-08/
---

# ST-08 — Cross-Reference and Link Integrity Standard

> **Authority.** `operative-form`, tier 5. Binds the **form** of every reference
> in the corpus. Addresses are [SITE-03](../site/routing-law.md) (tier 7);
> identifiers are [ST-01](../standards/st-01-identifier-and-url-grammar.md);
> required page furniture is [SITE-02](../site/page-contract.md).

> **Disclosure first.** This standard defines five checks. **None runs**
> ([DEF-001](../00-governance-map/defect-register.md);
> [ST-13 SENTINEL](st-13-static-build-and-sentinel.md) is specified and idle). At
> least one known stale anchor is **knowingly retained** in the corpus (R-42), and
> the estate cannot state how many others exist. A link-integrity standard with no
> runner is class **DC-4 unenforced obligation** under
> [REG-07 §2.1](../registries/reg-07-defect-classification-registry.md).

---

## 1. Position

The corpus's central design claim is that **every identifier links to its defining
document**. That claim is what makes the estate navigable without search, what
makes [RB-04](../rubrics/rb-04-reader-comprehension-rubric.md)'s C2 answerable, and
what makes [SITE-02](../site/page-contract.md)'s related blocks meaningful.

It is also the claim most vulnerable to silent decay. Prose rots visibly; a broken
link rots invisibly to the author, who never clicks their own references. Link
integrity therefore belongs in the same category as accessibility
([ST-12](st-12-accessibility-implementation.md)): a class of fault **the author
cannot detect by rereading**.

### 1.1 Why this is a tier 5 standard and not a site-layer rule

An address's validity is [SITE-03](../site/routing-law.md), tier 7. A
*reference's* validity is a property of the **text** that makes it, and text
standards sit at tier 5. So a page may be correctly addressed and still violate
this standard by pointing at the wrong thing — and the ordering trap applies:
**ST-08 outranks SITE-01.**

## 2. Definitions

| Term | Meaning here |
|---|---|
| **reference** | Any link from one instrument to another, or to a section within one |
| **anchor reference** | A link to a specific section (`#...`) |
| **identifier reference** | A mention of a `doc_id` (e.g. `MX-013`) in prose |
| **stale anchor** | An anchor whose target heading no longer exists |
| **dangling reference** | A reference whose target document does not exist — class DC-1 |
| **orphan** | An instrument no other instrument links to |
| **asymmetric pair** | A links to B on a matter where B should link back and does not |

### 2.1 The four properties of a well-formed reference

1. **Relative.** Reference paths between instruments are **relative** (`../corpus/mx-013-records-and-versioning.md`), never absolute file paths and never bare URLs to the live site. Relative paths survive the estate ending
   ([MX-019 W5](../corpus/mx-019-sunset-and-wind-down.md)): a portable Markdown
   archive must be navigable with no host.
2. **Resolvable.** The target exists.
3. **Labelled.** The link text names the instrument or its subject — never "here",
   "this", or a bare URL. A reference must be readable as text
   ([ST-12](st-12-accessibility-implementation.md)).
4. **Load-bearing or omitted.** A reference exists because a reader needs it, not
   to demonstrate connectivity. Decorative cross-referencing inflates the related
   blocks and devalues real links.

### 2.2 Every identifier reference is a link

**Rule.** The first mention of any identifier in an instrument's body **must** be a
link to the defining document. Later mentions in the same instrument may be plain
text.

This is the mechanical expression of the corpus's design claim. An identifier
mentioned without a link asks the reader to find it, and finding it requires the
document index, which requires knowing the index exists.

## 3. The five checks

| # | Check | Detects | Runnable by |
|---|---|---|---|
| **L1** | **Resolvability** — every relative path resolves to an existing file | Dangling references (DC-1) | A script; also a reader, slowly |
| **L2** | **Anchor validity** — every `#anchor` matches a heading in the target | Stale anchors | A script |
| **L3** | **First-mention linkage** — every identifier's first body mention is linked | §2.2 breaches | A script with an identifier list |
| **L4** | **Orphan detection** — every instrument has ≥ 1 inbound reference | Unreachable instruments | A script over the whole tree |
| **L5** | **Symmetry** — declared reciprocal pairs both link | Asymmetric pairs | A script with a pair list |

### 3.1 Status of each check

| Check | Specified | Implemented | Ever run |
|---|---|---|---|
| L1 | Yes | **No** | **No** |
| L2 | Yes | **No** | **No** — one known breach retained (R-42) |
| L3 | Yes | **No** | **No** |
| L4 | Yes | **No** | **No** |
| L5 | Yes | **No** | **No** |

Five specified, zero implemented, zero run. Published in this state rather than
withheld until a runner exists, because the standard's absence was itself
producing breaches.

### 3.2 L5 and the declared pairs

Symmetry is **not** a general duty — requiring every link to be reciprocal would
produce a fully connected graph and destroy the signal. It applies only to
**declared reciprocal pairs**, where a relationship is meaningless in one
direction:

| Pair | Why reciprocal |
|---|---|
| Defect ↔ the instrument it is filed against | A reader of the instrument must learn of the defect |
| Superseding text ↔ superseded text | Both directions are needed to trace a version |
| Objection ↔ the instrument objected to | [ST-06](st-06-objections-standard.md) |
| Registry row ↔ the instrument registered | [REG-02](../registries/reg-02-page-registry.md) |
| Harm ↔ the instrument answering it | [HX-002](../harms/hx-002-harm-instrument-map.md) |

**The first row is the important one and is widely breached.** Defects are filed
in the [defect register](../00-governance-map/defect-register.md) naming an
instrument; the named instrument usually does **not** link back. So a reader of
[SITE-01](../site/route-manifest.md) is not told that
[DEF-032](../00-governance-map/defect-register.md) describes it as a plan dressed
as an inventory — they must read the register to find out. That is the same fault
[RB-03 §6.1](../rubrics/rb-03-instrument-quality-rubric.md) scored as a Q3 failure,
arriving from a second direction.

## 4. Mechanism

### 4.1 When an instrument moves

Instruments should not move ([ST-01 Rule 2](st-01-identifier-and-url-grammar.md)),
but a path can change while an identifier does not. Order of operations:

```
1. create the redirect record (SITE-03, append-only)
2. update every INBOUND reference          ← the step that is skipped
3. verify with L1 and L2
4. log in the changelog
```

Step 2 is where link integrity is lost, because it requires knowing every inbound
reference — which is L4's data, which does not exist. **In practice the estate
cannot perform step 2 reliably**, and this is the honest mechanism-level reason
stale anchors persist.

### 4.2 When a heading is renamed

Renaming a heading breaks every inbound anchor to it, silently. Therefore:

> **Rule.** A heading that is the target of a cross-corpus anchor must not be
> renamed without running L2. Since L2 does not run, **headings referenced from
> other instruments should not be renamed at all** on present capacity.

This is a genuine constraint on editing that follows from a missing tool, and it is
stated rather than left to be discovered.

### 4.3 Known-stale references are marked, never silently left

Where a reference is known broken and is retained deliberately, it must be marked
in the text as known-stale with a pointer to the ledger entry. **R-42 is retained
without such a mark**, which is a second, smaller breach on top of the first.

## 5. Worked instance

**Tracing one reference that cannot currently be validated.**

[ML-2.3](../license/the-maher-license.md) §A.10 incorporates
[HX-000](../harms/hx-000-the-fourteen-structural-harms.md) by reference. That
single reference does more work than any other in the corpus: it is what places
HX-000 at **tier 1a** in the
[precedence ladder](../00-governance-map/precedence-and-conflict-rules.md), above
the Charter.

Apply the checks:

| Check | Result |
|---|---|
| **L1** resolvability | **Passes in part.** A file exists at `docs/harms/hx-000-the-fourteen-structural-harms.md` |
| **L2** anchor validity | **Cannot be assessed** — §A.10 incorporates the document, not a section |
| **L3** first-mention linkage | Passes |
| **L4** orphan | Passes — heavily referenced |
| **L5** symmetry | **Fails** — HX-000's own text links to `../license/ml-2-2.md`, which **does not exist**, rather than to ML-2.3 |

So the corpus's most load-bearing reference points at a document that: is titled
"Fourteen" while the licence governs **twenty-five** harms; is an unfinished draft
ending at an append-point; and whose own obligation blocks reference a
**superseded and unrecoverable** licence version
([version history](../license/version-history.md)).

**What L1 got wrong, and why it matters for the standard's design.** L1 passed. A
file exists at the path, so resolvability is satisfied. But the reference is
substantively broken in three ways L1 cannot see, because **L1 tests existence and
not identity** — it cannot tell that the document found is not the document
incorporated.

That is a real limit of mechanical link checking and it points at a sixth check
the standard does not have: **L6 — target identity**, verifying that a referenced
document's `doc_id` and `version` match what the referring text claims to
incorporate. Had L6 existed, [DEF-021](../00-governance-map/defect-register.md)
would have been caught by machine on the day §A.10 was written instead of being
found by reading.

L6 is therefore added to §3 as specified-and-unimplemented, alongside the other
five, and this instrument records that it was discovered by writing the worked
instance rather than by designing the check set — which is the ordinary way such
gaps are found and an argument for always writing the worked instance.

### 5.1 L6 — target identity

| # | Check | Detects | Status |
|---|---|---|---|
| **L6** | Referenced document's `doc_id` / `version` match what the referring text claims | Wrong-target references; incorporation of a superseded or mis-titled document | **Specified v2026.10.1; not implemented** |

## 6. Failure modes

| # | Failure | Mechanism | Current state |
|---|---|---|---|
| F1 | **Stale anchor** | Heading renamed | **Occurring** — R-42, retained and unmarked (§4.3) |
| F2 | **Dangling reference** | Target never written | **Occurring** — `ml-2-2.md` from HX-000; ~6 DC-1 defects |
| F3 | **Inbound references unknown** | No L4 data | **Actual** — makes §4.1 step 2 unperformable |
| F4 | **Asymmetric defect linkage** | Register names instrument; instrument silent | **Widespread** — §3.2 |
| F5 | **Decorative cross-referencing** | Links added to look connected | Guarded by §2.1(4); unaudited |
| F6 | **Absolute or live-URL links** | Convenience | Would break the portable archive ([MX-019 W5](../corpus/mx-019-sunset-and-wind-down.md)) |
| F7 | **Existence mistaken for identity** | L1 passes on a wrong target | **Actual** — §5; motivated L6 |

## 7. Limits

1. **No check runs.** Six specified, zero implemented. Everything this standard
   claims about corpus integrity is **E0** under
   [ST-07](st-07-evidence-and-verify.md).
2. **The estate cannot enumerate inbound references** (F3), so it cannot safely
   move a file or rename a referenced heading — §4.2's rule is a prohibition
   standing in for a tool.
3. **One known stale anchor is retained and unmarked**, breaching §4.3 as well as
   L2.
4. **L5 asymmetry is widespread** and each instance is a small Q3 disclosure
   failure under [RB-03](../rubrics/rb-03-instrument-quality-rubric.md).
5. **L6 was missing from the design** until §5 exposed it. A check set that gained
   a member by writing one example is probably still incomplete.
6. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** This standard is falsified if:
>
> - **(a)** any relative path in the corpus fails to resolve — **a reader can test
>   this on any page by following every link**, and L1 has never been run, so the
>   estate cannot predict the result;
> - **(b)** any anchor points to a heading that does not exist (at least one does);
> - **(c)** an identifier's first body mention is unlinked;
> - **(d)** an instrument exists with zero inbound references;
> - **(e)** a declared reciprocal pair (§3.2) links in one direction only — the
>   estate expects **many** hits;
> - **(f)** a reference incorporates a document whose `doc_id` or version differs
>   from what the referring text claims (L6) — **this fires now**, on
>   [ML-2.3 §A.10](../license/the-maher-license.md).
>
> **(f) fires on the corpus's most important reference.** The estate states that
> plainly rather than scoping the falsifier to avoid it.

## 9. Obligation

**On an author:**
- Use **relative paths** between instruments, always (§2.1(1)).
- Link the **first body mention** of every identifier (§2.2).
- Label links with the instrument or subject; never "here" (§2.1(3)).
- Omit decorative references (§2.1(4)).
- Do not rename a cross-referenced heading while L2 is unavailable (§4.2).
- Mark a knowingly retained broken reference as known-stale (§4.3) — **owed for
  R-42**.
- When filing a defect, add the reciprocal link **in the instrument** as well as
  the register (§3.2, F4).

**On the estate:**
- Implement L1 and L2 first; they are the cheapest and catch the most
  ([ST-13](st-13-static-build-and-sentinel.md)).
- Implement **L6**; it would have caught [DEF-021](../00-governance-map/defect-register.md)
  mechanically (§5).
- Build the L4 inbound index; without it §4.1 step 2 cannot be performed.
- Never publish an absolute or live-site URL where a relative path will serve —
  the portable archive depends on it ([MX-019](../corpus/mx-019-sunset-and-wind-down.md)).

---

### Related

**Addressing and identifiers** — [ST-01](st-01-identifier-and-url-grammar.md) ·
[SITE-03](../site/routing-law.md) · [SITE-01](../site/route-manifest.md) ·
[ST-02](st-02-front-matter-schema.md)

**Checks and their absence** — [ST-13](st-13-static-build-and-sentinel.md) ·
[DEF-001](../00-governance-map/defect-register.md) ·
[GM-08 verification log](../00-governance-map/verification-log.md) ·
[REG-07](../registries/reg-07-defect-classification-registry.md)

**The reference that fails L6** — [ML-2.3](../license/the-maher-license.md) ·
[HX-000 draft](../harms/hx-000-the-fourteen-structural-harms.md) ·
[version history](../license/version-history.md) ·
[precedence](../00-governance-map/precedence-and-conflict-rules.md)

**Why links must stay relative** — [MX-019](../corpus/mx-019-sunset-and-wind-down.md) ·
[MX-018](../corpus/mx-018-third-party-dependencies.md) ·
[GM-12 archive register](../00-governance-map/archive-register.md) ·
[SITE-02](../site/page-contract.md)

### Exit pair

1. **Run L1 by hand on one page.** Follow every link on this page. L1 has never
   been run; you would be the first.
2. **See L6 fire.** [ML-2.3 §A.10](../license/the-maher-license.md) incorporates a
   document titled "Fourteen" into a licence governing twenty-five harms.

<!-- mx-pagestamp: ST-08 · v2026.10.1 · operative-form · tier 5 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the published site is a demonstration; none of the six checks specified here is implemented -->
