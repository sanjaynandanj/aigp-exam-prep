# Crosswalk Drill: AI Act ↔ NIST RMF ↔ ISO 42001 — One Mapping Table to Rule Them All

**Phase 4 · Lesson 12 · ~1h · BoK Domain II**

## EXAM FOCUS

The AIGP's deepest skill: given a governance control, name **where each framework requires or supports it**. Scenario stems say things like "the company must demonstrate human oversight — which EU AI Act provision, NIST function, and ISO clause apply?" This lesson is one master table plus drills. It also cements the *category difference*: the AI Act **mandates** (law), NIST RMF **guides by outcome** (functions), ISO 42001 **institutionalizes** (auditable management clauses/controls). Mapping is conceptual, not one-to-one — the exam tests reasonable correspondence, not clause-number trivia for ISO.

## CORE

### The master crosswalk

| Governance theme | EU AI Act (article-level, high-risk regime) | NIST AI RMF function | ISO/IEC 42001 clause/control concept |
|---|---|---|---|
| **Risk assessment & management** | **Art. 9** risk management system (lifecycle, foreseeable misuse, vulnerable groups); Art. 27 FRIA for certain deployers | **MAP** (identify/context) + **MEASURE** (analyze) + **MANAGE** (treat/prioritize) | Clause 6 (planning: AI risk assessment & treatment) + clause 8 (operational performance of assessments); 23894 supplies the method |
| **Impact on people & society** | FRIA (Art. 27); fundamental-rights purpose woven through Arts. 1, 9 | MAP categories on impacts to individuals/groups/society; GOVERN stakeholder engagement | **AI system impact assessment** requirement (clauses 6/8; Annex A impact-assessment theme; ISO 42005 guidance) |
| **Data governance & quality** | **Art. 10** data & data governance (representativeness, bias examination, provenance; special-category allowance for bias correction) | MAP (data provenance in context) + MEASURE (data/bias evaluation) | Annex A "data for AI systems" controls (provenance, quality, preparation); clause 8 operation |
| **Technical documentation / records** | **Art. 11 + Annex IV** technical documentation; **Art. 18** retention (10 yrs); Art. 17 QMS documentation | GOVERN (policies, inventories) + MAP (system documentation) | Clause 7.5 documented information; Annex A lifecycle-documentation controls |
| **Logging & traceability** | **Art. 12** automatic event recording; Art. 19/26 log retention (≥6 months) | MEASURE (track/monitor) + MANAGE (incident forensics) | Annex A lifecycle/operation controls (event logging, traceability records) |
| **Transparency to users/deployers** | **Art. 13** instructions for use & interpretability; **Art. 50** transparency tier (AI-interaction disclosure, synthetic-content marking, deepfake labels); Art. 86-style explanation right for affected persons | GOVERN (transparency policies) + MAP (communication of limits); "Accountable & Transparent" characteristic | Annex A "information for interested parties" controls (system info, reporting, user communication) |
| **Human oversight** | **Art. 14** design for effective oversight (override, stop, automation-bias awareness; two-person RBI check); **Art. 26** deployer competence/training assignment | GOVERN (roles, human-AI configuration policies) + MANAGE (oversight in response plans); "human-AI teaming" threads in MAP | Annex A use-of-AI / lifecycle controls on human oversight; clause 5 roles & responsibilities; clause 7 competence |
| **Accuracy, robustness, cybersecurity** | **Art. 15** (declared metrics, resilience, poisoning/adversarial defenses) | MEASURE (TEVV: accuracy, robustness, security testing, red-teaming); "Valid & Reliable / Secure & Resilient" characteristics | Annex A lifecycle verification & validation controls; integration with ISO 27001 for security |
| **Quality/governance system** | **Art. 17** quality management system (providers) | **GOVERN** in its entirety (policies, accountability, culture) | The whole AIMS — clauses 4–10; certification is the assurance artifact |
| **Post-market monitoring** | **Art. 72** post-market monitoring system & plan | MANAGE (post-deployment monitoring) + MEASURE (ongoing tracking) | Clause 9 performance evaluation; Annex A operation/monitoring controls; clause 10 improvement |
| **Incident management** | **Art. 73** serious-incident reporting (15-day baseline, faster if severe); Art. 26 deployer duty to inform/suspend | MANAGE (incident response, recovery, communication) | Annex A incident/response-related operational controls; clause 10 nonconformity & corrective action |
| **Third-party / supply chain** | Art. 25 value-chain responsibilities; importer/distributor duties (Arts. 23–24); GPAI downstream info (Art. 53) | GOVERN third-party policies + MAP third-party risks + MANAGE third-party treatment | Annex A third-party/customer-relationship controls; clause 8 change/procurement control |
| **Competence & literacy** | **Art. 4** AI literacy (providers & deployers — live since Feb 2025); Art. 26 oversight competence | GOVERN (workforce diversity, training, culture) | Clause 7.2/7.3 competence & awareness |
| **Registration / external accountability** | Arts. 49/71 EU-database registration; CE marking + DoC (Arts. 47–48) | GOVERN (inventories, external accountability mechanisms) | Certification + Statement of Applicability as public-facing assurance (no legal analog) |

