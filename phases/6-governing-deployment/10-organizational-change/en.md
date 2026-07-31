# Organizational Change: Training, Culture, and the Operating Rhythm

**Phase 6 · Lesson 10 · ~0.75h · BoK Domain IV**

## EXAM FOCUS

Domain IV closes with the human system around the AI systems. Tested: AI literacy as an obligation (EU AI Act Art. 4 concept) and role-based training design, culture and incentives as controls, the governance operating rhythm (councils, review cadences, board reporting), and program KPIs/KRIs. Exam framing: governance that lives in documents fails; the "best answer" usually institutionalizes a rhythm, an incentive, or a competence — not another policy PDF.

## CORE

### AI literacy (EU AI Act Art. 4 concept)

Providers and deployers must take measures to ensure a sufficient level of **AI literacy** in staff and others operating/using AI on their behalf — accounting for their technical knowledge, experience, education, training, and the context of use (a duty applying broadly, from the Act's early application phase). Practical translation: documented, role-appropriate training, refreshed as systems and rules change.

### Role-based training design

One-size training fails; map competence to role:

| Audience | Needs |
|---|---|
| Board / executives | AI risk-appetite literacy, accountability duties, what to ask of management |
| AI governance / risk / privacy / legal | Deep framework fluency (AI Act, NIST AI RMF, ISO/IEC 42001), assessment skills |
| Developers / data scientists | Governance-by-design: documentation, testing, security controls as engineering practice |
| Human overseers | System limits, failure modes, automation-bias resistance, override procedure (Lesson 05's competence duty) |
| Procurement / vendor managers | AI due-diligence questions, clause sets (Lessons 02–03) |
| All staff | Acceptable-use policy (incl. shadow-AI rules for public GenAI tools), how to recognize and report AI incidents |

Training is *evidence*: attendance, content versions, and competence checks are records auditors and regulators ask for (Art. 4-concept compliance is demonstrated, not asserted).

### Culture and incentives

Culture is what happens when the policy isn't looking. Levers:

- **Incentives aligned:** if teams are bonused purely on shipping speed and model lift, governance loses every tie-break. Include risk-quality measures (documentation completeness, gate first-pass rates, incident learning) in performance goals.
- **Psychological safety:** people must be able to raise AI concerns, override models (Lesson 05), and report near misses (Lesson 07) without penalty — speak-up channels plus visible non-retaliation.
- **Tone from the top and the middle:** executives who waive gates under deadline pressure teach the real policy; middle managers translate values into daily trade-offs.
- **Make the right path the easy path:** templates, checklists, tooling embedded in developer workflows beat 60-page standalone policies.

### The governance operating rhythm

Programs run on cadence, not heroics:

| Forum | Cadence (typical) | Business |
|---|---|---|
| AI governance council/committee | Monthly–quarterly | Intake/tier approvals, exceptions, policy changes, incident postmortems |
| Use-case review / release gates | Per system, as pipelined | Lessons 02/09 (Phase 5) decisions |
| Model risk / monitoring review | Monthly | Drift dashboards, threshold breaches, retraining approvals |
| Executive risk committee | Quarterly | Aggregate risk posture, exception trends, resourcing |
| **Board / audit committee reporting** | Quarterly–semiannual | Program KPIs/KRIs, serious incidents, regulatory horizon, assurance results (third-line reports — Lesson 08) |
| Annual cycle | Yearly | Inventory recertification, policy refresh, training renewal, program self-assessment (ISO/IEC 42001 management-review concept) |

### KPIs and KRIs for the program

| Type | Examples |
|---|---|
| **KPIs (performance — is the program working?)** | % of AI systems in inventory with named owner and current risk tier; % high-risk systems with current assessments; training completion by role; gate first-pass rate; mean time to complete intake; audit findings closed on time |
| **KRIs (risk — is exposure rising?)** | Count/trend of shadow-AI discoveries; overdue monitoring alerts; exception register size and age; override-rate anomalies; incident and near-miss trends (by severity); vendor systems past reassessment date |

Good metrics attach to owners and thresholds (a KRI without a trigger level is trivia), and board reports pair the numbers with narrative: what changed, what's coming (regulatory timeline), what needs decision.

## CASES & EXAMPLES

**Scenario 1 — the shelfware program.** An enterprise has a beautiful AI policy suite but no council calendar, no training records, and gates that teams route around under deadline pressure. Regulator interviews reveal staff can't describe the policy. *Exam point:* governance is operational, not documentary — the fixes are rhythm (standing forums), role-based training with records (Art. 4 concept), and incentive alignment, not more policy text.

**Scenario 2 — literacy scope.** A deployer trains only its data-science team on AI risk, reasoning that "they build the models." Customer-service staff using an AI assistant daily receive nothing. *Exam point:* the Art. 4-concept duty covers staff *using* AI on the organization's behalf, calibrated to role and context — the users needed training most.

**Scenario 3 — measured into failure.** Overseers of a claims model are evaluated on cases-per-hour; override rates collapse to near zero; a systematic model error runs for months. *Exam point:* incentives are controls — throughput-only metrics silently dismantled human oversight; add quality/override-integrity measures and fix workload.

**Scenario 4 — board blindness.** The board learns of a serious AI incident from the press. No AI KPI/KRI reporting line existed. *Exam point:* the operating rhythm must include periodic board-level reporting (posture, incidents, exceptions, assurance) — accountability at the top requires information flow to the top.

## MEMORY HOOKS

**Program triangle:** *Competence (training) × Culture (incentives, safety to speak) × Cadence (councils, reporting).* All three or the program is paper.

**Art. 4 capsule:** *Sufficient AI literacy, for everyone operating or using AI on your behalf, proportionate to role and context — and provable.*

**KPI vs KRI:** *KPI = is the program performing? KRI = is the risk growing?*

The 5 facts to retain:

1. EU AI Act Art. 4 concept: providers and deployers ensure sufficient, role-and-context-appropriate AI literacy for staff and others using AI on their behalf — evidenced by records.
2. Training is role-based: board, governance functions, builders, overseers, procurement, and all staff each need different competence — overseer training doubles as an Art. 26-concept duty.
3. Incentives and psychological safety are controls: throughput-only metrics and gate-waiving leadership dismantle governance faster than any missing document.
4. The program runs on cadence: governance council, monitoring reviews, executive risk committee, and board/audit-committee reporting with an annual recertification cycle.
5. KPIs track program health (inventory coverage, assessment currency, training completion, gate discipline); KRIs track rising exposure (shadow AI, exception aging, override anomalies, incident trends) — each with owner and threshold.

## SELF-CHECK

1. **Who is covered by the Art. 4 AI-literacy concept, and what calibrates the training?**
   Staff and other persons operating or using AI systems on the provider's/deployer's behalf; calibrated to their technical knowledge, experience, education, role, and the context/purpose of use.
2. **Why are incentives described as governance controls?**
   Because behavior follows measurement: rewarding only speed/throughput causes gates to be routed around and overrides to vanish — incentive design determines whether written controls operate.
3. **Name four forums in a governance operating rhythm and one item of business for each.**
   AI governance council (intake/exception decisions); monitoring/model-risk review (drift and threshold breaches); executive risk committee (aggregate posture, resourcing); board/audit committee (KPIs/KRIs, serious incidents, assurance results). Also: release gates per system; annual recertification.
4. **Give three KPIs and three KRIs for an AI governance program.**
   KPIs: % systems inventoried with owner/tier, % high-risk systems with current assessments, role-based training completion, gate first-pass rate. KRIs: shadow-AI discoveries, exception register age/size, override-rate anomalies, overdue vendor reassessments, incident/near-miss trends. (Any three of each.)
5. **What three organizational elements must combine for governance to be real rather than documentary?**
   Competence (role-based training with evidence), culture (aligned incentives, psychological safety, leadership tone), and cadence (standing councils, reviews, and board reporting).
