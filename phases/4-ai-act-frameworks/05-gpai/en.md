# GPAI & Foundation Models: Tiers, Systemic Risk, the Code of Practice

**Phase 4 · Lesson 05 · ~1.5h · BoK Domain II**

## EXAM FOCUS

The GPAI chapter is the Act's answer to foundation models, bolted on late in negotiations and structured as a **two-tier regime**: baseline duties for **all GPAI model providers**, plus an extra layer for models with **systemic risk**. Applicable since **2 August 2025**. Test points: the model-vs-system distinction, the four baseline duties, the compute-threshold concept, systemic-risk duties, the open-source carve-out and its limits, and the **Code of Practice** as the compliance vehicle.

## CORE

### Model vs system — the foundational distinction

| Concept | Definition essence | Regime |
|---|---|---|
| **GPAI model** | An AI **model** (incl. those trained with large amounts of data using self-supervision at scale) displaying **significant generality**, competently performing a **wide range of distinct tasks**, integratable into downstream systems (excludes pure pre-market R&D models) | GPAI chapter (Arts. 51–56 territory) |
| **GPAI system** | An AI **system** based on a GPAI model | System-level rules: could be high-risk (if used in an Annex III context), transparency-tier, etc. |

One model can power thousands of systems; obligations attach to the **model provider** upstream and to system providers/deployers downstream. A downstream company that fine-tunes or substantially modifies a GPAI model can become a GPAI **model provider** for the modification (Commission guidance scopes duties to the modification).

### Tier 1 — duties of ALL GPAI model providers

| Duty | Content |
|---|---|
| **Technical documentation** | For the AI Office/national authorities: training and testing process, evaluation results (Annex XI concept) |
| **Information to downstream providers** | Documentation enabling integrators to understand capabilities/limitations and meet their own obligations (Annex XII concept) |
| **Copyright policy** | A policy to comply with EU copyright law, in particular to **identify and honor TDM opt-outs** (DSM Art. 4 rights reservations) — applies regardless of where training occurred |
| **Training-content summary** | Publish a **sufficiently detailed summary of training content**, using the AI Office's template |

Non-EU GPAI providers must appoint an EU **authorized representative**.

### The open-source carve-out (partial!)

Providers of models released under a **free and open-source licence** — with **weights, architecture and usage information publicly available** — are exempt from the technical-documentation and downstream-information duties, **but NOT from** the copyright policy and training-content summary. And the carve-out **evaporates entirely for systemic-risk models**. Monetized "open" models don't qualify.

### Tier 2 — GPAI models with systemic risk

**Classification triggers:**
- **High-impact capabilities** presumed when cumulative training compute exceeds **10^25 FLOPs** (floating-point operations) — a threshold the Commission can update as technology moves; or
- Commission designation (own initiative or scientific-panel alert) based on criteria (parameters, dataset size, users, capabilities, reach).

**Procedural duty:** providers must **notify the Commission without delay (within two weeks)** of meeting/expecting to meet the threshold; they may argue the model nonetheless lacks systemic risk.

**Additional duties for systemic-risk models:**
1. **Model evaluations** — state-of-the-art protocols, including **adversarial testing / red-teaming**;
2. **Systemic-risk assessment and mitigation** at Union level (misuse, loss of control, CBRN-uplift-type concerns per the risk taxonomy);
3. **Serious-incident tracking and reporting** to the AI Office (and national authorities) without undue delay, with corrective measures;
4. **Adequate cybersecurity protection** for the model **and its physical infrastructure** (protecting unreleased weights is the paradigm case).

### The Code of Practice & compliance presumptions

- The **GPAI Code of Practice** (published 2025; chapters on **Transparency, Copyright, Safety & Security**) is a **voluntary instrument** drawn up via AI Office-facilitated multi-stakeholder process: adhering signatories get a streamlined way to **demonstrate compliance** (reduced administrative burden, enforcement goodwill) until harmonized standards exist.
- Non-signatories must prove compliance by **alternative adequate means** — the Code is not mandatory, but it is the practical benchmark.
- Compliance ecosystem completed by Commission **guidelines on GPAI obligations** and the **training-content-summary template**.
- Enforcement of GPAI duties sits with the **AI Office** (exclusive supervisor for GPAI model providers); fines up to **3% of global turnover or €15M** for GPAI-specific violations. Timing nuance: rules applied from Aug 2025 for new models; models already on the market before Aug 2025 have until **Aug 2027** to comply.

### How GPAI meets the high-risk regime

- GPAI **model** duties ≠ high-risk **system** duties. If a GPAI-based system is deployed for an Annex III purpose (e.g., an LLM screening job applications), the **system** must meet the full high-risk requirements — the model documentation flows up the chain to make that possible.
- Transparency-tier duties also commonly ride along: chatbot disclosure, synthetic-content marking (machine-readable), deepfake labeling.

