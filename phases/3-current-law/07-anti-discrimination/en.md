# Anti-Discrimination Law: Disparate Treatment vs Disparate Impact in AI

**Phase 3 · Lesson 07 · ~1h · BoK Domain II**

## EXAM FOCUS

Anti-discrimination doctrine is the legal engine behind "AI bias" questions. You must cleanly distinguish **disparate treatment** (intent/explicit use of a protected trait) from **disparate impact** (neutral practice, discriminatory effect), apply the **four-fifths rule** arithmetic, spot **proxy discrimination**, and know which statutes protect which classes in **employment, credit, and housing**. Scenario stems often hide the doctrine inside a data-science fact pattern — your job is to translate.

## CORE

### The two theories

| | **Disparate treatment** | **Disparate impact (adverse impact)** |
|---|---|---|
| Essence | Treating people differently **because of** a protected characteristic | A **facially neutral** practice that disproportionately harms a protected group |
| Intent required? | Yes (or explicit classification) | **No** — effect suffices |
| AI form | Model explicitly uses race/sex/age as a feature; rules coded to exclude (e.g., auto-rejecting applicants above an age) | Model trained on biased history produces skewed outcomes; neutral features act as proxies |
| Defense structure | Almost none for explicit use (narrow BFOQ in employment) | Burden-shifting: plaintiff shows statistical disparity → defendant shows **job-relatedness & business necessity** (employment) or legitimate interest (housing/credit) → plaintiff shows a **less discriminatory alternative** existed |
| Exam cue words | "because of," "screened out women," "used age as an input" | "neutral criterion," "selection rate," "statistically correlated" |

The three-step disparate-impact burden shift matters for AI: the "less discriminatory alternative" step maps directly onto **algorithmic debiasing** — if a fairer model with comparable performance exists, insisting on the biased one loses.

### The four-fifths (80%) rule

From the EEOC's Uniform Guidelines on Employee Selection Procedures — a **rule of thumb, not a legal ceiling**:

> Selection rate of a protected group ÷ selection rate of the highest-scoring group < **0.80** → evidence of adverse impact.

Worked example: tool selects 30% of men (60/200) and 15% of women (30/200) → impact ratio = 15/30 = **0.50** < 0.80 → adverse impact indicated.

Caveats the exam tests: small samples make the ratio unreliable; statistical-significance testing is the more rigorous method; passing 4/5ths does **not** immunize a tool; failing it does not automatically equal liability — it triggers the justification analysis. NYC LL 144 operationalizes exactly these **impact ratios** in its bias audits.

### Proxy discrimination

A model never fed "race" can still discriminate through **correlated features**:

| Proxy | Correlates with |
|---|---|
| ZIP code / geolocation | Race, national origin (residential segregation → digital redlining) |
| Name, language patterns | Ethnicity, national origin |
| Shopping patterns, social graph | Sex, religion, health status |
| Gaps in employment history | Pregnancy/caregiving (sex), disability |
| Device type, typing cadence | Age, disability, income |

Removing the protected attribute ("fairness through unawareness") is **not** a defense and can make bias harder to detect. Word-embedding and historical-data bias mean models *learn* societal discrimination unless actively countered.

### Protected classes by domain

| Domain | Statute(s) | Protected classes |
|---|---|---|
| **Employment** | Title VII; ADEA; ADA; state laws add more | Race, color, religion, sex (incl. pregnancy, orientation/identity per *Bostock*), national origin; age 40+; disability |
| **Credit** | ECOA (Reg B); FCRA (process rights) | Race, color, religion, national origin, sex, marital status, age, public-assistance income, exercise of consumer rights |
| **Housing** | Fair Housing Act | Race, color, religion, sex, national origin, familial status, disability |
| **EU counterpart** | Equality directives + Charter | Broad grounds; note the CJEU has treated indirect discrimination analysis similarly to disparate impact |

Note the mismatch traps: age is protected in credit (ECOA) with special rules but only 40+ in employment (ADEA); familial status is housing-specific; marital status is credit-specific.

### AI-specific application points

