# Training Governance: Documentation, Reproducibility, Versioning

**Phase 5 · Lesson 04 · ~1h · BoK Domain III**

## EXAM FOCUS

This lesson covers governance of the build/train stage: making model development *reproducible, documented, and attributable*. The exam tests it at governance level — you won't tune hyperparameters, but you must know why they get documented, what experiment tracking and versioning give an auditor, and what records a foundation-model fine-tune should generate. Scenario stems often feature a team that "can't recreate the production model" and ask which control was missing.

## CORE

### Why training needs governance

A model is the product of code + data + configuration + randomness + compute environment. If any of those is unrecorded, the organization cannot: reproduce the model, explain it to a regulator, debug an incident, or prove which version made a contested decision. Training governance converts research chaos into an auditable engineering process.

### The core controls

| Control | What it is | Governance payoff |
|---|---|---|
| **Experiment tracking** | Logging every training run: dataset version, code commit, parameters, metrics, artifacts | Answers "what did we try, what won, and why" — decision evidence |
| **Reproducibility** | Pinned dependencies, recorded random seeds, captured environments (containers) | An independent party can re-derive the model — the foundation of auditability |
| **Model versioning** | Unique, immutable identifiers for each trained model artifact | Ties every prediction/incident to an exact model version |
| **Data versioning** | Immutable snapshots/hashes of training, validation, test sets | Ties every model version to exactly the data that produced it |
| **Hyperparameter documentation** | Recording configuration choices (learning rate, architecture size, thresholds) and their rationale | Explains design decisions; enables re-training and challenge |
| **Compute logging** | Records of training jobs, duration, hardware, and energy where tracked | Cost/environmental accountability; relevant to GPAI compute-threshold concepts in the EU AI Act (training-compute scale as a systemic-risk indicator) |

### The lineage triangle

Every production model should resolve to three pinned pointers:

**model version ↔ code version (commit) ↔ data version (snapshot/hash)**

If any leg is missing, reproducibility fails. Registries (a "model registry") hold the model artifacts, their lineage metadata, evaluation results, and approval status — the registry is where the release gate (Lesson 09) looks.

### Foundation-model fine-tune records

When you fine-tune a third-party foundation model rather than training from scratch, the record changes shape but not purpose:

| Record | Content |
|---|---|
| Base model identity | Provider, model name and exact version, license/terms of use |
| Upstream documentation | Provider's model card / technical documentation relied on |
| Fine-tuning dataset | Provenance, lawful basis, version (all of Lesson 03 applies) |
| Method & configuration | Fine-tuning technique, parameters, guardrail/system-prompt changes |
| Delta evaluation | How behavior changed vs the base model (safety and performance) |
| Role analysis | Whether the modification is substantial enough to shift EU AI Act responsibilities toward provider status (Lesson 10) |

### Who owns training governance

Engineering/ML teams operate the tooling; the AI governance function sets the *policy* (what must be logged, retention of records, when a training run requires review); model risk or internal audit periodically verifies the records are real and complete. Records produced here become the raw material for Annex IV-style technical documentation (Lesson 07).

## CASES & EXAMPLES

**Scenario 1 — the unreproducible model.** A regulator questions a loan-denial decision from 14 months ago. The team has the current model but overwrote earlier versions, and the training data has since been "refreshed" in place. *Failed controls:* model versioning and data versioning (immutable snapshots). Best answer: implement versioned model registry + dataset snapshots with retention aligned to accountability periods.

**Scenario 2 — two models, one name.** A hotfix retrain ships under the same model name with no new version ID. Monitoring later shows odd behavior, but logs can't distinguish which artifact served which requests. *Exam point:* every trained artifact needs a unique immutable version, and serving logs must record it.

**Scenario 3 — fine-tune surprise.** A company fine-tunes an open-weights LLM for medical-intake chat, materially changing its behavior and marketing it under its own brand. *Exam point:* fine-tune records must support the role analysis — substantial modification/rebranding can make the company a provider with provider-grade documentation duties (concept anchor; details in Lesson 10).

## MEMORY HOOKS

**The lineage triangle:** *model ↔ code ↔ data — three pins or no proof.*

**Mnemonic — "REV-CHD":** **R**eproducibility, **E**xperiment tracking, **V**ersioning (model+data), **C**ompute logs, **H**yperparameter docs, **D**elta evaluation (for fine-tunes).

The 5 facts to retain:

1. Training governance exists so an independent party can reproduce, attribute, and challenge any production model.
2. Reproducibility requires pinned code, data snapshots, recorded configuration/seeds, and captured environments.
3. Every model version must map immutably to a code version and a data version (the lineage triangle), stored in a model registry with approval status.
4. Compute logging matters for cost/environmental accountability and connects to the EU AI Act's use of training-compute scale as a GPAI systemic-risk indicator.
5. Fine-tuning a foundation model creates its own record set — base-model identity/version/license, delta evaluations, and a provider-vs-deployer role analysis.

## SELF-CHECK

1. **Name the three pointers every production model must resolve to for reproducibility.**
   An immutable model version, the exact code version (commit), and the exact data version (snapshot/hash).
2. **What is the governance purpose of experiment tracking, beyond engineer convenience?**
   It creates decision evidence — which alternatives were tried, why the chosen model won — supporting accountability, audits, and technical documentation.
3. **Why must hyperparameters and their rationale be documented?**
   They are design decisions that shape model behavior; documenting them enables reproduction, regulator explanation, and challenge/review of choices.
4. **What extra records does fine-tuning a third-party foundation model require?**
   Base-model identity and exact version, license/terms, provider documentation relied on, fine-tune data provenance, method/configuration, delta (behavior-change) evaluations, and an AI Act role analysis.
5. **Who sets training-record policy versus who verifies compliance with it?**
   The AI governance function sets logging/retention policy; ML teams operate it; model risk/internal audit independently verifies records exist and are complete.
