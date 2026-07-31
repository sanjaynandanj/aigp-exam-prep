# GDPR × AI: Lawful Basis, Purpose Limitation, Minimization vs Training Data

**Phase 3 · Lesson 01 · ~1.5h · BoK Domain II**

## EXAM FOCUS

Domain II tests whether you can apply *existing* data protection law to AI systems — the GDPR did not need an "AI amendment" to reach AI. Expect scenario questions where a company trains or deploys a model on personal data and you must pick the correct lawful basis, spot a purpose-limitation violation, or identify which GDPR principle is in tension with a described practice. The most-tested tensions: **minimization vs. training-data appetite**, **purpose limitation vs. re-use**, and **accuracy applied to model outputs**.

## CORE

### When does GDPR apply to AI at all?

GDPR applies whenever **personal data** (any information relating to an identified or identifiable natural person) is processed — during **training**, **fine-tuning**, **testing**, or **inference/output**. Fully anonymized data falls outside GDPR, but the bar for anonymization is high: if re-identification is reasonably likely (including via the model memorizing training examples), the data is only *pseudonymized* and GDPR still applies.

### The six lawful bases (Art. 6) applied to AI

| Lawful basis | AI training use | AI deployment use | Exam traps |
|---|---|---|---|
| **Consent** | Rare for large-scale scraping (must be specific, informed, freely given, withdrawable) | Common for optional features (e.g., voice assistant personalization) | Consent bundled into ToS is not "freely given"; withdrawal must be as easy as giving it |
| **Contract** | Almost never valid for training — training is rarely "necessary" to perform the contract | Valid only when the AI function is genuinely necessary to deliver the service | "Necessary" is strict; convenience or business benefit ≠ necessity |
| **Legal obligation** | Rare | E.g., AML screening required by law | Must be an actual legal requirement, not a business preference |
| **Vital interests** | Essentially never | Emergency medical scenarios only | Distractor answer in most scenarios |
| **Public task** | Public bodies with a legal mandate | Government AI services | Not available to private companies acting commercially |
| **Legitimate interests** | The workhorse basis claimed for model training (incl. web-scraped data) — requires the three-part balancing test | Fraud detection, security analytics | Fails if data subjects' rights override; requires documented LIA |

### The legitimate interests balancing test (three parts)

1. **Purpose test** — is the interest lawful, real, and clearly articulated?
2. **Necessity test** — is the processing necessary, or could a less intrusive method achieve it?
3. **Balancing test** — do the interests override the data subject's rights and freedoms, considering *reasonable expectations*, the nature of the data, and mitigations (pseudonymization, opt-outs, transparency)?

EU regulators (via EDPB opinions on AI models) have accepted that legitimate interests *can* support model training, but only with genuine mitigations and case-by-case assessment — it is not a rubber stamp.

### GDPR principles under stress from AI

| Principle (Art. 5) | What it requires | The AI tension |
|---|---|---|
| **Lawfulness, fairness, transparency** | Valid basis; no deception; clear info | Scraped subjects never saw a notice; black-box logic is hard to explain |
| **Purpose limitation** | Collect for specified, explicit, legitimate purposes; no incompatible further use | Data collected for service delivery re-used to train models — requires a **compatibility assessment** (link between purposes, context, data nature, consequences, safeguards) |
| **Data minimization** | Adequate, relevant, limited to what is necessary | Directly opposes "more data = better model"; mitigate via curation, sampling, synthetic data, pseudonymization |
| **Accuracy** | Personal data must be accurate and kept up to date | Applies to training data *and arguably to outputs about people* (e.g., LLM "hallucinating" false facts about a named person has triggered complaints) |
| **Storage limitation** | Keep no longer than necessary | Training corpora retained indefinitely; models that memorize data complicate deletion |
| **Integrity & confidentiality** | Appropriate security | Model inversion / membership inference attacks can leak training data |
| **Accountability** | Demonstrate compliance | Requires documentation: LIAs, DPIAs, records of processing |

### Special-category data (Art. 9) in models

Processing data revealing race/ethnicity, political opinions, religion, trade-union membership, genetic data, biometric data *for identification*, health, sex life/orientation is **prohibited unless an Art. 9(2) exception applies** (explicit consent, substantial public interest under law, etc. — note: legitimate interests is **not** an Art. 9 exception). Two AI-specific points:

- Large scraped datasets almost inevitably contain special-category data, and regulators have said inadvertent inclusion does not excuse the prohibition.
- Models can **infer** special-category data (e.g., inferring health status from purchase patterns). The CJEU has read Art. 9 broadly: data that indirectly *reveals* a special category can itself be special-category data.

### Data subject rights against models

