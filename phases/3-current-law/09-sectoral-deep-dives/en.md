# Sectoral Deep-Dives: Employment, Credit, Health, Insurance

**Phase 3 · Lesson 09 · ~1h · BoK Domain II**

## EXAM FOCUS

Scenario questions often anchor in a **sector** and expect you to assemble the applicable stack: the sector statute, the AI-specific overlay, and the governance response. This lesson consolidates four sectors: **employment** (hiring tools), **credit** (FCRA/ECOA adverse action), **health** (HIPAA + FDA SaMD at concept level), and **insurance** (state regulation, Colorado SB 21-169). Learn each sector's *decision*, *statutes*, *AI failure mode*, and *required consumer communication*.

## CORE

### 1. Employment — algorithmic hiring & management

| Layer | Content |
|---|---|
| Federal statutes | Title VII, ADA, ADEA (Lessons 04/07); Uniform Guidelines validation framework |
| AI-specific rules | NYC LL 144 bias audits; Illinois AI Video Interview Act (notice + consent + explanation before AI-analyzed video interviews; demographic reporting if used to screen); Colorado AI Act (employment = consequential decision); Maryland facial-recognition-in-interviews consent law — recognition level |
| Failure modes | Resume screeners replicating historical bias; video/game assessments screening out disability; scheduling/monitoring algorithms (algorithmic management) |
| Governance stack | Pre-deployment validation + adverse-impact testing (four-fifths), vendor due diligence and contractual audit rights, candidate notice, accommodation process, human review of rejections, periodic re-testing |
| EU angle | Employment is **Annex III high-risk** under the AI Act; GDPR Art. 22 + national worker-consultation rules; Platform Work Directive limits algorithmic management |

### 2. Credit — FCRA + ECOA adverse action

Two statutes, two different jobs — a classic exam contrast:

| | **ECOA / Reg B** | **FCRA** |
|---|---|---|
| Governs | Discrimination in any credit decision + adverse-action notices from **creditors** | Consumer reports: accuracy, permissible purpose, and adverse-action duties of **users of reports** and **CRAs** |
| AI hook | Model denials need **specific, accurate principal reasons** (CFPB: complexity is no excuse); fair-lending/disparate-impact testing; proxies | AI scores built on consumer-report data make the vendor potentially a **CRA**; users must give notice identifying the CRA + free-report and dispute rights; accuracy duties reach algorithmic matching (mismatched tenant-screening files drew CFPB/FTC actions) |
| Notice content | Principal reasons for denial (or right to request) | CRA identity, right to free report (60 days), right to dispute; credit-score disclosures |
| Trap | Applies to business credit too | "We're a tech company, not a CRA" fails if you assemble/sell consumer data for eligibility decisions — FCRA follows function |

Also: prudential regulators' **model risk management guidance** (SR 11-7 concept) — validation, monitoring, governance for bank models — a pre-AI framework the exam may reference as the banking template.

### 3. Health — HIPAA + FDA SaMD (concept level)

**HIPAA:**
- Applies to **covered entities** (providers, plans, clearinghouses) and **business associates** — an AI vendor processing PHI for a hospital must sign a **BAA** and use/disclose PHI only as permitted.
- Training models on PHI: needs to fit treatment/payment/operations, or use **de-identification** (Safe Harbor: strip 18 identifiers; or Expert Determination), or authorization. Re-identification risk from rich clinical data is the recognized weakness of de-identification.
- **Minimum necessary** standard tensions with training appetite (mirror of GDPR minimization).
- Gap: HIPAA does **not** cover consumer wellness apps/wearables outside covered entities — the FTC's Health Breach Notification Rule partially fills it.

**FDA — Software as a Medical Device (SaMD):**
- AI intended to **diagnose, treat, or prevent disease** can be a regulated medical device; risk-based pathways (510(k) clearance, De Novo, PMA). Many AI/ML-based devices have been authorized — largely in imaging.
- **Adaptive-algorithm problem:** traditional clearance freezes a device; FDA's answer is the **Predetermined Change Control Plan (PCCP)** — pre-authorize the *envelope* of future model updates (what will change, how it will be validated) so continuous learning doesn't require serial resubmission.
- Related concepts: Good Machine Learning Practice (GMLP) principles; clinical-decision-support software exclusion (non-device CDS must let clinicians independently review the basis — opaque AI recommendations tend to remain devices); lifecycle guidance for AI-enabled device software functions. Generative-AI-in-clinic oversight is still developing — verify current status.

### 4. Insurance — state-regulated + Colorado SB 21-169

