# Data Governance for AI: Provenance, Quality, Labeling, Minimization

**Phase 5 · Lesson 03 · ~1.5h · BoK Domain III**

## EXAM FOCUS

"Garbage in, garbage out" is the most-tested idea in Domain III. Expect questions on: data quality dimensions, provenance/lineage, labeling quality (including the inter-annotator agreement concept), representativeness vs bias, applying minimization and consent/licensing rules to training data, and retention. Scenario stems often describe a biased or unlawful dataset and ask which governance control failed.

## CORE

### Provenance and lineage

| Term | Meaning | Governance use |
|---|---|---|
| **Provenance** | Where the data originated (source, collector, legal basis, license) | Answers "may we use this?" — lawfulness, consent, licensing |
| **Lineage** | The documented path of transformations from source to training set | Answers "what happened to it?" — reproducibility, debugging, audit |

Every training dataset should carry a record of: source(s), collection method, legal basis/license, transformations applied, versions, and who approved its use. This record feeds datasheets (Lesson 07) and audit evidence (Phase 6, Lesson 08).

### Data quality dimensions

The classic dimensions, adapted for AI:

| Dimension | Question | AI failure if absent |
|---|---|---|
| Accuracy | Are values correct? | Model learns errors as patterns |
| Completeness | Are records/fields missing? | Systematic gaps → blind spots |
| Consistency | Same meaning across sources? | Spurious correlations |
| Timeliness / currency | Is it up to date? | Model trained on a world that no longer exists |
| Validity | Does it conform to expected formats/ranges? | Silent corruption |
| **Representativeness** | Does it reflect the population the system will serve? | Subgroup underperformance → unfair outcomes |

Representativeness deserves special attention: a dataset can be accurate, complete, and consistent yet still unrepresentative (e.g., a dermatology dataset dominated by light skin tones). The EU AI Act's high-risk data-governance concept requires training/validation/testing data to be relevant, sufficiently representative, and to the best extent possible free of errors and complete *for the intended purpose*.

### Labeling and annotation QA

Supervised learning inherits every labeling flaw. Controls:

- **Clear annotation guidelines** with edge-case examples, versioned like code.
- **Inter-annotator agreement (IAA):** have multiple annotators label the same samples and measure agreement (concept level: statistics such as Cohen's kappa). Low agreement means the task definition is ambiguous or annotators need retraining — the labels are not trustworthy ground truth.
- **Gold-standard sets and spot audits:** seed known-answer items; review samples of production labels.
- **Annotator workforce governance:** training, fair working conditions, and awareness that annotators' own backgrounds can encode bias into labels.

### Minimization, consent, and licensing of training data

Data-protection principles do not stop applying because the purpose is "training":

| Principle | Applied to training data |
|---|---|
| **Minimization** | Collect/retain only what the purpose needs; prefer de-identified, aggregated, or synthetic data where it preserves utility |
| **Purpose limitation** | Data collected for service delivery is not automatically reusable for training — compatibility analysis or a new legal basis is needed |
| **Lawful basis / consent** | Scraped or repurposed personal data still needs a lawful basis (in GDPR contexts, often contested legitimate-interest analyses — verify current status of regulator guidance) |
| **Licensing / IP** | Copyrighted works in training corpora require license, exception, or acceptance of legal risk; document license terms and any opt-outs honored |
| **Special categories** | Sensitive data (health, biometrics) triggers heightened conditions — including when used to *test for* bias |

### Retention

Retention rules pull in two directions: privacy law says delete when the purpose ends; accountability says keep enough to reproduce, audit, and defend the model. Resolution: define retention schedules per artifact — raw personal data (shortest), curated training sets and their documentation (kept for the model's life + accountability period), and evaluation data (kept to enable re-testing). Deleting training data does not delete what the model learned — a reason erasure requests against trained models are legally and technically hard (verify current status of regulator positions on model deletion/machine unlearning).

## CASES & EXAMPLES

**Scenario 1 — biased hiring data.** A recruiter trains a screening model on ten years of its own hiring decisions; the model downgrades women's résumés. This mirrors the widely reported Amazon experimental recruiting-tool case. *Failed control:* representativeness/bias analysis of historical labels — the "ground truth" encoded past discrimination. Best answer: assess and correct training-data representativeness and label bias, not "add more of the same data."

**Scenario 2 — repurposing without a basis.** A fintech wants to train a marketing model on transaction data collected solely to provide payment services, with no notice to customers. *Exam point:* purpose limitation — repurposing requires a compatibility assessment/new lawful basis and updated notices, before training begins.

**Scenario 3 — noisy labels.** Two annotation vendors label "toxic content" with 55% agreement. The team trains anyway; the moderation model behaves erratically. *Failed control:* inter-annotator agreement threshold and guideline refinement before training — low IAA signals the labels aren't reliable ground truth.

**Scenario 4 — scraped faces.** A startup scrapes social-media photos to build a face-recognition database sold to police. Regulators in several jurisdictions found this unlawful (the Clearview AI enforcement pattern). *Exam point:* provenance and lawful basis for scraped biometric data — "publicly available" does not mean "free to use."

## MEMORY HOOKS

**Quality mnemonic — "ACCTVR": Accuracy, Completeness, Consistency, Timeliness, Validity, Representativeness.**

**Provenance vs lineage:** *provenance = birth certificate; lineage = travel diary.*

**IAA one-liner:** *If humans can't agree on the label, the model can't learn the truth.*

The 5 facts to retain:

1. Provenance answers "may we use it" (source, basis, license); lineage answers "what was done to it" (transformations, versions).
2. Representativeness is the quality dimension most tied to fairness — data can be clean yet unrepresentative of the served population.
3. Inter-annotator agreement measures label reliability; low agreement means fix guidelines/training before using the labels.
4. Minimization and purpose limitation apply to training data; repurposing collected data for training needs a compatibility/basis analysis.
5. Retention must balance deletion duties against keeping training/eval artifacts for reproducibility and audit — schedule per artifact type.

## SELF-CHECK

1. **Distinguish data provenance from data lineage.**
   Provenance = origin: source, collection method, legal basis, license. Lineage = the documented chain of transformations from source to training set.
2. **Why is representativeness assessed against the *intended purpose*?**
   Because adequacy depends on the population and context the system will serve — a dataset representative for one deployment population may be unrepresentative for another.
3. **What does low inter-annotator agreement tell a governance reviewer?**
   The labeling task is ambiguous or annotators are inconsistent — the labels are unreliable ground truth; guidelines/training must be fixed before the data is used.
4. **A product team wants to reuse customer-support transcripts to fine-tune a model. What must happen first?**
   A purpose-compatibility/lawful-basis analysis (and updated notice or consent where required), plus minimization (e.g., redacting personal data) — before training.
5. **Why doesn't deleting a training dataset satisfy an erasure request aimed at a trained model?**
   The model's parameters may still encode information learned from that data; removing influence from a trained model is technically hard (machine unlearning) — verify current regulator status on this issue.
