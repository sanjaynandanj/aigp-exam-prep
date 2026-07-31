# Machine Learning Types: Supervised, Unsupervised, Reinforcement

**Phase 1 · Lesson 02 · ~1h · BoK Domain I**

## EXAM FOCUS

Domain I — understanding AI/ML technology. Almost pure **fact recall**: match a described system to its learning paradigm, or match a task (classification vs regression vs clustering) to its type. The classic trap: stems describe the *data situation* (labeled? unlabeled? reward signal?) and you must name the paradigm. Learn to key off the data, and you can't be fooled.

## CORE

### The three (and a half) paradigms

| Paradigm | Learns from | Human effort upfront | Canonical governance-relevant examples |
|---|---|---|---|
| **Supervised learning** | **Labeled** data — inputs paired with known correct outputs ("ground truth") | High: someone must label the data | Résumé screening (hire/no-hire labels), credit scoring (repaid/defaulted), medical image diagnosis (tumor/no tumor), spam filters |
| **Unsupervised learning** | **Unlabeled** data — the system finds structure on its own | Low labeling, high interpretation | Customer segmentation, anomaly detection in transactions (fraud/AML), grouping insurance claims, topic discovery in documents |
| **Reinforcement learning (RL)** | **Trial and error against a reward signal** — an agent acts in an environment and learns what maximizes reward | Designing the reward function | Robotics, game-playing systems, recommendation/ad-bidding optimization, RLHF for aligning chatbots (Lesson 05) |
| **Semi-supervised** (the half) | A *small* labeled set + a *large* unlabeled set | Medium | Fraud detection where only some cases were ever investigated and labeled |

Also worth one line each:

- **Self-supervised learning:** labels are generated from the data itself (e.g., "predict the next word") — how LLMs are pretrained. Technically a flavor of supervised learning with free labels.
- **Federated learning:** not a paradigm but a *training arrangement* — the model trains across decentralized data that never leaves its source (privacy relevance, Phase 2 Lesson 06).

### Task types within supervised learning

| Task | Output | Examples |
|---|---|---|
| **Classification** | A category (discrete) | Approve/deny; spam/not spam; which of 5 disease types |
| **Regression** | A number (continuous) | Predicted salary, house price, probability-like risk score, length of hospital stay |

And the flagship unsupervised task:

| Task | Output | Examples |
|---|---|---|
| **Clustering** | Groups discovered in the data (no predefined categories) | Market segments, "customers like this one," grouping incident reports |

Recall test: *classification and regression need labels (supervised); clustering doesn't (unsupervised).*

### Why the paradigm matters for governance

| Paradigm | Signature governance risks |
|---|---|
| Supervised | **Label bias** — the model inherits whatever is wrong with the labels. Historical hiring data encodes historical hiring discrimination. "Ground truth" is often just "recorded human judgment." |
| Unsupervised | **Interpretation risk** — clusters have no inherent meaning; humans name them, and can name them in discriminatory or spurious ways (e.g., a cluster that is effectively a proxy for ethnicity). Harder to test for fairness because there's no "correct answer" to compare against. |
| Reinforcement | **Reward misspecification / reward hacking** — the agent optimizes exactly what you measured, not what you meant (engagement-maximizing recommenders amplifying outrage is the canonical example). Behavior can also keep changing in production. |
| Semi-supervised | **Selection bias in the labeled slice** — if only investigated fraud cases got labels, the model learns "what investigators looked at," not "what fraud is." |

## CASES & EXAMPLES

1. **Amazon's experimental recruiting tool (reported 2018).** A supervised model trained on ~10 years of résumés — predominantly from men — learned to penalize signals associated with women (e.g., the word "women's" in activities) and was abandoned. Exam-ready takeaways: supervised learning + biased labels/history = biased predictions; removing the protected attribute doesn't help when **proxies** remain.

2. **Transaction anomaly detection at a bank.** Unsupervised clustering flags "unusual" transactions for AML review. Governance question: unusual *relative to whom*? If the customer base used to fit the model skews one way, normal behavior for a minority group can be systematically flagged as anomalous — disparate impact without any labels ever existing.

3. **The engagement recommender.** A streaming platform uses RL-style optimization to maximize watch time. It learns that escalating, sensational content keeps users watching. Nobody programmed "recommend extreme content" — the reward function *implied* it. Governance lesson: in RL, the reward function is the policy decision; review it like one.

4. **Paradigm-identification stem (exam style).** "A hospital system learns to group patients with similar readmission patterns without any predefined outcome variable." No labels, finding structure → unsupervised learning, clustering. If the stem had said "trained on records labeled with whether the patient was readmitted within 30 days" → supervised classification.

## MEMORY HOOKS

**Key off the data:**
- Labels present → **supervised** ("a teacher marked the homework").
- No labels → **unsupervised** ("find your own patterns").
- Reward signal + actions in an environment → **reinforcement** ("training a dog with treats").
- Few labels, many unlabeled → **semi-supervised**.

**Task triple:** *Classify a category, regress a number, cluster the unlabeled.*

The 5 facts to retain:

1. Supervised = labeled data; its signature risk is inherited label/historical bias.
2. Unsupervised = structure in unlabeled data; its signature risk is human (mis)interpretation of clusters and proxy discrimination.
3. Reinforcement = reward-driven trial and error; its signature risk is reward misspecification ("you get what you measure").
4. Classification → categories; regression → continuous numbers; clustering → discovered groups.
5. LLM pretraining is self-supervised (next-token prediction); RLHF adds a reinforcement-learning alignment step.

## SELF-CHECK

1. A model is trained on loan files labeled "defaulted / repaid." Paradigm and task type?
2. What is the characteristic governance failure of reinforcement learning, and what real-world system illustrates it?
3. Why is fairness testing structurally harder for unsupervised systems?
4. Which paradigm does semi-supervised learning blend, and what bias should you check for?
5. In one sentence: what did the Amazon recruiting tool case demonstrate about supervised learning?

<details>
<summary>Answers</summary>

1. Supervised learning; classification (binary).
2. Reward misspecification/hacking — the system optimizes the literal metric, not the intent; e.g., engagement-maximizing recommenders promoting sensational content.
3. There's no ground truth to compare outcomes against, and clusters acquire meaning only through human interpretation — bias can enter both in what the clusters proxy for and in how they're labeled and used.
4. A small labeled set with supervised methods plus a large unlabeled set; check selection bias in *which* cases got labeled.
5. A supervised model faithfully reproduces the biases embedded in its historical training labels — and finds proxies even when protected attributes are removed.

</details>
