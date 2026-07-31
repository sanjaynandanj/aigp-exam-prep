# GLOSSARY — 160+ Exam-Weighted Terms

Alphabetical, grouped A–Z. Definitions are deliberately **exam-oriented**: what a stem or distractor will test, not encyclopedia depth. The ~30 terms tagged **(high-yield)** appear constantly in stems, options and traps — know them cold. Legal specifics reflect the law as of mid-2026; verify volatile details against primary sources.

---

## A

- **accountability** — Being answerable for an AI system's outcomes, with identifiable owners and consequences; a core trustworthy-AI attribute paired on the exam with transparency.
- **accuracy (data quality)** — The degree to which data correctly describes what it represents; under AI Act Article 10, training/validation/testing data must meet quality criteria.
- **adverse impact** — Disproportionate negative effect of a neutral practice on a protected group; screened in US employment analytics with the four-fifths rule.
- **adversarial example** — An input deliberately perturbed (often imperceptibly) to cause a wrong model output at inference time; the payload of an evasion attack.
- **adversarial machine learning** — The study of attacks on ML systems (poisoning, evasion, extraction, inversion, membership inference) and their defenses.
- **AI agent** — An AI system that plans and executes multi-step actions using tools/APIs with limited human intervention; raises amplified oversight and security concerns (e.g., indirect prompt injection).
- **AI Act (EU) (high-yield)** — Regulation (EU) 2024/1689: the first comprehensive, risk-based horizontal AI law — prohibited / high-risk / transparency / minimal tiers plus GPAI rules; applies extraterritorially to systems placed on the EU market or whose output is used in the EU.
- **AI ethics board** — An advisory/decision body reviewing AI uses against ethical commitments; effective only with a defined mandate, authority and escalation path.
- **AI governance program** — The charter, policies, roles, committees, inventory, and lifecycle controls through which an organization directs and oversees AI.
- **AI inventory** — The maintained register of an organization's AI systems and models with owners, risk levels, and status; the precondition for governing anything.
- **AI literacy** — AI Act Article 4 duty (applicable since Feb 2025): providers and deployers must ensure staff dealing with AI have role- and context-appropriate skills and awareness.
- **AI Office** — The European Commission body supervising GPAI models, coordinating enforcement and drawing up codes of practice under the AI Act.
- **AI system (OECD/EU definition) (high-yield)** — A machine-based system that, for explicit or implicit objectives, **infers** from inputs how to generate outputs (predictions, content, recommendations, decisions) influencing physical or virtual environments; inference is the line separating AI from rule-only software.
- **algorithmic audit** — An independent, evidence-based examination of an AI system against defined criteria (e.g., NYC LL144 bias audits) using logs, documentation and test results.
- **algorithmic discrimination** — Unlawful differential treatment or impact produced by an automated system; the target concept of the Colorado AI Act.
- **algorithmic disgorgement** — US FTC settlement remedy ordering deletion of models/algorithms trained on unlawfully obtained data — not just the data itself.
- **algorithmic impact assessment (AIA)** — A broad (often voluntary) assessment of an AI system's risks to rights, fairness, safety and society; wider lens than a DPIA, distinct from a conformity assessment.
- **Annex III (high-yield)** — The EU AI Act's list of high-risk use areas: biometrics, critical infrastructure, education, employment, essential private/public services (incl. credit and life/health insurance), law enforcement, migration/border, justice and democratic processes.
- **anonymization** — Irreversibly preventing re-identification; truly anonymous data falls outside GDPR — but model memorization can defeat claimed anonymization.
- **automated decision-making (GDPR Art. 22) (high-yield)** — Individuals' right not to be subject to decisions based **solely** on automated processing with legal or similarly significant effects; exceptions: contract necessity, law with safeguards, explicit consent. Token human review doesn't escape it.
- **automation bias** — Human tendency to over-trust and under-scrutinize automated outputs; measured in practice via override rates and countered by oversight design, not slogans.
- **autonomy (system)** — The degree to which a system operates without human intervention; higher autonomy demands stronger oversight and fail-safe design.

## B

