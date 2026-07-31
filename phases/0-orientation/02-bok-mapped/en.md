# BoK v2.1 Mapped: Where the 85 Points Live

**Phase 0 · Lesson 02 · ~1h · BoK Domain —**

## EXAM FOCUS

No exam question asks about the blueprint itself, but the blueprint decides where your hours should go. This lesson turns the BoK v2.1 domain weights into an hour-allocation strategy and shows exactly which phase of this repo covers which domain.

## CORE

### The four domains of BoK v2.1

BoK v2.1 (effective 2026-02-02) organizes the exam into **four domains**. The IAPP publishes an approximate scored-question range per domain:

| Domain | Name | Scored Qs | Share of 85 | Covered by |
|---|---|---|---|---|
| **I** | Foundations of AI governance — AI/ML technology + responsible-AI concepts | 16–20 | ~19–24% | Phases 1–2 |
| **II** | Laws, standards and frameworks — current law, EU AI Act, NIST AI RMF, ISO, soft law | 19–23 | ~22–27% | Phases 3–4 |
| **III** | Governing AI development — lifecycle, data, testing, assessments, documentation | 21–25 | ~25–29% | Phase 5 |
| **IV** | Governing AI deployment and use — vendors, monitoring, oversight, incidents, audit | 21–25 | ~25–29% | Phase 6 |

Add the midpoints: Domains II–IV together carry roughly **70 of 85** scored questions. Domain I is the smallest — necessary scaffolding, but not where the exam is won.

### What each domain actually tests

| Domain | Typical question flavor |
|---|---|
| I | Fact recall: define supervised learning; identify a fairness metric; name a NIST trustworthiness characteristic |
| II | Mixed: recall (which AI Act article prohibits X) + scenario (classify this system's risk tier; which regulator has jurisdiction) |
| III | Scenario-heavy: a development team did X — what governance step is missing? Which assessment applies at this stage? |
| IV | Scenario-heavy: a deployed system drifted / a vendor won't share documentation / an incident occurred — what should the deployer do first? |

The ~30% scenario questions cluster in Domains II–IV. That means memorization alone passes Domain I but not the exam; you need to *apply* frameworks to fact patterns.

### Hour-allocation strategy

This repo's ~82 coursework hours already track the weights, so the simplest strategy is: follow the phases in order and do not over-linger in Phase 1.

| If your total budget is… | Phases 1–2 (Dom. I) | Phases 3–4 (Dom. II) | Phase 5 (Dom. III) | Phase 6 (Dom. IV) | Phase 0 + 7 |
|---|---|---|---|---|---|
| ~80h (Default track) | ~20h | ~26h | ~11h | ~11h | ~14h |
| ~55h (Sprint, prior privacy background) | ~10h (skim) | ~20h | ~10h | ~10h | ~5h |

Three allocation rules:

1. **The EU AI Act is the single highest-yield block** — the most detailed, most-tested content. It gets two passes (Week 4–5 and final review week).
2. **NIST AI RMF + ISO/IEC 42001** is the second-highest-yield block, because RMF vocabulary (Govern/Map/Measure/Manage) leaks into Domain III and IV scenario answers.
3. **Never rob Domains III–IV to polish Domain I.** A perfect Domain I score caps out around 20 questions; Domains III+IV together offer up to 50.

### How this repo maps

```
Phase 0  → exam logistics + study system      (no domain)
Phase 1  → AI/ML technology                   (Domain I)
Phase 2  → responsible AI + governance basics (Domain I)
Phase 3  → existing law applied to AI         (Domain II)
Phase 4  → EU AI Act, NIST RMF, ISO, soft law (Domain II — highest yield)
Phase 5  → governing development              (Domain III)
Phase 6  → governing deployment & use         (Domain IV)
Phase 7  → question technique + mocks         (all domains)
```

## CASES & EXAMPLES

1. **The engineer's mistake.** A ML engineer spends three weeks perfecting Phase 1 because it feels comfortable, then rushes the AI Act in four days. Result: strong on the ~18 Domain I questions, weak on the ~21 Domain II questions. The blueprint punishes studying what you already like.

2. **The lawyer's mistake.** A privacy lawyer skips Phase 1 entirely ("I don't need the tech"). On exam day, Domain III scenarios assume they know what drift, fine-tuning, and training/inference distinctions are — and Domain I stems use terms like "ground truth" without defining them. Skim, don't skip.

3. **Reading a diagnostic.** After the Phase 0 baseline, a candidate scores: Dom I 75%, Dom II 40%, Dom III 55%, Dom IV 50%. Correct reaction: shift ~5 hours from Phases 1–2 into Phase 4, and take the Sprint-track pacing for Phase 1 only.

## MEMORY HOOKS

**Weight mnemonic — "16-19-21-21":** the *lower bounds* of Domains I→IV (16-20, 19-23, 21-25, 21-25). Domain I starts lowest; III and IV tie for biggest.

**"Two thirds live downstream":** law + development + deployment ≈ 70 of 85 points.

The 5 facts to retain:

1. Four domains in BoK v2.1: Foundations / Laws & frameworks / Development / Deployment & use.
2. Question ranges: I: 16–20, II: 19–23, III: 21–25, IV: 21–25.
3. Domains II–IV ≈ 70 of 85 scored questions.
4. Highest-yield single topic: EU AI Act; second: NIST AI RMF + ISO/IEC 42001.
5. Scenario questions (~30%) cluster in II–IV — practice application, not just recall.

## SELF-CHECK

1. List the four BoK v2.1 domains in order.
2. Which two domains have the highest question ranges, and what is that range?
3. Roughly how many of the 85 scored questions come from Domains II–IV combined?
4. Which repo phases cover Domain II?
5. You have 10 spare study hours and your baseline shows equal weakness everywhere. Where do they go, and why?

<details>
<summary>Answers</summary>

1. I: Foundations of AI governance; II: Laws, standards and frameworks; III: Governing AI development; IV: Governing AI deployment and use.
2. Domains III and IV, each 21–25 scored questions.
3. Roughly 70.
4. Phases 3 (current law) and 4 (EU AI Act, NIST RMF, standards).
5. Phase 4 — the EU AI Act + NIST RMF block is the highest-yield content per hour, and Domain II feeds scenario answers in III and IV too.

</details>
