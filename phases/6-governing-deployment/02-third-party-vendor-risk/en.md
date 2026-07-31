# Third-Party & Vendor AI Risk: Assessment, Evidence, Assurance

**Phase 6 · Lesson 02 · ~1.5h · BoK Domain IV**

## EXAM FOCUS

Most organizations buy far more AI than they build, so Domain IV leans hard on vendor risk. Tested: the dimensions of AI vendor due diligence, the model-provenance questions that go beyond classic IT vendor review, what evaluation evidence to demand, what SOC 2 / ISO certifications do and do **not** prove, and fourth-party / model-supply-chain risk. The distractor to beat: "the vendor is certified, so we're covered."

## CORE

### Why AI vendor risk is different

Classic third-party risk covers security, availability, financials, and data handling. AI adds: opaque model behavior, training-data provenance you can't inspect, silent model updates that change behavior mid-contract, and regulatory roles (you may be the *deployer* accountable for oversight regardless of who built the model — accountability is not outsourceable).

### Due-diligence dimensions

| Dimension | Questions to the vendor |
|---|---|
| **Model provenance** | Who developed the model? Built, licensed, or wrapped around a third-party foundation model? Which base model and version? Training-data sources, licensing, personal data, consent basis? |
| **Performance evidence** | Evaluation results on data resembling *our* population; subgroup-disaggregated metrics; robustness/red-team results; known failure modes and limitations |
| **Documentation** | Model/system card, instructions for use, technical documentation availability (Phase 5 L07); what will they show under NDA? |
| **Regulatory posture** | Their AI Act role and yours; conformity status for high-risk; DPAs and data-protection compliance; sectoral approvals |
| **Security** | Adversarial-attack testing, prompt-injection defenses, access controls on model artifacts, vulnerability management |
| **Data handling** | Is *our* data used to train their models (opt-out?); retention; tenant isolation; cross-border flows |
| **Change management** | How are model updates notified and versioned? Can we pin a version? Re-validation rights on updates |
| **Operational** | Uptime SLAs, incident notification, support, exit/portability |
| **Viability & ethics** | Financial health, litigation/regulatory history, responsible-AI program maturity |

Depth should scale with the use case's risk tier (proportionality again): a grammar checker gets a questionnaire; a credit-decisioning engine gets evidence review, testing on your own data, and contractual teeth (Lesson 03).

### What certifications prove — and don't

| Assurance artifact | Proves | Does NOT prove |
|---|---|---|
| **SOC 2 (Type II)** | Controls over security/availability/confidentiality etc. operated effectively over a period — *organizational* controls | Anything about model accuracy, bias, or AI-specific risk |
| **ISO/IEC 27001** | Certified information-security management system | Same gap — security ≠ model quality |
| **ISO/IEC 42001** | Certified AI *management system* (governance processes exist and are audited) | Not that any specific model is accurate or fair |
| Penetration-test summaries | Point-in-time security posture | Model behavior |
| Model evaluation reports / bias-audit results | Model-level evidence (the thing certifications miss) | Performance on *your* population unless tested on it |

Exam rule: **certifications assure processes; only evaluations assure models** — and only evaluation on data like yours assures *your* deployment.

### Fourth-party and model-supply-chain risk

Your vendor's dependencies are your risk surface: the SaaS tool "with AI" may wrap a third-party foundation model (whose terms, region, and safety behavior flow down to you); it may run on hyperscaler infrastructure, use subprocessors for annotation/support, and pull open-source components (Phase 5 L08). Controls: require disclosure of material AI subprocessors and base models, flow-down of key obligations, and notification when the underlying model changes. The GenAI era's signature fourth-party event: **the base model your vendor wraps gets deprecated or swapped, and your product's behavior changes overnight.**

### Ongoing, not one-time

Vendor risk management continues through the contract: periodic reassessment, monitoring vendor incident disclosures, tracking model-version changes, re-running acceptance tests after major updates, and maintaining the vendor/AI inventory linkage (every third-party AI system in the AI inventory with an owner).

## CASES & EXAMPLES

**Scenario 1 — the certificate shield.** Procurement says an HR-screening vendor "passed SOC 2, so due diligence is done." *Exam point:* SOC 2 addresses organizational security controls, not model bias or accuracy. Demand model-level evidence: subgroup evaluations, bias-audit results, documentation, and ideally testing on your own applicant data.

**Scenario 2 — the hidden base model.** A "proprietary" contract-analysis tool turns out to be a thin wrapper on a general-purpose LLM API. The LLM provider changes model versions; extraction accuracy shifts materially, undetected for weeks. *Failed controls:* provenance disclosure (which base model?), change-notification clause, version pinning, and post-update re-validation.

**Scenario 3 — whose oversight duty?** A bank licenses a vendor credit model and argues the vendor "owns all AI compliance." *Exam point:* as deployer, the bank retains use-stage duties — oversight, monitoring, input-data appropriateness, logs (Art. 26 concept) — and sectoral accountability for its credit decisions. Accountability cannot be outsourced; only functions can.

**Scenario 4 — subprocessor surprise.** A healthcare transcription vendor is found sending audio to an offshore annotation subcontractor for "quality improvement." *Exam point:* fourth-party mapping and data-use restrictions (is our data training their models? who touches it?) belong in due diligence and contract — before signature.

## MEMORY HOOKS

**The vendor-risk trio:** *Provenance (where did the model come from) · Evidence (how well does it work, for whom) · Assurance (who verified what, how recently).*

**Certification limit:** *SOC 2 secures the house; it says nothing about the tenant's judgment.* Processes ≠ models.

**Fourth-party one-liner:** *You inherit your vendor's model choices.*

The 5 facts to retain:

1. AI vendor due diligence adds model provenance, evaluation evidence, documentation, and change-management to classic security/financial review — scaled to the use case's risk tier.
2. Ask what the product is built on: base/foundation model identity and version, training-data provenance, and whether your data trains their models.
3. SOC 2 / ISO 27001 / ISO 42001 assure organizational processes; they do not assure model accuracy or fairness — demand model-level evaluation evidence, ideally on your population.
4. Fourth-party risk: subprocessors, wrapped foundation models, and silent version changes flow down to you — require disclosure, flow-down clauses, and update notification/re-validation.
5. Buying AI does not transfer accountability: the deployer keeps oversight, monitoring, and regulatory duties for its own use.

## SELF-CHECK

1. **Name four due-diligence dimensions unique or heightened for AI vendors versus ordinary SaaS.**
   Model provenance (base model, training data), model evaluation evidence (incl. subgroup performance), model change management/version pinning, use of customer data for training (also: AI regulatory role analysis).
2. **What does a SOC 2 Type II report tell you about an AI product, and what gap remains?**
   That the vendor's organizational controls (security, availability, confidentiality) operated effectively over the review period; it says nothing about the model's accuracy, bias, robustness, or fitness for your population.
3. **Why should you require the vendor to disclose its base/foundation model?**
   Because its terms, safety behavior, geographic processing, and deprecation schedule flow down to you — a version swap by the upstream provider can change your product's behavior (fourth-party risk).
4. **Which obligations stay with you even when the AI is fully vendor-built?**
   Deployer duties: human oversight, monitoring, appropriate input data, log retention, transparency to affected persons, incident escalation — plus sectoral accountability for the decisions made.
5. **What ongoing vendor-risk activities follow contract signature?**
   Periodic reassessment, tracking model updates and re-validating after major ones, monitoring vendor incidents/disclosures, and keeping the AI inventory entry (owner, version, risk tier) current.
