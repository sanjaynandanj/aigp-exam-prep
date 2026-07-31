# ISO/IEC 42001 (AIMS) & 23894 (AI Risk): Certifiable AI Management

**Phase 4 · Lesson 09 · ~1h · BoK Domain II**

## EXAM FOCUS

Two standards, two jobs: **ISO/IEC 42001** is a **certifiable management-system standard** (the "ISO 27001 of AI"), while **ISO/IEC 23894** is **risk-management guidance** built on ISO 31000. The exam tests: what an AIMS is, the PDCA logic, the role of Annex A controls, what certification does and doesn't prove, how 23894's process differs from 42001, and how both complement the NIST AI RMF. Secondary standards (ISO 5338, 22989, 42005, IEEE 7000) appear at recognition level.

## CORE

### ISO/IEC 42001:2023 — the AI Management System (AIMS) standard

| Attribute | Value |
|---|---|
| What | Requirements for establishing, implementing, maintaining and **continually improving an AI Management System** — the first certifiable AI MSS |
| Who | Any organization developing, providing, **or using** AI — any size/sector |
| Family traits | Uses the ISO **harmonized structure** (same 10-clause skeleton as ISO 27001/9001) → integrates with existing ISMS/QMS; third-party **certification** available (accredited via ISO/IEC 42006 for cert bodies) |
| Engine | **PDCA — Plan, Do, Check, Act** continual improvement |

**The 10-clause skeleton (clauses 4–10 are the auditable requirements):**

| Clause | Theme | AI flavor |
|---|---|---|
| 4 | **Context** | Internal/external issues, interested parties, determine the organization's **role(s)** (developer, provider, user), AIMS scope |
| 5 | **Leadership** | Top-management commitment, **AI policy**, roles/responsibilities/authorities |
| 6 | **Planning** | Risk & opportunity treatment: **AI risk assessment, AI risk treatment, AI system impact assessment**, objectives |
| 7 | **Support** | Resources, **competence**, awareness, communication, documented information |
| 8 | **Operation** | Operational planning/control; performing the risk and **impact assessments** in practice; change control |
| 9 | **Performance evaluation** | Monitoring/measurement, **internal audit**, management review |
| 10 | **Improvement** | Nonconformity/corrective action, continual improvement |

**Annex A controls (the concept, not the memorized list):** a reference set of **~38 controls in 9 themes** — AI policies; internal organization; **resources for AI systems** (data, tooling, compute, people); **assessing impacts** on individuals/groups/society; **AI system lifecycle** (requirements, design, verification, deployment, operation/monitoring); **data for AI** (provenance, quality, preparation); **information for interested parties** (transparency, reporting); **use of AI systems** (responsible-use objectives, intended use); **third-party and customer relationships**. Like ISO 27001: organizations select applicable controls via risk treatment and justify choices in a **Statement of Applicability**; Annex B gives implementation guidance.

**Distinctive 42001 requirement to remember:** the **AI system impact assessment** — assessing consequences for individuals, groups, and societies (not just organizational risk) — this outward-facing assessment is what makes 42001 more than a rebadged quality standard.

**What certification proves / doesn't:** an accredited certificate attests the *management system* conforms — governance processes exist and operate. It does **not** certify that any particular model is safe, fair, accurate, or legally compliant. (Exam distractor: "ISO 42001 certification demonstrates the chatbot is unbiased" — false.)

### ISO/IEC 23894:2023 — AI risk-management guidance

| Attribute | Value |
|---|---|
| What | **Guidance** (not certifiable, no "shall" requirements) on managing AI-related risk, **built directly on ISO 31000:2018** — adapting the generic risk vocabulary to AI |
| Structure | Mirrors 31000: **principles** (risk management creates/protects value, integrated, customized, inclusive, dynamic…) → **framework** (leadership & commitment, integration, design, implementation, evaluation, improvement) → **process** |
| The process loop | **Scope/context/criteria → risk assessment (identification → analysis → evaluation) → risk treatment → recording & reporting**, wrapped in *communication & consultation* and *monitoring & review* |
| AI-specific value-add | Annexes mapping AI-specific **risk sources** (data quality, ML complexity, automation level, opacity, environment complexity…), objectives (fairness, safety, transparency…), and where in the AI lifecycle each process step lands |
| Relationship to 42001 | 42001 clause 6 *requires* risk assessment/treatment; 23894 tells you *how* to run it well — guidance inside the certified shell |

### How they complement the NIST AI RMF

| Dimension | NIST AI RMF | ISO/IEC 42001 | ISO/IEC 23894 |
|---|---|---|---|
| Type | Voluntary framework (functions/outcomes) | Certifiable requirements (management system) | Voluntary guidance (risk process) |
| Center of gravity | What outcomes good AI risk practice achieves | What the *organization* must institutionalize | How the *risk process* runs |
| Assurance | Self-attestation/profiles | **Third-party audit & certificate** | None |
| Rough mapping | GOVERN ≈ clauses 4–7 + 10; MAP/MEASURE/MANAGE ≈ clauses 6/8/9 + Annex A lifecycle controls; crosswalks published | | RMF MAP/MEASURE/MANAGE ≈ 31000 assessment/treatment loop |
| Legal hooks | Colorado presumption; US practice | Colorado presumption; candidate support for **EU AI Act** QMS/risk-management evidence (harmonized-standard work draws on it); procurement demands | Feeds both |

