# High-Risk AI: Annex III Categories and the Classification Flowchart

**Phase 4 · Lesson 03 · ~1.5h · BoK Domain II**

## EXAM FOCUS

"Is this system high-risk?" is the gateway question for the whole compliance regime, so the exam drills it relentlessly. You need: the **two routes** into high-risk (Annex I product-safety and Annex III use-cases), all **eight Annex III areas** with representative examples, and the **Art. 6(3) filter** that lets some Annex III systems escape — plus its own exception (profiling never escapes). Practice until you can run the flowchart on any scenario in under 30 seconds.

## CORE

### Route 1 — Annex I: product-safety AI (Art. 6(1))

A system is high-risk if **both**:
1. It is a product, or a **safety component** of a product, covered by EU harmonization legislation listed in **Annex I** (machinery, toys, lifts, radio equipment, pressure equipment, medical devices, in-vitro diagnostics, civil aviation, motor vehicles, marine equipment, rail, agricultural vehicles, cableways, PPE, gas appliances…);
2. That product/component must undergo a **third-party conformity assessment** under that legislation.

Examples: AI controlling a surgical robot, an AI braking module in a vehicle, AI in an insulin pump. These follow their **sectoral** conformity routes with AI Act requirements folded in (and get the latest application date — Aug 2027).

### Route 2 — Annex III: the eight stand-alone high-risk areas (Art. 6(2))

