---
doc_id: "MX-025"
title_en: "Credentialing and Assessment"
title_ar: "الاعتماد والتقييم"
family: "corpus"
version: "v2026.10.2"
status: "canonical"
authority: "governing"
prevailing_text: "en"
audience_tier: 2
depth: 5
evidence_class: "durable"
review_interval_months: 12
curator: "Maher"
license: "ML-2.3"
designated: true
last_reviewed: "2026-09-25"
domain_tags: ["corpus", "credentials", "assessment", "rubric", "verification"]
route: "/credentials/"
derived_from: "THE METAX CORPUS v2026.09.0 Part II MX-005 §§5.1–5.11; 00_CREDENTIALING_ALIGNMENT_MAP_v2026.08.28"
supersedes: ["Index allocation MX-005 'Credentialing and Assessment' (refuge number; see GM-13, RAT-25)"]
ratification: "PENDING — RAT-25"
provenance_of_purpose: "specification"
authorship_note: "Drafted by an AI system under AG-000. The normative content is the source MX-005 carried forward; the refuge number and annex structure are the agent's. No credential has been issued."
hreflang: "en, ar"
---

# MX-025 · Credentialing and Assessment

> **Authority.** `governing`, tier 3. This is the instrument the index allocated as **MX-005** and
> which the source corpus published as MX-005. That number is now occupied by *Scope and
> Boundaries* ([GM-13](../00-governance-map/identifier-reallocation-record.md)). Operative forms:
> [RB-01](../rubrics/rb-01-d1-d5-rubric.md) (the rubric), [RB-02](../rubrics/rb-02-proof-ladder.md)
> (the proof ladder), [ST-30](../standards/st-30-registry-and-verifier.md) (the verifier). Record:
> [REG-05](../registries/reg-05-credential-registry.md). Appeals: [MX-016](mx-016-appeals-and-due-process.md).

> **Disclosure first.** **Zero credentials have been issued, and none can be.** Issue requires two
> calibrated reviewers for most tracks; the reviewer pool is empty
> ([REG-08](../registries/reg-08-role-and-authority-registry.md)). Revocation requires a panel;
> there is no panel. Every rule below is operative text with no operator.

---

## 1. Position

A credential is a claim made by an institution about a person, to a third party who was not
present. Its value is exactly the probability that the claim is true, and the third party cannot
check that probability unless the institution publishes how it decides and how often it says
no. The source corpus puts it in one sentence and this instrument inherits it:
**"Publishing revocations is the only thing that makes the valid credentials mean anything."**

What MetaX certifies is **judgement tested under scrutiny**: a named reviewer examined a real
artefact produced by the candidate, against a published rubric, in a process the candidate could
see, and could defend the decision to a second calibrated reviewer who had not seen the first
reviewer's reasoning. It certifies nothing about employability, income, or aptitude.

## 2. Definition — the four tracks

Names are fixed by the source and prevail over any variant (Annex A).

| Track | Requirement | Assessment | Renewal |
|---|---|---|---|
| **Series Practitioner** | One series completed; capstone accepted | Single reviewer | Does not expire |
| **Professional Operator** | Coherent set of series; portfolio showing judgement across contexts | Two reviewers + calibration check | 36 months, on evidence of continued practice |
| **Master-Fellow** | Body of work; a public contribution to the corpus | Panel; co-signature required | Does not expire; standing review |
| **MetaX Contributor** | Professional Operator + Branch D completion + one of S12, S21 or S24 + ethics review | Panel + ethics review | 12 months. Confers contribution rights, **no authority over doctrine** |

A **Completion Marker** is not a credential. It records that a course was finished and carries no
assessment claim ([DS-05](../design/ds-05-certification-surfaces.md)).

## 3. Mechanism

### 3.1 The rubric
One frozen scheme, **D1–D5** ([RB-01](../rubrics/rb-01-d1-d5-rubric.md)). No local variants; an
academy modifying it is out of compliance. The earlier competing scheme is void as of v2026.08.12
and its archived copy remains linked.

### 3.2 The proof ladder
Source form: *assertion, artefact, third-party verification*. Operative form: **P0–P3**
([RB-02](../rubrics/rb-02-proof-ladder.md)). Assertions are context only; artefacts carry weight;
any outcome claim **with a number attached** requires third-party verification. The level is
printed on the credential.

### 3.3 Evidence and ON REQUEST
Public evidence is preferred. Genuinely confidential evidence may be marked ON REQUEST, disclosed
only to assigned reviewers via the token-gated mechanism in [ST-29](../standards/st-29-security-architecture.md).
Over-marking is judged as under licence §B.6.5 — minimal, justified, non-defeating, burden on the
marker.

### 3.4 AI disclosure
Every submission carries one, including "none". Undisclosed AI use voids the submission.
Disclosed use is assessed on whether the candidate's judgement is evidenced.

