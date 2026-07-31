# Domain III Quiz — Governing AI Development

> 20 questions · ~30 minutes · closed book. Take after Phase 5.
> Domain III tests whether you can run governance **through the build lifecycle** — intake to release gate.
> Answer key with full rationales at the bottom.

---

**Q1.** The primary purpose of stage gates in an AI development lifecycle is to:

- A. Slow development to reduce compute costs
- B. Force a documented go/no-go decision with defined evidence and accountable approvers before risk accumulates in the next stage
- C. Replace the need for post-deployment monitoring
- D. Ensure only senior engineers write model code

**Q2.** *Scenario.* A product team proposes an AI feature to infer employees' likelihood of resigning from their emails and calendar data. At use-case intake, the governance function's **first** action should be:

- A. Approve it and rely on post-deployment monitoring to catch problems
- B. Ask engineering to select the model architecture
- C. Buy insurance against employment claims
- D. Screen it against the organization's ban list and legal constraints (e.g., workplace surveillance and emotion-inference restrictions) before any build work

**Q3.** *Scenario.* A team wants to train on a popular web-scraped image dataset with no documented licensing, consent basis, or collection methodology. The core **data governance** problem is:

- A. Missing provenance: unknown origin, rights and lawfulness make downstream compliance claims (IP, privacy, quality) unverifiable
- B. The dataset is too small for deep learning
- C. Images are harder to store than text
- D. Web data cannot legally be used for training in any jurisdiction

**Q4.** The tension between GDPR's data-minimization principle and ML practice is best resolved by:

- A. Ignoring minimization, since AI is exempt
- B. Always training on the full raw dataset to maximize accuracy
- C. Defining what data is genuinely necessary for the stated purpose, and using techniques like sampling, pseudonymization, and de-identification to limit personal data used
- D. Collecting everything but storing it encrypted

**Q5.** Poor labeling quality in supervised training data most directly threatens which trustworthiness property?

- A. Privacy
- B. Validity and reliability of the model's outputs
- C. Energy efficiency
- D. Interpretability of the architecture

**Q6.** "Disaggregated evaluation" in fairness testing means:

- A. Measuring performance separately across demographic subgroups instead of relying on a single aggregate metric
- B. Splitting the test set randomly into ten folds
- C. Testing each neural-network layer independently
- D. Evaluating the model on data from a different country

**Q7.** *Scenario.* A US hiring-tool developer compares selection rates: the protected group's rate is 45%, the reference group's is 75%. The ratio is 0.6. Under the four-fifths (80%) rule of thumb used in employment analytics, this indicates:

- A. No concern, because both rates exceed 40%
- B. A violation of the EU AI Act's accuracy requirements
- C. Definitive proof of intentional discrimination
- D. Evidence of potential adverse impact warranting investigation, since 0.6 falls below the 0.8 threshold

**Q8.** Red teaming differs from standard model evaluation because it:

- A. Uses only automated benchmark suites
- B. Is performed exclusively by regulators
- C. Adversarially searches for failures, misuse paths and harmful outputs beyond expected use, rather than measuring performance on anticipated inputs
- D. Happens only after public release

**Q9.** *Scenario.* A lab's newest general-purpose model crosses the EU AI Act's systemic-risk compute presumption. Beyond baseline GPAI duties, the provider must additionally:

- A. Withdraw the model from the EU market permanently
- B. Perform model evaluations including adversarial testing, assess and mitigate systemic risks, report serious incidents, and ensure adequate cybersecurity
- C. Open-source the model weights
- D. Obtain individual consent from every EU internet user

**Q10.** The cleanest distinction between an **algorithmic impact assessment (AIA)** and a **DPIA** is:

- A. The AIA examines an AI system's broader risks (fairness, safety, rights, societal effects); the DPIA is a GDPR-mandated assessment focused on risks to individuals from personal-data processing
- B. They are identical documents with different logos
- C. A DPIA covers all AI risks; an AIA covers only privacy
- D. AIAs are legally required everywhere; DPIAs are always voluntary

**Q11.** Under the EU AI Act, a fundamental rights impact assessment (FRIA) must be carried out before first use of certain high-risk systems by:

- A. Every provider of any AI system, including minimal-risk
- B. Only notified bodies
- C. Any company with more than 250 employees, regardless of what it deploys
- D. Deployers that are public bodies or private entities providing public services, and deployers using high-risk AI for credit scoring or life/health insurance risk assessment

**Q12.** For most Annex III high-risk AI systems (e.g., employment, credit), the EU AI Act's conformity assessment route is:

- A. Mandatory third-party testing by the AI Office in Brussels
- B. A public referendum in the deploying member state
- C. Internal control — the provider self-assesses against the requirements, draws up the EU declaration of conformity and affixes CE marking (notified-body involvement is chiefly for biometrics and product-embedded AI)
- D. Certification by ISO, which is legally required