| # | Area | Representative systems |
|---|---|---|
| 1 | **Biometrics** (where permitted) | Remote biometric identification (non-real-time and permitted real-time), biometric categorization by sensitive/protected attributes (where not prohibited), **emotion recognition** (where not prohibited) |
| 2 | **Critical infrastructure** | Safety components in management/operation of critical digital infrastructure, road traffic, and water/gas/heating/electricity supply |
| 3 | **Education & vocational training** | Admission/assignment to institutions, evaluating learning outcomes, assessing appropriate education level, **monitoring prohibited behavior during tests** (exam proctoring) |
| 4 | **Employment & worker management** | Recruitment/selection (targeted ads for jobs, screening/filtering applications, evaluating candidates), decisions on promotion/termination, task allocation based on behavior/traits, monitoring and evaluating performance |
| 5 | **Essential services** (private & public) | Eligibility for public benefits; **creditworthiness/credit scoring** (except financial-fraud detection); **life & health insurance risk assessment and pricing**; classifying/dispatching emergency calls and emergency triage |
| 6 | **Law enforcement** (where permitted) | Victim-risk assessment, polygraph-type tools, evidence-reliability evaluation, recidivism/offending risk assessment (not solely-profiling — that's banned), profiling in investigations |
| 7 | **Migration, asylum & border control** | Polygraph-type tools, risk/security assessments of entrants, examining asylum/visa/residence applications, identifying persons (except travel-document verification) |
| 8 | **Administration of justice & democratic processes** | Assisting judicial authorities in researching/interpreting facts and law and applying law to facts (or ADR with legal effect); systems intended to **influence elections/referenda outcomes or voting behavior** (excluding backend campaign logistics tools) |

**Memory architecture:** areas 1–2 = *bodies and lifelines*; 3–5 = *life chances* (school, work, money); 6–8 = *state power* (police, borders, courts/votes).

### The Art. 6(3) filter (derogation)

An Annex III system is **NOT high-risk** if it "does not pose a significant risk of harm to health, safety or fundamental rights, including by not materially influencing the outcome of decision making," because it only:
- **(a)** performs a **narrow procedural task**; or
- **(b)** **improves the result of a previously completed human activity**; or
- **(c)** detects decision-making **patterns or deviations** without replacing/influencing prior human assessment (without proper human review); or
- **(d)** performs a **preparatory task** to an assessment.

**The override:** a system that performs **profiling of natural persons** is **always high-risk** — the filter can never rescue it.

**Paper trail:** a provider invoking Art. 6(3) must **document the assessment before market placement** and **register** the system in the EU database's derogation section; market-surveillance authorities can challenge the call. Misclassifying to dodge obligations is itself sanctionable.

### The classification flowchart — run it every time

```
1. Is the practice prohibited (Art. 5)?             → YES: banned. Stop.
2. Is it a safety component/product under Annex I
   legislation requiring 3rd-party conformity?      → YES: HIGH-RISK (Route 1).
3. Does the use case fall in an Annex III area?     → NO: not high-risk
                                                       (check transparency duties + GPAI).
4. Does it involve profiling of natural persons?    → YES: HIGH-RISK. No escape.
5. Does an Art. 6(3) ground apply (narrow procedural /
   improving completed human work / pattern detection
   with human review / preparatory) AND no significant
   risk incl. no material influence on the decision?  → YES: NOT high-risk — document + register.
                                                      → NO:  HIGH-RISK (Route 2).
```

Dynamic elements: the Commission can **amend Annex III** (add/modify use cases) and adjust the Art. 6(3) conditions via delegated acts, with guidelines and practical examples required — Annex III is a living list. (Simplification/omnibus discussions may adjust details — status as of mid-2026, verify.)

### Classification traps the exam sets

| Trap | Correct analysis |
|---|---|
| "It's only decision support; a human decides" | Human presence doesn't defeat classification — Annex III asks about the **intended use area**; material influence matters only inside the 6(3) filter analysis |
| Fraud-detection credit AI | Explicitly carved out of the creditworthiness item |
| General insurance pricing (auto/home) | Only **life and health** insurance risk assessment/pricing is listed |
| Spam filter at a bank | Not in Annex III at all — minimal risk |
| CV-parsing that only extracts fields into a form | Plausible 6(3)(a)/(d) narrow-procedural/preparatory escape — *if* documented and no profiling |
| Exam-proctoring software | Explicitly high-risk (education area) |
| Deepfake generator | Not high-risk per se — transparency-tier labeling duties instead |

## CASES & EXAMPLES

**Scenario 1 — The triage bot.** A hospital deploys AI that classifies and prioritizes incoming emergency calls. *Analysis:* Annex III area 5 (emergency-call classification/dispatch and emergency triage) → high-risk. The vendor is the provider; the hospital is a deployer with its own duties (Lesson 04).

**Scenario 2 — The interview scheduler vs the interview scorer.** Tool A automatically schedules interviews once recruiters pick candidates. Tool B ranks candidates from video interviews. *Analysis:* Both sit in the employment area, but Tool A performs a narrow procedural/preparatory task with no material influence on outcomes → documented Art. 6(3) escape plausible. Tool B evaluates candidates — squarely high-risk, and its trait-based evaluation is profiling, which forecloses the filter anyway.

**Scenario 3 — Annex I route.** A manufacturer adds an AI perception module as the safety component of an industrial robot covered by the Machinery Regulation with third-party assessment. *Analysis:* High-risk via **Art. 6(1)/Annex I**, not Annex III; conformity is integrated into the machinery assessment; the Aug 2027 application date applies to such embedded products.

**Scenario 4 — The over-cautious classifier.** A provider self-declares its grammar-checking tool "high-risk (education)" to look safe, while a competitor claims its student-essay grading engine is exempt as "just decision support." *Analysis:* The grammar checker isn't within the education use cases (not an evaluation of learning outcomes determining access/level) → not high-risk. The grading engine **is** the listed use case (evaluating learning outcomes); "decision support" is not one of the 6(3) grounds and grading materially influences outcomes → high-risk; the exemption claim invites market-surveillance action.

## MEMORY HOOKS

- **Annex III mnemonic — "B-C-E-E-E-L-M-J":** *"**B**ig **C**ompanies **E**valuate **E**very **E**mployee, **L**awyers **M**ind **J**ustice"* → **B**iometrics, **C**ritical infrastructure, **E**ducation, **E**mployment, **E**ssential services, **L**aw enforcement, **M**igration, **J**ustice & democracy.
- **Cluster story:** *bodies & lifelines → life chances → state power.*
- **6(3) filter — "NIPP":** **N**arrow procedural · **I**mproving completed human work · **P**attern detection (human-reviewed) · **P**reparatory. And **profiling pierces** all four.
- **Two doors into high-risk:** *Annex I = what the AI sits inside; Annex III = what the AI is used for.*
- **Escape hatch paperwork:** claim 6(3) → **document + register** or it doesn't count.

**The 5 facts to retain:**
1. High-risk has two routes: Annex I safety components (third-party-assessed products) and Annex III's eight use-case areas.
2. The eight Annex III areas: biometrics, critical infrastructure, education, employment, essential services (credit, life/health insurance, benefits, emergency), law enforcement, migration/border, justice & democratic processes.
3. Art. 6(3) exempts narrow-procedural, human-work-improving, human-reviewed pattern-detection, and preparatory systems that pose no significant risk — but **profiling systems are always high-risk**.
4. Providers using the derogation must document the assessment pre-market and register in the EU database; authorities can second-guess.
5. Annex III is amendable by the Commission — the list is designed to evolve (verify current list as of exam time).

## SELF-CHECK

1. **Q:** Name the eight Annex III areas.
   **A:** Biometrics; critical infrastructure; education and vocational training; employment and worker management; access to essential private and public services; law enforcement; migration, asylum and border control; administration of justice and democratic processes.

2. **Q:** What two conditions make a product-embedded AI high-risk under the Annex I route?
   **A:** It is a product or safety component covered by listed EU harmonization legislation, **and** that product requires third-party conformity assessment under that legislation.

3. **Q:** A bank's AI flags anomalous transactions for fraud analysts. High-risk?
   **A:** No — financial fraud detection is expressly excluded from the creditworthiness high-risk item, and fraud detection isn't otherwise listed (pattern-detection with human review also fits the 6(3) logic).

4. **Q:** Why can an HR analytics tool never use the Art. 6(3) derogation if it builds behavioral profiles of workers?
   **A:** Art. 6(3) contains an absolute exception: systems that perform profiling of natural persons are always considered high-risk regardless of the four escape grounds.

5. **Q:** What must a provider do administratively when it concludes its Annex III-area system is not high-risk under Art. 6(3)?
   **A:** Document that assessment before placing the system on the market, register the system in the EU database (derogation section), and be ready to provide the documentation to national authorities on request.