*(EU AI Act article numbers above are the commonly cited ones for the high-risk chapter and related duties; ISO mappings are conceptual clause/control themes, not official citations.)*

### The category-difference cheat sheet

| | EU AI Act | NIST AI RMF | ISO/IEC 42001 |
|---|---|---|---|
| Nature | Binding regulation | Voluntary outcome framework | Voluntary but **certifiable** requirements |
| Unit of analysis | AI **system** (+ GPAI model) by risk class | AI risk practice via 4 **functions** | The **organization's** management system |
| Verification | Conformity assessment, market surveillance, fines | Self-applied profiles | Third-party audit/certificate |
| Verb | *comply* | *align* | *certify* |
| Use in one program | Sets the floor for EU-touching systems | Structures the program & vocabulary | Institutionalizes and proves it |

### Drill method — "control → three addresses"

For any control, answer three questions:
1. **Where does law require it?** (AI Act article — or "not mandated; voluntary")
2. **Which RMF function houses it?** (GOVERN/MAP/MEASURE/MANAGE)
3. **Which 42001 element institutionalizes it?** (clause 4–10 or Annex A theme)

Run these ten until instant: risk assessment · bias testing of datasets · model logging · instructions for use · human override design · red-team/robustness testing · post-market monitoring plan · serious-incident reporting · vendor due diligence · staff AI training.

## CASES & EXAMPLES

**Drill 1 — "We need documented human oversight."** *Answer:* AI Act — Art. 14 (provider design duty) + Art. 26 (deployer assigns competent overseers); NIST — GOVERN (roles/accountability) with MANAGE operationalizing intervention; ISO 42001 — clause 5 roles + clause 7 competence + Annex A oversight controls. Bonus link: GDPR Art. 22 meaningful-human-involvement doctrine.

**Drill 2 — "Prove your training data was checked for bias."** *Answer:* AI Act — Art. 10 data-governance (bias examination/mitigation; special-category allowance for correction); NIST — MEASURE (bias evaluation/TEVV) informed by MAP context; ISO — Annex A data-for-AI controls executed under clause 8, verified by clause 9 internal audit. US bridge: four-fifths analysis (Title VII), NYC LL 144 audit.

**Drill 3 — "An incident occurred in production."** *Answer:* AI Act — Art. 73 serious-incident report to the MSA (15-day baseline; deployer informs provider, suspends on serious risk under Art. 26/29-era duties); NIST — MANAGE incident response/recovery/communication; ISO — clause 10 nonconformity + corrective action with Annex A response controls; feed lessons into Art. 9 risk iteration / clause 10 improvement / MANAGE re-prioritization.

