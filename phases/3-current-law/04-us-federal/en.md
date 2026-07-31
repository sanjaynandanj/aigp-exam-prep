# US Federal: FTC Section 5, EEOC, CFPB, and the Sectoral Approach

**Phase 3 · Lesson 04 · ~1.5h · BoK Domain II**

## EXAM FOCUS

The exam's US-federal theme is simple and heavily tested: **there is no comprehensive federal AI law** — the US governs AI through *existing sectoral statutes* enforced by agencies. You must match the agency to its statute, its AI theory of harm, and its signature remedy. The three stars: **FTC** (Section 5 unfairness/deception + algorithmic disgorgement), **EEOC** (Title VII + ADA for hiring tools), **CFPB** (ECOA adverse-action notices). Executive-branch AI policy shifts with administrations — the durable exam content is the statutory enforcement framework.

## CORE

### The big picture

| Feature | US federal approach |
|---|---|
| Comprehensive AI statute | **None** — contrast with the EU AI Act |
| Governing method | Sectoral statutes + agency enforcement + executive orders/agency guidance (non-binding or changeable) |
| Consequence | "Existing law applies to AI" — agencies jointly stated they need no new authority to police algorithmic harms |

### FTC — Section 5 of the FTC Act

Prohibits **"unfair or deceptive acts or practices"** (UDAP) in or affecting commerce.

| Theory | Applied to AI | Examples of the pattern |
|---|---|---|
| **Deception** | False/unsubstantiated claims about what AI can do ("AI washing"); undisclosed AI use; fake AI-generated reviews | FTC's "Operation AI Comply" sweep targeted exaggerated AI claims; action against a retailer's facial-recognition misidentifications framed partly on misrepresentation |
| **Unfairness** | Practice causing substantial injury, not reasonably avoidable, not outweighed by benefits — covers biased or reckless model deployment, using consumer data for training contrary to promises | Facial recognition falsely flagging shoppers as shoplifters; secretly repurposing user data for model training |
| **Algorithmic disgorgement** (model deletion) | Remedy requiring destruction of **models and algorithms trained on illegally obtained data** — not just the data | Ordered in matters involving a photo-storage service that trained facial recognition on user photos contrary to promises, a weight-loss app involving children's data (with COPPA), and an Everalbum-style consent decree line of cases |

