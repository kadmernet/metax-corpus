---
doc_id: "REG-13"
title_en: "Decay Calendar: Register Re-verification Dates (HX-000 v2027.1 and BX-018)"
title_ar: "تقويم التقادم [AR-DRAFT]"
family: "registries"
version: "v2026.10.3"
status: "draft"
authority: "record"
prevailing_text: "en"
audience_tier: 4
depth: 4
evidence_class: "perishable"
review_interval_months: 3
curator: "Maher"
license: "ML-2.3"
designated: false
last_reviewed: "2026-10-08"
domain_tags: ["registry", "decay", "verify", "harms", "review-calendar"]
route: "/library/decay/calendar/"
rule_hx: "verify(HX-n) = 2027-01 + (((n − 1) mod 12) + 1) months"
rule_bx: "verify(BX-n) = 2027-06 + (((n − 1) mod 12) + 1) months"
human_read: "none"
conformance_state: "met"
derived_from: "HX-000 v2027.1 §6 and §9; BX-018 §9; ML-2.4 §4 corrected rule; sources/BX-000_and_HX-000_v2027.1.md per-entry Verify fields"
authorship_note: "Computed by an AI system under AG-000 to close GM-17 M-18. Every date is computed from the rule. The 'source' column shows where the source's own date was read and agrees. This file supersedes no date: the registers keep theirs."
hreflang: "en, ar"
---

# REG-13 · Decay Calendar

> **Authority.** A **record**. It computes when each register entry falls due for re-verification
> under the corrected rule (ML-2.4 §4, BX-018 §9). It is the input to the Decay Watch surface
> (`/library/decay/`, MX-001 §1.2). It changes no register entry.

