# Training vs Inference; Overfitting, Drift, and the Black-Box Problem

**Phase 1 · Lesson 07 · ~1h · BoK Domain I**

## EXAM FOCUS

Domain I — the model lifecycle's two phases and their distinct risks, plus the failure vocabulary (overfitting, underfitting, three kinds of drift) that Domain IV monitoring scenarios assume you know. Tested both as recall (define concept drift) and scenario (production accuracy sagged after a market shock — name the phenomenon and the response). Learn the drift taxonomy cold; it is among the most reliably tested items in this phase.

## CORE

### Two phases, two risk profiles

| | **Training** (building the model) | **Inference** (using the model) |
|---|---|---|
| What happens | Model learns weights from historical data | Frozen model produces outputs on new inputs |
| When | Episodic — before deployment (and at retraining) | Continuous — every prediction in production |
| Data involved | Large historical datasets | Live, individual inputs |
| Characteristic risks | Data bias baked in, poisoning, privacy of training subjects, copyright, label errors, compute cost | Wrong/harmful individual outputs, drift, adversarial inputs, privacy of *users*, latency/availability, misuse |
| Governance instruments | Data governance, dataset docs, training documentation, evaluation gates (Phase 5) | Monitoring, logging, human oversight, incident response (Phase 6) |

Why the split matters: **errors created at training time surface at inference time**, often much later and on real people. Governance therefore needs controls at *both* phases — pre-deployment gates cannot catch what only production reveals, and monitoring cannot fix what training baked in.

### Overfitting and underfitting

| Failure | What it is | Symptom | Intuition |
|---|---|---|---|
| **Overfitting** | Model memorizes training data's noise and quirks instead of learning general patterns | Excellent on training data, poor on new data | The student who memorized past exams and fails a fresh one |
| **Underfitting** | Model too simple to capture the real pattern | Poor on training *and* new data | The student who only skimmed the summary |

Standard safeguard: evaluate on **held-out data** the model never trained on (test/validation sets). Governance echo: a vendor quoting accuracy "on our training data" is quoting a near-meaningless number — always ask for held-out (ideally out-of-sample, out-of-time) performance. Overfitting also connects to privacy: a model that memorized training examples can *leak* them (Phase 2, Lesson 06).

### Drift: the three kinds

Models are trained on the past; the world moves. "Drift" is the family of ways reality walks away from the training snapshot:

| Type | What changes | Example |
|---|---|---|
| **Data drift** (input/covariate drift) | The distribution of *inputs* | A credit model trained pre-pandemic sees post-pandemic income patterns; new phone models change photo characteristics for a vision system |
| **Concept drift** | The *relationship* between inputs and the outcome | Fraudsters change tactics, so yesterday's fraud signature no longer predicts fraud; consumer behavior shifts what "likely to churn" looks like |
| **Model drift / performance decay** | The observed result: the model's accuracy degrades over time | The umbrella symptom the first two produce |

Memory discipline: *data drift = the questions changed; concept drift = the answers changed.* Response toolkit (Domain IV): monitor input distributions and outcome metrics, set alert thresholds, retrain on fresh data, and define when degradation triggers human review or suspension.

### The black-box problem, restated precisely

From Lesson 03: deep models' knowledge lives in millions of uninterpretable weights. Precise formulation for exam purposes: **the inability to trace a specific output to human-comprehensible reasons, even with full access to the model.** Distinguish two opacity sources:

1. **Technical opacity** — complexity itself (deep learning's intrinsic problem).
2. **Proprietary opacity** — the builder won't show you (trade secrets, vendor contracts).

Both frustrate oversight, contestability, and audit — but the *remedies differ*: technical opacity → explainability techniques, interpretable-model requirements, rigorous outcome testing; proprietary opacity → contractual audit rights, regulator access powers, documentation duties. Scenario questions often hinge on picking the remedy that matches the opacity type.

## CASES & EXAMPLES

1. **The pandemic and the models.** In 2020, consumer-behavior shifts degraded fraud, credit, and demand-forecasting models across industries — a mass, simultaneous drift event. Systems kept confidently producing outputs calibrated to a vanished world. Takeaways: drift is inevitable, monitoring is not optional, and "the model was fine at launch" is the beginning, not the end, of due diligence.

2. **The overfit medical model.** A diagnostic model shows stellar validation numbers — but its training and test data came from the same hospital's scanner. Deployed at a second hospital with different equipment, performance collapses (a distribution-shift failure that peer-reviewed medical-imaging studies repeatedly document). Governance lesson: demand evaluation on data that resembles the *deployment* environment, not just any held-out set.

3. **Vendor opacity scenario (exam style).** A deployer's high-risk hiring tool produces contested outcomes; the vendor refuses model detail citing trade secrets. What kind of opacity, and which remedies fit? → Proprietary opacity; remedies: contractual information/audit rights, documentation obligations flowing from provider to deployer (an EU AI Act design feature — Phase 4), or switching vendors — not SHAP charts, which address technical opacity.

4. **Fraud model gone stale.** Alert rates drop 40% in six months while confirmed fraud rises. Name it: concept drift (fraud tactics changed the input→outcome relationship). Correct response chain: investigate → retrain on recent labeled cases → tighten monitoring cadence; interim compensating control: increased human review sampling.

## MEMORY HOOKS

**Phase split:** *Training bakes it in; inference serves it up.* Errors born in training surface at inference, on real people.

**Overfit vs underfit:** memorized the past exam vs never studied.

**Drift triad:** **data** drift = questions changed; **concept** drift = answers changed; **model** drift = the grade slipping (the symptom).

The 5 facts to retain:

1. Training is episodic and bakes in risk (bias, poisoning, memorization); inference is continuous and surfaces it (drift, adversarial inputs, harmful outputs).
2. Overfitting = memorization → great training scores, poor real-world scores; catch it with held-out and out-of-time evaluation.
3. Data drift changes inputs; concept drift changes the input→outcome relationship; both show up as performance decay.
4. Drift makes monitoring + retraining a permanent obligation — accuracy at launch guarantees nothing.
5. Technical opacity and proprietary opacity are different problems with different remedies (XAI/testing vs audit rights/documentation).

## SELF-CHECK

1. List three risks characteristic of the training phase and three of the inference phase.
2. Define overfitting and name the standard method for detecting it.
3. A résumé screener's inputs look statistically unchanged, but its shortlist quality collapses because the role's success profile changed. Which drift is this?
4. Why is a vendor's "99% accuracy on training data" claim inadequate, twice over?
5. Distinguish the two sources of AI opacity and give one remedy for each.

<details>
<summary>Answers</summary>

1. Training: baked-in data/label bias, data poisoning, privacy/copyright issues in corpora (also label errors, memorization). Inference: drift/performance decay, adversarial or out-of-distribution inputs, harmful individual outputs (also user privacy, misuse, availability).
2. Learning training data's noise/quirks rather than generalizable patterns; detect by evaluating on held-out data the model never saw (ideally out-of-time/out-of-sample).
3. Concept drift — the relationship between the same inputs and the outcome changed.
4. Training-data accuracy is inflated by potential overfitting, and even honest held-out accuracy at one point in time says nothing about performance under deployment conditions and future drift.
5. Technical opacity (complexity) → explainability techniques, interpretable models, outcome testing. Proprietary opacity (secrecy) → contractual audit/information rights, mandatory documentation, regulator access.

</details>
