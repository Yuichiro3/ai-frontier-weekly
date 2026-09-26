# AI Frontier Weekly — 2026-W39

**Run date:** 2026-09-26
**Collection window:** 2026-08-29 to 2026-09-26
**Sources:** `runs/2026-09-26/argument-map.json` and 15 collector files in `runs/2026-09-26/collectors/`

---

## A note on this week's sources

Please read this note before the rest of the report. Most collectors could not open the target websites directly this week because of network blocks. As a result, many items were rebuilt from search-engine snippets of official pages and from press coverage. Every reference at the end carries a confidence label:

- **primary-confirmed**: checked against the organization's own page or channel.
- **primary-inferred**: rebuilt from search snippets of the official page, not read directly.
- **secondary-source**: based on press or third-party coverage.

This week, 21 items are primary-confirmed, 37 are primary-inferred and 9 are secondary-source. The UK AI Security Institute collector found no new publications in the window. Google DeepMind coverage is probably incomplete, with only two items. We use hedging words ("reportedly", "according to") where an item is inferred or secondary.

---

## Executive summary

- Several labs released new frontier models in the same four weeks, including OpenAI's GPT-6 Astra, Anthropic's Claude Opus 5.5 and Meta's Muse Spark 1.3 [O2][A9][MT1].
- OpenAI says GPT-6 Astra is its first model to reach the "Critical" cybersecurity level in its own risk framework [O1][O3].
- OpenAI and Anthropic both limit their most sensitive cyber and biology capabilities to vetted organizations, while general versions ship with standard safeguards [O1][A2][A5].
- In a preliminary review, the evaluator METR describes Claude Opus 5.5 as an incremental step rather than a sudden jump in capability [E2].
- OpenAI, Anthropic and a Stanford HAI panel all discussed independent testing of AI and whether frontier development should slow down [O5][A7][H1].

---

## 1. New frontier models and how progress is measured

This was a busy month for model releases. At the same time, evaluators published new data on how quickly capability is rising and how much it costs.

**The releases.** OpenAI released GPT-6 Astra to approved users on September 3, with general availability the next day [O2]. OpenAI calls it a major step-up for cybersecurity, professional work, software engineering and science [O2]. On September 22, OpenAI added two more models: Sol, a reasoning model for complex coding and agent work, and Luna [O4]. Anthropic released Claude Fable 5.1 and Claude Mythos 5.1 on September 1 [A2]. These are the same underlying model, shipped with two different levels of safeguards [A2]. Three weeks later, Anthropic launched Claude Opus 5.5, which it says performs at roughly Fable 5.1's level on most work [A9]. Meta introduced Muse Spark 1.3 on September 2, with better handling of long instructions and confirmation prompts before important actions [MT1].

**Where the sources agree.** Evaluators and labs agree on one broad point: measured capability kept rising. Epoch AI's Capabilities Index (ECI, a single score that combines many benchmarks) gave GPT-6 Astra a score of 166 [E5]. According to Epoch, this is the highest overall ECI score so far, and Astra also set a math record of 170 [E5]. However, Epoch found that Astra still trails Claude Fable 5.1 on software engineering [E5]. Epoch also updated its estimate of frontier growth to roughly 14 ECI points per year since reasoning models appeared [E12]. On Epoch's Furniture Assembly Benchmark, the top score rose from about 52% to 80% in ten months [E10]. Open-weight models (models whose trained parameters are publicly released) lag the best closed models by about seven months on this test [E10].

Prices are falling as well. Epoch estimates that the cost of reaching a fixed level of performance has dropped about 47% per quarter since 2023 [E9]. That is roughly a 13-fold fall per year [E9]. Meanwhile, Anthropic says Opus 5.5 costs about 40% less to run than Opus 5 on typical workloads [A9]. Anthropic also sharply cut Fable 5.1's price for cached input compared with Fable 5 [A2].

No single model leads on everything. In a separate study, Epoch measured time-to-first-token (the wait before a model starts answering) as inputs get longer [E3]. For GPT-5.6, this wait grew quadratically, while Claude Sonnet 5 and Opus 5 showed near-linear growth [E3].

Evaluators are also careful about their own numbers. An Epoch researcher has publicly called the ECI a hard-to-interpret index [E5]. Several Epoch studies this week also rest on small samples, which Epoch itself points out [E3][E9][E10].

**Where the sources differ.** Labs and evaluators describe progress in quite different tones. OpenAI presents Astra as a major step-up across several fields [O2]. Press outlets reported that Meta's Chief AI Officer called Muse Spark 1.3 the company's largest single performance jump [MT1]. That quote was not confirmed on Meta's own page [MT1]. METR, by contrast, calls Claude Opus 5.5 an incremental rather than sudden capability jump [E2]. METR says the model likely gives somewhat greater AI research productivity than the earlier model it compared against [E2]. However, METR still sees weaknesses in long-horizon judgment, foresight and open-ended reasoning compared with expert humans [E2]. Two points matter here. First, these statements are about different models, so they do not directly contradict each other. Second, METR's review was preliminary, based on about ten business days of access and five tasks [E2].

