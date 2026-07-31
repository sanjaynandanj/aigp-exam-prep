# High-Risk Obligations: Risk Management, Data Governance, Logging, Oversight

**Phase 4 · Lesson 04 · ~1.5h · BoK Domain II**

## EXAM FOCUS

Once a system is high-risk, two duty sets attach: the **system requirements + provider obligations** (Chapter III, Sections 2–3 — Arts. 8–17 territory) and the **deployer obligations** (Art. 26 territory, plus the FRIA in Art. 27). Exam questions either quiz a single requirement in depth (what must logging capture? what are the human-oversight measures?) or hand you a scenario and ask *which actor owes which duty*. Learn the seven system requirements as a unit — they are the most list-tested content in Domain II after Art. 5.

## CORE

### The seven requirements for high-risk AI systems (provider must ensure)

| # | Requirement (Art.) | Substance |
|---|---|---|
| 1 | **Risk management system** (Art. 9) | **Continuous, iterative process across the entire lifecycle**: identify reasonably foreseeable risks to health/safety/fundamental rights (intended use + reasonably foreseeable misuse), estimate/evaluate, adopt targeted mitigations in order (eliminate by design → mitigate/control → information/training to deployers), test against defined metrics incl. real-world testing where appropriate; special consideration for impacts on **persons under 18** and vulnerable groups; residual risk must be judged acceptable |
| 2 | **Data & data governance** (Art. 10) | Training/validation/testing datasets subject to governance practices: design choices, provenance and collection, preparation (labeling, cleaning), suitability assessment, **examination for possible biases** likely to affect health/safety/rights or cause prohibited discrimination, bias mitigation, gap identification. Datasets must be **relevant, sufficiently representative, and to the best extent possible error-free and complete for the intended purpose**, with appropriate statistical properties for the persons affected, considering the **geographical, contextual, behavioural or functional setting** of use. Narrow permission to process **special-category data strictly necessary for bias detection/correction** with strong safeguards |
| 3 | **Technical documentation** (Art. 11 / Annex IV) | Drawn up **before** market placement, kept current: general description, intended purpose, development process, architecture, data requirements, human-oversight measures, performance metrics and limits, risk management, changes, standards applied — enough for authorities to assess conformity. SMEs may use a simplified form |
| 4 | **Record-keeping / logging** (Art. 12) | Systems must **automatically record events (logs)** over their lifetime to ensure traceability appropriate to the intended purpose: identifying risk-situations and substantial modifications, facilitating post-market monitoring; for remote biometric ID: period of use, reference-database checks, input data, verifying humans. Providers keep logs under their control (≥ six months baseline, per contract/law) |
| 5 | **Transparency & information to deployers** (Art. 13) | Design so deployers can **interpret output and use it appropriately**; **instructions for use**: provider identity, characteristics/capabilities/limitations (intended purpose, accuracy incl. metrics, robustness, cybersecurity, known foreseeable misuse risks), human-oversight measures, expected lifetime/maintenance, log-collection mechanisms |
| 6 | **Human oversight** (Art. 14) | Designed for **effective oversight by natural persons** while in use, via measures built into the system and/or ones deployers implement, enabling overseers to: understand capacities/limits, **remain aware of automation bias**, correctly interpret output, **decide not to use / disregard / override / reverse** output, and **intervene or stop** (a "stop button" or similar). For remote biometric identification: no action on an identification unless **separately verified by at least two natural persons** (with narrow law-enforcement exceptions) |
| 7 | **Accuracy, robustness & cybersecurity** (Art. 15) | Appropriate levels achieved and consistent through lifecycle; declared accuracy metrics in instructions; resilience to errors/faults (fail-safes, redundancy), to feedback-loop risks in continuously learning systems, and to attacks — **data poisoning, model poisoning, adversarial examples/model evasion, confidentiality attacks** named as concerns |

### Provider obligations beyond the seven (Art. 16 cluster)

- Have a **quality management system** (Art. 17: strategy for regulatory compliance, design/development controls, testing, data management, post-market monitoring, incident reporting, communication, documentation control);
- Ensure/undergo **conformity assessment**, draw up **EU declaration of conformity**, affix **CE marking**, **register** in the EU database (Lesson 06);
- Keep documentation/logs for authorities (documents 10 years);
- **Corrective actions**: withdraw/disable/recall non-conforming systems, inform supply chain and authorities;
- **Post-market monitoring** system + plan; report **serious incidents** to market-surveillance authorities (baseline within **15 days** of awareness; faster for widespread infringement or death — know that timelines tighten with severity);
- Name, contact details on the system/packaging; accessibility compliance; cooperate with authorities.

### Deployer obligations (Art. 26 cluster)

| Duty | Substance |
|---|---|
| Use per **instructions** | Technical/organizational measures to ensure use follows the provider's instructions for use |
| **Human oversight** | Assign oversight to natural persons with the necessary **competence, training, authority and support** |
| **Input data control** | To the extent the deployer controls inputs: ensure they are **relevant and sufficiently representative** for the intended purpose |
| **Monitor** operation | Watch for risks per instructions; **suspend use and inform** provider/distributor and market surveillance if a serious risk emerges; report serious incidents |
| **Retain logs** | Logs under deployer control kept ≥ **6 months** (unless law provides otherwise) |
| **Worker notice** | Inform workers and their representatives before deploying high-risk AI in the workplace |
| **Downstream transparency** | Public authorities register their use in the EU database; inform natural persons subject to decisions where the system makes/assists **decisions about them**; credit/insurance deployers fold analysis into DPIAs |
| **GDPR bridge** | Use provider-supplied information to run DPIAs |

