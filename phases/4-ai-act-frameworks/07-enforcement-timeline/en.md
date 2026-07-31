# Enforcement: The AI Office, Penalties, and the Application Timeline

**Phase 4 · Lesson 07 · ~1h · BoK Domain II**

## EXAM FOCUS

Three memorization blocks with near-guaranteed questions: (1) the **institutional map** — AI Office vs national market-surveillance authorities vs AI Board (who enforces what); (2) the **three penalty tiers** with their percentages and amounts; (3) the **staggered application timeline** from entry into force to full applicability. Timeline questions are usually direct recall ("which obligations applied from February 2025?"). Note: EU digital-omnibus/simplification discussions have floated adjusting some dates and duties — learn the enacted schedule below, and in practice **verify current status (as of mid-2026)**.

## CORE

### The institutional map

| Body | What it is | Enforces / does |
|---|---|---|
| **AI Office** (within the European Commission) | EU-level centre of AI expertise, established 2024 | **Exclusive supervisor/enforcer for GPAI model providers**; develops codes of practice, guidelines, training-content template; coordinates implementation; supports sandboxes; can request information, order evaluations, demand mitigation for GPAI |
| **National market-surveillance authorities (MSAs)** | Member-state designated authorities (each state names MSAs + a notifying authority; single point of contact) | Enforce the Act for **AI systems** in their territory: investigations, access to documentation/logs (source code as last resort), corrective orders, withdrawals/recalls, penalties per national procedures; fundamental-rights authorities get cooperation rights |
| **European Artificial Intelligence Board (AI Board)** | Representatives of member states (+ observers) | Coordination and consistency: advises Commission, opinions, shares best practices — the AI Act's cousin of the EDPB |
| **Advisory Forum** | Stakeholders (industry, SMEs, academia, civil society) | Advises Board & Commission |
| **Scientific Panel of independent experts** | Technical experts | Supports GPAI oversight; can issue **qualified alerts** that a model poses systemic risk |
| **EDPS** | European Data Protection Supervisor | Market surveillance for **EU institutions'** AI use; can fine EU bodies |
| **Notifying authorities / notified bodies** | Lesson 06 | Conformity-assessment infrastructure |

Individuals may **lodge complaints** with market-surveillance authorities; affected persons hold the explanation right (Lesson 04).

### The penalty tiers — memorize cold

| Tier | Violation | Maximum fine (whichever is **higher**) |
|---|---|---|
| **Top** | **Prohibited practices (Art. 5)** | **€35,000,000 or 7%** of total worldwide annual turnover |
| **Middle** | Most other obligations: high-risk requirements and operator duties (providers, deployers, importers, distributors, authorized reps), transparency-tier duties, notified-body duties | **€15,000,000 or 3%** |
| **Bottom** | **Supplying incorrect, incomplete or misleading information** to notified bodies or authorities | **€7,500,000 or 1%** |
| GPAI providers | GPAI-chapter violations (incl. ignoring Commission measures) | Up to **3% or €15M** (Commission-imposed) |
| SMEs/startups | Same tiers but **whichever is LOWER** applies | The pro-SME inversion — a favorite exam nuance |

Fines are set considering nature/gravity/duration, intent/negligence, cooperation, size, and prior violations; member states lay down procedures (and can fine public authorities per national rules); the Commission fines GPAI providers directly.

### The application timeline — the exam's favorite date drill

| Date | What becomes applicable |
|---|---|
| **1 Aug 2024** | **Entry into force** (20 days after OJ publication of Regulation (EU) 2024/1689) — clock starts, nothing yet enforceable |
| **2 Feb 2025** (+6 months) | **Prohibited practices (Art. 5)** + the general-provisions chapter incl. the **AI-literacy duty** (providers/deployers must ensure adequate AI literacy of their staff/operators) |
| **2 Aug 2025** (+12 months) | **GPAI model obligations**; governance institutions (AI Office operational role, Board, scientific panel); **penalties regime**; notified-body/notification chapters; confidentiality |
| **2 Aug 2026** (+24 months) | **General applicability** — the bulk: high-risk Annex III regime, transparency-tier duties, sandboxes operational, registration, deployer duties, FRIAs |
| **2 Aug 2027** (+36 months) | **Annex I high-risk** (AI as safety components of sectorally regulated products); deadline for **pre-Aug-2025 GPAI models** to comply |
| Legacy systems | High-risk systems already on the market before their applicability date are caught when **substantially modified** (public-authority systems get a longer catch-up: by 2030) |

> **Flux warning:** Commission "digital omnibus" simplification proposals (2025–2026) contemplate targeted adjustments — e.g., easing some documentation/registration burdens and potentially re-timing parts of the high-risk regime pending standards readiness. Nothing in the enacted baseline above should be treated as moved until adopted. **Status as of mid-2026 — verify current dates before relying on them (and before your exam).**

### Enforcement mechanics worth knowing

- **Market-surveillance model:** post-market policing (documentation requests, evaluations of compliance, corrective orders, recalls/withdrawals) — not a licensing regime; the pre-market gate is conformity assessment (Lesson 06).
- **Safeguard procedures:** an MSA restricting a system notifies the Commission/other states; disputes escalate to Commission decision — keeping the single market coherent.
- **Serious-incident reports** (providers; deployers feed in) go to MSAs — 15-day baseline, shorter for deaths/widespread incidents.
- **Union testing facilities** and coordinated actions support technically demanding evaluations (esp. GPAI).
- No US-style private damages action **in the Act itself** — individual redress rides on the explanation right, complaints, and national/PLD liability law (Lesson 3.08).