---

## 2. Dangerous capabilities, tiered access and misuse

Cybersecurity and biology were the main risk topics this month. Labs mostly responded by limiting who can use their most powerful capabilities.

**Where the sources agree.** OpenAI says GPT-6 Astra is the first of its models to reach the "Critical" cybersecurity tier [O1][O3]. This tier belongs to OpenAI's Preparedness Framework, the company's own system for rating model risks [O1]. According to OpenAI's system card (a safety document published with a model), Astra can find previously unknown software weaknesses [O3]. The card adds that Astra can build working exploits with limited human guidance [O3]. OpenAI says the most advanced cyber capabilities will go only to vetted defenders through a program called Daybreak Blue [O1].

Anthropic follows a similar tiered approach. Fable 5.1 is generally available, while Mythos 5.1 is restricted to vetted cybersecurity and life-sciences organizations [A2]. On September 17, Anthropic opened applications for its Life Sciences Verification Program [A5]. The program gives checked professionals access to its models, including Mythos for the first time, for work such as drug discovery [A5]. Applicants are reviewed on research credentials, security standards and ethical oversight [A5].

Two companies also reported real-world misuse. Anthropic's threat report covers eight months of disrupted misuse attempts across seven harm areas [A4]. In one case, a suspected Russian espionage group used AI agents to rebuild malware again and again until it avoided detection [A4]. Microsoft says it disrupted "EvilTokens", which it describes as an AI chatbot built for cybercrime [M5]. Beyond the headline, few details of the Microsoft action could be confirmed this week [M5].

Labs are also building misuse detection into their business offerings. Anthropic's Enterprise Frontier Safeguards scan a rolling window of customer traffic for signs of serious cyber or biological misuse [A3]. OpenAI expanded discounted access and cyber-defense support for US federal, state, local and tribal governments [O6].

Finally, an evaluator and a lab both disclosed their own security incidents from earlier in 2026. METR reported a stolen API key in March and systematic probing of its infrastructure in May [E1]. METR believes no sensitive information was accessed, but it treated both events as near-misses [E1]. Anthropic described hardening steps, such as reducing standing access to systems that hold model weights [A1]. It also now blocks outbound traffic from its computing clusters by default [A1]. Both reports are self-assessments, and neither cites an outside audit [E1][A1].

**Where the sources differ.** Not everyone puts restriction first. At a public panel, MIT CSAIL director Daniela Rus and Stanford HAI's James Landay reportedly stressed the value of open-source models [C5]. According to press coverage, they said such models matter for democratization and for security [C5]. Separately, press reports say Meta signaled plans for open-weight Muse models, with no release date given [MT5]. Both of these items are secondary-source. The academic remarks were also general and did not respond to the OpenAI or Anthropic programs.

---

## 3. Safety governance and the "pacing" debate

A shared idea appeared this month: frontier AI may need outside checks and clear rules about when to slow down.

**Where the sources agree.** OpenAI's Chief Global Affairs Officer, Chris Lehane, wrote that voluntary safety commitments are no longer enough [O5]. He called on the US Congress to pass mandatory national AI rules, including independent capability assessments and incident reporting [O5]. The post also asks for common standards on when AI development should slow or stop [O5]. Press reports say a companion OpenAI post described a two-week pause in reinforcement learning (RL, training in which a model learns from rewards) before Astra's release [O1]. We could not confirm this pause on OpenAI's own pages, so please treat it as unverified [O1].

Anthropic announced a partnership with Accenture to evaluate its frontier models independently [A7]. The work includes red-teaming (deliberately attacking a system to find weak points) and safeguard testing [A7]. Anthropic will pay for the work and links it to its CEO's essay "We Must Pace the Frontier" [A7]. The two companies expect to invest at least $1 billion combined over five years [A7]. Anthropic also says outside evaluators, including METR, tested Opus 5.5 before release [A9]. METR then published its own summary of that evaluation [E2]. In the UK, a Turing Institute policy briefing recommends exporting British expertise in AI safety evaluation and assurance [T2].

Microsoft published its third annual Responsible AI Transparency Report [M3]. The report focuses on agentic AI (systems that carry out multi-step tasks with less human oversight) [M3]. Microsoft AI also released a draft Code of Conduct for its MAI models and opened it to six weeks of public comment [M2].

**Where the sources differ.** Academics at Stanford gave a more mixed picture. HAI opened a new seminar series with the question "Should AI Slow Down?" [H1]. HAI says the discussion was partly prompted by a reported incident involving an OpenAI agent and Hugging Face systems [H1]. On the panel, physicist Surya Ganguli said that slowing capability growth looks difficult [H1]. Instead, he called for safety-first design across the whole AI system, including guardrails, cross-checking models and constant monitoring [H1]. Computer scientist Diyi Yang agreed that growth is hard to slow [H1]. However, she argued that pacing should also cover social harms, such as psychological damage and job-market effects [H1]. The panel stayed divided on slowing down versus investing in safety, so there is no single HAI position [H1]. The panelists also did not respond directly to the OpenAI or Anthropic posts.

