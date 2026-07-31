# The AI Tech Stack: Data, Compute, Models, Applications

**Phase 1 · Lesson 06 · ~1h · BoK Domain I**

## EXAM FOCUS

Domain I — understanding the layers an AI system is built from and, crucially for later domains, *who controls each layer*. Tested as recall ("which layer does X belong to") and as setup for value-chain scenarios in Domains III–IV: provider vs deployer duties only make sense once you can place each actor on the stack. Open-vs-closed weights is a reliable one-question topic.

## CORE

### The four layers

| Layer | What it contains | Who typically controls it | Governance pressure points |
|---|---|---|---|
| **1. Data** | Training corpora, labels, fine-tuning sets, retrieval stores, user inputs/feedback | Data brokers, platforms, the open web, each enterprise for its own data | Provenance, consent/lawful basis, copyright, quality, bias, minimization |
| **2. Compute / infrastructure** | Specialized chips (GPUs/accelerators), data centers, cloud platforms | A small set of chipmakers and hyperscale cloud providers | Concentration/dependency, cost barriers, energy & water footprint, export controls, availability |
| **3. Model** | Foundation and task models, weights, fine-tunes, model APIs | Model developers ("providers"); open-weight communities | Capability risks, evaluation, documentation (model cards), GPAI obligations, release strategy |
| **4. Application** | Products embedding models: chatbots, copilots, screening tools, plus system prompts, guardrails, UX | App vendors and deploying enterprises | Use-case risk classification, transparency to users, human oversight, sector law |

Two structural facts the exam builds on:

1. **Control is fragmented.** The company a consumer blames (app layer) rarely built the model, never assembled the training data, and rents the compute. Accountability frameworks (and the EU AI Act's provider/deployer/importer/distributor roles — Phase 4) exist to re-attach obligations across this fragmentation.
2. **Risk flows down; information doesn't flow up or down well.** App builders inherit model flaws they can't see; model builders can't foresee app misuse. Documentation artifacts (model cards, system cards — Phase 5) are the designed remedy.

### Open vs closed weights

**Weights** are the learned parameters — release them and anyone can run, fine-tune, and modify the model.

| | Closed weights (API access only) | Open weights (downloadable) |
|---|---|---|
| Access | Via the provider's API; provider can monitor, filter, revoke | Anyone can run locally/on-prem |
| Control after release | Provider retains a kill switch, usage policies, abuse monitoring | Effectively **irrevocable** — copies proliferate |
| Safety guardrails | Enforced centrally | Can be fine-tuned away by downstream users |
| Transparency/scrutiny | Limited external inspection | Researchers can probe, audit, reproduce |
| Enterprise privacy | Data goes to provider (contract-dependent) | Can run fully in-house — data never leaves |
| Ecosystem effect | Concentration around few providers | Broad access, innovation, but also broad misuse access |

The honest framing (and the exam's): **a trade-off, not a good/evil split** — openness aids scrutiny, competition, and privacy-preserving self-hosting; it also removes post-release control. Note vocabulary precision: "open weights" ≠ fully "open source" (training data and code often remain closed even when weights are released).

### Where governance attaches, layer by layer

| Layer | Typical instruments |
|---|---|
| Data | Data governance programs, DPIAs, licensing/provenance records, dataset documentation |
| Compute | Vendor/cloud contracts, resilience & concentration risk management, sustainability reporting |
| Model | Model evaluations, red teaming, model cards, GPAI code-of-practice duties |
| Application | Use-case risk tiering, conformity assessment, user transparency, human oversight, monitoring |

## CASES & EXAMPLES

1. **The four-company chatbot.** A retail bank launches a support chatbot: model from an AI lab (via API), hosted on a hyperscaler, augmented with the bank's document store, built by a systems integrator. The bot gives harmful financial guidance. Untangling: model behavior (lab), retrieval content (bank's data layer), guardrail configuration (integrator), deployment decision (bank). Exam point: the *deployer-facing* accountability is the bank's, whatever the internal indemnities say — customers and regulators start there.

2. **Guardrails fine-tuned away.** A research team demonstrates that an open-weight model's safety refusals can be removed with modest fine-tuning. Nothing the original provider can do — copies are already everywhere. This is the standard illustration of "open release is irrevocable" and why model-release strategy is itself a governance decision.

3. **The compute bottleneck.** An enterprise's AI roadmap stalls because GPU capacity is scarce and concentrated in a few clouds; a regional outage takes down its production inference. Governance lesson: layer-2 dependency is an operational-resilience risk like any critical outsourcing — treat cloud/compute like financial services treat critical third parties.

4. **Exam-style placement question.** "A company compiles and licenses labeled medical images to model developers." Which layer? → Data. "A company offers a downloadable 7-billion-parameter model." → Model layer, open weights. "A hospital integrates that model into a triage tool." → Application layer (and the hospital picks up deployer/system-provider duties).

## MEMORY HOOKS

**Stack mnemonic — "D-C-M-A":** **D**ata → **C**ompute → **M**odel → **A**pplication ("**D**on't **C**onfuse **M**odels with **A**pps").

**Open-weights one-liner:** *open = inspectable but irrevocable; closed = controllable but concentrated.*

The 5 facts to retain:

1. Four layers: data, compute/infra, model, application — governance instruments differ per layer.
2. Control is fragmented across layers; legal roles (provider/deployer/etc.) exist to re-attach accountability.
3. Compute is highly concentrated (few chipmakers, few clouds) — a dependency and resilience risk, plus environmental footprint.
4. Open weights: scrutiny, competition, self-host privacy — but post-release control (and centrally enforced guardrails) are gone for good.
5. "Open weights" is not the same as "open source" — data and training code may stay closed.

## SELF-CHECK

1. Name the four stack layers and one governance pressure point for each.
2. Why does the fragmentation of the stack create an accountability problem, and what is the legal response pattern?
3. Give two governance advantages and two governance drawbacks of open-weight release.
4. Why is compute concentration a governance issue at all?
5. Place these on the stack: a labeling firm; a GPU cloud; a fine-tuned customer-service model; the SaaS product embedding it.

<details>
<summary>Answers</summary>

1. Data (provenance/consent/bias), compute (concentration/energy/resilience), model (evaluation/documentation/release strategy), application (use-case risk, transparency, oversight).
2. The actor facing the end user didn't build most of what they deploy, and builders can't see end uses — so laws define chained roles (provider, deployer, importer, distributor) with obligations at each link and documentation flowing between them.
3. Advantages: external scrutiny/auditability, on-prem privacy, competition/access. Drawbacks: irrevocability of release, guardrails removable by fine-tuning (plus broad misuse access).
4. Dependency on a handful of providers creates operational-resilience and market-power risks, cost barriers to entry, geopolitical exposure (export controls), and a significant energy/water footprint.
5. Labeling firm → data layer; GPU cloud → compute layer; fine-tuned model → model layer; SaaS product → application layer.

</details>
