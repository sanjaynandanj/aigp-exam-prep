# Procurement: Questions to Ask Before Buying AI

**Phase 6 · Lesson 03 · ~1h · BoK Domain IV**

## EXAM FOCUS

Procurement operationalizes vendor risk (Lesson 02) into RFP questions and contract clauses. The exam tests: what to ask *before* selection, which clauses belong in an AI contract (performance warranties, audit rights, data-use limits, IP/indemnity, incident-notification SLAs), and which assurance artifacts to demand as deliverables. Scenario stems often present a signed contract missing a key clause and ask what should have been negotiated.

## CORE

### Procurement as a governance gate

Buying AI *is* an intake + release decision about someone else's system. Well-run programs route AI purchases through the same pipeline: use-case intake and risk tiering first (Phase 5 L02), vendor due diligence (L02 here), then contract, then deployment readiness (L01). The biggest practical failure is **shadow procurement** — business units buying AI-embedded SaaS on credit cards, bypassing review entirely; the countermeasure is procurement-policy triggers ("any product with AI features routes to AI governance review") plus inventory sweeps.

### RFP questions that matter

| Theme | Ask |
|---|---|
| Fit & claims | What exactly does the AI do? What are its documented limitations and out-of-scope uses? |
| Provenance | Built in-house, licensed, or wrapped on a foundation model (which, what version)? Training-data sources and rights? |
| Evidence | Provide evaluation results (incl. subgroup breakdowns), robustness/red-team findings, bias-audit reports; will you support a proof-of-concept **on our data**? |
| Compliance | Your AI Act role and conformity status (if high-risk); privacy compliance; sectoral approvals |
| Data | Is customer data used for training (default? opt-out?); retention; residency; deletion on exit |
| Operations | Update cadence and notification; version pinning; monitoring hooks/logs we can access; explainability outputs |
| Assurance | SOC 2/ISO 27001/ISO 42001 status; third-party audits; documentation you will share (model card, instructions for use) |

Best practice: score responses against pre-set criteria tied to the risk tier — the same "acceptance criteria first" logic as testing (Phase 5 L05).

### The AI contract clause set

| Clause | What it must do |
|---|---|
| **Intended use & restrictions** | Bind both sides to the validated purpose; changes require agreement (protects your deployer position) |
| **Performance warranties** | Measurable commitments (accuracy/error bounds on defined data, uptime), remedies for breach — not marketing adjectives |
| **Data-use limits** | Your data: no training on it without explicit consent; confidentiality; residency; deletion/return on exit |
| **Audit & inspection rights** | Right to audit relevant controls/evidence (directly or via third party), receive audit summaries, and access documentation regulators may demand of you |
| **IP & indemnity** | Ownership of outputs and fine-tuned artifacts; indemnification for third-party IP claims over training data/outputs (a live GenAI issue — several major vendors now offer copyright indemnities; verify current status of any specific program) |
| **Change management** | Advance notice of material model changes; right to re-validate; version pinning where feasible |
| **Incident notification SLAs** | Defined timeframes to notify you of security/AI incidents affecting your use — sized so *you* can meet your own regulatory clocks (e.g., serious-incident reporting concepts, breach laws) |
| **Regulatory cooperation** | Vendor assists with regulator inquiries, conformity evidence, FRIA inputs |
| **Exit & portability** | Data return/deletion, transition assistance, escrow where justified |
| **Liability** | Caps and carve-outs matched to the harm the AI could cause — a $50k cap on a system making credit decisions is misaligned |

### Assurance artifacts to demand as deliverables

Make documentation contractual, not aspirational: model/system card, instructions for use, evaluation and bias-testing reports (refreshed on major versions), security-testing summaries, certifications kept current, and — for high-risk EU deployments — the provider documentation you need to discharge deployer duties. Public-sector buyers often must also satisfy AIA/transparency regimes (e.g., Canada's Directive on Automated Decision-Making applies to procured systems too).

## CASES & EXAMPLES

**Scenario 1 — the missing clock.** A vendor's model leaks personal data. Your regulator expects prompt reporting, but the contract has no incident-notification SLA and the vendor tells you three weeks later. *Exam point:* incident-notification SLAs must be negotiated up front and sized to your regulatory deadlines — after signature is too late.

**Scenario 2 — trained on your data.** A year in, you discover the vendor's default terms let it train shared models on your customer conversations. *Exam point:* data-use limits (no training without consent, or verified opt-out) are a core AI clause; "standard terms" silently permitting training is the classic trap.

**Scenario 3 — warranty of adjectives.** The contract warrants the tool is "highly accurate and state-of-the-art." Performance disappoints; legal finds nothing enforceable. *Exam point:* performance warranties must be measurable (metric + dataset/context + threshold + remedy), ideally anchored to a proof-of-concept on your data.

**Scenario 4 — audit dead-end.** A regulator asks the deployer for evidence about a high-risk vendor system; the vendor refuses, citing trade secrets, and the contract grants no audit or documentation rights. *Exam point:* audit/documentation-access rights exist precisely because the deployer carries regulatory exposure it can only discharge with vendor cooperation.

## MEMORY HOOKS

**Clause mnemonic — "WARranty DAICE": Warranties (measurable), Data-use limits, Audit rights, Incident SLAs, Change notice, Exit.** (IP/indemnity rides alongside as the GenAI-era addition.)

**Procurement rule:** *If you'll be accountable for it, contract for the evidence of it.*

**Shadow-procurement flag:** any SaaS "with AI features" = AI procurement, whatever the price tag.

The 5 facts to retain:

1. AI procurement runs through the governance pipeline: intake/risk tier → due diligence → contract → deployment readiness; AI-embedded SaaS counts.
2. RFPs must extract provenance (base model, training data), model-level evidence (ideally a PoC on your data), and compliance posture — scored against pre-set criteria.
3. The core AI clause set: measurable performance warranties, data-use limits (no training on your data without consent), audit/documentation rights, change notification with re-validation rights, incident-notification SLAs, IP/indemnity, exit terms.
4. Incident SLAs must be shorter than your own regulatory reporting clocks — you can't report what you haven't been told.
5. Assurance artifacts (cards, evaluation reports, certifications, instructions for use) should be contractual deliverables refreshed with each major version.

## SELF-CHECK

1. **Why must AI purchases go through use-case intake even though the system is vendor-built?**
   Risk tiering, ban-list screening, and necessity analysis depend on the *use*, not on who built it — and the buyer will hold deployer accountability.
2. **What makes a performance warranty enforceable?**
   A defined metric, threshold, and evaluation context/dataset, plus a remedy for breach — measurable commitments, not qualitative claims.
3. **Name three data-use limits an AI contract should impose on the vendor.**
   No training on customer data without explicit consent/opt-in; retention/residency restrictions; deletion or return of data (and derived artifacts) on exit.
4. **Why do deployers need audit and documentation-access rights against AI vendors?**
   Deployers carry regulatory duties (oversight, monitoring, responding to authorities) they can only evidence with vendor cooperation; without contractual rights, trade-secret refusals leave the deployer exposed.
5. **How should an incident-notification SLA be sized?**
   Shorter than the buyer's own regulatory notification deadlines (serious-incident, breach, sectoral rules), with severity definitions and named contact channels.