| Right | AI application |
|---|---|
| Access (Art. 15) | What personal data is in training sets / profiles about me |
| Rectification (Art. 16) | Correcting false outputs about a person — technically hard for LLMs; regulator complaints filed on exactly this |
| Erasure (Art. 17) | "Machine unlearning" problem; may require filtering, retraining, or output suppression |
| Objection (Art. 21) | Must be offered when relying on legitimate interests — several large model providers added opt-outs under regulator pressure |
| Portability (Art. 20) | Applies to provided data under consent/contract bases |

## CASES & EXAMPLES

**Scenario 1 — Repurposing CRM data.** A retailer collected customer emails and purchase histories "to fulfil orders." It now wants to train a churn-prediction model on that data. *Exam answer pattern:* This is **further processing** — run the Art. 6(4) compatibility assessment; if compatible (analytics closely linked to the service, safeguards applied), it may proceed on the original basis; if not, a new lawful basis and fresh transparency are needed. Simply "we already have the data" is always the wrong answer.

**Scenario 2 — Web-scraped training corpus.** A startup scrapes public social-media posts to train a foundation model, arguing "the data is public." *Exam answer pattern:* Publicly accessible ≠ free to process. GDPR still applies; the realistic basis is legitimate interests with a documented LIA, transparency measures, opt-out mechanisms, and filtering of special-category data. Regulators (e.g., the Italian Garante's 2023 action against a major chatbot provider) have suspended services over exactly these gaps.

**Scenario 3 — Health inference.** An insurer's model infers likely diabetes from grocery-loyalty data to adjust marketing. *Exam answer pattern:* The inference itself is special-category (health) data → Art. 9 prohibition applies; legitimate interests cannot cure it; explicit consent or another Art. 9(2) condition is required, plus fairness concerns.

**Scenario 4 — Minimization pushback.** A data scientist insists on ingesting the full customer database "because more data improves accuracy." *Exam answer pattern:* Minimization requires necessity analysis — use only fields with demonstrated predictive relevance, pseudonymize, consider synthetic or aggregated data. "Model performance" alone never overrides Art. 5(1)(c).

## MEMORY HOOKS

- **Lawful bases mnemonic:** "**C**an **C**ompanies **L**egally **V**alidate **P**rocessing **L**awfully" — Consent, Contract, Legal obligation, Vital interests, Public task, Legitimate interests.
- **The training-basis ladder:** for commercial model training, the realistic candidates are *consent* (rarely practical at scale) or *legitimate interests* (needs the 3-part LIA). Contract is almost always a distractor.
- **Art. 6 vs Art. 9:** Art. 6 = you need *a* basis for any personal data; Art. 9 = you need an *additional* exception for special categories — and **legitimate interests is not one of them**.
- **Public ≠ free:** publicly available data is still personal data.

**The 5 facts to retain:**
1. GDPR applies to AI at every lifecycle stage where personal data is processed — no AI-specific trigger needed.
2. Legitimate interests is the primary claimed basis for large-scale training and always requires the documented three-part balancing test.
3. Re-using data to train models is "further processing" requiring a compatibility assessment or a new basis.
4. Special-category data (including *inferred* attributes) needs an Art. 9(2) exception; legitimate interests never suffices.
5. The accuracy principle can reach model *outputs* about identifiable people, not just inputs.

## SELF-CHECK

1. **Q:** A SaaS provider claims "performance of a contract" as its basis for training its product-improvement model on customer data. Why is this weak?
   **A:** Training is rarely *necessary* to perform the contract with that user — the service can be delivered without it. Necessity is interpreted strictly; the realistic basis is legitimate interests (with an LIA) or consent.

2. **Q:** Name the three parts of the legitimate interests assessment.
   **A:** Purpose test (legitimate interest), necessity test (least intrusive means), balancing test (subjects' rights and reasonable expectations vs. the interest, considering safeguards).

3. **Q:** Under what conditions can data collected for one purpose be re-used for AI training without a new lawful basis?
   **A:** When the new purpose is *compatible* with the original under the Art. 6(4) factors: link between purposes, collection context/expectations, data nature, consequences for subjects, and safeguards (e.g., pseudonymization).

4. **Q:** An LLM outputs a false criminal allegation about a named individual. Which GDPR principle and right are most directly engaged?
   **A:** The accuracy principle (Art. 5(1)(d)) and the right to rectification (Art. 16) — plus fairness; complaints on this exact fact pattern have been filed with EU regulators.

5. **Q:** Why doesn't "the data was publicly posted online" resolve GDPR concerns for a scraped training set?
   **A:** GDPR applies to personal data regardless of public availability; scraping still requires a lawful basis, transparency, minimization, and handling of any special-category data present.
