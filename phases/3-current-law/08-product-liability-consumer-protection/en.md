# Product Liability & Consumer Protection Meets AI

**Phase 3 · Lesson 08 · ~1h · BoK Domain II**

## EXAM FOCUS

Two threads: (1) **civil liability theories** when AI causes harm — negligence vs strict product liability, and the EU's modernization via the **revised Product Liability Directive (PLD)** that now expressly covers software and AI; (2) **consumer protection** — dark patterns and UDAP theories applied to AI interfaces and claims. The exam tests which theory fits a fact pattern, what the new PLD changed (software = product; burden-easing disclosure/presumptions), and recognizing manipulative design.

## CORE

### US civil-liability theories applied to AI

| Theory | Elements | AI application | Friction points |
|---|---|---|---|
| **Negligence** | Duty, breach (unreasonable conduct), causation, damages | Careless model development/testing, deploying with known failure modes, no monitoring, foreseeable misuse ignored | Standard of care for AI is unsettled; causation through a black box is hard to trace |
| **Strict product liability** | Defective **product** (manufacturing, design, or warning defect) causing harm — no fault needed | Embedded AI in physical products (vehicles, devices, robots) fits most easily | Is standalone software a "product" or a "service"? US courts split historically; "design defect" for a model that learns post-sale is conceptually awkward |
| **Design defect tests** | Consumer expectations test; risk-utility test (incl. reasonable alternative design) | "A reasonable alternative model/guardrail existed" mirrors the less-discriminatory-alternative idea | |
| **Failure to warn** | Inadequate instructions/warnings of non-obvious risks | Not disclosing hallucination rates, automation limits, off-label uses | Learned-intermediary questions with professional users |
| **Misrepresentation / warranty** | False statements of fact; breach of express/implied warranties | Overstated accuracy claims; chatbot giving binding wrong answers | An airline was held to honor a refund policy its customer-service chatbot invented (Canadian tribunal) — companies own their bots' statements |
| **Section 230 note** | Platform immunity for third-party content likely does **not** shield a company for content its own generative model creates | Litigation over chatbot harms to minors is testing these boundaries — unsettled, verify status | |

### EU: the revised Product Liability Directive (adopted 2024; member-state transposition by end-2026)

The headline modernization — know these changes:

| Old PLD (1985) | **Revised PLD** |
|---|---|
| "Product" = tangible movables; software status doubtful | **Software and AI systems are expressly products** (standalone or embedded); so are digital manufacturing files |
| Defect assessed at time of placing on market | Post-sale factors count: **software updates, machine learning after deployment**, cybersecurity vulnerabilities can make a product defective; failure to supply updates can too |
| Compensable harm: death, injury, property | Adds **destruction/corruption of data** and medically recognized **psychological harm** |
| Liable party: producer/importer | Extended chain: manufacturers, importers, **authorized representatives**, fulfilment service providers; **substantial modifiers**; providers of integrated components |
| Claimant proves defect + causation | **Disclosure of evidence** duty on defendants; **rebuttable presumptions** of defect/causation where proof is excessively difficult due to technical/scientific complexity (aimed squarely at AI opacity) or where disclosure is refused |
| — | Development-risk defense retained (member-state options); no fault required throughout |

Companion history: a proposed **AI Liability Directive** (fault-based claims easing) was tabled alongside it but was **withdrawn by the Commission in 2025** — the revised PLD is the operative instrument. Status as of mid-2026 — verify transposition progress.

### Consumer protection: UDAP and dark patterns

**UDAP** = Unfair or Deceptive Acts or Practices — the FTC Act Section 5 template, mirrored by state "mini-FTC Acts" (many with private rights of action) and by the EU's Unfair Commercial Practices Directive.

**Dark patterns** (deceptive design): interface designs that subvert user autonomy. AI supercharges them via personalization ("hyper-nudging"). Canonical taxonomy:

| Dark pattern | Example | AI twist |
|---|---|---|
| Roach motel / obstruction | Easy subscribe, labyrinthine cancel | FTC "click-to-cancel" rulemaking & cases (e.g., against a major e-commerce Prime flow) |
| False urgency/scarcity | Fake countdown timers | Generated dynamically per user |
| Confirmshaming / interface interference | Guilt-tripping decline buttons, pre-ticked boxes | Chatbots emotionally steering users |
| Drip pricing | Fees revealed late | Personalized pricing opacity |
| Disguised ads / impersonation | Bots posing as humans, fake reviews | Generative fake-review mills — FTC finalized a rule banning fake/AI-generated reviews (2024) |
| Anthropomorphic manipulation | Companion bots exploiting attachment/vulnerability | Overlaps EU AI Act Art. 5 manipulation prohibitions |

Regulatory hooks: FTC Section 5 + the fake-reviews rule + Negative Option rule; state UDAP; GDPR fairness + EDPB dark-pattern guidelines for social media; EU Digital Services Act bans dark patterns on platforms; the EU AI Act prohibits *materially distortive* manipulative AI techniques (Lesson 4.02).

