# Conformity Assessment, CE Marking, Notified Bodies, the EU Database

**Phase 4 · Lesson 06 · ~1h · BoK Domain II**

## EXAM FOCUS

This is the product-law machinery of the AI Act — the part privacy professionals find most alien, which is exactly why the exam tests it. Know: the **two assessment routes** (internal control vs notified body) and **when each applies**, what **CE marking** and the **EU declaration of conformity** are, **registration** in the EU database, the **presumption of conformity** from harmonized standards, and what **substantial modification** does to a completed assessment.

## CORE

### What conformity assessment is

The process of **demonstrating, before market placement**, that a high-risk AI system meets the seven requirements (Lesson 04). It is the gate between development and the EU market — the AI Act's pre-market control, borrowed from the New Legislative Framework used for machinery, toys, and medical devices.

### The two routes

| Route | Who assesses | When it applies |
|---|---|---|
| **Internal control** (self-assessment, Annex VI concept) | The **provider itself** verifies its QMS, technical documentation, and design meet requirements | **The default for almost all Annex III high-risk systems** — employment, education, credit, essential services, law enforcement, migration, justice systems all self-assess |
| **Third-party assessment** (notified body, Annex VII concept) | An independent **notified body** examines the QMS and technical documentation | (1) **Biometrics** (Annex III point 1) — *and even then only if* harmonized standards/common specifications were **not** applied fully; (2) **Annex I products** — where sectoral law already requires third-party assessment, the AI requirements ride inside that sectoral procedure |

**The exam's favorite subtlety:** the AI Act relies overwhelmingly on **self-assessment** — a deliberate contrast with medical-device-style regimes and a common critique of the Act. Third-party involvement is the exception, not the rule.

### Notified bodies

- **Conformity assessment bodies** that apply to a national **notifying authority**, demonstrate competence, independence, and confidentiality, and are then **notified to the Commission** (listed in the NANDO database with an ID number).
- They audit providers' QMS and technical documentation, issue certificates (validity periods with renewals), conduct surveillance, and can suspend/withdraw certificates.
- Providers can choose any EU notified body designated for the relevant AI scope.

### Harmonized standards & the presumption of conformity

- **Harmonized standards** (developed by CEN/CENELEC JTC 21 under a Commission standardization request, cited in the Official Journal) give a **presumption of conformity** with the requirements they cover — follow the standard, and you're presumed compliant on that requirement.
- Where standards are absent/insufficient, the Commission can adopt **common specifications** as a fallback with the same presumption effect.
- This is why standards work (and delays in it) dominates AI Act implementation discourse — without cited standards, self-assessment is harder to evidence. (Standards citation status as of mid-2026 — verify.)

### The compliance parade — provider's pre-market checklist (order matters)

1. Build the system to the seven requirements + run the **QMS**;
2. Compile **technical documentation** (Annex IV);
3. Run/undergo the **conformity assessment** (internal control or notified body);
4. Draw up the **EU declaration of conformity (DoC)** — a signed legal statement, per system, that it complies; keep 10 years; provide to authorities on request. Signing it means **assuming responsibility for compliance**;
5. Affix the **CE marking** — visibly, legibly, indelibly (physically or digitally for software) — with the notified body's ID number where one was involved;
6. **Register** the system (provider + system info) in the **EU database** for high-risk AI (public, Commission-run) — including Art. 6(3) derogation claims; public-authority deployers register their *use*;
7. Place on market → then operate **post-market monitoring**, incident reporting, corrective actions.

### Substantial modification

A **substantial modification** = a change not foreseen in the provider's initial assessment that affects compliance or the intended purpose. Consequences:
- The system must undergo a **new conformity assessment**;
- Whoever makes the substantial modification (e.g., a deployer) **becomes the provider** (Lesson 01 role-switch);
- Not substantial: changes **pre-determined** by the provider and covered in the initial documentation — the Act's accommodation of **continuously learning systems** (declare the learning envelope up front, like an FDA PCCP).

### Related valves

- **Derogation:** market-surveillance authorities can authorize placing a specific high-risk system on the market **before** assessment for exceptional public-security/health/safety reasons (temporary, conditioned).
- **Regulatory sandboxes:** every member state must provide at least one **AI regulatory sandbox** — supervised testing environments (incl. real-world testing under conditions) to foster innovation, with priority SME access. Exiting the sandbox doesn't waive conformity — it eases the path to it.
- Certificates, DoCs, and registrations are what **importers/distributors must verify** before handling a system (their Lesson 01 duties connect here).

## CASES & EXAMPLES