Also FTC-adjacent: **COPPA** (children's data — feeds disgorgement cases), commercial-surveillance rulemaking interest, and warnings that quietly **changing privacy policies retroactively** to permit AI training may be deceptive.

### EEOC — employment discrimination

Enforces **Title VII** (race, color, religion, sex, national origin), the **ADA**, and **ADEA** against employers — including when discrimination is delivered by a vendor's algorithm.

- **Title VII guidance on algorithmic selection tools:** an employer can be liable for **disparate impact** caused by an AI hiring/promotion tool even if a third party built it; the four-fifths rule is a starting heuristic; employers should demand validation evidence (job-relatedness/business necessity).
- **ADA guidance:** AI assessments can unlawfully **screen out** people with disabilities (e.g., video-analysis penalizing speech impairments; gamified tests disadvantaging motor impairments); employers must provide **reasonable accommodations** and avoid tools that function as unlawful **medical inquiries**.
- **Settled matter to know generically:** the EEOC settled its first AI hiring case against a tutoring company whose software automatically rejected older applicants based on age — straight disparate treatment via a coded rule.

### CFPB — credit and consumer finance

Enforces **ECOA/Regulation B** and shares FCRA territory.

- **Adverse action notices:** creditors must give **specific, accurate reasons** for denials. CFPB circulars confirm: *"the model is too complex to explain" is not a defense* — you may not use a model you cannot explain to the required specificity, and reasons must reflect the actual factors, not boilerplate checklists.
- Scrutiny of **digital marketing/steering, chatbots in banking** (deficient service can violate consumer law), and home-appraisal algorithms (with prudential regulators — AVM quality-control rules).

### Other federal actors at recognition level

| Agency | AI hook |
|---|---|
| **DOJ Civil Rights** | Fair Housing Act — settled with a large platform over discriminatory ad-delivery algorithms; joined interagency statement |
| **FDA** | AI/ML as Software as a Medical Device (covered in Lesson 09) |
| **NIST** | Voluntary standards & AI RMF — *not* a regulator |
| **NHTSA / FAA / SEC / FINRA** | Autonomous vehicles / aviation / AI-related securities claims ("AI washing" enforcement by the SEC against advisers overstating AI use) |
| **Congress** | Narrow enactments only (e.g., the National AI Initiative Act — coordination/R&D, TAKE IT DOWN-style content laws); repeated comprehensive bills have not passed |
| **Executive orders** | Set federal-agency policy direction; changeable with each administration — the exam expects you to know they are **not statutes** |

### The joint agencies statement

FTC, EEOC, CFPB, and DOJ issued a joint statement (2023) affirming that **existing legal authorities apply fully to automated systems** — the canonical citation for the "enforcement-led, sectoral" characterization.

## CASES & EXAMPLES

**Scenario 1 — Marketing meets Section 5.** A startup advertises "our AI detects fraud with 99.9% accuracy" with no substantiation, and quietly uses customer uploads to train new products despite a policy promising otherwise. *Analysis:* Two Section 5 counts — **deception** (unsubstantiated performance claims) and unfair/deceptive **data re-use**; plausible remedy includes deletion of models trained on the improperly used data (algorithmic disgorgement).

**Scenario 2 — The vendor excuse.** An employer's AI video-interview tool disproportionately rejects candidates over 55. HR argues "the vendor is responsible." *Analysis:* Under EEOC guidance, the **employer** remains liable under Title VII/ADEA for tools used in its selection process; it should have measured adverse impact and demanded validation. Vendor contracts can allocate costs but not statutory liability.

**Scenario 3 — Black-box denial.** A fintech's deep-learning credit model denies an applicant; the adverse-action notice lists generic reasons pulled from a standard checklist that don't match the model's actual drivers. *Analysis:* ECOA/Reg B violation per CFPB circulars — reasons must be specific and accurate; complexity is no excuse. Governance answer: use explainability methods or constrain the model class.

**Scenario 4 — Disgorgement stakes.** A photo app trained a face-recognition model on user photos after telling users their photos were used only for storage. *Analysis:* FTC pattern case: consent decree requiring deletion of the ill-gotten data **and the models derived from it** — the point being that violating data promises can cost you the model itself.

## MEMORY HOOKS

- **Agency → statute → AI harm:** "**F**TC **U**ses **D**eception; **E**EOC **T**ests **T**ools; **C**FPB **E**xplains **C**redit" → FTC = UDAP/Section 5; EEOC = Title VII/ADA on selection tools; CFPB = ECOA adverse-action specificity.
- **Algorithmic disgorgement in one sentence:** *ill-gotten data poisons the model — delete both.*
- **Three unfairness elements (FTC):** substantial injury + not reasonably avoidable + not outweighed by benefits.
- **No federal AI act:** if an answer choice assumes a comprehensive US AI statute, it's wrong (status as of mid-2026 — verify current status).

**The 5 facts to retain:**
1. The US approach = sectoral statutes + enforcement + soft guidance; no omnibus federal AI law.
2. FTC Section 5 reaches both **false AI claims** and **unfair AI deployment/data misuse**; its signature AI remedy is **algorithmic disgorgement**.
3. Employers are liable for discriminatory outcomes of **vendor** hiring tools (Title VII disparate impact; ADA screen-out/accommodation).
4. Under ECOA, adverse-action reasons must be **specific and accurate** — model opacity is no defense.
5. The 2023 joint FTC-EEOC-CFPB-DOJ statement: existing authority fully applies to automated systems.

## SELF-CHECK

1. **Q:** What are the two prongs of FTC Section 5 and one AI application of each?
   **A:** Deception (e.g., unsubstantiated "AI-powered" performance claims) and unfairness (e.g., deploying facial recognition that causes substantial, unavoidable consumer injury; repurposing user data for training contrary to promises).

2. **Q:** Define algorithmic disgorgement and why the FTC uses it.
   **A:** A remedy ordering destruction of models/algorithms trained on unlawfully collected or used data — it removes the economic benefit of the violation, since deleting only the raw data would leave the value embedded in the model.

3. **Q:** Under EEOC guidance, can an employer escape Title VII liability because a third-party vendor designed the biased screening tool?
   **A:** No. The employer using the tool in its selection process bears responsibility for adverse impact and must show job-relatedness/business necessity; vendor origin is not a defense.

4. **Q:** A lender says its neural network is too complex to generate specific denial reasons. What does the CFPB say?
   **A:** ECOA/Reg B still requires specific, accurate adverse-action reasons; if the creditor cannot explain the model to that standard, it may not lawfully use it.

5. **Q:** Why are US executive orders on AI of limited durability compared with the frameworks above?
   **A:** They bind only the executive branch, are not statutes, and can be revoked or replaced by subsequent administrations — the statutory/enforcement framework (FTC Act, Title VII, ECOA) is the stable law.
