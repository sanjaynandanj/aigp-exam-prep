# Neural Networks & Deep Learning, Explained for Governance People

**Phase 1 · Lesson 03 · ~1h · BoK Domain I**

## EXAM FOCUS

Domain I — the technology layer. Tested at **intuition level, no math**: what layers/weights/training mean, why deep models are opaque, and where deep learning is (and isn't) the right tool. The dependable exam link: *depth → opacity → explainability and oversight obligations get harder* — that chain reappears in Domains III and IV scenarios.

## CORE

### The core idea in three sentences

A **neural network** is a stack of simple numeric units ("neurons") organized in **layers**: an input layer (the data goes in), one or more **hidden layers** (intermediate transformations), and an output layer (the prediction comes out). Each connection between units has a **weight** — a number expressing how strongly one unit's signal influences the next — and these weights *are* the model: everything it "knows" is stored in them. **Deep learning** simply means many hidden layers (deep = many), which lets the network learn layered, increasingly abstract representations.

### Training, at intuition level

1. **Forward pass:** feed an example in; the network produces a guess.
2. **Compare:** measure how wrong the guess was against the label (the *loss*).
3. **Adjust:** nudge every weight slightly in the direction that would have reduced the error (this is what *backpropagation* and *gradient descent* do — names are enough for the exam).
4. **Repeat** across millions of examples, many passes (**epochs**), until performance stops improving.

Analogy that holds up: turning millions of tiny dials, a hair at a time, until the machine's guesses stop being embarrassing. No dial has a human-readable meaning; competence is smeared across all of them.

### Key vocabulary (these appear in exam stems)

| Term | One-liner |
|---|---|
| **Parameters / weights** | The learned numbers inside the model; modern LLMs have billions |
| **Hyperparameters** | Settings humans choose *before* training (learning rate, number of layers) — not learned |
| **Layers** | Stages of transformation; "hidden" = between input and output |
| **Epoch** | One full pass through the training dataset |
| **Loss function** | The formal measure of "how wrong" that training minimizes |
| **Features** | The input variables the model consumes; deep nets *learn* their own internal features |

### Why depth produces opacity

| Cause | Effect |
|---|---|
| Knowledge is stored as millions–billions of weights | No single weight or rule to point at; nothing resembling "the reason" |
| Internal features are learned, not designed | Middle layers detect patterns no human named or intended |
| Non-linear interactions across layers | You cannot trace an output back through the stack by inspection |
| Scale | Even full access to all weights doesn't yield understanding |

This is the **black-box problem** (revisited in Lesson 07): the system can be inspected completely and understood barely. Consequences for governance: explainability requires *dedicated post-hoc techniques* (Phase 2 Lesson 04), oversight humans can't simply "check the logic," and documentation duties (model cards, logging) become the substitute for readable code.

Contrast class: **inherently interpretable models** — small decision trees, linear scoring rules — where you *can* read the logic. A recurring real-world governance decision: accept a possibly-small accuracy gain from deep learning, or keep an interpretable model where explanation duties are strict (credit, employment)?

### Where deep learning is used — and why there

Deep learning dominates wherever inputs are **unstructured** — images, audio, natural language, video — because it learns its own features instead of needing humans to hand-craft them:

| Domain | Example uses |
|---|---|
| Vision | Medical imaging, face recognition, autonomous-vehicle perception, defect inspection |
| Language | Translation, chatbots/LLMs, document summarization, content moderation |
| Speech | Transcription, voice assistants, speaker identification |
| Structured/tabular data | Often *not* the winner — simpler models (gradient-boosted trees, logistic regression) frequently match it and stay far more explainable |

Governance implication of that last row: if a vendor pitches a deep neural network for a tabular credit-scoring problem, "why not an interpretable model?" is a legitimate governance challenge, not a technical nitpick.

## CASES & EXAMPLES

1. **The dermatology classifier's shortcut.** A deep model for skin-lesion photos performs suspiciously well — investigation-style audits of such systems have found models keying on artifacts like rulers or markings present in malignant-lesion photos rather than the lesion itself. Layered learned features found a *correlate*, not the pathology. Governance lesson: opacity hides shortcut learning; validation must test *what* the model uses, not just accuracy.

2. **Credit denial and the explanation duty.** A lender deploys a deep model; a rejected applicant demands reasons (adverse-action style obligations exist in credit law — Phase 3). The team can't produce them from the model itself and must bolt on post-hoc explanation tooling. The governance failure happened at *model selection*: explainability requirements should have been an input to choosing the architecture.

3. **Exam-style stem.** "A model's behavior is determined by billions of learned numerical values, and its developers cannot state which input factors drove a specific output." What is described, and what governance consequence follows? → A deep neural network / the black-box problem; consequence: post-hoc explainability techniques and stronger documentation/oversight are required, or an interpretable model should be preferred.

## MEMORY HOOKS

**Chain to burn in: DATA → WEIGHTS → DEPTH → OPACITY → OVERSIGHT BURDEN.** Each arrow is an exam question somewhere.

**Dials analogy:** training = millions of dials nudged until outputs look right; no dial means anything alone — that *is* the explainability problem.

**Parameter vs hyperparameter:** parameters are *learned* by the machine; hyperparameters are *chosen* by humans. (Hyper = human, if you need the crutch.)

The 5 facts to retain:

1. A neural network = layers of units connected by learned weights; the weights are the model.
2. Deep learning = many hidden layers, enabling learned, abstract features — best on unstructured data (images, text, audio).
3. Training = iteratively adjusting weights to reduce a loss over many epochs (backpropagation + gradient descent, names only).
4. Depth causes opacity: no human-readable logic exists, so explainability needs dedicated techniques and documentation substitutes for readable code.
5. For tabular data, interpretable models are often competitive — architecture choice is a governance decision, not just an engineering one.

## SELF-CHECK

1. What are weights/parameters, and how do they differ from hyperparameters?
2. In one sentence each: layer, epoch, loss function.
3. Give three reasons deep models are opaque even to their builders.
4. Why does deep learning dominate vision and language but not always tabular problems?
5. A regulated lender wants a deep net for credit scoring. What governance question should be asked before development starts?

<details>
<summary>Answers</summary>

1. Weights/parameters are the numbers learned during training that constitute the model's knowledge; hyperparameters are configuration choices humans make before training (layers, learning rate).
2. Layer: a stage of transformation between input and output. Epoch: one full pass through the training data. Loss function: the formal measure of error that training minimizes.
3. Knowledge distributed across millions/billions of weights; internal features are learned rather than human-designed; non-linear cross-layer interactions defeat tracing — and sheer scale means access ≠ understanding.
4. Unstructured data needs learned features, deep learning's strength; tabular data already has human-defined features, where simpler interpretable models often match performance.
5. Whether explanation obligations (adverse action, contestability, oversight) can be met with this architecture — and if not, whether an interpretable model should be used instead; explainability requirements belong at model selection.

</details>
