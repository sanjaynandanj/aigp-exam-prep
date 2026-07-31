# Domain I Quiz — Foundations of AI Governance

> 20 questions · ~30 minutes · closed book. Take after Phases 1–2.
> Mirrors the exam mix: mostly recall/best-answer, with scenario items like the real thing.
> Answer key with full rationales is at the bottom — don't peek until you've committed to all 20.

---

**Q1.** Which element of the OECD's 2023 AI-system definition most cleanly distinguishes AI from conventional rule-based software?

- A. It runs on a machine rather than being performed by a human
- B. It operates with objectives that may be explicit or implicit
- C. It **infers** how to generate outputs from the input it receives
- D. It produces outputs in digital rather than physical form

**Q2.** A retailer clusters its customers into previously unknown segments based on purchasing behavior, with no labels provided. The ML approach is:

- A. Supervised learning
- B. Unsupervised learning
- C. Reinforcement learning
- D. Transfer learning

**Q3.** In reinforcement learning, the model improves primarily by:

- A. Memorizing labeled input–output pairs
- B. Minimizing reconstruction error over unlabeled data
- C. Receiving reward or penalty signals for actions taken in an environment
- D. Copying the parameters of a larger teacher model

**Q4.** What most distinguishes a **foundation model** from a traditional narrow ML model?

- A. It is always open-source and free to use
- B. It is trained on broad data at scale and is adaptable to many downstream tasks
- C. It cannot be fine-tuned once trained
- D. It is guaranteed to be free of bias because of its data volume

**Q5.** A legal-tech startup connects an LLM to the firm's own document repository so answers are grounded in retrieved firm documents rather than only the model's training data. This technique is:

- A. Retrieval-augmented generation (RAG)
- B. Reinforcement learning from human feedback (RLHF)
- C. Federated learning
- D. Model distillation

**Q6.** A vision model performs at 98% accuracy in the lab but fails badly when cameras are slightly tilted or lighting changes — conditions barely different from training. The failure mode is best described as:

- A. Hallucination
- B. Data leakage
- C. Automation bias
- D. Brittleness (lack of robustness)

**Q7.** A model achieves near-perfect accuracy on its training data but performs poorly on new, unseen data. This is:

- A. Underfitting
- B. Drift
- C. Poisoning
- D. Overfitting

**Q8.** Which list matches the NIST AI RMF's characteristics of trustworthy AI?

- A. Profitable, scalable, patentable, proprietary
- B. Valid & reliable; safe; secure & resilient; accountable & transparent; explainable & interpretable; privacy-enhanced; fair with harmful bias managed
- C. Lawful, ethical, robust — and nothing further
- D. Fast, accurate, cheap, and continuously learning

**Q9.** "The system's outputs can be understood by affected people, and the organization can be answerable for them" maps to which pair of trustworthy-AI attributes?

- A. Explainability and accountability
- B. Robustness and safety
- C. Privacy and security
- D. Validity and reliability

**Q10.** *Scenario.* A university admissions model is calibrated so that a predicted score of 80 means the same likelihood of success for every demographic group. However, its selection rates differ significantly between groups. The model satisfies:

- A. Demographic parity but not calibration
- B. Calibration (predictive parity) but not demographic parity
- C. Both demographic parity and equalized odds
- D. Individual fairness, which guarantees all group metrics simultaneously

**Q11.** The "impossibility" results in fairness research show that:

- A. No AI system can ever be made fairer through technical means
- B. Fairness metrics are only definable for binary classifiers
- C. When base rates differ between groups, several common fairness metrics cannot all be satisfied at once, forcing a documented trade-off choice
- D. Regulators have banned the use of statistical fairness metrics

**Q12.** *Scenario.* A bank deploys a fraud model that automatically blocks transactions in real time; analysts review a dashboard of blocked transactions each morning and can reverse errors. The oversight model in operation is:

- A. Human-in-the-loop
- B. Human-out-of-the-loop with no oversight
- C. Human-in-command only at the design stage
- D. Human-on-the-loop

**Q13.** "Human-in-command" (HIC) is best characterized as:

