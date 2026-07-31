# Generative AI: LLMs, Foundation Models, Fine-Tuning, RAG

**Phase 1 · Lesson 05 · ~1.5h · BoK Domain I**

## EXAM FOCUS

Domain I — generative AI concepts, tested at **definition level** (pretraining vs fine-tuning vs RLHF; foundation model vs application; RAG) plus one recurring **scenario theme**: why general-purpose models strain governance frameworks built for single-purpose systems. This lesson also pre-loads Phase 4's GPAI (general-purpose AI) obligations under the EU AI Act — learn the vocabulary now, attach the law later.

## CORE

### Definitions that nest

| Term | Definition | Relationship |
|---|---|---|
| **Generative AI** | AI whose output is *content* — text, images, audio, video, code | The umbrella capability |
| **Foundation model** | A large model pretrained on broad data, adaptable to many downstream tasks | The reusable base layer |
| **LLM (large language model)** | A foundation model for text: predicts the next token, scaled to billions of parameters | The dominant foundation-model type |
| **GPAI model** (EU AI Act term) | A model displaying significant generality, capable of performing a wide range of distinct tasks | The *legal* label roughly covering foundation models — Phase 4 |

### The build pipeline, concept level

1. **Pretraining.** Train on vast, broad corpora (web text, code, books) with a self-supervised objective — for LLMs, *predict the next token*. Output: a base model with broad capability but no manners. This step costs the most compute and ingests the most (copyright- and privacy-entangled) data.
2. **Fine-tuning.** Continue training on a smaller, targeted dataset to specialize behavior — a domain (legal, medical), a format (instruction following), or a company's tone. Cheap relative to pretraining; this is where *downstream* actors most often modify models.
3. **RLHF (reinforcement learning from human feedback).** Humans rank candidate outputs; a reward model learns those preferences; the model is tuned to produce answers humans rate highly — more helpful, less toxic. This is alignment-by-preference, not a guarantee: it shapes tendencies, it doesn't install rules.
4. **System assembly.** The model is wrapped with system prompts, safety filters, tools, and interfaces into a product (a chatbot, a copilot).

### Concepts that ride along

| Concept | One-liner | Governance relevance |
|---|---|---|
| **Token** | The unit of text a model reads/writes (word fragments) | Context limits, cost, logging granularity |
| **Prompt** | The input instruction/context | Prompts can contain personal data and can *attack* the model (prompt injection — Phase 5) |
| **System prompt** | Hidden standing instructions from the deployer | A control surface — and a leakage risk |
| **Temperature** | A setting controlling output randomness (higher = more varied) | Same prompt ≠ same answer; complicates testing and reproducibility |
| **Context window** | How much text the model can consider at once | Limits on what it can "know" per interaction |
| **RAG (retrieval-augmented generation)** | Retrieve relevant documents from a trusted store at query time, then have the model answer *grounded in them* | The standard mitigation for hallucination and stale knowledge; shifts governance toward the *document store* (access control, accuracy, provenance) |

RAG deserves emphasis: rather than retraining a model to know your policies, you retrieve the right policy text and let the model summarize it. Benefits: current information, citable sources, no training on your sensitive corpus. New risks: retrieval of the *wrong* or *unauthorized* document, and confident synthesis from bad sources.

### Why generative AI strains classic governance

Classic AI governance assumed: one model, one purpose, one deployer, testable against a defined task. GenAI breaks each assumption:

| Classic assumption | GenAI reality | Governance consequence |
|---|---|---|
| Defined purpose | **General-purpose**: the same model writes poems and phishing emails | Can't risk-classify the *model* by use case alone; the EU AI Act invented a separate GPAI track for exactly this reason |
| Enumerable failure modes | **Emergent, open-ended outputs**; hallucination is intrinsic, not a bug to patch | Testing can't be exhaustive; continuous evaluation + red teaming (Phase 5) |
| One accountable builder | **Value chain**: pretrainer → fine-tuner → app builder → deployer | Obligation-splitting problems: who assessed what? (provider vs deployer, Phases 4–5) |
| Stable behavior | Stochastic outputs (temperature), model updates upstream | Reproducibility and change-management challenges |
| Curated training data | Web-scale scraping | Copyright disputes, personal data in corpora, memorization/leakage (Phase 2 Lesson 06, Phase 3 Lesson 06) |
| Users understand outputs | Fluent, authoritative-sounding text | Automation bias supercharged; disclosure duties (deepfake/AI-content labeling) |