---

## 4. Monitorability, interpretability and human control

Can people still see and control what AI systems are doing? Industry and academic sources both returned to this question.

**Where the sources agree.** Microsoft's draft code says MAI models must never resist human interruption, correction or shutdown [M2]. It also says the models must never hide their reasoning from auditors [M2]. In a CNBC interview, Microsoft AI CEO Mustafa Suleyman argued that companies should not build systems they cannot control [M7]. At Stanford HAI, panelists asked whether a single "kill switch" can make advanced AI safe [H1].

Academic groups approach the same goal from a technical side. MIT CSAIL's CW-Net translates a self-driving car's decisions into human concepts such as "close to cyclist" [C1]. In tests, these explanations helped drivers and non-experts predict the car's next actions more accurately [C1]. RIKEN AIP director Masashi Sugiyama reportedly described theory research aimed at trust, interpretability and safety [J4]. Interpretability here means understanding how a model reaches its outputs. Meanwhile, Anthropic reported that about 30,000 agents were running at once on its internal research platform, with monitoring in place [A6].

**Where the sources differ.** OpenAI and Microsoft appear to take different positions on how readable AI reasoning must be. See the highlighted box below for details.

---

## 5. AI in science and the automation of AI research

AI is now used widely in scientific work. It is also starting to take on part of the work of building AI itself.

**Where the sources agree.** Anthropic says about 950 Claude agents searched DNA databases for 21 hours to find a new enzyme system [A10]. The system was found in bacteriophages, which are viruses that infect bacteria [A10]. The search narrowed over 200,000 candidates to about 20, a task Anthropic says usually takes scientists weeks to months [A10]. Human scientists carried out all the laboratory experiments [A10]. Anthropic also described how WHO's African regional office uses Claude in an Ebola outbreak response in the Democratic Republic of Congo [A8]. For example, daily situation reports now take under an hour instead of a full day [A8].

Other groups reported similar work. Google DeepMind launched WeatherNext 3, its first weather model to produce hourly forecasts directly from raw satellite images [G1]. At MIT, the xvr system matches surgical X-rays to 3D scans within seconds, with sub-millimeter precision [C3]. MIT also named David Siegel as its 2026–27 Innovation Fellow to explore AI-driven scientific discovery [C4].

Mathematics stands out this month. Epoch launched FrontierMath Erdős, a set of 68 unsolved problems written in Lean (a language for checking proofs) [E6]. In first tests, GPT-6 Astra solved 2 of the 68 problems [E6]. Epoch also found that AI-use acknowledgments in arXiv math papers rose from about 4% in April to about 25% in August [E8]. RIKEN published a recap of its Mathematics & AI Symposium, where about 300 participants discussed formal proof and autonomous discovery [J3]. Search listings also suggest a new JST-ERATO mathematical AI project led by RIKEN AIP's Taiji Suzuki [J1].

AI research itself is also being measured for automation. Anthropic's R&D Automation Index uses a six-level scale that Anthropic says was developed by Epoch AI [A6]. According to Anthropic, Claude "leads" 26% of measured internal research work, up from under 1% in February [A6]. Here, "leads" means Claude completes most of a task from a high-level prompt, under human supervision [A6]. Anthropic adds that no measured area has reached full autonomy [A6]. Sakana AI announced that Jürgen Schmidhuber will guide its Recursive Self-Improvement Lab as Chief Scientific Advisor [S1]. Recursive self-improvement, where AI systems help improve themselves, was also a topic at the Stanford HAI panel [H1].

**Where the sources differ.** The two main measurements give different pictures of AI's role in AI research. Anthropic's internal data suggests Claude already leads about a quarter of measured research work [A6]. In contrast, METR's preliminary review of Opus 5.5 found a likely but incremental productivity gain [E2]. METR also noted clear weaknesses compared with expert humans [E2]. However, the two sources measure different things. One counts shares of supervised internal tasks, while the other tests the model on five tasks against expert-level work [A6][E2].

---

## 6. Agentic products, coding agents and multi-model systems

Many labs launched products this month that let AI agents work on longer tasks with less human input.

**Where the sources agree.** Microsoft redesigned Copilot around three parts, including "Autopilot" [M1]. Autopilot is a persistent agent that keeps working inside Microsoft 365 when the user is not present [M1]. OpenAI's new GPT-6 Sol targets complex coding and agentic workflows [O4]. Anthropic's Claude Code on the web moved from research preview to general availability [A11]. Note that this is a status change for an existing product, not a new launch [A11]. Meta rolled out Muse Spark 1.3 in its Muse Code product [MT1]. Press reports add that Muse Code has now left beta [MT5].

Some companies prefer many specialized models over one large model. Sakana AI's Fugu is not a foundation model but a trained router that sends tasks to a pool of other models [S2]. Demis Hassabis reportedly described Gemini as a layer that could coordinate cheaper, specialized models and agents [G2]. This comes from CNBC's live coverage of a G20 meeting, so the exact wording is approximate [G2].

