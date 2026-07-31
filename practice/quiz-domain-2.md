# Domain II Quiz — Laws, Standards and Frameworks

> 20 questions · ~30 minutes · closed book. Take after Phases 3–4.
> This is the heaviest-weighted content family on the exam. Expect the AI Act, GDPR and NIST RMF to dominate.
> Answer key with full rationales at the bottom.

---

**Q1.** A company wants to train a marketing-personalization model on customer data originally collected to fulfill orders. Under GDPR, its first-order legal questions are:

- A. Whether it has a lawful basis for the new processing and whether training is compatible with the original purpose
- B. Whether the model architecture is a neural network
- C. Whether the CE marking has been affixed
- D. Whether the data is stored inside the EU, which alone resolves the issue

**Q2.** *Scenario.* A lender's system auto-scores applications; a staff member clicks "confirm" on every recommendation within seconds, without authority or information to change outcomes. A rejected applicant invokes GDPR Article 22. The strongest analysis is:

- A. Article 22 does not apply because a human clicked the button
- B. Article 22 does not apply because credit decisions never have legal or similarly significant effects
- C. Article 22 likely applies: token human involvement without real influence leaves the decision "based solely on automated processing"
- D. Article 22 applies only if the applicant is a minor

**Q3.** Under GDPR, a DPIA is required before processing that is "likely to result in a high risk" to individuals — which of these AI uses most clearly triggers one?

- A. Spell-checking internal memos with an ML library
- B. Systematic and extensive automated profiling of individuals that significantly affects them
- C. Counting anonymized foot traffic in a mall with no individual-level data
- D. Using AI to compress image files

**Q4.** The FTC has moved against companies for AI-related conduct primarily using its authority over:

- A. Copyright infringement under the DMCA
- B. Prudential banking supervision
- C. Spectrum licensing
- D. Unfair or deceptive acts or practices under FTC Act Section 5 — including deceptive AI claims and, in settlements, ordering deletion of models built on ill-gotten data

**Q5.** *Scenario.* A US employer uses a vendor's AI video-interview scoring tool. The tool disproportionately screens out applicants over 55. Under EEOC guidance on federal anti-discrimination law, the employer:

- A. Can remain liable for discriminatory outcomes even though a vendor built the tool
- B. Is immune because liability follows the software developer alone
- C. Is safe as long as the vendor certified the tool as "EEOC compliant"
- D. Faces liability only if it intended to discriminate

**Q6.** The Colorado AI Act is best summarized as:

- A. A ban on all AI use in consumer-facing products in Colorado
- B. A duty of reasonable care on developers and deployers of high-risk AI used in consequential decisions, to protect consumers from algorithmic discrimination — with notices, impact assessments and AG enforcement
- C. A biometric-consent statute with a private right of action
- D. A copyright statute for AI-generated works

**Q7.** *Scenario.* An Illinois gym chain uses fingerprint scanners for member check-in without obtaining written releases or publishing a retention policy. Members sue directly. Which statute fits this fact pattern?

- A. NYC Local Law 144
- B. The Colorado AI Act
- C. GDPR Article 9
- D. Illinois BIPA — informed written consent and retention rules for biometric identifiers, enforceable through a private right of action

**Q8.** NYC Local Law 144 applies to:

- A. Any AI system used anywhere in New York State, in any sector
- B. Only fully autonomous hiring decisions with no human involvement at any stage
- C. Automated employment decision tools that substantially assist hiring or promotion decisions for NYC roles — requiring an annual independent bias audit, publication of results, and candidate notice
- D. Credit-scoring models used by New York banks

**Q9.** As of mid-2026, the dominant US litigation theory against foundation-model developers over training data is:

- A. Copyright infringement claims for unlicensed reproduction of protected works in training, with fair use as the developers' central defense
- B. Antitrust price-fixing
- C. Patent infringement of the transformer architecture
- D. Criminal wiretapping

**Q10.** *Scenario.* A US marketing agency generates an image entirely from a text prompt and seeks to register the copyright, listing the AI as author. Under current US Copyright Office practice, the registration will:

- A. Succeed, because prompts are creative expression that automatically confers authorship over outputs
- B. Fail for the AI-authored material: works lacking human authorship are not copyrightable, though human creative selection/arrangement may be protectable
- C. Succeed only if the model was trained on licensed data
- D. Fail unless the agency registers the model itself first

**Q11.** Which practice is **prohibited** under Article 5 of the EU AI Act?

- A. Emotion recognition used by a hospital for medical diagnostics with patient safety purposes
- B. An AI chatbot that fails to disclose it is not human
- C. AI-based spam filtering
- D. AI systems inferring emotions of employees in the workplace, outside medical or safety purposes

**Q12.** *Scenario.* A German company deploys an AI system that ranks and filters incoming job applications before any human sees them. Under the EU AI Act, the system is:

- A. Prohibited under Article 5
- B. High-risk under Annex III (employment), triggering provider and deployer obligations
- C. Minimal risk, because a human makes the final hiring decision
- D. Outside the Act's scope because recruitment is a private matter

**Q13.** Under the EU AI Act, a general-purpose AI model is presumed to pose **systemic risk** when:

- A. The cumulative compute used for its training exceeds 10^25 floating-point operations (or the Commission designates it)
- B. It has more than one million users in the EU
- C. It is open-source
- D. It generates images rather than text

**Q14.** The EU AI Act's maximum administrative fines are tiered as follows:

- A. A flat 4% of global turnover for any infringement, mirroring GDPR
- B. 10% for prohibited practices, 5% for everything else
- C. Up to 7% of global annual turnover (or €35M) for prohibited practices; up to 3% (€15M) for most other obligations; up to 1% (€7.5M) for supplying incorrect information
- D. Criminal penalties only, with no administrative fines

**Q15.** Which statement about the EU AI Act's application timeline is correct?

- A. Every provision became applicable on the date of entry into force in 2024
- B. Prohibitions applied first in August 2026, followed by GPAI rules in 2027
- C. High-risk obligations applied before the prohibitions
- D. Staggered application: prohibitions (with AI-literacy duties) from February 2025, GPAI obligations from August 2025, and most high-risk (Annex III) obligations from August 2026

**Q16.** Under the EU AI Act, the actor that first makes an AI system from a third-country provider available on the EU market is the:

- A. Importer — who must verify the provider completed conformity assessment and documentation before placing the system on the market
- B. Deployer
- C. Notified body
- D. Authorized representative, who assumes all provider obligations automatically

**Q17.** In the NIST AI RMF, establishing the system's context, intended purposes, and identifying risks belongs to ______, while applying quantitative/qualitative techniques to analyze and track those risks belongs to ______.

- A. GOVERN; MANAGE
- B. MEASURE; MAP
- C. MAP; MEASURE
- D. MANAGE; GOVERN

**Q18.** ISO/IEC 42001 is best described as:

- A. A product-safety certification that individual AI models receive after lab testing
- B. A certifiable management-system standard (AIMS) specifying organizational requirements — policy, roles, risk processes, controls, continual improvement — for governing AI
- C. A mandatory EU regulation applicable from 2026
- D. A glossary standard defining AI terminology

**Q19.** The Council of Europe Framework Convention on AI (2024) is notable because it is:

- A. A voluntary code of conduct for European startups
- B. Binding only on EU member states, as an annex to the AI Act
- C. A technical interoperability standard
- D. The first binding international treaty on AI — anchored in human rights, democracy and the rule of law — open for signature by non-European states as well

**Q20.** Which "rest of world" pairing is accurate?

- A. UK: comprehensive horizontal AI statute in force since 2023
- B. China: purely voluntary guidance with no binding AI rules
- C. Singapore: voluntary Model AI Governance Framework and AI Verify testing toolkit rather than a horizontal AI statute
- D. Brazil: constitutional ban on all automated decision-making

---

## ANSWER KEY & RATIONALES

**Q1 — A.** Repurposing personal data for training requires a lawful basis plus a purpose-compatibility analysis (Art. 5(1)(b), Art. 6).
- B: GDPR is technology-neutral; architecture is irrelevant.
- C: CE marking is an AI Act/product-law concept, not GDPR.
- D: Storage location doesn't answer lawfulness or compatibility.

**Q2 — C.** Rubber-stamping is the classic Article 22 edge case: human involvement must be meaningful (authority + competence + real influence) to take a decision outside "solely automated."
- A: A click without power to change the outcome doesn't count.
- B: Credit denial is a textbook "similarly significant" effect.
- D: Article 22 protects all data subjects, not only minors.

**Q3 — B.** Systematic, extensive profiling with significant effects is an explicit DPIA trigger (Art. 35(3)(a)).
- A/D: Trivial-risk processing; no high risk to individuals.
- C: Anonymized, non-individual data falls outside the trigger.

**Q4 — D.** Section 5 UDAP is the FTC's workhorse — deceptive AI capability claims, unfair uses, and settlements requiring deletion of models trained on improperly obtained data ("algorithmic disgorgement").
- A: Copyright is not FTC turf.
- B: That's the Fed/OCC.
- C: That's the FCC.

**Q5 — A.** Under Title VII/ADEA disparate-impact principles, the employer using the tool retains responsibility for discriminatory outcomes; outsourcing the tool doesn't outsource liability.
- B: Vendors may face exposure too, but employer liability persists.
- C: Vendor self-certifications have no safe-harbor effect.
- D: Disparate impact requires no intent.