**Q13.** Which content belongs in a **model card**?

- A. The provider's quarterly revenue figures
- B. Intended use and out-of-scope uses, evaluation results disaggregated across conditions/subgroups, limitations, and ethical considerations of the trained model
- C. Only the dataset's collection methodology
- D. Employee performance reviews of the ML team

**Q14.** *Scenario.* An acquirer's diligence team asks specifically how a dataset was collected, what it contains, known gaps, consent basis, and recommended uses. The artifact designed to answer exactly these questions is:

- A. A datasheet for datasets
- B. A model card
- C. A CE marking certificate
- D. A confusion matrix

**Q15.** An attacker subtly perturbs a stop-sign image so a vision model classifies it as a speed-limit sign, while humans see a normal stop sign. This is:

- A. Data poisoning of the training set
- B. Membership inference
- C. Prompt injection
- D. An evasion attack using an adversarial example at inference time

**Q16.** The difference between **model inversion** and **membership inference** is:

- A. Inversion targets vision models; membership inference targets language models
- B. Both are defenses, not attacks
- C. Model inversion reconstructs (approximations of) training-data attributes from the model; membership inference determines whether a specific record was in the training set
- D. Model inversion requires physical access to servers; membership inference does not involve the model

**Q17.** *Scenario.* A team downloads a pretrained open-source model file from an unofficial mirror; it later executes malicious code embedded in the serialized model artifact. The governance lesson is:

- A. Open-source models can never be used in enterprises
- B. AI supply-chain security requires provenance verification, trusted sources, artifact scanning and safe serialization formats — models are executable supply-chain artifacts, not passive data
- C. The problem would vanish if the model were larger
- D. Malware is out of scope for AI governance programs

**Q18.** *Scenario.* At the release gate for a credit model, the data science lead says accuracy targets are met and demands launch. Fairness testing across protected groups was skipped "for time." The correct release-gate outcome is:

- A. Launch, because accuracy is the only gate criterion
- B. Launch, but ask legal to watch for complaints
- C. Let the data science lead decide alone, since it's their model
- D. No-go: the gate's defined evidence package (including fairness evaluation for a consequential-decision model) is incomplete, and the accountable approver must withhold sign-off

**Q19.** *Scenario.* A distributor takes a provider's high-risk AI system and markets it in the EU under the distributor's **own name and trademark**, without any agreement stating otherwise. Under the EU AI Act, the distributor:

- A. Is now considered the provider and assumes provider obligations for the system
- B. Remains a mere distributor with no new duties
- C. Becomes a notified body
- D. Escapes the Act entirely, because rebranding removes the original CE marking's validity

**Q20.** *Scenario.* A deployer takes a provider's high-risk recruitment model and retrains it to make automated final rejections in a new domain (tenant screening) — a purpose the provider never intended. The most accurate analysis under the EU AI Act:

- A. The original provider remains solely responsible forever
- B. Nothing changes so long as the deployer keeps the provider's user manual
- C. By substantially modifying the system and changing its intended purpose, the deployer becomes the provider of the (new) high-risk system, taking on provider obligations
- D. The system is now exempt because tenant screening is not in Annex III

---

## ANSWER KEY & RATIONALES

**Q1 — B.** Gates exist to force evidence-based go/no-go decisions with named approvers before the next stage compounds risk.
- A: Cost control is incidental.
- C: Monitoring remains essential post-release.
- D: Gates govern decisions, not staffing seniority.

**Q2 — D.** Intake screening against ban lists and legal red lines (surveillance, emotion inference in workplaces under the AI Act) comes before any design work.
- A: "Ship then watch" inverts the lifecycle.
- B: Architecture is premature before permissibility.
- C: Insurance doesn't make an impermissible use case permissible.

**Q3 — A.** Provenance is the foundation: without documented origin, rights, and lawfulness, IP, privacy and quality assurances downstream are unverifiable.
- B: Scale isn't the issue raised.
- C: Storage is irrelevant.
- D: Overbroad — web data can be usable subject to rights and legal analysis.

**Q4 — C.** Minimization applies to AI; the resolution is necessity analysis plus privacy-preserving techniques, not exemption or maximalism.
- A: No AI exemption exists.
- B: "Everything, always" is the opposite of the principle.
- D: Encryption is security, not minimization.

**Q5 — B.** Garbage labels → the model learns wrong mappings → invalid, unreliable outputs.
- A: Labeling quality is orthogonal to privacy.
- C/D: Unrelated properties.

**Q6 — A.** Aggregate metrics hide subgroup failures; disaggregated evaluation reports performance per subgroup/condition.
- B: That's cross-validation.
- C: That's an interpretability/debugging technique.
- D: That's out-of-distribution testing.