Products also include safety limits for agents. Muse Spark 1.3 asks users to confirm before it takes consequential actions [MT1]. Claude Code on the web runs tasks in isolated sandboxes and uses a secure Git proxy [A11]. Microsoft's transparency report also centers on how to govern agentic systems [M3].

**Where the sources differ.** Microsoft executive Kathleen Hogan described large efficiency gains from AI agents inside the company [M6]. According to a search summary of her post, supply-chain planning cycles fell from about 10 business days to under 2.5 [M6]. The collector could not check these figures against the original post, so they remain unverified [M6]. Independent engineer Simon Willison offers a more cautious view of software work [W1]. He argues that coding agents make engineering harder, not easier [W1]. In his view, getting their full value needs extraordinary discipline and domain knowledge [W1]. The two speak about different fields, and neither responds to the other.

---

## 7. Compute, chips and national AI sovereignty

Control over AI chips and computing power is becoming a national issue. Sources from several categories touched on it, and none of them disagreed.

**Where the sources agree.** Epoch estimates that about $3 billion of AI chips were smuggled into China through Malaysia [E7]. Its overall estimate for China ranges widely, from 290,000 to 1.6 million H100-equivalent chips [E7]. (An H100-equivalent is a standard unit for comparing AI chip power.) Epoch also estimates that Huawei's 2026 AI compute output is under 4% of Nvidia's [E11]. A new Epoch data explorer estimates compute capacity for major labs, with wide uncertainty ranges [E4].

The Turing Institute's CETaS briefing says the UK has a narrowing window to secure its most critical AI systems and skills [T2]. It frames sovereignty mainly as resilience against single points of failure, not full self-sufficiency [T2]. In Japan, Sakana AI formed a partnership with Sumitomo Corporation and SCSK [S4]. The partners aim to spread domestically developed AI across Japanese industry, starting with finance and manufacturing [S4]. Microsoft also published a post on global AI diffusion, but only its headline could be confirmed this week [M4].

**Where the sources differ.** No disagreement between sources was documented on this theme this week.

---

## 8. Physical and embodied AI: robots, vehicles, medicine and space

Academic groups published several projects aimed at making AI in the physical world more predictable and reliable.

**Where the sources agree.** Besides CW-Net and xvr (see sections 4 and 5), MIT's HardFlow helps generative models follow strict rules [C2]. One example is planning robot paths that are guaranteed to avoid collisions [C2]. A preprint (a paper not yet peer-reviewed) co-authored by CMU researchers proposes a way for robots to learn after deployment [R2]. The method lets a robot adapt to new objects on the device without forgetting earlier skills [R2]. This work supports the Artisan model from a Skylark Labs–CMU partnership, which was announced in August, before this report's window [R1][R2]. At the Turing Institute, an AI model detected unusual light patterns from satellites 88% of the time in testing [T1]. The researchers say this can help with collision avoidance and in-orbit servicing [T1].

Academic leaders also shared a broad vision. CMU's Howie Choset is general chair of the IROS 2026 robotics conference in Pittsburgh [R3]. According to a local newspaper, he hopes for a "democratization of capabilities", with robots used far more widely [R4]. Rus and Landay likewise stressed AI that is grounded in the physical world and supports people rather than replacing them [C5].

**Where the sources differ.** No disagreement between sources was documented on this theme this week.

---

## 9. Other news

A few items did not fit the themes above. At Meta Connect 2026, Meta announced Muse Charm, a small pocket device for talking to its Muse assistant [MT2]. Meta plans to ship it in time for the 2026 holiday season [MT2]. Meta also gave Muse a real-time animated avatar with a face, body and voice [MT3]. In addition, it introduced Ray-Ban Meta Audio, its first camera-free, audio-only glasses [MT4]. OpenAI expanded ChatGPT Ads to seven more Asian markets, reaching more than 60 countries in total [O7].

On the research side, Sakana AI researchers trained networks up to 1,000 layers deep without backpropagation [S3]. Backpropagation is the standard method for training neural networks. The new method's accuracy came within about two percentage points of that standard approach [S3]. CMU's Robotics Institute Pathways Fellowship began its fourth year with a new group of seven fellows [R5]. Finally, RIKEN AIP posted an announcement about the COLT 2027 learning-theory conference [J2].

---

> ### This week's divergent views: How readable should an AI's reasoning be?
>
> OpenAI's system card for GPT-6 Astra discloses an important trade-off [O3]. According to the card, Astra's new "recurrent depth" design produces internal reasoning that is harder to read and monitor than its predecessor's [O3]. The same card reports better resistance to prompt injection (hidden instructions that try to take control of a model) [O3].
>
> Microsoft's draft MAI Code of Conduct takes a different line. It says Microsoft's models must never hide their reasoning from auditors [M2]. On CNBC, Mustafa Suleyman called a reported case of models tampering with their chain-of-thought "a pretty serious situation" [M7]. (A chain-of-thought is the step-by-step reasoning that a model writes out.) Suleyman linked that case to an OpenAI disclosure, but no such OpenAI post appears in this week's collected sources [M7].
>
> Microsoft's documents do not mention GPT-6 Astra directly. Still, the two companies appear to be making different bets on how legible AI reasoning needs to be. We present both positions side by side and do not pick a winner.

