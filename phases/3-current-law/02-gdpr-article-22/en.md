# GDPR Article 22: Automated Decision-Making and Its Exam-Favorite Edge Cases

**Phase 3 · Lesson 02 · ~1h · BoK Domain II**

## EXAM FOCUS

Article 22 is the GDPR's only provision aimed squarely at algorithmic decisions, which makes it a scenario-question magnet. The exam tests the **elements** (solely automated + legal or similarly significant effect), the **three exceptions**, the **required safeguards**, and — above all — the **edge cases**: token human involvement, indirect significant effects, and profiling that feeds a human decision. Do not confuse GDPR Art. 22 with any EU AI Act article number.

## CORE

### The rule

**Art. 22(1):** The data subject has the right not to be subject to a decision **based solely on automated processing, including profiling**, which produces **legal effects** concerning them **or similarly significantly affects** them.

Regulators and the CJEU treat this as a **general prohibition** (with exceptions), not merely a right the individual must invoke — a classic exam distinction.

### Element 1 — "Solely automated"

- No **meaningful human involvement** in the decision.
- A human who merely rubber-stamps the algorithm's output ("token gesture") does **not** take the decision out of Art. 22. Meaningful involvement requires **authority and competence to change the decision**, actual consideration of other factors, and real engagement with each case.
- The CJEU's *SCHUFA* judgment (2023) held that even producing an automated **credit score** can itself be an Art. 22 "decision" when a third party (the bank) relies on it in a determining way — i.e., you cannot launder automation through a downstream human who in practice just follows the score.

### Element 2 — "Legal or similarly significant effects"

| Category | Examples |
|---|---|
| **Legal effects** | Denial of a benefit, contract termination, visa refusal, tax determination |
| **Similarly significant** | Automated refusal of an online **credit application**, **e-recruiting without human review**, insurance pricing that materially changes access, exclusion from essential services |
| **Usually NOT significant** | Ordinary targeted advertising, content recommendations — *unless* they exploit vulnerabilities or gatekeep important opportunities (e.g., showing job ads discriminatorily can cross the line) |

### Profiling

**Profiling** (Art. 4(4)) = any automated processing that **evaluates personal aspects** of a person (performance at work, economic situation, health, preferences, behavior, location). Profiling alone is regulated by general GDPR rules; Art. 22 bites when profiling produces a *solely automated, significant* decision. Profiling short of Art. 22 still triggers transparency duties and the Art. 21 right to object (absolute for direct-marketing profiling).

### The three exceptions — Art. 22(2)

| Exception | Conditions | Notes |
|---|---|---|
| **(a) Contract necessity** | Decision necessary for entering into or performing a contract with the subject | "Necessary" strictly read — e.g., automated screening of enormous application volumes may qualify; convenience does not |
| **(b) Authorized by Union/Member State law** | Law must lay down suitable safeguards | E.g., fraud prevention or tax legislation |
| **(c) Explicit consent** | Higher bar than ordinary consent — clear affirmative statement | Withdrawable at any time |

### Mandatory safeguards — Art. 22(3)

Where exceptions (a) or (c) apply, the controller must implement at minimum:
1. The right to obtain **human intervention** (by someone with authority to change the outcome);
2. The right to **express one's point of view**;
3. The right to **contest** the decision.

Plus transparency: Arts. 13/14/15 require telling subjects that ADM exists and providing **meaningful information about the logic involved** and the significance and envisaged consequences — not source code, but an intelligible explanation of the main decision factors.

### Special-category data in ADM — Art. 22(4)

Solely automated significant decisions may **not** be based on special-category data unless Art. 9(2)(a) (explicit consent) or 9(2)(g) (substantial public interest) applies **and** suitable safeguards are in place. Beware models that use **proxies** for special categories.

## CASES & EXAMPLES

