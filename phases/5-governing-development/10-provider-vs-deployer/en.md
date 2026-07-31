# Provider vs Deployer: How Obligations Shift Across Build, Buy, Fine-Tune

**Phase 5 · Lesson 10 · ~0.75h · BoK Domain III**

## EXAM FOCUS

Provider/deployer role confusion is one of the exam's most reliable distractor patterns. You must be able to: classify an organization's role for a given system, list which obligations follow each role (EU AI Act concept level), and — the advanced twist — recognize when a *deployer becomes a provider* through substantial modification, rebranding (white-labeling), or repurposing. Build vs buy vs fine-tune scenarios are the natural stem format.

## CORE

### The roles (EU AI Act framing)

| Role | Definition (concept) | Center of gravity |
|---|---|---|
| **Provider** | Develops an AI system (or has it developed) and places it on the market / puts it into service **under its own name or trademark** | Pre-market: design, testing, documentation, conformity |
| **Deployer** | Uses an AI system **under its own authority** in a professional context (not personal, non-professional use) | In-use: proper operation, oversight, monitoring |
| Importer / distributor | Bring a third-country provider's system to the EU market / make it available | Verification of provider compliance (Phase 4 coverage) |

### Obligation split for high-risk systems (concept level)

| Provider obligations | Deployer obligations |
|---|---|
| Risk-management system across lifecycle | Use per the provider's **instructions for use** |
| Data governance for training/validation/testing | Assign competent **human oversight** (Art. 14/26 concepts) |
| Technical documentation (Annex IV concept) + logging capability | Ensure relevant, representative **input data** under its control |
| Accuracy, robustness, cybersecurity | **Monitor** operation; suspend & inform provider on suspected risk |
| Conformity assessment, declaration, CE marking, registration | Retain **logs** under its control; cooperate with authorities |
| Post-market monitoring & serious-incident reporting (Art. 73 concept) | Inform affected workers/persons where required; FRIA where in scope (Art. 27 concept) |

Memory shape: **providers make it safe to sell; deployers keep it safe to use.**

### Becoming a provider: the reclassification triggers

A deployer (or distributor/importer) is treated as the provider of a high-risk system when it:

1. **Puts its name or trademark** on a high-risk system already on the market (rebranding/white-labeling);
2. Makes a **substantial modification** to a high-risk system (a change affecting compliance or intended purpose beyond what the provider foresaw); or
3. **Modifies the intended purpose** of a system (including a non-high-risk or GPAI system) such that it *becomes* high-risk.

Consequence: the full provider obligation set (documentation, conformity assessment, registration) lands on the new provider; the original provider must cooperate by supplying information (concept level).

### Build vs buy vs fine-tune

| Posture | Likely role | Governance implications |
|---|---|---|
| **Build in-house** and use internally | Provider *and* deployer (putting into service under own name) | Full stack of both obligation sets — no vendor to lean on |
| **Buy/license** and use as instructed | Deployer | Due diligence on provider docs (Phase 6 L02–03); operate within intended purpose; oversight, monitoring, logs |
| **Buy and rebrand** under own trademark | Provider (by reclassification) | Inherits provider duties — a commonly missed consequence of white-labeling |
| **Fine-tune / substantially modify** a third-party or GPAI model into a high-risk use | Likely provider for the resulting system (fact-dependent) | Role analysis required; keep fine-tune records (Lesson 04); verify current status of guidance on when modification of GPAI models creates provider duties |
| **Use GPAI via API** inside your own high-risk product under your name | Provider of the high-risk system (deployer of nothing — you built the product) | Upstream GPAI provider has GPAI transparency/documentation duties to you; you carry high-risk duties downstream |

The role is assessed **per AI system, per use** — one company can be provider of System A, deployer of System B, and both for System C.

## CASES & EXAMPLES

**Scenario 1 — the classic swap.** A logistics firm licenses a vendor's high-risk worker-scheduling AI and uses it unchanged, per the manual. Who runs conformity assessment? *Answer:* the vendor (provider). The firm, as deployer, must ensure oversight, appropriate input data, monitoring, and log retention. Distractor: assigning conformity assessment to the deployer.

**Scenario 2 — white-label trap.** An HR-tech reseller takes a third party's CV-screening engine, puts its own brand on it, and sells it to EU customers. *Answer:* by affixing its trademark to a high-risk system, the reseller **becomes the provider** and owns technical documentation, conformity assessment, and registration. "It's really the upstream developer's problem" is the trap answer.

**Scenario 3 — repurposing into high risk.** A company licenses a general document-summarization model and integrates it to auto-score job applications under its own name. *Answer:* it has created/placed into service a high-risk system — provider duties attach to it for that system; the upstream model vendor's role depends on what it placed on the market.

**Scenario 4 — both hats.** A bank builds its own credit-scoring model and uses it internally. *Answer:* the bank is provider (developed it, put it into service under its own name) *and* deployer (uses it under its authority) — it owes both obligation sets. Exam stems love organizations wearing both hats.

## MEMORY HOOKS

**Role one-liner:** *Provider = whose name is on it when it hits the market; Deployer = who uses it on people.*

**Reclassification triggers — "Name, Change, Aim":** put your **Name** on it, substantially **Change** it, or change its **Aim** into high-risk → you're the provider now.

**Obligation split:** *Providers: make it compliant. Deployers: keep it compliant in use.*

The 5 facts to retain:

1. Provider = develops and places on market/into service under own name; deployer = uses under own authority professionally.
2. Providers own pre-market duties (risk management, data governance, technical documentation, conformity, CE, registration, post-market monitoring); deployers own use-stage duties (instructions, oversight, input data, monitoring, logs, cooperation, FRIA where in scope).
3. Rebranding, substantial modification, or repurposing into high-risk converts a deployer/distributor into a provider with the full duty set.
4. Building for internal use makes you both provider and deployer — both obligation sets apply.
5. Roles are assessed per system and per use; fine-tuning scenarios need a documented role analysis (and verify current status of GPAI-modification guidance).

## SELF-CHECK

1. **Define provider and deployer in one sentence each.**
   Provider: develops an AI system (or has it developed) and places it on the market or puts it into service under its own name/trademark. Deployer: uses an AI system under its own authority in a professional capacity.
2. **Name the three triggers by which a deployer/distributor becomes a provider of a high-risk system.**
   Affixing its own name/trademark; making a substantial modification; modifying the intended purpose so the system becomes (or is used as) high-risk.
3. **Which actor performs the conformity assessment, and which performs the FRIA (where triggered)?**
   Conformity assessment: provider. FRIA (Art. 27 concept): deployer (public bodies/public services and specified private uses).
4. **A company builds an AI tool purely for internal HR use. What roles does it hold?**
   Both provider (put into service under its own name) and deployer (uses it under its authority) — it must satisfy both obligation sets.
5. **List four deployer obligations for a high-risk system.**
   Any four of: use per instructions for use; assign competent human oversight; ensure relevant/representative input data it controls; monitor operation and suspend/report on risk; retain logs under its control; inform affected persons/workers; conduct a FRIA where in scope; cooperate with authorities.
