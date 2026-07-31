# What Is AI: The OECD Definition and Why Definitions Matter Legally

**Phase 1 · Lesson 01 · ~1h · BoK Domain I**

## EXAM FOCUS

Domain I, Foundations of AI governance — understanding what AI is and how it differs from other software. Tested mostly as **fact recall**: identify the elements of the OECD definition, or pick which of four described systems *is* an AI system under an OECD-aligned definition. Occasionally a scenario asks whether a rules-based tool falls in scope of an AI law — that turns entirely on the definition.

## CORE

### The OECD definition (the one that matters)

The OECD's updated definition (2023 revision of the 2019 AI Principles definition) is the reference point for the exam because major legal instruments — including the **EU AI Act** — deliberately aligned with it. In substance, an AI system is:

> A **machine-based system** that, for explicit or implicit objectives, **infers, from the input it receives, how to generate outputs** such as predictions, content, recommendations, or decisions that can influence physical or virtual environments. Different AI systems **vary in their levels of autonomy and adaptiveness** after deployment.

Decompose it — the exam tests the *elements*:

| Element | Meaning | Why it's there |
|---|---|---|
| **Machine-based** | Runs on hardware/software; excludes purely human processes | Scopes to technology |
| **Explicit or implicit objectives** | Goals may be programmed in, or emerge from data/learning | Covers learned behavior, not just coded rules |
| **Infers how to generate outputs** | The system derives outputs from inputs — the load-bearing word is **infers** | Distinguishes AI from software that only executes fixed, human-written rules |
| **Outputs: predictions, content, recommendations, decisions** | Four canonical output types | Content was emphasized in the 2023 update — generative AI is squarely in scope |
| **Influence physical or virtual environments** | Outputs have effects, digital or real-world | Connects the system to consequences (and thus risk) |
| **Varying autonomy and adaptiveness** | Some operate with little human input; some keep learning after deployment | Spectrum, not binary — governance must scale with both |

### AI vs automation vs traditional software

| | Traditional software / automation | AI system |
|---|---|---|
| Logic | Rules written explicitly by humans (if-then, formulas, workflows) | Behavior largely **inferred from data** or learned objectives |
| Behavior change | Only when a human changes the code | Can change with new data, retraining, or online adaptation |
| Predictability | Deterministic; same input → same output | Often probabilistic; edge cases surprise even the builders |
| Explainability of a given output | Read the code | May require dedicated techniques (Phase 2, Lesson 04) |
| Example | Payroll calculator; a thermostat with a fixed setpoint rule | Résumé-screening model; a thermostat that learns your schedule |

Nuance the exam likes: **automation is a spectrum and AI can sit inside automation.** A robotic process automation (RPA) bot following scripted clicks is not AI; the same bot calling an ML model to classify invoices embeds an AI component — and the *system* may then fall under AI rules.

### Why definitions matter legally

1. **Scope = obligations.** If a system meets the legal definition of "AI system," an entire regulatory apparatus can attach (risk classification, conformity assessment, transparency duties). If not, only general law applies.
2. **The EU AI Act adopted an OECD-aligned definition** (Article 3(1)), precisely so that international frameworks, standards, and national laws point at roughly the same class of systems. Its recitals clarify that systems based solely on rules defined by natural persons to automatically execute operations are *not* AI systems.
3. **Boundary-drawing is a live compliance task.** Organizations must inventory systems and decide which ones are "AI" — under-inclusion risks non-compliance; over-inclusion wastes governance capacity.
4. **Definitions travel.** NIST AI RMF, ISO/IEC standards, and the Council of Europe Framework Convention all orbit OECD-style language, so one well-learned definition unlocks several frameworks.

### Related terms you must not confuse

| Term | One-liner |
|---|---|
| Artificial intelligence | The field + the class of systems per definitions above |
| Machine learning | A *subset* of AI: systems that learn patterns from data rather than being explicitly programmed |
| Deep learning | A *subset* of ML using multi-layer neural networks |
| Generative AI | AI that produces content (text, images, audio, code) as its output type |
| AGI (artificial general intelligence) | Hypothetical human-level, cross-domain AI — not a regulated category; don't pick it as an answer to scope questions |

Nesting: **AI ⊃ ML ⊃ deep learning**, and generative AI is (currently) built mostly on deep learning.

## CASES & EXAMPLES

1. **The mortgage rules engine.** A bank's loan tool applies a fixed, human-written checklist: income ratio > X, credit score > Y → approve. Purely explicit rules, no inference from data. Under an OECD-aligned definition this is **not** an AI system — though it may still be regulated as automated decision-making under privacy law (GDPR Art. 22 doesn't require "AI," only automated processing — Phase 3).

2. **The same bank, upgraded.** The bank replaces the checklist with a model trained on historical repayment data that scores applicants. Now the system **infers** outputs (predictions) from inputs — an AI system, and depending on jurisdiction potentially a high-risk one (credit scoring appears in EU AI Act Annex III — Phase 4).

3. **The chatbot boundary question.** A vendor sells "an intelligent FAQ assistant." Diligence reveals it does keyword lookup against a hand-written answer table. Marketing says AI; the definition says no. Lesson: govern by *technical reality*, not product branding — in both directions (some "simple tools" quietly embed models).

4. **The thermostat pair.** Fixed-rule thermostat: automation. Learning thermostat that adapts to occupancy patterns: AI system with post-deployment adaptiveness — the exact property the OECD definition's final clause flags for governance attention.

## MEMORY HOOKS

**Mnemonic — "M-O-I-O-E-A":** **M**achine-based, **O**bjectives (explicit/implicit), **I**nfers, **O**utputs (predictions/content/recommendations/decisions), **E**nvironments (physical/virtual), **A**utonomy & adaptiveness vary.

**Contrast anchor:** *Rules written by hand = software. Behavior inferred from data = AI.* The load-bearing verb is **infers**.

The 5 facts to retain:

1. The OECD 2023-revised definition is the international reference; the EU AI Act aligned with it.
2. Four canonical outputs: predictions, content, recommendations, decisions.
3. "Infers from input" is what excludes fixed rules-based software.
4. Autonomy and adaptiveness are spectrums the definition explicitly flags.
5. AI ⊃ ML ⊃ deep learning; generative AI is defined by its content outputs.

## SELF-CHECK

1. Recite the elements of the OECD definition of an AI system.
2. What single word in the definition separates AI from traditional software, and why?
3. True or false: a system must keep learning after deployment to count as AI.
4. Why did the EU AI Act align its definition with the OECD's?
5. A vendor's "AI-powered" tool turns out to be a static lookup table. What governance conclusion follows, and what caution applies?

<details>
<summary>Answers</summary>

1. Machine-based system; explicit or implicit objectives; infers from input how to generate outputs (predictions, content, recommendations, decisions); outputs influence physical or virtual environments; varying autonomy and adaptiveness after deployment.
2. **Infers** — traditional software executes rules humans wrote; AI derives how to produce outputs from inputs/data.
3. False — adaptiveness *varies*; a frozen, non-learning model is still an AI system.
4. International interoperability: one broadly shared scope so laws, standards (NIST, ISO), and soft law address the same class of systems.
5. It's likely out of scope of AI-specific rules (not an AI system) — but verify technical reality rather than marketing labels, and remember other law (consumer protection, privacy/ADM rules) may still apply.

</details>
