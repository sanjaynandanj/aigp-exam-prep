# Domain I Vocabulary Drill: The 40 Terms That Show Up in Stems

**Phase 1 · Lesson 10 · ~0.75h · BoK Domain I**

## EXAM FOCUS

Domain I recall, concentrated. Exam stems use these terms *without defining them*, and distractors are built from the confusable neighbor of each term. Drill method: cover the middle column, produce each definition aloud, and pay special attention to column three — it names the exact confusion the exam will offer you. Misses go into the question journal (+2/+7).

## CORE

### The 40 terms

| # | Term | One-line definition | Trap / tested confusion |
|---|---|---|---|
| 1 | **Ground truth** | The accepted correct answers used to train/evaluate a model | Often just recorded human judgment — "truth" can carry label bias |
| 2 | **Feature** | An input variable the model uses | vs label (the output); deep nets also *learn* internal features |
| 3 | **Label** | The known outcome attached to a training example | vs feature; only supervised learning requires labels |
| 4 | **Training** | The phase where the model learns weights from data | vs inference; training risks ≠ inference risks |
| 5 | **Inference** | Running the trained model on new inputs to get outputs | Also OECD-definition verb ("infers") — different sense, same word |
| 6 | **Parameters / weights** | Numbers learned during training that constitute the model | vs hyperparameters (human-set, e.g., learning rate, layer count) |
| 7 | **Hyperparameter** | A configuration choice made before training | Not learned from data — the reverse of parameters |
| 8 | **Epoch** | One complete pass through the training dataset | vs iteration/batch (smaller steps); more epochs ≠ always better (overfitting) |
| 9 | **Loss function** | The formal measure of error training tries to minimize | The optimized metric may diverge from the *intended* goal (reward misspecification) |
| 10 | **Overfitting** | Memorizing training data's noise; poor generalization | vs underfitting (too simple to learn the pattern at all) |
| 11 | **Underfitting** | Model too simple; poor even on training data | vs overfitting — symptoms differ on training data |
| 12 | **Generalization** | Performing well on unseen data | The point of ML; measured on held-out data, never training data |
| 13 | **Held-out / test set** | Data withheld from training, used for honest evaluation | Vendor accuracy "on training data" is near-meaningless |
| 14 | **Classification** | Predicting a category | vs regression (a number) vs clustering (no labels at all) |
| 15 | **Regression** | Predicting a continuous number | Not the statistics-only sense; still supervised learning |
| 16 | **Clustering** | Discovering groups in unlabeled data | Unsupervised — no ground truth to test "accuracy" against |
| 17 | **Supervised learning** | Learning from labeled examples | Key off labels; signature risk = label/historical bias |
| 18 | **Unsupervised learning** | Finding structure in unlabeled data | Signature risk = human misinterpretation, proxy clusters |
| 19 | **Reinforcement learning** | Learning by acting and receiving rewards | Signature risk = reward hacking; also the RL in RLHF |
| 20 | **Semi-supervised learning** | Small labeled set + large unlabeled set | Check selection bias in which cases got labeled |
| 21 | **Neural network** | Layered units connected by learned weights | Depth (many layers) = deep learning = opacity |
| 22 | **Deep learning** | ML with many-layered neural networks | Subset of ML, which is a subset of AI — nesting is tested |
| 23 | **Transfer learning** | Reusing a model trained on one task as the start for another | Basis of foundation-model economics; inherited flaws transfer too |
| 24 | **Fine-tuning** | Further training a pretrained model on targeted data | vs pretraining (broad, expensive) and vs RAG (no weight changes) |
| 25 | **Pretraining** | Broad self-supervised training creating a base model | Where web-scale data (copyright, privacy) enters |
| 26 | **RLHF** | Aligning a model via human preference rankings | Shapes tendencies, not guarantees; contains RL, not supervised labels |
| 27 | **Foundation model** | Large pretrained model adaptable to many tasks | Legal cousin: "GPAI model" (EU AI Act) — know both names |
| 28 | **LLM** | Foundation model for text; next-token prediction at scale | Optimizes plausibility, not truth → hallucination is intrinsic |
| 29 | **Token** | The text fragment unit an LLM reads/writes | Not a word; context windows and costs are counted in tokens |
| 30 | **Embedding** | A numeric vector representing meaning/similarity of data | Enables semantic search/RAG; can still encode personal data and bias |
| 31 | **Prompt** | The input instruction/context given to a genAI model | Attack surface too (prompt injection); may contain personal data |
| 32 | **Temperature** | Setting controlling output randomness | Same prompt, different answers — breaks naive testing/reproducibility |
| 33 | **Context window** | How much text a model can consider at once | Model doesn't "remember" beyond it; not the same as training data |
| 34 | **RAG** | Retrieving trusted documents at query time to ground answers | Alternative to fine-tuning; shifts risk to the retrieval store |
| 35 | **Hallucination** | Fluent, confident, false generated content | Intrinsic to LLMs, reducible not eliminable; not "lying" (no intent) |
| 36 | **Model / data / concept drift** | Post-deployment degradation: performance / inputs / input-outcome relationship change | Data drift = questions changed; concept drift = answers changed |
| 37 | **Black box** | Output can't be traced to human-readable reasons | Technical opacity vs proprietary opacity — different remedies |
| 38 | **Explainability** | Ability to give reasons for a specific output | vs transparency (openness about the system) vs interpretability (understandable by design) — Phase 2 L04 |
| 39 | **Automation bias** | Humans over-trusting automated outputs | Defeats nominal human review — the oversight-design failure |
| 40 | **Proxy (variable)** | A feature correlated with something else — often a protected attribute or the true target | Why removing protected attributes doesn't remove bias; why cost ≠ need (Obermeyer) |

