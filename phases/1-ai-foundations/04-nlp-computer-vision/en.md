# NLP, Computer Vision, and the Major AI Application Families

**Phase 1 · Lesson 04 · ~1h · BoK Domain I**

## EXAM FOCUS

Domain I — recognizing the main AI application families and their characteristic risk profiles. Tested as **recall plus light scenario**: match a use case to its family, or (more usefully) match a family to its signature harms. The pattern to internalize: *the family tells you the failure modes to expect and the laws most likely to bite.*

## CORE

### The five application families

| Family | What it does | Everyday examples |
|---|---|---|
| **NLP (natural language processing)** | Understands and/or generates human language | Chatbots, translation, sentiment analysis, résumé parsing, content moderation, LLMs |
| **Computer vision (CV)** | Interprets images and video | Face recognition, medical imaging, OCR, autonomous-vehicle perception, quality inspection |
| **Speech** | Converts between audio and language | Transcription, voice assistants, voice cloning, speaker verification |
| **Recommender systems** | Ranks/personalizes content or options per user | Feeds, product recommendations, ad targeting, job-post matching |
| **Robotics / embodied AI** | Acts in the physical world via sensors + actuators | Industrial robots, warehouse automation, drones, autonomous vehicles, surgical robots |

### Risk profile by family

This table is the heart of the lesson — the exam loves "which risk is *most characteristic* of X":

| Family | Signature risks | Typical legal/regulatory hooks |
|---|---|---|
| **NLP** | Bias in language data (dialect, gender associations); toxic/harmful generation; hallucination; manipulation at scale; processing sensitive content | Anti-discrimination law (hiring tools), consumer protection, platform/content rules, AI Act transparency duties for chatbots |
| **CV — especially biometrics** | Demographic error-rate disparities (documented in face-recognition evaluations such as NIST's FRVT studies); mass-surveillance potential; misidentification with liberty consequences | Biometric laws (Illinois BIPA), AI Act's prohibited practices + high-risk categories for biometrics, GDPR special-category data |
| **Speech** | Accent/dialect accuracy gaps; voice cloning → fraud and impersonation (deepfake audio); always-on listening → privacy | Wiretap/recording consent laws, fraud law, AI Act deepfake labeling duties |
| **Recommenders** | Filter bubbles, amplification of extreme content, addictive design, discriminatory ad delivery (e.g., housing/job ads), manipulation of vulnerable users | EU Digital Services Act (recommender transparency), consumer protection, housing/employment discrimination law |
| **Robotics** | **Physical safety** first; then security (a hacked robot is a weapon), workplace displacement, liability puzzles when hardware + AI + human interact | Product safety & liability regimes, machinery rules, sector safety regulators; AI Act safety-component provisions |

### Two cross-cutting observations

1. **The same technique changes risk class with context** (full treatment in Lesson 09). Face *detection* to auto-focus a camera ≈ trivial; face *identification* by police in public spaces sits at the top of every regulatory pyramid — same CV core.
2. **Families combine.** An autonomous vehicle = CV + speech interface + planning/robotics. A modern "chatbot" = NLP + recommender-like ranking + speech. Governance must assess the *system*, and each embedded family imports its risks.

### Biometrics deserves its own paragraph

Because it recurs across the AI Act (Phase 4) and US state law (Phase 3): **biometric identification** (who is this, one-to-many), **biometric verification** (is this the claimed person, one-to-one), and **biometric categorization** (inferring attributes — emotion, ethnicity — from biometric data) are treated very differently in law. Identification in public spaces and categorization by sensitive attributes attract the harshest treatment; verification (your phone's face unlock) the lightest. Keep the three verbs separate now and Phase 4 gets much easier.

## CASES & EXAMPLES

1. **Face recognition misidentification arrests.** In the US, several documented wrongful arrests (widely reported cases in Detroit and elsewhere, disproportionately affecting Black men) followed police reliance on face-recognition matches. Research including NIST's face-recognition vendor testing has documented higher error rates for some demographic groups on some algorithms. Family: CV/biometrics. Signature risk realized: demographic error disparity + automation bias (treating a candidate match as an answer). Exam-ready.

2. **Discriminatory ad delivery.** US enforcement and litigation (including a settled DOJ action involving Facebook's housing-ad tools) addressed ad systems that delivered housing ads along demographic lines. Family: recommender. Lesson: *delivery optimization itself* can discriminate even when the advertiser targets neutrally.

3. **Voice-clone fraud.** Reported corporate frauds have used cloned executive voices to authorize transfers. Family: speech. Governance response pattern: out-of-band verification procedures — a process control, not a model control (a Lesson 09 theme).

4. **Exam-style matcher.** "Which application family most characteristically raises *physical* safety as its primary risk?" → Robotics/embodied AI. "Which most characteristically raises amplification and manipulation concerns?" → Recommenders.

## MEMORY HOOKS

**Family → flagship risk, one word each:**
- NLP → **bias/hallucination**
- CV/biometrics → **misidentification** (and surveillance)
- Speech → **impersonation**
- Recommenders → **amplification**
- Robotics → **physical safety**

**Biometric verbs:** *verify* (1:1, mild) < *identify* (1:many, severe) < *categorize by sensitive traits* (often prohibited territory).

The 5 facts to retain:

1. Five families: NLP, CV, speech, recommenders, robotics — each with a signature risk (see one-worders above).
2. Face-recognition demographic error disparities are empirically documented (NIST vendor testing) — a stock exam fact.
3. Recommenders can discriminate through *delivery*, not just targeting.
4. Robotics uniquely leads with physical safety and product-liability law.
5. Same technique + different context = different risk class; systems combine families and import each one's risks.

## SELF-CHECK

1. Name the five application families and one signature risk each.
2. Distinguish biometric verification, identification, and categorization — which draws the harshest legal treatment?
3. Why can an ad system discriminate even when the advertiser chose neutral targeting?
4. Which family's primary regulatory anchor is product safety and liability law, and why?
5. A hospital deploys a system that reads chest X-rays and dictates draft reports the radiologist edits by voice. Which families are involved?

<details>
<summary>Answers</summary>

1. NLP — language bias/hallucination; CV — misidentification/surveillance; speech — impersonation/voice cloning; recommenders — amplification/manipulation; robotics — physical safety.
2. Verification = 1:1 match to a claimed identity (lightest); identification = 1:many search (heavily restricted, especially in public spaces); categorization = inferring attributes from biometrics (harshest — sensitive-attribute categorization reaches prohibited territory under the EU AI Act).
3. The delivery/optimization algorithm decides who actually sees the ad and can skew along demographic lines on its own.
4. Robotics/embodied AI — its systems act physically, so failures cause bodily harm, engaging safety regimes rather than only informational harms.
5. CV (image interpretation), NLP (report generation), speech (voice editing) — governance must cover all three families' risks.

</details>
