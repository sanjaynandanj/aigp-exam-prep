# The AI Lifecycle: Stages, Gates, and Where Governance Intervenes

**Phase 5 · Lesson 01 · ~1h · BoK Domain III**

## EXAM FOCUS

Domain III is built on one skeleton: the AI lifecycle. Nearly every Domain III question implicitly asks "which lifecycle stage is this, and what governance activity belongs there?" Expect recall questions on the canonical stage sequence, and scenario questions where you must place an activity (a DPIA, a red-team exercise, a drift alert) at the correct stage or spot a *missing gate* between stages. Learn the stages cold — every later Phase 5 and 6 lesson hangs off this map.

## CORE

### The canonical stages

There is no single mandated lifecycle, but governance frameworks (ISO/IEC 5338 for AI system lifecycle processes, the OECD's lifecycle framing used in its AI system definition work, and NIST AI RMF's lifecycle view) converge on the same arc:

| # | Stage | Core activity | Primary governance question |
|---|-------|---------------|------------------------------|
| 1 | **Plan / inception** | Define the problem, business case, success criteria | Should we build this at all? (necessity, proportionality, ban list) |
| 2 | **Design** | Architecture, model approach, oversight design, requirements | Are risk controls designed in, not bolted on? |
| 3 | **Data** | Collect, license, clean, label, document datasets | Is the data lawful, representative, fit for purpose? |
| 4 | **Build / train** | Train or fine-tune models, track experiments | Is development reproducible and documented? |
| 5 | **Test / evaluate (verify & validate)** | Accuracy, robustness, fairness, security testing against acceptance criteria | Does evidence show the system meets its criteria? |
| 6 | **Deploy / release** | Release decision, staged rollout, user notices | Who signed off, on what evidence? |
| 7 | **Operate & monitor** | Drift detection, incidents, oversight, logging | Is it still performing and still compliant? |
| 8 | **Retire / decommission** | Wind-down, data disposition, archival | Did we exit responsibly and keep the accountability record? |

Two cross-cutting truths the exam rewards:

- **The lifecycle is iterative, not linear.** Monitoring findings loop back to data and retraining; a failed test loops back to design. "Waterfall" answers are usually wrong.
- **Governance is continuous, but decisions are gated.** Risk management runs across all stages (NIST AI RMF, EU AI Act's continuous risk-management concept); formal *approvals* happen at the transitions.

### Governance gates at each transition

A **gate** is a defined decision point where the system cannot advance without evidence review and an accountable sign-off.

| Gate (transition) | Typical evidence reviewed | Typical decision-maker |
|---|---|---|
| Plan → Design | Use-case intake form, initial risk tier, legal screen | AI governance committee / intake reviewer |
| Design → Data/Build | Design review, DPIA/AIA trigger check, oversight plan | Governance lead + privacy + security |
| Build → Test | Training records, data documentation complete | Technical lead / model risk function |
| Test → Deploy | Test results vs acceptance criteria, impact assessment, docs bundle | **Go/no-go review board** (Lesson 09) |
| Deploy → Operate | Rollout results, monitoring plan live, rollback tested | Product owner + governance sign-off |
| Operate → Retire | Retirement plan, migration, archival plan | System owner + governance |

### Mapping to framework language

| Framework | How it frames the lifecycle |
|---|---|
| **ISO/IEC 5338** | AI-specific extension of software lifecycle processes (ISO/IEC 12207/15288 lineage): adds data-centric and continuous-learning processes |
| **OECD** | Lifecycle phases: design/data/models → verification & validation → deployment → operation & monitoring |
| **NIST AI RMF** | Lifecycle actors ("AI actors") mapped across design, development, deployment, operation; MAP early, MEASURE mid, MANAGE throughout, GOVERN over all |
| **EU AI Act** | Obligations attach by lifecycle position: providers dominate pre-market stages, deployers dominate use stage; risk management is a continuous, iterative process across the lifecycle |

## CASES & EXAMPLES

**Scenario 1 — the missing gate.** A retail bank's data science team builds a credit-scoring model and pushes it live because "accuracy beat the old model." Three months later a regulator asks who approved deployment; no record exists. *Exam point:* the failure is not the model — it is the absent Test → Deploy gate with accountable sign-off and an evidence bundle. Best answer usually: "establish a formal release gate with documented approval," not "retrain the model."

**Scenario 2 — placing the activity.** A hospital plans an AI triage tool. When should the fundamental-rights/impact assessment happen? *Best answer:* early — at plan/design, before significant build investment, and revisited before deployment. Distractors will offer "after deployment, once real data exists" — wrong, assessments are ex ante instruments.

**Scenario 3 — lifecycle loops.** A deployed fraud model's false-positive rate climbs. The team retrains on fresh data. *Exam point:* retraining re-enters the lifecycle at the data/build stages and must pass the test gate again before redeployment ("re-validation"). An answer that lets the retrained model ship without re-testing is a trap.

## MEMORY HOOKS

**Stage mnemonic — "People Don't Deliver Bad Tech; Diligent Owners Retire it":**
**P**lan → **D**esign → **D**ata → **B**uild → **T**est → **D**eploy → **O**perate → **R**etire.

**Gate rule of thumb:** *No transition without evidence + an accountable name.*

The 5 facts to retain:

1. Canonical arc: plan → design → data → build → test → deploy → operate/monitor → retire — iterative, with feedback loops.
2. Governance runs continuously; formal go/no-go *decisions* sit at stage transitions (gates).
3. ISO/IEC 5338 is the AI system lifecycle standard; OECD and NIST AI RMF use compatible lifecycle framings.
4. Impact assessments belong early (ex ante); monitoring and incident duties belong in operation; both feed back into earlier stages.
5. Retrained or substantially changed models must re-pass testing/validation gates before going back into production.

## SELF-CHECK

1. **List the eight canonical lifecycle stages in order.**
   Plan, design, data, build/train, test/evaluate, deploy, operate & monitor, retire.
2. **What two things does every governance gate require?**
   Reviewed evidence and an accountable, documented sign-off (a named decision-maker).
3. **Which ISO standard addresses AI system lifecycle processes?**
   ISO/IEC 5338.
4. **A monitoring alert triggers retraining. What must happen before the new model version serves users?**
   It must re-pass the testing/validation gate (re-validation) with documented approval — retraining re-enters the lifecycle, it does not bypass it.
5. **Under the EU AI Act framing, which actor's obligations dominate pre-market lifecycle stages, and which actor's dominate the use stage?**
   Providers pre-market (design through conformity/placing on market); deployers during use/operation.
