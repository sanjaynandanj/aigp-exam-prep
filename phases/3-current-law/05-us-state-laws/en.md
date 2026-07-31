# US State AI Laws: Colorado AI Act, Illinois BIPA, NYC Local Law 144, California

**Phase 3 · Lesson 05 · ~1.5h · BoK Domain II**

## EXAM FOCUS

With no comprehensive federal law, US states are the laboratory — and the exam loves comparing them. Highest yield: **Colorado AI Act** (first comprehensive state AI law: developer/deployer duty structure), **Illinois BIPA** (biometrics + private right of action), **NYC Local Law 144** (AEDT bias audits), and **California's** ADMT rules under CCPA/CPRA. Know each law's *trigger*, *who it binds*, *core duty*, and *enforcement mechanism* — those four attributes are what stems test.

## CORE

### Colorado AI Act (SB 24-205) — the first comprehensive US state AI law

> Status note: Colorado's legislature has amended the timeline since enactment; the effective date was pushed from its original 2026 target (to June 30, 2026 by special-session amendment). **Status as of mid-2026 — verify current effective date and any substantive amendments.**

| Element | Rule |
|---|---|
| Scope | **High-risk AI systems** = those making, or a substantial factor in making, **consequential decisions** (education, employment, financial/lending, essential government services, health care, housing, insurance, legal services) |
| Core concept | Duty of **reasonable care** to protect consumers from **algorithmic discrimination** (unlawful differential treatment/impact on protected classes) |
| **Developer duties** | Documentation and disclosures to deployers (intended use, data summaries, limitations, discrimination-risk mitigation), public statement of high-risk systems, disclose known risks to the AG |
| **Deployer duties** | Risk management program (explicitly may align with **NIST AI RMF / ISO 42001**), **impact assessments** (pre-deployment and periodic), notify consumers of AI use in consequential decisions, adverse-decision explanation + **right to correct data and appeal to human review** where feasible |
| Transparency | Consumers must be told when they're interacting with AI (unless obvious) |
| Enforcement | **Attorney General only** — no private right of action; rebuttable presumption of reasonable care for compliance with recognized frameworks |

### Illinois BIPA — Biometric Information Privacy Act (2008)

| Element | Rule |
|---|---|
| Covers | Biometric identifiers (fingerprint, voiceprint, face geometry, retina/iris scans, hand geometry) and biometric information |
| Core duties | **Written notice + written release (consent) before collection**; public retention/destruction policy; no selling/profiting from biometrics; reasonable security |
| Enforcement | **Private right of action** — the feature that makes BIPA the most litigated biometric law: statutory damages per violation ($1,000 negligent / $5,000 reckless-intentional) |
| Key litigation facts | *Rosenbach*: no actual harm needed — statutory violation suffices for standing; a social-media platform paid a **$650M class settlement** over face-tagging; a facial-recognition scraping company settled a BIPA class action with a novel equity-share structure; a 2024 amendment limited claims so repeated scans of the same person count as **one** violation for accrual |
| AI relevance | Face recognition, voice-based AI, emotion analysis pipelines all touch BIPA when Illinois residents' biometrics are processed without consent |

### NYC Local Law 144 (effective/enforced 2023) — AEDT bias audits

| Element | Rule |
|---|---|
| Covers | **Automated Employment Decision Tools** used to *substantially assist or replace* discretionary hiring/promotion decisions for NYC jobs |
| Core duties | Annual **independent bias audit** (impact ratios by sex, race/ethnicity, and intersectional categories); **publish** a summary of results; give candidates **notice** (≥10 business days) of AEDT use and the qualifications/characteristics assessed; offer info on data + alternative process where available |
| Enforcement | Civil penalties per violation per day; enforced by the city (DCWP); no private right of action under the law itself (discrimination claims still ride under other statutes) |
| Exam hook | First US mandate for **algorithmic bias audits** in employment — a template concept |

### California

| Instrument | AI relevance |
|---|---|
| **CCPA/CPRA + CPPA ADMT regulations** | The privacy agency finalized regulations on **automated decision-making technology** (approved 2025, phasing in): businesses using ADMT for **significant decisions** (finance, housing, employment, education, healthcare) must give **pre-use notice**, honor **opt-out rights** (with exceptions), and provide **access/explanation** of ADMT logic and outcomes; plus risk-assessment and cybersecurity-audit requirements for high-risk processing. Status as of mid-2026 — verify final scope/compliance dates |
| **SB 1001 (B.O.T. Act, 2019)** | Unlawful to use a **bot to mislead** a person about its artificial identity to incentivize a sale or influence an election vote — disclosure cures |
| **Other CA laws to recognize** | AB 2013 (training-data transparency for generative AI), SB 942 (AI content disclosures), CMIA/physician rules on AI in utilization review; a broad frontier-model safety bill was vetoed in 2024 with a narrower transparency law (SB 53) following in 2025 — mention level |

### Texas & Utah — mention level