**Q7 — D.** 0.45/0.75 = 0.6 < 0.8 → potential adverse impact flag warranting investigation and justification/validation — a screening heuristic, not proof.
- A: Absolute rates aren't the test; the ratio is.
- B: The four-fifths rule is US employment analytics, not the AI Act.
- C: Disparate impact analysis doesn't establish intent.

**Q8 — C.** Red teaming is adversarial discovery of failure and misuse beyond intended use — complementary to benchmark evaluation.
- A: It's typically human-led (optionally tool-assisted), open-ended.
- B: Providers and independent testers do it, not just regulators.
- D: It is most valuable pre-release (and repeated after).

**Q9 — B.** Systemic-risk GPAI adds: model evaluation with adversarial testing, systemic-risk assessment/mitigation, serious-incident tracking and reporting, and cybersecurity protection.
- A: No withdrawal duty.
- C: Open-sourcing is not required (and doesn't erase systemic-risk duties).
- D: No such consent mechanism exists.

**Q10 — A.** AIA = broad AI-risk lens (rights, fairness, safety, societal); DPIA = GDPR Article 35 instrument scoped to personal-data risks. They overlap but aren't substitutes.
- B/C: Scopes differ and neither subsumes the other.
- D: Legal status is roughly the reverse where DPIAs are triggered.

**Q11 — D.** Article 27 places FRIA duties on deployers that are public bodies or private providers of public services, plus deployers using high-risk AI for credit scoring and life/health insurance risk pricing.
- A: It's a deployer duty for defined categories, not all providers.
- B: Notified bodies assess conformity, not FRIAs.
- C: Headcount is not the criterion.

**Q12 — C.** Most Annex III systems use the internal-control route: self-assessment, technical documentation, EU declaration of conformity, CE marking; notified bodies enter mainly for biometric systems (absent harmonized standards) and Annex I product-embedded AI.
- A: The AI Office doesn't test individual high-risk systems for conformity.
- B: Fabricated.
- D: ISO certification is voluntary support, not the legal route.

**Q13 — B.** Model cards document the trained model: intended/out-of-scope use, disaggregated performance, limitations, ethical considerations.
- A/D: Corporate/HR content doesn't belong.
- C: Dataset collection detail is the datasheet's job.

**Q14 — A.** Datasheets for datasets answer exactly: motivation, composition, collection, consent, gaps, recommended uses.
- B: Model cards describe models, not dataset collection.
- C: CE marking is a conformity claim, not documentation of a dataset.
- D: A confusion matrix is one evaluation artifact.

**Q15 — D.** Inference-time perturbation crafted to flip the classification = evasion via adversarial example.
- A: Poisoning corrupts training, not inference inputs.
- B: Membership inference extracts training-set membership.
- C: Prompt injection targets instruction-following LLMs.

**Q16 — C.** Inversion ≈ reconstruct training-data attributes; membership inference ≈ "was this exact record in training?" Both are privacy attacks on models.
- A: Neither is modality-restricted.
- B: They are attacks.
- D: Neither requires physical access; both query the model.

**Q17 — B.** Model artifacts are executable supply-chain components; controls = trusted sources, provenance/signature verification, scanning, safe serialization.
- A: Overbroad; open source is manageable with controls.
- C: Size is irrelevant.
- D: Model-borne malware is squarely an AI security-governance issue.

**Q18 — D.** A gate without enforced evidence requirements is decoration; missing fairness evaluation on a consequential-decision model = incomplete package = no-go.
- A: Accuracy alone was never the full gate.
- B: "Launch and hope" defeats the gate's purpose.
- C: Self-approval by the builder violates separation of duties.

**Q19 — A.** Putting your name/trademark on a high-risk system makes you the provider under the Act (Article 25 logic) — with the full obligations that follow.
- B: Rebranding is exactly what triggers the shift.
- C: Notified bodies are designated assessment organizations, not market actors.
- D: Obligations transfer; they don't evaporate.

**Q20 — C.** Substantial modification / change of intended purpose converts the deployer into the provider of the resulting high-risk system.
- A: Responsibility for the modified system shifts (the original provider must cooperate/hand over documentation, not carry the new system).
- B: Keeping the manual is irrelevant once purpose and behavior change.
- D: Essential private services (and the employment-adjacent screening context) keep it in high-risk territory; exemption is wishful thinking.

---

## Score interpretation

| Score | Verdict |
|---|---|
| **17–20** | Ready — lifecycle governance is solid; carry the provider/deployer-shift logic into Domain IV. |
| **14–16** | Review weak areas — the usual gaps are assessment-type distinctions (AIA/DPIA/FRIA/conformity) and the attack taxonomy; reread those lessons and journal each miss. |
| **< 14** | Redo the phase — rework Phase 5 lesson by lesson before retaking this quiz. |
