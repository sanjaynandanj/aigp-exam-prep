# Domain IV Quiz — Governing AI Deployment and Use

> 20 questions · ~30 minutes · closed book. Take after Phase 6.
> Domain IV is the "operations" domain: readiness, vendors, monitoring, oversight, incidents, audits, retirement.
> Answer key with full rationales at the bottom.

---

**Q1.** A deployment-readiness review for a consequential-decision AI system should confirm, at minimum:

- A. That the marketing launch materials are approved
- B. That the model's parameter count exceeds industry averages
- C. That documentation, testing evidence, monitoring plans, human-oversight arrangements, rollback procedures and user communications are all in place before go-live
- D. That the vendor has signed an NDA

**Q2.** *Scenario.* A hospital wants confidence in a sepsis-prediction model before letting it influence care. It runs the model silently on live patient data for eight weeks, comparing its alerts to clinicians' actual decisions, with no model output shown to staff. This technique is:

- A. Shadow deployment — parallel evaluation on production data without operational effect
- B. A/B testing on patients, which is what makes it lawful
- C. Red teaming
- D. Concept drift correction

**Q3.** Rolling a model out to 5% of traffic, monitoring KPIs and error rates, then progressively expanding, is called:

- A. Shadow deployment
- B. A staged (canary/phased) rollout
- C. Big-bang deployment
- D. Regression testing

**Q4.** *Scenario.* A bank is buying a third-party credit-decisioning model. Which due-diligence package is most defensible?

- A. A product demo and the vendor's marketing whitepaper
- B. The vendor's stock price history and headcount
- C. A verbal assurance that the model is "explainable and compliant"
- D. Evidence of training-data governance, validation and fairness-testing results, documentation (model card), security posture, regulatory alignment, and the vendor's monitoring/incident practices

**Q5.** Which contract-clause set most directly protects a deployer of vendor AI?

- A. Audit and information rights, performance/bias warranties, change-notification duties for model updates, incident notification SLAs, liability allocation, and cooperation with the deployer's regulatory obligations
- B. A perpetual license fee discount
- C. A non-compete clause preventing the vendor from serving competitors
- D. A clause forbidding the deployer from testing the model

**Q6.** Under the EU AI Act, a provider of a high-risk system must supply deployers with:

- A. The complete training dataset
- B. The model's source code and weights
- C. Instructions for use enabling the deployer to operate the system properly — including its capabilities, limitations, human-oversight measures and expected performance conditions
- D. Nothing, since obligations end at the point of sale

**Q7.** A fraud model degrades because the statistical relationship between the input features and fraud itself has changed (fraudsters changed tactics). The inputs' distribution looks similar. This is best described as:

- A. Data (covariate) drift
- B. Concept drift
- C. Label leakage
- D. Overfitting

**Q8.** *Scenario.* A production monitoring plan for a pricing model should specify — beyond dashboards — what?

- A. Only quarterly PowerPoint reviews
- B. That any drift automatically triggers full model deletion
- C. Nothing; monitoring is the vendor's problem in all cases
- D. Defined metrics with alert thresholds, ownership for response, and escalation paths that can trigger investigation, retraining, rollback or suspension

**Q9.** *Scenario.* A neighborhood-patrol allocation model sends more patrols to areas with more recorded incidents; more patrols generate more recorded incidents there, which increases future patrol allocations. This dynamic is:

- A. A self-reinforcing feedback loop that can entrench and amplify historical bias
- B. Proof the model is accurately learning ground truth
- C. Concept drift caused by criminals
- D. A hardware scaling problem

**Q10.** Which design measure most directly counteracts automation bias in human reviewers?

- A. Making the AI's recommendation the default that reviewers must click through quickly
- B. Paying reviewers per case processed
- C. Requiring reasons for overrides *and* for approvals in sampled cases, showing confidence/uncertainty information, and monitoring override rates for rubber-stamping
- D. Hiding from reviewers the fact that a machine produced the recommendation

**Q11.** *Scenario.* A radiologist's workstation flags scans as "AI: no abnormality." Audits show radiologists now miss more tumors on AI-cleared scans than they did before the tool existed. The phenomenon is:

- A. Model drift in the radiology AI
- B. Automation bias (and complacency) degrading human vigilance on AI-cleared cases
- C. Adversarial evasion by the scans
- D. Evidence the AI should make final decisions alone

**Q12.** The EU AI Act requires deployers of high-risk AI systems to assign human oversight to:

- A. Any available staff member, since presence is what counts
- B. The provider's engineers exclusively
- C. An external notified body on a monthly schedule
- D. Persons with the necessary competence, training, authority and support — able to understand, monitor, and if needed intervene in or suspend the system

**Q13.** Under the EU AI Act's transparency rules (Article 50), a customer-service chatbot must:

- A. Ensure people are informed they are interacting with an AI system, unless that is obvious from context
- B. Obtain a notified-body certificate before chatting
- C. Provide its full system prompt on request
- D. Be registered in the EU high-risk database

**Q14.** *Scenario.* A studio releases a hyper-realistic AI-generated video of a real politician appearing to say things he never said, as "satire," with no marking. Under the EU AI Act's transparency regime, deepfakes must:

- A. Be banned outright in all cases under Article 5
- B. Only be disclosed if the subject files a complaint first
- C. Be disclosed as artificially generated or manipulated (with accommodations for evidently artistic/satirical works in how disclosure is made — not a blanket exemption from it)
- D. Carry a CE marking

**Q15.** Under the EU AI Act, providers of high-risk systems must report serious incidents to market surveillance authorities:

- A. Only in an annual transparency report
- B. Without undue delay after establishing the causal link (or its reasonable likelihood), and at the latest within 15 days — with shorter deadlines for the gravest cases (e.g., 10 days for a death, 2 days for widespread infringement or critical-infrastructure disruption)
- C. Within 72 hours in all cases, mirroring GDPR
- D. Never; only deployers report incidents

**Q16.** *Scenario.* A deployer's HR team notices its high-risk screening tool behaving erratically, potentially harming candidates. Under the EU AI Act, the deployer's immediate duties include:

- A. Continuing use while quietly gathering more evidence for a quarter
- B. Deleting all logs to limit liability
- C. Reporting directly to the European Commission only, bypassing everyone else
- D. Suspending that use and informing the provider (and relevant authorities where required) — using its monitoring duty, logs and the provider's instructions as the framework

**Q17.** *Scenario.* An NYC employer's HR-analytics team proposes to run the annual LL144 bias audit itself "to save budget." This fails because LL144 requires:

- A. No audit at all if the tool's vendor is ISO-certified
- B. An **independent** auditor — one without a material interest in the employer or vendor — plus a published results summary and candidate notice
- C. The audit be performed by the EEOC
- D. Audits only when a candidate complains

**Q18.** In auditing AI systems, the distinguishing feature of the **third line** (internal audit) relative to second-line compliance reviews is:

- A. Independence from management of the activities audited, providing objective assurance to the board/audit committee
- B. It builds the models it audits
- C. It sets the AI risk policies the business must follow
- D. It reports to the head of data science

**Q19.** *Scenario.* A bank retires a loan-decisioning model after five years. Which decommissioning concern is MOST commonly missed?

- A. Telling the press
- B. Deleting the model's name from the intranet
- C. Retention obligations — preserving the model version, logs and decision records needed for pending disputes, audits and regulatory look-back periods before anything is destroyed
- D. Reusing the GPU cluster quickly

**Q20.** Article 4 of the EU AI Act requires providers and deployers to:

- A. Certify every employee as an AIGP
- B. Publish annual AI ethics reports
- C. Employ at least one PhD in machine learning
- D. Ensure a sufficient level of AI literacy in staff dealing with AI systems, accounting for their roles, context, and the persons affected

---

## ANSWER KEY & RATIONALES

**Q1 — C.** Readiness = the full operational package: documentation, test evidence, monitoring, oversight, rollback, and user comms — verified before go-live.
- A/D: Neither is a governance gate criterion.
- B: Size is not readiness.

**Q2 — A.** Silent parallel run on live data with no operational effect is the definition of shadow deployment.
- B: No outputs reached care, so it isn't A/B treatment of patients.
- C: No adversarial probing occurred.
- D: Nothing was corrected; it's evaluation.

**Q3 — B.** Progressive traffic expansion with monitoring = staged/canary rollout.
- A: Shadow mode has zero operational traffic.
- C: Big-bang is the opposite.
- D: Regression testing is pre-release verification.

**Q4 — D.** Defensible diligence demands evidence: data governance, validation/fairness results, documentation, security, regulatory fit, and the vendor's operational practices.
- A/C: Marketing and verbal assurances are not evidence.
- B: Financial health matters but is not AI diligence.

**Q5 — A.** These clauses operationalize the deployer's ability to know, verify, react and comply — the core of vendor-AI risk transfer that actually works.
- B: Commercial nicety, no risk coverage.
- C: Competition clause, irrelevant to risk.
- D: Anti-testing clauses are the opposite of protective.