- **Texas (TRAIGA, Texas Responsible AI Governance Act, enacted 2025, effective Jan 1, 2026):** prohibited-uses approach (intentional discrimination, manipulation, certain government social scoring/biometrics), AG enforcement, regulatory sandbox — notably *intent-based* rather than effects-based. Verify current status.
- **Utah (AI Policy Act, 2024):** generative AI **disclosure** duties in consumer transactions (on request; proactive for regulated professions), an Office of AI Policy + learning-lab/sandbox model.

### Comparison table (the exam's favorite format)

| Law | Trigger | Who's bound | Core duty | Enforcement |
|---|---|---|---|---|
| Colorado AI Act | High-risk AI in consequential decisions | Developers & deployers | Reasonable care vs algorithmic discrimination; impact assessments; notices | AG only |
| Illinois BIPA | Biometric collection | Private entities | Notice + written consent + retention policy | **Private right of action** |
| NYC LL 144 | AEDT in hiring/promotion (NYC) | Employers/agencies | Annual independent bias audit + publish + candidate notice | City penalties |
| CA ADMT regs | ADMT in significant decisions | CCPA-covered businesses | Notice, opt-out, access/explanation, risk assessments | CPPA/AG (CCPA remedies) |
| CA SB 1001 | Bots influencing sales/votes | Bot operators | Disclose bot identity | UDAP-style |

## CASES & EXAMPLES

**Scenario 1 — Time-clock biometrics.** A national employer uses fingerprint time clocks in its Chicago warehouses without written releases. *Analysis:* Classic BIPA violation; employees can sue directly (private right of action), statutory damages accrue without proving injury (*Rosenbach*); post-2024 amendment, repeated scans of one worker = one accruing violation.

**Scenario 2 — The multi-state hiring tool.** A company uses an AI resume screener for roles in NYC and Denver. *Analysis:* NYC → LL 144: annual independent bias audit, published summary, 10-business-day candidate notice. Colorado → deployer duties under the AI Act (risk program, impact assessment, notice, human appeal) once effective — plus EEOC exposure federally. The exam rewards spotting that **one tool triggers multiple overlapping regimes**.

**Scenario 3 — Reasonable-care safe harbor.** A Colorado deployer aligns its AI risk program to the NIST AI RMF and documents impact assessments. *Analysis:* The Colorado AI Act gives a **rebuttable presumption of reasonable care** for following recognized frameworks — a direct statutory payoff for framework adoption (and a favorite exam link between law and NIST RMF).

**Scenario 4 — Sales chatbot.** A California e-commerce chatbot poses as "Ashley from support" and never discloses it's automated while upselling. *Analysis:* SB 1001 violation — bots used to incentivize a sale must not mislead about artificial identity; clear disclosure cures.

## MEMORY HOOKS

- **"Colorado copies Europe, Illinois lets you sue, New York audits, California discloses."** — one line per regime.
- **BIPA damages ladder:** $1k negligent / $5k reckless — and *no injury required*.
- **LL 144 trio:** **A**udit annually, **A**nnounce results, **A**dvise candidates (10 business days).
- **Colorado's two hats:** *developers document, deployers assess* — duties split by role, mirroring the EU AI Act's provider/deployer architecture.
- Anything with a moving effective date (Colorado, CA ADMT phase-ins, Texas) → answer "verify current status" in real life; on the exam, know the *structure*, not the date.

**The 5 facts to retain:**
1. Colorado AI Act = first comprehensive US state AI law; duty of reasonable care against algorithmic discrimination; developer/deployer split; AG-only enforcement; effective date amended (verify).
2. BIPA is dangerous because of **private right of action + statutory damages without proof of harm**.
3. NYC LL 144 mandates **annual independent bias audits** with published results and candidate notice for AEDTs.
4. California regulates AI mainly through **privacy law (ADMT regulations)** plus targeted statutes like the bot-disclosure law.
5. Framework compliance (NIST RMF/ISO 42001) earns a **rebuttable presumption** under Colorado — the exam's favorite law-to-framework bridge.

## SELF-CHECK

1. **Q:** Which state law is most likely to produce a class action over an AI face-tagging feature, and why?
   **A:** Illinois BIPA — it has a private right of action with per-violation statutory damages, and *Rosenbach* held no actual injury is required.

2. **Q:** Contrast enforcement of the Colorado AI Act with BIPA.
   **A:** Colorado: exclusive Attorney General enforcement, no private suits, with a rebuttable presumption for framework compliance. BIPA: private right of action driving mass class litigation.

3. **Q:** List three obligations NYC Local Law 144 imposes on an employer using an AEDT.
   **A:** Commission an annual independent bias audit (impact ratios incl. intersectional), publicly post an audit-results summary, and give candidates advance notice (≥10 business days) of AEDT use and assessed qualifications.

4. **Q:** Under Colorado's law, what must a *developer* hand a *deployer*?
   **A:** Documentation of intended uses, training-data summaries, known limitations and discrimination risks, performance/mitigation information — enough for the deployer to run its own impact assessments.

5. **Q:** What consumer rights attach to a "significant decision" made with ADMT under California's CPPA regulations?
   **A:** Pre-use notice, the right to opt out of the ADMT (subject to exceptions), and rights of access/explanation regarding the logic and outcome — alongside business-side risk assessments.