- Insurance is regulated by **states** (McCarran-Ferguson); unfair-discrimination prohibitions in rating are longstanding.
- **NAIC Model Bulletin on the Use of AI Systems by Insurers** (2023, adopted by many states): insurers must run a written **AIS program** — governance, risk management, vendor oversight — proportionate to risk; decisions must comply with unfair-trade-practice laws.
- **Colorado SB 21-169** — the trailblazer statute: prohibits insurers' use of **external consumer data and information sources (ECDIS)**, algorithms, and predictive models that **unfairly discriminate** based on race, color, national/ethnic origin, religion, sex, sexual orientation, disability, gender identity/expression; implementing rules (life insurance first) require a governance framework and **quantitative bias testing** (e.g., BIFSG-style race estimation to test outcomes) with reporting to the regulator.
- **New York DFS Circular Letter (2024):** similar expectations for underwriting/pricing — ECDIS transparency, bias analysis, board-level governance.
- Failure modes: proxy discrimination via credit-based scores, ZIP codes, social data; claim-denial automation (litigation over health insurers' bulk claim-review algorithms is ongoing — recognition level).

### Cross-sector pattern (the takeaway grid)

| Sector | Decision | Key statutes | Consumer communication owed |
|---|---|---|---|
| Employment | Hire/promote | Title VII, ADA, ADEA, LL 144, state | Notice of AI use, audit publication (NYC), accommodations |
| Credit | Lend/price | ECOA, FCRA | Adverse-action notice with specific reasons + FCRA disclosures |
| Health | Diagnose/treat/coverage | HIPAA, FDA FD&C Act, state | Authorization/notice for PHI; device labeling; clinician transparency |
| Insurance | Underwrite/price/claims | State codes, SB 21-169, NAIC bulletin | Reasons for adverse underwriting decisions (state-dependent) |

## CASES & EXAMPLES

**Scenario 1 — The screening-report mismatch.** A tenant-screening algorithm merges records of people with similar names; an applicant is rejected over someone else's eviction. *Analysis:* FCRA — the screening firm is a CRA with **maximum possible accuracy** duties (matching algorithms included); the landlord (user) owes an adverse-action notice identifying the CRA so the applicant can dispute. Real enforcement has targeted exactly this.

**Scenario 2 — The adaptive radiology model.** A vendor wants its cleared imaging AI to keep learning from new hospital data post-market. *Analysis:* Unmanaged post-market modification can exceed the device's authorization; the FDA-fit answer is a **PCCP** authorized up front describing planned modifications and validation methods.

**Scenario 3 — Life insurer's social-data model.** A Colorado life insurer prices policies using an external "lifestyle score" built from purchasing and social data. *Analysis:* SB 21-169 territory: ECDIS + predictive model → insurer must test for unfair discrimination against the enumerated classes (quantitative outcome testing per rules), document governance, and remediate disparities — even without any intent.

**Scenario 4 — Hospital chatbot vendor.** A startup pilots a symptom-triage chatbot with a health system, receiving identifiable patient records, and wants to reuse them to improve its general model. *Analysis:* Vendor is a **business associate** — BAA required; reuse for product improvement must be permitted by the BAA and HIPAA (often only de-identified data may be used); minimum-necessary applies; if the bot's function crosses into diagnosis, FDA SaMD analysis is also triggered.

## MEMORY HOOKS

- **Sector = statute pair:** Employment→Title VII+LL 144 · Credit→ECOA+FCRA · Health→HIPAA+FDA · Insurance→state codes+SB 21-169.
- **ECOA vs FCRA one-liner:** *ECOA polices the decision; FCRA polices the data about you.*
- **HIPAA de-ID:** *Safe Harbor = strip 18; Expert = statistician signs.*
- **PCCP:** *pre-approve the change envelope, not each change.*
- **Insurance acronym ECDIS:** External Consumer Data and Information Sources — the regulated fuel of insurtech models.

**The 5 facts to retain:**
1. Employers own hiring-tool outcomes across Title VII/ADA/state overlays; NYC demands audited, published impact ratios.
2. Credit AI owes two notices: ECOA's specific reasons (creditor) and FCRA's CRA-identification/dispute rights (report user) — different statutes, different jobs.
3. AI vendors touching PHI are business associates needing BAAs; training reuse usually requires de-identification or authorization.
4. Adaptive medical AI is managed through FDA's risk pathways plus **Predetermined Change Control Plans**.
5. Insurance AI is state-governed; Colorado SB 21-169 mandates quantitative unfair-discrimination testing of ECDIS-driven models, and the NAIC model bulletin sets governance expectations broadly.

## SELF-CHECK

1. **Q:** A lender uses an AI score from a data broker to deny credit. Which two federal statutes drive the required notices, and what does each add?
   **A:** ECOA/Reg B — adverse-action notice with specific principal reasons; FCRA — if the score derives from a consumer report, notice identifying the CRA plus free-report and dispute rights.

2. **Q:** When does HIPAA permit an AI vendor to train on hospital patient data?
   **A:** Only as a business associate under a BAA within permitted purposes; broader model-improvement reuse generally requires HIPAA de-identification (Safe Harbor's 18 identifiers or Expert Determination) or patient authorization.

3. **Q:** What problem does the FDA's Predetermined Change Control Plan solve for AI devices?
   **A:** It lets manufacturers pre-specify and pre-validate the scope of future model updates so continuously learning SaMD can evolve without a new submission per change.

4. **Q:** What does Colorado SB 21-169 prohibit, and what does compliance practically require of insurers?
   **A:** Use of external consumer data sources, algorithms, and predictive models that unfairly discriminate on enumerated protected traits; practically — a governance framework, quantitative outcome/bias testing (including estimating protected class where not collected), documentation, and regulator reporting.

5. **Q:** Why can a "tech platform" selling AI-generated tenant-risk scores be regulated as a consumer reporting agency?
   **A:** FCRA applies functionally: assembling or evaluating consumer information to furnish reports for eligibility decisions (housing, credit, employment) makes the seller a CRA regardless of its self-description, triggering accuracy and dispute obligations.