### Other standards — mention level

- **ISO/IEC 22989** — AI concepts & terminology (the vocabulary base).
- **ISO/IEC 5338** — AI system **lifecycle processes** (extends ISO 15288 software lifecycle to AI stages).
- **ISO/IEC 42005** — AI system **impact assessment** guidance (the deep-dive companion to 42001's requirement).
- **ISO/IEC TR 24027/24028/TS 12791** — bias, trustworthiness, bias-in-ML treatment (technical reports).
- **ISO/IEC 27001/27701** — information security / privacy management systems that an AIMS typically bolts onto.
- **IEEE 7000 series** — value-based engineering: embedding ethical values in system design (IEEE 7000 model process; 7001 transparency; 7010 well-being metrics).

## CASES & EXAMPLES

**Scenario 1 — Which instrument?** A CEO asks: "I want an external stamp we govern AI responsibly for enterprise sales." *Analysis:* **ISO/IEC 42001 certification** — the only third-party-certifiable option among the three; NIST RMF and 23894 provide no certificate. Caveat to state: the stamp covers the management system, not individual model quality.

**Scenario 2 — Building clause 6.** During 42001 implementation, the risk lead asks how to actually run AI risk assessment. *Analysis:* Use **ISO/IEC 23894**: establish context/criteria, then identify → analyze → evaluate risks (with the AI-specific risk-source annex: opacity, data quality, drift, automation level), treat, record, monitor, communicate. 42001 demands the *that*; 23894 supplies the *how*.

**Scenario 3 — The integration play.** A company already ISO 27001-certified wants AI governance fast. *Analysis:* The harmonized structure means it can extend existing context, leadership, audit, and improvement machinery — adding the AI policy, AI roles, **AI system impact assessments**, Annex A AI controls and a combined Statement of Applicability — rather than building a parallel bureaucracy. This integration story is 42001's core selling point.

**Scenario 4 — Multi-framework shop.** A multinational must satisfy the EU AI Act (binding), wants Colorado's reasonable-care presumption, and its US customers ask for NIST RMF alignment. *Analysis:* Implement one AIMS (42001) with 23894-driven risk processes, then **crosswalk**: the AIMS QMS/risk/documentation work evidences AI Act Art. 9/17-style duties; RMF function mapping satisfies US expectations; both 42001 and RMF are named paths to Colorado's presumption. One system, many badges — the Lesson 12 drill.

## MEMORY HOOKS

- **Identity cards:** *42001 = certifiable AIMS (the what, org-wide) · 23894 = risk guidance on 31000 (the how, process-level) · 42005 = impact-assessment guidance (the who's-affected).*
- **PDCA to clauses:** **P**lan = 4–6 (context, leadership, planning) · **D**o = 7–8 (support, operation) · **C**heck = 9 (evaluation) · **A**ct = 10 (improvement).
- **Annex A rhythm:** *policies → people → resources → impacts → lifecycle → data → transparency → use → third parties.*
- **31000 loop chant:** *context → identify → analyze → evaluate → treat — communicate throughout, monitor forever.*
- **Certification scope warning:** *the certificate audits the system that manages the AI, not the AI itself.*

**The 5 facts to retain:**
1. ISO/IEC 42001 (2023) is the first **certifiable AI management system** standard — harmonized 10-clause structure, PDCA, any organization developing/providing/using AI.
2. Its distinctive demands: an **AI policy**, defined organizational **role**, AI **risk** assessment/treatment, **AI system impact assessment** (individuals/groups/society), and Annex A control selection justified in a Statement of Applicability.
3. ISO/IEC 23894 adapts **ISO 31000's** principles-framework-process risk model to AI — guidance only, never certified, with AI-specific risk sources.
4. Certification attests governance-process conformity, **not** model-level safety/fairness/legality.
5. The three instruments interlock: RMF gives outcome functions, 42001 institutionalizes and certifies, 23894 runs the risk engine — and crosswalks (plus Colorado's presumption and EU AI Act evidence value) make them one program.

## SELF-CHECK

1. **Q:** What kind of standard is ISO/IEC 42001 and what uniquely distinguishes it from NIST AI RMF and ISO 23894?
   **A:** A requirements-based management-system standard for an AIMS — the only one of the three that is third-party **certifiable**.

2. **Q:** Name three AI-specific things 42001 requires beyond generic quality management.
   **A:** An AI policy and defined AI roles/responsibilities; AI risk assessment and treatment with Annex A control selection; an AI **system impact assessment** addressing effects on individuals, groups and society (plus AI lifecycle and data-governance controls).

3. **Q:** On what parent standard is ISO/IEC 23894 built, and what is its process sequence?
   **A:** ISO 31000 risk management: establish scope/context/criteria → risk identification → analysis → evaluation → treatment → recording/reporting, with continuous communication/consultation and monitoring/review.

4. **Q:** A vendor's marketing says "our model is ISO 42001-certified fair." What's wrong?
   **A:** Certification applies to the organization's management system, not to a model's properties — it cannot certify fairness, accuracy, or legal compliance of specific outputs.

5. **Q:** Which mention-level standards cover (a) AI vocabulary, (b) AI lifecycle processes, (c) AI impact-assessment guidance, (d) value-based ethical design?
   **A:** (a) ISO/IEC 22989; (b) ISO/IEC 5338; (c) ISO/IEC 42005; (d) IEEE 7000 series.
