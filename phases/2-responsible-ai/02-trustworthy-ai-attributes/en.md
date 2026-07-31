# Trustworthy AI Attributes: NIST's Seven Characteristics

**Phase 2 · Lesson 02 · ~1h · BoK Domain I**

## EXAM FOCUS

Domain I — the attributes of trustworthy AI, anchored to the **NIST AI Risk Management Framework's seven characteristics**. Tested as recall (name/complete the list; match a control to its characteristic) and as scenario (which characteristic is compromised in this fact pattern?). The list is verbatim-memorizable and worth verbatim memorization: it returns in Phase 4 (NIST AI RMF) and quietly structures Domains III–IV answer options.

## CORE

### The seven characteristics (NIST AI RMF 1.0)

NIST frames trustworthy AI as exhibiting seven characteristics — note that three are *compound* phrases, and the exam checks whether you know both halves:

| # | Characteristic | What it means | Example controls |
|---|---|---|---|
| 1 | **Valid & reliable** | Valid: the system measures/does what it claims, confirmed by objective evidence. Reliable: it keeps doing so over time and conditions | Held-out and out-of-time evaluation, defined intended use, robustness testing, drift monitoring, retraining triggers |
| 2 | **Safe** | Does not endanger human life, health, property, or environment under intended or reasonably foreseeable use | Hazard analysis, fail-safe design, operating-condition limits, staged rollout, kill switches, incident response |
| 3 | **Secure & resilient** | Secure: withstands attacks (poisoning, evasion, extraction, prompt injection). Resilient: degrades gracefully and recovers from disruption | Adversarial testing, access controls, supply-chain vetting, redundancy, fallback modes |
| 4 | **Accountable & transparent** | Accountability: identifiable humans/organizations answer for outcomes. Transparency: appropriate information about the system is available to those who need it | Assigned owners, RACI, documentation (model/system cards), disclosure of AI use, audit trails, registries |
| 5 | **Explainable & interpretable** | Explainable: mechanisms for how/why an output happened can be described. Interpretable: outputs are meaningful/understandable to users in context | XAI tooling (LIME/SHAP/counterfactuals), interpretable-model preference where stakes demand it, reason codes for decisions |
| 6 | **Privacy-enhanced** | Values like anonymity and confidentiality are protected in data and model behavior | Data minimization, PETs (differential privacy, federated learning), memorization/leakage testing, purpose limitation |
| 7 | **Fair — with harmful bias managed** | Concerns for equality/equity are addressed; harmful bias is identified and managed (NIST names three bias sources: systemic, computational/statistical, human-cognitive) | Bias testing across groups, representative data checks, fairness metrics, diverse review, redress channels |

Two framing points NIST itself makes (both exam-quotable):

1. **Validity and reliability are the precondition** — an inaccurate system can't be meaningfully "fair" or "safe"; and **accountability sits atop the others** — someone must own each characteristic.
2. **Trade-offs are inherent.** Characteristics tension against each other (privacy vs the data appetite of fairness auditing; explainability vs accuracy in some model choices; security vs transparency). Trustworthiness is *balanced in context*, not maximized on every axis — answers claiming you can maximize all seven simultaneously are wrong.

### Mapping to neighboring vocabularies

Other frameworks slice the same pie with different knives — recognize the family resemblance rather than relearning from zero:

| NIST characteristic | OECD principles echo | EU "Trustworthy AI" (HLEG) echo |
|---|---|---|
| Valid & reliable / Safe / Secure & resilient | Robustness, security and safety | Technical robustness and safety |
| Accountable & transparent | Accountability; transparency and explainability | Accountability; transparency |
| Explainable & interpretable | Transparency and explainability | Transparency |
| Privacy-enhanced | (within human-centred values) | Privacy and data governance |
| Fair with harmful bias managed | Human-centred values and fairness | Diversity, non-discrimination and fairness |

(The EU High-Level Expert Group's seven requirements also include *human agency and oversight* and *societal & environmental well-being* — broader social scope than NIST's system-property focus.)

## CASES & EXAMPLES

1. **Name the compromised characteristic.** A chatbot for benefits applicants gives correct answers but cannot indicate why, and applicants can't tell whether they're talking to a machine. → Two hits: *explainable & interpretable* (no reasons) and *accountable & transparent* (no AI disclosure). The distractor "valid & reliable" fails — accuracy wasn't the problem.

2. **The trade-off scenario.** A team wants to publish full model details to maximize transparency; security objects that detailed disclosure eases evasion attacks (e.g., of a fraud model). Right answer shape: acknowledge the *transparency↔security* tension and calibrate disclosure to audience (regulators get more than the public) — not "transparency always wins" or "security always wins."

3. **Valid-but-not-reliable.** A demand-forecasting model passes validation, then quietly decays over eight months without monitoring. Validity was demonstrated once; *reliability* — sustained performance over time and conditions — was never engineered. Control gap: drift monitoring and retraining triggers.

4. **Fairness without accuracy is meaningless.** A triage model performs near chance for everyone — equally poorly across all demographic groups. "Fair" in the statistical-parity sense, useless and unsafe in fact. Illustrates NIST's point that validity/reliability is the precondition for the other characteristics mattering.

## MEMORY HOOKS

**Mnemonic — "Very Safe Systems Are Enormously Private & Fair":**
**V**alid & reliable · **S**afe · **S**ecure & resilient · **A**ccountable & transparent · **E**xplainable & interpretable · **P**rivacy-enhanced · **F**air (harmful bias managed).

**Compound check:** three characteristics are double-barreled (valid&reliable, secure&resilient, accountable&transparent, explainable&interpretable — four, actually). If an answer option splits or drops a half, it's testing you.

The 5 facts to retain:

1. Seven NIST characteristics: valid & reliable; safe; secure & resilient; accountable & transparent; explainable & interpretable; privacy-enhanced; fair with harmful bias managed.
2. Valid & reliable is the necessary precondition; accountability overarches all.
3. Trade-offs among characteristics are inherent — trustworthiness is balanced in deployment context, never maximized on all axes.
4. NIST's fairness characteristic names three bias sources: systemic, computational/statistical, human-cognitive.
5. OECD and EU HLEG lists are cousins, not clones — HLEG adds human agency/oversight and societal & environmental well-being.

## SELF-CHECK

1. Recite the seven characteristics, keeping every compound intact.
2. Which characteristic is the precondition for the rest, and why?
3. Give one concrete control for each of: secure & resilient, privacy-enhanced, fair with harmful bias managed.
4. A regulator asks who in the company answers for a model's outcomes; nobody can say. Which characteristic failed?
5. Describe one inherent trade-off pair and how a governance answer should handle it.

<details>
<summary>Answers</summary>

1. Valid & reliable; safe; secure & resilient; accountable & transparent; explainable & interpretable; privacy-enhanced; fair — with harmful bias managed.
2. Valid & reliable — a system that doesn't actually work as claimed cannot be meaningfully safe, fair, or trustworthy in any other dimension.
3. Secure & resilient: adversarial/red-team testing (or fallback modes). Privacy-enhanced: differential privacy or minimization plus leakage testing. Fair: disaggregated performance testing across demographic groups with defined metrics and redress.
4. Accountable & transparent — specifically the accountability half: no identifiable human owner for outcomes.
5. E.g., transparency vs security: detailed disclosure can enable gaming/attacks; resolve by calibrating disclosure depth to audience and channel (public notice vs regulator dossier), not by abandoning either value. (Privacy vs fairness-auditing data needs is an equally good answer.)

</details>