- **backdoor (trojan) attack** — Poisoning that implants a hidden trigger; the model behaves normally until the trigger input activates the malicious behavior.
- **benchmark** — A standardized evaluation dataset/task; passing one benchmark never establishes safety or fairness across contexts.
- **bias (statistical/societal)** — Systematic error or unjust skew in data, model or deployment; sources include historical, representation, measurement, aggregation and evaluation bias.
- **BIPA (Illinois Biometric Information Privacy Act) (high-yield)** — Requires informed **written** consent and retention/destruction policies for biometric identifiers; unique for its private right of action with statutory damages, driving major class actions.
- **black-box model** — A model whose internal logic is not directly interpretable by humans; drives the need for XAI and documentation.
- **brittleness** — Failure under small distribution shifts or unusual inputs; the robustness gap between lab and world.

## C

- **calibration (predictive parity)** — A fairness/validity property: a given score means the same outcome probability across groups; can be mathematically incompatible with error-rate parity when base rates differ.
- **canary (staged) release** — Serving a small share of live traffic with the new model, expanding as monitored KPIs hold; contrast with shadow deployment (no live effect).
- **CE marking (high-yield)** — The provider's affixed mark declaring a high-risk AI system conforms to EU requirements after conformity assessment; an AI Act/product-law concept, never a GDPR one.
- **chatbot disclosure** — AI Act Article 50: people must be informed they are interacting with an AI system unless obvious from context.
- **code of practice (GPAI)** — AI Office-facilitated instrument helping GPAI providers demonstrate compliance pending harmonised standards.
- **Colorado AI Act (high-yield)** — First broad US state AI law: reasonable-care duties on developers and deployers of high-risk AI in consequential decisions to prevent algorithmic discrimination — impact assessments, notices, AG enforcement (no private right of action).
- **compute threshold (10^25 FLOPs)** — The training-compute level at which an EU GPAI model is presumed to pose systemic risk; triggers Commission notification and added obligations.
- **concept drift** — The input→outcome relationship changes over time (e.g., fraud tactics evolve) even if input distributions look stable; contrast data drift.
- **confusion matrix** — Table of true/false positives/negatives underpinning accuracy, precision, recall and error-rate fairness metrics.
- **conformity assessment (high-yield)** — Mandated pre-market verification that a high-risk system meets AI Act requirements; mostly internal control (self-assessment) for Annex III, with notified bodies chiefly for biometrics and product-embedded AI.
- **Council of Europe Framework Convention on AI** — 2024; the first binding international AI treaty — human rights, democracy, rule of law — open to non-European states; principles-level, distinct from the EU AI Act.
- **counterfactual explanation** — "What minimal change would flip the decision" — a user-facing explainability technique (e.g., "income above X would have led to approval").
- **cross-validation** — Rotating train/test splits to estimate generalization; a validity technique, not a fairness one.

## D

- **data controller** — GDPR actor determining purposes and means of processing; contrasted with the processor acting on instructions.
- **data drift (covariate shift)** — The input distribution changes relative to training (new market, new demographics); the model sees data it never learned.
- **data governance** — Policies and controls over data provenance, quality, rights, minimization and lifecycle; AI Act Article 10 makes it a high-risk obligation.
- **data minimization** — GDPR principle: only personal data necessary for the purpose; in tension with "collect everything" ML habits, resolved by necessity analysis and PETs.
- **data poisoning** — Deliberate corruption of training data to degrade or manipulate a model's future behavior; the training-time attack (contrast evasion at inference).
- **data processor** — GDPR actor processing personal data on the controller's documented instructions.
- **data protection by design and by default** — GDPR Article 25: build privacy into systems from the outset; maps naturally onto AI lifecycle gates.
- **datasheet (for datasets)** — Standardized dataset documentation: motivation, composition, collection process, consent, gaps, recommended uses; the dataset-side sibling of the model card.
- **deep learning** — ML using multi-layer neural networks that learn hierarchical features from raw data; powerful, data-hungry, and typically opaque.
- **deepfake** — AI-generated/manipulated content depicting real people or events deceptively; AI Act requires disclosure of artificial origin (manner adapted for artistic/satirical works — the duty itself remains).
- **demographic parity (statistical parity)** — Equal selection/positive rates across groups; one fairness definition among several mutually conflicting ones.
- **deployer (high-yield)** — AI Act actor using an AI system under its authority (not the developer, importer or distributor); owes use-per-instructions, competent oversight, monitoring, log retention (≥6 months), worker/candidate information and (some) FRIAs.
- **disparate impact (high-yield)** — Facially neutral practice with disproportionate effect on a protected group; actionable without intent, subject to business-necessity defenses. The exam's favorite contrast with disparate treatment.
- **disparate treatment** — Intentional differential treatment based on a protected characteristic (e.g., using race as a feature).
- **distributor** — AI Act supply-chain actor making a system available on the EU market other than the provider/importer; rebranding it as its own converts it into the provider.
- **DPIA (data protection impact assessment) (high-yield)** — GDPR Article 35 assessment required before high-risk personal-data processing (e.g., systematic extensive profiling); scoped to data-protection risks — narrower than an AIA, different trigger than a FRIA.
- **drift (model drift)** — Post-deployment performance decay as the world diverges from training conditions; the reason monitoring, thresholds and retraining triggers exist.