### How liability and consumer law interlock for AI governance

- Product-safety-style **pre-market duties** (EU AI Act) reduce post-market **liability** exposure — documentation and logs generated for conformity double as litigation evidence (both shield and sword: discoverable).
- Marketing review is a governance control: every accuracy/capability claim is a potential deception count.
- Incident response and post-market monitoring limit negligence exposure (foreseeability + duty to fix known defects via updates now baked into the revised PLD).

## CASES & EXAMPLES

**Scenario 1 — The hallucinating service bot.** An airline's chatbot invents a bereavement-refund policy; a customer relies on it and is refused the refund. *Analysis:* Company bound by its agent-like bot's representation (negligent misrepresentation/consumer-protection theory); the tribunal-decided real case rejected the argument that the chatbot was "a separate legal entity responsible for its own actions." Governance: constrain bots to vetted content; honor what they say.

**Scenario 2 — Post-sale drift under the revised PLD.** An EU-marketed home robot receives an ML update after which it misjudges obstacles and injures a user; the claimant can't penetrate the model internals. *Analysis:* Software update/learning is assessable for defectiveness under the revised PLD; the claimant can seek **evidence disclosure**, and technical complexity can trigger a **rebuttable presumption** of defect/causation. Strict liability — no negligence proof needed.

**Scenario 3 — Cancel-flow AI.** A subscription app uses a model to predict which users are about to cancel and dynamically inserts extra retention screens and guilt prompts only for them. *Analysis:* Classic dark-pattern obstruction + interface interference, aggravated by personalization; FTC/UDAP exposure (negative-option and Section 5), EU UCPD/DSA exposure, and possible AI Act manipulation analysis if materially distorting behavior causing significant harm.

**Scenario 4 — Overstated autonomy.** A vehicle maker markets driver assistance as "full self-driving" while manuals require constant supervision; a distracted driver crashes. *Analysis:* Parallel exposure: failure-to-warn/design-defect claims, deceptive-advertising claims (regulators have pursued exactly this naming issue), and comparative-fault battles over foreseeable misuse.

## MEMORY HOOKS

- **Negligence vs strict liability:** *negligence judges the maker's conduct; strict liability judges the product itself.*
- **Revised PLD headline — "SUDden Proof":** **S**oftware is a product, **U**pdates & learning count post-sale, **D**ata loss & psych harm compensable, **P**resumptions + disclosure ease **Proof**.
- **AILD is dead (withdrawn 2025); long live the PLD.**
- **Your bot speaks for you** — chatbot promises are company promises.
- **Dark-pattern radar:** urgency, obstruction, shame, disguise, drip — any interface that would look bad read aloud.

**The 5 facts to retain:**
1. US AI harms are litigated through classic theories — negligence, strict product liability (easiest for embedded AI), failure to warn, misrepresentation — with software-as-product and causation as the friction points.
2. The revised EU PLD expressly makes **software/AI a product**, covers post-sale updates and learning, adds data-loss and psychological harm, and eases claimant proof via disclosure duties and rebuttable presumptions.
3. The proposed EU AI Liability Directive was **withdrawn** (2025); the PLD (transposition by end-2026) carries the load — verify current status.
4. UDAP theories police AI **claims** (deception) and AI **design** (unfair manipulation, fake reviews, dark patterns).
5. Companies are accountable for their chatbots' statements and their interfaces' manipulations — "the algorithm did it" is never a defense.

## SELF-CHECK

1. **Q:** Which liability theory requires no proof of fault, and what must be shown instead?
   **A:** Strict product liability — the claimant shows the product was defective (manufacturing, design, or warning defect) and the defect caused the harm.

2. **Q:** Name four claimant-friendly changes in the revised EU Product Liability Directive relevant to AI.
   **A:** Software/AI expressly qualify as products; defectiveness can arise from post-sale updates/machine learning/cyber vulnerabilities; compensable harm extends to data destruction and psychological injury; disclosure obligations plus rebuttable presumptions of defect/causation address AI opacity.

3. **Q:** What happened to the EU's proposed AI Liability Directive?
   **A:** It was withdrawn by the Commission in 2025; fault-based national regimes plus the revised PLD govern (status as of mid-2026 — verify).

4. **Q:** Why did the airline chatbot case matter for AI governance?
   **A:** It established that an organization is responsible for representations its customer-facing AI makes — the bot is not a separate entity; companies must honor or control bot outputs.

5. **Q:** Give three examples of dark patterns and the main US and EU legal hooks against them.
   **A:** False urgency, obstruction of cancellation, confirmshaming/pre-ticked boxes, fake AI-generated reviews. US: FTC Act Section 5, fake-review and negative-option rules, state UDAP. EU: Unfair Commercial Practices Directive, DSA dark-pattern ban, GDPR fairness, AI Act manipulation prohibition.
