# EU AI Act: Structure, Scope, Actors (Provider, Deployer, Importer, Distributor)

**Phase 4 · Lesson 01 · ~1.5h · BoK Domain II**

## EXAM FOCUS

The EU AI Act (Regulation (EU) 2024/1689) is the single most-tested subject on the AIGP. This lesson gives you the chassis everything else bolts onto: what kind of law it is, who it binds, how far it reaches, what it excludes, and how it stacks with GDPR. Actor identification — *"in this scenario, who is the provider?"* — is one of the most common question types, especially the traps where a **deployer becomes a provider**.

## CORE

### What kind of law

| Attribute | Value | Why it matters |
|---|---|---|
| Instrument | **Regulation** (not a directive) | Directly applicable in all member states, no national transposition, uniform text — contrast with the PLD (a directive) |
| Legal family | **Product-safety / New Legislative Framework** law | Explains CE marking, conformity assessment, market surveillance, harmonized standards — AI treated like machinery or medical devices, with fundamental-rights goals layered on |
| Approach | **Risk-based pyramid** | Prohibited → high-risk → limited-risk (transparency) → minimal risk; plus a parallel regime for GPAI models |
| Adopted / in force | 2024; entry into force **1 Aug 2024**, staggered application (Lesson 07) | |
| Definition of AI system | Machine-based system, designed to operate with varying autonomy, possibly adaptive, that **infers from inputs how to generate outputs** (predictions, content, recommendations, decisions) influencing environments — aligned with the **OECD definition** | "Infers" excludes purely rule-following traditional software |

### Scope and extraterritorial reach

Covered (Art. 2 concept):
- **Providers** placing AI systems or GPAI models **on the EU market** or into service in the EU — *wherever established*;
- **Deployers** established/located in the EU;
- Providers **and deployers in third countries where the output** produced by the AI system **is used in the EU**;
- Importers and distributors; product manufacturers integrating AI under their own name; authorized representatives; affected persons in the EU (rights like the explanation right for high-risk decisions).

### Exclusions — know all of them

| Exclusion | Notes |
|---|---|
| **Military, defence, national security** exclusive purposes | Placed under member-state/national-security competence |
| Third-country **public authorities / international organizations** under law-enforcement/judicial cooperation agreements | With safeguards |
| **Scientific research and development** as sole purpose | Pre-market R&D and testing (not real-world testing) also carved out until placed on market/into service |
| **Purely personal, non-professional** use by natural persons | The "hobbyist" carve-out |
| **Free and open-source** AI | Exempt *unless* prohibited practice, high-risk, or triggering transparency obligations; GPAI open-source carve-out is partial (Lesson 05) |

### The actors — the exam's favorite vocabulary

| Actor | Definition (essence) | One-line duty summary |
|---|---|---|
| **Provider** | Develops (or has developed) an AI system/GPAI model and **places it on the market or puts it into service under its own name or trademark**, whether for payment or free | Bears the heavy compliance load: conformity, documentation, registration, CE marking |
| **Deployer** | Uses an AI system **under its authority** in a professional context (not personal use) | Use per instructions, human oversight, monitoring, input-data relevance, some FRIAs and notices |
| **Importer** | EU-established entity placing on the EU market a system bearing the name/trademark of a **non-EU** entity | Verify conformity assessment done, documentation present, CE marking; hold certificates |
| **Distributor** | Supply-chain actor (other than provider/importer) making a system available on the EU market | Verify CE marking + documentation; don't supply non-conforming systems; storage/transport care |
| **Authorized representative** | EU-established person mandated in writing by a non-EU provider | Compliance liaison: keep documentation, cooperate with authorities |
| **Operator** | Umbrella term: any of the above | |
| **Product manufacturer** | Integrates a high-risk AI system into its product under its own name | Takes on provider obligations |

**The role-switch trap (Art. 25 concept):** a **deployer, distributor, or importer becomes a provider** of a high-risk system if it (a) puts its **name/trademark** on it, (b) makes a **substantial modification** to a high-risk system, or (c) **modifies the intended purpose** of a non-high-risk system such that it becomes high-risk. The original provider then must hand over documentation to enable compliance. Fine-tuning a GPAI model can analogously create provider duties for the modifier (scoped to the modification, per Commission guidance).

### Relationship to GDPR

| Question | Answer |
|---|---|
| Does the AI Act replace GDPR? | **No — cumulative.** AI Act is product law for systems; GDPR is rights law for personal data. Both can apply to the same system simultaneously |
| Overlaps to know | AI Act transparency vs GDPR notices; FRIA can build on a DPIA; AI Act logging vs GDPR storage limitation (tension); Art. 22 GDPR governs the *decision*, AI Act governs the *system* |
| Special hook | AI Act permits special-category data processing **strictly for bias detection/correction** in high-risk systems, with safeguards, where strictly necessary — a narrow bridge over the GDPR Art. 9 wall |
| Regulators | DPAs enforce GDPR; market-surveillance authorities + AI Office enforce the AI Act (DPAs may be designated for some categories); EDPS supervises EU institutions for both |

