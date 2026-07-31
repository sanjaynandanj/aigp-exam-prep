# Building the Governance Program: Charters, Policies, Inventories, Gates

**Phase 2 · Lesson 08 · ~1h · BoK Domain I**

## EXAM FOCUS

Domain I — the anatomy of an AI governance program. Tested heavily as **scenario**: an organization is described mid-failure and you name the missing component (usually: no inventory, no risk tiering, or no gates). Also tested as sequence ("what comes first when standing up a program?" — mandate and inventory before tooling) and light recall on maturity models. This lesson is the skeleton Phases 5–6 hang controls on.

## CORE

### The program stack, top to bottom

| Layer | Artifact | What it does |
|---|---|---|
| Mandate | **Charter** | Board/executive authorization: scope, objectives, authority, resourcing, risk appetite for AI |
| Rules | **Policy hierarchy** | Policy → standards → procedures → guidelines (see below) |
| Visibility | **AI inventory / registry** | The authoritative list of all AI systems/use cases with owners and risk tiers |
| Prioritization | **Risk tiering** | Classifies each use case so scrutiny scales with risk |
| Control points | **Gates** | Mandatory checkpoints in the lifecycle where evidence is reviewed and go/no-go decided |
| People | Roles & committees | Lesson 09 |
| Assurance | Monitoring, audit, metrics, reporting | Phases 5–6 |

### The charter

A program without a charter is a volunteer effort. The charter states: purpose and scope (what counts as "AI" here — inherit the OECD-aligned definition), the governance body's **authority** (can it stop a launch?), escalation paths, resourcing, and reporting lines to executive/board level. Exam cue: when a scenario shows a governance team ignored by product teams, the root cause on offer is usually a missing/weak mandate — not missing tools.

### The policy hierarchy

| Level | Nature | Example |
|---|---|---|
| **Policy** | Binding "what and why," stable, board/exec-approved | "All AI use cases must be inventoried, risk-tiered, and pass required gates before deployment" |
| **Standard** | Binding "how much / which," specific and testable | "High-tier systems require disaggregated fairness testing across defined groups pre-release" |
| **Procedure** | Step-by-step "how," role-assigned | "How to submit a use case for intake review" |
| **Guideline** | Recommended good practice, non-binding | "Prompt-writing guidance for approved genAI tools" |

Design principle: policies change rarely; standards and procedures absorb the churn of technology and law. AI policy should also *integrate with* existing policies (privacy, security, procurement, records) rather than duplicate them — contradictory duplicate regimes are a named failure pattern.

### The AI inventory / registry

The single most load-bearing artifact — you cannot govern what you cannot list. Minimum fields per entry:

- System/use-case name and description; business purpose
- **Named owner** (accountability anchor — Lesson 05)
- Risk tier; applicable laws/obligations
- Data used (categories, sources); models involved (built/bought/embedded)
- Lifecycle status; gate history; review dates

Practical hard parts (and exam scenario fodder): **shadow AI** (teams using unapproved tools — discovery requires procurement hooks, network telemetry, and amnesty-style intake), **AI embedded in purchased SaaS** (vendor features count), and keeping the register *live* (periodic attestation by owners, not a one-time census). Regulatory echo: the EU AI Act's database registration for high-risk systems is a public cousin of the internal inventory.

### Risk tiering of use cases

Scrutiny must scale with risk or the program drowns. Typical internal scheme (deliberately rhyming with the EU AI Act pyramid — Phase 4):

| Tier | Criteria (illustrative) | Treatment |
|---|---|---|
| **Prohibited** | On the organization's ban list (e.g., manipulative uses, unlawful surveillance) | Rejected at intake |
| **High** | Legal/rights effects on people; safety; regulated domains (employment, credit, health); vulnerable populations | Full assessments, all gates, senior sign-off, enhanced monitoring |
| **Medium** | Meaningful business/customer impact, human mediation present | Standard assessment and gates |
| **Low** | Internal productivity, no personal-data or rights impact | Lightweight registration, periodic review |

Tiering keys off **use context**, not algorithm sophistication (Lesson 1.09). Common trap: tier assigned once and never revisited — re-tiering on repurposing/scope change is a required control.

### Gates

| Gate | Placed at | Sample evidence demanded |
|---|---|---|
| Intake/ideation | Before build/procure | Use-case description, initial tier, ban-list check |
| Design | Before development at scale | Data sourcing plan, DPIA/AIA triggers, oversight design |
| Pre-deployment | Before go-live | Test results (incl. fairness/robustness where required), documentation, sign-offs |
| Post-deployment | In operation | Monitoring reports, incident reviews, periodic re-assessment |

