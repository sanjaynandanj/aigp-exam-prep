# AI Incident Response: Detection, Escalation, Serious-Incident Reporting

**Phase 6 · Lesson 07 · ~1.5h · BoK Domain IV**

## EXAM FOCUS

High-yield. Tested: what counts as an *AI* incident (broader than a security breach), detection channels, severity classification, the escalation runbook, the EU AI Act serious-incident reporting concept (Art. 73 — provider reports to market surveillance authorities; deployers inform providers), notification of regulators and affected parties, and disciplined post-incident review. Know the OECD AI Incidents Monitor at mention level. Classic trap: treating an AI harm incident as reportable only if personal data was breached.

## CORE

### What is an AI incident?

An AI incident is any event where an AI system's development, behavior, or use causes or nearly causes harm — **not limited to cyber events**. Categories:

| Category | Examples |
|---|---|
| Performance/harm | Systematic wrong decisions, discriminatory outcomes at scale, harmful/hallucinated outputs acted upon |
| Safety | Physical harm involving AI-controlled or AI-informed systems |
| Security | The Phase 5 L08 attack classes realized (poisoning, injection, model theft) |
| Privacy | Training-data leakage, membership-inference exposure, unlawful processing surfaced |
| Misuse/abuse | Users weaponizing the system beyond intended purpose; deepfake abuse |
| Transparency/compliance | Undisclosed AI interaction, missing labels, operating outside approved scope |

Include **near misses** ("AI incident hazards" in OECD terminology) — events that could plausibly have caused harm. Near-miss reporting is where cheap learning lives. The **OECD AI Incidents Monitor (AIM)** tracks publicly reported AI incidents globally and supports shared learning and taxonomy work (mention level).

### Detection channels

Incidents arrive through many doors — the program must wire them all to the same intake: monitoring alerts (Lesson 04), human overseers' overrides/escalations (Lesson 05), user complaints and appeals, employee reports (plus whistleblowing routes), vendor notifications (the SLA from Lesson 03), media/researchers/regulators. A single intake queue with an on-call owner prevents the classic failure: five teams each holding one piece of the picture.

### Severity classification and escalation

Pre-defined severity drives speed and seniority:

| Severity | Concept | Response posture |
|---|---|---|
| SEV-1 / critical | Ongoing serious harm; safety; legal reporting likely triggered | Immediate containment (suspend system/rollback), executive + legal engaged, regulator-clock assessment starts now |
| SEV-2 / major | Material harm to individuals/groups or major malfunction, contained | Same-day escalation, containment plan, reporting assessment |
| SEV-3 / minor | Limited impact, no rights harm | Standard queue, trend analysis |
| Near miss | No harm occurred, but could have | Log, analyze, feed prevention |

The **runbook** pre-answers: who classifies, who can suspend the system (authority to pull the plug — decided *before* the crisis), who informs legal/comms/privacy, which regulator clocks might start, and how evidence (logs! Lesson 04) is preserved.

### EU AI Act serious-incident reporting (Art. 73 concept)

- A **serious incident** concept covers: death or serious harm to health, serious and irreversible disruption of critical infrastructure management/operation, infringement of fundamental-rights obligations, or serious harm to property/environment.
- **Providers** of high-risk systems report serious incidents to the **market surveillance authority** of the Member State where the incident occurred — after establishing a causal link (or reasonable likelihood) between the system and the incident. Timelines are tiered by gravity: immediately-upon-link, with outer bounds of days (the Act sets short clocks — e.g., 15 days standard, faster for widespread infringement or critical-infrastructure/death cases; verify current status of exact operational deadlines and templates).
- **Deployers** who identify a serious incident inform the **provider** (then importer/distributor and authorities per the arrangement) — the reason vendor incident-notification SLAs (Lesson 03) matter in both directions.
- Reporting obligations sit alongside others: personal-data breach notification (GDPR clocks), sectoral regimes (medical devices, financial services), and contractual notice duties. One event can trigger several regimes at once.

### Affected-party notification and post-incident review