- A. A human approving each individual output before it takes effect
- B. A human supervising outputs in real time and intervening on exceptions
- C. Humans retaining overarching authority over whether, where and how the AI system is used at all, including the power to shut it down
- D. A human labeling the training data

**Q14.** *Scenario.* A social platform's recommender maximizes engagement and, over two years, measurably contributes to polarization of public debate in a region. In a harms taxonomy, this is primarily an example of:

- A. Individual harm
- B. Societal harm
- C. Purely economic harm to the company
- D. A harm outside the scope of AI governance

**Q15.** Which trio correctly illustrates individual, group, and societal harms respectively?

- A. A wrongly denied loan; systematically lower scores for one ethnicity; erosion of trust in elections from synthetic media
- B. Election disinformation; a data breach; a mispriced product
- C. A biased dataset; an unencrypted server; a missing policy
- D. Overfitting; drift; hallucination

**Q16.** *Scenario.* A mid-size insurer is standing up an AI governance program. Who is the most appropriate owner of **day-to-day operational accountability** for the program?

- A. The board of directors, which should personally review each model
- B. Each data scientist individually, with no central function
- C. The external auditor
- D. A designated AI governance lead/office, reporting into an executive with a cross-functional committee

**Q17.** In an AI governance operating model, the board of directors is primarily responsible for:

- A. Writing model documentation
- B. Performing fairness testing before each release
- C. Oversight of AI risk appetite and strategy, and holding management accountable
- D. Approving every individual use case at intake

**Q18.** In the "three lines of defense" model applied to AI:

- A. First line = internal audit; second line = the business; third line = risk/compliance
- B. First line = business/development teams owning risk; second line = risk & compliance functions setting policy and challenging; third line = internal audit providing independent assurance
- C. All three lines are performed by the AI vendor
- D. First line = regulators; second line = courts; third line = the press

**Q19.** *Scenario.* A company's ethics board reviewed a controversial emotion-detection product and recommended against launch; the product shipped anyway and the board learned about it from the press. The core governance failure is:

- A. The ethics board lacked a defined mandate, authority and escalation path integrated into the release process
- B. The ethics board had too many external members
- C. Emotion detection is always illegal, so no board was needed
- D. The board met too frequently

**Q20.** *Scenario.* A generative-AI vendor claims its new model is "fully aligned and bias-free" because it passed one benchmark. The most governance-literate response is:

- A. Accept the claim; benchmarks are dispositive evidence of fairness
- B. Reject AI entirely; no assurance is ever possible
- C. Require the model's failure modes, evaluation scope and residual risks to be documented, since no single benchmark establishes that a system is bias-free across contexts
- D. Ask only for the model's parameter count

---

## ANSWER KEY & RATIONALES

**Q1 — C.** Inference — deriving how to generate outputs from inputs — is the definitional hinge separating AI from pre-programmed rules.
- A: Conventional software is also machine-based.
- B: Objectives exist in ordinary software too.
- D: Output form is irrelevant to the definition.

**Q2 — B.** No labels + discovering hidden structure (clustering) = unsupervised learning.
- A: Supervised requires labeled outcomes.
- C: Reinforcement needs actions and reward signals.
- D: Transfer learning reuses a pretrained model, not described here.

**Q3 — C.** RL learns a policy from reward/penalty feedback through interaction with an environment.
- A: That describes supervised learning.
- B: That describes unsupervised/self-supervised objectives.
- D: That describes distillation.

