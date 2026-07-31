# Question Anatomy: Stems, Distractors, and Scenario Strategy

**Phase 7 · Lesson 01 · ~1h · Exam technique (all domains)**

## EXAM FOCUS

This lesson is about the exam itself: how AIGP questions are built, how wrong answers are engineered, and how to work a 100-question paper (~85 scored + ~15 unscored pilot items you cannot identify — treat every question as scored) in the allotted time. Verify format specifics against your current candidate handbook. Then drill the method on `practice/quiz-domain-1.md` through `quiz-domain-4.md` and the full `practice/mock-exam.md`.

## CORE

### The three stem types

| Stem type | Recognizable by | What it's really testing | How to attack |
|---|---|---|---|
| **Recall** | "Which of the following is…", "Under the EU AI Act, who…" | A definition, list membership, or actor-obligation pairing | Answer from memory *before* reading options; then find your answer among them |
| **Best-answer** | "MOST appropriate", "BEST next step", "FIRST action", "PRIMARY purpose" | Judgment among several defensible options | Rank, don't verify: several options are *true*; only one best satisfies the qualifier (most/first/primary) |
| **Scenario** | A paragraph of facts about an organization, then 1+ questions | Applying frameworks to messy facts; ~30% of the exam | Triage method below; read the *question line first*, then mine the scenario for the relevant facts |

Qualifier words are load-bearing: FIRST asks for sequence (intake before DPIA before build), MOST asks for proportionality, EXCEPT/NOT reverses the task (slow down; mark the three true statements to expose the one false).

### The distractor patterns

Distractors are engineered, and AIGP's favorites are predictable:

| Pattern | Example | Counter |
|---|---|---|
| **Right framework, wrong function** | Offering "MEASURE" when the NIST AI RMF activity described is "MAP"; citing ISO/IEC 42001 for risk-metric detail that belongs to 23894 | Know each framework's internal structure, not just its name |
| **GDPR / AI Act confusion** | A DPIA offered where a FRIA is required; "supervisory authority" where "market surveillance authority" belongs; GDPR fine tiers attached to AI Act violations | Anchor: GDPR governs personal-data processing; the AI Act governs AI systems by risk class — different triggers, owners, regulators |
| **Provider / deployer swap** | Assigning conformity assessment to the deployer or Art. 26 oversight duties to the provider | "Name, Change, Aim" and *providers make it safe to sell; deployers keep it safe to use* (Phase 5 L10) |
| **Lifecycle misplacement** | An ex ante instrument (impact assessment) offered as a post-deployment fix | Place every activity on the lifecycle map (Phase 5 L01) |
| **True but off-target** | A correct statement that doesn't answer *this* question | Re-read the question line; truth is not relevance |
| **Extreme absolutes** | "always", "never", "guarantees", "eliminates all bias" | Governance language is proportionate; absolutes are usually wrong |
| **Kitchen-sink overreach** | The option demanding every control at maximum for a minimal-risk tool | Proportionality: match rigor to risk tier |

### Scenario triage method (the 4-step)

For every scenario question, extract in order:

1. **Actor** — who are we? Provider, deployer, importer, vendor, controller, auditor? (Obligations follow the role.)
2. **Lifecycle stage** — design, data, testing, pre-release, in operation, retirement? (Controls follow the stage.)
3. **Jurisdiction/framework** — EU AI Act? GDPR? US sectoral/state (LL144, Colorado)? NIST/ISO voluntary? (Duties follow the regime.)
4. **Eliminate** — strike options that contradict the actor, the stage, or the regime; among survivors, apply the qualifier (first/most/best).

Most scenario questions die at step 4 with only one option left standing. When two survive, prefer the one that is more proportionate, more ex ante, and more accountable (named owner, documented decision).

### Time budgeting and flagging

- Assume ~180 minutes for 100 questions ⇒ **~1.8–1.9 min/question** (confirm current timing in the handbook). Bank time on recall items (30–45s) to fund scenarios (2.5–3 min).
- **Three-pass discipline:** Pass 1 — answer everything answerable, flag the hard ones (target: through all 100 with ~25–30 min spare). Pass 2 — flagged items with fresh eyes. Pass 3 — sanity sweep; change answers only for a *reason* (misread, recalled fact), not a feeling.
- **Guessing discipline:** scoring counts correct answers; **no penalty for wrong answers — never leave a blank.** Eliminate one or two distractors and guess from the rest; before submitting, ensure every question has a selection.
- One question = one data point: a brutal item may be an unscored pilot. Spend your budget, pick, flag, move.