Beyond regulators: inform affected individuals where harm or legal duty requires — honestly, promptly, with remedy/recourse. Then run a **blameless post-incident review**: timeline, root cause (usually process + model + context, not one person), what detection missed, corrective actions with owners and dates, and updates to risk assessments, testing, monitoring thresholds, and training. Feed lessons to the AI inventory and, where appropriate, share externally (industry bodies, OECD AIM ecosystem). An incident that produces no control change will repeat.

## CASES & EXAMPLES

**Scenario 1 — not just breaches.** A benefits-eligibility model is discovered to have wrongly reduced payments to thousands of recipients over months. No data was breached. Is this an incident? *Answer:* yes — a harm/performance incident with fundamental-rights dimensions; potentially a serious incident (rights infringement concept) requiring reporting analysis. The "no breach, no incident" answer is the trap.

**Scenario 2 — deployer's move.** A hospital (deployer) suspects its high-risk diagnostic tool contributed to a patient's serious deterioration. First external step? *Answer:* inform the provider (Art. 73 concept flow) while suspending/containing use and preserving logs; the provider owes the market-surveillance-authority report once causality is assessed. Internal escalation and clinical remediation run in parallel.

**Scenario 3 — the unpluggable system.** During a live incident, no one can say who is authorized to switch off the trading model; two hours pass in escalation confusion. *Failed control:* the runbook must pre-assign suspension authority (including out-of-hours) — kill-switch governance is decided before, not during.

**Scenario 4 — multi-regime event.** A chatbot is prompt-injected into revealing other customers' data and produces defamatory content about a public figure. *Exam point:* one event, multiple tracks — security incident, personal-data breach clock (GDPR), possible AI-regime reporting, contractual notices, and affected-person notification. The runbook's job is to run the clocks in parallel.

## MEMORY HOOKS

**Definition hook:** *AI incident = harm or near-harm from behavior, not just breach of data.*

**Art. 73 flow:** *Deployer spots → informs Provider → Provider reports → Market surveillance authority.* (Say it as "D-P-M.")

**Response arc — "DCERN": Detect, Classify, Escalate/contain, Report, Never-again (post-incident review).**

The 5 facts to retain:

1. AI incidents span performance/discrimination harm, safety, security, privacy, misuse, and compliance events — including near misses; the OECD AI Incidents Monitor catalogs them globally.
2. Detection is multi-channel (monitoring, overseers, complaints, employees, vendors, media) and must converge on one owned intake with pre-set severity tiers.
3. EU AI Act Art. 73 concept: serious incidents (death/serious health harm, irreversible critical-infrastructure disruption, fundamental-rights infringement, serious property/environmental harm) → provider reports to market surveillance authorities on short, gravity-tiered clocks; verify current status of operational deadlines.
4. Deployers who identify a serious incident inform the provider — making two-way incident SLAs with vendors essential; parallel regimes (GDPR breach, sectoral, contract) can all fire on one event.
5. Suspension/kill-switch authority and evidence preservation are pre-assigned in the runbook; blameless post-incident reviews must change controls (thresholds, tests, training) or the incident repeats.

## SELF-CHECK

1. **Why is "AI incident" broader than "security incident"?**
   Because AI can cause harm through its ordinary operation — systematically wrong or discriminatory outputs, unsafe recommendations — without any attacker or data breach.
2. **List the four serious-incident categories in the Art. 73 concept.**
   Death or serious harm to a person's health; serious and irreversible disruption of critical-infrastructure management/operation; infringement of fundamental-rights obligations; serious harm to property or the environment.
3. **In the EU flow, what does a deployer do upon identifying a serious incident, and who files with the authority?**
   The deployer informs the provider (and per arrangements the importer/distributor/authorities); the provider reports to the market surveillance authority of the Member State where the incident occurred.
4. **Name four detection channels an AI incident program must wire to one intake.**
   Production monitoring alerts, human-overseer escalations/overrides, user complaints/appeals, employee reports, vendor notifications, external sources (media, researchers, regulators) — any four.
5. **What makes a post-incident review effective?**
   Blameless root-cause analysis (process + model + context), documented timeline, corrective actions with owners/dates, and concrete updates to assessments, tests, monitoring thresholds, and training — closing the loop so the class of failure can't silently recur.