**Q6 — B.** Colorado's law targets algorithmic discrimination in consequential decisions, imposing reasonable-care duties, notices and impact assessments on developers and deployers, enforced by the Attorney General. (Its effective date was pushed into 2026 during Colorado's 2025 special session — timing details are volatile; the structure is the exam point.)
- A: It regulates, not bans.
- C: That's BIPA.
- D: It doesn't address copyright.

**Q7 — D.** Biometric identifiers + no written release + no retention schedule + private lawsuits = BIPA.
- A: LL144 is NYC hiring tools.
- B: Colorado's act covers consequential-decision AI, no private right of action.
- C: GDPR doesn't govern an Illinois gym's domestic processing.

**Q8 — C.** LL144 = AEDTs substantially assisting NYC hiring/promotion decisions: annual independent bias audit, published summary, advance candidate notice.
- A: It's a city law limited to employment decisions.
- B: "Substantially assist" covers more than fully autonomous decisions.
- D: Credit models are outside its scope.

**Q9 — A.** The wave of suits by authors, artists and media companies alleges unlicensed copying for training; developers principally argue fair use (transformativeness vs. market harm). Outcomes remain in flux as of mid-2026 — the exam tests the theory, not case scores.
- B/C/D: Not the operative theories.

**Q10 — B.** The US Copyright Office requires human authorship; purely AI-generated material is unregistrable, though human selection/arrangement/modification can be protected.
- A: Prompts alone haven't been accepted as conferring authorship.
- C: Training-data licensing doesn't create authorship.
- D: No such requirement exists.

**Q11 — D.** Workplace (and education) emotion inference is prohibited, save for medical or safety purposes — which is why option A's hospital use survives.
- A: Falls within the medical/safety carve-out.
- B: Nondisclosure breaches Article 50 transparency, a lower tier — not Article 5.
- C: Spam filtering is minimal risk.

**Q12 — B.** Recruitment/CV-filtering systems sit in Annex III's employment category → high-risk, with the full obligations cascade.
- A: Not on the Article 5 list.
- C: Downstream human decision doesn't remove the classification.
- D: The Act squarely covers private-sector employment tools.

**Q13 — A.** The 10^25 FLOPs training-compute threshold creates the systemic-risk presumption; the Commission can also designate models.
- B/C/D: User counts, licensing model and modality are not the statutory test.

**Q14 — C.** 7%/3%/1% (€35M/€15M/€7.5M) is the memorized trio; SMEs get the lower of the amounts.
- A: 4% is GDPR's ceiling, a favorite distractor.
- B/D: Fabricated tiers; the Act uses administrative fines.

**Q15 — D.** Entry into force August 2024, then staggered: Feb 2, 2025 (prohibitions, AI literacy), Aug 2, 2025 (GPAI, governance, penalties), Aug 2, 2026 (most remaining, incl. Annex III high-risk), with embedded-product high-risk running to 2027.
- A/B/C: Each scrambles the sequence.

**Q16 — A.** The importer places a third-country provider's system on the EU market and must verify conformity assessment, documentation and marking beforehand.
- B: Deployers use systems; they don't place them on the market.
- C: Notified bodies assess conformity.
- D: Authorized representatives act on a provider's mandate; obligations don't transfer "automatically."

**Q17 — C.** MAP establishes context and identifies risks; MEASURE analyzes, assesses and tracks them (GOVERN is the cross-cutting culture function; MANAGE prioritizes and acts).
- A/B/D: Function confusions — MAP-before-MEASURE is a top exam trap.

**Q18 — B.** ISO/IEC 42001 is an auditable, certifiable AI management system standard for organizations, in the family of ISO 27001 — not a per-model product certificate.
- A: It certifies management systems, not models.
- C: It's voluntary (though useful toward AI Act conformity culture).
- D: Terminology lives in ISO/IEC 22989.

**Q19 — D.** The Framework Convention is the first binding international AI treaty, rights-and-rule-of-law oriented, and open to signature beyond Europe (e.g., by non-CoE states).
- A: It binds ratifying states, not startups voluntarily.
- B: It is a Council of Europe instrument, distinct from the EU and its AI Act.
- C: It sets legal principles, not technical specs.

**Q20 — C.** Singapore leads with voluntary tools: the Model AI Governance Framework and AI Verify.
- A: The UK has (as of mid-2026) favored a principles-based, regulator-led approach rather than a comprehensive horizontal statute.
- B: China has binding, targeted rules (recommendation-algorithm provisions, deep synthesis rules, generative AI measures).
- D: Brazil has been advancing risk-based AI legislation, not a constitutional ban.

---

## Score interpretation

| Score | Verdict |
|---|---|
| **17–20** | Ready — Domain II is where exams are won; keep the AI Act tables warm with a final-week second pass. |
| **14–16** | Review weak areas — most misses cluster in AI Act actors/timeline and Article 22; reread those lessons and journal every miss. |
| **< 14** | Redo the phase — return to Phases 3–4 in full before retaking. Do not proceed to Phase 5 on a sub-14 Domain II score. |