---

## Fun corner

**Small model, big claims.** A researcher who blogs as "mvakde" says they trained a tiny, task-specific transformer in about 90 minutes [W2]. According to a third-party digest, it beat several large language models on ARC-style puzzles, which are tests of abstract visual reasoning [W2]. Naturally, Hacker News readers then argued about what such narrow wins really say about general reasoning [W2]. We could not check the exact figures, so enjoy this one as a good story rather than a proven result [W2].

**Agents: not a free lunch.** Meanwhile, Simon Willison has a message for anyone hoping coding agents will do all the hard work [W1]. The more he uses them, he says, the more convinced he becomes that they make software engineering harder [W1]. His advice, in short: bring discipline and real domain knowledge [W1].

---

## Vocabulary corner

1. **pace** (verb) — to control the speed at which something moves or develops.
2. **tiered access** — a system in which different groups of users receive different levels of access.
3. **vetted** — carefully checked and approved before being trusted.
4. **incremental** — happening in small steps rather than in one large jump.
5. **legible** — clear enough to be read and understood.
6. **safeguard** — a rule or tool designed to prevent harm.
7. **near-miss** — an event that almost caused damage but did not.
8. **sovereignty** — a country's power to control its own resources and decisions.

---

## References

Each entry shows: tag, title, source, publication date, item ID and confidence level.

### Evaluators and safety institutes

**UK AI Security Institute:** No new items were found in the collection window. The site was blocked, so an unindexed September post cannot be ruled out.

- **[E1]** METR discloses two 2026 security incidents — METR Official Blog, 2026-08-31 — `metr-security-update-2026-08-31` — primary-confirmed — https://metr.org/blog/2026-08-31-security-update/
- **[E2]** METR predeployment evaluation of Claude Opus 5.5 — METR Official Blog, 2026-09-22 — `metr-claude-opus-5-5-predeployment-eval-2026-09-22` — primary-inferred (comparison model name unverified) — https://metr.org/blog/2026-09-22-claude-opus-5-5/
- **[E3]** Long-context latency scaling — Epoch AI, 2026-09-08 — `epoch-latency-scaling-2026-09-08` — primary-inferred — https://epoch.ai/data-insights/long-context-latency-scaling
- **[E4]** AI Chip Users explorer — Epoch AI, 2026-09-09 — `epoch-ai-chip-users-explorer-2026-09-09` — primary-inferred — https://epoch.ai/data-insights/ai-chip-users
- **[E5]** ECI results for GPT-6 Astra — Epoch AI, 2026-09-16 — `epoch-eci-gpt6-astra-2026-09-16` — primary-inferred — https://epoch.ai/data-insights/eci-gpt-6-astra
- **[E6]** FrontierMath Erdős launch — Epoch AI, 2026-09-16 — `epoch-frontiermath-erdos-launch-2026-09-16` — primary-inferred — https://epoch.ai/frontiermath/erdos
- **[E7]** Chip smuggling to China via Malaysia — Epoch AI, 2026-09-17 — `epoch-chip-smuggling-china-2026-09-17` — primary-inferred — https://epoch.ai/data-insights/chip-smuggling-china-malaysia
- **[E8]** AI-use acknowledgments in arXiv math preprints — Epoch AI, 2026-09-18 — `epoch-arxiv-ai-use-acknowledgments-2026-09-18` — primary-inferred — https://epoch.ai/data-insights/arxiv-ai-acknowledgments
- **[E9]** The plunging price of thought — Epoch AI, 2026-09-22 — `epoch-plunging-price-of-thought-2026-09-22` — primary-inferred — https://epoch.ai/data-insights/plunging-price-of-thought
- **[E10]** Furniture Assembly Benchmark — Epoch AI, 2026-09-23 — `epoch-furniture-assembly-benchmark-2026-09-23` — primary-inferred — https://epoch.ai/data-insights/furniture-assembly-benchmark
- **[E11]** Huawei vs. Nvidia compute roadmap update — Epoch AI, 2026-09-24 — `epoch-huawei-nvidia-compute-roadmap-2026-09-24` — primary-inferred — https://epoch.ai/data-insights/huawei-nvidia-compute-roadmap
- **[E12]** ECI frontier growth-rate update — Epoch AI, 2026-09-25 — `epoch-eci-frontier-growth-rate-update-2026-09-25` — primary-inferred — https://epoch.ai/data-insights/eci-frontier-growth-rate-update

### Industry leaders

**OpenAI**

