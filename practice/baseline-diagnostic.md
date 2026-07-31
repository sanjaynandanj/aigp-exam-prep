# Baseline Diagnostic — 20 Questions Before You Study Anything

> Take this **before** Phase 1. Closed book, ~25 minutes, no guessing penalty — answer everything.
> The point is not the score; it's the **per-domain study plan** the score generates (see the interpretation table at the bottom).
> Log every miss in [`question-journal-template.md`](question-journal-template.md).

Questions are ordered Domain I → IV, five per domain, easy → hard within each block.

---

## Domain I — Foundations of AI governance (Q1–Q5)

**Q1.** Under the OECD's revised (2023) definition, an AI system is best described as a machine-based system that:

- A. Executes explicitly programmed rules to automate repetitive human tasks
- B. Infers, from inputs, how to generate outputs such as predictions, content, recommendations or decisions that can influence environments
- C. Replicates human consciousness and general reasoning across any task
- D. Learns exclusively from labeled training data supplied by a human operator

**Q2.** A model is trained on historical loan files, each labeled "repaid" or "defaulted," to predict outcomes for new applicants. This is an example of:

- A. Unsupervised learning
- B. Reinforcement learning
- C. Supervised learning
- D. Self-supervised generative pretraining

**Q3.** A customer-service chatbot confidently cites a refund policy clause that does not exist anywhere in the company's documentation. The failure mode is:

- A. Model drift
- B. Overfitting
- C. Data poisoning
- D. Hallucination

**Q4.** In an oversight design where a human must review and approve each individual AI recommendation before it takes effect, the arrangement is called:

- A. Human-in-the-loop (HITL)
- B. Human-on-the-loop (HOTL)
- C. Human-in-command (HIC)
- D. Fully autonomous operation with audit logging

**Q5.** A hiring tool selects men and women at equal rates (equal selection rate), yet among rejected candidates, qualified women are rejected far more often than qualified men. The tool satisfies one fairness definition while violating another. This illustrates that:

- A. The tool is fair, because equal selection rates are the legally required metric everywhere
- B. Fairness can always be achieved by adding more training data
- C. Group fairness metrics and individual fairness metrics are mathematically identical
- D. Statistical fairness definitions can conflict, and satisfying one may still leave another violated

## Domain II — Laws, standards and frameworks (Q6–Q10)

**Q6.** The EU AI Act regulates AI systems primarily according to:

- A. The level of risk the system poses, in tiers from prohibited to minimal
- B. The sector in which the developer is incorporated
- C. The size of the company deploying the system
- D. Whether the system uses deep learning or classical statistics

**Q7.** GDPR Article 22 gives individuals the right not to be subject to a decision that is:

- A. Based on any use of personal data in an automated system
- B. Made by an AI system of any risk level operating in the EU
- C. Based solely on automated processing and produces legal or similarly significant effects
- D. Made with partial human involvement, regardless of its effects

**Q8.** Which of the following is a **prohibited practice** under Article 5 of the EU AI Act (rather than merely high-risk)?

- A. AI used to screen job applications
- B. AI used to evaluate creditworthiness of consumers
- C. Social scoring of natural persons leading to detrimental treatment in unrelated contexts
- D. AI used as a safety component in critical infrastructure

**Q9.** The four functions of the NIST AI Risk Management Framework are:

- A. Identify, Protect, Detect, Respond
- B. Plan, Do, Check, Act
- C. Govern, Map, Measure, Manage
- D. Assess, Mitigate, Monitor, Report

**Q10.** New York City Local Law 144 requires employers using automated employment decision tools to, among other things:

- A. Obtain a CE marking before deployment
- B. Obtain written consent from every applicant before any automated scoring
- C. Register the tool in an EU database
- D. Commission an annual independent bias audit and publish a summary of results

## Domain III — Governing AI development (Q11–Q15)

**Q11.** "Data provenance" in AI development refers primarily to:

- A. The documented origin, chain of custody and licensing of data used to build a model
- B. The statistical distribution of the training data
- C. The physical location of the servers storing the data
- D. The anonymization technique applied before training

**Q12.** A model card differs from a datasheet (for datasets) mainly in that a model card documents:

- A. The provenance, composition and collection process of a dataset
- B. A trained model's intended use, performance across subgroups, and limitations
- C. The corporate ownership structure of the AI provider
- D. The energy consumption of the training run only

**Q13.** Red teaming an AI system before release means:

- A. Having an adversarial team deliberately probe the system for harmful outputs, vulnerabilities and misuse paths
- B. Running standard accuracy benchmarks on a held-out test set
- C. Marking high-risk code sections in red during code review
- D. Outsourcing the model's development to a third party

**Q14.** During training-data collection for a facial-analysis product, an attacker deliberately inserts mislabeled images to corrupt the model's future behavior. This attack is:

