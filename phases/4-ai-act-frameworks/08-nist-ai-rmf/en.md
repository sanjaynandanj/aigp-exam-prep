# NIST AI RMF: Govern, Map, Measure, Manage — the Exam's Backbone Framework

**Phase 4 · Lesson 08 · ~1.5h · BoK Domain II**

## EXAM FOCUS

The NIST AI Risk Management Framework (AI RMF 1.0, January 2023) is the exam's backbone *framework*: it supplies the vocabulary for Domains III and IV (risk, trustworthiness characteristics, lifecycle governance) and appears directly in Domain II. You must know: its **voluntary, non-sector-specific nature**, the **seven trustworthy-AI characteristics**, and — above all — the **four functions** (GOVERN, MAP, MEASURE, MANAGE) with their purposes and representative activities, plus **profiles** and the **Generative AI Profile**. Expect "which function does this activity belong to?" questions.

## CORE

### What the AI RMF is

| Attribute | Value |
|---|---|
| Issuer | US National Institute of Standards and Technology, directed by the National AI Initiative Act of 2020 |
| Nature | **Voluntary**, rights-preserving, non-sector-specific, use-case agnostic; consensus-developed with industry/civil society |
| Goal | Cultivate a **risk-management culture** to increase AI **trustworthiness** and minimize negative impacts to people, organizations, ecosystems |
| Structure | Part 1: framing (risk, harms, trustworthiness); Part 2: the **Core** — 4 functions → 19 categories → ~72 subcategories; plus **Profiles**; companion **Playbook** (suggested actions), crosswalks to ISO/OECD/EU |
| Key framing ideas | Risk = f(**probability × magnitude** of impact, positive or negative); risk is **contextual**; zero risk is unattainable — aim for **risk tolerance**-informed prioritization; harms taxonomy: **people / organizations / ecosystems**; measure at points across the **lifecycle**; socio-technical lens with diverse actors |

### The seven trustworthy-AI characteristics

**Valid & reliable** (the precondition) · **Safe** · **Secure & resilient** · **Accountable & transparent** · **Explainable & interpretable** · **Privacy-enhanced** · **Fair — with harmful bias managed**. Trade-offs among them are expected and must be negotiated in context (e.g., explainability vs accuracy, privacy vs fairness testing). NIST's bias companion work distinguishes **systemic, computational/statistical, and human-cognitive** bias.

### The four functions — the big table

| Function | Purpose in one line | Representative categories/activities | Question cues |
|---|---|---|---|
| **GOVERN** (cross-cutting — feeds all others) | Cultivate the organizational **culture, structures, policies and accountability** for AI risk | Policies/processes for the RMF aligned to legal requirements; **roles, responsibilities and lines of accountability**; workforce diversity & training/AI literacy; culture that surfaces risk; stakeholder-engagement processes; **third-party/supply-chain risk policies**; inventories; decommissioning policies; risk appetite/tolerance setting | "Board," "policy," "accountability," "culture," "vendor policy," "training program" |
| **MAP** | Establish **context** and **identify** risks before you can measure or manage them | Define intended purpose, users, deployment context and expectations; categorize the system; map capabilities, targeted usage, goals, costs/benefits; identify risks & benefits for **individuals, groups, communities, organizations, society**; assess **third-party components** (incl. data provenance); document assumptions/limitations; interdisciplinary + external input | "Context," "intended use," "stakeholder identification," "impact identification," "use-case scoping" |
| **MEASURE** | **Analyze, assess, benchmark and monitor** risks using quantitative/qualitative methods | Select and apply metrics/TEVV (test, evaluation, verification, validation); evaluate systems for the **trustworthy characteristics** (accuracy, robustness, fairness/bias testing, privacy, security, explainability); red-teaming; track identified risks over time; assess measurement effectiveness itself; mechanisms for **feedback from affected communities**; independent review | "Metrics," "testing," "benchmark," "evaluation," "monitoring results," "bias audit," "red team findings" |
| **MANAGE** | **Prioritize, respond to and act on** measured risks; allocate resources | Rank risks by tolerance/impact; decide: avoid, mitigate, transfer or **accept**; plan responses & resourcing; treat residual risk explicitly (documented, communicated to deployers/users); **incident response, recovery and communication plans**; post-deployment **monitoring + improvement**; third-party risk treatment; **decommissioning/phase-out**; document and report | "Prioritize," "treatment," "accept the risk," "incident response," "mitigation plan," "sunset" |