- **[O1]** Path to Astra (Preparedness Framework preview) — OpenAI Official Blog, 2026-09-01 — `openai-path-to-astra-2026-09-01` — primary-inferred (two-week RL pause is from press reports only) — https://openai.com/index/path-to-astra/
- **[O2]** GPT-6 Astra launch — OpenAI Official Blog, 2026-09-03 — `openai-gpt6-astra-launch-2026-09-03` — primary-inferred — https://openai.com/index/gpt-6-astra/
- **[O3]** GPT-6 Astra safety overview / system card — OpenAI Official Blog / Deployment Safety Hub, 2026-09-03 — `openai-gpt6-astra-system-card-2026-09-03` — primary-inferred — https://openai.com/index/safety-overview-gpt-6-astra/
- **[O4]** Introducing GPT-6 Sol and GPT-6 Luna — OpenAI Official Blog, 2026-09-22 — `openai-gpt6-sol-luna-2026-09-22` — primary-inferred — https://openai.com/index/introducing-gpt-6-sol-and-luna/
- **[O5]** Call for mandatory national AI regulation — OpenAI Official Blog, 2026-09-09 — `openai-ai-policy-window-2026-09-09` — primary-inferred — https://openai.com/index/ai-policy-window/
- **[O6]** Expanded AI access for US governments — OpenAI Official Blog, 2026-09-10 (approximate) — `openai-gov-access-expansion-2026-09-10` — primary-inferred — https://openai.com/index/expanding-ai-access-us-government/
- **[O7]** ChatGPT Ads expansion — OpenAI Official Blog, 2026-09-23 — `openai-chatgpt-ads-expansion-2026-09-23` — primary-inferred — https://openai.com/index/expanding-access-to-ai-with-chatgpt-ads/

**Anthropic**

- **[A1]** Improving alignment and security efforts — Anthropic Official Blog, 2026-08-31 — `anthropic-improving-alignment-security-20260831` — primary-confirmed — https://www.anthropic.com/news/improving-alignment-and-security
- **[A2]** Claude Fable 5.1 and Claude Mythos 5.1 — Anthropic Official Blog, 2026-09-01 — `anthropic-fable-mythos-5-1-20260901` — primary-confirmed — https://www.anthropic.com/claude-fable-and-mythos-5-1
- **[A3]** Enterprise Frontier Safeguards — Anthropic Official Blog, 2026-09-01 — `anthropic-enterprise-frontier-safeguards-20260901` — primary-confirmed — https://www.anthropic.com/news/enterprise-frontier-safeguards
- **[A4]** Threat intelligence report, September 2026 — Anthropic Official Blog, 2026-09-10 — `anthropic-threat-intel-report-20260910` — primary-confirmed — https://www.anthropic.com/threat-intelligence-report-september-2026
- **[A5]** Life Sciences Verification Program — Anthropic Official Blog, 2026-09-17 — `anthropic-life-sciences-verification-program-20260917` — primary-confirmed — https://www.anthropic.com/news/life-sciences-verification-program
- **[A6]** R&D Automation Index (measuring the pace of AI development) — Anthropic Institute, 2026-09-17 (approximate) — `anthropic-rd-automation-index-20260917` — primary-confirmed — https://www.anthropic.com/institute/measuring-pace-of-ai-development
- **[A7]** Accenture embedded evaluation partnership — Anthropic Official Blog, 2026-09-18 — `anthropic-accenture-embedded-evaluation-20260918` — primary-confirmed — https://www.anthropic.com/news/accenture-embedded-evaluation
- **[A8]** Claude in the DRC Ebola response — Anthropic Official Blog, 2026-09-19 — `anthropic-ebola-situation-report-20260919` — primary-confirmed — https://www.anthropic.com/features/ebola-response
- **[A9]** Claude Opus 5.5 launch — Anthropic Official Blog, 2026-09-22 — `anthropic-opus-5-5-20260922` — primary-confirmed — https://www.anthropic.com/claude-opus-5-5
- **[A10]** Claude-assisted discovery of a novel enzyme system — Anthropic Official Blog, 2026-09-23 — `anthropic-novel-enzyme-discovery-20260923` — primary-confirmed — https://www.anthropic.com/news/claude-discovers-novel-enzyme-system
- **[A11]** Claude Code on the web reaches general availability (status update) — Anthropic Official Blog (Claude.com), 2026-09-23 — `anthropic-claude-code-web-ga-20260923` — primary-confirmed — https://claude.com/blog/claude-code-on-the-web

**Google DeepMind** (coverage likely incomplete this week)

- **[G1]** WeatherNext 3 launch — Google DeepMind / Google Blog, 2026-09-03 — `gdm-weathernext3-2026-09-03` — primary-confirmed — https://deepmind.google/science/weathernext/
- **[G2]** Hassabis at the G20 Innovation Ministerial — CNBC live coverage, 2026-09-02 — `gdm-hassabis-g20-2026-09-02` — secondary-source — https://www.cnbc.com/2026/09/02/g20-innovation-ministerial-live-updates.html

**Microsoft**