### The +2/+7 question-journal loop

Every practice question you miss (or guess right) enters the journal (`practice/question-journal-template.md`): the question's *concept*, why the right answer is right, why yours was wrong, and the distractor pattern it used. Re-test yourself on journal items at **+2 days** and **+7 days** — spaced retrieval converts near-misses into locked knowledge. Journal analytics beat re-reading: three misses tagged "provider/deployer swap" tells you exactly which lesson to re-drill (Phase 5 L10), which no amount of passive review reveals.

## CASES & EXAMPLES

**Worked example 1 — qualifier control.** *"A deployer discovers its high-risk vendor system may have caused a serious incident. What should it do FIRST?"* Options: (a) report to the market surveillance authority, (b) inform the provider, (c) conduct a FRIA, (d) notify affected persons. Triage: actor = deployer; regime = AI Act Art. 73 concept; the deployer's reporting flow runs through the provider → **(b)**. (a) is the provider's job — the provider/deployer swap distractor; (c) is ex ante, wrong stage; (d) may follow but isn't FIRST.

**Worked example 2 — true but off-target.** *"What is the PRIMARY purpose of a model card?"* Option (a) "documents dataset collection methodology" is a true description *of a datasheet* — right artifact family, wrong object (Phase 5 L07 pattern). The answer is the option about communicating a model's intended use, limits, and evaluated performance.

**Worked example 3 — elimination cascade.** A scenario describes a bank *using* a licensed credit model in the EU that is drifting. Strike every option assigning the bank provider duties (conformity re-assessment, technical documentation) — actor mismatch. Strike "retrain and redeploy immediately" — skips re-validation, lifecycle violation. Survivor: suspend/mitigate per instructions, inform the provider, investigate per monitoring runbook.

## MEMORY HOOKS

**Triage mantra — "A-L-J-E": Actor, Lifecycle, Jurisdiction, Eliminate.**

**Distractor top-3 — "the three swaps":** framework-function swap, GDPR↔AI-Act swap, provider↔deployer swap. When stuck, check whether the tempting option commits one.

**Clock rule:** *~1.9 minutes each; recall funds scenarios; three passes; zero blanks.*

The 5 facts to retain:

1. Stems come in three builds — recall, best-answer (qualifier-driven), scenario (~30% of the exam) — and the qualifier word (FIRST/MOST/EXCEPT) decides the answer among true options.
2. The highest-frequency distractor engines: right-framework-wrong-function, GDPR/AI-Act confusion, and provider/deployer swaps — plus true-but-irrelevant and absolutist options.
3. Scenario method: identify Actor → Lifecycle stage → Jurisdiction/framework → Eliminate; survivors are judged on proportionality and the qualifier.
4. Budget ~1.9 min/question, run three passes with flag-and-return, and answer everything — there is no wrong-answer penalty.
5. Misses go into the question journal and get re-tested at +2 and +7 days; tag them by distractor pattern to target your re-study.

## SELF-CHECK

1. **What do the words FIRST, MOST, and EXCEPT each demand of you?**
   FIRST: correct sequencing (earliest proper action). MOST: ranking among several true/defensible options. EXCEPT/NOT: reversal — find the one false/non-fitting option (verify the other three are true).
2. **Name the three "swap" distractor patterns and one immunization for each.**
   Framework-function swap (learn each framework's internal parts); GDPR/AI-Act swap (GDPR = personal data & supervisory authorities; AI Act = risk-classified AI systems & market surveillance authorities); provider/deployer swap ("providers make it safe to sell, deployers keep it safe to use").
3. **Recite the four scenario-triage steps.**
   Identify the actor/role; identify the lifecycle stage; identify the jurisdiction/framework in play; eliminate options contradicting any of the three, then apply the qualifier.
4. **Why should you never leave a question blank, and when may you change an answer on review?**
   There is no penalty for wrong answers — only correct answers score, so a guess strictly dominates a blank. Change on review only with an articulable reason (misread stem, recalled a fact), never on vague second-guessing.
5. **Describe the +2/+7 journal loop.**
   Every missed or lucky-guess question is journaled with concept, correct rationale, your error, and the distractor pattern; you actively re-test those items 2 days later and again 7 days later, and use pattern tags to direct which lessons to re-drill.
