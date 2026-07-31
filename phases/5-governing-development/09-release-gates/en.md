# Release Gates & Go/No-Go Decisions: Who Signs, On What Evidence

**Phase 5 · Lesson 09 · ~1h · BoK Domain III**

## EXAM FOCUS

The release gate is where Domain III's development controls converge into one accountable decision. Exam angles: who sits on a go/no-go review, what belongs in the evidence bundle, why sign-off must be individual and documented, staged approvals for higher-risk systems, and how exceptions/risk acceptance work without becoming rubber stamps. Scenario stems often present a launch under commercial pressure and ask what a defensible process requires.

## CORE

### What a release gate is

A **release gate** is the formal checkpoint between "tested" and "live": a structured review that verifies the evidence, weighs residual risk, and produces a documented go / no-go / go-with-conditions decision by people with authority to stop the launch. Its purpose is to make someone *accountable by name* for the decision to expose real people to the system.

### Composition of the go/no-go review

| Seat | Brings | Typical veto/escalation power |
|---|---|---|
| Business/product owner | Purpose, benefit case, launch conditions | Owns the request |
| Technical/ML lead | Test results, limitations, honest uncertainty | Flags unmet criteria |
| AI governance / risk lead | Policy compliance, risk-tier requirements, assessment status | Can block or escalate |
| Privacy (DPO where applicable) | DPIA status, data-protection conditions | Can block on privacy grounds |
| Security | Threat findings, red-team results | Can block on security grounds |
| Legal/compliance | Regulatory posture (conformity, sectoral rules) | Can block on legal grounds |
| Independent chair (higher tiers) | Neutrality; ensures challenge happens | Casts/records the decision |

Design principle: **separation of build and approve** — those who built the system should present evidence but not approve their own work; independence scales with risk tier.

### The evidence bundle

The gate reviews artifacts, not vibes. A defensible bundle for a higher-risk system:

| Category | Artifacts (lessons where built) |
|---|---|
| Intent & scope | Approved intake, risk tier, intended-use statement (L02) |
| Data | Datasheets, provenance/lawful-basis records (L03) |
| Build | Model version + lineage triangle, training records (L04) |
| Evaluation | Test results **vs pre-set acceptance criteria**, fairness/robustness/red-team reports (L05) |
| Assessments | DPIA/FRIA/AIA as triggered; conformity status where applicable (L06) |
| Documentation | Model/system card, instructions for use, technical documentation status (L07) |
| Security | Threat model, adversarial-testing results, supply-chain checks (L08) |
| Operations readiness | Monitoring plan, oversight design, incident runbook, rollback plan (Phase 6 previews) |

### Sign-off, staged approvals, and conditions

- **Sign-off is individual and recorded:** name, role, date, evidence version reviewed, decision, rationale. "The committee approved" without a record fails audit.
- **Staged approvals:** higher tiers may require sequential sign-offs (technical → governance → executive), and a "go" may be scoped — e.g., approve only a limited pilot/shadow deployment (Phase 6, Lesson 01), with full launch requiring a second gate after pilot evidence.
- **Go-with-conditions:** approval bound to conditions (e.g., human review of all adverse decisions for 90 days, weekly drift reports). Conditions must be tracked to closure — untracked conditions are the classic audit finding.

### Exceptions and risk acceptance

Sometimes a system fails a criterion and the business still wants to launch. A governed path exists:

1. The gap is documented precisely (which criterion, by how much, whose risk).
2. Mitigations/compensating controls are specified.
3. **Risk acceptance is signed by someone senior enough to own the consequence** — at the level the risk-appetite framework requires, never by the project team itself.
4. The exception is time-bound, logged in an exception register, and revisited.

Anti-patterns the exam punishes: retro-fitting acceptance criteria to match results; deadline-driven "conditional" approvals with conditions nobody tracks; exception-by-default cultures; approvals by the builders themselves.

## CASES & EXAMPLES

**Scenario 1 — pressure launch.** Marketing has announced a launch date; testing shows the model misses its subgroup-fairness threshold. The VP says "ship it, we'll fix it live." *Best answer:* the gate issues no-go or a formal, senior, time-bound risk acceptance with compensating controls — not silent shipping. The announced date is irrelevant to the evidence.

**Scenario 2 — who approves?** The lead ML engineer who built the model proposes to sign the release himself since "he knows it best." *Exam point:* separation of duties — builders present evidence; approval belongs to reviewers independent of the build, with independence scaling by risk.

**Scenario 3 — conditions vanish.** A credit model was approved "on condition of manual review of all declines for 60 days." Nobody implemented the reviews. An audit later flags it. *Exam point:* go-with-conditions requires tracking conditions to closure with an owner and due date — otherwise the approval itself is invalid evidence.

**Scenario 4 — staged go.** A hospital's triage assistant gets gate approval *only* for a 3-site shadow deployment with clinician review; full rollout requires a second gate reviewing shadow-phase results. *Exam point:* staged approval is the correct pattern for high-risk novel systems — expanding scope is itself a gated decision.

## MEMORY HOOKS

**Gate formula:** *Evidence bundle + independent challenge + named sign-off = defensible release.*

**Mnemonic — the 4 gate outcomes "G-C-N-E": Go, go-with-Conditions, No-go, Exception (senior risk acceptance).**

**Anti-rubber-stamp rule:** *Whoever built it doesn't bless it; whoever accepts the risk must be able to afford it.*

The 5 facts to retain:

1. A release gate is a formal go/no-go decision point between testing and deployment, with authority to stop launch.
2. The review is cross-functional (product, technical, governance, privacy, security, legal) with build/approve separation.
3. Decisions rest on an evidence bundle: intake + data + training + evaluation + assessments + documentation + security + operational readiness.
4. Sign-off is individual, documented, and may be staged/scoped (pilot first, second gate for full rollout); conditions must be tracked to closure.
5. Failing a criterion permits launch only via formal, senior, time-bound risk acceptance recorded in an exception register — never informal override.

## SELF-CHECK

1. **What three ingredients make a release decision defensible?**
   A complete evidence bundle, independent (non-builder) challenge/review, and a named, documented, accountable sign-off.
2. **Why shouldn't the development team approve its own release?**
   Separation of duties — self-approval removes challenge and biases the decision; builders present evidence, independent reviewers decide.
3. **List five categories in a release evidence bundle.**
   Any five of: approved intake/risk tier; data provenance/datasheets; training records/model lineage; test results vs acceptance criteria (incl. fairness/robustness/red team); impact assessments; documentation artifacts; security testing; operational readiness (monitoring, oversight, rollback).
4. **What must accompany a "go-with-conditions" decision to keep it valid?**
   Each condition needs an owner, a deadline, and tracking to documented closure — plus consequences (e.g., rollback) if unmet.
5. **A system misses an acceptance criterion but leadership wants to launch. What is the governed path?**
   Document the gap, define compensating controls, obtain time-bound risk acceptance signed at the seniority level the risk-appetite framework requires, register the exception, and set a review date.
