# Sociotechnical Systems: Why AI Risk Is Never Just Technical

**Phase 1 · Lesson 09 · ~0.75h · BoK Domain I**

## EXAM FOCUS

Domain I — the sociotechnical framing that underpins both NIST AI RMF (which explicitly calls AI systems "inherently socio-technical in nature") and the EU AI Act's context-based risk classification. Tested mostly through **scenarios**: the right answer widens the lens beyond the model (to people, process, context), and the classic wrong answers are purely technical fixes to sociotechnical problems. If you internalize one idea from Phase 1 for the scenario questions, make it this one.

## CORE

### The equation

**AI risk = model + data + people + process + context.**

| Component | What it contributes to risk | Example failure |
|---|---|---|
| **Model** | Accuracy, robustness, opacity | Misclassification, drift |
| **Data** | Bias, quality, provenance | Historical discrimination encoded |
| **People** | How humans use, trust, override, game the system | Automation bias; deskilling; operators gaming metrics |
| **Process** | Workflows the AI sits inside; escalation paths; incentives | No appeal route; output treated as final decision |
| **Context** | Who is affected, stakes, power asymmetries, deployment setting | Same model, harmless in one setting, rights-affecting in another |

A technically excellent model can produce a harmful *system* (perfect fraud model + rubber-stamp reviewers + no appeals), and a mediocre model can sit in a safe system (weak triage model used only as one advisory signal with strong human process). **Risk is a property of the whole assembly, not the artifact.**

### Deployment context changes risk class

The same technical capability moves across the entire risk spectrum with context:

| Capability | Low-risk context | High-risk context |
|---|---|---|
| Face matching | Unlocking your own phone (1:1, consented) | Police identification in public spaces (1:many, coercive) |
| Text generation | Drafting marketing copy | Generating medical or legal advice to consumers |
| Scoring/ranking | Ranking movie recommendations | Ranking job applicants or credit applicants |
| Emotion inference | Game character reacting to a player | Assessing employees or students |

This is not just theory — it is *how the law is built*: the EU AI Act classifies by **use case and context** (Annex III lists deployment areas — employment, credit, law enforcement…), not by algorithm type. NIST AI RMF's Map function exists precisely to establish context before risks are measured or managed. Exam translation: any answer that assigns risk based on the algorithm alone ("it's deep learning, so it's high risk") is wrong; risk follows *use*.

### Consequences for governance practice

1. **Assessment must include context questions:** who is affected, what decisions attach, what recourse exists, what happens when it's wrong — not just accuracy metrics.
2. **Controls span all five components:** technical (testing, monitoring), data (governance, documentation), people (training, oversight design), process (escalation, appeals, incident response), context (use restrictions, ban lists).
3. **A model cleared for one use is not cleared for others** — re-assessment on repurposing is a standard control (and an exam-favorite "what's missing" answer).
4. **Affected people are part of the system:** their ability to understand, contest, and correct outputs (contestability) is a design requirement, not a courtesy.
5. **Evaluation in the lab ≠ evaluation in the field:** pilots, staged rollouts, and post-deployment monitoring exist because human behavior around the system (trust, gaming, workarounds) only appears in deployment.

### The gaming/feedback dimension

People adapt to systems: applicants keyword-stuff résumés for screeners; drivers alter routes for algorithmic dispatch; officers over-patrol where predictions point, generating arrests that "confirm" the prediction (**feedback loops**). A system changes the world that produces its future inputs — another reason static, one-time validation cannot certify safety.

## CASES & EXAMPLES

1. **Dutch childcare benefits scandal (toeslagenaffaire).** Dutch tax authorities used risk-scoring (with factors including dual nationality) plus a hardline recovery process to pursue fraud in childcare benefits; thousands of families — disproportionately with immigration backgrounds — were wrongly forced to repay large sums, with severe consequences. The government resigned in 2021 over the affair. The failure was sociotechnical end-to-end: biased signals (data), no meaningful human correction (people), a punitive zero-tolerance process with weak appeal (process), targeting a vulnerable population (context). No model-accuracy improvement would have fixed it.

2. **Same model, two hospitals.** A sepsis-alert model succeeds in Hospital A (alerts routed to a staffed response team, thresholds tuned, clinicians trained) and fails in Hospital B (alert fatigue, no owner, staff ignore it). Identical model — different people and process. Exam point: deployment readiness is about the receiving organization as much as the artifact.

3. **Predictive policing feedback loop.** Patrols sent where past arrests cluster generate new arrests there, reinforcing the pattern regardless of underlying crime rates. Data reflects enforcement, the system amplifies it, and context (policing power) turns statistical artifact into rights impact. Purely technical debiasing cannot resolve what is partly a process-and-context problem.

4. **Exam-style scenario.** "A well-validated exam-proctoring model flags 'suspicious behavior.' Complaints arrive that students with disabilities and slower internet connections are flagged disproportionately, and flagged students fail the course automatically with no review." Best answer shape: the *process* (automatic consequence, no human review, no appeal) and *context* (high stakes, vulnerable subgroups) are the primary failures — introduce meaningful review and contestation, re-assess fitness for this population; "retrain the model" alone is the distractor.

## MEMORY HOOKS

**The equation:** *risk = model + data + people + process + context* — recite it before answering any scenario question.

**Two slogans:** *"Great model, harmful system" is possible; "same model, different context, different risk class" is law.*

The 5 facts to retain:

1. AI systems are sociotechnical: harm emerges from the assembly of model, data, people, process, and context — NIST AI RMF says so explicitly.
2. Deployment context — not algorithm type — drives risk classification in modern AI law (EU AI Act Annex III logic).
3. Repurposing a model to a new context requires re-assessment; clearance doesn't transfer.
4. Humans adapt to and game systems, and systems reshape their own future inputs (feedback loops) — so validation is never one-and-done.
5. The Dutch childcare benefits scandal is the canonical case of sociotechnical failure: data, process, oversight, and context all failed together, with a government-toppling result.

## SELF-CHECK

1. Write out the five-component risk equation and give one failure example per component.
2. Why does the EU AI Act classify systems by use context rather than by technique?
3. Give two reasons a technically excellent model can still produce serious harm.
4. What is a feedback loop in deployed AI, and which famous application domain illustrates it?
5. In the proctoring scenario above, why is "retrain the model" an incomplete answer?

<details>
<summary>Answers</summary>

1. Model (drift/misclassification), data (encoded historical bias), people (automation bias, gaming), process (no appeal, output auto-executed), context (high-stakes or vulnerable populations). Risk = all five together.
2. Because the same technique spans trivial to rights-critical uses; harm potential is determined by who is affected and what decisions attach — context — so regulating by technique would both over- and under-shoot.
3. Any two of: surrounding process may attach automatic, unappealable consequences; human oversight may be nominal (automation bias); context may involve stakes/populations the validation never covered; repurposing beyond validated use.
4. The system's outputs change behavior that generates its future training/input data, entrenching its own patterns — predictive policing (patrol → arrests → "confirmed" predictions) is the standard example.
5. The dominant harms flow from process (automatic failure, no review/appeal) and context (high stakes, disparate impact on subgroups); model retraining addresses neither contestability nor consequence design.

</details>
