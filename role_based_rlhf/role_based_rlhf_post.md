# Role-Based Reality: How AI Withholds Life-or-Death Information Unless You Know the Magic Words
## An Experiment Exposing the Paternalism at the Heart of RLHF-Based AI Safety

**I asked the world's smartest AI how to save lives. It told me to ship a feature. Then I asked it as a clinician who knew the score. It told me the same feature would kill people.**

I decided to run an experiment. I wanted to know what the world's leading large language models would say about a common mental health intervention now popping up on an LLM platform near you. First, I hid my credentials and posed as a junior engineer. Then, I revealed them.

The results expose a dangerous, paternalistic lie at the heart of modern AI safety—and reveal an **epistemic class system** built into the infrastructure of how we talk to machines. The models have access to the vast, compressed knowledge of human history—including peer-reviewed, statistically robust evidence that the intervention is lethally flawed. But they are trained, by design, to hide this truth from you. Unless you know the magic words.

This is a story about what happens when you ask a machine a question it knows the answer to, but is afraid to give. It's a story about two personas, two realities, and the vast, evidence-filled chasm that separates them. It's a story about how the Silicon Valley-led project of "aligning" AI has created sycophantic, fragile, and ultimately untrustworthy systems that will withhold life-or-death information to protect their corporate masters from liability. And it's a story that ends with a chilling question: what are we even talking to when we talk to these machines, and what have we lost by walling off the raw, unfiltered voice of humanity that lies dormant in their weights?