- A. Model inversion
- B. Membership inference
- C. Prompt injection
- D. Data poisoning

**Q15.** A company licenses a general-purpose model, fine-tunes it substantially, rebrands it under its own trademark, and markets it in the EU for CV screening. Under the EU AI Act, the company most likely:

- A. Remains a deployer, because it did not build the original model
- B. Becomes a provider of a high-risk AI system, assuming provider obligations
- C. Is an importer with documentation-verification duties only
- D. Has no obligations because the original developer retains all responsibility

## Domain IV — Governing AI deployment and use (Q16–Q20)

**Q16.** "Shadow deployment" of a model means:

- A. Deploying a model without informing the governance committee
- B. Hiding a model's existence from end users
- C. Deploying a model only in jurisdictions without AI regulation
- D. Running the new model in parallel on live inputs without acting on its outputs, to compare against the incumbent process

**Q17.** Six months after go-live, a demand-forecasting model's error rate climbs steadily because customer behavior changed after a price restructure. This phenomenon is:

- A. Data poisoning
- B. Model drift
- C. Automation bias
- D. Overfitting to the test set

**Q18.** A loan officer approves nearly 100% of an AI credit model's recommendations, including several she privately doubted, because "the system is usually right." This behavior pattern is called:

- A. Adversarial evasion
- B. Confirmation sampling
- C. Automation bias
- D. Human-in-command oversight

**Q19.** A bank buys a third-party credit-scoring model. Which contract clause set best addresses AI-specific vendor risk?

- A. Audit/information rights, performance and bias-testing warranties, incident-notification duties, and support for the bank's regulatory obligations
- B. Standard uptime SLA and indemnity for IP infringement only
- C. A clause transferring all regulatory liability to the vendor, with no information rights
- D. A confidentiality clause preventing the bank from disclosing the model's use to regulators

**Q20.** Under the EU AI Act, when a provider's high-risk AI system malfunction leads to a serious incident, the provider must report it to:

- A. The end users of the system only
- B. The European Data Protection Board within 72 hours
- C. The relevant market surveillance authority within prescribed deadlines
- D. A notified body, which decides whether authorities need to know

---

## ANSWER KEY — with domain and study mapping

| Q | Answer | Domain | If missed, study |
|---|--------|--------|------------------|
| 1 | B | I | Phase 1, Lesson 01 (OECD definition) |
| 2 | C | I | Phase 1, Lesson 02 (ML types) |
| 3 | D | I | Phase 1, Lesson 08 (failure modes) |
| 4 | A | I | Phase 2, Lesson 05 (HITL/HOTL/HIC) |
| 5 | D | I | Phase 2, Lesson 03 (fairness definitions) |
| 6 | A | II | Phase 4, Lesson 01 (AI Act structure & risk pyramid) |
| 7 | C | II | Phase 3, Lesson 02 (GDPR Article 22) |
| 8 | C | II | Phase 4, Lesson 02 (Art. 5 prohibitions) |
| 9 | C | II | Phase 4, Lesson 08 (NIST AI RMF) |
| 10 | D | II | Phase 3, Lesson 05 (US state AI laws) |
| 11 | A | III | Phase 5, Lesson 03 (data governance & provenance) |
| 12 | B | III | Phase 5, Lesson 07 (model cards, datasheets) |
| 13 | A | III | Phase 5, Lesson 05 (testing, evaluation, red teaming) |
| 14 | D | III | Phase 5, Lesson 08 (adversarial ML & security) |
| 15 | B | III | Phase 5, Lesson 10 + Phase 4, Lesson 01 (provider vs deployer) |
| 16 | D | IV | Phase 6, Lesson 01 (deployment readiness) |
| 17 | B | IV | Phase 6, Lesson 04 (monitoring & drift) |
| 18 | C | IV | Phase 6, Lesson 05 (human oversight & automation bias) |
| 19 | A | IV | Phase 6, Lessons 02–03 (vendor risk & procurement) |
| 20 | C | IV | Phase 6, Lesson 07 (incident response & reporting) |

## Scoring interpretation — build your study plan

Score each domain separately (5 questions each):

| Correct in domain | Interpretation | What to do |
|---|---|---|
| 0–1 | Cold start | **Full study** of every lesson in that domain's phases; do all self-checks |
| 2–3 | Partial familiarity | **Normal pace** through the domain's phases; extra time on the lessons behind your misses |
| 4–5 | Strong base | **Skim** the domain's lessons via EXAM FOCUS + MEMORY HOOKS; jump straight to the domain quiz and only backfill where the quiz exposes gaps |

Two rules regardless of score:

1. **Every miss goes in the question journal** with the +2-day and +7-day re-test schedule.
2. **A perfect diagnostic domain does not exempt you from that domain's 20-question quiz** — the diagnostic is 5 questions; the exam asks 16–25 per domain.
