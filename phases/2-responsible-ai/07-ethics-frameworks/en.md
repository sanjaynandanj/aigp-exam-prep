# Ethics Frameworks: OECD AI Principles, UNESCO, and the Principles-to-Practice Gap

**Phase 2 · Lesson 07 · ~1h · BoK Domain I**

## EXAM FOCUS

Domain I — the international ethics-framework landscape. The **OECD AI Principles are the highest-yield item**: know the structure (5 values-based principles + 5 recommendations to governments) and recognize each principle from a paraphrase. UNESCO's Recommendation is tested at identity level (what it is, who adopted it, what's distinctive). The principles→practice gap is a scenario theme: spot the company with beautiful principles and no operational machinery.

## CORE

### OECD AI Principles (2019, updated 2024)

The first intergovernmental AI standard — adopted by OECD members and additional adherent countries, and the basis for the G20's AI principles. Two halves:

**Half 1 — five values-based principles** (for all AI actors):

| # | Principle | Substance |
|---|---|---|
| 1 | **Inclusive growth, sustainable development and well-being** | AI should benefit people and planet — growth, inclusion, environment |
| 2 | **Human rights and democratic values, incl. fairness and privacy** | Respect rule of law, human rights, equality, privacy throughout the lifecycle (2024 update sharpened this framing) |
| 3 | **Transparency and explainability** | Meaningful, context-appropriate information so people can understand and challenge outcomes |
| 4 | **Robustness, security and safety** | Systems function appropriately and safely across their lifecycle, with risk managed continuously |
| 5 | **Accountability** | AI actors are accountable for proper functioning, per their roles and the state of the art |

**Half 2 — five recommendations to governments** (policy-maker duties):

| # | Recommendation |
|---|---|
| 1 | Invest in AI research and development |
| 2 | Foster an inclusive AI-enabling ecosystem (data, compute, technologies) |
| 3 | Shape an enabling, interoperable governance and policy environment |
| 4 | Build human capacity and prepare for labour-market transition |
| 5 | International co-operation for trustworthy AI |

Why the OECD framework matters beyond its text (exam-quotable): it supplied the **shared definition of an AI system** (Lesson 1.01) and the **lifecycle framing** that later hard law (EU AI Act) and frameworks (NIST) built on — the connective tissue of global AI governance.

### UNESCO Recommendation on the Ethics of AI (2021)

| Fact | Value |
|---|---|
| What | The first *global* standard on AI ethics — a (non-binding) Recommendation |
| Who | Adopted by acclamation by UNESCO's member states (193 at adoption) — broader than the OECD's largely wealthy-democracy membership |
| Distinctives | Strong emphasis on **human dignity and human rights, environmental sustainability, gender equality, cultural diversity**; includes concrete *policy action areas* (incl. ethical impact assessment, data governance, education) |
| Notable exclusion | States are asked not to use AI for **social scoring or mass surveillance** — language that foreshadows EU AI Act prohibitions |

Contrast to remember: **OECD = influential among advanced economies, source of the canonical definition; UNESCO = near-universal membership, broadest ethical scope, explicit implementation tools.**

### Industry and other principle sets

| Source | Note |
|---|---|
| Asilomar AI Principles (2017) | Early influential researcher/industry statement — research culture, value alignment, long-term/existential-safety issues; the "safety research" vocabulary originates here |
| IEEE's Ethically Aligned Design | Engineering-community ethics effort feeding technical standards (IEEE 7000 series) |
| Montreal Declaration for Responsible AI (2018), Beijing AI Principles (2019), Rome Call for AI Ethics (2020) | Regional/religious counterparts — same five-theme convergence, different cultural emphasis |
| Partnership on AI, GPAI (Global Partnership on AI), MLCommons AI Safety Benchmark | Multistakeholder bodies translating principles into shared research, tooling, and evaluation |

### Company AI principles — know the big four

Exam cue: scenario-based questions sometimes name a specific firm's principle (e.g., *"Google's AI principles require…"*, *"Microsoft's Responsible AI Standard…"*). You need recognition, not recitation.

