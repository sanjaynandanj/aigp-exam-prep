# Deployment Readiness: Checklists, Staged Rollouts, Shadow Deployment

**Phase 6 · Lesson 01 · ~1h · BoK Domain IV**

## EXAM FOCUS

Domain IV opens where the release gate ended: the system is approved — now deploy it *safely*. Tested concepts: the readiness checklist, the rollout spectrum (shadow → pilot → staged/canary → full), what shadow deployment uniquely offers, governance of A/B tests on real users, rollback planning, and re-assessing when deployment context differs from the context the system was validated in. Scenario stems typically ask for the *most cautious appropriate* rollout pattern.

## CORE

### The readiness checklist

Deployment readiness verifies that everything the *operating* phase needs exists **before** exposure to real users:

| Readiness domain | Verify |
|---|---|
| Approval | Release-gate decision current; conditions implemented; scope of approval matches planned rollout |
| Monitoring | Metrics, dashboards, alert thresholds live (Lesson 04); logging enabled and retained |
| Oversight | Human-oversight roles staffed and trained (Lesson 05); override mechanisms working |
| Transparency | User notices/labels in place (Lesson 06) |
| Incident response | Runbook, on-call ownership, escalation paths tested (Lesson 07) |
| Rollback | A tested way to revert to the previous system/process within a defined time |
| Context | Deployment population/environment matches what was validated — else re-assess |

### The rollout spectrum

| Pattern | What it is | Real-user impact | Best for |
|---|---|---|---|
| **Shadow deployment** | New system runs on live inputs in parallel; outputs are **recorded but not acted on**; incumbent still decides | None | Highest-risk or novel systems; validating real-world performance safely |
| **Pilot** | Limited scope (sites, users, geography) with full effect | Small, bounded | Testing operational fit, oversight workload |
| **Staged / canary rollout** | Gradually increasing traffic share (e.g., 5% → 25% → 100%) with health checks between stages | Growing, controlled | Most production systems |
| **A/B test** | Users randomly split between variants; outcomes compared | Real, randomized | Comparing variants — needs its own governance (below) |
| **Big-bang** | Everyone at once | Total | Low-risk systems only; usually the wrong exam answer |

Shadow deployment's unique value: it is the only pattern that yields **real-world evidence with zero user consequences** — the bridge between offline test results and live operation. Its limits: it can't measure effects that depend on the system's outputs being acted on (feedback effects, user behavior).

### A/B testing governance

Experimenting on real users is not governance-free: define hypothesis and stopping rules up front; cap exposure and duration; exclude vulnerable contexts where randomization itself harms (e.g., withholding a safety feature); consider whether the experiment needs consent/notice or ethics review — consequential-decision contexts (credit, health, employment) demand far more caution than UI tweaks.

### Rollback plans

Every deployment needs a pre-tested answer to "how do we turn this off?": what triggers rollback (thresholds, incident severities), who has authority to pull it (including out-of-hours), what users fall back *to* (previous model, manual process), and how long reversion takes. A rollback that has never been rehearsed is a hypothesis, not a plan.

### Deployment-context re-assessment

Validation evidence is context-bound. Re-assessment is required when the deployment context shifts from the validated one: new population (different demographics, language, geography), new domain, new integration (outputs now feed another system), or new scale. Rule: **a model validated *there* is not validated *here*.** This is also the deployer's duty angle — deployers must ensure input data and use context match the provider's intended purpose (Art. 26 concept).

## CASES & EXAMPLES

**Scenario 1 — choose the pattern.** A hospital network will introduce an AI sepsis-alert system, its first clinical AI. Safest first step? *Answer:* shadow deployment — run on live patient data, record alerts, clinicians never see or act on them; compare against outcomes. Distractors: pilot with live alerts (premature), A/B test (randomizing a safety alert raises ethical problems), full rollout.

**Scenario 2 — context shift.** A US-validated résumé screener is switched on for the German subsidiary. Performance drops; German-language CVs and different career-path norms weren't in validation data. *Failed control:* deployment-context re-assessment before extending to a new population. "The model passed testing" is the trap — it passed *elsewhere*.

**Scenario 3 — the untested rollback.** A canary release of a pricing model misbehaves at 25% traffic; the team discovers the "rollback" requires a 6-hour rebuild because the old model was deleted. *Exam point:* rollback must be pre-tested with a defined reversion time and a preserved fallback (previous model version — link to model registry, Phase 5 L04).

**Scenario 4 — A/B overreach.** A lender wants to A/B test two credit-decision models on live applicants without notice. *Exam point:* randomized experiments on consequential decisions require governance review — fairness between arms, legal notice obligations, and pre-set stopping rules; "just ship both and compare" is the wrong answer.

## MEMORY HOOKS

**Rollout ladder — "SPSAB": Shadow → Pilot → Staged → (A/B where justified) → Big-bang (rarely).** Exam heuristic: the higher the risk, the lower you start on the ladder.

**Shadow one-liner:** *real inputs, recorded outputs, zero consequences.*

**Context rule:** *Validated there ≠ valid here.*

The 5 facts to retain:

1. Readiness = release approval **plus** live monitoring, staffed oversight, user transparency, incident runbook, and a tested rollback — verified before exposure.
2. Shadow deployment runs on live data without acting on outputs — the safest bridge from testing to production for high-risk systems.
3. Staged/canary rollouts expand traffic gradually with health checks between stages; big-bang is for low-risk only.
4. A/B tests on real users need governance: pre-set hypotheses/stopping rules, exposure caps, and heightened care in consequential-decision contexts.
5. Any material change in deployment context (population, language, domain, integration, scale) invalidates prior validation and triggers re-assessment.

## SELF-CHECK

1. **What distinguishes shadow deployment from a pilot?**
   Shadow: outputs are recorded but never acted on — no user impact. Pilot: the system operates with real effect on a limited scope.
2. **Name five items on a deployment-readiness checklist beyond the release approval itself.**
   Live monitoring/alerting and logging; staffed and trained human oversight; user transparency notices; incident-response runbook with ownership; tested rollback plan (also: context match verification).
3. **What can a shadow deployment *not* tell you?**
   Effects that depend on outputs being acted upon — user behavior changes, feedback loops, downstream operational impacts.
4. **What must be defined before starting an A/B test of an AI system on real users?**
   Hypothesis, success metrics, stopping rules, exposure caps/duration, and whether notice/consent or ethics review is required given the decision's consequences.
5. **Give three context changes that should trigger re-assessment before deployment.**
   New population/demographics or language, new domain or purpose, new integration or scale (outputs feeding other systems, order-of-magnitude volume growth).
