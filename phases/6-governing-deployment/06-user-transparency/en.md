# User-Facing Transparency: Notices, Labels, Disclosures

**Phase 6 · Lesson 06 · ~1h · BoK Domain IV**

## EXAM FOCUS

Transparency to *affected people* (distinct from regulator-facing documentation, Phase 5 L07). Tested: when AI interaction must be disclosed (chatbot notices), synthetic-content labeling and deepfake disclosure (EU AI Act Art. 50 concept), explanations of AI-assisted decisions to affected persons, and plain-language design. Distractor patterns: confusing Art. 50 transparency-risk duties with high-risk obligations, and confusing machine-readable marking (provider duty) with disclosure of deepfakes (deployer duty).

## CORE

### The transparency stack

| Layer | Question answered for the person | Instruments |
|---|---|---|
| **Interaction disclosure** | "Am I talking to a machine?" | Chatbot notices, voice-agent announcements |
| **Content provenance** | "Was this made/altered by AI?" | Watermarks/machine-readable marks, visible labels, deepfake disclosures |
| **Decision transparency** | "Did AI decide about me, and why?" | ADM notices, meaningful-explanation statements, adverse-action reasons |
| **Recourse** | "What can I do about it?" | Contest/appeal channels, human review requests |

### EU AI Act Art. 50 concept — the transparency-risk tier

| Duty (concept) | Who owes it | Substance |
|---|---|---|
| AI interaction disclosure | Provider | People must be informed they are interacting with an AI system, unless obvious to a reasonably informed person |
| Synthetic-content marking | Provider | Outputs of generative systems (audio, image, video, text) marked in a **machine-readable** way as artificially generated/manipulated |
| **Deepfake disclosure** | **Deployer** | Those deploying deepfake content (realistic image/audio/video of persons, places, events) must disclose the artificial generation/manipulation — with carve-out concepts for artistic/creative works (disclosure in a non-spoiling way) |
| Emotion recognition / biometric categorization notice | Deployer | Inform exposed persons where such systems are used (interacting with the prohibited-practices boundary from Phase 4) |
| AI-generated public-interest text | Deployer | Disclose AI generation of text published to inform the public on matters of public interest (unless human editorial review/responsibility applies — concept) |

Note the split the exam loves: **providers mark (machine-readable); deployers disclose (human-facing)**. These duties apply *regardless* of risk tier — a minimal-risk chatbot still owes interaction disclosure; a high-risk system owes these *plus* its high-risk obligations.

### Explanations of decisions

Where AI materially informs decisions about people (credit, hiring, benefits), affected persons need decision-level transparency:

- **That** an automated system was involved (notice);
- **Why** the outcome occurred — the main factors, in terms the person can act on (US adverse-action notices under fair-lending law are the long-standing model: specific principal reasons, not "the algorithm said so");
- **What now** — the route to contest or obtain human review (GDPR Art. 22 lineage from Phase 3; the EU AI Act adds an explanation-of-individual-decision concept for certain high-risk systems affecting people's rights).

A good decision explanation is: **specific** (this decision, not the system in general), **actionable** (what would change the outcome — counterfactual framing), **truthful** (reflects what actually drove the model), and **timely**.

### Plain-language design

Transparency fails when technically true but incomprehensible. Principles: write for the audience's reading level; put the key fact first ("This chat is answered by an AI assistant"); make labels *perceptible in the medium* (audible for voice, visible for video); don't bury AI disclosures in terms of service; test notices with real users; provide the disclosure **at the right moment** (before or during interaction, not after). Dark-pattern disclosure — technically present, practically invisible — is both an ethics failure and increasingly an enforcement theory (unfair/deceptive practices).

## CASES & EXAMPLES

**Scenario 1 — the "obvious" defense.** An insurer's website chat is AI-driven, styled with a human name, photo avatar, and typing indicators. The insurer argues disclosure is unnecessary. *Exam point:* Art. 50-concept disclosure is excused only where AI interaction is obvious to a reasonably informed person — actively humanizing the bot defeats that argument. Best answer: clear upfront notice ("You're chatting with an AI assistant").

**Scenario 2 — who labels the deepfake?** A marketing agency uses a licensed video-generation tool to create a realistic clip of a city flood for a campaign. The tool provider embedded machine-readable marks. Is the agency done? *Answer:* no — as deployer of a deepfake, the agency owes the human-facing disclosure that the content is artificially generated; the provider's watermarking duty and the deployer's disclosure duty are separate layers.

**Scenario 3 — the useless explanation.** A loan applicant is declined and receives: "Your application was assessed by our advanced scoring model." *Exam point:* fails decision transparency — no principal reasons, nothing actionable, no recourse route. The adverse-action model answer: specific main factors + how to contest/seek human review.

**Scenario 4 — voice agent.** A telecom's outbound AI voice agent calls customers about renewals, sounding fully human, and never announces itself. *Exam point:* interaction disclosure must fit the medium — an audible announcement at call start; visual small print elsewhere doesn't cure a voice-channel omission.

## MEMORY HOOKS

**The four user questions:** *Machine? Made-up? Decided about me? What now?* — interaction, provenance, decision, recourse.

**Art. 50 split:** *Providers mark, deployers disclose.* (Machine-readable watermark = provider; "this is a deepfake" to humans = deployer.)

**Explanation quality test — "SATT": Specific, Actionable, Truthful, Timely.**

The 5 facts to retain:

1. Transparency-risk duties (Art. 50 concept) apply across risk tiers: chatbot interaction disclosure, machine-readable marking of synthetic content, deepfake disclosure, emotion-recognition/biometric-categorization notices, public-interest text disclosure.
2. Provider duty = machine-readable marking of generative outputs; deployer duty = human-facing deepfake/content disclosure — separate, stacking obligations.
3. Interaction disclosure is excused only when AI involvement is obvious to a reasonably informed person — humanizing design destroys the exemption.
4. Decision transparency = notice of ADM + principal actionable reasons + contest/human-review route (adverse-action notices are the model; GDPR Art. 22 and the AI Act's explanation concept anchor it in law).
5. Disclosures must be plain-language, medium-appropriate, and delivered at the moment of interaction — buried or post-hoc notices fail.

## SELF-CHECK

1. **List the four layers of user-facing transparency.**
   Interaction disclosure (am I talking to AI?), content provenance (is this synthetic?), decision transparency (did AI decide about me and why?), and recourse (how do I contest?).
2. **Under the Art. 50 concept, who marks synthetic content and who discloses deepfakes?**
   Providers must ensure machine-readable marking of AI-generated/manipulated content; deployers of deepfakes must disclose the manipulation to people (with artistic-work carve-out concepts).
3. **When is chatbot disclosure not required, and what design choice forfeits that exception?**
   When AI interaction is obvious to a reasonably informed person; humanizing the bot (name, photo, human-like behavior) forfeits the "obvious" argument.
4. **What are the elements of an adequate explanation to a person adversely affected by an AI-assisted decision?**
   The fact of AI involvement, the specific principal factors behind the outcome (actionable/counterfactual where possible), and the route to contest or obtain human review — delivered promptly and in plain language.
5. **Do Art. 50-style transparency duties replace high-risk obligations for a high-risk system?**
   No — they stack: a high-risk system with generative or interactive features owes both its high-risk obligations and the applicable transparency duties.