### 3.5 Reviewers
Calibrated twice yearly against the specimen set ([RB-07](../rubrics/rb-07-agent-evaluation-specimens.md)
holds the agent set; the human set is **unwritten**, DEF-038). Identity disclosed to the candidate
at decision. Conflicts declared under [MX-017](mx-017-conflicts-of-interest.md). Paid for review,
never for outcome.

### 3.6 Decisions and reasons
Every decision carries written reasons mapped to D1–D5; rejections name the gap and the shortest
path to close it. **A decision without reasons is void.**

### 3.7 Fees
Fees purchase review — not outcome, not priority. No fee tier alters assessment. The evidence for
this claim is the published rejection rate, which does not yet exist.

### 3.8 Revocation
Grounds are closed: fraud in the submission, forgery, undisclosed material conflict, Charter
§0.4 conduct. Panel process, reasons published. **The Curator cannot revoke unilaterally.** A
revoked credential shows as revoked, with date and reason category, permanently.

### 3.9 Verification
Every credential has a pre-rendered static page with JSON-LD and a signed status-list entry. Three
states only: **valid, expired, revoked**. An unknown identifier is reported as *never issued* and
never confused with revocation ([ST-30](../standards/st-30-registry-and-verifier.md)).

### 3.10 Integrity Report
Annually: issued, rejected, expired, revoked, appeals filed, appeals upheld.

## 4. Worked instance (hypothetical, labelled)

*Hypothetical.* A candidate submits an S20 capstone claiming a 14% conversion lift. D4 cannot be
scored above the P1 line because the number has no third-party verification; the reviewer's
reasons say so and name the path — an independent analytics export. Series Practitioner is
awarded at P1 with the level printed. The lift claim is **not** printed on the credential.

## 5. Failure modes

- **Pay-for-pass by drift** — a "priority review" tier appears; forbidden by §3.7.
- **Reviewer as teacher** — the reviewer coached the candidate; conflict under MX-017.
- **Silent revocation** — removing a credential from the registry rather than marking it revoked.
- **Track-name drift** — "Pro Operator", "Fellow"; Annex A controls.

## 6. Limits

A credential here confers **no legal right to practise** any regulated profession. MetaX is not
accredited by any authority and does not seek to be. A credential certifies a judgement at a date;
it cannot certify the holder's current competence.

## 7. Falsifier

This instrument's central claim — that a MetaX credential is evidence of judgement — is falsified
if published rejection rates are near zero across a year of submissions, or if appeals are upheld
at a rate implying first-instance decisions are unreliable (>1 in 4 is the estate's proposed
threshold, `[VERIFY]` V-14: no empirical basis for the figure).

## 8. Obligation

**Curator:** name reviewers ([RAT-04](../00-governance-map/open-questions-and-ratifications.md));
write the human calibration set; publish the fee schedule ([RAT-08](../00-governance-map/open-questions-and-ratifications.md)).
**Until then:** no credential may be offered for sale, and every credential page states issue is
blocked.

## 9. Macro register

Credential inflation is a structural harm of mass education: when institutions are paid per
credential and never publish refusals, the credential converges on a receipt. The only known
counter-pressure is **public refusal statistics** plus **revocation that is visible forever**.
This instrument bets the estate's credibility on both.

---

## Annex A — Credential naming map

(Formerly index path `mx-005-annex-a-credential-naming-map.md`; source:
[Credentialing Alignment Map v2026.08.28](../../sources/00_CREDENTIALING_ALIGNMENT_MAP_v2026.08.28.md).)

| Earlier element | Governing name | Disposition |
|---|---|---|
| badge / completion marker | Completion Marker | Non-credential signalling only |
| Series Practitioner | Series Practitioner | Exact |
| Professional Operator | Professional Operator | Exact |
| Master-Fellow | Master-Fellow | Exact |
| contributor-readiness path | MetaX Contributor | Preparation language only; award is *MetaX Contributor* |
| D1–D5 rubric | RB-01 | Exact; frozen |
| P0–P3 proof ladder | RB-02 | Operational form of source §5.3 |

**Rule.** Every handbook, verifier page, dossier template, academy directory, and badge generated
after this annex uses these names exactly. Older files keep their text with a
superseded-terminology annotation.

---

**Related:** [RB-01](../rubrics/rb-01-d1-d5-rubric.md) · [RB-02](../rubrics/rb-02-proof-ladder.md) ·
[REG-05](../registries/reg-05-credential-registry.md) · [ST-30](../standards/st-30-registry-and-verifier.md) ·
[DS-05](../design/ds-05-certification-surfaces.md) · [MX-016](mx-016-appeals-and-due-process.md) ·
[MX-017](mx-017-conflicts-of-interest.md) · [MX-029](mx-029-academies-charter.md) ·
[ST-33](../standards/st-33-assessment-and-academy-templates.md)