## E

- **EEOC** — US Equal Employment Opportunity Commission; applies Title VII/ADEA/ADA to AI hiring tools — employers stay liable for vendor tools' discriminatory outcomes.
- **emotion recognition** — Inferring emotions from biometric data; **prohibited** by the AI Act in workplaces and education (save medical/safety), transparency-regulated elsewhere.
- **equalized odds** — Fairness metric requiring equal true-positive and false-positive rates across groups; conflicts with calibration when base rates differ.
- **EU database (high-risk registration)** — Public EU registry where providers register Annex III high-risk systems before market placement (certain public-authority deployers register uses too).
- **evasion attack** — Fooling a deployed model with adversarial inputs at inference time; the runtime counterpart of poisoning.
- **explainability (high-yield)** — The capacity to convey why a system produced a particular output, in terms meaningful to the audience; distinct from transparency (disclosure about the system).
- **explicit consent** — GDPR's heightened consent standard; one of the three Article 22 gateways for solely automated significant decisions.
- **extraterritoriality** — Laws reaching actors outside their territory: the AI Act binds foreign providers whose systems or outputs reach the EU; GDPR binds foreign controllers targeting EU data subjects.

## F

- **fairness** — Family of competing definitions (parity, equalized odds, calibration, individual fairness) that cannot all hold simultaneously when base rates differ; governance = choose, justify, document.
- **feature** — An input variable a model learns from; proxy features can smuggle protected attributes into "neutral" models.
- **federated learning** — Training across decentralized data holders without centralizing raw data; a privacy-enhancing training pattern.
- **fine-tuning** — Continued training of a pretrained model on narrower data to specialize it; substantial downstream modification can shift regulatory responsibility to the modifier.
- **FLOPs** — Floating-point operations; the compute currency of the AI Act's 10^25 systemic-risk presumption.
- **foundation model (high-yield)** — A model trained on broad data at scale, adaptable to many downstream tasks; the concept behind the AI Act's GPAI regime.
- **four-fifths (80%) rule** — US employment screening heuristic: selection-rate ratio below 0.8 flags potential adverse impact warranting investigation — evidence, not proof.
- **FRIA (fundamental rights impact assessment) (high-yield)** — AI Act Article 27: pre-use assessment by deployers that are public bodies/private providers of public services, plus deployers using high-risk AI for credit scoring or life/health insurance pricing.
- **FTC Act Section 5** — US prohibition on unfair or deceptive acts; the FTC's main AI enforcement hook (deceptive AI claims, unfair uses, algorithmic disgorgement remedies).

## G

- **GDPR (high-yield)** — The EU General Data Protection Regulation: lawful basis, purpose limitation, minimization, data-subject rights, DPIAs, 72-hour breach notification, fines to 4%/€20M. On the exam, keep its numbers separate from the AI Act's.
- **general-purpose AI (GPAI) model (high-yield)** — AI Act category for models displaying significant generality across tasks; providers owe technical documentation, downstream information, a copyright policy and a public training-content summary — plus systemic-risk duties above the compute threshold.
- **generative AI** — Models producing novel content (text, image, audio, video, code); triggers AI Act marking/disclosure duties and copyright disputes.
- **GOVERN (NIST)** — The cross-cutting NIST AI RMF function: culture, accountability, policies enabling MAP, MEASURE and MANAGE.
- **governance committee (AI)** — Cross-functional decision body for AI risk: use-case approval, policy, escalation; effective only with documented authority.
- **ground truth** — The reference labels/outcomes a model is trained and judged against; when labels encode human bias, "ground truth" is neither.

## H