Gate mechanics that make them real: defined evidence, named approvers with authority to say no, recorded decisions, and a route to escalate disputes. Gates without recorded refusals ever = decoration.

### Maturity models

Programs are assessed on maturity ladders (CMM-style, five levels are the convention):

**1 Initial/ad hoc** (heroics, no repeatability) → **2 Repeatable** (some documented process, inconsistent) → **3 Defined** (org-wide standard processes — policies, inventory, gates exist) → **4 Managed** (quantitatively measured — metrics, KPIs, systematic monitoring) → **5 Optimizing** (continuous improvement, feedback loops).

Use on the exam: place a described organization on the ladder and name the *next* step — the right answer moves one level, not from 1 to 5 in a bound.

## CASES & EXAMPLES

1. **The unlisted chatbot.** A regulator inquiry asks a bank to enumerate its AI systems affecting customers; the bank finds three customer-facing models nobody centrally knew about (one inside a purchased CRM). Missing component: inventory (with vendor-embedded coverage). Every downstream control — tiering, gates, monitoring — was structurally impossible without it. "Inventory first" is the canonical sequencing answer.

2. **One-size-fits-all review.** A company routes *every* AI use case — meeting-notes summarizer and credit model alike — through the same 12-week full review. Backlog explodes; teams start bypassing (shadow AI). Missing component: risk tiering to scale scrutiny. The fix is proportionality, not more reviewers.

3. **The gate that never says no.** An insurer's pre-deployment gate has approved 100% of 214 submissions, mostly same-day. Diagnosis parallels the rubber-stamp oversight case (Lesson 05): evidence requirements undefined, approvers lack authority/independence. A gate is a control only if refusal is a live possibility — look for recorded rejections and conditions.

4. **Sequencing stem (exam style).** "A newly appointed AI governance lead should FIRST: (a) procure a governance platform, (b) draft detailed genAI procedures, (c) secure a chartered mandate and build the AI inventory, (d) commission an external audit." → (c). Mandate gives authority; inventory gives visibility; everything else orders after.

## MEMORY HOOKS

**Program spine — "C-P-I-T-G":** **C**harter → **P**olicies → **I**nventory → **T**iering → **G**ates ("**C**an't **P**olice **I**nvisible **T**hings, **G**enius").

**Two aphorisms that answer many stems:** *you can't govern what you can't list* (inventory) and *scrutiny scales with risk or the program drowns* (tiering).

The 5 facts to retain:

1. Charter first: authority, scope, and escalation from the top — governance without mandate is advice.
2. Policy hierarchy: policy (what/why) → standard (testable how-much) → procedure (how) → guideline (recommended); stability decreases going down.
3. The AI inventory with named owners and risk tiers is the load-bearing artifact; shadow AI and vendor-embedded AI are its hard cases.
4. Risk tiering keys off use context; prohibited/high/medium/low with treatment scaling — re-tier on repurposing.
5. Gates = lifecycle checkpoints with defined evidence, empowered approvers, recorded decisions; maturity climbs ad hoc → repeatable → defined → managed → optimizing.

## SELF-CHECK

1. Order the program components a new lead should establish, and justify the first two.
2. Distinguish policy, standard, procedure, guideline with one AI example each.
3. Name three minimum fields of an AI inventory entry and the two hardest population challenges.
4. What makes a gate a genuine control rather than decoration?
5. An org has documented org-wide processes but no metrics on them. Maturity level, and what does the next level add?

<details>
<summary>Answers</summary>

1. Charter/mandate → inventory → tiering → policies/standards → gates → monitoring/assurance. Charter first because nothing binds without authority; inventory second because every control needs to know what exists.
2. Policy: "all AI use cases must be tiered and gated." Standard: "high-tier systems require disaggregated fairness testing." Procedure: "steps to submit intake requests." Guideline: "recommended prompt practices."
3. Fields (any three): owner, purpose/description, risk tier, data categories, model provenance, lifecycle/gate status, review dates. Challenges: shadow AI (unapproved tools) and AI embedded in purchased vendor software.
4. Defined evidence requirements, named approvers with real authority (refusals actually occur and are recorded), documented decisions/conditions, and escalation paths.
5. Level 3 (Defined); level 4 (Managed) adds quantitative measurement — KPIs, monitoring metrics, measured control performance.

</details>
