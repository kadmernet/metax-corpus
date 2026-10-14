---
doc_id: MX-019
title_en: Sunset and Wind-Down
title_ar: الإيقاف والتصفية
family: corpus
version: v2026.10.1
status: published
authority: governing
prevailing_text: ar
audience_tier: 2
depth: macro
evidence_class: durable
review_interval_months: 12
curator: Maher
license: ML-2.3
designated: yes
last_reviewed: 2026-09-16
domain_tags: [sunset, wind-down, decommissioning, permanence, ending]
hreflang: [en, ar]
authorship_note: Drafted by an AI system under AG-000. No wind-down provision here has ever been tested, and by construction it can be tested only once.
provenance_of_purpose: Implied by MX-013's permanence rules and MX-015's succession triggers, neither of which states what happens if succession fails; absent until v2026.10.1.
route: /sunset/
---

# MX-019 — Sunset and Wind-Down

> **Authority.** `governing`, tier 3. Complements
> [MX-015 succession and continuity](mx-015-succession-and-continuity.md), which
> covers handover. This instrument covers the case MX-015 does not: **succession
> fails and the estate ends.**

> **Disclosure first.** [MX-015](mx-015-succession-and-continuity.md) names four
> roles and **three are unfilled**; the Successor is one of them
> ([REG-08](../registries/reg-08-role-and-authority-registry.md)). So the branch
> this instrument governs — *nobody takes over* — is not the unlikely tail. On
> present facts it is **the default outcome**, and every commitment below is one
> the estate cannot currently keep because keeping it requires someone to be there.

---

## 1. Position

The corpus makes permanence promises throughout. Identifiers are immortal
([ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md)); routes resolve
forever or redirect ([SITE-03](../site/routing-law.md)); records are append-only
([MX-013](mx-013-records-and-versioning.md)); withdrawn duties are retained
([GM-12](../00-governance-map/archive-register.md)).

Every one of those promises is **unbounded in time** and made by an estate with a
**bounded** life. That mismatch has to be addressed somewhere, and addressing it
has exactly two honest resolutions:

- **Narrow the promises** to the estate's actual expected life — which destroys
  their value, because a redirect promised "until we stop" is not a permanence
  guarantee.
- **State what happens at the end**, so a reader knows which promises survive the
  estate and which do not.

