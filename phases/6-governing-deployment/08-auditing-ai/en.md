# Auditing AI Systems: Internal, External, and Algorithmic Audits

**Phase 6 · Lesson 08 · ~1h · BoK Domain IV**

## EXAM FOCUS

Tested: internal audit's third-line role (vs first/second lines), what an algorithmic audit covers (data, model, outcomes, governance), when external/independent audits are used or mandated, NYC Local Law 144 as the concrete mandated bias-audit regime, and what audit evidence/workpapers look like for AI. Distractor patterns: confusing second-line risk review with third-line audit, and confusing a vendor's self-assessment with an independent audit.

## CORE

### The three lines, applied to AI

| Line | Who | AI role |
|---|---|---|
| **First line** | Product, ML/engineering, business owners | Own and operate the risk: build controls, run monitoring, keep records |
| **Second line** | AI governance, risk, compliance, privacy | Set policy, challenge, review gates and assessments |
| **Third line** | **Internal audit** | *Independent assurance* to board/audit committee that lines 1–2 actually work |

Internal audit does not design AI controls (that would compromise independence); it verifies they exist, operate, and produce the evidence they claim. Typical AI audit universe items: the AI inventory's completeness (are there shadow systems?), gate discipline (were releases actually approved as policy requires?), monitoring effectiveness, model documentation, vendor-risk execution, incident handling.

### Anatomy of an algorithmic audit

An algorithmic audit examines a specific system across four scopes:

| Scope | Questions | Evidence examined |
|---|---|---|
| **Data** | Provenance lawful? Representative? Quality-controlled? | Datasheets, lineage records, quality reports, licenses/bases |
| **Model** | Built and validated as claimed? Reproducible? Documented? | Training records, versioning, test results vs acceptance criteria, model cards |
| **Outcomes** | What does it actually do to people? Disparate impact? Error distribution? | Production outputs, disaggregated outcome analysis, override and complaint data |
| **Governance** | Were the required processes followed? | Intake, assessments, gate sign-offs, monitoring logs, incident records |

Outcome analysis is what distinguishes algorithmic auditing from documentation review: auditors test *behavior* (e.g., re-run evaluations, analyze production decision data by subgroup), not just paperwork.

### Internal vs external/independent audits

| Type | Strength | When |
|---|---|---|
| Internal (third line) | Context, access, continuous coverage | Ongoing program assurance |
| External/independent | Credibility, specialist skill, required independence | Legal mandates (LL144), certification (ISO/IEC 42001 audits), high-stakes public trust, board demand |
| Vendor self-assessment | Cheap, fast | Never a substitute for independence — input evidence only |

Independence essentials: auditor selects methods and samples, has unrestricted access to records/systems within scope, reports findings without the auditee editing conclusions, and has no stake in the system's success.

### NYC Local Law 144 — the concrete regime

New York City's Local Law 144 (in force with enforcement from 2023) governs **Automated Employment Decision Tools (AEDTs)** used for hiring/promotion decisions concerning NYC candidates/employees:

| Element | Requirement (concept) |
|---|---|
| **Bias audit** | Annual, by an **independent auditor**, before use continues |
| **Content** | Selection/scoring outcomes disaggregated by sex and race/ethnicity — computing impact ratios (selection rate or average score of each group vs the most favored group) |
| **Publication** | A public summary of results and the distribution date of the tool |
| **Notice** | Candidates/employees notified of AEDT use (in advance) and of the job qualifications/characteristics assessed |

LL144 is the exam's model of a *mandated, published, independent* algorithmic audit — narrow in scope (employment tools, two demographic axes) but real, enforced, and a template regulators elsewhere study.

### Audit evidence and workpapers

AI audits stand on evidence discipline: defined scope and criteria (audit against *what* — policy, ISO/IEC 42001, NIST AI RMF, statute); sampling methodology recorded; workpapers preserving what was examined (versions! which model, which data snapshot, which period of logs); findings tied to criteria with severity ratings; management responses with owners and remediation dates; and follow-up verification. The Phase 5–6 record trail (lineage triangle, gate sign-offs, monitoring logs) is precisely what makes an AI system *auditable* — systems without records are unauditable, which is itself a reportable finding.

## CASES & EXAMPLES

**Scenario 1 — line confusion.** The AI governance team reviews and approves release gates, then proposes to also "audit" the program annually and report to the board that all is well. *Exam point:* second line cannot provide third-line assurance on its own work — internal audit (or an external party) must independently assess, or the board is grading homework the same team wrote.

**Scenario 2 — LL144 in practice.** A company uses a vendor's video-interview scoring AEDT for NYC roles. The vendor offers its internal fairness report as compliance. *Answer:* insufficient — LL144 requires an annual bias audit by an *independent* auditor, a published results summary, and advance candidate notice; the deploying employer cannot rely on the vendor's self-assessment.

**Scenario 3 — paperwork vs behavior.** An algorithmic audit of a credit model finds impeccable documentation, but outcome testing on production data reveals a materially higher error rate for older applicants — never surfaced because monitoring didn't disaggregate by age. *Exam point:* the outcomes scope is indispensable; documentation review alone would have passed the system.

**Scenario 4 — the unauditable model.** Auditors request the training-data snapshot and version lineage for a two-year-old production model; neither exists. *Exam point:* inability to audit is a finding in itself — record-keeping failures (Phase 5 L04) escalate to the audit committee as a control breakdown, not a shrug.

## MEMORY HOOKS

**Three lines one-liner:** *First line runs it, second line challenges it, third line proves whether the first two are true.*

**Algorithmic audit scope — "DMOG": Data, Model, Outcomes, Governance.** (Outcomes = the scope only audits of *behavior* cover.)

**LL144 capsule:** *AEDT + annual independent bias audit + impact ratios by sex & race/ethnicity + public summary + candidate notice.*

The 5 facts to retain:

1. Internal audit is the third line: independent assurance over AI controls to the board — it verifies, it does not design or operate controls.
2. Algorithmic audits cover four scopes — data, model, outcomes, governance — and must test actual behavior/outcomes, not just documents.
3. External/independent audits are required by mandate (LL144), certification (ISO/IEC 42001), or trust demands; vendor self-assessments never substitute for independence.
4. NYC LL144: annual independent bias audits of automated employment decision tools, impact ratios by sex and race/ethnicity, published summaries, advance candidate notice.
5. Auditability is a system property built from records (versioned data/models, gate sign-offs, logs); missing records are themselves a reportable control failure.

## SELF-CHECK

1. **Why can't the AI governance function audit the AI program it oversees?**
   It is second line — it sets and operates the control framework; independent assurance requires a party (third line/internal audit or external) with no ownership of the controls being assessed.
2. **Name the four scopes of an algorithmic audit and the distinctive one.**
   Data, model, outcomes, governance; outcomes is distinctive — testing what the system actually does to people in production, not what documents claim.
3. **What does NYC LL144 require before an employer keeps using an AEDT on NYC candidates?**
   An annual bias audit by an independent auditor (impact ratios of selection rates/scores by sex and race/ethnicity), public posting of a results summary, and advance notice to candidates of AEDT use and assessed qualifications.
4. **What belongs in AI audit workpapers to make findings defensible?**
   Scope and criteria, sampling method, exact artifact versions examined (model/data/log periods), evidence collected, findings mapped to criteria with severity, management responses with owners/dates, and follow-up records.
5. **An audited system has no data snapshots or version history. What is the correct audit outcome?**
   Report the record-keeping/control breakdown as a finding (the system is effectively unauditable) and escalate — do not issue assurance based on unverifiable claims.
