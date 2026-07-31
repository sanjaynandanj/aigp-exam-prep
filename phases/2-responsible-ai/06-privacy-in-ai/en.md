# Privacy in AI: Data Protection Principles Applied to Models

**Phase 2 · Lesson 06 · ~1h · BoK Domain I**

## EXAM FOCUS

Domain I — privacy concepts as they collide with AI (the *legal* GDPR mechanics come in Phase 3; here it's the conceptual layer). Tested on: the tension between data-protection principles and ML's data appetite, model memorization/leakage as a privacy phenomenon, and **PETs at name level** (differential privacy, federated learning, synthetic data — recognize, define in one line, match to use case). A favorite stem: "which PET fits this constraint?"

## CORE

### The core collision

Classical data-protection principles (FIPs → GDPR and cousins) assume data is collected for a purpose, used for it, and deleted. Machine learning wants the opposite:

| Principle | What it demands | What ML wants | The friction |
|---|---|---|---|
| **Minimization** | Collect/process only what's necessary | More data ≈ better models | "Necessary for what?" — necessity is arguable when more data always helps a little |
| **Purpose limitation** | Use data only for specified, compatible purposes | Repurpose everything as training data | Data collected to run a service quietly becomes fuel for model building — compatibility analysis required |
| **Storage limitation** | Delete when no longer needed | Keep corpora for retraining, reproducibility, audits | Retention schedules vs "we might retrain" |
| **Accuracy** | Keep personal data correct | Tolerates noisy data statistically | Individual inaccuracies still harm individuals in individual decisions |
| **Individual rights** (access, erasure, objection) | Honor per-person control | Data is baked into weights | Can you delete a person *from a model*? (see below) |

Governance takeaway: these tensions are managed, not dissolved — via purpose decisions made *before* training, minimization by design (do you need raw identifiers? full text?), retention rules for corpora, and the PETs below.

### Memorization and leakage — the model *is* a data risk

Models, especially large ones, can **memorize** training examples and later emit or reveal them. The named phenomena (recognition level):

| Phenomenon | What happens |
|---|---|
| **Training-data extraction / regurgitation** | Research has demonstrated verbatim recovery of training text (including personal contact details) from LLMs via crafted prompts |
| **Membership inference attack** | Attacker determines *whether a given person's record was in the training set* — itself a privacy breach (e.g., membership in a clinical dataset implies a diagnosis) |
| **Model inversion / attribute inference** | Reconstructing or inferring sensitive attributes of training subjects from model behavior |

Consequences: the trained model may itself constitute or contain personal data; **erasure is hard** — removing a person from a model may require retraining or "machine unlearning" (immature); overfit models leak more (link to Lesson 1.07); and *inference outputs* create new personal data too (a model *inferring* health status manufactures sensitive data about a user who never disclosed it).

### PETs — privacy-enhancing technologies, name level

| PET | One-line mechanism | Fits when | Honest limits |
|---|---|---|---|
| **Differential privacy (DP)** | Add calibrated statistical noise so results barely change whether any one individual is in the data — a provable, tunable guarantee (the "privacy budget," ε) | Publishing statistics; training models with formal privacy guarantees (DP-SGD); used by, e.g., the US Census Bureau (2020) | Privacy–accuracy trade-off; guarantees are per the math, not per marketing — "we use DP" needs parameters |
| **Federated learning** | Train across many devices/sites; raw data never leaves its source — only model updates travel | Data can't move (hospitals, banks, phones): keyboards' next-word models are the classic deployment | Updates can still leak (hence often combined with DP/secure aggregation); orchestration complexity |
| **Synthetic data** | Generate artificial records mimicking real data's statistics for training/testing/sharing | Sharing "data-like" material with vendors, testing, augmenting rare classes | If too faithful, it re-leaks real individuals; if not, it distorts — utility/privacy tension; quality must be validated |
| *(also name-check)* Anonymization/pseudonymization, encryption in use (homomorphic, secure enclaves/multi-party computation) | Traditional and cryptographic families | — | Re-identification risk haunts "anonymized" high-dimensional data |

Matching heuristic for exams: *formal guarantee wanted → DP; data cannot move → federated; need shareable stand-in data → synthetic.*

### Privacy across the AI lifecycle

| Stage | Privacy questions |
|---|---|
| Sourcing/training | Lawful basis for corpus, scraping legitimacy, sensitive categories present?, minimization, DPIA triggers |
| Model | Memorization testing, membership-inference resistance, DP training? |
| Deployment | User inputs (prompts!) as personal data, inference outputs creating new data, logging retention |
| Rights handling | Access/erasure against datasets *and* models; explanation duties for automated decisions |

## CASES & EXAMPLES

1. **The scraped-faces company.** Clearview AI built a face-recognition database from billions of scraped web photos and sold search access to police. Multiple data-protection authorities (across the EU) and other regulators found violations and issued fines/orders; it became the emblem of "publicly available ≠ free to process." Concepts hit: purpose limitation, lawful basis, biometric sensitivity.

2. **Extraction demonstrated.** Published research (Carlini et al.) showed LLMs can regurgitate memorized training text, including personal details, under crafted prompting. Governance translation: leakage testing belongs in model evaluation, and "the data is only in the weights" is not a privacy defense.

3. **The keyboard that learns without taking.** Mobile keyboards improve next-word prediction via federated learning: the model trains on-device; only aggregated updates return. Standard exemplar for "data cannot leave the device" — pair with DP/secure aggregation as the belt-and-suspenders answer.

4. **Exam-style PET matcher.** "A hospital consortium wants to co-train a model but no site may share patient records." → federated learning. "An agency must publish neighborhood statistics with a provable bound on individual disclosure." → differential privacy. "A vendor needs realistic test records without exposure of real customers." → synthetic data (with validation of both fidelity and leakage).

## MEMORY HOOKS

**The collision in one line:** *data protection says less, later, narrower; ML says more, forever, for anything.*

**Leakage trio:** *extract* (get records out), *member* (was she in it?), *invert* (reconstruct attributes).

**PET picker:** **D**P = provable noise · **F**ederated = data stays home · **S**ynthetic = convincing stand-ins. ("DFS")

The 5 facts to retain:

1. Minimization and purpose limitation collide head-on with training appetite; managing that collision is a *pre-training* governance decision.
2. Models memorize: extraction, membership inference, and inversion make the model itself a personal-data risk — test for it.
3. Erasure from a trained model is genuinely hard (retraining/unlearning) — a rights-handling problem unique to AI.
4. DP = formal noise-based guarantee (Census-grade); federated = train where data lives; synthetic = statistical stand-ins with a fidelity/leakage tension.
5. Prompts in and inferences out are both personal data events at deployment time — privacy doesn't end at training.

## SELF-CHECK

1. Name three data-protection principles and the specific way ML strains each.
2. Distinguish a membership inference attack from training-data extraction.
3. Why is the right to erasure uniquely difficult against a trained model?
4. Pick the PET and justify: three banks want a joint fraud model but cannot pool customer data.
5. What two privacy-relevant data events happen at inference time with a public chatbot?

<details>
<summary>Answers</summary>

1. Minimization vs more-data-is-better; purpose limitation vs repurposing collected data as training fuel; storage limitation vs indefinite corpus retention (also accuracy vs noise tolerance; rights vs data baked into weights).
2. Membership inference reveals *whether* a person's record was in the training set (the fact of inclusion is the leak); extraction recovers the *content* of training records from the model's outputs.
3. The person's data is distributed into learned weights, not stored as a deletable record — honoring erasure may require retraining or machine-unlearning techniques that remain immature.
4. Federated learning — the constraint is that raw data cannot move across institutions; each bank trains locally and shares only model updates (ideally with secure aggregation/DP on top).
5. Users' prompts are collected/processed personal data (and may contain third parties' data); the model's outputs may *infer/create new* personal — even sensitive — data about individuals.

</details>
