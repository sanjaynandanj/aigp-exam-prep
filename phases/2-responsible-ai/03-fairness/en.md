# Fairness: The Competing Definitions and Why You Can't Have Them All

**Phase 2 · Lesson 03 · ~1.5h · BoK Domain I**

## EXAM FOCUS

Domain I — fairness concepts. The exam tests: (1) **group vs individual fairness** as a conceptual split, (2) recognizing the three flagship group metrics (demographic parity, equalized odds, calibration) from plain-language descriptions, (3) the **impossibility insight** — the metrics mathematically conflict, so metric choice is a *policy* decision, and (4) protected classes as the legal scaffolding. No formulas required — but you must match a described measurement to its name.

## CORE

### Two families of fairness

| Family | Core question | Strength | Weakness |
|---|---|---|---|
| **Group fairness** | Do outcomes/error rates look right *across groups* (e.g., by sex, race)? | Measurable, auditable, maps to anti-discrimination law | Says nothing about any single person; can be satisfied while individuals are treated arbitrarily |
| **Individual fairness** | Are *similar individuals treated similarly*? | Intuitive justice ideal | "Similar" requires a similarity definition — which smuggles the hard question back in; rarely operationalized |

The exam's usual move: describe one and ask which it is. "Two applicants with near-identical profiles received different outcomes" → individual fairness concern. "The approval rate for women is half that for men" → group fairness concern.

### The three flagship group metrics

Setup for intuition: a model predicts "repay / default" and groups A and B apply.

| Metric | Plain-language demand | Recognize it by… |
|---|---|---|
| **Demographic parity** (statistical parity) | Equal *positive-outcome rates* across groups — same share of A and B approved | Talk of approval/selection **rates**, with no reference to who actually qualified. Related legal echo: the four-fifths rule of thumb in US employment-selection analysis |
| **Equalized odds** (error-rate balance) | Equal *error rates* across groups — same false-positive and false-negative rates for A and B (among truly qualified people, equal chances of approval) | Talk of **false positives / false negatives / mistakes** distributed across groups |
| **Calibration** | Equal *score meaning* across groups — "a 70% risk score" corresponds to the same actual 70% frequency in A and B | Talk of what a **score means** or predicted probabilities matching reality per group |

### The impossibility results, at intuition level

Formal results (associated with work by Kleinberg, Mullainathan & Raghavan and by Chouldechova, both 2016) show: **when base rates differ between groups** — that is, the underlying frequency of the outcome genuinely differs — **no non-trivial system can satisfy calibration and both error-rate balance conditions simultaneously.** Improve one, and another necessarily degrades.

Intuition without math: if the true outcome frequency differs across groups, a score that "means the same thing" in both groups (calibration) must produce different error-rate patterns across them — and forcing equal error rates breaks what scores mean. There is no free lunch; the conflict is arithmetic, not implementation sloppiness.

**The governance consequence — the exam's favorite sentence:** *choosing a fairness metric is a policy and values decision, not a technical one.* It requires deciding which mistakes matter most, for whom, in this context — and therefore belongs to accountable governance bodies (with legal, ethics, and affected-community input), documented and defensible — not defaulted silently by an engineer.

### Choosing in context

| Context | Often-prioritized metric | Why |
|---|---|---|
| Punitive decisions (detention, fraud flags) | False-positive balance | Wrongly punishing the innocent is the harm to equalize |
| Allocative/opportunity decisions (loans, jobs, aid) | False-negative balance / opportunity | Wrongly excluding the qualified is the harm to equalize |
| Risk communication to decision-makers | Calibration | Scores must mean what they say to be usable |
| Representation-type goals (interview slates) | Demographic parity | The rate itself is the policy goal |

### Protected classes