- **Employment:** EEOC guidance confirms employers own the adverse impact of vendor tools; validation under the Uniform Guidelines (content/criterion/construct validity) is the business-necessity evidence.
- **Housing:** HUD has applied disparate impact to algorithmic tenant screening and ad-targeting; DOJ settled with a major platform requiring it to rebuild its ad-delivery system (the "variance reduction" remedy) — algorithmic ad delivery can discriminate even when advertisers target neutrally.
- **Credit:** regulators expect **fair-lending testing** of models (including searching for less discriminatory alternatives); adverse-action specificity (Lesson 04) is the companion duty.

## CASES & EXAMPLES

**Scenario 1 — The historical mirror.** A recruiter tool trained on ten years of hires at a male-dominated firm downgrades resumes containing the word "women's" (as a famous withdrawn internal tool reportedly did). *Analysis:* No intent needed — this is **disparate impact** from biased training data (and arguably treatment if the gendered token is effectively an explicit sex signal). Remedy path: measure selection rates, validate job-relatedness, adopt less discriminatory alternatives, or scrap.

**Scenario 2 — Four-fifths arithmetic.** An AEDT advances 40% of white applicants and 28% of Black applicants. *Analysis:* 28/40 = 0.70 < 0.80 → adverse-impact indicator; employer must be ready to show validity/business necessity and to consider alternatives; in NYC this shows up in the published audit.

**Scenario 3 — The ZIP-code lender.** A credit model excludes race but weights ZIP code, mobile-device type, and shopping categories; denial rates for Hispanic applicants are double. *Analysis:* **Proxy discrimination / digital redlining** under ECOA disparate-impact analysis; "we don't collect race" is not a defense (regulators estimate race via proxy methods like BISG to test for exactly this).

**Scenario 4 — Intent in the code.** A tutoring firm's application software auto-rejects women 55+ and men 60+. *Analysis:* Explicit age/sex rules = **disparate treatment** — the theory requiring intent or explicit classification; this mirrors the EEOC's first AI settlement. No validity defense can save an explicit classification.

## MEMORY HOOKS

- **Treatment vs impact in four words:** *treatment = bad input* (protected trait used); *impact = bad output* (neutral input, skewed result).
- **Burden-shift dance (impact claims):** *Disparity → Justify → Alternative* ("D-J-A").
- **Four-fifths one-liner:** *divide the lower selection rate by the higher; below 0.8 = red flag, not verdict.*
- **Proxy mantra:** *deleting the column doesn't delete the correlation.*
- **Class-coverage traps:** marital status → credit only; familial status → housing only; age → credit (all ages) vs employment (40+).

**The 5 facts to retain:**
1. Disparate treatment requires intent/explicit classification; disparate impact requires only discriminatory effect from a neutral practice.
2. The four-fifths rule (selection-rate ratio < 0.80) is an evidentiary *rule of thumb* that triggers — not concludes — the analysis.
3. In impact litigation, defendants must show job-relatedness/business necessity, and lose if a **less discriminatory alternative** with comparable utility exists.
4. Proxy discrimination defeats "fairness through unawareness" — ZIP codes, names, and behavior patterns encode protected traits.
5. Employment (Title VII/ADEA/ADA), credit (ECOA), and housing (FHA) each have distinct protected-class lists — match the list to the domain.

## SELF-CHECK

1. **Q:** A model's selection rates are 50% (group A) and 35% (group B). Apply the four-fifths rule.
   **A:** 35/50 = 0.70 < 0.80 → evidence of adverse impact; the deployer must investigate and be prepared to justify validity/business necessity and consider less discriminatory alternatives.

2. **Q:** Why isn't removing protected attributes from the feature set a sufficient fairness control?
   **A:** Correlated proxies (geography, names, behavioral data) let the model reconstruct the protected trait — proxy discrimination — while removal also blinds the organization to measuring the bias.

3. **Q:** In a Title VII disparate-impact case over an AI screener, what must the employer prove once disparity is shown, and how can the plaintiff still win?
   **A:** That the tool is job-related and consistent with business necessity (validation evidence); plaintiff prevails by showing an equally effective, less discriminatory alternative was available and refused.

4. **Q:** Which statute protects marital status and public-assistance income, and in what sector?
   **A:** ECOA — consumer credit.

5. **Q:** Classify: (a) a model that includes gender as a pricing feature; (b) a model using only "years since first job" that disadvantages older applicants.
   **A:** (a) disparate treatment (explicit protected-trait use); (b) potential disparate impact via an age proxy — neutral on its face, discriminatory in effect.