**Cycle logic:** GOVERN is the soil; MAP → MEASURE → MANAGE iterate continuously through the lifecycle — the RMF is a loop, not a one-time gate.

### Profiles

- **Use-case / sector profiles:** tailored implementations of the Core for a domain (e.g., hiring, lending) — "current profile" (where you are) vs "target profile" (where you should be), gap-driving.
- **The Generative AI Profile (NIST AI 600-1, July 2024):** the cross-sectoral profile for GenAI, cataloguing **12 risks unique to or exacerbated by GenAI** — CBRN information or capabilities · confabulation (hallucination) · dangerous, violent or hateful content · data privacy · environmental impacts · harmful bias and homogenization · human-AI configuration (over-reliance, anthropomorphization) · **information integrity** (mis/disinformation, synthetic content) · **information security** (prompt injection, model theft, data exfiltration) · intellectual property · obscene/degrading/abusive content (incl. CSAM/NCII) · **value chain and component integration** — with ~200 suggested actions mapped to GOVERN/MAP/MEASURE/MANAGE.
- **Companion NIST publications to recognize by name:**
  - **AI 100-1** — the AI RMF 1.0 itself (Jan 2023).
  - **AI 100-2 E2023/E2025** — *Adversarial Machine Learning* taxonomy of attacks & defenses (feeds MEASURE/MANAGE for security).
  - **AI 100-4** — Reducing Risks Posed by Synthetic Content (provenance, watermarking, labeling).
  - **AI 100-5** — Plan for Global Engagement on AI Standards.
  - **SP 1270** — Towards a Standard for Identifying & Managing **Bias in AI** (systemic, computational/statistical, human-cognitive).
- **Related NIST ecosystem:** the **Dioptra** open-source adversarial-ML test platform; the **ARIA** (Assessing Risks and Impacts of AI) evaluation program; and the former **US AI Safety Institute (USAISI)** housed in NIST — **renamed in June 2025 to the Center for AI Standards and Innovation (CAISI)** with its mission re-centered on standards development, pre-deployment evaluations, and international standards engagement (post-rescission of EO 14110). Mention-level only.

### Why the RMF matters legally (the bridges)

- **Colorado AI Act (SB 24-205):** compliance with the NIST AI RMF (or ISO 42001, or another nationally/internationally recognized framework identified by the AG) supports the **rebuttable presumption of reasonable care** against algorithmic-discrimination claims.
- Referenced across US federal **agency AI guidance and procurement** (OMB M-24-10 for federal agencies survived EO changes in substance via M-25-21/-22; DoD RAI strategy; sector regulators) — the de facto US governance vocabulary even after EO 14110 was rescinded in Jan 2025 and partially replaced by **EO 14179** ("Removing Barriers to American Leadership in AI") and the **AI Action Plan (July 2025)**.
- **Crosswalks** to ISO/IEC 42001, ISO/IEC 23894, the EU AI Act, OECD, and Singapore's AI Verify — connective tissue for one-program-many-laws compliance (Lesson 12).
- Contrast anchor for the exam: **EU AI Act = binding product law; NIST RMF = voluntary process framework** — they answer different questions and pair well.
- **Flux warning:** federal AI policy in the US shifted materially in 2025. The RMF *itself* was not withdrawn and remains the reference framework; what moved is the EO/OMB layer above it. Treat exam questions as testing the RMF substance, not the political overlay.

## CASES & EXAMPLES

**Scenario 1 — Sort the activities.** A company: (a) adopts an AI policy assigning model-owner accountability; (b) documents the intended users and misuse potential of a new chatbot; (c) runs quarterly fairness metrics and red-team exercises; (d) decides the residual hallucination risk is acceptable for internal use only and writes an incident plan. *Analysis:* (a) GOVERN, (b) MAP, (c) MEASURE, (d) MANAGE — the canonical four-way sort the exam loves.

**Scenario 2 — The missing function.** A fintech has excellent testing dashboards and a mitigation backlog but no accountable executive, no policy, and no risk appetite statement; efforts stall in committee. *Analysis:* MEASURE and MANAGE exist without **GOVERN** — the cross-cutting function that makes the others stick. RMF answer: establish policies, roles/accountability lines, and risk tolerance first.