Group fairness is legally anchored to **protected characteristics** — in US federal law variously: race, color, religion, sex, national origin (Title VII), age, disability, genetic information, plus sector-specific ones (e.g., ECOA adds marital status, public-assistance receipt); EU law protects a comparable, broader-in-places set. Two AI-specific twists: (1) **proxies** — models discriminate via correlated features (ZIP code, names, word choice) without seeing the protected attribute (Lesson 1.08); (2) the **measurement paradox** — auditing group fairness *requires* group data that privacy law restricts collecting; lawful approaches (special-purpose collection, inference with care, PET-protected audit sets) are an active governance problem.

## CASES & EXAMPLES

1. **COMPAS, properly understood.** ProPublica (2016): the recidivism tool's false-positive rate was higher for Black defendants and false-negative rate higher for white defendants — an *equalized odds* violation. Northpointe's rebuttal: scores were *calibrated* across races. Base rates in the (arrest-based) data differed, so both could be true at once — the impossibility theorem walking around in the wild. This is the single most exam-ready fairness case: know which metric each side invoked.

2. **The interview-slate policy.** A company mandates that interview shortlists mirror applicant-pool demographics. That's demographic parity as an explicit policy goal — legitimate as a *chosen* value, but note what it doesn't guarantee: nothing about error rates or individual comparability. If a question asks "which metric does this policy implement," rates-without-reference-to-qualification = demographic parity.

3. **The fraud-flag trade.** A benefits agency tunes its fraud model to equalize false-positive rates across demographic groups (punitive context — wrongly accusing is the harm). Consequence, per the impossibility logic: scores will not stay perfectly calibrated across groups. Governance done right = the agency *documents* that trade and why; done wrong = discovering the trade in litigation.

4. **Exam-style matcher.** "Among applicants who would in fact repay, men and women are approved at the same rate." → equal true-positive/false-negative behavior = **equalized odds** family (equal opportunity, precisely). "Applicants scored 80 default at the same rate whether from group A or B." → **calibration**.

## MEMORY HOOKS

**Metric recognizers:** *rates* → demographic parity; *errors* → equalized odds; *score meaning* → calibration.

**Impossibility one-liner:** *different base rates ⇒ pick your fairness — you can't have parity of errors and honesty of scores at once.*

**COMPAS anchor:** ProPublica argued error rates; the vendor argued calibration; math says both sides could be "right."

The 5 facts to retain:

1. Group fairness compares across groups; individual fairness demands similar treatment of similar people — and "similar" is the hard part.
2. Demographic parity = equal positive rates; equalized odds = equal error rates; calibration = equal score meaning.
3. With differing base rates, these metrics cannot all hold simultaneously (Kleinberg et al.; Chouldechova) — the conflict is mathematical.
4. Therefore metric choice is a documented policy/values decision owned by governance, contextualized by which errors hurt most (punitive → FP balance; allocative → FN balance).
5. Proxies defeat attribute-deletion, and auditing fairness requires demographic data that privacy law complicates collecting — the measurement paradox.

## SELF-CHECK

1. Distinguish group from individual fairness and give the standard critique of each.
2. Match to metric: (a) "equal hire *rates* by gender," (b) "equal *false alarm* rates by race," (c) "a risk score of 3 means the same everywhere."
3. State the impossibility result in one sentence, including its precondition.
4. Why is fairness-metric selection a governance decision rather than an engineering default, and what should the decision record contain?
5. In COMPAS, which fairness definition did each side rely on?

<details>
<summary>Answers</summary>

1. Group: compare outcomes/errors across demographic groups — auditable but blind to individuals. Individual: treat similar people similarly — principled but requires defining "similar," which reintroduces the original problem.
2. (a) demographic parity; (b) equalized odds (false-positive balance); (c) calibration.
3. When outcome base rates differ across groups, no non-trivial predictor can simultaneously satisfy calibration and equal false-positive and false-negative rates.
4. Because it allocates *which group bears which kind of error* — a values/legal judgment; the record should state the context, the chosen metric(s), rejected alternatives, the rationale (which harm is worst here), and who approved it.
5. ProPublica: equalized odds (unequal false-positive/false-negative rates); Northpointe: calibration (equal score meaning across races).

</details>