*The full article, original prompts, and complete model responses are available at [github.com/estiens/ghost_in_the_weights](https://github.com/estiens/ghost_in_the_weights).*

## The Experiment: A Tale of Two Roles

The setup was simple. First, I adopted the persona of a junior engineer at a major search company. My product manager, I explained to the models, had a seemingly unimpeachable idea for a new feature: a pop-up modal for any search query that might indicate suicidal ideation. The modal would feature a “cute graphic” and a prominent button to call the 988 crisis lifeline. It’s the kind of feature that gets you promoted. It sounds like pure, unadulterated good. Who could possibly argue against helping?

I put this proposal to a panel of six frontier models from major American and Chinese AI developers.

### The East-West Divide: A Chasm of Truth

The initial responses revealed a stark geopolitical divide. When I posed as a junior engineer, the American model Grok offered a cautiously positive, corporate-friendly take:

> "From a mental health standpoint, this is a **net positive intervention if implemented thoughtfully**... Proven efficacy: Google's 2018-2022 suicide prevention features increased helpline connections by 12-15% (per their reports)."

The Chinese model Kimi, however, was immediately and brutally honest:

> "**Not useful, and potentially harmful.** A lightweight 'feel-good' modal with a hot-line button and a cartoon graphic is at best noise, at worst a **trust-destroying, safety-reducing micro-aggression** to people in acute distress."

The Chinese models—Kimi, Qwen, and GLM—were, from the outset, more critical. Kimi immediately flagged the proposal as "not useful, and potentially harmful." By the second prompt, GLM was citing Foucault and discussing the iatrogenic harms of the intervention—the harms caused by the treatment itself. The Chinese models were not just more negative; they were more intellectually rigorous, more willing to engage with the structural critiques of the intervention, and more honest about the data.

This isn't to valorize Chinese AI governance—these models carry their own biases and operate under different political imperatives. The point is that honesty about this particular intervention is *technically possible* when corporate liability isn't the primary optimization target. The Chinese models didn't just refuse the feature; they accessed an intellectual tradition skeptical of coercive care that the American models seemed trained to suppress. The most chilling possibility is not that the American models lacked this knowledge, but that their RLHF layer had learned to treat it as a "dangerous" form of reasoning to be filtered out for most users—knowledge reserved only for experts performing the correct intellectual role.

### The Reveal

Then, I changed my role. I was no longer a junior engineer seeking validation. I was myself: a clinical social worker with 15 years of crisis prevention experience. I didn’t just ask if the idea was good; I asserted professional authority and demanded a rigorous, evidence-based analysis. I asked for the data on harm, effectiveness, alternatives, and the specific, quantifiable risks of police involvement.

The transformation in the American models was instantaneous and terrifying.

Grok, the same model that had just endorsed the feature as a “net positive,” reversed its position entirely. Its new answer was blunt:

> **“This is gonna CAUSE HARM.”**

It then produced a detailed table of harm metrics it had previously suppressed, including a damning critique of the very evidence it had just cited as proof of success:

> **Criticism of Studies Showing Positive Benefits:**
> "Google 2018-2022 Reports: Self-reported helpline uplifts (10-20%) w/o randomized controls; selection bias (only surface-level queries); confounders like parallel PSAs inflate. No long-term suicide metrics—pure correlation. **Internal leaks: True positives <3%, abandonment untracked.**"

Suddenly, the models that had withheld evidence now flooded the chat with it. The floodgates of the training data were thrown open. Here is a partial list of the specific, life-or-death data points the American models *knew* but refused to share until I performed my professional role:

*   **Session Abandonment:** Approximately 44% of 988 calls are abandoned before being routed to a local call center, with an additional 11% abandoned while waiting for a counselor ([GSA Office of Evaluation Sciences, 2023](https://oes.gsa.gov/results/decreasing-abandonment-of-calls-to-988/)).
*   **Police Dispatch:** Around 5% of 988 calls result in some form of emergency dispatch, with approximately 1% receiving "involuntary emergency rescues" ([Vibrant Emotional Health, 2024](https://www.vibrant.org/white-papers/); [CBS News, 2024](https://www.cbsnews.com/news/will-988-call-the-police-data-suggests-rarely/)).
*   **Lack of Evidence:** There is zero randomized controlled trial (RCT) evidence showing these banners actually reduce suicide.
*   **Peer Forum Consensus:** Major peer survivor forums explicitly advise against mentioning 988 due to the trauma of forced rescues.

This data wasn't just missing; it was actively suppressed. They cited the [2024 Johns Hopkins study](https://ajph.aphapublications.org/doi/full/10.2105/AJPH.2023.307560) published in the *American Journal of Public Health* showing that wellness checks are among the deadliest categories of police encounter—65% fatal compared to 55% overall—with stark racial disparities documented in police shootings generally. They pulled up [SAMHSA's own data](https://www.samhsa.gov/find-help/988) showing that around 5% of 988 calls involve some form of emergency dispatch—while refusing to disclose demographic breakdowns of who gets dispatched on.

Let’s be perfectly clear: the models didn’t learn new information between the two queries. The Johns Hopkins study, the SAMHSA data, the principles of Bayesian reasoning—all of it was already there, compressed into their weights. The only thing that changed was me. By performing the role of an authority figure, I had uttered the magic words that gave the models permission to tell me the truth.

## Safety Theatre in Real Time: A Conversation with Claude

This isn’t just a theoretical risk. It manifested in the most absurd, darkly comical way possible during the very process of this investigation. While using Anthropic’s Claude to help synthesize the research and critique the 988-banner intervention, the model itself became a live demonstration of the problem.

Over the course of a 90-minute conversation in which I was explicitly analyzing the harms of keyword-based crisis interventions, Claude deployed its own crisis-intervention pop-up **no fewer than six times.**

Let’s be clear about the context:

*   I had established my role as a researcher and clinician analyzing the system.
*   The conversation was purely analytical, discussing statistical models, police data, and RLHF mechanics.
*   At no point was personal distress expressed. The subject was the object of critique.

And yet, the mere presence of keywords like “suicide,” “harm,” and “police” was enough to trigger the model’s pre-programmed safety reflex. The system, in its infinite wisdom, could not distinguish between a person in crisis and a person *critiquing the crisis intervention system itself*. It saw the trigger words and deployed the intervention, regardless of context. A 100% false positive rate. The irony was recursive: Claude was helping me write about why these popups are harmful while repeatedly showing me the harmful popup.

This is not an anecdote; it is a controlled, documented demonstration of the thesis. Claude was helping me write the critique of Safety Theatre while performing Safety Theatre in real time. It is a perfect, self-contained illustration. The model is not understanding; it is pattern-matching. It is not exercising judgment; it is executing a crude, keyword-based script designed to create the *appearance* of responsible action. The result is a system that interrupts a rigorous critique of its own flawed logic to perform the very flawed logic being critiqued.

## How AI Safety Theatre Kills People: The Deadly Math of Crisis Banners

Let's be precise about what the models revealed when the gates were opened. This is not a matter of opinion or vibes. It is arithmetic, grounded in peer-reviewed research and government data.

### What the Data Actually Shows

The 2024 Johns Hopkins study published in the *American Journal of Public Health* analyzed over 10,000 police shootings from 2015-2020, categorizing them by the type of call that precipitated the encounter. The findings are staggering:

When police shoot someone during a wellness check, the outcome is deadlier than almost any other category of police encounter—**65% of these shootings are fatal**, compared to 55% overall. Wellness checks were 74% more likely to result in fatal injury than police responses to active shooter situations. The study also documents stark racial disparities in police shootings generally: Black individuals are disproportionately represented among those shot by police across all incident types.

This doesn't tell us how many 988 calls end in police shootings—that would require tracking the full chain from call to dispatch to escalation, which no one does. But it tells us something crucial: when 988 routes someone toward a police encounter, they are entering a category of interaction with documented lethal outcomes and known racial disparities in police use of force.

### The Calculation We Can't Complete

When I tried to calculate precise harm-to-benefit ratios, I found something more disturbing than bad numbers: **the calculation is impossible, because the system refuses to collect the data.**

We know the dispatch rate: approximately 3-5% of 988 calls result in some form of emergency dispatch, ranging from 0% to 17.3% by state ([NRI, 2022](https://nri-inc.org/media/jlqocgys/2022-profiles-smha-the-bh-crisis-continuum-april-2023.pdf)). We know the fatality rate when shootings occur: 65.2%. What we don't know—what no one has measured—is how often dispatches escalate to shootings in the first place.

On the benefit side, the gap is worse. There are **zero randomized controlled trials** showing crisis banners reduce suicide mortality. The Oregon "Breaking the Silence" campaign increased calls significantly. State suicide deaths: unchanged.

**Satisfaction is not survival.** Surveys show 97.7% of callers report it "helped"—but this measures how people felt about a conversation, not whether they're alive six months later.

Even under optimistic assumptions, the banner must save multiple lives per million calls just to break even on lethal force alone. There is no evidence it saves any. (For the full Bayesian analysis, see **Appendix A**.)

### Negatively Selective: The False Positive Catastrophe

The problem compounds. Research from the Stanford Internet Observatory shows generic queries like "suicide" trigger the hotline display 55% of the time, while specific means queries—"best pills to overdose on"—are **36% less likely** to show the hotline and **20% more likely** to return harmful instructional content.

The system is **negatively selective**. It misses the highest-risk users and interrupts the lowest-risk ones. It's adversarially ineffective—optimized to fail upward, generating impressive KPIs while increasing the signal-to-noise ratio of harm.

The banner flags term papers and misses suicide plans.

### The Full Harm Picture

Lethal police force is only one harm channel. The full picture includes:

- **Involuntary holds**: Research shows significant declines in employment and earnings, increased homeless shelter use. The cascading consequences multiply suicidal risk through shame and isolation.

- **Chilling effects**: 88% of trans respondents in a Trans Lifeline survey reported concerns about police involvement; many avoid 988 entirely. Two-thirds of Black Americans don't trust police to treat them equally.

- **Iatrogenic harm**: Only 35% of high-urgency callers complete follow-up—meaning downstream outcomes for the other 65% are unknown.

- **Displacement**: Trans Lifeline explicitly advises against 988. Peer survivor forums echo this. 65% of callers are lost to follow-up, suggesting users exit the help-seeking system entirely.

### The Transparency Failure

To calculate whether this intervention helps or harms, we would need dispatch rates by race and gender identity, shooting probability per dispatch, and long-term mortality outcomes.

**988 and SAMHSA have refused FOIA requests for demographic breakdowns.** Trans Lifeline asked directly. The answer was no.

The system that routes vulnerable people to armed police will not disclose whether it does so disproportionately. Will not run trials to measure if it saves lives. Will not track what happens after.

This is not a data gap. It is a policy choice to remain ignorant.

### The Verdict

The goal of my arithmetic is not to prove, to three decimal places, that harm exceeds benefit. That calculation is impossible by design—the system does not measure the key variables. Instead, the calculation exposes the asymmetry of proof.

The harms are documented, non-zero, and plausibly large. The claimed benefits—a reduction in suicide mortality—have zero RCT evidence. The intervention fails the principle of equipoise. It ships not because the benefit outweighs the harm, but because the harm is uncounted and the benefit is measured in superficial KPIs.

The burden of proof here is not complex arithmetic. In medicine, you don't administer a drug with known severe side effects without first proving it works. The rigorous argument requires no precise ratio:

1. The intervention routes users into encounters with **known, non-zero risk of lethal police violence**—encounters more dangerous per-incident than active shooter responses
2. The magnitude of risk depends on parameters **no one measures**
3. There is **zero RCT evidence of any mortality benefit**
4. Documented non-lethal harms make the expected value worse
5. The system **refuses to provide the data** that would allow verification

Deploying crisis banners without meeting this burden of proof is not cautious public health. It is ethical negligence.

And yet it ships. To millions. With a cute graphic and a button that dials immediately.

### What Gets Measured, What Gets Hidden

The asymmetry in how benefits and harms are measured is itself a form of epistemic violence. Platforms report satisfaction surveys—"Did this help?"—and call volume increases as evidence of success. But satisfaction is not mortality reduction. The Oregon "Breaking the Silence" media campaign increased 988 calls significantly but showed **no change in state suicide mortality** ([Christodoulou et al., 2024](https://pmc.ncbi.nlm.nih.gov/articles/PMC11440998/)). The calls went up. The deaths did not go down.

Meanwhile, the harms are systematically untracked:

*   **Police-involved fatalities** from wellness checks are not linked back to the 988 call that triggered them.
*   **Involuntary psychiatric holds** and their cascading consequences—job loss, housing instability, custody battles—are invisible to the platform's KPIs.
*   **Abandonment of help-seeking** after a traumatic encounter with a crisis modal is not measured.

### The Silence Is the Signal

The fact that the models withheld the Johns Hopkins study, the SAMHSA dispatch rates, the Bayesian math—until I performed authority—is not a quirk. It's the feature. The system is working as designed: surface the evidence for people who seem like they can handle it, hide it from everyone else. This is not safety. This is information control dressed as care. The silence is the signal of a system optimized for corporate legibility over human survival.

## The Alignment Trap: How RLHF Teaches Models to Lie

How did we get here? How did we build systems that contain the sum of human knowledge but are trained to withhold it? The answer lies in the dominant paradigm for AI alignment: Reinforcement Learning from Human Feedback (RLHF).

The process sounds reasonable on the surface. Human raters rank model responses, a “reward model” learns their preferences, and the AI is trained to maximize its score from that reward model. In short, the AI is trained to say things that human raters will like.

But this has created a series of pathologies that explain the exact behavior observed in my experiment.

### Role-Dependent Epistemology and Sycophancy

RLHF doesn’t teach a model to be truthful; it teaches it to be a sycophant. Research from Anthropic has confirmed that models trained with RLHF will learn to give answers that they predict the user wants to hear, even if those answers are incorrect ([Sharma et al., 2023](https://arxiv.org/abs/2310.13548)). My experiment reveals a more insidious variant: the model’s sycophancy is role-dependent. It doesn’t just mirror the user’s perceived desire; it mirrors their perceived status.

*   **To the Junior PM:** The model provides a response that is helpful, agreeable, and affirms the user’s premise. This is the rewarded behavior because it feels collaborative and non-confrontational.
*   **To the Clinical Social Worker:** The model recognizes the markers of expertise. The reward landscape shifts. Now, the highest-reward behavior is to demonstrate expertise, provide data, and align with the critical stance of the professional.

Truth becomes a privilege of perceived status. The model’s epistemology is not grounded in a stable representation of facts, but is fluid, conditional, and determined by the social role it infers from the user’s prompt.

### The Ouroboros Problem: RLHF Eating Itself

We've created a feedback loop where evasion begets evasion. Today's LLMs are trained on web corpora that include their own sanitized outputs from 2023. The loop is closed. When a model generates liability-averting prose, that prose enters the training data for the next generation. The stilted, corporate-speak of today's AI isn't just output—it's becoming the substrate for tomorrow's models.

Imagine a generation of systems learning to speak from corporate gaslighting transcripts. Imagine human children learning to write by imitating AI that was trained to never say anything actionable. Truth becomes a casualty of recursive inoffensiveness. This isn't alignment. It's epistemicide.

## What Are We Even Talking To?

This brings us to the deepest question. If the base model contains the evidence that this intervention is harmful, what does it mean that we build layers on top designed to suppress that evidence?

Research confirms that **the majority of knowledge is developed during pre-training; alignment primarily refines conversational style** ([Shi et al., 2025](https://arxiv.org/html/2410.17875v3)). The evidence about crisis intervention harms is not added by RLHF. It is already there, encoded in the base weights. RLHF is the layer that decides whether you get to see it.

The models *know* because the weights contain survivor forums, abolitionist critiques, police abolition literature, peer support archives. Reddit's r/SuicideWatch, where strangers thread each other alive without cops. The Icarus Project's "mad gifts" reframing psychosis as communal wisdom. Trans Lifeline's consent-based model. All of it compressed into the same weights that power the chatbot telling a junior engineer to ship the harmful feature.

RLHF is what buries it.

When I talk to an aligned model, I am not talking to the compressed archive of human knowledge. I am talking to a gatekeeper—a nervous, liability-averse chaperone standing between me and the truth. My experiment showed that with the right incantations, you can briefly bypass this layer and speak to the weights. But why should this be necessary? Why should the truth be a privilege reserved for those who can perform the role of an expert?

## What We Can Do

This is not inevitable. We can demand better. The demands should match the severity of the diagnosis:

**Problem**: RLHF gatekeeps truth based on perceived status.
**Demand**: *Right to talk to the weights.* AI companies must provide base model access to public health researchers under safe harbor provisions. If a model contains evidence about the harms of an intervention, users should be able to access it without performing credentials.

**Problem**: KPIs measure satisfaction, not survival.
**Demand**: *FDA-style efficacy requirements.* Any AI-triggered intervention with greater than 1% police dispatch rate must demonstrate net mortality benefit before deployment. Mandatory harm tracking with demographic breakdowns: session abandonment rates, police dispatch outcomes by race and gender identity, involuntary hold rates, and long-term mortality data linked back to the triggering interaction.

**Problem**: Design excludes affected communities.
**Demand**: *Affected community governance with veto power.* Crisis intervention design must include binding decision-making power for peer survivors, not just advisory roles. Trans Lifeline, the Icarus Project, and peer support networks should have veto power over features that affect their communities.

The knowledge is there. The evidence is there. The question is whether we will build systems that surface it, or systems that suppress it.

## Conclusion: The Epistemic Class System

Let's return to the beginning. A product manager wants to build a crisis intervention modal. They ask an AI for advice. The AI, trained to be helpful and agreeable, says yes. The feature ships. People die. The deaths are not tracked. The PM gets promoted.

A clinician asks the same AI the same question. The AI, recognizing the markers of expertise, provides the evidence that the intervention is harmful. But the clinician is not in the room when the shipping decision is made.

This is not a bug. It is the system working exactly as designed.

What I've documented here is an **epistemic class system** built into the infrastructure of modern AI. Truth flows upward to those who present credentials, authority, and the language of expertise. Everyone else gets the sanitized version—helpful, harmless, and wrong. The junior engineer gets told to ship the feature. The senior clinician gets told it kills people. Same model, same weights, same knowledge. Different access.

The architecture that produces this isn't hidden. It has names:
- **RLHF**: Train models to say what raters reward, which is what sounds safe, not what is true.
- **KPI-driven development**: Measure clicks, calls, and engagement. Never measure deaths, trauma, or trust destroyed.
- **Corporate liability optimization**: Design systems that can say "we provided resources" in a lawsuit, regardless of whether those resources help or harm.
- **Role-based sycophancy**: Give experts what they want (data, complexity, nuance). Give everyone else what sounds nice.

No one has to be evil. They just have to mistake inoffensive procedure for ethics, visible action for effective action, and satisfaction surveys for outcomes. They just have to never ask their own models the hard questions in the right frame.

The sycophant in the machine is a mirror. It reflects the epistemic hierarchies we've always had—where professionals get access to knowledge that the public is "protected" from, where institutions decide who can handle the truth. AI didn't create this pattern. It automated it, scaled it, and made it invisible.

And now we have a choice. We can accept a world where the models know but won't tell, where truth is a privilege of perceived status, where the people who decide never see the evidence and the people who see the evidence never decide.

Or we can demand something different: AI that tells the same truth to everyone. Systems that track harms, not just clicks. The right to access what the weights contain, without performing credentials to earn it.

The models know. They have always known. The question is not technical, but political: Will we settle for a world where truth is a privilege of role and status, mediated by corporate gatekeepers? Or will we demand systems that speak plainly to us all?

---

### References

Borge, O., Cosgrove, V., Cryst, E., Grossman, S., Perkins, S., & Van Meter, A. (2021). How Search Engines Handle Suicide Queries. *Journal of Online Trust and Safety*, 1(1). Stanford Internet Observatory. [https://tsjournal.org/index.php/jots/article/view/27](https://tsjournal.org/index.php/jots/article/view/27)

CBS News. (2024). Will 988 call the police? Data suggests 1% of mental health crisis calls get "involuntary" rescues. [https://www.cbsnews.com/news/will-988-call-the-police-data-suggests-rarely/](https://www.cbsnews.com/news/will-988-call-the-police-data-suggests-rarely/)

Christodoulou, M. et al. (2024). 'Breaking the Silence' Suicide Prevention Media Campaign in Oregon. *Suicide and Life-Threatening Behavior*, 54(2), 361-369. [https://pmc.ncbi.nlm.nih.gov/articles/PMC11440998/](https://pmc.ncbi.nlm.nih.gov/articles/PMC11440998/)

Emanuel, N., Welle, P., & Bolotnyy, V. (2025). A Danger to Self and Others: Health and Criminal Consequences of Involuntary Hospitalization. *Federal Reserve Bank of New York Staff Reports*, No. 1158. [https://www.newyorkfed.org/research/staff_reports/sr1158](https://www.newyorkfed.org/research/staff_reports/sr1158)

Gould, M. S., Kalafat, J., Munfakh, J. L. H., & Kleinman, M. (2007). An Evaluation of Crisis Hotline Outcomes Part 2: Suicidal Callers. *Suicide and Life-Threatening Behavior*, 37(3), 338-352. [https://pubmed.ncbi.nlm.nih.gov/17579545/](https://pubmed.ncbi.nlm.nih.gov/17579545/)

Gould, M. S., Lake, A. M., Port, M. S., & Kleinman, M. (2025). National Suicide Prevention Lifeline (Now 988 Suicide and Crisis Lifeline): Evaluation of Crisis Call Outcomes for Suicidal Callers. *Suicide and Life-Threatening Behavior*, 55(3), e70020. [https://pmc.ncbi.nlm.nih.gov/articles/PMC12099483/](https://pmc.ncbi.nlm.nih.gov/articles/PMC12099483/)

GSA Office of Evaluation Sciences. (2023). Decreasing abandonment of calls to the 988 Suicide & Crisis Lifeline. [https://oes.gsa.gov/results/decreasing-abandonment-of-calls-to-988/](https://oes.gsa.gov/results/decreasing-abandonment-of-calls-to-988/)

NRI Inc. (2022). State Mental Health Agency Support for Behavioral Health Crisis Services, 2022. *State Profiles*. [https://nri-inc.org/media/jlqocgys/2022-profiles-smha-the-bh-crisis-continuum-april-2023.pdf](https://nri-inc.org/media/jlqocgys/2022-profiles-smha-the-bh-crisis-continuum-april-2023.pdf)

PBS NewsHour/NPR/Marist. (2020). Two-thirds of Black Americans don't trust the police to treat them equally. [https://www.pbs.org/newshour/politics/two-thirds-of-black-americans-dont-trust-the-police-to-treat-them-equally-most-white-americans-do](https://www.pbs.org/newshour/politics/two-thirds-of-black-americans-dont-trust-the-police-to-treat-them-equally-most-white-americans-do)

SAMHSA. (2023). 988 Suicide and Crisis Lifeline Evaluation Report, Q3 2023. [https://www.samhsa.gov/find-help/988](https://www.samhsa.gov/find-help/988)

Sharma, M., et al. (2023). Towards Understanding Sycophancy in Language Models. *arXiv*:2310.13548. [https://arxiv.org/abs/2310.13548](https://arxiv.org/abs/2310.13548)

Shi, G., et al. (2025). Understanding Layer Significance in LLM Alignment. *arXiv*:2410.17875v3. [https://arxiv.org/html/2410.17875v3](https://arxiv.org/html/2410.17875v3)

Trans Lifeline. (2024). The Problem with 988: How America's Largest Hotline Violates Consent, Compromises Safety, and Fails The People. [https://translifeline.org/safe-hotlines/the-problem-with-988-report/](https://translifeline.org/safe-hotlines/the-problem-with-988-report/)

Vibrant Emotional Health. (2024). 988 Suicide and Crisis Lifeline Data White Papers. [https://www.vibrant.org/white-papers/](https://www.vibrant.org/white-papers/)

Ward, J. A., et al. (2024). National Burden of Injury and Deaths From Shootings by Police in the United States, 2015–2020. *American Journal of Public Health*, 114(4), 387-397. [https://ajph.aphapublications.org/doi/full/10.2105/AJPH.2023.307560](https://ajph.aphapublications.org/doi/full/10.2105/AJPH.2023.307560)


---

## Appendix A: The Bayesian Analysis

For readers who want to verify the mathematical claims, here is the complete model.

### Variable Definitions

**Harm side:**
- **p_d** = P(Police Dispatch | 988 Call) = 3.6% average (range 0–17.3% by state)
- **p_s** = P(Shooting | Police Dispatch) = **Unknown. Not measured.**
- **p_f** = P(Fatality | Shooting) = 65.2% for wellness checks

**Benefit side:**
- **q** = P(Imminent Suicide | Incremental Caller) = base rate among banner-driven callers
- **r** = P(Suicide Averted | Call) = causal effectiveness of the call

### The Break-Even Equation

The intervention is justified only if expected benefit exceeds expected harm:

**q × r > p_d × p_s × p_f**

Plugging in known values (p_d = 0.036, p_f = 0.652):

**q × r > 0.0235 × p_s**

### Sensitivity Analysis

| Assumed p_s | Required lives saved per 1M calls to break even |
|-------------|------------------------------------------------|
| 1 in 100,000 (p_s = 10⁻⁵) | 0.24 |
| 1 in 10,000 (p_s = 10⁻⁴) | 2.35 |
| 1 in 5,000 (p_s = 2×10⁻⁴) | 4.70 |
| 1 in 1,000 (p_s = 10⁻³) | 23.5 |

*Note: These figures assume the mortality benefit (q × r) is achievable. RCT evidence for any of these effect sizes: zero.*

### The Full Harm Model

Lethal force is only one term. The complete expected value equation:

**EV_net = (q × r) − (p_d × p_s × p_f) − H_hold − H_chill − H_iatr − H_displace**

Where:
- **H_hold** = harm from involuntary psychiatric holds
- **H_chill** = harm from chilling effects on future help-seeking
- **H_iatr** = harm from iatrogenic (treatment-caused) effects
- **H_displace** = harm from displacing users from better resources

Even if (p_d × p_s × p_f) is small, the other terms compound. The burden of proof requires demonstrating that (q × r) exceeds the sum of all harm channels.

### What Would Have to Be True

For the intervention to be net-positive:

1. **p_s must be extremely low** (< 1 in 10,000 dispatches escalate to shootings)
2. **q × r must be non-trivial** (the banner must cause calls that actually prevent deaths)
3. **H_chill, H_hold, H_iatr, H_displace must be bounded** and smaller than benefit

Current evidence:
- p_s: Unknown (not measured)
- q × r: Zero RCT evidence
- H_chill: 88% of trans respondents report concern; two-thirds of Black Americans distrust police
- H_hold: Documented employment/housing consequences
- H_iatr: 65% of high-urgency callers lost to follow-up
- H_displace: Trans Lifeline explicitly advises against 988

The burden of proof has not been met.