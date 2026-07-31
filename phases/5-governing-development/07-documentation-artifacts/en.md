# Documentation Artifacts: Model Cards, Datasheets, System Cards

**Phase 5 · Lesson 07 · ~1h · BoK Domain III**

## EXAM FOCUS

The exam expects you to distinguish the major AI documentation artifacts — what each documents, who it is for, and where it sits in the lifecycle. Classic distractor pattern: "right artifact, wrong object" (a datasheet documents a *dataset*, a model card documents a *model*, a system card documents the *composed system*). Also tested: the EU AI Act Annex IV technical-documentation concept and the principle of audience-layered documentation.

## CORE

### The artifact family

| Artifact | Documents | Origin/lineage | Core contents | Primary audience |
|---|---|---|---|---|
| **Datasheet for datasets** | A *dataset* | Gebru et al., "Datasheets for Datasets" | Motivation, composition, collection process, preprocessing, recommended/discouraged uses, distribution, maintenance | Developers reusing the data; reviewers; auditors |
| **Model card** | A *trained model* | Mitchell et al., "Model Cards for Model Reporting" | Intended use & out-of-scope uses, training data summary, evaluation results **disaggregated by subgroup**, limitations, ethical considerations | Downstream developers, deployers, reviewers |
| **System card** | A *deployed AI system* (model + guardrails + UX + integrations) | Popularized by large labs (e.g., OpenAI's GPT-4 System Card) | System-level behavior, safety evaluations, red-team findings, mitigations, residual risks | Deployers, regulators, sophisticated public |
| **Technical documentation** (EU AI Act **Annex IV concept**) | A *high-risk AI system*, for regulators | EU AI Act | Comprehensive: general description, development process, data requirements, risk management, testing/validation results, human-oversight measures, lifecycle/change management, monitoring plan | Market surveillance authorities, notified bodies |
| **Instructions for use** | Deployer-facing operating manual | EU AI Act high-risk concept | Capabilities, limitations, oversight measures, expected lifetime/maintenance | Deployers/users |

Distinctions the exam rewards:

- **Datasheet ≠ model card:** the datasheet travels with the *data*; the model card travels with the *model*. A model trained on five datasets links to five datasheets.
- **Model card ≠ system card:** a system card covers the whole product — safety layers, filters, UI disclosures — not just the weights. GenAI products made this distinction mainstream.
- **Voluntary vs mandatory:** cards and datasheets are best-practice transparency artifacts; **Annex IV-style technical documentation is a legal precondition** for high-risk market access in the EU, must be kept up to date, and underpins the conformity assessment (Lesson 06).

### Audience-layered documentation

One system, several readers, several layers:

| Layer | Audience | Register |
|---|---|---|
| Regulator layer | Authorities, notified bodies, auditors | Exhaustive, evidence-linked (Annex IV-style) |
| Professional layer | Deployers, integrators, risk teams | Model/system cards, instructions for use |
| Affected-person layer | End users, decision subjects | Plain-language notices, explanations (Phase 6, Lesson 06) |

Writing only the regulator layer fails users; writing only marketing-grade summaries fails regulators. Governance sets a documentation *standard* specifying which artifacts each risk tier must produce, when they're updated (every new version/material change), and who approves them.

### Documentation as evidence infrastructure

These artifacts aren't paperwork for its own sake: they are the transmission mechanism of the AI value chain. The provider's model card and instructions for use are what let a *deployer* meet its own duties (use per instructions, oversight, monitoring). Missing or vague upstream docs are a vendor-risk red flag (Phase 6, Lessons 02–03).

## CASES & EXAMPLES

**Scenario 1 — name that artifact.** A team publishes a document describing a dataset's collection methodology, consent status, known gaps, and discouraged uses. *Answer:* a datasheet for datasets — not a model card (no model is described).

**Scenario 2 — subgroup evaluations.** A vendor's model documentation reports one aggregate accuracy number. A governance reviewer requests disaggregated performance by demographic subgroup and explicit out-of-scope uses. *Exam point:* those are canonical model-card elements; their absence is a due-diligence red flag.

**Scenario 3 — Annex IV concept.** An EU market surveillance authority requests the technical documentation for a high-risk recruitment system. The provider offers its public model card. *Exam point:* insufficient — Annex IV-style technical documentation is far deeper (development process, risk management records, test results, oversight design) and must be maintained and available to authorities.

**Scenario 4 — layered audiences.** A hospital deploys a diagnostic-support system. The CIO gets the system card and instructions for use; clinicians get workflow-level guidance and limitation warnings; patients get a plain-language notice that AI supports (not replaces) clinical judgment. *Exam point:* correct audience layering — one document cannot serve all three.

## MEMORY HOOKS

**Object mapping — "Data gets a Datasheet, Models get Model cards, Systems get System cards, Regulators get the Annex."**

**Card question test:** *What is being described?* dataset → datasheet · weights + evals → model card · whole product + safety layers → system card · everything, for authorities → technical documentation.

The 5 facts to retain:

1. Datasheets document datasets (motivation, composition, collection, recommended uses) — lineage: Gebru et al.
2. Model cards document trained models — intended/out-of-scope uses and subgroup-disaggregated evaluations are their signature elements (Mitchell et al.).
3. System cards document the full deployed system including guardrails and red-team results — the GenAI-era artifact.
4. EU AI Act Annex IV-concept technical documentation is mandatory for high-risk systems, regulator-facing, kept current, and feeds conformity assessment.
5. Documentation must be audience-layered: regulator, professional/deployer, and affected-person layers — and provider docs are what enable deployer compliance downstream.

## SELF-CHECK

1. **Match artifact to object: datasheet, model card, system card, Annex IV technical documentation.**
   Dataset; trained model; deployed system (model + guardrails + UX); high-risk AI system documented exhaustively for regulators.
2. **Which two elements are signature features of a model card?**
   Intended use / out-of-scope uses, and evaluation results disaggregated across relevant subgroups (plus limitations and ethical considerations).
3. **Why did system cards emerge as distinct from model cards?**
   Deployed products add safety filters, system prompts, UX and integrations that change real-world behavior — the system, not just the weights, needs documenting.
4. **How does provider documentation enable deployer compliance?**
   Instructions for use and model/system cards tell deployers the intended purpose, limitations, and oversight measures — the basis of the deployer's duties to use the system properly and supervise it.
5. **Is a public model card sufficient when an EU authority requests high-risk technical documentation?**
   No — the Annex IV concept requires comprehensive development, risk-management, testing, and oversight documentation maintained for authorities; a card is only a summary layer.