**Drill 4 — spot-the-gap.** A company is ISO 42001-certified and RMF-aligned but sells an uncertified high-risk system in the EU with no CE marking or registration. *Answer:* Certification/alignment ≠ legal conformity: the AI Act still demands conformity assessment, DoC, CE marking, EU-database registration (Arts. 43, 47–49) — items with **no voluntary-framework substitute**. Conversely, frameworks add value law doesn't require (culture, profiles, continual-improvement audit).

## MEMORY HOOKS

- **Address format:** every control has three addresses — *Article (law) / Function (NIST) / Clause-control (ISO).* If you can't give all three, you don't own the control yet.
- **Article anchors worth memorizing:** *9 risk · 10 data · 11 docs · 12 logs · 13 tell · 14 human · 15 strong* — then *17 QMS, 26 deployers, 27 FRIA, 43 conformity, 49 register, 50 transparency, 72 monitor, 73 report.* (Rhyme: "9 through 15, the compliance spine.")
- **Function sorting reflex:** org/culture → GOVERN; context/impacts → MAP; tests/metrics → MEASURE; decisions/incidents → MANAGE.
- **ISO reflex:** *plan it (6), do it (8), check it (9), fix it (10) — document everything (7.5), pick controls from Annex A.*
- **Category one-liner:** *the Act punishes, the RMF orients, the ISO certifies.*

**The 5 facts to retain:**
1. The high-risk compliance spine — Arts. 9–15 (risk, data, docs, logs, transparency, oversight, robustness) — maps cleanly onto RMF functions and 42001 clauses/Annex A themes.
2. GOVERN ≈ Art. 17 QMS ≈ 42001 clauses 4–7/10: the organizational shell around every technical control.
3. Post-market monitoring (Art. 72) and incident reporting (Art. 73) live in MANAGE and in ISO clauses 9–10 — the "after deployment" column exam scenarios favor.
4. Voluntary frameworks can **evidence** legal duties (and earn Colorado's presumption) but never replace AI Act conformity artifacts: assessment, DoC, CE marking, registration.
5. Mappings are conceptual and published as crosswalks (NIST↔42001↔AI Act↔OECD) — expect "best-fit" answers, not exact equivalence.

## SELF-CHECK

1. **Q:** Give the three addresses for "continuous risk management across the AI lifecycle."
   **A:** EU AI Act Art. 9 (risk management system); NIST RMF — MAP/MEASURE/MANAGE cycle (governed by GOVERN); ISO 42001 clause 6 planning + clause 8 operation, with ISO 23894 as method guidance.

2. **Q:** A regulator asks for automatically generated event records from your high-risk system. Which article, function, and ISO mechanism are implicated?
   **A:** Art. 12 record-keeping/logging (with retention under Arts. 18–19/26); NIST MEASURE (tracking/monitoring) supporting MANAGE forensics; ISO 42001 Annex A traceability/logging controls plus clause 7.5 documented information.

3. **Q:** Which obligations have *no* voluntary-framework equivalent, making "we're ISO-certified" an insufficient answer in the EU?
   **A:** The AI Act's market-entry artifacts: conformity assessment, EU declaration of conformity, CE marking, EU-database registration (and FRIA/serious-incident reporting duties as legal acts) — voluntary alignment can evidence but not substitute.

4. **Q:** Sort into RMF functions: (a) adopting a third-party AI procurement policy; (b) running adversarial robustness tests; (c) defining the deployment context and affected groups; (d) choosing to restrict a model to internal use after risk review.
   **A:** (a) GOVERN; (b) MEASURE; (c) MAP; (d) MANAGE.

5. **Q:** Why does the Colorado AI Act make this crosswalk commercially valuable, not just pedagogically neat?
   **A:** Colorado grants deployers/developers a rebuttable presumption of reasonable care when their risk program conforms to recognized frameworks like the NIST AI RMF or ISO 42001 — so one crosswalked program simultaneously satisfies EU legal duties, earns US liability protection, and produces certifiable assurance.