## CASES & EXAMPLES

**Scenario 1 — The threshold crosser.** A lab's next training run is projected at 3×10^25 FLOPs. *Analysis:* Presumption of high-impact capabilities → notify the Commission within two weeks (can argue against systemic-risk classification); on release, full Tier 2 stack: adversarial evaluations, systemic-risk mitigation, incident reporting, cybersecurity for weights — plus all Tier 1 duties. Signing the Code of Practice is the low-friction compliance route.

**Scenario 2 — Open-source, but…** A company releases model weights under a genuine open licence; the model was trained on ~10^24 FLOPs. It publishes nothing about training data and has no copyright policy. *Analysis:* The open-source carve-out excuses technical-documentation/downstream-information duties, but the **copyright policy and training-content summary still apply** — it is in breach of those two. If it later crosses the systemic-risk line, the carve-out disappears entirely.

**Scenario 3 — The fine-tuner.** An EU HR-tech firm fine-tunes an open foundation model on hiring data and sells "TalentRank." *Analysis:* Three hats: (1) possible GPAI-model-provider duties **scoped to the modification** (per Commission guidance); (2) provider of a **high-risk system** (employment) → full Chapter III compliance; (3) transparency duties toward candidates. Upstream model documentation is its lifeline for technical-documentation content — this is why Tier 1 information duties exist.

**Scenario 4 — Legacy model.** A GPAI model has been on the EU market since 2024. *Analysis:* GPAI obligations applied from Aug 2025 to *new* placements; pre-existing models get until **Aug 2027** — but any significant new version/placement restarts the analysis. (Status as of mid-2026 — verify transition specifics.)

## MEMORY HOOKS

- **Tier 1 duties — "DICT":** **D**ocumentation (technical), **I**nformation (downstream), **C**opyright policy, **T**raining-content summary. *All GPAI providers speak DICT.*
- **Tier 2 add-ons — "ERIC":** **E**valuations (adversarial), **R**isk assessment/mitigation (systemic), **I**ncident reporting, **C**ybersecurity. *Systemic risk? Call ERIC.*
- **The magic number:** **10^25 FLOPs** — presumption line for systemic risk; **2 weeks** to notify; the Commission can move the line.
- **Open-source rule of thumb:** *open weights skip the paperwork to others, never the copyright duties — and systemic risk cancels all discounts.*
- **Model upstream, system downstream:** GPAI chapter regulates the *engine*; high-risk chapter regulates the *vehicle* it's put into.

**The 5 facts to retain:**
1. GPAI = model with significant generality across tasks; regulated separately from (and cumulatively with) the system-level risk tiers; applicable since **Aug 2025**.
2. All GPAI providers owe DICT: technical docs, downstream info, EU-copyright/TDM-opt-out policy, published training-content summary.
3. Systemic-risk tier presumed at >10^25 FLOPs training compute (or Commission designation); notification within two weeks; duties add evaluations/red-teaming, systemic-risk mitigation, incident reporting, cybersecurity.
4. Open-source carve-out is partial (docs/info only) and void for systemic-risk models.
5. The voluntary **Code of Practice** (transparency, copyright, safety & security) is the practical path to demonstrating compliance; the **AI Office** is the exclusive GPAI enforcer (3%/€15M tier).

## SELF-CHECK

1. **Q:** Distinguish a GPAI model from a GPAI system and explain why the distinction matters.
   **A:** The model is the trained artifact with significant generality; the system is an application built on it. Duties differ: model providers owe the GPAI chapter (DICT + systemic tier); system providers/deployers owe the risk-pyramid duties (high-risk, transparency) for the use case.

2. **Q:** Which two Tier 1 duties survive the open-source carve-out?
   **A:** The copyright-compliance policy (honoring TDM opt-outs) and the public training-content summary.

3. **Q:** What triggers the systemic-risk presumption, and what must the provider then do procedurally?
   **A:** Cumulative training compute above 10^25 FLOPs (or Commission designation). The provider must notify the Commission without delay — within two weeks of meeting or foreseeing the threshold — and may present arguments that the model doesn't pose systemic risk.

4. **Q:** List the four additional obligations of systemic-risk GPAI providers.
   **A:** State-of-the-art model evaluations including adversarial testing; assessment and mitigation of systemic risks at Union level; tracking and reporting serious incidents with corrective measures; adequate cybersecurity for model and infrastructure.

5. **Q:** Is signing the GPAI Code of Practice mandatory? What's the benefit?
   **A:** No — it's voluntary. Signatories gain a recognized, streamlined means of demonstrating compliance (a de facto presumption route with lower administrative burden) until harmonized standards arrive; non-signatories must demonstrate equivalent compliance by other adequate means.