### The seven highest-value contrasts

If drilling time is short, these pairs generate the most distractors:

| Contrast | The one-line separator |
|---|---|
| Parameter vs hyperparameter | Learned by the machine vs chosen by the human |
| Training vs inference | Building the model vs using it |
| Overfitting vs underfitting | Memorized the noise vs never learned the pattern |
| Classification vs regression vs clustering | Category vs number vs discovered groups (no labels) |
| Fine-tuning vs RAG | Change the weights vs look it up at query time |
| Transparency vs explainability vs interpretability | Open about the system vs reasons for an output vs understandable by design |
| Data drift vs concept drift | Inputs changed vs input→outcome relationship changed |

## CASES & EXAMPLES

1. **Stem dissection.** "A deployer notices the *distribution of incoming applications* has shifted since training." — the phrase "distribution of inputs" pins **data drift**; "concept drift" is the planted distractor and is wrong because nothing says the input→outcome relationship changed.
2. **Stem dissection.** "To adapt the model, the team continues training it on 2,000 company documents." — *continues training* = **fine-tuning** (weights change). Had they "connected it to a document search index consulted at question time," it would be **RAG**.
3. **Stem dissection.** "The vendor reports 99.4% accuracy achieved during model development on the data used to build the model." — the trap phrase is *on the data used to build the model*: this signals no **held-out** evaluation and likely **overfitting**-inflated numbers.

## MEMORY HOOKS

**Drill protocol:** three passes. Pass 1: cover definitions, produce them. Pass 2: cover terms, produce them from definitions. Pass 3: read only the trap column and name both confused terms. Journal every miss (+2/+7).

The 5 facts to retain (meta-level):

1. Parameters learned / hyperparameters chosen — the single most-planted distractor pair.
2. Labels exist only in supervised learning; clustering has no accuracy in the ground-truth sense.
3. Fine-tuning changes weights; RAG changes nothing but retrieves — different privacy and control profiles.
4. Drift trio: data (inputs), concept (relationship), model (the resulting decay).
5. "Proxy" is the word that explains why deleting protected attributes never de-biases a model.

## SELF-CHECK

1. Define: ground truth, embedding, token, temperature — one line each, no peeking.
2. Which learning paradigm has no labels, and what does that imply for fairness testing?
3. A team wants a chatbot to answer from current internal policies without training on them. Which technique, and why is it the privacy-preferred option here?
4. What's the difference between an epoch and a hyperparameter?
5. Name the three "-ability/-ency" terms that Phase 2 Lesson 04 will separate, with a two-word cue for each.

<details>
<summary>Answers</summary>

1. Ground truth: the accepted correct answers for training/evaluation. Embedding: a numeric vector capturing meaning/similarity. Token: the fragment unit of LLM text. Temperature: the randomness setting for generation.
2. Unsupervised learning; without ground truth there's no outcome to compare across groups, so fairness assessment must examine what clusters proxy for and how humans use them.
3. RAG — documents are retrieved at query time, not absorbed into weights, so information stays governed in its source store (access control, updating, deletion remain possible).
4. An epoch is a unit of training progress (one full data pass); a hyperparameter is a pre-training configuration choice — the *number* of epochs is itself a hyperparameter.
5. Transparency ("system openness"), explainability ("output reasons"), interpretability ("by design").

</details>