## CASES & EXAMPLES

**Scenario 1 — Wrong regulator.** A French deployer's high-risk hiring tool draws complaints; simultaneously, a GPAI lab's model shows dangerous capabilities. Who acts? *Analysis:* The hiring system → **French market-surveillance authority** (national enforcement of system-level duties). The GPAI model → the **AI Office/Commission** (exclusive GPAI supervision), possibly triggered by a scientific-panel qualified alert. The AI Board coordinates neither case directly — it aligns practice.

**Scenario 2 — Tier arithmetic.** A mid-cap with €2B global turnover (a) deploys an emotion-recognition system on its factory floor, and (b) files an incomplete technical file with a notified body. *Analysis:* (a) prohibited practice → up to the higher of €35M or 7% (€140M) → **€140M ceiling**; (b) misleading/incomplete information to a notified body → up to the higher of €7.5M or 1% (€20M) → **€20M ceiling**. For an SME, each tier flips to the **lower** figure.

**Scenario 3 — Date logic.** In March 2025 a company plans: (a) to keep selling its social-scoring product "until the AI Act fully applies in 2026," and (b) to launch a new GPAI model in September 2025. *Analysis:* (a) wrong — Art. 5 bans applied **2 Feb 2025**; continued marketing is already sanctionable. (b) the model launches after **2 Aug 2025**, so full GPAI duties apply at launch — no 2027 grace (that's only for models on the market before Aug 2025).

**Scenario 4 — Literacy sleeper clause.** An auditor asks a deployer in mid-2025 what AI Act duties it already has, given it uses only minimal-risk tools. *Analysis:* The **AI-literacy obligation** (applicable since Feb 2025) applies to providers and deployers of AI systems broadly — staff dealing with AI need sufficient literacy proportionate to context. It's the most commonly forgotten "already-live" duty.

## MEMORY HOOKS

- **Penalty ladder — "7-3-1":** *7% bans, 3% breaches, 1% lies* (prohibitions / most obligations / misinformation to authorities), paired with **35-15-7.5** in millions. GPAI sits at the 3%/15M rung, fined by the Commission.
- **Higher-or-lower flip:** big companies pay the **higher** of the two; SMEs the **lower**.
- **Timeline chant — "6-12-24-36":** months after Aug 2024 → *bans & literacy (Feb 25) → GPAI & penalties (Aug 25) → the big bang (Aug 26) → embedded products & legacy GPAI (Aug 27).*
- **Institution one-liners:** *Office = GPAI sheriff; MSAs = everything-else sheriffs; Board = coordination, not enforcement; Panel = the alarm bell; EDPS = polices the EU's own house.*
- **Omnibus asterisk:** enacted schedule first, then "verify current status" — the exam may reward knowing dates *were* subject to simplification debate.

**The 5 facts to retain:**
1. AI Office exclusively supervises **GPAI model providers**; national market-surveillance authorities enforce against AI-system operators; the AI Board coordinates.
2. Penalty tiers: **7%/€35M** (prohibitions), **3%/€15M** (most obligations, incl. GPAI), **1%/€7.5M** (misleading information) — higher of the two, inverted to lower for SMEs.
3. Timeline: in force **Aug 2024**; prohibitions + AI literacy **Feb 2025**; GPAI + penalties **Aug 2025**; general application **Aug 2026**; Annex I products + legacy GPAI **Aug 2027**.
4. Enforcement is market-surveillance-style (documents, logs, corrective orders, recalls) with complaint rights for individuals; no self-standing damages action in the Act.
5. Simplification/omnibus adjustments were under discussion — status as of mid-2026, always verify current dates.

## SELF-CHECK

1. **Q:** Match the enforcer: (a) a systemic-risk GPAI provider ignoring evaluation duties; (b) a Spanish clinic deploying a non-compliant high-risk triage system; (c) an EU agency using AI unlawfully.
   **A:** (a) AI Office/Commission; (b) Spain's market-surveillance authority; (c) the EDPS.

2. **Q:** State the three penalty tiers with amounts and percentages, and the SME twist.
   **A:** Prohibited practices: up to €35M or 7% of worldwide turnover; most other obligations: €15M or 3%; supplying incorrect/incomplete/misleading information: €7.5M or 1% — whichever is higher, except SMEs/startups pay whichever is lower.

3. **Q:** Which obligations applied from 2 February 2025, and which from 2 August 2025?
   **A:** Feb 2025: Article 5 prohibitions and the AI-literacy duty (plus general provisions). Aug 2025: GPAI model obligations, governance bodies, notified-body chapters, and the penalties regime.

4. **Q:** When do the core high-risk (Annex III) obligations and the Annex I embedded-product obligations apply?
   **A:** Annex III high-risk regime: 2 August 2026. Annex I product-embedded high-risk AI: 2 August 2027 (also the compliance deadline for GPAI models marketed before Aug 2025).

5. **Q:** What is the AI Board, and what is it *not*?
   **A:** A coordination body of member-state representatives ensuring consistent application, issuing opinions and best practices (EDPB-analog) — it is not an enforcement authority and does not fine anyone.
