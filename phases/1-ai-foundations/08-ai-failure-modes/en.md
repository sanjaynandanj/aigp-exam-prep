# AI Failure Modes: Bias, Hallucination, Brittleness, Misuse

**Phase 1 · Lesson 08 · ~1h · BoK Domain I**

## EXAM FOCUS

Domain I — the catalogue of ways AI systems fail, with special weight on the **bias sub-taxonomy** (data / label / measurement / aggregation), which appears in stems expecting you to name the *specific* bias type from a fact pattern. Automation bias crosses over into Domain IV oversight scenarios. This is a "name the failure precisely" lesson: the exam's distractors are always the *other* failure modes.

## CORE

### 1. Bias — the four data-side types

"Bias" alone is too coarse for the exam. Learn where in the pipeline each type enters:

| Type | Where it enters | Definition | Example |
|---|---|---|---|
| **Data (representation/sampling) bias** | Collection | Training data under- or over-represents groups relative to the deployment population | Face datasets skewed toward lighter-skinned faces → higher error rates for darker-skinned faces |
| **Label bias** | Annotation | The labels encode biased human judgments — "ground truth" is really recorded opinion | Past hiring decisions used as "good hire" labels import past discrimination |
| **Measurement bias** | Variable choice | The measured variable is a flawed **proxy** for the real target | Using healthcare *cost* as a proxy for health *need* — documented in a widely cited 2019 study (Obermeyer et al.) of a US care-management algorithm that under-referred Black patients because less money had historically been spent on them at equal illness levels |
| **Aggregation bias** | Modeling | One model for everyone when the underlying relationships differ across groups | A single diabetes-risk model ignoring known cross-population differences in biomarker baselines |

Also name-check (they appear as distractors): **selection bias** (whose data got collected at all), **historical bias** (the world itself was inequitable and the data records it faithfully), and **survivorship bias** (only observed outcomes for people the old process approved — you never learn how rejected applicants would have performed).

Two governance corollaries: (a) removing the protected attribute does **not** remove bias — proxies (ZIP code, purchase patterns, word choice) carry it; (b) each bias type has a different fix (rebalance data / re-examine labels / change the proxy / segment models), so *diagnosis precision matters*.

### 2. Hallucination

**Definition:** a generative model producing fluent, confident content that is false or fabricated. Root cause: LLMs are next-token predictors optimizing plausibility, not truth — hallucination is **intrinsic to the mechanism**, reducible (RAG, grounding, better training) but not eliminable. Highest-risk pattern: fabricated *specifics* — citations, case law, dosages, prices — delivered in authoritative register (see *Mata v. Avianca* and the Air Canada chatbot, Lesson 05).

### 3. Brittleness and distribution shift