- **hallucination** — Confident generation of false or fabricated content by generative models; mitigable (grounding, verification, human review) but not eliminable.
- **harmonised standards** — European standards cited in the EU Official Journal; compliance creates a **presumption of conformity** with corresponding AI Act requirements — a status ISO certification alone does not confer.
- **high-risk AI system (high-yield)** — AI Act tier for Annex III use areas and regulated-product safety components; triggers the full obligations cascade (risk management, data governance, documentation, logging, transparency, oversight, accuracy/robustness/cybersecurity, conformity assessment).
- **HITL (human-in-the-loop) (high-yield)** — A human must act/approve before each AI output takes effect; contrast HOTL (monitor and intervene) and human-in-command (overarching authority).
- **HOTL (human-on-the-loop)** — Automated operation with human supervision and power to intervene or reverse after the fact.
- **human-in-command (HIC)** — Humans retain ultimate authority over whether/where/how the system is used at all, including shutdown.
- **human oversight (AI Act Art. 14)** — Providers must design high-risk systems so competent, authorized humans can understand, monitor, decide not to use, override or halt them; deployers must actually staff that oversight.

## I

- **impact ratio** — Selection rate of a category divided by that of the most-selected category; the metric NYC LL144 bias audits must report.
- **importer** — AI Act actor placing a third-country provider's system on the EU market; must verify conformity assessment, documentation and marking first.
- **incident response (AI)** — Defined taxonomy, detection, roles, escalation, communications, regulatory reporting and post-incident learning for AI failures; runs parallel to (not instead of) GDPR breach handling.
- **individual fairness** — "Similar individuals receive similar outcomes"; distinct from group-statistical metrics.
- **inference (ML)** — Applying a trained model to new inputs in production; the phase monitoring governs (contrast training).
- **instructions for use** — Provider-supplied information enabling deployers to operate a high-risk system properly: capabilities, limitations, oversight measures, performance conditions.
- **inter-annotator agreement** — Consistency between human labelers; low agreement means the model learns subjective disagreement as fact.
- **interpretability** — The degree to which a model's mechanics can be understood directly (inherently interpretable models) versus approximated post hoc.
- **ISO/IEC 22989** — The AI terminology and concepts standard.
- **ISO/IEC 23894** — AI risk-management guidance ("should"); operationalized inside a 42001 management system.
- **ISO/IEC 42001 (high-yield)** — Certifiable AI management system (AIMS) requirements standard ("shall"): policy, roles, risk processes, controls, continual improvement — organizational certification, not product certification.

## J

- **jailbreak** — Prompting that bypasses a model's safety guardrails to elicit prohibited outputs; a red-teaming staple.

## K

- **k-anonymity** — Privacy property where each record is indistinguishable from at least k−1 others on quasi-identifiers; illustrative of PET thinking (and its limits against inference attacks).

## L

- **label** — The target value attached to a training example in supervised learning; label quality bounds model validity.
- **large language model (LLM)** — A foundation model trained on text at scale to predict tokens; powers chatbots, agents and the exam's generative-AI scenarios.
- **lawful basis** — One of GDPR's six grounds (consent, contract, legal obligation, vital interests, public task, legitimate interests) required for any personal-data processing, including model training.
- **lifecycle (AI)** — Plan/design → data → build/train → verify/validate → deploy → operate/monitor → retire; governance attaches gates and artifacts to each stage.
- **Local Law 144 (NYC) (high-yield)** — Requires annual **independent** bias audits of automated employment decision tools used for NYC hiring/promotion, publication of a results summary (selection rates/impact ratios), and 10-business-day advance candidate notice.
- **logging (AI Act)** — High-risk systems must automatically record events; deployers retain logs at least six months (more where law requires).

## M

- **machine learning (ML)** — Techniques where systems learn patterns from data rather than following only explicit rules; the dominant path to modern AI.
- **MANAGE (NIST)** — RMF function: prioritize risks and act — treat, monitor, respond, improve.
- **MAP (NIST)** — RMF function: establish context, intended purpose, stakeholders, and identify risks. MAP comes **before** MEASURE — a standing exam trap.
- **MEASURE (NIST)** — RMF function: analyze, assess, benchmark and track identified risks with quantitative/qualitative methods.
- **membership inference** — Attack determining whether a specific record was in a model's training set; a privacy attack demonstrating models leak training information.
- **model card (high-yield)** — Standardized model documentation: intended and out-of-scope uses, disaggregated performance, limitations, ethical considerations; the model-side sibling of the datasheet.
- **model inversion** — Attack reconstructing (approximations of) training-data attributes from model outputs/parameters; contrast membership inference (in/out determination).
- **model owner** — The named business-side individual accountable for a model's purpose, risk acceptance, performance and lifecycle — separate from builders and validators.