This instrument takes the second. Its most important output is [§5](#5-what-survives-and-what-does-not),
which sorts every permanence promise into *survives* and *dies with the estate*.
Most die.

## 2. Definitions

| Term | Meaning here |
|---|---|
| **sunset** | A planned, announced ending with a date |
| **abandonment** | An unplanned ending: publication simply stops |
| **wind-down** | The acts owed between a sunset decision and the final state |
| **final state** | What remains reachable after wind-down completes |
| **orphaning** | The estate ends with no wind-down performed at all |

### 2.1 Three endings, not one

| Ending | Trigger | Wind-down performed? | Likelihood on present facts |
|---|---|---|---|
| **E1 Sunset** | Curator decides to stop | Yes, per §4 | Possible |
| **E2 Succession failure** | [MX-015](mx-015-succession-and-continuity.md) trigger fires, no successor accepts | Partial at best | **Most likely** |
| **E3 Orphaning** | Curator becomes unavailable with no warning | **No** | Substantial |

E3 is the case where nothing in this document happens. A wind-down policy that
only operates when someone is available to operate it does not cover the ending it
most needs to cover, and §6 works through exactly that.

### 2.2 Sunset is not deletion

Sunset means the estate stops **changing**. It does not mean the corpus is
removed. The distinction is the whole design: a frozen corpus that still resolves
is a far better outcome for a reader who relied on it than a deleted one, and it
is also cheaper to sustain.

## 3. The wind-down obligations

Owed on E1, and to the extent possible on E2.

| # | Obligation | Why |
|---|---|---|
| W1 | **Announce** the sunset, with a date, in the [changelog](../00-governance-map/changelog.md) and on the root page | A reader relying on a live corpus must learn it is ceasing |
| W2 | **Freeze and stamp** every instrument: `status: sunset`, with the sunset date | A reader arriving later must not mistake frozen text for maintained text |
| W3 | **Close or declare** every open item: defects, blockers, `RAT-` questions, verification items. `declared-permanent` where no remedy will come | Leaving items `open` in a dead corpus falsely implies work continues |
| W4 | **Publish the final census** — what was written, what never was | [REG-02](../registries/reg-02-page-registry.md); the corpus's last honest act |
| W5 | **Release the archive** in a portable form: plain Markdown, no build step, no platform dependency | Survives [MX-018](mx-018-third-party-dependencies.md) D1, D2, D5 |
| W6 | **Address the licence**: state whether [ML-2.3](../license/the-maher-license.md) continues to govern the corpus after sunset, and who, if anyone, may enforce it | Otherwise licensees are bound by terms with no counterparty |
| W7 | **Fund or transfer the domain (D3)**, or state plainly that routes will die | The only way any route survives — [MX-018 D3](mx-018-third-party-dependencies.md) |
| W8 | **Withdraw unmet promises explicitly** into [GM-12 Class D](../00-governance-map/archive-register.md) | Class D is currently **empty**; at sunset it should be the largest class in the estate |

### 3.1 W6 is harder than it looks

[ML-2.3](../license/the-maher-license.md) grants rights subject to conditions and
covenants, with cure periods running from notice. After sunset there is no one to
give notice ([MX-006 §5](mx-006-contact-and-correspondence.md) already shows notice
is barely servable **now**), no one to accept a cure, and no one to enforce a
termination.

The practical effect: at sunset the licence's **nineteen curable covenants become
unenforceable in fact**, while the **four automatic conditions and eight
absolutes** continue to operate as self-executing terms. So sunset silently
converts the licence from a twenty-three-provision instrument into a
twelve-provision one.

The estate has **not decided** whether to (a) declare that consequence expressly,
(b) grant a broader post-sunset licence so the residue is coherent, or (c) name a
steward who may enforce. This is filed as an open ratification question, and it
requires the Ratifying Authority that is also vacant.

### 3.2 W8 and the empty Class D

[GM-12](../00-governance-map/archive-register.md) defines Class D as **withdrawn
duties** and it is empty. [REG-07 §3.2](../registries/reg-07-defect-classification-registry.md)
already notes this is suspicious given the estate's history.

At sunset, W8 forces the issue: every duty the estate specified and never
discharged — independent appeal review, harm review, ratification, Arabic
publication, SENTINEL checks — must be written into Class D as withdrawn. That is
an unflattering list and it is the correct final record, because the alternative
leaves those duties reading as live in a corpus that will never perform them.

## 4. Mechanism

### 4.1 Sunset sequence (E1)

```
decision               →  W1 announce, with a date not less than 90 days out
during the 90 days     →  W3 close or declare; W4 census; W8 Class D
                          W6 licence decision; W7 domain decision
at the date            →  W2 freeze and stamp every instrument
after the date         →  W5 archive released; no further changes except
                          corrections of fact, each logged
final state            →  frozen corpus, resolving routes (if W7 funded),
                          portable archive, Class D complete
```

The 90-day minimum exists so W3 and W6 have time to be done properly rather than
declared in a rush.

### 4.2 Degradation on E2

On succession failure the curator may be present but unwilling, or present and
constrained. The obligations degrade in a stated order — **the last to be dropped
is the most valuable to a reader**:

| Priority | Obligation | Rationale |
|---|---|---|
| 1 (never dropped) | **W5 portable archive** | Survives every dependency; one command |
| 2 | **W2 freeze and stamp** | Prevents frozen text being read as maintained |
| 3 | **W1 announce** | Cheap, high value |
| 4 | **W7 domain** | Determines whether any route survives |
| 5 | **W4 census** | Mostly already written in [REG-02](../registries/reg-02-page-registry.md) |
| 6 | **W8 Class D** | Laborious |
| 7 | **W3 close or declare** | Laborious |
| 8 (first dropped) | **W6 licence decision** | Requires a vacant role anyway (§3.1) |

Ordering the degradation in advance is the only thing this instrument can usefully
do about E2, because at the time of an E2 ending nobody will be in a position to
weigh priorities calmly.

### 4.3 No provision operates on E3

Stated flatly because the alternative is a policy that implies coverage it does
not have. On orphaning: hosting lapses when unpaid, the domain lapses at its
renewal date, the repository persists only if the host keeps it, and **no
instrument is stamped, no duty is withdrawn, and no archive is released.**

## 5. What survives and what does not

The operative sort. "Survives" means: remains true and useful to a reader after
the estate has no participants.

| Promise | Source | Survives? | Why |
|---|---|---|---|
| Identifier immortality | [ST-01 Rule 2](../standards/st-01-identifier-and-url-grammar.md) | **Yes** | A number in a frozen text stays unreused because nothing reassigns it |
| Text of every instrument | corpus | **Yes, if W5 done** | Portable Markdown needs no platform |
| Append-only history | [MX-013](mx-013-records-and-versioning.md) | **Yes, if W5 done** | The record stops growing; it does not become false |
| Falsifiers remain runnable | [ST-04](../standards/st-04-falsifiability-and-claim-cards.md) | **Mostly yes** | Most are reader-runnable against the text itself |
| Disclosure of defects | defect register | **Yes** | Frozen disclosure is still disclosure |
| **Routes resolve** | [SITE-03](../site/routing-law.md) | **No, unless W7 funded** | Depends on D3 |
| **Redirects honoured** | [SITE-03](../site/routing-law.md) | **No, same reason** | — |
| **Corrections published** | [Charter §0.8](mx-000-charter.md) | **No** | Requires a publisher |
| **Review intervals honoured** | [ST-05](../standards/st-05-decay-and-review-intervals.md) | **No** | Every instrument becomes stale on a stated schedule |
| **Reports filed** | [MX-006 §4.2](mx-006-contact-and-correspondence.md) | **No** | Requires a recipient |
| **Appeals available** | [MX-016](mx-016-appeals-and-due-process.md) | **No** — already unavailable | Stage 2 vacant now |
| **Nineteen curable covenants** | [ML-2.3 §F.4](../license/the-maher-license.md) | **No** | No one to serve or accept notice (§3.1) |
| Four conditions, eight absolutes | [ML-2.3 §H.3(a)](../license/the-maher-license.md) | **Yes** | Self-executing |

**Eight promises die, five survive**, and the five that survive are all properties
of *text*, while the eight that die are all properties of *process*. That is the
same division that runs through this whole estate — the documents outlive the
institution because the institution was never built.

## 6. Worked instance

**E3 walked through: the estate is orphaned tomorrow.**

No announcement, no freeze, no archive release. Trace what a reader finds at
successive intervals:

| When | What a reader sees | Is it misleading? |
|---|---|---|
| **Week 1** | A live corpus. Version stamps read v2026.10.1; `status: published`; review dates in the future | No — accurate |
| **Month 4** | Identical. But three `perishable` instruments ([MX-003](mx-003-privacy-notice.md), [MX-006](mx-006-contact-and-correspondence.md), [REG-02](../registries/reg-02-page-registry.md)) have passed their review date | **Yes, mildly** — a reader cannot tell a missed review from a confirmed one |
| **Month 13** | Identical. Every `durable` instrument is past review. [REG-03](../registries/reg-03-book-registry.md)'s `BK-03` announcement clock has expired with no defect filed | **Yes** — the estate's own automatic trigger failed silently, which is the exact failure §3.2 of REG-03 was written to prevent |
| **Renewal date** | **Every route 404s.** 321 addresses die at once | The permanence promise breaks completely |
| **After** | Repository may persist, unfindable without the domain | The corpus survives as text and is unreachable in practice |

Two lessons the estate did not expect when it began drafting this.

**First: stale review dates are the earliest visible symptom of death, and the
corpus has no way to show them.** A reader at month 13 sees `last_reviewed:
2026-09-16` and `review_interval_months: 12` and must do the arithmetic
themselves. Nothing on the page says *overdue*. [ST-05](../standards/st-05-decay-and-review-intervals.md)
sets intervals and [ST-13](../standards/st-13-static-build-and-sentinel.md) would
flag breaches — and **SENTINEL does not run**
([DEF-001](../00-governance-map/defect-register.md)). So the estate's freshness
guarantee is unobservable at exactly the moment it starts to fail.

That is a live defect **now**, not only at sunset, and it is cheap to mitigate
without any runner: print the **next review date** in the page stamp, which most
instruments in this corpus already do. A reader can then compare it to today's
date with no tooling. This instrument therefore makes a small, concrete
recommendation rather than a governance one, and it is the most useful thing on
this page.

**Second: W7 is the binary.** Everything else in wind-down is a matter of degree.
The domain is all-or-nothing — one unpaid renewal converts a corpus with 321
permanent addresses into an unreachable archive, and no other single act has that
leverage. [MX-018 D3](mx-018-third-party-dependencies.md) records that no plan
exists.

## 7. Failure modes

| # | Failure | Current state |
|---|---|---|
| F1 | **Orphaning** — E3, no provision operates | **Substantial likelihood**; §4.3 |
| F2 | **Frozen text read as maintained** | **Live now** — no overdue signal (§6) |
| F3 | **Class D never populated** | **Actual** — empty today; W8 forces it only at sunset |
| F4 | **Licence residue undecided** | **Actual** — §3.1, needs a vacant role |
| F5 | **Archive never released** | W5 is priority 1 and has **never been performed** |
| F6 | **Domain lapse** | **Unmitigated** — §6 |
| F7 | **Wind-down policy itself untestable** | By construction: testable once |

## 8. Limits

1. **This instrument is untestable in advance** and operates exactly once.
2. **It cannot cover E3**, the ending it most needs to cover (§4.3).
3. **W6 requires the vacant Ratifying Authority** (§3.1).
4. **W5 has never been performed**, though it is priority 1 and is a single act.
   An untested priority-1 obligation is a claim, not a plan.
5. **The 90-day minimum in §4.1 is asserted**, not derived from any experience.
6. **No Arabic text**, while `prevailing_text: ar` — so the authoritative text of
   the estate's own ending does not exist.
7. **Written by [MX-018 D5](mx-018-third-party-dependencies.md)**, a dependency
   that does not survive sunset either.

## 9. Falsifier

> **IF FALSE.** Falsified if:
>
> - **(a)** the estate ends and any W1–W8 obligation applicable to the ending kind
>   is unperformed;
> - **(b)** any promise in §5's "survives" column is shown to fail on a frozen,
>   archived corpus;
> - **(c)** any promise in the "dies" column is shown to survive — which would
>   **improve** the estate's position;
> - **(d)** a portable archive (W5) is shown to require a build step, a platform,
>   or a dependency to read;
> - **(e)** an instrument passes its review interval with no reader-visible signal
>   — **this fires today** for any instrument whose stamp omits the next review
>   date.
>
> **(e) is runnable right now**, on this page: the stamp below prints a next review
> date, so a reader can check it against today. Any instrument in the corpus whose
> stamp omits one falsifies this clause immediately.

## 10. Obligation

**On the estate:**
- Perform **W5 now**, not at sunset. A portable archive is priority 1, is one act,
  and is the only obligation that survives every ending kind (§4.2).
- Print the **next review date** in every page stamp so staleness is
  reader-visible without tooling (§6, §9e).
- Write the **domain plan (W7)** — the single binary in the whole wind-down
  ([MX-018 D3](mx-018-third-party-dependencies.md)).
- Decide the **licence residue (W6)** or record expressly that sunset reduces
  ML-2.3 to twelve operative provisions (§3.1).
- Populate [GM-12 Class D](../00-governance-map/archive-register.md) **before**
  sunset; the duties to be withdrawn are already known.
- Announce with not less than 90 days on E1 (§4.1).
- Never let frozen text present as maintained (W2, F2).

**On a reader:**
- Check the next review date in the stamp. If it has passed, treat the instrument
  as unreviewed and the estate as possibly ended.
- Keep your own copy of anything you rely on. §5 says the text survives; it does
  not say the estate will hand it to you.

---

### Related

**Continuity and roles** — [MX-015](mx-015-succession-and-continuity.md) ·
[REG-08](../registries/reg-08-role-and-authority-registry.md) ·
[MX-013](mx-013-records-and-versioning.md) ·
[DEF-031](../00-governance-map/defect-register.md)

**Permanence promises at stake** — [ST-01](../standards/st-01-identifier-and-url-grammar.md) ·
[SITE-03](../site/routing-law.md) · [SITE-01](../site/route-manifest.md) ·
[GM-12 archive register](../00-governance-map/archive-register.md)

**Dependencies that end with the estate** — [MX-018](mx-018-third-party-dependencies.md) ·
[MX-024](mx-024-infrastructure-and-migration.md) ·
[MX-011](mx-011-security-and-disclosure.md) ·
[ST-22](../standards/st-22-platform-and-persistence.md)

**Decay and freshness** — [ST-05](../standards/st-05-decay-and-review-intervals.md) ·
[ST-13](../standards/st-13-static-build-and-sentinel.md) ·
[REG-02](../registries/reg-02-page-registry.md) ·
[GM-08 verification log](../00-governance-map/verification-log.md)

### Exit pair

1. **Release the archive today.** W5 is priority 1, survives every ending, has
   never been done, and takes one act.
2. **Check this page's own freshness.** The stamp below prints the next review
   date; compare it to today. [§9(e)](#9-falsifier) makes that your test, not the
   estate's.

<!-- mx-pagestamp: MX-019 · v2026.10.1 · governing · tier 3 · reviewed 2026-09-16 · next review 2027-09-16 -->
<!-- mx-demo: the live site is a demonstration; no wind-down obligation has ever been performed -->