**Brittleness:** competence collapses outside the training distribution — models fail on inputs that differ from training data in ways humans find trivial. Related: **adversarial examples** — inputs *deliberately* perturbed to cause misclassification (small pixel changes or physical stickers fooling image classifiers, demonstrated repeatedly in the research literature). **Distribution shift** is the non-adversarial version: deployment conditions simply differ from training conditions (new hospital's scanner, new dialect, new market regime — connects to drift, Lesson 07). Governance response: robustness testing, out-of-distribution detection, defined operating conditions ("intended use") and refusal/escalation behavior outside them.

### 4. Misuse and dual use

The failure is in the *user*, not the model working incorrectly — the model works exactly as built, for a harmful purpose:

| Pattern | Examples |
|---|---|
| Deliberate misuse | Deepfakes for fraud/harassment/disinformation, voice cloning scams, generating phishing or malware |
| **Dual use** | Same capability serves good and ill: drug-discovery models can be inverted toward toxins (a published 2022 demonstration); text generators write both marketing and propaganda |
| Off-label use | A tool built for one purpose applied to a riskier one — a chatbot pressed into medical advice |

Governance responses: use policies and terms, abuse monitoring (feasible for closed/API models — Lesson 06), release-strategy decisions, misuse red teaming, and law targeting *uses* (e.g., deepfake labeling, prohibited practices).

### 5. Automation bias

**Definition:** the human tendency to over-trust automated outputs — accepting them uncritically (errors of commission) or failing to act without a system prompt (errors of omission). It is the failure mode *of the human-AI team*, and it quietly defeats the standard safeguard: "a human reviews every decision" is worthless if the human rubber-stamps. Aggravators: time pressure, high system accuracy history, authoritative UX, deskilling. Mitigations (Domain IV): oversight designed for *meaningful* review — showing confidence/uncertainty, requiring justification to agree in edge cases, measuring override rates, training reviewers on system limits.

## CASES & EXAMPLES

1. **COMPAS (2016 debate).** ProPublica reported that the COMPAS recidivism-risk tool produced higher false-positive rates for Black defendants (flagged high-risk but didn't reoffend) and higher false-negative rates for white defendants; the vendor countered that scores were *calibrated* equally across races. Both claims were, on their own terms, statistically true — the deep lesson (formalized in Phase 2 Lesson 03) is that fairness metrics conflict mathematically. For this lesson: label/historical bias territory, since arrest data proxies enforcement patterns, not just crime.

2. **The healthcare-cost proxy (Obermeyer et al., 2019).** Measurement bias, canonical: predicting cost when you mean need systematically deprioritized Black patients. Fix implemented: change the target variable — not the model class. Precisely the "each bias type has its own fix" point.

3. **Sticker on a stop sign.** Researchers showed physical perturbations can cause traffic-sign misclassification. Brittleness/adversarial failure — the model isn't "wrong" on its training distribution; it's operating outside it by design of an attacker. Distractor discipline: this is *not* bias, *not* drift.

4. **The rubber-stamp reviewer (exam style).** A bank requires human sign-off on every AI-flagged transaction; reviewers approve 99.7% of flags within seconds. A discriminatory pattern in flags flows straight through "human review." Name it: automation bias defeating nominal oversight. Fix: redesign the review task (sampling depth, justification prompts, override-rate monitoring) — not more of the same review.

## MEMORY HOOKS

**Bias entry points — "Collect, Label, Measure, Merge":** data bias at collection, label bias at annotation, measurement bias in proxy choice, aggregation bias in one-model-fits-all.

**Failure-mode discriminator questions:** False content, fluently stated? → hallucination. Wrong on weird/novel inputs? → brittleness/shift. Wrong for a *group*? → bias (then name which). Works perfectly for a bad actor? → misuse. Human waves it through? → automation bias.

The 5 facts to retain:

1. Four core bias types by pipeline stage: data (collection), label (annotation), measurement (proxy), aggregation (one-size-fits-all) — plus proxies mean deleting the protected attribute never suffices.
2. The 2019 healthcare-algorithm study is the canonical *measurement bias* case: cost stood in for need; the fix was changing the target variable.
3. Hallucination is intrinsic to generative models (plausibility ≠ truth); mitigable via grounding/RAG, never fully removed.
4. Brittleness = failure outside the training distribution; adversarial examples are its deliberately induced form.
5. Automation bias defeats nominal human review — oversight must be *designed* to stay meaningful and measured (e.g., override rates).

## SELF-CHECK

1. Name the four core bias types and the pipeline stage where each enters.
2. In the Obermeyer healthcare study: which bias type, what was the proxy, and what was the fix?
3. Why is hallucination not simply a bug to be patched?
4. What distinguishes misuse from the other failure modes in this lesson?
5. A hospital's reviewers accept 99% of an AI triage tool's recommendations within seconds. Name the phenomenon and two design mitigations.

<details>
<summary>Answers</summary>

1. Data/representation bias — collection; label bias — annotation; measurement bias — choice of proxy variable; aggregation bias — modeling one population as homogeneous.
2. Measurement bias; healthcare cost proxied health need; fix: replace the target variable with direct measures of need.
3. LLMs generate by predicting plausible next tokens — truth is not the optimization target, so fabrication is a structural property; grounding and RAG reduce it but cannot eliminate it.
4. The system functions as designed — the harm comes from the purpose or user (deliberate misuse, dual use, off-label use), so remedies target access, monitoring, policy, and law rather than model accuracy.
5. Automation bias; mitigations include displaying uncertainty, requiring justification/active engagement on edge cases, monitoring override rates, deep-sampling reviews, and training reviewers on known failure modes.

</details>
