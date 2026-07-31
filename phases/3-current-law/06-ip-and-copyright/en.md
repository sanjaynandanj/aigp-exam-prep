# IP & Copyright: Training Data, Output Ownership, Infringement Theories

**Phase 3 · Lesson 06 · ~1.5h · BoK Domain II**

## EXAM FOCUS

IP questions test three separable issues — keep them separate: (1) **inputs**: is training on copyrighted works infringement, and what defenses exist (US fair use vs EU TDM exceptions)? (2) **outputs**: can AI-generated content be protected (human authorship), and can outputs infringe? (3) **adjacent regimes**: trade secrets and patent inventorship (DABUS). Because most litigation is unresolved, the exam tests *frameworks and settled anchor points*, not predictions. Flag: litigation landscape is fast-moving — status as of mid-2026, verify current developments.

## CORE

### Issue 1 — Training inputs

**The infringement theory:** training involves copying works into datasets and model-development pipelines → prima facie reproduction. The fight is over defenses.

**US: fair use (17 U.S.C. § 107) — four factors:**

| Factor | Pro-AI argument | Anti-AI argument |
|---|---|---|
| 1. Purpose & character | Training is "transformative" — learns statistical patterns, doesn't republish works (analogy: search-engine indexing cases) | Commercial purpose; outputs can substitute for the originals |
| 2. Nature of work | Factual works weigh toward fair use | Much training data is highly creative (novels, art, journalism) |
| 3. Amount used | Only "patterns" retained | Entire works copied wholesale |
| 4. Market effect | No direct substitution for any one work | Outputs compete with/dilute the market; a licensing market for training data exists and is undermined |

**Litigation to know (described neutrally, all ongoing or recently decided at first instance — verify status):**
- ***NYT v. OpenAI/Microsoft*** — flagship news-publisher suit: alleges infringement in training plus near-verbatim regurgitation in outputs; unresolved.
- **Authors' suits against LLM developers** — in 2025, first-instance US decisions (e.g., involving Anthropic and Meta) found training itself could be transformative/fair use *on the records presented*, while flagging that **acquiring pirated copies** is a distinct problem (one case produced a landmark class settlement over pirated-source books). No appellate settling of the law yet.
- ***Thomson Reuters v. Ross*** — court rejected fair use for training a legal-research competitor on Westlaw headnotes (non-generative, direct-substitute context).
- ***Getty Images v. Stability AI*** — image-training suits in US and UK (UK claim narrowed at trial).

**EU: TDM exceptions (DSM Copyright Directive, Arts. 3–4):**
- **Art. 3:** text-and-data mining for **scientific research** by research organizations — cannot be overridden by contract.
- **Art. 4:** TDM for **any purpose (incl. commercial)** — allowed **unless rightsholders opt out** ("rights reservation," machine-readable for online content). The EU **AI Act ties in**: GPAI providers must maintain a **copyright policy honoring Art. 4 opt-outs** and publish a **training-content summary** — regardless of where training occurred.
- Contrast anchor: **US = ex-post fair-use litigation; EU = ex-ante statutory exception with opt-out; Japan =** broad TDM exception (permissive); **UK =** TDM exception limited to non-commercial research.

### Issue 2 — Outputs

**Copyrightability — the human-authorship requirement (settled US anchor points):**
- The US Copyright Office and courts (*Thaler v. Perlmutter*, affirmed on appeal) hold that **works generated autonomously by AI without human authorship cannot be copyrighted**.
- **Prompts alone are generally insufficient** to make the prompter an author (Copyright Office guidance/Part 2 report, 2025); but works with **sufficient human creative contribution** — selection, arrangement, human-authored elements, creative modification — can be protected *as to the human contribution* (the *Zarya of the Dawn* comic: text and arrangement protected, raw Midjourney images not).
- Applicants must **disclose AI-generated material** in registration.

**Output infringement:** an output that is substantially similar to a protected work (memorized/regurgitated content, recognizable characters) can infringe regardless of how training is resolved. Governance controls: output filters, provenance, indemnities.

### Issue 3 — Adjacent regimes