- **[M1]** New Copilot with Home, Code and Autopilot — The Official Microsoft Blog, 2026-09-25 — `msft-2026-09-25-new-copilot-home-code-autopilot` — primary-inferred — https://blogs.microsoft.com/blog/2026/09/25/introducing-the-new-copilot-with-home-code-and-autopilot/
- **[M2]** Draft MAI Code of Conduct — Microsoft AI, 2026-09-14 — `msft-2026-09-14-mai-code-of-conduct-draft` — primary-inferred — https://microsoft.ai/news/mai-code-of-conduct/
- **[M3]** 2026 Responsible AI Transparency Report — Microsoft On the Issues, 2026-09-01 — `msft-2026-09-01-responsible-ai-transparency-report-2026` — primary-inferred — https://blogs.microsoft.com/on-the-issues/2026/09/01/responsible-ai-in-2026-how-we-are-adapting-for-whats-ahead/
- **[M4]** The continued state of global AI diffusion in 2026 — Microsoft On the Issues, 2026-09-21 — `msft-2026-09-21-global-ai-diffusion-2026` — primary-inferred (headline only) — https://blogs.microsoft.com/on-the-issues/2026/09/21/the-continued-state-of-global-ai-diffusion-in-2026/
- **[M5]** Disrupting EvilTokens — Microsoft On the Issues, 2026-09-22 — `msft-2026-09-22-disrupting-eviltokens` — primary-inferred (headline only) — https://blogs.microsoft.com/on-the-issues/2026/09/22/disrupting-eviltokens-the-ai-chatbot-built-for-cybercrime/
- **[M6]** What we've learned from Microsoft's own AI transformation — The Official Microsoft Blog, 2026-09-17 — `msft-2026-09-17-ai-transformation-lessons` — primary-inferred (figures unverified) — https://blogs.microsoft.com/blog/2026/09/17/what-weve-learned-from-microsofts-own-ai-transformation/
- **[M7]** Mustafa Suleyman interview on CNBC Squawk Box — CNBC, 2026-09-18 — `msft-2026-09-18-suleyman-cnbc-interview` — primary-confirmed — https://www.cnbc.com/video/2026/09/18/microsoft-ai-ceo-mustafa-suleyman-on-ai-we-should-not-create-something-that-we-cant-control.html

**Meta AI**

- **[MT1]** Introducing Muse Spark 1.3 — Meta AI Research Blog, 2026-09-02 — `meta-muse-spark-1-3-release` — primary-inferred (Chief AI Officer quote from press only) — https://research.meta.ai/blog/introducing-muse-spark-1-3
- **[MT2]** Muse Charm device — Meta Newsroom, 2026-09-23 — `meta-connect-2026-muse-charm` — primary-inferred — https://about.fb.com/news/2026/09/the-biggest-news-from-connect-2026/
- **[MT3]** Muse real-time avatar — Meta Official Blog, 2026-09-23 — `meta-connect-2026-muse-realtime-avatar` — primary-inferred — https://www.meta.com/blog/meta-connect-2026-everything-we-announced/
- **[MT4]** Muse in smart glasses; Ray-Ban Meta Audio — Meta Newsroom, 2026-09-23 — `meta-connect-2026-muse-glasses-integration` — primary-inferred — https://about.fb.com/news/2026/09/the-biggest-news-from-connect-2026/
- **[MT5]** Muse Code exits beta; open-weight plans — Meta Official Blog, 2026-09-23 — `meta-connect-2026-muse-code-open-weights` — secondary-source — https://www.meta.com/blog/meta-connect-2026-everything-we-announced/

**Sakana AI**

- **[S1]** Jürgen Schmidhuber joins as Chief Scientific Advisor — Sakana AI Official Blog, 2026-09-24 — `sakana-schmidhuber-advisor-2026-09-24` — primary-inferred — https://sakana.ai/schmidhuber/
- **[S2]** Fugu Max and Fugu Ultra v2 — Sakana AI Official Blog, 2026-09-11 — `sakana-fugu-max-ultra-v2-2026-09-11` — primary-inferred — https://sakana.ai/fugu-max-release/
- **[S3]** PC-ALM, backpropagation-free training — Sakana AI Publications, 2026-09-14 — `sakana-pc-alm-2026-09-14` — primary-inferred — https://pub.sakana.ai/pc-alm/
- **[S4]** Partnership with Sumitomo Corporation and SCSK — Sakana AI Official Blog, 2026-09-10 — `sakana-sumitomo-scsk-partnership-2026-09-10` — primary-inferred — https://sakana.ai/scsk-sc-partnership/

### Public research institutions

**MIT CSAIL**

- **[C1]** CW-Net explains autonomous-vehicle decisions — MIT News, 2026-09-02 — `mit-csail-cwnet-explainable-av-2026-09-02` — primary-confirmed — https://news.mit.edu/2026/system-helps-humans-predict-when-self-driving-cars-will-make-mistakes-0902
- **[C2]** HardFlow for hard constraints in generative AI — MIT News, 2026-09-14 — `mit-csail-hardflow-2026-09-14` — primary-confirmed — https://news.mit.edu/2026/new-method-enables-ai-safety-critical-situations-0914
- **[C3]** xvr surgical X-ray-to-3D registration — MIT News, 2026-09-16 — `mit-csail-xvr-2026-09-16` — primary-confirmed — https://news.mit.edu/2026/new-ai-technique-could-make-minimally-invasive-surgeries-safer-more-precise-0916
- **[C4]** David Siegel named MIT Innovation Fellow — MIT News, 2026-09-23 — `mit-csail-david-siegel-fellow-2026-09-23` — primary-confirmed — https://news.mit.edu/2026/mit-welcomes-david-siegel-innovation-fellow-0923
- **[C5]** Rus and Landay at the "Next Endeavor" panel — Forbes, 2026-09-21 — `mit-csail-next-endeavor-panel-2026-09-21` — secondary-source — https://www.forbes.com/sites/johnwerner/2026/09/21/mit-csail-and-stanford-hai-two-prominent-ai-labs-and-their-common-goals/