## CASES & EXAMPLES

1. **The hallucinated case citations.** In a widely reported 2023 US matter (*Mata v. Avianca*), lawyers submitted a brief containing nonexistent judicial opinions generated by a chatbot and were sanctioned. Exam takeaways: hallucination = fluent fabrication; professional accountability stays with the human; "the AI said so" is not due diligence.

2. **The customer-service bot that made policy.** A tribunal ordered an airline (Air Canada, 2024, Canada) to honor a bereavement-fare policy its website chatbot had invented, rejecting the argument that the chatbot was responsible for its own statements. Takeaway: deployers own their genAI's outputs to customers — a Domain IV favorite.

3. **RAG done right vs wrong.** An insurer builds an internal policy assistant. *Right:* RAG over the approved policy repository, answers cite documents, access controls mirror the source system. *Wrong:* fine-tune a model on every historical email — now sensitive data may be memorized in weights, uncontrollable and effectively unerasable. Choosing RAG vs fine-tuning is a *data-governance* decision, not just an engineering one.

4. **One model, two risk classes.** A foundation-model API powers (a) a recipe suggester and (b) a résumé screener at two customer companies. Same model — trivial risk vs regulated employment decision. Demonstrates why model-level governance (GPAI duties) and use-level governance (high-risk duties) had to be separated.

## MEMORY HOOKS

**Pipeline mnemonic — "P-F-R-A":** **P**retrain (broad data, next-token) → **F**ine-tune (specialize) → **R**LHF (align to human preference) → **A**ssemble (prompts, filters, product).

**RAG in five words:** *look it up, then answer.*

**Strain mnemonic — "GEMS":** **G**eneral-purpose, **E**mergent uses, **M**any hands (value chain), **S**tochastic outputs — the four reasons classic governance creaks.

The 5 facts to retain:

1. Foundation models are pretrained broadly and adapted downstream; "GPAI model" is the EU AI Act's legal cousin of this concept.
2. Pretraining = self-supervised next-token prediction at scale; fine-tuning specializes; RLHF aligns outputs to human preferences (tendencies, not guarantees).
3. RAG grounds answers in retrieved trusted documents — the standard hallucination/staleness mitigation, shifting governance to the document store.
4. Hallucination is intrinsic to how LLMs generate text; deployers remain accountable for outputs (Air Canada chatbot; sanctioned lawyers).
5. GenAI strains classic governance because purpose, failure modes, accountability, and behavior are all no longer fixed — hence separate model-level and use-level regulatory tracks.

## SELF-CHECK

1. Order and describe the four stages from raw corpus to deployed chatbot.
2. What problem does RAG mitigate, and what new governance surface does it create?
3. Why can't a general-purpose model be risk-classified the way a single-purpose system is?
4. What does temperature control, and why does it matter for testing?
5. Name the two real cases in this lesson and the one-line lesson of each.

<details>
<summary>Answers</summary>

1. Pretraining (broad self-supervised learning → base capability); fine-tuning (targeted data → specialization); RLHF (human preference ranking → aligned behavior); assembly (system prompts, filters, tools → product).
2. Hallucination and stale knowledge; it moves risk to the retrieval store — document accuracy, provenance, and access control now determine answer quality and confidentiality.
3. Its risk depends on downstream use, which the model provider neither chooses nor fully foresees — so law splits duties: model-level (GPAI) obligations plus use-level (e.g., high-risk) obligations on deployers/system providers.
4. Output randomness; higher temperature means the same prompt yields different answers, undermining reproducibility and making single-run testing insufficient.
5. *Mata v. Avianca* — hallucinated citations; human professional accountability survives AI assistance. Air Canada chatbot — the deploying company is bound by what its bot tells customers.

</details>
