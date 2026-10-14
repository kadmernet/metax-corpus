---
doc_id: MX-018
title_en: Third-Party Dependencies and Vendors
title_ar: التبعيات والجهات الخارجية
family: corpus
version: v2026.10.1
status: published
authority: governing
prevailing_text: ar
audience_tier: 2
depth: meta
evidence_class: semi-durable
review_interval_months: 6
curator: Maher
license: ML-2.3
designated: yes
last_reviewed: 2026-09-16
domain_tags: [dependencies, vendors, supply-chain, exit, lock-in]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000 — itself an undeclared dependency of the estate, addressed in §6.
provenance_of_purpose: Cited by MX-024 and ST-22 since inception; absent until v2026.10.1, during which period no dependency inventory existed.
route: /dependencies/
---

# MX-018 — Third-Party Dependencies and Vendors

> **Authority.** `governing`, tier 3. Platform tiers are
> [MX-024](mx-024-infrastructure-and-migration.md) and
> [ST-22](../standards/st-22-platform-and-persistence.md); asset provenance is
> [REG-04](../registries/reg-04-media-registry.md); supply-chain threats are
> [MX-011 T3](mx-011-security-and-disclosure.md).

> **Disclosure first.** The estate depends on parties it has no contract with, no
> leverage over, and in two cases **no archived permission from**
> ([REG-04 §5.1](../registries/reg-04-media-registry.md)). The largest dependency
> is the one this instrument was written by: an AI system whose withdrawal would
> stop the corpus's growth entirely. That dependency has no exit plan and is
> addressed in [§6](#6-worked-instance) rather than omitted because it is
> awkward.

---

## 1. Position

A dependency register is not a list of tools. It is a list of **parties who can
change the estate's behaviour without the estate's consent**.

That framing changes what belongs on it. A text editor is not a dependency; a
remotely served font is, because the font provider's decision to move a URL
changes what a reader's browser does. The test used throughout this instrument:

> **Can this party, acting unilaterally, alter what a reader of the estate
> experiences, or prevent the estate from publishing?**

If yes, it is a dependency and it is enumerated in §3. If no, it is a tool and it
is out of scope.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **dependency** | A party satisfying the §1 test |
| **hard dependency** | Its withdrawal stops publication or breaks published pages |
| **soft dependency** | Its withdrawal degrades the estate without stopping it |
| **lock-in** | The cost of substituting the dependency, in time and lost content |
| **exit plan** | A written, dated route to substitution |
| **undeclared dependency** | One the estate relies on and has not enumerated |

### 2.1 Four properties per dependency

Each row in §3 records:

1. **What it does** for the estate.
2. **Hard or soft.**
3. **Lock-in** — what substitution would cost.
4. **Exit plan** — present, absent, or **impossible**.

Property 4 is where dependency registers usually go quiet. "Exit plan: absent" is
an admission; "exit plan: impossible" is a much larger one, and the estate has one
of those.

### 2.2 Contract is not the test

The estate holds **no negotiated contract with any dependency**. Every
relationship is a standard-terms arrangement the estate accepted without
modification, and several are free tiers with no service commitment at all.

This means the estate's protection against a dependency's unilateral change is
**zero across the board**. Recording "no contract" in nine rows would be repetitive;
it is stated once, here, and applies to every row in §3.

## 3. The dependency register

| # | Dependency | What it does | Hard/Soft | Lock-in | Exit plan |
|---|---|---|---|---|---|
| D1 | **Git hosting / repository** | Holds the canonical text and the history on which "no silent edits" rests | **Hard** | Low — git is distributable; the history can be cloned | **Absent** but cheap: a mirror. See [MX-011 §3.3](mx-011-security-and-disclosure.md) |
| D2 | **Static hosting / CDN** | Serves published pages; determines what is logged | **Hard** | Low — static files move easily | **Absent**; migration path sketched in [MX-024](mx-024-infrastructure-and-migration.md) |
| D3 | **Domain registrar / DNS** | Controls whether published routes resolve at all | **Hard** | **High** — a lost domain breaks every published route permanently, defeating [SITE-03](../site/routing-law.md) | **Absent.** The most under-considered row |
| D4 | **Web font provider** (`FNT-001`) | Typography; possibly a third-party request per reader | **Soft** | Low — self-host or substitute | **Absent**; licence terms **unarchived** ([REG-04](../registries/reg-04-media-registry.md)) |
| D5 | **AI authoring system** | Drafts essentially all prose in the corpus | **Hard** | **Very high** — see §6 | **Impossible** on current capacity |
| D6 | **Databases (six)** | Storage tiers under [MX-024](mx-024-infrastructure-and-migration.md); 80% tripwire | Soft *(currently)* | Moderate — schema is the estate's; rows are few | Partial — VPS path named, undated |
| D7 | **Payment processor** | Would handle payment under [ST-20](../standards/st-20-payment-integration.md) | n/a — **inactive** | n/a | n/a; [MX-021](mx-021-payments-and-commerce.md) path unbuilt |
| D8 | **Counsel** | Would set `counsel_reviewed` and validate the two-track split | **Hard for a claim class**, not for publication | — | **Vacant, not a dependency yet** — [REG-08](../registries/reg-08-role-and-authority-registry.md) |

### 3.1 Notes

- **D3 is the estate's most serious unmanaged dependency** after D5. Every
  permanence commitment in [ST-01](../standards/st-01-identifier-and-url-grammar.md)
  and [SITE-03](../site/routing-law.md) — immortal identifiers, append-only
  redirects, routes that resolve forever — is conditional on continuing control of
  one domain name, held on a renewable registration with no succession
  arrangement. [MX-015](mx-015-succession-and-continuity.md) does not name who
  renews it.
- **D8 is listed to be explicit that it is not yet a dependency.** The estate does
  not depend on counsel; it *lacks* counsel. The distinction matters because a
  missing capability and a risky dependency call for different remedies.
- **D7 is listed as inactive** rather than omitted, so that activating payments is
  visibly the addition of a dependency rather than a feature.

## 4. Mechanism

### 4.1 Adding a dependency

```
proposed dependency
  → apply the §1 test                         fails → it is a tool, not recorded
  → hard or soft?
  → state lock-in cost
  → state exit plan (present / absent / impossible)
  → if HARD and exit plan IMPOSSIBLE → record as a launch-blocking risk
  → enumerate in §3 BEFORE first use
```

Enumeration precedes use. A dependency adopted first and recorded later is an
**undeclared dependency**, which is the condition the estate was in for its entire
prior life — recorded in `provenance_of_purpose`.

### 4.2 The no-silent-adoption rule

Adopting a dependency is a governance act, not a technical convenience. It is
logged in the [changelog](../00-governance-map/changelog.md) like any other change,
because a reader's exposure changes when the set of parties who can affect them
changes.

### 4.3 Review trigger

Dependencies are reviewed on **change of terms or capability**, not only at the
6-month interval. A provider's unilateral change of terms is the event this
instrument exists to catch, and it does not arrive on a schedule.

## 5. Failure modes

| # | Failure | Mechanism | Current state |
|---|---|---|---|
| F1 | **Undeclared dependency** | Adopted for convenience, never enumerated | **Was total until this version**; D5 was undeclared for the estate's whole life |
| F2 | **Domain loss** | Lapsed renewal, transfer dispute, registrar action | **Unmitigated** — D3, no succession arrangement |
| F3 | **Silent terms change** | Provider changes terms; estate does not notice | **No watcher** |
| F4 | **Third-party request per reader** | Remote asset discloses reader requests | **Live** — D4 unverified ([MX-003 §3.3](mx-003-privacy-notice.md)) |
| F5 | **Exit plan absent where lock-in is high** | Nobody wrote one | **Actual** — D3 high lock-in, no plan; D5 impossible |
| F6 | **Dependency mistaken for capability** | Estate believes it can author; in fact D5 authors | **Addressed in §6** |
| F7 | **History rewritable** | D1 offers no external witness | **Unmitigated** — [MX-011 T8](mx-011-security-and-disclosure.md) |

## 6. Worked instance

**D5 traced to its uncomfortable conclusion.**

Every substantive document in this corpus — including this sentence — was drafted
by an AI system operating under [AG-000](../agents/ag-000-agent-constitution.md).
The estate discloses this per [MX-007](mx-007-ai-use-and-disclosure.md) and in
every instrument's `authorship_note`. What it has **not** previously done is
classify it as a dependency and cost the exit.

Apply §2.1:

| Property | Answer |
|---|---|
| **What it does** | Drafts the prose. Not "assists with" — drafts |
| **Hard or soft** | **Hard.** Without it, corpus growth stops |
| **Lock-in** | **Very high.** The corpus's voice, structure, cross-reference density, and eight-part discipline are all artefacts of this authoring mode |
| **Exit plan** | **Impossible** on current capacity |

Why *impossible* and not merely *absent*: an exit plan requires a substitute. The
substitute for D5 is a human author with the estate's subject knowledge and the
time to write ~80 instruments at ~1200 words each in the eight-part form. The
estate has **one participant**
([DEF-031](../00-governance-map/defect-register.md)) who is the curator, and the
curator's capacity is the binding constraint that produced D5 in the first place.
So the exit from D5 requires the same acquisition — a second person — that
[MX-005 Annex A.1](mx-005-scope-and-boundaries.md) identifies as the estate's
core missing thing.

**The sharper problem: F6.** A dependency this deep is easy to mistake for a
capability. [MX-005 §2](mx-005-scope-and-boundaries.md) states that a subject is
in scope only if it "can be discharged by publishing a checkable text," and treats
authorship as the estate's **sole capability**. That is now visibly wrong, or at
least mis-stated: authorship is not a capability the estate holds, it is a service
the estate **receives from D5**. The scope instrument's capability condition should
read *dischargeable by a text the estate can cause to be written*, which is a
weaker and truer claim.

This is a substantive inconsistency between two governing instruments, discovered
by writing this one. Under
[REG-07 §2.1](../registries/reg-07-defect-classification-registry.md) it is class
**DC-3 overclaim** — MX-005 asserts a capability the estate does not independently
hold — at severity **S2**, because a reader relying on MX-005's scope reasoning is
relying on a mis-stated premise. It is filed rather than fixed by a quiet edit to
MX-005, per [Charter §0.8](mx-000-charter.md).

**What the estate does not claim.** It does not claim the corpus is worse for
being AI-drafted, nor better. It claims only that the drafting arrangement is a
dependency with no exit, that it was undeclared until now, and that one governing
instrument mis-describes it.

## 7. Limits

1. **No contract with any dependency** (§2.2). The estate's exposure to unilateral
   change is complete.
2. **D3 (domain) has high lock-in and no plan**, and every permanence commitment in
   the corpus is conditional on it.
3. **D5 has no possible exit** on current capacity (§6).
4. **Two dependencies are unverified**: D4's licence terms are unarchived and its
   self-hosting is unconfirmed.
5. **No watcher for terms changes** (F3). §4.3's trigger relies on the curator
   noticing an email.
6. **This register was written by D5.** A dependency assessing itself is a conflict
   under [MX-017 C1](mx-017-conflicts-of-interest.md); the direction of interest
   (S2) is toward understating D5's severity, and a reader should discount §6
   accordingly.
7. **No Arabic text**, while `prevailing_text: ar`.

## 8. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** the estate relies on a party satisfying §1's test that is absent from
>   §3 — the register's central claim is completeness, and it was **totally
>   incomplete** until this version;
> - **(b)** any dependency is shown to be governed by a negotiated contract,
>   contrary to §2.2;
> - **(c)** a reader's browser is shown to contact a domain not implied by §3 —
>   checkable by any reader with developer tools;
> - **(d)** a dependency was adopted without a changelog entry (§4.2);
> - **(e)** §6's classification of D5 as `exit: impossible` is shown to be wrong by
>   exhibiting a workable substitute — the estate would welcome this.
>
> **(c) is the reader-runnable test** and overlaps
> [MX-003 §10(e)](mx-003-privacy-notice.md). **(a) is the one the estate expects to
> fire**, because a register written in one sitting by the party that benefits from
> it being short is unlikely to be complete.

## 9. Obligation

**On the estate:**
- Enumerate a dependency **before** first use (§4.1).
- Log every adoption in the [changelog](../00-governance-map/changelog.md) (§4.2).
- State the exit plan honestly, including `impossible` (§2.1).
- Write an exit plan for **D3** — the domain underwrites every permanence promise
  in the corpus and has none.
- Mirror the repository (D1), which also mitigates
  [MX-011 T8](mx-011-security-and-disclosure.md).
- Confirm D4 is self-hosted and archive its terms
  ([REG-04](../registries/reg-04-media-registry.md)).
- File the MX-005 capability-overclaim defect found in §6 rather than editing
  MX-005 silently ([Charter §0.8](mx-000-charter.md)).
- Review on terms change, not only at the interval (§4.3).

**On a reader:**
- Run §8(c) yourself.
- Discount §6 in the direction §7.6 states.

---

### Related

**Platform and storage** — [MX-024](mx-024-infrastructure-and-migration.md) ·
[ST-22](../standards/st-22-platform-and-persistence.md) ·
[REG-06](../registries/reg-06-dataset-registry.md) ·
[ST-21 performance budgets](../standards/st-21-performance-budgets.md)

**Supply chain and integrity** — [MX-011](mx-011-security-and-disclosure.md) ·
[REG-04](../registries/reg-04-media-registry.md) ·
[MX-003](mx-003-privacy-notice.md) ·
[GM-12 archive register](../00-governance-map/archive-register.md)

**Permanence that depends on D3** — [ST-01](../standards/st-01-identifier-and-url-grammar.md) ·
[SITE-03](../site/routing-law.md) · [SITE-01](../site/route-manifest.md) ·
[MX-015](mx-015-succession-and-continuity.md)

**The D5 problem** — [MX-007](mx-007-ai-use-and-disclosure.md) ·
[AG-000](../agents/ag-000-agent-constitution.md) ·
[MX-005](mx-005-scope-and-boundaries.md) ·
[MX-017](mx-017-conflicts-of-interest.md)

### Exit pair

1. **Write the domain exit plan.** D3 has high lock-in, no plan, and silently
   underwrites every permanence commitment in the corpus.
2. **Read the dependency that wrote this.** [§6](#6-worked-instance) — including
   the governing-instrument inconsistency it exposed in
   [MX-005](mx-005-scope-and-boundaries.md).

<!-- mx-pagestamp: MX-018 · v2026.10.1 · governing · tier 3 · reviewed 2026-09-16 · next review 2027-03-16 -->
<!-- mx-demo: the live site is a demonstration; no dependency is governed by a negotiated contract -->