**Q6 — C.** Providers owe deployers instructions for use covering capabilities, limitations, oversight measures and performance conditions — the interface that makes deployer duties performable.
- A/B: Neither datasets nor source code are required disclosures.
- D: Provider duties continue post-market (monitoring, corrective action).

**Q7 — B.** Changed input→outcome relationship with stable input distributions = concept drift.
- A: Covariate drift is input-distribution change.
- C: Leakage is a training-time evaluation flaw.
- D: Overfitting is a generalization failure, not temporal change.

**Q8 — D.** Monitoring is only governance when metrics, thresholds, owners and escalation (investigate/retrain/rollback/suspend) are defined in advance.
- A: Cadence decks aren't controls.
- B: Deletion as an automatic response is disproportionate.
- C: Deployers retain monitoring duties even with vendor models.

**Q9 — A.** Output-influences-future-input dynamics create self-reinforcing loops that can launder historical bias into "objective" allocations.
- B: Recorded incidents ≠ ground truth when recording depends on patrol presence.
- C: The loop, not offender behavior change, drives the pattern.
- D: Irrelevant.

**Q10 — C.** Countermeasures target the human factors: friction and reasons, uncertainty display, and metrics that expose rubber-stamping.
- A: Defaults + speed pressure amplify automation bias.
- B: Per-case pay incentivizes speed over scrutiny.
- D: Hiding AI involvement undermines transparency and vigilance.

**Q11 — B.** Vigilance decays on AI-cleared cases — classic automation complacency; the joint human-AI system can perform worse than the human baseline.
- A: Nothing indicates the model changed.
- C: No adversary in the fact pattern.
- D: A misread of the evidence; oversight design needs fixing, not removal.

**Q12 — D.** The Act requires competent, trained, authorized and supported overseers who can understand, monitor, intervene and suspend.
- A: Warm-body oversight is exactly what the Act rejects.
- B/C: Oversight is the deployer's operational duty, not outsourceable to provider engineers or notified bodies.

**Q13 — A.** Article 50: inform people they're interacting with AI unless obvious from context.
- B/D: Chatbots as such are transparency-tier, not high-risk certification/registration cases.
- C: No system-prompt disclosure right exists.

**Q14 — C.** Deepfakes must be disclosed as artificially generated/manipulated; artistic or satirical contexts adjust the manner of disclosure, they don't erase the duty.
- A: Deepfakes are transparency-regulated, not Article 5-prohibited per se.
- B: The duty is proactive.
- D: CE marking belongs to high-risk conformity, not content labeling.

**Q15 — B.** Article 73's ladder: without undue delay, ≤15 days generally; ≤10 days for death; ≤2 days for widespread infringement or critical-infrastructure serious incidents.
- A: Annual reporting is far too slow.
- C: 72 hours is the GDPR breach clock — a deliberate trap.
- D: Providers are the primary reporters; deployers inform providers.

**Q16 — D.** Deployer playbook: suspend the problematic use, inform the provider (and authorities where the incident is serious), preserve logs, follow instructions for use.
- A: Continued use compounds harm and liability.
- B: Log destruction violates retention duties and spoliation principles.
- C: The reporting chain runs through providers/market surveillance authorities, not solo Commission notices.

**Q17 — B.** LL144's audit must be independent (no material interest), with a public results summary and candidate notice; self-audit defeats the statute's design.
- A: No ISO substitute exists.
- C: The EEOC doesn't perform LL144 audits.
- D: Audits are annual and proactive.

**Q18 — A.** Third line = organizationally independent assurance to board/audit committee; second line advises and challenges but sits with management.
- B: Auditing what you built destroys objectivity.
- C: Policy-setting is second line.
- D: Reporting into data science would break independence.

**Q19 — C.** Retirement is a records-governance event: version, logs and decisions must survive for disputes, audits and look-back periods before deletion.
- A/B/D: None address the legal exposure that outlives the model.

**Q20 — D.** Article 4 requires role-appropriate AI literacy for staff operating/using AI systems — one of the earliest-applying duties (from February 2025).
- A: No certification mandate.
- B: No annual-report requirement in Article 4.
- C: No credential quota exists.

---

## Score interpretation

| Score | Verdict |
|---|---|
| **17–20** | Ready — operations governance is exam-solid; you're cleared for the mock. |
| **14–16** | Review weak areas — misses usually cluster on incident-reporting deadlines and oversight design; reread those lessons and journal each miss. |
| **< 14** | Redo the phase — rework Phase 6 before retaking; Domain IV carries 21–25 scored questions. |
