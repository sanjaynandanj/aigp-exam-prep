# Governance Roles: Who Owns What, from Board to Data Steward

**Phase 2 · Lesson 09 · ~0.75h · BoK Domain I**

## EXAM FOCUS

Domain I — organizational roles in AI governance. Tested as **role-matching**: a scenario describes a task (approve risk appetite; maintain the inventory; validate a model independently) and asks whose job it is. The **three lines of defense** model applied to AI is a dependable question — know which line does what and the independence rules. Wrong answers typically assign second-line work to the first line, or board work to management.

## CORE

### The vertical chain

| Role | Owns | Does NOT own |
|---|---|---|
| **Board** | Oversight of management; approving **risk appetite** for AI; assurance that a governance framework exists and works; asking the informed questions | Day-to-day decisions; individual model approvals |
| **C-suite / accountable executive** | Strategy-risk alignment; resourcing the program; owning major AI risk acceptance; championing the charter | Detailed technical review |
| **AI governance lead / office** (sometimes CAIO or committee-supported) | Running the program: policies, inventory, tiering, gates, training, reporting upward; advising teams; escalating | *Owning each system's outcomes* — that stays with system owners; the lead runs the framework, not the models |
| **AI governance committee** | Cross-functional decision forum: hard cases, metric/trade-off calls (Lesson 03), exceptions, escalations | Substituting for named individual accountability |
| **System/model owner** (business) | A specific system's purpose, risk acceptance at its tier, lifecycle compliance, gate submissions, monitoring response | Building the model (that's the developer's craft) — ownership is accountability, not authorship |
| **Model developers / ML engineers** | Building to standards; documentation (model cards); testing; flagging risks honestly | Approving their own work at gates |
| **Data stewards** | Data quality, provenance, lawful sourcing, access, retention for training/operational data | Model design decisions |
| **Operators / human reviewers** | Run-time oversight, overrides, incident flagging (Lesson 05) | Policy setting |

Supporting cast to recognize in stems: privacy officer/DPO (DPIAs, data-subject rights), CISO (model/security threats), legal & compliance (obligations mapping), procurement (vendor AI intake — Phase 6), internal audit (below), HR (workforce impacts, training).

### Three lines of defense, applied to AI

The classic risk-governance geometry, AI edition:

| Line | Who | AI-specific work | The independence rule |
|---|---|---|---|
| **First line** — owns and manages risk | Business units, product teams, developers, system owners | Build, document, test, deploy, monitor; comply with policy; keep inventory entries current | They *take* the risk — they cannot be its only check |
| **Second line** — sets framework and challenges | AI governance office, risk management, compliance, (often) model risk management | Policies/standards, tiering methodology, gate review, **independent model validation**, advice and effective challenge, aggregate reporting | Independent of delivery pressure; challenges the first line without doing its work |
| **Third line** — independent assurance | **Internal audit** | Audits whether the whole framework (lines 1+2) is designed and operating effectively; reports to the board/audit committee | Independent of *both* other lines; assures the system of controls, not individual launches |

Banking heritage worth knowing: model risk management with independent validation (formalized in US supervisory guidance SR 11-7) is the mature template many AI programs borrow — "effective challenge" is its key phrase.

Classic exam traps: developers validating their own models (first line self-checking); internal audit designing the controls it will later audit (third line doing second-line work); the governance lead "owning" every model's risk (second line absorbing first-line accountability). Each violates the geometry.

### Committee vs individual

Committees decide *policies, exceptions, and hard trade-offs*; individuals own *systems and outcomes*. A program with only committees diffuses accountability ("everyone = no one," Lesson 05); a program with only individuals lacks a forum for cross-functional values decisions (like fairness-metric choice). You need both, wired by escalation paths.

## CASES & EXAMPLES

1. **Role-match stem.** "Who should approve the organization's overall tolerance for AI-related risk?" → the **board** (risk appetite is board-level). Distractors: CAIO, governance committee — they operate *within* the appetite, they don't set it.

2. **The self-validating team.** A pricing team builds, tests, and approves its own model, citing deadline pressure; governance learns post-launch. Two geometry violations: no second-line independent validation/gate, first line accepting risk beyond its authority. Fix: tier-triggered mandatory second-line review before deployment — with authority to block.

3. **Audit in the wrong seat.** Internal audit writes the AI policy and staffs the pre-deployment gate — then is asked to audit the program. It can no longer assure independently what it built. Correct placement: audit assesses the *framework's* design and operation and reports to the audit committee; second line writes policy and runs gates.

4. **The overloaded governance lead.** Every AI incident, model choice, and vendor question lands on one "Head of AI Governance," while business owners disclaim responsibility ("governance owns AI now"). Failure: second line absorbing first-line ownership. Fix: named system owners in the inventory, with the lead running framework, advice, and challenge — not each system.

## MEMORY HOOKS

**Three-lines one-liner:** *First line owns it, second line checks it, third line checks the checkers.*

**Board test:** if the word is *appetite*, *oversight*, or *assurance* → board. If it's *run*, *build*, *operate* → management/first line. If it's *framework*, *challenge*, *validate* → second line. If it's *independent assurance of the whole thing* → internal audit.

The 5 facts to retain:

1. Board: risk appetite + oversight + assurance questions — never day-to-day model decisions.
2. The AI governance lead runs the *framework*; named system owners own each system's outcomes — the distinction defeats several distractors.
3. Three lines: business owns risk (1), governance/risk/compliance sets framework and challenges — including independent model validation (2), internal audit independently assures both (3).
4. Independent validation ("effective challenge," SR 11-7 heritage) means developers never solely approve their own models.
5. Committees for cross-functional trade-offs and exceptions; individuals for system accountability — both, connected by escalation.

## SELF-CHECK

1. Assign the line (1/2/3): (a) maintaining a system's monitoring dashboards; (b) auditing whether gates operate as designed; (c) writing the fairness-testing standard; (d) independently validating a credit model.
2. What does the board own in AI governance, in three words or phrases?
3. Why must the AI governance lead not be recorded as "owner" of every AI system?
4. What is "effective challenge" and where does the concept come from?
5. A stem says: "the committee approved the exception; no individual is accountable for the system." What's wrong?

<details>
<summary>Answers</summary>

1. (a) first line; (b) third line; (c) second line; (d) second line (independent validation function).
2. Risk appetite, oversight of management, assurance that the framework works.
3. It collapses the second line into the first: the challenger becomes the owner, business teams shed accountability, and independence of review disappears — ownership must sit with the business system owner.
4. Independent, qualified, empowered review of models by people not involved in building them — from banking model-risk supervisory guidance (US SR 11-7), the template for AI model validation.
5. Committee decisions don't substitute for named individual accountability — a specific system owner must still answer for the system's outcomes; otherwise responsibility is diffused.

</details>
