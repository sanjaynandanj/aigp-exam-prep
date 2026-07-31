# Use-Case Intake: Problem Definition, Feasibility, Ban Lists

**Phase 5 · Lesson 02 · ~1h · BoK Domain III**

## EXAM FOCUS

This lesson covers the very first governance gate: deciding whether an AI use case should exist at all. The exam tests it through scenarios where a team wants to build something and you must pick the *first* correct step (almost always: define the problem and screen the use case — not "collect data" or "select a model"). Also tested: risk tiering at intake, prohibited/banned use screening, and who reviews intake submissions.

## CORE

### Why intake exists

The cheapest place to stop a bad AI system is before it is built. Intake converts an idea into a structured, reviewable record and applies three filters:

| Filter | Question | Kills the use case when… |
|---|---|---|
| **Problem definition** | What decision or task is this improving, for whom, measured how? | The problem is vague ("use AI for HR"), or a non-AI solution works as well |
| **Feasibility** | Do we have lawful, sufficient data, skills, and budget? Is the target actually predictable? | Data is unavailable/unlawful, or the outcome cannot be reliably inferred |
| **Necessity & proportionality** | Is AI necessary for the goal, and is the intrusion/risk proportionate to the benefit? | A less risky means achieves the same end (a concept imported from data-protection law) |

### Risk tiering at intake

Intake assigns a provisional **risk tier** that drives everything downstream (depth of assessment, testing rigor, approval level). A typical scheme mirrors the EU AI Act pyramid:

| Tier | Examples | Consequence |
|---|---|---|
| **Prohibited / banned** | Social scoring, manipulative techniques, uses on the organization's own ban list | Rejected at intake; no build |
| **High risk** | Employment screening, credit, essential services, safety components, biometric categorization | Full impact assessment, enhanced gates, senior sign-off |
| **Limited / transparency risk** | Chatbots, content generation | Disclosure duties, standard review |
| **Minimal risk** | Spam filters, internal productivity aids | Lightweight review, inventory entry only |

Key exam nuance: the tier reflects the **use case in context** (purpose + affected persons + domain), not the model technology. The same LLM is minimal-risk as a brainstorming aid and high-risk as a CV screener.

### Ban lists

Organizations maintain an internal **ban list** (red lines) that typically includes: legally prohibited practices (EU AI Act Art. 5 categories where applicable), uses incompatible with company values (e.g., covert emotion inference on employees), and uses the organization cannot govern safely (e.g., fully automated adverse decisions with no human review). Ban lists make intake fast: a screener can reject without debate.

### The intake form and reviewers

A defensible intake record captures:

- Business owner + accountable sponsor (a *named* person, not a team)
- Problem statement, success metrics, affected populations
- Data sources contemplated (personal data? special categories? licensed?)
- Build/buy/fine-tune posture (drives provider vs deployer analysis — Lesson 10)
- Provisional risk tier + trigger checklist (DPIA? FRIA? sectoral rules?)

| Reviewer | Looks for |
|---|---|
| AI governance lead / secretariat | Completeness, tier assignment, routing |
| Privacy / DPO | Personal data triggers, DPIA need |
| Legal / compliance | Prohibited practices, sectoral law, IP |
| Security | Data sensitivity, attack surface |
| Business / ethics committee (higher tiers) | Necessity, proportionality, reputational fit |

Low-tier cases may pass on a screener's review; high-tier cases go to the AI governance committee. **Proportionate governance** — matching review depth to risk — is itself an exam-favored principle.

## CASES & EXAMPLES

**Scenario 1 — first step.** A sales VP asks the data team to "add AI churn prediction." The team's *first* governance step? *Best answer:* submit a use-case intake defining the problem, affected persons, data needs, and provisional risk tier. Distractors: "procure a vendor model," "begin data collection," "run a DPIA" (a DPIA may follow, but intake determines whether one is triggered).

**Scenario 2 — ban-list catch.** A retailer proposes cameras that infer shoppers' emotions to adjust prices in real time. Intake flags it against the ban list (manipulative/emotion-inference red lines; potential prohibited-practice territory in the EU). *Exam point:* the right outcome is rejection at intake — not "proceed with strong safeguards."

**Scenario 3 — tier depends on context.** Team A wants a foundation model to summarize internal meeting notes; Team B wants the same model to rank job applicants. *Exam point:* Team B's use case is high-risk (employment) and triggers full assessment; Team A's is minimal. Same model, different tier — context governs.

**Scenario 4 — necessity test.** A university wants AI proctoring with webcam emotion analysis to catch cheating. A rules-based lockdown browser achieves most of the benefit with far less intrusion. *Exam point:* proportionality analysis favors the less intrusive alternative; "AI because AI" fails the necessity filter.

## MEMORY HOOKS

**Intake mnemonic — "P-F-N-T-B": Problem, Feasibility, Necessity, Tier, Ban-check.**

**Contrast to burn in:** *Intake asks "should we?"; testing asks "does it work?"; release gates ask "may it ship?"*

The 5 facts to retain:

1. Intake is the first governance gate: it screens problem definition, feasibility, and necessity/proportionality before any build.
2. Risk tier is assigned by **use case in context**, not by the underlying model.
3. Ban lists encode legal prohibitions plus organizational red lines and enable fast rejection.
4. Every intake needs a named accountable owner and a documented tier with trigger checks (DPIA/FRIA/sectoral).
5. Review depth scales with tier — proportionate governance, screener review for low risk, committee review for high risk.

## SELF-CHECK

1. **What three filters does use-case intake apply before anything is built?**
   Problem definition, feasibility, and necessity/proportionality.
2. **Why can the same model land in different risk tiers?**
   Because tiering follows the use case's purpose, domain, and affected persons — context — not the technology itself.
3. **Name three things an internal AI ban list typically contains.**
   Legally prohibited practices (e.g., EU AI Act Art. 5-type uses), uses conflicting with organizational values, and uses the organization cannot safely control/oversee.
4. **Who typically reviews a high-risk intake versus a minimal-risk one?**
   High-risk: cross-functional AI governance committee (privacy, legal, security, ethics) with senior sign-off; minimal-risk: a lightweight screener review plus inventory registration.
5. **In an exam scenario where a business unit "wants AI," what is almost always the correct first action?**
   File/complete a use-case intake (define the problem and screen it) — before data collection, vendor selection, or model building.
