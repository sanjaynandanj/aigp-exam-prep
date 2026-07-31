# Testing & Evaluation: Accuracy, Robustness, Fairness, Red Teaming

**Phase 5 · Lesson 05 · ~1.5h · BoK Domain III**

## EXAM FOCUS

High-yield lesson. The exam tests: reading a confusion matrix at concept level, choosing the right metric for a context (precision vs recall is a classic stem), what robustness and fairness testing add beyond accuracy, what red teaming is and when it's used, why benchmarks mislead, and the role of pre-defined acceptance criteria. You need governance-level fluency, not math.

## CORE

### The confusion matrix and core metrics

For a binary classifier, four outcomes:

| | Predicted positive | Predicted negative |
|---|---|---|
| **Actually positive** | True positive (TP) | False negative (FN) |
| **Actually negative** | False positive (FP) | True negative (TN) |

| Metric | Formula (concept) | Plain meaning | Optimize when… |
|---|---|---|---|
| **Accuracy** | (TP+TN)/all | Share of all predictions correct | Classes are balanced and errors cost the same (rare) |
| **Precision** | TP/(TP+FP) | When it says "positive," how often is it right? | False positives are costly (e.g., fraud accusations, spam-flagging legit mail) |
| **Recall (sensitivity)** | TP/(TP+FN) | Of the real positives, how many did it catch? | False negatives are costly (e.g., cancer screening, safety threats) |
| **F1** | Harmonic mean of precision & recall | Single balance score | You need one number balancing both error types |
| **AUC (ROC)** | Area under the ROC curve | Ranking quality across all thresholds | Comparing models before choosing an operating threshold |

Governance insight: **accuracy alone misleads under class imbalance** (a model predicting "no fraud" always is 99% accurate if 1% of cases are fraud). The threshold choice — trading precision against recall — is a *policy decision about whose errors matter*, and belongs to accountable humans, not just engineers.

### Beyond average performance

| Test type | Question it answers | Typical methods |
|---|---|---|
| **Robustness** | Does it hold up under noise, edge cases, distribution shift, adversarial inputs? | Perturbation/stress tests, out-of-distribution sets, corrupted inputs |
| **Fairness across subgroups** | Does performance/error distribution differ across protected or salient groups? | Disaggregated metrics per subgroup, fairness metrics (e.g., comparing selection or error rates), per-group confusion matrices |
| **Red teaming / adversarial testing** | What can a motivated adversary or misuse make it do? | Structured attack exercises: jailbreaks/prompt injection for LLMs, evasion attempts, harmful-content elicitation, misuse scenarios |
| **Safety/security testing** | Does it fail dangerously? Can it be exploited? | Overlaps with Lesson 08 threat classes |

Fairness testing requires subgroup labels — which may themselves be sensitive data; collecting them for bias testing needs a lawful pathway (link back to Lesson 03).

**Red teaming** is deliberately adversarial, exploratory, human-driven testing — it finds what scripted test suites miss. It is prominent in GPAI/frontier-model governance (model evaluations and adversarial testing are core expectations for systemic-risk GPAI under the EU AI Act's GPAI provisions, and in voluntary commitments like the G7/White House-era frontier safety pledges).

### Benchmark limits

Public benchmarks (leaderboard scores) are weak governance evidence because of:

- **Contamination** — benchmark items may appear in training data, inflating scores.
- **Construct gap** — a benchmark measures the benchmark, not your deployment task/population.
- **Goodhart effect** — optimizing the metric degrades what it proxied ("when a measure becomes a target…").
- **Static snapshots** — real-world data drifts; benchmarks don't.

Rule: benchmarks may inform model *selection*; deployment decisions need **context-specific evaluation on data representative of the intended use**.

### Acceptance criteria

Define **before** testing: metrics, thresholds, subgroups, robustness cases, and required evidence — tied to the risk tier from intake. Pre-registration prevents "moving the goalposts" after results arrive. Test results vs acceptance criteria form the heart of the release-gate evidence bundle (Lesson 09). Independence matters: evaluators should be organizationally separate from builders for higher-risk systems.

## CASES & EXAMPLES

**Scenario 1 — metric choice.** A hospital deploys a sepsis early-warning model. Which error is worse? Missing a septic patient (FN). *Best answer:* prioritize recall/sensitivity, accepting more false alarms — then manage alarm fatigue via oversight design. A distractor will push "maximize accuracy."

**Scenario 2 — imbalance trap.** A fraud model shows 99.2% accuracy; the team wants to ship. Fraud is 0.5% of transactions. *Exam point:* accuracy is uninformative under imbalance — demand precision/recall (or the confusion matrix) before any release decision.

**Scenario 3 — subgroup failure.** A face-analysis system performs well on aggregate but far worse for darker-skinned women — the pattern documented in the Gender Shades research on commercial gender classifiers. *Exam point:* aggregate metrics hide subgroup harm; disaggregated evaluation is the control that catches it.

**Scenario 4 — red team before launch.** Before releasing a customer-facing LLM assistant, a bank runs a structured exercise where testers try prompt-injection, data-exfiltration prompts, and harmful financial advice elicitation. *Exam point:* that is red teaming — adversarial, exploratory, pre-release — distinct from scripted regression tests; findings feed the go/no-go review.

## MEMORY HOOKS

**Precision vs recall:** *Precision = "when I point, am I right?" Recall = "did I find them all?"* Spam filter → precision; cancer screen → recall.

**Benchmark caution — "CCGS": Contamination, Construct gap, Goodhart, Static.**

**Testing ladder:** *Accuracy → Robustness → Fairness → Red team* — each rung answers a question the previous one can't.

The 5 facts to retain:

1. Accuracy misleads under class imbalance; precision (FP-costly contexts) and recall (FN-costly contexts) express whose errors matter — a policy choice.
2. F1 balances precision/recall; AUC compares ranking quality across thresholds before an operating point is set.
3. Fairness testing means disaggregating performance by subgroup; aggregate scores can conceal severe subgroup failure.
4. Red teaming is human-driven adversarial testing for misuse/jailbreaks/edge behavior — expected for high-risk and systemic-risk GPAI models.
5. Acceptance criteria (metrics, thresholds, subgroups) are fixed *before* testing, scaled to risk tier, and become the release-gate evidence.

## SELF-CHECK

1. **A model flags employees for security investigation. Which metric matters most and why?**
   Precision — false positives wrongly subject people to investigation; when the model points, it must be right. (Recall matters too, but FP harm dominates the stem.)
2. **Why is 99% accuracy potentially meaningless?**
   Under class imbalance, always predicting the majority class yields high accuracy while catching zero positives — check the confusion matrix.
3. **What does fairness testing require that aggregate evaluation does not?**
   Subgroup membership data and per-subgroup (disaggregated) metrics — comparing performance and error rates across groups.
4. **Give three reasons public benchmarks are weak deployment evidence.**
   Training-data contamination, gap between benchmark task and deployment context, Goodhart-style over-optimization (and benchmarks are static while reality drifts).
5. **When should acceptance criteria be defined, and why?**
   Before evaluation begins — pre-registration prevents post-hoc goalpost-moving and gives the release gate an objective pass/fail standard.