**Q4 — B.** Foundation models = broad data, large scale, adaptable to many downstream tasks (the AI Act's GPAI concept is closely related).
- A: Many are proprietary.
- C: Fine-tuning is precisely how they're adapted.
- D: Scale does not remove bias; web-scale data often imports it.

**Q5 — A.** Grounding generation in retrieved external documents at query time is RAG.
- B: RLHF is a training-time alignment technique.
- C: Federated learning trains across decentralized data holders.
- D: Distillation compresses a model into a smaller one.

**Q6 — D.** Failure under small, natural distribution shifts = brittleness/lack of robustness.
- A: Hallucination is fabricated content, mainly in generative systems.
- B: Data leakage inflates test scores; it doesn't describe deployment fragility.
- C: Automation bias is a human overreliance behavior.

**Q7 — D.** Memorizing training data at the expense of generalization is overfitting.
- A: Underfitting is poor performance on both training and new data.
- B: Drift is degradation over time as the world changes.
- C: Poisoning is deliberate data corruption by an adversary.

**Q8 — B.** These seven characteristics are NIST AI RMF 1.0's trustworthiness vocabulary — exam gold.
- A: Commercial attributes, not trustworthiness characteristics.
- C: "Lawful, ethical, robust" is the EU HLEG trilogy, and it's incomplete here.
- D: Performance attributes, not the NIST set.

**Q9 — A.** Understandable outputs = explainability; answerability = accountability.
- B: Robustness/safety concern failure behavior, not understanding.
- C: Privacy/security concern data and attack resistance.
- D: Validity/reliability concern correctness and consistency.

**Q10 — B.** Equal meaning of scores across groups = calibration/predictive parity; unequal selection rates = demographic parity violated.
- A: Reversed.
- C: Differing selection rates rule out demographic parity.
- D: Individual fairness doesn't guarantee group metrics.

**Q11 — C.** With different base rates, calibration and error-rate-balance metrics are mutually incompatible — you must choose and justify.
- A: Overstates; technical mitigation still helps.
- B: Metrics extend beyond binary classification.
- D: No such ban exists.

**Q12 — D.** Automated action with human monitoring and after-the-fact intervention = human-ON-the-loop.
- A: HITL requires approval before effect; blocking happens automatically here.
- B: There is oversight — the analysts.
- C: HIC describes overarching authority, not this operational pattern.

**Q13 — C.** HIC = ultimate human authority over the decision to use the system at all, including kill-switch power.
- A: That's HITL.
- B: That's HOTL.
- D: Labeling is a data-preparation role.

**Q14 — B.** Polarization of public discourse is a collective, society-level harm.
- A: No single identified individual is the locus of harm.
- C: The harm described is civic, not corporate-financial.
- D: Societal harms are squarely within governance scope (and the AIGP BoK).

**Q15 — A.** One person harmed → individual; a demographic systematically disadvantaged → group; degraded democratic trust → societal.
- B: Items don't map to the three levels in order.
- C: Those are causes/control gaps, not harms.
- D: Those are technical failure modes, not harm categories.

**Q16 — D.** Operational ownership sits with a designated governance lead/office with executive sponsorship and cross-functional support.
- A: Boards oversee; they don't run programs model-by-model.
- B: Fully decentralized ownership = no accountability.
- C: External audit must stay independent of management.

**Q17 — C.** Board = oversight of risk appetite, strategy, and management accountability.
- A/B: Operational and technical tasks belong to management and teams.
- D: Intake approval is a management-committee function.

**Q18 — B.** Business owns risk (1st), risk/compliance sets policy and challenges (2nd), internal audit independently assures (3rd).
- A: Order scrambled.
- C: Outsourcing all three lines destroys the model's independence logic.
- D: External actors are not the organization's lines of defense.

**Q19 — A.** An advisory body with no mandate, authority or wired-in escalation path is governance theater; the process failure is structural.
- B: Composition wasn't the failure described.
- C: Emotion detection is restricted in specific contexts (e.g., EU workplaces), not universally illegal.
- D: Meeting cadence is irrelevant to being bypassed.

**Q20 — C.** Governance demands documented evaluation scope, failure modes and residual risk; "bias-free" is an unfalsifiable marketing claim.
- A: One benchmark cannot establish context-wide fairness.
- B: Nihilism isn't governance; assurance is about evidence, not perfection.
- D: Parameter count says nothing about bias.

---

## Score interpretation

| Score | Verdict |
|---|---|
| **17–20** | Ready — Domain I is exam-solid. Move on; re-test your misses at +2/+7 days. |
| **14–16** | Review weak areas — reread the specific lessons behind each miss (fairness and oversight modes are the usual culprits), journal every miss. |
| **< 14** | Redo the phase — go back through Phases 1–2 lesson by lesson before retaking this quiz. |