## N

- **neural network** — Model of layered weighted connections trained by adjusting weights against error; the substrate of deep learning.
- **NIST AI RMF (high-yield)** — Voluntary US framework: GOVERN + MAP + MEASURE + MANAGE, plus seven trustworthy-AI characteristics (valid & reliable; safe; secure & resilient; accountable & transparent; explainable & interpretable; privacy-enhanced; fair with harmful bias managed).
- **notified body (high-yield)** — Independent organization designated by a member state to perform third-party conformity assessment — relevant under the AI Act mainly for biometric systems and product-embedded AI.

## O

- **OECD AI Principles** — First intergovernmental AI standard (2019, updated 2024): inclusive growth, human-centered values, transparency/explainability, robustness/security/safety, accountability; source of the canonical AI-system definition.
- **opt-out (TDM reservation)** — Rightsholders' reservation of text-and-data-mining rights under EU copyright law; GPAI providers must maintain policies to identify and respect it.
- **overfitting** — Memorizing training data at the expense of generalization: high training accuracy, poor real-world performance.
- **override rate** — Share of AI recommendations that human overseers change; near-zero at high speed signals rubber-stamping.

## P

- **penalty tiers (AI Act) (high-yield)** — Up to 7%/€35M for prohibited practices; up to 3%/€15M for most other violations; up to 1%/€7.5M for supplying incorrect information. Never confuse with GDPR's 4%.
- **personal data** — Any information relating to an identified or identifiable person; the trigger for the entire GDPR machinery, including in training sets.
- **post-market monitoring** — AI Act provider duty to systematically collect and analyze real-world performance data across the system's lifetime, feeding corrective action.
- **precision & recall** — Of predicted positives, how many are right (precision); of actual positives, how many were found (recall); the trade-off behind many threshold decisions.
- **privacy-enhancing technologies (PETs)** — Techniques limiting personal-data exposure: pseudonymization, differential privacy, federated learning, synthetic data.
- **prohibited practices (Art. 5) (high-yield)** — The AI Act's bans (from Feb 2025): harmful manipulation/exploitation of vulnerabilities, social scoring, predictive policing based solely on profiling, untargeted facial-image scraping, emotion recognition in work/education (save medical/safety), biometric categorization inferring sensitive attributes, and real-time remote biometric identification in public for law enforcement (narrow exceptions).
- **prompt injection (high-yield)** — Attack embedding instructions in prompts or in content the model processes (indirect injection) to hijack its behavior; the signature LLM/agent vulnerability.
- **provider (high-yield)** — AI Act actor that develops (or has developed) an AI system/model and places it on the market under its own name; carries the heaviest obligations. Rebranding, substantial modification, or repurposing can turn a deployer/distributor into the provider.
- **pseudonymization** — Replacing identifiers so data can't be attributed to a person without separate additional information; still personal data under GDPR.
- **purpose limitation** — GDPR principle: data collected for specified purposes may not be reused incompatibly — the core question when repurposing data for training.

## Q

- **quality management system (AI Act Art. 17)** — The provider's documented organizational system (procedures, resources, accountability) ensuring high-risk compliance across design, development and post-market phases.

## R

- **RAG (retrieval-augmented generation)** — Grounding a generative model's answers in documents retrieved at query time; a leading hallucination mitigation.
- **real-time remote biometric identification** — Live identification of individuals in publicly accessible spaces; prohibited for law enforcement under the AI Act save narrowly defined, authorized exceptions.
- **red teaming (high-yield)** — Adversarial testing that actively hunts for harmful outputs, vulnerabilities and misuse paths beyond intended use; expected of systemic-risk GPAI providers and mature programs generally.
- **reinforcement learning** — Learning a policy from reward/penalty signals through interaction with an environment; contrast supervised (labels) and unsupervised (structure).
- **representativeness** — Whether data reflects the population and conditions the system will actually serve; its absence is a root cause of group harm.
- **reproducibility** — Ability to re-derive a model from versioned data, code, hyperparameters, seeds and environment; the technical backbone of auditability.
- **risk-based approach** — Calibrating obligations to the level of risk rather than regulating all AI identically; the design principle of the AI Act, NIST RMF and most governance programs.
- **risk management system (AI Act Art. 9)** — The provider's continuous, iterative lifecycle process to identify, evaluate and mitigate high-risk-system risks — explicitly not a one-time checklist.
- **robustness** — Maintaining performance under noise, perturbation, edge cases and shift; tested by stress and out-of-distribution evaluation.

