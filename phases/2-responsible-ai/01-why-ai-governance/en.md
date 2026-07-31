# Why AI Governance: The Harms Taxonomy and the Business Case

**Phase 2 · Lesson 01 · ~1h · BoK Domain I**

## EXAM FOCUS

Domain I — understanding the potential harms of AI, the reason governance exists. Tested two ways: **classification recall** (sort a described harm into individual / group / societal, tangible / intangible) and **scenario framing** (identify which harms a fact pattern raises). This taxonomy is also the quiet grammar of everything later: risk assessments, impact assessments, and the EU AI Act's risk tiers are all harm taxonomies wearing legal clothes.

## CORE

### The three levels of harm

| Level | Who is hurt | Harm categories | Examples |
|---|---|---|---|
| **Individual** | An identifiable person | **Discrimination** (denied job/loan/housing), **privacy** (exposure, surveillance, inference of sensitive traits), **safety** (physical injury from vehicles, medical AI, robotics), economic loss, dignitary harm, loss of opportunity | A wrongly rejected applicant; a misidentified arrestee; a patient triaged incorrectly |
| **Group** | A class of people sharing a characteristic | Systematic disadvantage to a protected or vulnerable group, stereotyping, representational harm (degrading portrayals), collective privacy (inferences about a group applied to members) | Higher face-recognition error rates for darker-skinned women; ad systems steering job ads by gender |
| **Societal** | Institutions, publics, the commons | **Manipulation & disinformation** (deepfakes, eroded epistemic trust, election interference), **environmental** (energy and water demands of training/inference), **labor** (displacement, degraded working conditions, algorithmic management), concentration of power, chilling of expression, erosion of due process | Synthetic media flooding an election; mass surveillance normalizing self-censorship |

Why the levels matter practically: **remedies scale with level.** Individual harms suit complaint/appeal channels and compensation; group harms need testing, metrics, and anti-discrimination enforcement; societal harms need regulation, standards, and collective action — no individual lawsuit fixes epistemic pollution.

### Tangible vs intangible

| | Tangible | Intangible |
|---|---|---|
| Nature | Measurable, often monetizable | Real but hard to quantify or evidence |
| Examples | Physical injury, financial loss, lost job | Dignity, autonomy (being manipulated), chilling effects, loss of trust, emotional distress, opportunity you never knew you lost |
| Governance problem | Fits existing liability/compensation regimes | Under-weighted in risk assessments; victims often can't detect it (you never see the ad, job, or price you weren't shown) |

Exam-relevant insight: AI's signature harms skew **intangible and invisible-to-the-victim** — a person never learns an algorithm silently filtered them out. This is a core argument for *ex ante* governance (assess before deployment) rather than relying on *ex post* complaints, and it explains legal designs like transparency duties and registration databases: they make the invisible contestable.

### The governance business case

Governance is not only harm-avoidance; the exam expects the affirmative case:

| Driver | Content |
|---|---|
| **Legal & regulatory** | EU AI Act penalties, sectoral regulators (FTC, EEOC…), privacy law, liability exposure — non-compliance is now priced |
| **Financial** | Failed AI projects, remediation costs, litigation, fines; governance as project-failure insurance |
| **Reputational** | AI scandals are headline events (recruiting tools, chatbots gone wrong); trust is slow to build, fast to lose |
| **Operational** | Governance artifacts (inventories, documentation, monitoring) are also *quality* infrastructure — they make AI work better and scale safer |
| **Commercial** | Enterprise buyers and procurement now demand governance evidence; certification (ISO/IEC 42001) becomes a market signal; trust as differentiator |
| **Innovation-enabling** | Clear guardrails let teams move fast *within* them; without governance, every deployment is a bespoke legal fire drill |

The mature framing (and the one right answers use): governance as **enabler of sustainable AI adoption**, not brake. Distractor framings — "governance exists to slow AI down" or "compliance is purely a cost center" — are wrong on this exam.

## CASES & EXAMPLES

1. **Individual + group: the recruiting tool.** Amazon's abandoned experimental résumé screener (Lesson 1.02) harmed *individuals* (women filtered from consideration — mostly without ever knowing: intangible, invisible) and a *group* (systematic gender disadvantage). Note the governance-positive ending: internal testing caught it and the tool was scrapped pre-scale — detection processes are themselves governance.

2. **Societal: synthetic media in elections.** Documented incidents — such as the AI-generated robocall imitating President Biden's voice before the 2024 New Hampshire primary (which led to FCC action and penalties) — illustrate manipulation harm: the target is not one voter but the integrity of public discourse. No individual remedy suffices; the responses were regulatory and platform-level.

3. **All three levels at once: Dutch childcare benefits scandal.** Individual (families ruined financially), group (disproportionate impact on families with immigration backgrounds), societal (collapse of trust in a public institution; the government resigned in 2021). Use this case when a question asks for a harm that "cascades across levels."

4. **Exam-style classifier.** "A city's predictive-policing tool leads residents of certain neighborhoods to avoid public gatherings for fear of being flagged." — Chilling effect: **societal** (also group), **intangible**. The planted distractor will be "individual, tangible."

## MEMORY HOOKS

**Levels ladder:** *One person → a class of people → the commons.* Individual / group / societal — and remedies scale with the rung.

**"DPS" for individual harms:** **D**iscrimination, **P**rivacy, **S**afety — the big three at person level.

**"MEL" for societal harms:** **M**anipulation, **E**nvironment, **L**abor — plus power concentration.

The 5 facts to retain:

1. Harms classify by level (individual / group / societal) and tangibility (tangible / intangible); both axes appear in stems.
2. AI's signature harms are often intangible and invisible to victims — the core argument for ex ante assessment and transparency duties.
3. Remedies scale with level: appeals for individuals, testing/enforcement for groups, regulation and standards for society.
4. Environmental footprint (energy, water) and labor impacts are *societal harms inside the taxonomy*, not side notes.
5. The business case is affirmative: legal, financial, reputational, operational, commercial, and innovation-enabling — governance enables adoption.

## SELF-CHECK

1. Give the three harm levels with two examples each.
2. Why do intangible, invisible harms argue for ex ante governance rather than complaint-driven enforcement?
3. Classify: an insurer's model quietly charges higher premiums in ZIP codes correlated with ethnicity. Level(s)? Tangible or intangible? Would affected people know?
4. Name four distinct pillars of the governance business case.
5. Which real case cascades across all three harm levels, and what were its consequences?

<details>
<summary>Answers</summary>

1. Individual: wrongful loan denial, physical injury from an autonomous system (also privacy exposure). Group: higher biometric error rates for a demographic group, gender-skewed ad delivery. Societal: deepfake-driven disinformation, environmental footprint of training, labor displacement.
2. Victims cannot complain about filtering, pricing, or exclusion they never perceive — so waiting for complaints systematically under-detects harm; assessment, transparency, and registration must happen before and during deployment.
3. Group-level discrimination via proxy (with individual financial harm); the premium difference is tangible, but victims typically cannot detect it — the invisibility is the governance problem.
4. Any four: legal/regulatory exposure, financial (fines, failed projects, litigation), reputational trust, operational quality, commercial/procurement demands, innovation-enablement.
5. The Dutch childcare benefits scandal — ruined families (individual), disproportionate impact on immigrant-background families (group), institutional trust collapse and the government's 2021 resignation (societal).

</details>
