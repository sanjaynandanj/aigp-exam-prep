# Cross-Border: Extraterritoriality, Data Transfers, Conflicts of Law

**Phase 3 · Lesson 10 · ~1h · BoK Domain II**

## EXAM FOCUS

Global AI programs face three cross-border questions the exam recycles constantly: (1) **whose law reaches me?** (extraterritoriality of GDPR and the EU AI Act); (2) **how do I move data legally?** (transfer mechanisms, summary level); (3) **how do the world's regulatory philosophies collide?** (EU rights-based vs US sectoral vs China state-led — and the "Brussels effect" that pushes EU rules worldwide). Expect a scenario with a non-EU company and a question about which regime applies and why.

## CORE

### 1. Extraterritoriality

**GDPR (Art. 3):** applies to
- **(3(1))** processing in the context of an EU **establishment** (regardless of where processing happens);
- **(3(2))** non-EU controllers/processors that **(a) offer goods/services** to people in the EU (even free) or **(b) monitor their behaviour** in the EU — the hooks that caught US facial-recognition scrapers and chatbot providers. Non-EU entities in scope must appoint an **EU representative** (Art. 27).

**EU AI Act:** applies to
- **providers** placing AI systems/GPAI models on the EU market or putting them into service in the EU, **wherever the provider is established**;
- **deployers** located in the EU;
- providers **and** deployers in third countries **where the output produced by the system is used in the EU** — the famously long arm (e.g., a US company running analysis abroad whose results are used on EU customers);
- importers/distributors; non-EU providers of high-risk systems must appoint an **authorized representative** in the EU.
- Exclusions still apply (military, third-country public authorities under international cooperation, personal non-professional use).

**Comparison anchor:** GDPR reaches you through *people in the EU*; the AI Act reaches you through *the EU market and EU-used outputs*.

**Others:** US state laws use resident/business-nexus thresholds; China's PIPL has GDPR-like extraterritorial reach; the Colorado AI Act binds those doing business in Colorado.

### 2. Data transfer mechanisms (summary level — CIPP/E depth not required)

GDPR Chapter V: personal data may leave the EEA only via:

| Mechanism | Essence | AI relevance |
|---|---|---|
| **Adequacy decision** (Art. 45) | Commission finds the destination essentially equivalent (e.g., UK, Japan, Korea; **EU–US Data Privacy Framework** for certified US companies) | Simplest route for US cloud/AI vendors — but *Schrems* history shows adequacy can be struck down; DPF remains under challenge — verify status |
| **Appropriate safeguards** (Art. 46) | **SCCs** (standard contractual clauses) + transfer impact assessment; **BCRs** for intra-group | The default for AI vendor contracts; TIA must consider destination surveillance law |
| **Derogations** (Art. 49) | Consent, contract necessity, vital interests — narrow, occasional | Not a basis for systematic training-data flows |

AI-specific transfer wrinkles: training pipelines often centralize global data in one region (mass transfers); model weights trained on EU personal data may themselves embed personal data (unsettled whether transferring a model = transferring personal data — flagged by regulators, verify status); support access from third countries counts as a transfer.

**Non-EU transfer regimes to recognize:** China requires security assessments/CAC mechanisms for outbound data (and localizes "important data"); Russia localizes; India's DPDP Act uses a blacklist approach; the US restricts **bulk sensitive data flows to countries of concern** (DOJ rule under EO 14117) — data can be geopolitically restricted in *both* directions.

### 3. Three regulatory philosophies in conflict

| Dimension | **EU — rights-based** | **US — sectoral/market-led** | **China — state-led** |
|---|---|---|---|
| Anchor value | Fundamental rights, dignity, precaution | Innovation, market correction via enforcement/litigation | State security, social stability, tech leadership |
| Instrument style | Horizontal omnibus laws (GDPR, AI Act) | Sector statutes + FTC/EEOC/CFPB enforcement + state patchwork | Vertical rules per technology (recommendation algorithms, deep synthesis, generative AI) + filing/registration with CAC |
| Pre-market control | Conformity assessment, CE marking for high-risk | Essentially none outside FDA-like sectors | Security assessments, algorithm filing, content review before public LLM release |
| Individual rights | Extensive, enforceable | Fragmented (state privacy laws) | Present on paper vs. state access broad |
| Content rules | Transparency/labeling | First Amendment limits content mandates | Alignment with "core socialist values," mandatory labeling |
| Signature risk for firms | Fines % of global turnover; market exclusion | Class actions; FTC consent decrees; disgorgement | Service suspension, license loss |

**Conflicts in practice:** a single hiring tool may need EU AI Act conformity + GDPR basis, US bias audits without collecting EU-style special-category data (which some US regimes *require* estimating and EU law restricts collecting), and Chinese algorithm filing if deployed there. Compliance-by-jurisdiction vs. one-global-standard is a board-level architecture choice.

### 4. The Brussels effect

**Definition (Anu Bradford):** the EU's market size + regulatory capacity cause its rules to become **de facto global standards** — companies standardize on the strictest regime (unilateral, market-driven spread), and other legislatures copy EU templates (de jure spread).