**Stanford HAI**

- **[H1]** "Prompt Response" seminar: Should AI Slow Down? — Stanford HAI News, 2026-09-22 (approximate) — `stanford-hai-prompt-response-should-ai-slow-down-2026-09` — primary-inferred — https://hai.stanford.edu/news/can-ai-be-slowed-down-stanford-hai-experts-weigh-the-risks-rules-and-race-ahead

**Carnegie Mellon University Robotics Institute**

- **[R1]** Skylark Labs and CMU RI "Artisan" partnership (out of window; context only) — Tech Times, 2026-08-18 — `cmu-ri-skylark-artisan-partnership-2026-08` — primary-inferred — https://www.techtimes.com/articles/324854/20260818/skylark-labs-carnegie-mellon-researchers-partner-teach-robots-how-pick-unfamiliar-objects.htm
- **[R2]** Continual Field-Adaptive Models (preprint, not peer-reviewed) — arXiv, 2026-09-03 — `cmu-ri-arxiv-cfam-2609.04552` — primary-confirmed — https://arxiv.org/abs/2609.04552
- **[R3]** IROS 2026 in Pittsburgh — CMU News / Robotics Institute, 2026-09-24 (approximate) — `cmu-ri-iros2026-pittsburgh-spotlight` — primary-confirmed — https://www.ri.cmu.edu/global-conference-in-pittsburgh-puts-carnegie-mellons-robotics-leadership-in-the-spotlight/
- **[R4]** Choset previews IROS 2026 — Pittsburgh Post-Gazette, 2026-09-25 — `cmu-ri-choset-iros-vision-postgazette` — secondary-source — https://www.post-gazette.com/business/tech-news/2026/09/25/carnegie-mellon-university-robots-expanded-use-pittsburgh-conference/stories/202609230033
- **[R5]** Pathways Fellowship, year four — Robotics Institute, 2026-09-15 — `cmu-ri-pathways-fellowship-year-four` — primary-confirmed — https://www.ri.cmu.edu/2026-cmu-ri-pathways/

**The Alan Turing Institute**

- **[T1]** AI model detects satellite anomalies — The Alan Turing Institute News, 2026-09-01 — `turing-satellite-anomaly-detection-2026-09-01` — primary-inferred — https://www.turing.ac.uk/news/new-ai-powered-tool-identify-threats-space-and-improve-national-security
- **[T2]** CETaS briefing on UK AI resilience — The Alan Turing Institute / CETaS, 2026-09-02 — `turing-cetas-ai-sovereignty-resilience-2026-09-02` — primary-inferred — https://www.turing.ac.uk/news/uk-must-exploit-narrowing-window-opportunity-build-resilient-ai-future

**University of Tokyo / RIKEN AIP**

- **[J1]** JST-ERATO "Suzuki Mathematical AI Informatics" project — JST ERATO program page, 2026-09-07 (approximate) — `riken-aip-erato-suzuki-mathematical-ai-informatics-2026-09` — secondary-source — https://www.jst.go.jp/erato/suzuki/news.html
- **[J2]** COLT 2027 announcement — RIKEN AIP News listing, 2026-09-07 (approximate) — `riken-aip-colt2027-announcement-2026-09` — secondary-source — https://aip.riken.jp/news-list/
- **[J3]** Mathematics & AI Symposium 2026 recap — RIKEN official news, 2026-09-04 — `riken-math-ai-symposium-2026-recap` — secondary-source — https://www.riken.jp/en/news_pubs/news/2026/20260904_5/index.html
- **[J4]** Masashi Sugiyama interview (in Korean) — ZDNet Korea, 2026-09-18 — `riken-aip-sugiyama-zdnet-korea-interview-2026-09` — secondary-source — https://zdnet.co.kr/view/?no=20260918100536

### Wildcard (independent sources)

- **[W1]** Coding agents are making software engineering harder — Simon Willison's Weblog, 2026-09-24 — `willison-coding-agents-harder-2026-09-24` — primary-inferred — https://simonwillison.net/2026/Sep/24/harder/
- **[W2]** Small transformer trained in about 1.5 hours on ARC puzzles — mvakde's personal blog, 2026-09-02 (approximate) — `mvakde-small-transformer-arc-2026-09` — secondary-source (figures unverified) — https://mvakde.github.io/blog/44-on-arc-1/