### The risk pyramid (orientation for the next lessons)

1. **Unacceptable risk** → banned (Art. 5 — Lesson 02)
2. **High risk** → conformity regime (Lessons 03–04, 06)
3. **Transparency risk** → disclosure duties (chatbots must reveal AI nature; deepfakes and AI-generated content labeled; emotion-recognition/biometric-categorization subjects informed)
4. **Minimal risk** → no new obligations (most AI: spam filters, games) — voluntary codes encouraged
5. **GPAI models** → parallel horizontal regime with a systemic-risk tier (Lesson 05)

## CASES & EXAMPLES

**Scenario 1 — Who's the provider?** A Dutch bank licenses a US vendor's credit-scoring engine, rebrands it "BankScore," and offers it to sister banks. *Analysis:* By affixing its own trademark to a high-risk system, the bank **becomes the provider** with full provider obligations; the US vendor must supply the technical documentation. Had the bank merely *used* the vendor's system under the vendor's name, it would be a deployer.

**Scenario 2 — The repurposer.** A firm buys a general document-classification system (not high-risk) and configures it to screen job applications. *Analysis:* Modifying the intended purpose so the system becomes high-risk (employment, Annex III) converts the modifier into a **provider**. Intended purpose is defined by the original provider's documentation — stray from it and you inherit the duties.

**Scenario 3 — Outside the Act?** (a) A defense ministry procures targeting AI. (b) A university lab develops a novel model purely for research. (c) A hobbyist runs an open-source image generator at home. *Analysis:* All three are excluded — military purpose, scientific R&D, personal non-professional use. But the moment the lab **commercializes** or the hobbyist offers a paid service, the Act attaches.

**Scenario 4 — GDPR + AI Act stack.** An EU insurer deploys an Annex III risk-assessment system processing health data. *Analysis:* Both regimes: AI Act deployer duties (oversight, monitoring, possibly FRIA) + GDPR (Art. 9 condition, DPIA, transparency). Passing an AI Act conformity assessment does not answer a single GDPR question, and vice versa.

## MEMORY HOOKS

- **Actor chain mnemonic — "P-D-I-D-A":** **P**rovider builds & brands, **D**eployer uses, **I**mporter brings in, **D**istributor passes on, **A**uthorized rep answers for absentees.
- **Provider test in 5 words:** *develops + markets under own name.*
- **Deployer→provider triggers — "Name, Change, Purpose":** rebrand it, substantially modify it, or repurpose it into high-risk — and it's yours.
- **Exclusions mnemonic — "M-R-P-O":** **M**ilitary, **R**esearch, **P**ersonal use, **O**pen source (partial).
- **Regulation vs directive:** *regulations apply themselves; directives need national laws* — AI Act is the former, PLD the latter.

**The 5 facts to retain:**
1. The AI Act is a directly applicable EU **regulation** built on product-safety (NLF) architecture with a **risk-based pyramid**.
2. It reaches non-EU providers and deployers whenever the system is on the EU market **or its output is used in the EU**.
3. Provider = develops and places on market under own name; deployer = professional user under whose authority the system runs.
4. Deployers/importers/distributors **become providers** by rebranding, substantially modifying, or repurposing a system into high-risk.
5. Exclusions: military/national security, R&D, personal non-professional use, partial open-source — and the Act applies **cumulatively with GDPR**, never instead of it.

## SELF-CHECK

1. **Q:** Why does it matter that the AI Act is a regulation rather than a directive?
   **A:** It applies directly and uniformly across all member states without national transposition — one text, one compliance baseline (unlike the revised PLD, which member states must transpose).

2. **Q:** A Brazilian HR-tech company sells resume-screening software to a Portuguese employer, hosting everything in Brazil. Which AI Act roles exist, and is the Brazilian firm covered?
   **A:** Yes — it is a provider placing a high-risk (employment) system on the EU market (and outputs are used in the EU); it needs an EU authorized representative. The Portuguese employer is the deployer.

3. **Q:** List the three ways a deployer of a high-risk system becomes its provider.
   **A:** Putting its own name/trademark on the system; substantially modifying a high-risk system; modifying the intended purpose of a non-high-risk system so it becomes high-risk.

4. **Q:** Name four categories of activity excluded from the AI Act's scope.
   **A:** Exclusively military/defence/national-security purposes; sole-purpose scientific research and development; purely personal non-professional use; free and open-source AI (unless prohibited, high-risk, or transparency-triggering) — plus third-country authorities under international cooperation agreements.

5. **Q:** An AI system passes its AI Act conformity assessment. Its deployer processes personal data with it. What remains to be done under GDPR?
   **A:** Everything GDPR requires: lawful basis (plus Art. 9 conditions if relevant), transparency, DPIA where triggered, data-subject rights, Art. 22 analysis for automated decisions — the two laws apply cumulatively.