- Evidence pro: GDPR's global privacy-law wave; AI Act concepts (risk tiers, provider/deployer, FRIA) surfacing in Brazil's bill, Colorado's act, Korea's framework act.
- Limits/counter-currents: US federal resistance and innovation framing; the compute frontier sits outside the EU; EU "omnibus/simplification" pressure on its own digital rules (status as of mid-2026 — verify) suggests recalibration; China's model exports through its own channels. Exam expects you to *define* the effect and give one example and one limit.

### Interoperability tools

Cross-jurisdiction convergence instruments (bridge to Phase 4): OECD AI Principles (shared vocabulary, incl. the OECD AI definition adopted by both the EU AI Act and US frameworks), Council of Europe Framework Convention (binding treaty open beyond Europe), NIST RMF↔ISO 42001 crosswalks, G7 Hiroshima code of conduct — these are how multinationals build **one program, many laws**.

## CASES & EXAMPLES

**Scenario 1 — The output long-arm.** A Singapore analytics firm scores loan applicants for a Frankfurt bank; all processing happens in Singapore, results emailed to Germany. *Analysis:* EU AI Act applies — third-country provider/deployer whose **output is used in the EU**; the system is Annex III high-risk (creditworthiness); an EU authorized representative and conformity obligations follow. GDPR also applies to the personal data (processor obligations + Chapter V transfers for sending applicant data to Singapore).

**Scenario 2 — The monitoring hook.** A US ad-tech firm with no EU office builds behavioral profiles from EU users' browsing to train targeting models. *Analysis:* GDPR Art. 3(2)(b) — monitoring behavior in the EU; full GDPR compliance + Art. 27 representative required. "We have no EU presence" is the distractor.

**Scenario 3 — Transfer stack for an AI vendor.** An EU hospital wants a US vendor to fine-tune a model on patient data in US data centers. *Analysis:* Needs (i) GDPR processor terms, (ii) a Chapter V mechanism — DPF certification or SCCs plus transfer impact assessment, (iii) special-category safeguards (Art. 9), and realistically EU-region processing or de-identification given sensitivity; Art. 49 derogations are the wrong answer for systematic flows.

**Scenario 4 — One product, three philosophies.** A global platform launches an AI companion chatbot in the EU, US, and China. *Analysis:* EU — AI Act transparency (disclose AI nature), GDPR basis, possible manipulation analysis; US — FTC Section 5 (deception/unfair design, children's protection), state bot-disclosure laws; China — generative-AI measures: security assessment, filing, content moderation, output labeling. Same product, three distinct pre-launch checklists — the exam wants you to spot that *no single compliance file transfers wholesale*.

## MEMORY HOOKS

- **Two long arms:** GDPR = *people* in the EU (goods/services or monitoring); AI Act = *market + outputs used* in the EU.
- **Transfer ladder:** **A**dequacy → **S**afeguards (SCCs/BCRs) → **D**erogations ("ASD — in descending order of comfort").
- **Philosophy triangle:** EU protects the **person**, US polices the **market**, China secures the **state**.
- **Brussels effect = strictest-regime gravity:** comply once at EU level, sell everywhere — plus copycat legislation.
- **Representative rhyme:** no EU seat → appoint a rep (GDPR Art. 27 / AI Act authorized representative).

**The 5 facts to retain:**
1. GDPR Art. 3(2) captures non-EU entities offering services to or monitoring people in the EU; the AI Act captures non-EU providers/deployers when the system is on the EU market **or its output is used in the EU**.
2. Transfers out of the EEA need adequacy, appropriate safeguards (SCCs/BCRs + TIA), or narrow derogations — the EU–US DPF is the current US bridge but remains challenge-prone (verify status).
3. Model training centralization, third-country support access, and possibly model weights themselves are transfer events to assess.
4. EU rights-based, US sectoral/enforcement-led, China state-led — three philosophies producing conflicting pre-market, content, and data rules.
5. The Brussels effect spreads EU standards de facto (corporate standardization) and de jure (legislative copying) — with real limits.

## SELF-CHECK

1. **Q:** A Canadian company sells an emotion-analytics API; a Spanish call center uses its outputs on EU customers. Does the EU AI Act reach the Canadian provider?
   **A:** Yes — third-country providers are covered where the system's output is used in the EU; high-risk/prohibition analysis (emotion recognition in workplaces is prohibited) and an EU authorized representative follow.

2. **Q:** Which GDPR provision catches a non-EU scraper building face templates of EU residents, and what governance duty follows besides compliance itself?
   **A:** Art. 3(2)(b) monitoring of behavior in the EU (with Art. 9 biometric issues); it must also designate an EU representative under Art. 27.

3. **Q:** Rank the three GDPR transfer families and state why derogations can't support routine training-data exports.
   **A:** Adequacy decisions, appropriate safeguards (SCCs, BCRs, with transfer impact assessments), derogations. Art. 49 derogations are for occasional, non-repetitive situations — systematic training pipelines are neither.

4. **Q:** Contrast pre-market control of AI in the EU, US, and China in one line each.
   **A:** EU — conformity assessment/CE marking for high-risk before market entry; US — generally none (post-hoc enforcement, sector exceptions like FDA); China — security assessment and algorithm filing with the CAC before public release.

5. **Q:** Define the Brussels effect and give one mechanism by which it operates.
   **A:** The EU's market power turning its regulations into global standards — e.g., multinationals adopting EU-compliant practice worldwide because a single strictest-standard build is cheaper (de facto), or foreign legislatures modeling laws on GDPR/AI Act templates (de jure).