**Scenario 1 — Which route?** (a) A vendor of an exam-proctoring system (education, Annex III). (b) A vendor of a remote biometric identification system that ignored the (hypothetically available) harmonized standards. (c) A manufacturer embedding AI in a medical device. *Analysis:* (a) **Internal control** — Annex III non-biometric default. (b) **Notified body** — biometrics without full application of harmonized standards. (c) Assessment under the **medical-device regime**, with AI requirements integrated into that third-party procedure.

**Scenario 2 — The learning loan model.** A provider documents, in its technical file, that its credit model will retrain monthly on new repayment data within defined performance bounds and drift limits. Two years later it also adds an entirely new data source and repurposes the model for insurance pricing. *Analysis:* The pre-declared monthly retraining is **not** a substantial modification (foreseen and assessed). The new data source + purpose change **is** → new conformity assessment, updated DoC, documentation, and registration.

**Scenario 3 — The rebrander's paperwork.** A consultancy white-labels a third party's high-risk HR system under its own brand. *Analysis:* It becomes the provider → it now owns the conformity assessment, DoC, CE marking, registration, post-market monitoring; the original provider must hand over the technical documentation. Buying "CE-marked" software doesn't transfer the paperwork burden when you rebrand.

**Scenario 4 — Standards shortcut.** Two providers build employment-screening systems; one implements the cited harmonized standards for risk management and data governance, the other invents its own approach. *Analysis:* Both may self-assess, but the standards-follower enjoys a **presumption of conformity** for the covered requirements — the other must independently evidence equivalence, and bears more risk in market-surveillance review.

## MEMORY HOOKS

- **Route rule in one line:** *everyone self-assesses, except biometrics without standards — and Annex I products follow their own sectoral third party.*
- **Compliance parade — "Q-T-C-D-C-R":** **Q**MS → **T**ech docs → **C**onformity assessment → **D**oC → **C**E mark → **R**egister. (*"Quality Teams Check Documents, Certify, Register."*)
- **DoC vs CE:** the **DoC is the legal promise** (a document you sign); the **CE mark is the visible badge** (the symbol you affix). One is paper, one is paint.
- **Substantial modification = unforeseen + compliance/purpose-affecting** → new assessment + possible provider switch. *Declare your learning envelope and drift within it freely.*
- **Standards = presumption:** harmonized standard followed → conformity presumed for what it covers; common specifications are the Commission's stand-in.

**The 5 facts to retain:**
1. Most Annex III high-risk systems undergo **internal-control self-assessment**; notified-body assessment is required only for biometrics without fully applied harmonized standards, and Annex I products use their sectoral third-party procedures.
2. Pre-market sequence: QMS → technical documentation → conformity assessment → EU declaration of conformity → CE marking → EU-database registration.
3. Harmonized standards (CEN/CENELEC) confer a **presumption of conformity**; common specifications substitute where standards lag.
4. **Substantial modification** (unforeseen, compliance- or purpose-affecting change) forces reassessment and can transfer provider status; pre-declared changes for learning systems are exempt.
5. The EU database makes high-risk systems (and Art. 6(3) derogation claims, and public-sector deployments) publicly registrable and searchable.

## SELF-CHECK

1. **Q:** Your client sells an Annex III recruitment-screening AI. Which conformity route applies, and who signs what?
   **A:** Internal control (self-assessment). The provider verifies QMS + documentation + requirements itself, then draws up and signs the EU declaration of conformity, affixes CE marking, and registers the system in the EU database.

2. **Q:** When is a notified body mandatory for an Annex III system?
   **A:** Only for biometric systems (Annex III point 1) where the provider has not applied (or only partially applied) harmonized standards/common specifications covering the requirements.

3. **Q:** What legal effect does following a cited harmonized standard have?
   **A:** A presumption of conformity with the AI Act requirements that the standard covers — shifting the evidentiary burden to authorities to show non-compliance.

4. **Q:** Define substantial modification and give an example of a change that is NOT one.
   **A:** A change not foreseen in the initial conformity assessment that affects compliance with the requirements or the intended purpose — triggering reassessment. Not substantial: model updates/retraining pre-determined by the provider and covered in the original technical documentation (the declared learning envelope).

5. **Q:** Name three things an importer should verify before placing a foreign provider's high-risk AI system on the EU market.
   **A:** That the provider performed the conformity assessment (certificates/DoC exist), that technical documentation is drawn up and the system bears CE marking with required information (incl. authorized representative), and that registration obligations are met — refusing to place non-conforming systems and informing authorities of serious risks.
