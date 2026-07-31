# DPIAs for AI Systems; GDPR Fines & Enforcement Patterns Against AI

**Phase 3 · Lesson 03 · ~1h · BoK Domain II**

## EXAM FOCUS

Two testable clusters: (1) **when a DPIA is mandatory** for an AI system and what it must contain, including how it differs from and complements AI-specific assessments; (2) **the pattern of EU enforcement against AI** — what regulators actually sanction (no valid lawful basis, scraping biometrics, no transparency, children's data) so you can recognize the violation category in a scenario. You don't need to memorize fine amounts; you need to recognize *which obligation was breached*.

## CORE

### When is a DPIA required? (Art. 35)

A DPIA is mandatory when processing is **"likely to result in a high risk to the rights and freedoms of natural persons"**, and Art. 35(3) gives three automatic triggers — all three map naturally onto AI:

| Art. 35(3) trigger | Typical AI example |
|---|---|
| **(a)** Systematic and extensive **evaluation based on automated processing, including profiling**, with legal/significant effects | Credit scoring models, algorithmic hiring, insurance risk models |
| **(b)** Large-scale processing of **special-category** or criminal-offense data | Health-diagnosis models, biometric identification systems |
| **(c)** Systematic **monitoring of publicly accessible areas** on a large scale | Facial recognition CCTV, smart-city analytics |

Supervisory authorities also publish lists of high-risk operations; common list items that catch AI: **innovative use of new technologies**, matching/combining datasets, data on vulnerable subjects (children, employees), and processing that prevents people from exercising rights or accessing services. EDPB rule of thumb: **two or more risk criteria → do a DPIA**. In practice, *almost any consequential AI system processing personal data warrants one*.

### DPIA required content (Art. 35(7))

1. **Systematic description** of the processing and its purposes (for AI: data sources, model function, decision logic, recipients);
2. **Necessity and proportionality** assessment;
3. **Assessment of risks** to rights and freedoms (not just privacy — discrimination, exclusion, chilling effects);
4. **Mitigation measures**, safeguards, and security to bring risk down.

Consult the **DPO** where designated. If residual risk stays high after mitigation → **prior consultation** with the supervisory authority (Art. 36) before processing starts. DPIAs are **living documents** — revisit on model retraining, new data sources, or purpose changes.

### DPIA vs AI-specific assessments

| Dimension | **DPIA (GDPR)** | **AI impact assessment / FRIA-type** | **Conformity assessment (EU AI Act)** |
|---|---|---|---|
| Trigger | High-risk *personal data* processing | Organizational policy, or law (e.g., AI Act FRIA for certain deployers; Colorado AIA impact assessments) | Placing a high-risk AI system on the EU market |
| Lens | Rights and freedoms of data subjects | Broader: fundamental rights, fairness, safety, societal effects — even with no personal data | Technical/legal conformity with product requirements |
| Who | Controller | Developer and/or deployer | Provider (mostly) |
| Overlap | One exercise can feed the others; the AI Act expressly lets deployers build a FRIA on top of an existing DPIA | | |

Exam angle: a DPIA is **not** automatically satisfied by an AI Act conformity assessment or vice versa — they are complementary, and well-run programs integrate them.

### EU enforcement patterns against AI (described generically and accurately)

| Pattern | What happened | Lesson tested |
|---|---|---|
| **Facial-recognition scraping** | A US facial-recognition company that scraped billions of face images from the web was fined by multiple EU DPAs (Italy, Greece, France, UK ~€20M-scale each, plus orders to delete data and repeated non-compliance penalties) | No lawful basis, biometric special-category data, extraterritorial reach of GDPR (Art. 3(2) targeting/monitoring), ignoring orders compounds liability |
| **Chatbot / LLM providers** | The Italian Garante temporarily suspended a major generative-AI chatbot (2023) over lawful basis, transparency, accuracy, and age verification; later imposed a €15M fine; similar scrutiny hit an AI companion app and other LLM services | Regulators can act *fast* using urgency powers; training-data legality and children's protections are enforcement priorities |
| **Biometric categorization & emotion claims** | DPAs and the EDPB have condemned scraping for biometric databases and questioned emotion-recognition claims | "Publicly available" is no defense; scientific validity feeds fairness analysis |
| **Workplace algorithmic management** | Fines against delivery-platform algorithms (e.g., Italian actions against gig-work rating algorithms) for opaque automated management and discrimination risk | Art. 22 + fairness + transparency in employment contexts |
| **Children and recommender systems** | Large fines to social platforms concerning children's data and design | Vulnerable subjects raise the risk bar and DPIA necessity |

### Fine architecture (know the tiers, not each case)

- Up to **€20M or 4% of global annual turnover** (whichever higher): violations of principles, lawful basis, data subject rights, transfers.
- Up to **€10M or 2%**: controller/processor operational duties (security, DPIA failures, records, breach notification).
- Plus corrective powers that often hurt more than fines: **processing bans, deletion orders (including trained-on data), suspension orders**. "Delete the model/data" orders are the GDPR cousin of algorithmic disgorgement.

## CASES & EXAMPLES

**Scenario 1 — Skipped DPIA.** A hospital deploys a triage-prediction model on patient records without a DPIA, reasoning "we already did an AI ethics review." *Analysis:* Large-scale special-category processing → DPIA mandatory under Art. 35(3)(b). An ethics review doesn't satisfy Art. 35's content requirements; the DPIA failure itself is finable (2% tier) independent of any substantive harm.

**Scenario 2 — Residual high risk.** A city's DPIA for public-space crowd analytics concludes risks remain high even after mitigations, but the project proceeds anyway. *Analysis:* Art. 36 requires **prior consultation** with the supervisory authority before processing when residual risk is high — proceeding without it is the exam-flagged error.

**Scenario 3 — The scraping vendor.** A vendor tells an EU customer that GDPR doesn't apply to it because it's US-based and only scrapes public photos. *Analysis:* Art. 3(2) extends GDPR to non-EU controllers monitoring behavior of people in the EU; biometric templates for identification are special-category data; multiple DPAs have fined precisely this model and ordered deletion.

## MEMORY HOOKS

- **DPIA triggers mnemonic — "SLS":** **S**ystematic profiling with significant effects, **L**arge-scale special categories, **S**urveillance of public spaces.
- **DPIA content — "DNRM":** **D**escription, **N**ecessity/proportionality, **R**isk assessment, **M**itigations. ("Do Not Risk Models.")
- **High residual risk → phone the regulator first** (Art. 36 prior consultation).
- **Enforcement pattern in one line:** regulators attack AI through *lawful basis + transparency + special categories + children*, and their sharpest weapon is the **order to stop and delete**, not the fine.

**The 5 facts to retain:**
1. Consequential AI on personal data almost always requires a DPIA; profiling with significant effects and large-scale special-category data are automatic triggers.
2. DPIA = description, necessity/proportionality, risk assessment, mitigations — a living document revisited on retraining/purpose change.
3. High residual risk after mitigation → mandatory prior consultation with the DPA before going live.
4. DPIA, AI impact assessment, and AI Act conformity assessment are **complementary, not substitutes**.
5. EU enforcement against AI clusters around unlawful scraping/biometrics, transparency failures, and children's data — with deletion/suspension orders as the signature remedy.

## SELF-CHECK

1. **Q:** Name the three Art. 35(3) automatic DPIA triggers and give one AI example of each.
   **A:** (a) systematic extensive automated evaluation/profiling with significant effects — algorithmic credit scoring; (b) large-scale special-category or criminal data — medical diagnostic models; (c) large-scale systematic monitoring of public areas — facial-recognition CCTV.

2. **Q:** What must a controller do if a DPIA shows high residual risk despite mitigations?
   **A:** Consult the supervisory authority under Art. 36 *before* commencing the processing.

3. **Q:** Does completing an EU AI Act conformity assessment remove the need for a GDPR DPIA?
   **A:** No — they serve different legal tests (product conformity vs. data subjects' rights). They can share evidence, but each must be satisfied where triggered.

4. **Q:** What recurring GDPR violations underpin EU enforcement against facial-recognition scraping companies?
   **A:** No lawful basis (Art. 6/9) for biometric special-category data, lack of transparency, disregard of data subject rights, plus extraterritorial applicability via Art. 3(2); non-compliance with orders added further penalties.

5. **Q:** Which fine tier applies to failing to conduct a required DPIA, and what non-monetary remedy should organizations fear more?
   **A:** The 2%/€10M tier (operational obligations). The more feared remedies are corrective orders — processing bans and orders to delete unlawfully processed data (potentially including trained models).