**Right to explanation:** affected persons subject to a decision based on a high-risk (Annex III) system's output that produces legal/similarly significant adverse effects can demand a **clear, meaningful explanation of the role of the AI system in the decision** — the AI Act's own mini-Art. 22.

### FRIA — Fundamental Rights Impact Assessment (Art. 27)

Required **before first use** for deployers that are **bodies governed by public law or private entities providing public services**, and for deployers of **creditworthiness/credit-scoring and life/health-insurance pricing** systems (the two Annex III 5(b)/(c) use cases). Content: description of deployment processes, period/frequency of use, categories of affected persons, specific risks of harm to them, human-oversight measures, and measures if risks materialize (governance, complaints). Notify the market-surveillance authority; may build on/complement an existing **DPIA**; update when elements change.

## CASES & EXAMPLES

**Scenario 1 — The unrepresentative dataset.** A dermatology-triage provider trains mostly on light-skinned images, then sells across the EU. *Analysis:* Art. 10 breach — datasets must be relevant, sufficiently representative and appropriate to the geographical/contextual setting, with bias examination and mitigation. Bias surfacing post-market also triggers risk-management iteration and possibly corrective action + incident reporting.

**Scenario 2 — Who trains the overseers?** A staffing agency buys a CV-ranking system; managers accept its rankings wholesale within weeks. *Analysis:* Provider must have designed oversight measures (incl. automation-bias awareness — Art. 14); the **deployer** must assign competent, trained, authorized overseers and ensure use per instructions (Art. 26). Rubber-stamping shows failed deployer oversight — and links to GDPR Art. 22 "solely automated" exposure.

**Scenario 3 — Public-sector FRIA.** A municipality deploys a benefits-eligibility scoring tool. *Analysis:* Public-law body + Annex III essential services → **FRIA before first use** (processes, affected categories, harm risks, oversight, remediation), notify the authority, register use in the EU database, inform affected persons, and give explanations for adverse decisions. The FRIA can build on the DPIA but doesn't replace it.

**Scenario 4 — The silent malfunction.** A high-risk grid-management AI misjudges load and causes a regional outage; the provider learns of it and quietly patches. *Analysis:* Serious incident (critical-infrastructure disruption) → mandatory report to market surveillance (15-day baseline, faster for severe cases), investigation, corrective action, documentation. "Patch quietly" is the wrong answer every time.

## MEMORY HOOKS

- **The seven requirements — "R-D-T-L-T-H-A":** *"**R**isk **D**ata **T**ech-docs **L**ogs **T**ransparency **H**umans **A**ccuracy"* — say it as a drumbeat: *Risk, Data, Docs, Logs, Tell, Human, Accurate.*
- **Human-oversight powers — "UDOIS":** **U**nderstand, **D**etect automation bias, **O**verride/disregard, **I**ntervene, **S**top.
- **Provider vs deployer in one line:** *providers build compliance into the product; deployers operate it responsibly* — docs/CE/registration vs instructions/oversight/monitoring/logs.
- **FRIA trigger memory:** *public bodies & public services + credit & life/health insurance deployers.*
- **Two-person rule:** remote biometric ID matches need verification by **two humans** before action.

**The 5 facts to retain:**
1. Seven high-risk system requirements: risk management, data governance, technical documentation, logging, transparency/instructions, human oversight, accuracy-robustness-cybersecurity.
2. Risk management is **lifecycle-continuous** and must weigh reasonably foreseeable misuse and impacts on minors/vulnerable groups.
3. Data governance demands relevant, sufficiently representative, bias-examined datasets fit to the deployment context — with a narrow special-category allowance solely for bias work.
4. Deployers owe: use per instructions, competent human oversight, input-data relevance, monitoring + suspension on serious risk, 6-month log retention, worker notice, affected-person information, and (for public-service and credit/insurance deployers) a pre-use **FRIA**.
5. Affected individuals get a **right to explanation** of the AI's role in significant adverse decisions; serious incidents must be reported (15-day baseline, faster when severe).

## SELF-CHECK

1. **Q:** List the seven requirements every high-risk AI system must meet.
   **A:** Risk management system; data and data governance; technical documentation; record-keeping/automatic logging; transparency and instructions for deployers; human oversight; accuracy, robustness and cybersecurity.

2. **Q:** What four abilities must human-oversight design give the humans monitoring a high-risk system?
   **A:** Understand the system's capacities/limits (staying alert to automation bias), correctly interpret outputs, decide to disregard/override or not use outputs, and intervene in or halt operation. (For RBI, add two-person verification of matches.)

3. **Q:** Which deployers must conduct a FRIA, and when?
   **A:** Public-law bodies and private providers of public services deploying Annex III systems, plus deployers of credit-scoring/creditworthiness and life & health insurance risk-pricing systems — before first use, updating it as elements change, and notifying the market-surveillance authority.

4. **Q:** Name four attack/failure types Art. 15's robustness-cybersecurity requirement explicitly targets.
   **A:** Data poisoning, model poisoning, adversarial examples/model evasion, confidentiality attacks — plus resilience to errors/faults and biased feedback loops in learning systems.

5. **Q:** A deployer notices its high-risk system presenting a serious risk. What is the required sequence?
   **A:** Suspend use, inform the provider (and distributor/importer as relevant) and the market-surveillance authority without undue delay, and report any serious incident; resume only when the risk is addressed.