| Company | Framework | Distinctive emphasis & operational hooks |
|---|---|---|
| **Google (2018, updated 2024/2025)** | *AI Principles* + annual Responsible AI Progress Report | Original 2018 list: socially beneficial · avoid unfair bias · built & tested for safety · accountable to people · privacy-by-design · scientific excellence · available for uses that accord with these principles. Original "will not pursue" list (weapons, mass-surveillance, breach of international law/human rights) was **revised in Feb 2025** to focus on bold+responsible+collaborative innovation with human-rights/international-law due diligence — frequently cited as an example of principles evolving under commercial/geopolitical pressure. Operational: internal review bodies, model cards, SAIF (Secure AI Framework), responsible-release checklists. |
| **Microsoft (2018)** | *Six Responsible AI Principles* + *Responsible AI Standard v2 (2022)* | Six principles: **fairness · reliability & safety · privacy & security · inclusiveness · transparency · accountability** (with transparency+accountability as "foundational"). Operational machinery is the exam-worthy bit: **Office of Responsible AI (ORA)**, Aether committee, Responsible AI Champs network, mandatory **Impact Assessment template**, Sensitive Uses review process, and the Responsible AI Standard that translates each principle into testable requirements. Microsoft was the first big tech to publish a prescriptive internal standard. |
| **OpenAI** | *Charter* (2018) + *Usage Policies* + *Model Spec* (2024, updated 2025) | Charter commitments: broadly distributed benefit, long-term safety, technical leadership, cooperative orientation. Operational: **Preparedness Framework** (catastrophic-risk evaluation across cyber/CBRN/persuasion/autonomy with capability thresholds and a *Safety Advisory Group* → board), **Model Spec** (hierarchy of platform > developer > user > guideline), usage policies, system cards, Red Teaming Network. "Scaling with safety" vocabulary. |
| **Anthropic** | *Responsible Scaling Policy (RSP)* (2023, updated 2024/2025) + *Acceptable Use Policy* + *Core Views on AI Safety* | **AI Safety Levels (ASL-1…ASL-5)** gating capabilities to safety commitments — the clearest industry example of a *capability-triggered* governance regime. **Constitutional AI** training method tied to a public "constitution." Explicit focus on catastrophic/existential risk, interpretability research, and policy engagement. |
| **IBM** | *Principles for Trust and Transparency* (2018) + Everyday Ethics for AI | Three pillars — purpose (augment, not replace), transparency, skills — plus five "Everyday Ethics" areas. Operational: AI Ethics Board, FactSheets for models, OpenScale/Watson Governance tooling. Enterprise-governance tilt. |
| **Meta** | Responsible AI pillars + system/model cards + open-weights (Llama) acceptable-use policy | Fairness, privacy, safety, transparency, accountability, governance; distinctive emphasis on **open-release risk management** (acceptable-use policy for Llama, cybersecurity evals, red-teaming). |
| **Amazon / AWS** | Responsible AI dimensions + Bedrock Guardrails + service-level policies | Eight dimensions (fairness, explainability, privacy & security, safety, controllability, veracity & robustness, governance, transparency) and tooling (AI Service Cards, Bedrock Guardrails). Enterprise-platform framing. |

**Meta-finding** (supported by academic mapping studies of dozens of AI ethics documents): **remarkable convergence on ~5 themes** — transparency, justice/fairness, non-maleficence/safety, responsibility/accountability, privacy. The *what* is settled; the *how* is not — which sets up:

### The principles → practice gap

Principles fail to self-execute for identifiable reasons — and each reason names its remedy:

| Gap driver | Remedy (the operational turn) |
|---|---|
| Abstract values, no decision procedure ("be fair" — by which metric? — Lesson 03) | Standards, metrics, and documented trade-off decisions |
| No assigned owners or consequences | Governance roles, accountability chains (Lessons 05, 09) |
| No lifecycle integration | Gates, impact assessments, reviews embedded in delivery (Lesson 08; Phases 5–6) |
| No measurement or assurance | Testing, audits, KPIs, certification (ISO/IEC 42001) |
| Incentive conflict (ship fast vs check first) | Executive mandate, resourced second line, protected escalation |

The label for the failure mode: **"ethics washing"** — publishing principles as reputation management while decision-making continues unchanged. The 2019–2026 arc of the whole field is the move from *principles* (what) to *operationalization* (how) to *regulation* (must) — a framing worth carrying into every later phase.

## CASES & EXAMPLES