**Scenario 3 — GenAI profile in action.** A media company deploying an LLM assistant wants a structured risk review. *Analysis:* Apply the **Generative AI Profile**: work its GenAI risk list (confabulation, information integrity, prompt-injection/security, IP, human-AI over-reliance…), then use its suggested actions organized by GOVERN/MAP/MEASURE/MANAGE to build the target profile and gap plan.

**Scenario 4 — Regulatory payoff.** A Denver HR-tech deployer documents an RMF-aligned program (policies, context maps, bias measurements, treatment decisions, incident plans). *Analysis:* Under the Colorado AI Act, that alignment supports a rebuttable presumption of reasonable care in an algorithmic-discrimination action — voluntary framework, legal dividend.

## MEMORY HOOKS

- **Function mnemonic — "Good Managers Measure & Manage":** **G**OVERN (culture & accountability) → **M**AP (context & risk ID) → **M**EASURE (test & track) → **M**ANAGE (prioritize & respond).
- **One-word essences:** GOVERN = *culture* · MAP = *context* · MEASURE = *metrics* · MANAGE = *action*.
- **Trustworthy-7 mnemonic:** "**V**ery **S**mart **S**ystems **A**re **E**xplainable, **P**rivate & **F**air" → Valid/reliable, Safe, Secure/resilient, Accountable/transparent, Explainable/interpretable, Privacy-enhanced, Fair.
- **GOVERN is the odd one out:** cross-cutting and continuous — if the scenario smells of org charts, policies, or culture, the answer is GOVERN.
- **Risk formula flashcard:** risk = probability × magnitude, judged against *tolerance*, aiming at *prioritization* — never elimination.

**The 5 facts to retain:**
1. The AI RMF is a **voluntary**, sector-agnostic NIST framework (Jan 2023) to build trustworthy-AI risk management — process guidance, not law.
2. Four functions: **GOVERN** (cross-cutting culture/accountability), **MAP** (context and risk identification), **MEASURE** (TEVV, metrics, monitoring), **MANAGE** (prioritization, treatment, incident response, decommissioning).
3. Seven trustworthiness characteristics — valid/reliable, safe, secure/resilient, accountable/transparent, explainable/interpretable, privacy-enhanced, fair — with explicit trade-off management.
4. **Profiles** tailor the Core; the **Generative AI Profile (AI 600-1)** adds 12 GenAI-specific risks (confabulation, information integrity, prompt injection, IP…).
5. Legal bridges: Colorado's reasonable-care presumption, US agency practice, and crosswalks to ISO 42001/23894 and the EU AI Act make the RMF the interoperability hub.

## SELF-CHECK

1. **Q:** Name the four AI RMF functions and each one's purpose in a phrase.
   **A:** GOVERN — establish culture, policies, roles and accountability (cross-cutting); MAP — establish context and identify risks/impacts; MEASURE — analyze, test, benchmark and monitor risks; MANAGE — prioritize, treat, respond, and improve.

2. **Q:** Which function owns each: vendor-AI risk policy; deciding to accept residual risk; framing intended purpose and foreseeable misuse; bias-metric selection?
   **A:** Vendor policy — GOVERN; risk acceptance — MANAGE; intended purpose/misuse framing — MAP; metric selection — MEASURE.

3. **Q:** List the seven trustworthy-AI characteristics and note the one NIST treats as the baseline precondition.
   **A:** Valid & reliable (the precondition), safe, secure & resilient, accountable & transparent, explainable & interpretable, privacy-enhanced, fair with harmful bias managed.

4. **Q:** What is a profile, and what does the Generative AI Profile add?
   **A:** A tailored application of the RMF Core to a use case/sector/technology, comparing current vs target states. The GenAI Profile (NIST AI 600-1) identifies twelve risks unique to or amplified by generative AI — e.g., confabulation, information integrity, information security/prompt injection, IP, CBRN uplift — with actions mapped to the four functions.

5. **Q:** Contrast the NIST AI RMF with the EU AI Act in two dimensions.
   **A:** Bindingness: RMF is voluntary guidance; the AI Act is enforceable law with penalties. Mechanism: RMF is a process/culture framework applicable to any AI; the Act is risk-tiered product regulation with pre-market conformity for high-risk systems. (They interlock: RMF practice evidences AI Act-style compliance and earns Colorado's presumption.)
