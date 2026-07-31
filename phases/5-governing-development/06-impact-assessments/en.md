# Impact Assessments: AIA vs DPIA vs FRIA vs Conformity Assessment

**Phase 5 · Lesson 06 · ~1.5h · BoK Domain III**

## EXAM FOCUS

A guaranteed exam area, and a favorite distractor factory: four assessment types with overlapping names and different triggers, scopes, and owners. Master the comparison table below. Classic traps: confusing the DPIA (data-protection law) with the FRIA (EU AI Act Art. 27 concept), assigning the FRIA to providers (it belongs to certain *deployers*), and treating conformity assessment as an ethics review (it is a pre-market compliance verification).

## CORE

### The four instruments

| | **DPIA** | **AIA (Algorithmic Impact Assessment)** | **FRIA** (EU AI Act Art. 27 concept) | **Conformity assessment** (EU AI Act concept) |
|---|---|---|---|---|
| **Legal home** | GDPR (and similar privacy laws) | Policy/soft-law & some statutes (e.g., Canada's Directive on Automated Decision-Making; Colorado AI Act-style impact assessments) | EU AI Act Art. 27 | EU AI Act (high-risk chapter) |
| **Trigger** | Processing likely to result in **high risk to rights and freedoms** of individuals (profiling, large-scale sensitive data, etc.) | Deploying an automated decision system covered by the policy/statute | Deploying certain **high-risk AI**: deployers that are public bodies / provide public services, plus specific private uses (e.g., creditworthiness, life/health insurance pricing concepts) | **Before placing a high-risk AI system on the market** or putting it into service |
| **Owner** | **Controller** (data-protection role) | The deploying organization/agency | **Deployer** | **Provider** (mostly self-assessment; notified body in specific cases like certain biometrics) |
| **Scope** | Risks to individuals from *personal-data processing*; necessity & proportionality; mitigations | Broader socio-technical impacts of the automated decision: fairness, recourse, transparency, service impact | Impacts on **fundamental rights** of affected persons: categories affected, specific risks, oversight measures, mitigation/complaint arrangements | Verification that the system meets the Act's **technical requirements** (risk management, data governance, documentation, logging, oversight, accuracy/robustness/cybersecurity) |
| **Output** | DPIA report; prior consultation with the supervisory authority if residual risk stays high | Risk score/tier driving required mitigations (Canada's AIA questionnaire produces impact Levels I–IV) | FRIA record; notify the market surveillance authority (concept); can build on the DPIA | EU declaration of conformity, CE marking, registration in the EU database |
| **Timing** | Before processing starts | Before deployment (and on material change) | **Before first use** of the system | Before market placement; repeat on substantial modification |

Key relationships:

- These instruments **stack, not substitute**: one high-risk HR screening tool deployed by a bank in the EU could require the provider's conformity assessment *and* the deployer's DPIA *and* (if in scope) a FRIA.
- The FRIA may **leverage the DPIA** — the Act contemplates the FRIA complementing an existing DPIA rather than duplicating it.
- Necessity/proportionality thinking (from intake, Lesson 02) is the common analytical spine of DPIA/AIA/FRIA.

### The Canadian AIA as a concrete example

Canada's federal **Directive on Automated Decision-Making** requires an **Algorithmic Impact Assessment** — a public, standardized questionnaire — before federal institutions deploy automated decision systems. Answers produce an impact level (I–IV); higher levels mandate stronger measures (peer review, human-in-the-loop, notice, explanation). It is the exam's go-to real-world AIA example: questionnaire-based, tiered, public-sector, published results.

### Running an assessment well

Whatever the instrument, quality markers are the same: done **early enough to change the design** (ex ante), documented assumptions, consultation with affected stakeholders where feasible, named owner and reviewer, mitigation actions tracked to closure, and **re-assessment on material change** (new population, new purpose, major retrain).

## CASES & EXAMPLES

**Scenario 1 — which assessment?** A city government will deploy a vendor's high-risk AI system to prioritize social-benefit fraud investigations in the EU. Which assessments, by whom? *Answer:* the **vendor/provider** completes conformity assessment before market placement; the **city (deployer, public body)** conducts a FRIA before first use and a DPIA (personal data, high risk to individuals). All three coexist.

**Scenario 2 — the swap trap.** Stem: "Under the EU AI Act, which actor must assess the fundamental-rights impact before using a high-risk system for creditworthiness decisions?" Distractors offer "the provider" and "the notified body." *Answer:* the **deployer** (Art. 27 concept). Providers do conformity assessment; notified bodies verify conformity in limited categories.

**Scenario 3 — Canada.** A Canadian federal department automates immigration-application triage. Before launch it must complete the AIA questionnaire; the resulting impact level dictates mitigations such as human review of decisions and public notice. *Exam point:* AIA = questionnaire → impact level → scaled obligations.

**Scenario 4 — re-assessment.** A hiring tool assessed last year is repurposed to also rank internal promotion candidates. *Exam point:* material change of purpose/population → refresh the impact assessment(s); assessments are living documents, not one-time paperwork.

## MEMORY HOOKS

**Owner mnemonic — "Providers Conform, Deployers Feel the Rights":** provider → conformity assessment; deployer → FRIA. DPIA → whoever is the data **controller**.

**Scope ladder:** DPIA = privacy risks · AIA = decision-system impacts · FRIA = fundamental rights · Conformity = technical/legal requirements checklist.

The 5 facts to retain:

1. DPIA: controller-owned, triggered by high-risk personal-data processing, may require regulator consultation if residual risk stays high.
2. FRIA (EU AI Act Art. 27 concept): deployer-owned, before first use of certain high-risk systems — mainly public bodies/public services plus specified private uses; can build on the DPIA.
3. Conformity assessment: provider-owned, pre-market verification of high-risk technical requirements → declaration of conformity, CE marking, EU database registration; redo on substantial modification.
4. Canada's Directive on Automated Decision-Making AIA: public questionnaire → impact Levels I–IV → scaled mitigations; the model AIA regime.
5. The instruments stack — one deployment can lawfully require several — and all must be refreshed on material change.

## SELF-CHECK

1. **Who owns the FRIA and when must it be done?**
   The deployer (in-scope categories: public bodies/public-service providers and specified private uses), before first use of the high-risk system.
2. **What triggers a DPIA, and what happens if high residual risk remains?**
   Processing likely to result in high risk to individuals' rights and freedoms; if mitigations leave risk high, prior consultation with the data-protection supervisory authority.
3. **What are the outputs of a successful conformity assessment?**
   EU declaration of conformity, CE marking, and registration in the EU database — permitting market placement of the high-risk system.
4. **How does Canada's AIA determine the strength of required mitigations?**
   A standardized questionnaire scores the system into impact Levels I–IV; higher levels trigger stronger measures (peer review, human involvement, notice/explanation).
5. **A provider substantially modifies a high-risk system already on the market. Assessment consequence?**
   The conformity assessment must be repeated for the modified system (and deployers should refresh FRIAs/DPIAs if use or impact materially changes).