1. **Identify the framework.** "An intergovernmental standard whose five principles include accountability and transparency, and which also directs governments to invest in AI R&D and prepare labour markets." → OECD AI Principles (the government-directed half is the giveaway — UNESCO's is broader-scoped and near-universal; NIST is a risk framework, not principles to governments).

2. **The two-halves trap.** Exam stem asks which of the following is an OECD *values-based principle*: "international co-operation for trustworthy AI" vs "robustness, security and safety." The first is a *recommendation to governments*; the second is the principle. Knowing the split defeats the distractor.

3. **Ethics washing in the wild.** A company publishes AI principles, then disbands or under-resources the team meant to apply them; product launches never see an ethics review. Scenario answers should name the missing machinery — ownership, gates, measurement — not propose "better principles."

4. **Convergence, used properly.** A multinational must draft global AI policy across jurisdictions. Because OECD/UNESCO/industry principles converge on the same ~5 themes, it can adopt one values baseline globally and vary only the *legal compliance layer* per jurisdiction — the practical payoff of convergence, and a realistic exam answer.

5. **Pick the firm.** A capability-triggered governance regime that pre-commits the company to safety requirements once a model crosses defined capability thresholds. → **Anthropic's Responsible Scaling Policy (ASL levels).** OpenAI's analog is the **Preparedness Framework**; Google's is the **Frontier Safety Framework**. Microsoft's analog is the pre-launch Sensitive Uses review + Responsible AI Standard. Recognizing *which firm, which name* is a common Phase-2 distractor pattern.

## MEMORY HOOKS

**OECD principles mnemonic — "I Heart That Robust Accountability":** **I**nclusive growth · **H**uman rights & democratic values (fairness, privacy) · **T**ransparency & explainability · **R**obustness, security & safety · **A**ccountability.

**OECD recommendations mnemonic — "R.E.G.I.C.":** **R**&D investment · **E**cosystem · **G**overnance environment · **I**nvest in people (human capacity/labour) · **C**o-operation internationally.

**OECD vs UNESCO in one line:** *OECD wrote the definition; UNESCO signed up (nearly) the world.*

**Firm → signature program (one-liners):**
- **Google** → AI Principles + Frontier Safety Framework + SAIF
- **Microsoft** → Six principles + **Responsible AI Standard v2** + ORA/Aether governance
- **OpenAI** → Charter + **Preparedness Framework** + Model Spec
- **Anthropic** → **Responsible Scaling Policy / ASL levels** + Constitutional AI
- **IBM** → Trust & Transparency pillars + FactSheets + AI Ethics Board
- **Meta** → Responsible AI pillars + Llama acceptable-use + system cards
- **AWS** → Eight responsible-AI dimensions + Bedrock Guardrails + AI Service Cards

The 5 facts to retain:

1. OECD AI Principles (2019, updated 2024): 5 values-based principles + 5 recommendations to governments — the first intergovernmental AI standard, source of the canonical AI-system definition, basis for G20.
2. The five principles: inclusive growth; human rights & democratic values (fairness/privacy); transparency & explainability; robustness/security/safety; accountability.
3. UNESCO Recommendation (2021): adopted by all member states — the first truly global AI-ethics instrument; distinctives include environment, gender, cultural diversity, and warnings against social scoring/mass surveillance.
4. Dozens of principle sets converge on ~5 themes (transparency, fairness, safety, accountability, privacy) — consensus on *what*, not *how*.
5. The principles→practice gap is closed by machinery — owners, gates, metrics, audits — and its absence has a name: ethics washing.
6. Industry signatures to know by name: Microsoft **Responsible AI Standard**, Google **Frontier Safety Framework + SAIF**, OpenAI **Preparedness Framework + Model Spec**, Anthropic **Responsible Scaling Policy (ASL levels) + Constitutional AI**, IBM **FactSheets**, AWS **Bedrock Guardrails**.

## SELF-CHECK

1. Reproduce the OECD structure: how many of what, addressed to whom?
2. Name all five OECD values-based principles.
3. Give three features that distinguish the UNESCO Recommendation from the OECD Principles.
4. What five themes do AI ethics documents worldwide converge on?
5. A firm has published principles but no review gates, owners, or metrics. Name the failure mode and the three most direct fixes.
6. Match firm → named program: (a) ASL levels; (b) Responsible AI Standard v2; (c) Preparedness Framework; (d) Frontier Safety Framework + SAIF; (e) FactSheets.
7. Which **six** principles make up Microsoft's responsible-AI framework?

<details>
<summary>Answers</summary>

1. Five values-based principles addressed to all AI actors, plus five recommendations addressed to governments/policy-makers.
2. Inclusive growth, sustainable development and well-being; human rights and democratic values incl. fairness and privacy; transparency and explainability; robustness, security and safety; accountability.
3. Near-universal adoption (all UNESCO member states) vs OECD's narrower adherence; broader ethical scope (environment, gender equality, cultural diversity); concrete policy action areas incl. ethical impact assessment — plus explicit language against social scoring and mass surveillance.
4. Transparency, justice/fairness, non-maleficence/safety, responsibility/accountability, privacy.
5. Ethics washing; fixes: assign accountable owners, embed review gates into the lifecycle, and measure/assure compliance (metrics, audits) — i.e., build the operational machinery the principles lack.
6. (a) Anthropic; (b) Microsoft; (c) OpenAI; (d) Google; (e) IBM.
7. Fairness; reliability & safety; privacy & security; inclusiveness; transparency; accountability — with transparency and accountability treated as foundational.

</details>