## S

- **self-supervised learning** — Pretraining on unlabeled data using proxy objectives (e.g., next-token prediction); how foundation models get made.
- **serious incident (AI Act) (high-yield)** — Incident/malfunction leading (directly or indirectly) to death or serious health harm, serious & irreversible critical-infrastructure disruption, breach of fundamental-rights obligations, or serious property/environmental damage. Provider reporting: ≤15 days generally, ≤10 days for death, ≤2 days for widespread infringement/critical infrastructure.
- **shadow deployment** — Running a model on live inputs with zero operational effect, comparing outputs to the incumbent process; the pre-launch confidence builder.
- **social scoring** — Evaluating people over time across contexts, producing detrimental treatment unrelated to the data's origin or disproportionate to conduct; an Article 5 prohibition.
- **sociotechnical system** — Frame recognizing AI risk emerges from interaction of models, people, processes and institutions — so governance must reach beyond code.
- **substantial modification** — A change to a system's purpose or behavior beyond the provider's intent that can reclassify the system and make the modifier the new provider.
- **supervised learning** — Learning a mapping from labeled examples (input → known outcome); the paradigm behind most consequential-decision models.
- **synthetic data** — Artificially generated data easing privacy/scarcity constraints — while inheriting generator bias and missing real edge cases; still requires evaluation.
- **system card** — Documentation extending model cards to a whole deployed system (components, guardrails, evaluations) — the artifact for systems built from multiple models.
- **systemic risk (GPAI) (high-yield)** — AI Act tier for GPAI models with high-impact capabilities (presumed at >10^25 training FLOPs or via Commission designation); adds adversarial evaluation, risk mitigation, incident reporting and cybersecurity duties.

## T

- **TDM (text and data mining) exception** — EU copyright exception permitting mining, with a commercial-use opt-out for rightsholders; the pivot of EU training-data copyright analysis.
- **technical documentation (Annex IV)** — Provider-maintained documentation demonstrating a high-risk system's compliance and enabling authorities to assess it; drafted before market placement, kept current.
- **testing data** — Held-out data used for final performance estimation; contamination with training data (leakage) inflates every downstream claim.
- **three lines of defense (high-yield)** — First line: business/development owns risk. Second line: risk & compliance set policy and challenge. Third line: internal audit gives independent assurance to the board. The exam loves scrambling the order.
- **training data** — Data from which model parameters are learned; its provenance, rights, quality and representativeness are the first battleground of AI governance.
- **transfer learning** — Reusing knowledge from a model trained on one task/domain for another; fine-tuning is its most common form.
- **transparency (AI Act Art. 50) (high-yield)** — Disclosure duties for limited-risk interactions: inform people they face an AI (chatbots), mark synthetic content machine-readably, disclose deepfakes, inform persons exposed to emotion recognition/biometric categorization.
- **trustworthy AI** — Umbrella for the attribute set (valid/reliable, safe, secure/resilient, accountable/transparent, explainable/interpretable, privacy-enhanced, fair); the shared vocabulary of NIST, OECD and the AI Act's aims.

## U

- **underfitting** — Model too simple to capture the signal: poor performance on training *and* new data (contrast overfitting).
- **unsupervised learning** — Finding structure (clusters, patterns, anomalies) in unlabeled data.
- **use-case intake** — The lifecycle's front gate: screening proposed AI uses against ban lists, legal constraints and feasibility before any build spend.

## V

- **validation data** — Data used during development to tune hyperparameters and compare candidate models — distinct from the final test set.
- **validity & reliability** — Producing correct outputs for the intended purpose, consistently over time and conditions; NIST lists it first among trustworthiness characteristics.
- **vendor due diligence (AI)** — Pre-contract evidence gathering on a third-party AI supplier: documentation, validation/fairness results, data governance, security, update and incident practices, regulatory support.

## W

- **watermarking (content provenance)** — Embedding detectable signals in AI-generated content to support the machine-readable marking and deepfake-disclosure duties.

## X

- **XAI (explainable AI)** — Methods making model behavior understandable: inherently interpretable models, post-hoc feature attributions, counterfactuals; post-hoc methods approximate and can mislead.

## Z

- **zero-shot learning** — A model performing a task it was never explicitly trained on, from instructions alone; evidence of foundation-model generality (and of unpredictable capability surface).
