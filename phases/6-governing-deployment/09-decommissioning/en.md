# Decommissioning: Retirement, Data Disposition, User Migration

**Phase 6 · Lesson 09 · ~0.75h · BoK Domain IV**

## EXAM FOCUS

The lifecycle's forgotten stage — which is exactly why exams like it. Tested: what triggers retirement, why decommissioning is a governed project (not a switch-off), the tension between deletion duties and accountability archival, user/dependent-system migration, contract unwind with vendors, and lessons-learned capture. The trap answer is always some version of "just turn it off and delete everything."

## CORE

### Retirement triggers

| Trigger class | Examples |
|---|---|
| Performance | Irrecoverable drift/decay; retraining no longer viable (Lesson 04's end state) |
| Risk/compliance | System can't meet new legal requirements (e.g., a rule change reclassifies it); unacceptable residual risk found in audit or incident review |
| Business | Purpose ended; replaced by a successor system; vendor product sunset/deprecation |
| Technical | Unsupported dependencies; base model deprecated (the fourth-party event from Lesson 02) |

Retirement should also be *planned from the start*: readiness reviews (Lesson 01) and contracts (Lesson 03) that never contemplated exit produce hostage situations later. The AI inventory's periodic review is where zombie systems — running, unowned, unmonitored — get caught and queued for retirement.

### Decommissioning as a governed transition

Switching off a consequential AI system is itself a decision with impacts, so it passes through governance like any other gate (Phase 5 L01's final gate):

| Workstream | Content |
|---|---|
| **Decision & plan** | Documented retirement decision (owner, rationale, date), impact analysis of removal, timeline, rollback-of-the-rollout |
| **User & process migration** | Who/what depends on the outputs? Successor system, manual process, or sunset of the service; notice to users; parallel-run where decisions are consequential |
| **Dependent systems** | Downstream integrations consuming the model's outputs identified and re-pointed — the "hidden consumer" is the classic failure |
| **Data disposition** | Per retention schedule: delete what must be deleted (privacy), return/destroy vendor-held data, *retain* what accountability requires |
| **Model disposition** | Archive or destroy model artifacts deliberately; revoke access/keys; remove from serving infrastructure and registries (marked retired, not erased from history) |
| **Contract unwind** | Exercise exit clauses: data return/deletion certification, license termination, final audit rights, escrow release |
| **Records & inventory** | Update AI inventory (retired status, date, reason); preserve the accountability archive |
| **Lessons learned** | Retrospective feeding intake, testing, monitoring, and procurement practice |

### The archival tension

Two duties pull opposite ways:

- **Deletion:** privacy law's storage limitation — personal data goes when purposes end.
- **Accountability:** decisions the system made may be contested for years (litigation, regulator inquiries, audits); logs, model versions, documentation, and assessment records must survive long enough to explain and defend past decisions. (EU AI Act concept: providers keep technical documentation and related records available to authorities for a substantial period after the system's life — ten-year availability concepts attach to provider documentation.)

Resolution, as in Phase 5 L03: **schedule per artifact** — raw personal data on the shortest lawful clock; decision logs, model versions, documentation, and sign-off records retained for the defined accountability period, access-restricted and archived rather than live.

### In-flight decisions and people

Retirement must handle people mid-process: applications half-scored, cases queued on model outputs, users owed explanations about decisions the retired system made. The plan defines how in-flight items complete (successor, manual review) and how post-retirement explanation requests are answered — which is precisely why the archive keeps *which model version decided what* (lineage discipline to the very end).

## CASES & EXAMPLES

**Scenario 1 — the eager deletion.** A bank retires a credit model and deletes all model artifacts and logs "for data minimization." A year later, a discrimination claim arrives concerning that model's decisions; the bank cannot reconstruct what the model did. *Exam point:* accountability archival should have preserved decision logs, the model version, and documentation for the defensibility period — deletion duties apply to raw personal data, not to the evidence of governance.

**Scenario 2 — the hidden consumer.** A team switches off a legacy risk-scoring model; three weeks later, collections prioritization quietly breaks — it had been consuming the model's scores through an undocumented feed. *Exam point:* dependency mapping before switch-off; decommissioning is an impact-assessed transition, not an infrastructure task.

**Scenario 3 — vendor sunset.** A vendor announces end-of-life for the AI product embedded in a hospital's workflow, with 90 days' notice. *Exam point:* exit planning is a procurement-time control (transition assistance, data return with deletion certification, documentation handover for the accountability archive); scrambling at sunset means the contract failed, not just the timeline.

**Scenario 4 — zombie system.** An annual inventory review finds a five-year-old churn model still emailing scores to a distribution list with no owner, no monitoring, and an unknown training provenance. *Exam point:* orphaned systems are risk without accountability — the correct disposition is a fast-tracked retirement decision through governance, not silent continued operation.

## MEMORY HOOKS

**Retirement one-liner:** *End the system, not the accountability.*

**Decommission mnemonic — "MDCAL": Migrate users/dependents, Dispose data (per schedule), Contract unwind, Archive for accountability, Lessons learned.**

**Archival split:** *Delete the raw, keep the record* — personal data goes, decision evidence stays (for its defined period).

The 5 facts to retain:

1. Retirement triggers: irrecoverable performance decay, compliance infeasibility, business replacement/purpose end, vendor or dependency sunset — plus zombie systems caught by inventory review.
2. Decommissioning is a governed, impact-assessed transition: migration of users and dependent systems, deliberate data/model disposition, contract unwind, inventory update.
3. Deletion and accountability duties are reconciled per artifact: shortest lawful retention for raw personal data; decision logs, model versions, and documentation archived for the accountability period (provider documentation availability concepts run for years post-market).
4. Dependency mapping before switch-off prevents the "hidden consumer" failure; in-flight decisions get a defined completion path.
5. Every retirement ends with a lessons-learned retrospective feeding intake, contracting, and monitoring practice — closing the full lifecycle loop.

## SELF-CHECK

1. **Name four distinct classes of retirement trigger.**
   Performance (irrecoverable drift), risk/compliance (can't meet new requirements), business (replacement, purpose ended, vendor sunset), technical (unsupported dependencies/base-model deprecation).
2. **Why is "delete everything at retirement" wrong?**
   Contested decisions, litigation, audits, and regulator inquiries can arise years later; decision logs, model versions, and documentation must be archived for a defined accountability period — deletion applies on its own schedule to raw personal data.
3. **What must be mapped before a model is switched off, and why?**
   All downstream consumers of its outputs (systems, reports, processes) and its users — undocumented dependencies break silently when the feed stops.
4. **Which contract clauses (from procurement) get exercised at vendor-AI retirement?**
   Exit/portability: data return or certified deletion, transition assistance, license termination, documentation handover, escrow release, final audit rights.
5. **What happens to the AI inventory entry and the organization at large after decommissioning?**
   The entry is marked retired (date, reason, archive location) — never deleted — and a lessons-learned review feeds improvements back into intake, testing, procurement, and monitoring.