> **Disclosure first.** Computing this calendar showed that an earlier finding was wrong. DEF-051
> said that the source's verify dates follow neither rule. **They all follow the corrected rule.**
> The source stated the wrong formula and applied the right one. This is corrected at
> [C-18](../00-governance-map/corrections-log.md#c-18).

---

## 1. Rules

| Register | Rule | Why "(n − 1) mod 12 + 1" |
|---|---|---|
| HX-000 v2027.1 | `2027-01 + (((n − 1) mod 12) + 1)` months | `(n mod 12)` returns 0 for n = 12, 24, which would place the entry at 2027-01, before the cycle opens |
| BX-018 | `2027-06 + (((n − 1) mod 12) + 1)` months | same defect, same correction |

**Spreading.** Each register has entries falling due in every month of a 12-month cycle, so no single review month carries the whole register. After a verification the entry's next date is **the same month one year later**, unless the entry's evidence class requires a shorter interval (ST-05). In that case the shorter interval governs.

## 2. HX-000 v2027.1 (28 entries)

| Month | Entries due | Absolutes among them | Source date agrees? |
|---|---|---|---|
| **2027-02** | HX-01, HX-13, HX-25 | HX-01 (i) | yes (all three) |
| **2027-03** | HX-02, HX-14, HX-26 | HX-14 (v) | yes |
| **2027-04** | HX-03, HX-15, HX-27 | HX-03 (iv); HX-27 (ix, proposed) | yes |
| **2027-05** | HX-04, HX-16, HX-28 | HX-04 (ii) | yes |
| **2027-06** | HX-05, HX-17 | — | yes |
| **2027-07** | HX-06, HX-18 | HX-06 (iii) | yes |
| **2027-08** | HX-07, HX-19 | — | yes |
| **2027-09** | HX-08, HX-20 | HX-20 (vi) | yes |
| **2027-10** | HX-09, HX-21 | — | yes |
| **2027-11** | HX-10, HX-22 | HX-22 (viii) | yes |
| **2027-12** | HX-11, HX-23 | — | yes |
| **2028-01** | HX-12, HX-24 | HX-24 (vii) | yes. *These are the two entries the uncorrected rule would have sent to month 0* |

**Load.** The first four months carry three entries each and the others carry two. Every month except 2027-06, -08, -10 and -12 includes an absolute. **An absolute's verification can narrow it only through Track 2** (ML-2.4 §2). Verification can reaffirm or flag an absolute, never repeal it.

## 3. BX-018 (24 entries)

| Month | Entries due | Refusals among them | Source date checked |
|---|---|---|---|
| **2027-07** | BX-01, BX-13 | — | **BX-01 yes, BX-13 yes** |
| **2027-08** | BX-02, BX-14 | BX-02 (A-1) | not checked |
| **2027-09** | BX-03, BX-15 | — | not checked |
| **2027-10** | BX-04, BX-16 | BX-16 (A-8 part) | not checked |
| **2027-11** | BX-05, BX-17 | BX-05 (A-2), BX-17 (A-5) | not checked |
| **2027-12** | BX-06, BX-18 | — | not checked |
| **2028-01** | BX-07, BX-19 | BX-07 (A-3), BX-19 (A-6) | not checked |
| **2028-02** | BX-08, BX-20 | — | not checked |
| **2028-03** | BX-09, BX-21 | — (BX-21 flagged) | not checked |
| **2028-04** | BX-10, BX-22 | BX-22 (A-7) | not checked |
| **2028-05** | BX-11, BX-23 | BX-23 (A-8) | not checked |
| **2028-06** | BX-12, BX-24 | BX-12 (A-4) | not checked |

**Two further "2027-07" dates in the source were checked and are not BX dates.** Source l.962 ("Crosswalk → BX-12 … absolute, in force") is the end of the **HX-06** entry. Source l.1178 ("Crosswalk → BX-20 …") is the end of the **HX-18** entry. Both are 2027-07 under the HX rule, as §2 shows. A reader who searches the source for "BX-12" will find an HX date. The crosswalk arrows (→ BX-nn) mark HX entries, and the arrows (← HX-nn) mark BX entries.

**Re-derivation overrides the calendar.** BX-018 is re-derived in full at 2029-06, or at the first S2+/I1+ Deployment, whichever is earlier (§B-E.6). Re-derivation means re-argued, not re-dated.

**The four flagged entries** (BX-02, BX-07, BX-11, BX-21) are reviewed **first in their month** (BX-018 §9).

## 4. What "verified" means on a date

On its date, an entry is re-checked against its **falsifier**. The outcome is one of:
- `reaffirmed`: the falsifier has not been met.
- `narrowed`: published under §E.5. An absolute can be narrowed only via Track 2.
- `flagged`: the evidence has weakened and the entry is held for the Curator.
- `withdrawn`: published under §E.5.

**A date that passes without a recorded outcome is shown in Decay Watch as `overdue`, in public.** That is the whole point of the surface.

## 5. Machine form

```json
{"calendar":"REG-13","version":"2026.10.3",
 "rules":{"HX":"2027-01 + (((n-1) mod 12) + 1) months","BX":"2027-06 + (((n-1) mod 12) + 1) months"},
 "hx":{"2027-02":["HX-01","HX-13","HX-25"],"2027-03":["HX-02","HX-14","HX-26"],"2027-04":["HX-03","HX-15","HX-27"],
       "2027-05":["HX-04","HX-16","HX-28"],"2027-06":["HX-05","HX-17"],"2027-07":["HX-06","HX-18"],
       "2027-08":["HX-07","HX-19"],"2027-09":["HX-08","HX-20"],"2027-10":["HX-09","HX-21"],
       "2027-11":["HX-10","HX-22"],"2027-12":["HX-11","HX-23"],"2028-01":["HX-12","HX-24"]},
 "bx":{"2027-07":["BX-01","BX-13"],"2027-08":["BX-02","BX-14"],"2027-09":["BX-03","BX-15"],"2027-10":["BX-04","BX-16"],
       "2027-11":["BX-05","BX-17"],"2027-12":["BX-06","BX-18"],"2028-01":["BX-07","BX-19"],"2028-02":["BX-08","BX-20"],
       "2028-03":["BX-09","BX-21"],"2028-04":["BX-10","BX-22"],"2028-05":["BX-11","BX-23"],"2028-06":["BX-12","BX-24"]},
 "bx_rederivation":"2029-06 or first S2+/I1+ deployment","outcomes":["reaffirmed","narrowed","flagged","withdrawn","overdue"]}
```

## 6. Falsifier

This calendar is wrong if any date in §2 or §3 differs from its rule applied to its entry number.
It is also wrong if any source verify date that has been checked differs from the computed date and is
not listed in §3. The second check covers 28 HX entries and 2 BX entries. The other 22 BX dates are unchecked (V-22), and that is the limit of this file.

---

**Related:** [HX-000 v2027.1](../harms/hx-000-register-v2027-1.md) · [BX-018](../bcia/bx-018-register-of-substrate-harms.md) · [ST-05](../standards/st-05-decay-and-review-intervals.md) ·
[C-18](../00-governance-map/corrections-log.md#c-18) · [GM-17](../00-governance-map/corpus-review-v2027.1.md)
