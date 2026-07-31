# Monitoring in Production: Drift, Performance Decay, Feedback Loops

**Phase 6 · Lesson 04 · ~1.5h · BoK Domain IV**

## EXAM FOCUS

Core Domain IV territory. You must distinguish the drift types (data drift vs concept drift; label/prediction drift as signals), explain why models decay without code changes, recognize feedback loops, and know the governance machinery: thresholds → alerts → investigation → retraining triggers → re-validation before redeploy. Also tested: logging duties at concept level (EU AI Act high-risk systems must support automatic event logging; deployers retain logs under their control).

## CORE

### Why models decay

Traditional software fails when code changes; **models fail when the world changes.** A model is a frozen snapshot of historical patterns — as reality moves, silent degradation begins. Monitoring is the deployer-side control that makes degradation visible.

### The drift taxonomy

| Type | What changes | Example | Detection signal |
|---|---|---|---|
| **Data drift (covariate shift)** | Input distribution P(X) | New customer demographic; sensor replaced; new slang in text | Statistical distance between live and training input distributions |
| **Concept drift** | The X→Y relationship itself | Fraud tactics evolve; pandemic rewrites purchasing behavior | Rising error once ground truth arrives; pattern breaks |
| **Label/prior shift** | Outcome base rate P(Y) | Default rates rise in recession | Outcome frequency vs training baseline |
| **Prediction drift** (symptom) | Distribution of model outputs | Approval rate slides from 60% to 45% with no policy change | Output distribution monitoring — an early proxy when labels are delayed |

Key subtlety: **ground truth is often delayed** (loan defaults take months to observe), so programs monitor input and prediction distributions as leading indicators, and true performance as a lagging indicator.

### What to monitor

| Layer | Metrics |
|---|---|
| System | Latency, availability, error rates |
| Data | Input distributions, missing/out-of-range values, schema changes |
| Model | Performance vs acceptance criteria (as labels arrive), confidence distributions, prediction drift |
| Fairness | Subgroup performance and outcome rates over time — bias can *emerge* in production even if launch testing was clean |
| Usage | Volumes, override/rejection rates by human overseers (an oversight-health signal), out-of-scope use |

### Feedback loops

A feedback loop arises when the model's outputs shape its own future inputs:

- **Self-fulfilling:** predictive policing sends patrols where crime was recorded → more arrests recorded there → model grows more confident in the same areas.
- **Selective labels:** a credit model only observes repayment for approved applicants — the rejected are never labeled, so errors on them are invisible and get baked into retraining data.
- **Degenerate loops (GenAI):** model outputs published to the web get scraped into future training data.

Governance responses: recognize the loop at design time, retain holdout/exploration data, audit outcomes for the *unselected* population where possible, and treat "model performance looks great" with suspicion when the model controls its own evidence.

### Thresholds, retraining triggers, and re-validation

- **Alert thresholds** are set *before* launch (release-gate deliverable): metric floors, drift-distance ceilings, fairness-gap limits — each with a severity and an owner. Untuned thresholds produce alert fatigue; unowned alerts produce ignored ones.
- **Retraining triggers:** scheduled (periodic refresh) and/or conditional (threshold breach). Both are governance decisions, not just engineering ones.
- **Re-validation rule:** a retrained model is a **new model version** — it re-passes evaluation against acceptance criteria and (for material changes) the release gate before serving users (Phase 5 L01/L09 loop). Automatic continuous retraining without gated validation is an exam-flagged anti-pattern for high-risk systems.

### Logging duties (concept level)

The EU AI Act requires high-risk systems to be technically capable of **automatic event logging** over their lifetime (traceability of operation), and **deployers must retain the logs under their control** for an appropriate period (the Act anchors a minimum period concept — at least six months, subject to other applicable law). Logs serve: incident forensics, monitoring evidence, regulator requests, and audit trails linking each decision to a model version (the lineage discipline of Phase 5 L04 extended into operations).

## CASES & EXAMPLES

**Scenario 1 — name the drift.** A demand-forecasting model trained pre-2020 collapses when lockdowns transform buying behavior: the relationship between historic features and demand itself changed. *Answer:* concept drift. If instead a new sales channel merely shifted the customer mix while relationships held, that's data drift.

**Scenario 2 — silent decay.** A résumé screener's shortlists slowly skew as applicant language norms evolve; no alert fires because only accuracy-on-old-test-data was ever checked, and nobody monitors production distributions. *Failed control:* production drift monitoring with thresholds — offline test results age; monitoring is the control that notices.

**Scenario 3 — the loop.** A hospital readmission model directs extra care to high-risk patients; their readmissions drop; a naive retrain "learns" those patient profiles are low-risk. *Exam point:* intervention feedback — the model's own success contaminates its labels; retraining data must account for the intervention.

**Scenario 4 — logs, whose duty?** After a contested automated decision, a regulator asks the deploying bank for operation logs. The bank says "the vendor keeps those." *Exam point:* deployers must retain logs *under their control* (Art. 26 concept) — log access/retention should have been contracted (Lesson 03) and operationalized at readiness (Lesson 01).

## MEMORY HOOKS

**Drift contrast:** *Data drift = the inputs moved. Concept drift = the meaning moved.* (Prediction drift = the smoke alarm; performance drop = the fire, confirmed late.)

**Decay one-liner:** *Models don't break — the world walks away from them.*

**Retrain rule:** *Retrained = new version = re-test = re-gate.*

The 5 facts to retain:

1. Data drift changes input distributions; concept drift changes the input-outcome relationship; prediction drift is the early symptom monitored when ground truth lags.
2. Monitor four layers — system health, data quality/distributions, model performance, and subgroup fairness — because bias can emerge post-launch.
3. Feedback loops (self-fulfilling predictions, selective labels) let models corrupt their own evidence; design monitoring and retraining data to counter them.
4. Alert thresholds and retraining triggers are pre-defined governance artifacts with owners; retrained models re-pass validation and gating before redeployment.
5. EU AI Act concept: high-risk systems must log events automatically; deployers retain logs under their control (minimum-period concept, at least six months) as traceability and audit evidence.

## SELF-CHECK

1. **Distinguish data drift from concept drift with one example each.**
   Data drift: input distribution shifts while relationships hold (new demographic starts using the product). Concept drift: the input→outcome relationship changes (fraudsters change tactics, so old fraud signatures stop predicting fraud).
2. **Why monitor prediction distributions at all if what we care about is accuracy?**
   Ground truth often arrives late (defaults, outcomes); prediction drift is a leading indicator that flags trouble while accuracy metrics are still blind.
3. **Explain the "selective labels" problem in a credit model.**
   Only approved applicants generate repayment labels; the model never learns its errors on rejected applicants, so those errors persist and re-enter retraining data unchallenged.
4. **What must happen between a retraining trigger firing and the new model serving customers?**
   Re-evaluation against acceptance criteria (including fairness/robustness) and passage through the appropriate release gate — the retrained artifact is a new, versioned model.
5. **State the two halves of the EU AI Act logging concept.**
   Providers must build high-risk systems capable of automatic event logging (traceability); deployers must retain the logs under their control for an appropriate minimum period (at-least-six-months concept).
