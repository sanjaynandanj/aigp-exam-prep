# Transparency & Explainability: XAI, Disclosures, Counterfactuals

**Phase 2 · Lesson 04 · ~1h · BoK Domain I**

## EXAM FOCUS

Domain I — the transparency cluster. The exam's single most reliable trick here is **conflating the three terms** (transparency / explainability / interpretability); learn the separations verbatim. Also tested: global vs local explanations, XAI technique names at recognition level (LIME, SHAP, counterfactuals), and matching a **disclosure duty** to its audience. Technique math is never tested — names and purposes are.

## CORE

### The three terms, separated

| Term | Definition | Question it answers | Example |
|---|---|---|---|
| **Transparency** | Appropriate openness *about the system*: that AI is used, what it's for, what data it uses, how it was built and governed | "What is this system and how is it used?" | Notice that a chatbot is a bot; a published model card; entry in a public registry |
| **Explainability** | Ability to give *reasons for a specific output* (often via post-hoc techniques) | "Why did I get this result?" | "Your application scored low mainly due to short credit history and high utilization" |
| **Interpretability** | The degree to which a model's mechanics are *understandable by design* | "Can a human follow how it works internally?" | A small decision tree or points-based scorecard you can read |

Relationships worth stating: a system can be *transparent but unexplainable* (fully disclosed deep model, no per-decision reasons) and *explainable but not interpretable* (post-hoc reasons for a black box). Interpretable models are explainable for free; deep models need bolted-on XAI.

### Global vs local explanations

| Scope | Explains | Serves | Example |
|---|---|---|---|
| **Global** | The model's overall behavior — which features matter in general, how it behaves across the input space | Validators, auditors, regulators, model risk teams | "Overall, income and credit history dominate this model's decisions" |
| **Local** | One specific output for one specific input | The affected person, the reviewing human, complaint handlers | "Denied *because* utilization 92% and two recent delinquencies" |

Exam cue: rights of affected individuals (contest a decision, adverse-action reasons) call for **local** explanations; model validation and audit call for **global** ones.

### XAI techniques — name-level knowledge

| Technique | One-liner | Notes |
|---|---|---|
| **LIME** | Approximates the model *locally* with a simple surrogate model to explain one prediction | Local; model-agnostic; an approximation, not the model's truth |
| **SHAP** | Attributes a prediction across input features using game-theoretic (Shapley-value) credit assignment | Local per-prediction, aggregates to global insight; the most-cited attribution method |
| **Counterfactual explanations** | "What minimal change would flip the outcome?" — *"had your income been $5k higher, approved"* | Directly actionable for the affected person; closest fit to recourse/contestation rights |
| **Feature importance (global)** | Ranking of which features drive the model overall | The standard global summary |
| **Surrogate models** | Train an interpretable model to mimic the black box | Fidelity is the question: the surrogate is not the model |

Two governance caveats the exam rewards knowing: **(1) post-hoc explanations are approximations** — they can be unstable or even misleadingly reassuring ("fairwashing"); **(2) where stakes and law demand solid reasons** (credit adverse action), choosing an interpretable model may beat explaining a black box — architecture choice is a governance decision (Lesson 1.03).

### Disclosure duties — who must be told what

| Audience | Typical duty | Legal anchors (previewing Phases 3–4) |
|---|---|---|
| **End users / consumers** | That they're interacting with AI (chatbots); that content is AI-generated or manipulated (deepfake labeling); that emotion recognition/biometric categorization is in use | EU AI Act transparency obligations (Art. 50 family); consumer-protection law (deception) |
| **Affected individuals** | Meaningful information about automated decision-making and its logic; reasons for adverse decisions; route to contest | GDPR Arts. 13–15 & 22; US adverse-action notices (FCRA/ECOA); Colorado AI Act notices |
| **Deployers (from providers)** | Instructions for use, capabilities, limitations, intended purpose | EU AI Act provider→deployer documentation |
| **Regulators / auditors** | Technical documentation, logs, registration entries | EU AI Act technical documentation + EU database; sectoral exam powers |
| **Public** | Registries of systems in use (esp. public sector), published model/system cards | EU database for high-risk systems; municipal/ agency registers |

