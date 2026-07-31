# Stakeholder Engagement & AI Ethics Boards in Practice

**Phase 2 · Lesson 10 · ~0.75h · BoK Domain I**

## EXAM FOCUS

Domain I — stakeholder engagement and ethics-committee design. Tested as **design-and-diagnose scenarios**: an ethics board fails (no authority, wrong composition, conflicted) and you name the flaw; or a deployment harms a group nobody consulted and the answer is participatory engagement earlier. Recall side: the internal/external stakeholder split and the three design axes of an ethics board (composition, authority, escalation).

## CORE

### Mapping stakeholders

| Sphere | Stakeholders | What they hold |
|---|---|---|
| **Internal** | Board, executives, product/dev teams, governance/risk/legal/privacy/security, procurement, HR, **employees affected by AI** (monitored, managed, displaced), employee representatives/works councils | Authority, expertise, labor — and duties toward each other |
| **External** | Customers/users, **affected non-users** (people scored, screened, surveilled without ever choosing the product), regulators, vendors/partners, investors, civil society & advocacy groups, academia, impacted communities, the public | Rights, legitimacy, scrutiny, lived knowledge of impacts |

Two distinctions the exam rewards:

1. **Users vs affected persons.** The job *applicant* screened by a hiring tool is not the tool's customer (the employer is). AI's harms often land on people with no contract, no interface, and no exit — which is why engagement can't stop at "user research."
2. **Engagement is a spectrum**, not a binary: *inform → consult → involve → collaborate → empower* (the classic participation ladder). Publishing a notice is the floor; co-designing with affected communities and giving them decision influence is the top. Scenario answers should match the rung to the stakes.

### Participatory design

Engaging affected people **during design**, not after harm: co-design workshops, community advisory panels, worker consultation on algorithmic management, pilot feedback loops with affected groups, public comment for government systems. Rationale (three prongs, all quotable): **epistemic** — affected people know failure modes designers can't see (Lesson 1.09's context component); **legitimacy** — those subject to a system have a claim to shape it, especially in public-sector uses; **practical** — issues found in design cost less than issues found in litigation. Also name-check **red-team diversity**: testers drawn from varied backgrounds find harms homogeneous teams miss.

### AI ethics boards/committees — the three design axes

**Axis 1 — Composition**

| Choice | Options and trade-offs |
|---|---|
| Disciplines | Technical + legal + ethics + domain + affected-community perspectives; homogeneity is the classic failure |
| Internal vs external members | External members add independence and credibility, cost confidentiality friction; internal-only boards risk capture |
| Independence protections | Terms, removal protections, conflict-of-interest rules — a board the CEO can dissolve mid-controversy isn't independent |

**Axis 2 — Authority**

| Model | Meaning | Weakness |
|---|---|---|
| Advisory only | Recommends; business decides | Ignorable — advice without teeth |
| Binding within scope | Can block/condition defined categories (e.g., high-tier launches) | Needs charter backing and executive cover |
| Escalatory | Can force decisions upward to exec/board level | Only as good as the escalation destination |

The recurring real-world failure is **authority mismatch**: a board created for reputational signaling, given no veto, then bypassed when its view is inconvenient.

**Axis 3 — Escalation & process**

What reaches the board (triggers by risk tier, novel-use flags, whistleblower routes); what it must produce (reasoned, recorded decisions); where disagreement goes (to the executive/board level, documented); transparency of its existence and, where appropriate, its reasoning.

### Civil society and external scrutiny

Civil society organizations, investigative journalists, and academic researchers function as an unofficial assurance layer: much of the field's foundational knowledge of AI harm came from outside the deploying organizations (ProPublica on COMPAS; academic audits of face recognition such as the Gender Shades study; NGO litigation and complaints driving enforcement). Governance implications: engage rather than stonewall — publish meaningful transparency artifacts, provide researcher access paths, treat external findings as free red-teaming with an incident-response route (Phase 6), not as PR attacks.

## CASES & EXAMPLES

1. **The one-week ethics board.** In 2019, Google announced an external AI ethics advisory council; controversy over member selection led to its dissolution about a week later, and its lack of any binding authority was widely noted. Design-axis reading: composition process without legitimacy + advisory-only authority + no independence protections. The stock case for "ethics board as structure vs ethics board as signal."

2. **Consulting the people scored.** A city introducing an algorithmic benefits-fraud screen holds sessions with recipient communities and legal-aid groups before procurement; feedback surfaces that a planned data source (utility arrears) proxies poverty, not fraud, and an appeal-route gap. Both are fixed pre-launch. This is participatory design paying its epistemic and legitimacy dividends — contrast with the Dutch benefits scandal (Lesson 01), where affected families were the last to be heard.

3. **Works council friction.** A logistics firm deploys algorithmic shift-scheduling without consulting employee representatives; in several European jurisdictions co-determination rules make that consultation legally required, not just wise, and the rollout is challenged. Internal stakeholders have *rights*, not just opinions — employees affected by workplace AI are stakeholders of the first rank.

4. **Diagnose the board (exam style).** "A firm's AI ethics committee consists of five senior engineers from the AI lab, meets when the CTO convenes it, and records no decisions." Three named flaws: homogeneous composition (no legal/ethics/affected voices), no independent standing or regular process (convened at pleasure), no traceability (unrecorded decisions) — and implicitly advisory-only authority.

## MEMORY HOOKS

**Board design triad:** **C-A-E** — **C**omposition (who), **A**uthority (teeth), **E**scalation (where disagreements go). Every ethics-board question is one of these three.

**Participation ladder:** *inform → consult → involve → collaborate → empower* — match the rung to the stakes.

**One-liner:** *AI's most affected stakeholders are often not its users* — look for the scored, screened, and surveilled.

The 5 facts to retain:

1. Stakeholders split internal/external, and "affected persons" ≠ "users" — hiring, credit, and policing AI act on people who never chose the product.
2. Engagement is a ladder (inform→empower); high-stakes and public-sector uses demand higher rungs, in design, not post-launch.
3. Ethics boards are designed on three axes: composition (multidisciplinary, independence-protected), authority (advisory vs binding vs escalatory), escalation/process (triggers, recorded reasons, route upward).
4. The canonical board failure is authority mismatch — created to signal, powerless to stop anything (Google's 2019 council is the reference case).
5. Civil society, journalists, and academics are an external assurance layer (COMPAS, Gender Shades); mature programs build engagement and response channels for them.

## SELF-CHECK

1. Give three examples of affected non-user stakeholders and the systems that touch them.
2. Name the five rungs of the participation ladder in order.
3. What are the three design axes of an ethics board, with one failure mode each?
4. Why does participatory design have *epistemic* value, not just legitimacy value?
5. A scenario describes external researchers publishing bias findings about your deployed model. What does mature governance do with that?

<details>
<summary>Answers</summary>

1. Job applicants screened by a hiring tool (employer is the customer); individuals scored by credit/fraud models; people identified by police face recognition; benefit recipients screened by fraud algorithms — none chose or contracted for the system.
2. Inform → consult → involve → collaborate → empower.
3. Composition — homogeneous/captured membership; authority — advisory-only boards that get bypassed; escalation/process — no triggers, unrecorded decisions, nowhere for disagreement to go.
4. Affected people hold knowledge designers lack — real-world contexts, failure modes, proxy variables, and gaming behaviors — so consultation improves the system technically, not just politically.
5. Treat it as free external red-teaming: route findings into incident/issue management, verify and remediate, engage the researchers, and feed lessons into testing and monitoring — rather than dismissing or lawyering first.

</details>