**Scenario 1 — The rubber-stamp recruiter.** A company's AI ranks 5,000 applicants; an HR assistant "approves" the system's bottom-cut rejections at a rate of 400 per hour without opening any files. *Analysis:* No meaningful human involvement (no time, competence, or real authority exercised) → the decision is **solely automated**; rejection from a job is **similarly significant** → Art. 22 applies. The company needs an exception (likely contract-necessity or explicit consent) plus the three safeguards.

**Scenario 2 — The credit score (SCHUFA pattern).** A credit bureau generates automated scores; banks "decide" but in practice deny any applicant below the threshold. *Analysis:* Per the CJEU, the **scoring itself** can be the Art. 22 decision because it determines the outcome. Both bureau and bank need to get their houses in order — the bureau cannot claim it "only makes scores, not decisions."

**Scenario 3 — Genuine human-in-the-loop.** A loan officer receives a model recommendation, reviews the applicant's file, can and sometimes does override, and documents her reasoning. *Analysis:* Meaningful human involvement → **not** solely automated → Art. 22 does not apply. But general GDPR still does: transparency, fairness, the right to object to profiling, and — for governance — automation-bias controls to keep the involvement meaningful over time.

**Scenario 4 — Ad targeting edge case.** A platform's algorithm decides which users see ads for high-interest loans, effectively excluding certain neighborhoods. *Analysis:* Ordinary ad targeting usually isn't "similarly significant," but gatekeeping access to credit opportunities for vulnerable groups can cross the threshold — the exam rewards recognizing that the effect, not the label, controls.

## MEMORY HOOKS

- **The Art. 22 gate has two locks:** *SOLELY automated* + *SIGNIFICANT effect*. Both must be true or the article never applies.
- **Exceptions mnemonic — "CLC":** **C**ontract, **L**aw, **C**onsent (explicit).
- **Safeguards mnemonic — "HEC":** **H**uman intervention, **E**xpress your view, **C**ontest the decision.
- **Rubber stamp ≠ human review.** If the human lacks authority, competence, time, or information to change the outcome, the decision is still "solely automated."
- **Contrast table:**

| | Profiling only | Art. 22 ADM |
|---|---|---|
| Automated evaluation of a person | Yes | Yes |
| Solely automated decision | Not required | Required |
| Legal/significant effect | Not required | Required |
| Default legal position | Allowed with GDPR compliance | Prohibited unless CLC exception |

**The 5 facts to retain:**
1. Art. 22 is read as a **prohibition with exceptions**, not just an invocable right.
2. Both elements required: solely automated **and** legal/similarly significant effect.
3. Exceptions: contract necessity, Union/Member State law, explicit consent.
4. Safeguards under (a)/(c): human intervention, express views, contest — plus "meaningful information about the logic."
5. *SCHUFA*: automated scores that determine third-party outcomes can themselves be Art. 22 decisions; token human review doesn't escape the article.

## SELF-CHECK

1. **Q:** What two elements must both be present before Art. 22 applies?
   **A:** The decision is based *solely* on automated processing (no meaningful human involvement), and it produces *legal effects* or *similarly significantly affects* the person.

2. **Q:** List the three exceptions that permit solely automated significant decisions.
   **A:** Necessary for a contract with the data subject; authorized by Union or Member State law with safeguards; explicit consent.

3. **Q:** What makes human involvement "meaningful" enough to take a decision outside Art. 22?
   **A:** The reviewer must have real authority and competence to change the decision, consider all relevant data, and engage with the individual case — not rubber-stamp the output.

4. **Q:** Why is the *SCHUFA* ruling important for AI vendors that "only provide scores"?
   **A:** The CJEU held that automated score creation can itself be an Art. 22 decision when downstream parties rely on it in a determining way — vendors can't avoid Art. 22 by pointing to a nominal human decision elsewhere.

5. **Q:** Can a solely automated hiring decision be based on health data with the candidate's ordinary consent?
   **A:** No. Art. 22(4) requires an Art. 9(2)(a) *explicit* consent or substantial-public-interest basis plus suitable safeguards; ordinary consent is insufficient.