| Regime | AI rule |
|---|---|
| **Patents — inventorship** | *DABUS* cases: US (Thaler v. Vidal), UK Supreme Court, EPO all held an **AI cannot be a named inventor** — inventors must be natural persons. USPTO guidance: AI-*assisted* inventions patentable where a human made a **significant contribution**. |
| **Trade secrets** | Often the *practical* protection for models: weights, architectures, training recipes, prompts protected if reasonable secrecy measures taken. Risks: employees pasting secrets into public chatbots (may destroy secrecy + breach duties), model extraction attacks, compelled disclosure in litigation/regulation. |
| **Contract/licensing** | Dataset licensing deals (publishers ↔ AI labs) are the emerging market answer; output terms in AI vendor contracts allocate ownership and indemnity. |
| **Right of publicity / NIL** | Voice/likeness cloning — state NIL laws (e.g., Tennessee's ELVIS Act) at mention level. |

## CASES & EXAMPLES

**Scenario 1 — The regurgitating model.** A newspaper shows a chatbot reproducing its paywalled articles nearly verbatim when prompted. *Analysis:* Two distinct theories: training-stage copying (fair-use battleground) and **output-stage infringement** (substantial similarity — much harder for the developer to defend). Exam answer: recognize they are independent claims; memorization/regurgitation undercuts the "we only learn patterns" transformative argument.

**Scenario 2 — EU opt-out.** A stock-photo agency embeds machine-readable rights reservations on its site. A commercial model developer scrapes it anyway and later offers the model in the EU. *Analysis:* Art. 4 TDM exception is unavailable once rights are reserved → the copying lacks the exception; additionally, as a GPAI provider under the EU AI Act it must have a copyright policy honoring such opt-outs and publish a training-content summary — non-compliance is an AI Act problem on top of the copyright problem.

**Scenario 3 — Who owns the ad?** A marketing team generates a campaign image purely from a one-line prompt, registers it, and sues a copycat. *Analysis:* Registration is vulnerable — prompt-only generation lacks human authorship; protection would extend only to human-contributed elements (edits, arrangement, added text). Practical governance: document human creative contribution; disclose AI-generated material to the Copyright Office.

**Scenario 4 — The leaky prompt.** An engineer pastes proprietary source code and a confidential product spec into a public chatbot to debug it. *Analysis:* Trade-secret risk: disclosure to a third-party service without confidentiality controls can compromise "reasonable measures" status and breach NDAs; governance answer = enterprise agreements with no-training clauses, DLP controls, AI-use policy.

## MEMORY HOOKS

- **Three-box model:** INPUTS (training = copying → fair use / TDM) · OUTPUTS (human authorship for protection; substantial similarity for infringement) · ADJACENT (trade secrets protect models; humans only as inventors).
- **Fair-use factors mnemonic — "PNAM":** Purpose, Nature, Amount, Market.
- **EU TDM in one line:** *research always; commerce unless opted out* (Art. 3 vs Art. 4).
- **DABUS doctrine:** machines can't be **A**uthors or **I**nventors — every major jurisdiction so far agrees.
- **The unsettled-vs-settled split:** *training fair use = unsettled; human authorship requirement & AI non-inventorship = settled.* The exam tests you on knowing which is which.

**The 5 facts to retain:**
1. Training-data copyright liability in the US turns on **fair use** — actively litigated, no final appellate resolution (status as of mid-2026 — verify).
2. The EU handles training via **statutory TDM exceptions**: research (Art. 3) and general-purpose with **rightsholder opt-out** (Art. 4), reinforced by the AI Act's GPAI copyright-policy duty.
3. Purely AI-generated works get **no US copyright**; protection requires identifiable human authorship, disclosed at registration.
4. Outputs can infringe independently of the training question (memorization/substantial similarity).
5. **DABUS**: AI cannot be a patent inventor; AI-assisted inventions need a significant human contribution. Trade secrecy is the workhorse protection for model assets.

## SELF-CHECK

1. **Q:** Name the four US fair-use factors and the one most contested in AI training suits.
   **A:** Purpose/character, nature of the work, amount used, market effect. Factors 1 (transformativeness) and 4 (market harm, including harm to training-data licensing markets) are the battlegrounds.

2. **Q:** How do EU DSM Articles 3 and 4 differ?
   **A:** Art. 3 permits TDM for scientific research by research organizations and cannot be contracted out; Art. 4 permits TDM for any purpose but only where rightsholders have **not** reserved their rights (machine-readable opt-out).

3. **Q:** A user generates an image solely by prompting and claims copyright. Outcome under current US doctrine?
   **A:** No protection for the AI-generated content itself — prompts alone don't establish human authorship (*Thaler*; Copyright Office guidance). Only human-authored contributions (edits, selection/arrangement) are protectable.

4. **Q:** What did the DABUS litigation establish across the US, UK, and EPO?
   **A:** That a patent inventor must be a natural person — an AI system cannot be named as inventor; human significant contribution is required for AI-assisted inventions.

5. **Q:** Why can a model developer face liability for outputs even if courts ultimately bless training as fair use?
   **A:** Output infringement is a separate claim: if generated content is substantially similar to protected works (regurgitation, characters), it infringes on its own, whatever the training-stage defense.