Design principle: **transparency is audience-calibrated** — depth and form differ per audience; a data scientist's SHAP plot is not a consumer explanation, and dumping documentation on consumers is not transparency.

## CASES & EXAMPLES

1. **Adverse action meets the black box.** A US lender using a complex model must give rejected applicants specific principal reasons (adverse-action notice regime). Post-hoc attribution (SHAP-style) is commonly used to generate reason codes — regulators (e.g., CFPB circulars) have signaled that "the model is too complex to explain" is not a defense. Governance chain: legal explanation duty → architecture and tooling requirements *upstream*.

2. **The undisclosed chatbot.** A company's support "agent Emma" is a bot; customers aren't told. Even before AI-specific law, deception-based consumer protection applies; under the EU AI Act, chatbot disclosure is an explicit transparency obligation. Note the term hit: this is a *transparency* failure — no explainability question anywhere.

3. **Counterfactual as recourse.** A rejected mortgage applicant asks "what would it take?" A counterfactual explanation ("$6k lower revolving balance") gives actionable recourse — but governance must ensure counterfactuals are *honest* (achievable, and the flip would actually happen) and don't leak the model to gamers.

4. **Exam-style discriminator.** "An auditor wants to know which features drive the model overall; a complainant wants to know why *she* was denied." → Global explanation for the auditor; local explanation (reason codes or counterfactual) for the complainant. Any option offering the auditor's artifact to the complainant is the distractor.

## MEMORY HOOKS

**Three-term ladder:** **Transparency** = about the *system* · **Explainability** = about an *output* · **Interpretability** = about the *mechanics, by design*. (System / output / mechanics.)

**Scope rule:** *individual rights → local; validation & audit → global.*

**Technique tags:** LIME = local surrogate; SHAP = feature credit-splitting; counterfactual = "smallest change that flips it."

The 5 facts to retain:

1. Transparency (system openness) ≠ explainability (output reasons) ≠ interpretability (understandable-by-design) — the exam's favorite conflation.
2. Global explanations serve auditors/validators; local explanations serve affected individuals and human reviewers.
3. LIME/SHAP/counterfactuals are post-hoc approximations — useful, imperfect, and capable of false reassurance.
4. Where explanation duties are strict, preferring an interpretable model is a legitimate (often best) governance answer.
5. Disclosure is audience-calibrated: users (AI/label notices), individuals (reasons + contestation), deployers (instructions for use), regulators (technical docs), public (registries).

## SELF-CHECK

1. Assign each term: (a) publishing that a hiring tool is in use and what data it processes; (b) telling a candidate the main factors behind her rejection; (c) using a points-based scorecard anyone can read.
2. When is a local explanation required rather than a global one? Give a legal-flavored example.
3. What is a counterfactual explanation, and why is it especially suited to individual recourse?
4. Give two documented weaknesses of post-hoc XAI that governance should account for.
5. Name three distinct audiences of transparency and the artifact each typically receives.

<details>
<summary>Answers</summary>

1. (a) transparency; (b) explainability (local); (c) interpretability.
2. When a specific person needs reasons for a specific decision — e.g., adverse-action notices in US credit, GDPR meaningful-information/contestation around automated decisions.
3. The minimal change to the input that would have changed the outcome; it directly tells the person what to do differently, matching the logic of recourse and contestation.
4. They are approximations that may be unstable (small input changes → different explanations) and can be curated to look reassuring ("fairwashing"); surrogate fidelity is never perfect.
5. E.g., consumers → AI-interaction/content labels; affected individuals → reason codes/counterfactuals and appeal routes; regulators → technical documentation and logs (also: deployers → instructions for use; public → registries).

</details>
