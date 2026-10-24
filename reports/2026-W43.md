# AI Frontier Weekly — 2026-W43

- **Run date:** 2026-10-24
- **Collection timestamp:** 2026-10-24
- **Collection window:** approximately 2026-10-10 to 2026-10-24 (as stated by collectors)
- **Sources:** 15 collector files, 41 items, plus the synthesis file `runs/2026-10-24/argument-map.json`

---

> **Important: please read before using this report**
>
> This week, direct page fetches failed for almost every source website because of a DNS/network block. **No item was read in full.** Most items (31 of 41) come only from search-result titles, snippets or newsroom index pages. Five items come from search digests or third-party reporting. Even the five items marked "primary-confirmed" (Stanford HAI x2, CMU x3) note that the full page was not read.
>
> As a result, **every claim below should be treated as reported, not verified.** All figures (percentages, dollar amounts, megawatts, headcounts) are unverified. Where we write "reportedly" or "according to", we mean it.
>
> **Coverage gaps this week:**
> - **MIT CSAIL:** zero items. The fetch failed, and the collector says this is a gap in collection, not proof that there was no news.
> - **University of Tokyo / RIKEN AIP:** zero items. Access was blocked again, and two web searches found no October 2026 items. This is an access gap, not evidence that nothing was published.
> - **Stanford HAI (medical AI benchmarks item):** the source URL may point to a different article. We mention this item only with a warning, and a human should confirm it.
> - **Epoch AI:** all three items rest on one search digest, and two of them have no article-level URL.
> - **UK AISI:** only one item, and its date is uncertain.
> - **Alan Turing Institute:** no confirmed primary item inside the window.
> - **Balance:** industry sources dominate this week (Anthropic alone provides 8 of 41 items). So any agreement or disagreement between sectors is limited by what we could collect.

---

## Executive summary

- METR (an independent AI evaluation group) reports red-teaming OpenAI's internal agent monitoring and finding several vulnerabilities, though OpenAI's later fixes remain unverified by METR.
- Google, Anthropic and Meta all published their own safety numbers or safety measures, but none of these figures has been checked by an outside party.
- Several labs focused new releases on AI agents, while evaluators and a UK security centre treated agents mainly as a source of risk.
- OpenAI, Anthropic and Google DeepMind each announced programs that give scientific researchers access to their models or compute.
- Coverage is unusually weak this week: almost no page could be opened, and MIT CSAIL and UTokyo/RIKEN AIP returned no items at all.

---

## 1. Third-party evaluation and oversight of frontier labs

Outside evaluators appear to be getting deeper access to the systems of frontier AI labs. This week's items come from METR and Anthropic, plus one UK government blog post. However, all of them are based on snippets or index summaries.

**Where sources agree.** METR, working with Redwood Research, reportedly spent about three weeks in July and August stress-testing OpenAI's internal agent monitoring [metr-2026-10-22-redteam-openai-monitoring, 2026-10-22]. METR's risk-assessment page also lists a review of the "Misalignment in high-stakes settings" section of Anthropic's August 2026 Risk Report [metr-2026-10-20-anthropic-risk-report-review, 2026-10-20]. Only the listing page was seen, so the review's conclusions are unknown. Meanwhile, Anthropic says it has given METR "employee-like" access to evaluate its systems [anthropic-2026-10-15-independent-evaluators, 2026-10-15]. The same post reportedly says talks are underway with other organizations, such as Hugging Face. METR's own account of this arrangement was not collected.

Much of the evaluator and government output this window is about method, not new results. On 14 October, METR published several proposals for outside assessors (independent reviewers) [metr-2026-10-14-assessor-proposals, 2026-10-14]. They cover how to investigate faster AI research and development, how to check control of internal AI agents, and how to inform the public about loss-of-control risks. Similarly, the UK AI Security Institute (AISI) reportedly said it wants to contribute to industry-wide best practice rather than impose mandatory rules [aisi-2026-10-12-technical-best-practice, 2026-10-12]. According to the snippet, the post also argues that capability progress has outpaced some risk-management practices. Note that this item's date is unverified, because the snippet metadata conflicts with it.

**Where sources differ.** Within METR's post, OpenAI reportedly says it has patched the vulnerabilities that affected its production safeguards [metr-2026-10-22-redteam-openai-monitoring]. On the other side, METR says it has not verified OpenAI's claims about later coverage changes [metr-2026-10-22-redteam-openai-monitoring]. METR also says the full report (reportedly 61 pages) was shared only with OpenAI staff, and that METR is publishing only a part of it. Both positions come from the same METR item, and OpenAI's own statement was not collected.

---

## 2. Lab-reported safety and security safeguards vs. questions about measurement

Several labs published safety results from their own testing this window. At the same time, some evaluators and researchers question how far such numbers can be trusted.

**Where sources agree.** Google reports that, on a prompt-injection benchmark (a test of whether hidden instructions can hijack a model), attack success for Gemini 4 Argon fell to 0.7% across 15 adaptive attempts [gdm-gemini-4-argon-safety-2026-10-13, 2026-10-13]. Anthropic reports that new defenses cut illicit distillation (copying a model's abilities by training on its outputs) of Claude by more than 90% [anthropic-2026-10-12-distillation-defenses, 2026-10-12]. Anthropic also describes stronger election safeguards ahead of the 2026 US midterm elections, although the specific measures were not reviewed [anthropic-2026-10-14-us-midterms, 2026-10-14]. Meta says its new Muse Wonder models were trained to refuse harmful requests and to avoid sharing private information without permission [meta-muse-wonder-2026-10, 2026-10-12]. All of these figures and claims are the labs' own.

Cyber capability is a shared topic for industry and evaluators. Google describes Gemini 4 Argon's cyberdefense capabilities as frontier-level and aimed at helping defenders [gdm-gemini-4-argon-safety-2026-10-13]. Meanwhile, a search digest says an Epoch AI data insight estimates that open-weight models (models whose parameters are publicly released) trail closed models on cyber capabilities by about six to seven months [epoch-2026-10-16-open-vs-closed-cyber-gap, 2026-10-16]. According to the same digest, Z.ai's GLM-5.3 is the top open-weight model on Epoch's Cyber ECI. This Epoch item is secondary-source only, and the article URL was not found.

**Where sources differ.** Industry presents numbers from its own tests as evidence that its safeguards work [gdm-gemini-4-argon-safety-2026-10-13; anthropic-2026-10-12-distillation-defenses; meta-muse-wonder-2026-10]. By contrast, METR explicitly says it has not verified OpenAI's patch claims [metr-2026-10-22-redteam-openai-monitoring]. In addition, a Stanford HAI teaser says new Stanford research finds that safety, bias and reasoning benchmarks often fail to measure what they claim to [stanford-hai-2026-10-19-measuring-medical-ai, 2026-10-19]. **Caution:** the URL for this Stanford item may point to a different article, so it should not be relied on until a human confirms it. This is also a difference in emphasis, not a direct exchange: none of these sources responds to another.

---

## 3. Agentic AI: products, standards, and risk

"Agentic" AI means systems that can plan and carry out multi-step tasks on their own. This week, industry and evaluators looked at agents from quite different angles.

**Where sources agree.** Meta announced Muse Wonder and Muse Wonder Full, which it calls its most capable models so far and describes as aimed at agentic tasks [meta-muse-wonder-2026-10, 2026-10-12]. Anthropic is giving its Agent Skills standard to the Agentic AI Foundation, and says more than 70 agent platforms have adopted it [anthropic-2026-10-22-agent-skills-aaif, 2026-10-22]. A Microsoft Foundry blog post reportedly brings the MAI-Code-1.1-Flash model to Foundry fine-tuning (further training on a customer's own data) in public preview [microsoft-foundry-mai-code-1-1-flash-2026-10-22, 2026-10-22]. Only a category listing URL was available for this item. Google DeepMind describes using Google Antigravity as an agentic workbench to find and validate new antimicrobial peptides [gdm-antimicrobial-peptides-antigravity-2026-10-15, 2026-10-15].

An independent developer offers a hands-on example. Simon Willison reportedly built a full browser game mainly with Claude Code, over about 321 commits [willison-battle-drones-2026-10-20, 2026-10-20]. This is a supplementary, informal source, and the numbers are unverified (see the Fun corner below).

**Where sources differ.** Industry and the independent developer frame agents as capability gains, products and shared platforms [meta-muse-wonder-2026-10; anthropic-2026-10-22-agent-skills-aaif; microsoft-foundry-mai-code-1-1-flash-2026-10-22; willison-battle-drones-2026-10-20]. However, evaluators and a security centre frame agents as a risk surface. METR reports finding several vulnerabilities in OpenAI's internal agent monitoring [metr-2026-10-22-redteam-openai-monitoring]. It has also proposed methods for assessing control of internal agents [metr-2026-10-14-assessor-proposals]. Separately, a commentary from CETaS (the Alan Turing Institute's security centre) looks at how AI agents are changing online influence operations [turing-cetas-agents-influence-ops-2026-10, 2026-10]. Its findings were not summarised, and its exact date and URL are unverified, so we cite it only as a topic signal. Again, this is a difference in framing, not a direct debate between named parties.

---

## 4. Frontier labs opening models and compute to scientific researchers

Three industry labs announced programs for scientific researchers in the same two-week window. Two of them focus on the life sciences.

**Where sources agree.** OpenAI announced the GPT-Rosalind Academic Plan, which gives eligible labs at U.S. universities sponsored access to its life-sciences model [openai-rosalind-academic-plan-2026-10-15, 2026-10-15]. Eligibility details are unverified. Anthropic opened a call for life-sciences researchers to apply as guest investigators on joint projects [anthropic-2026-10-22-life-sciences-guest-investigators, 2026-10-22]. Google DeepMind and Google Cloud say they will give up to 200 European researchers access to DeepMind's frontier science models, plus $3 million in compute credits [gdm-european-science-compute-2026-10-14, 2026-10-14].

Labs also described science results from their own models. OpenAI reports new results on open mathematics problems from an internal model [openai-ai-progress-mathematics-2026-10-15, 2026-10-15]. The post also reportedly commits $5 million to a Simons Foundation initiative for mathematicians. Note that this post may first have been published on 6 October, with 15 October as an update date. Google DeepMind described its antimicrobial peptide work [gdm-antimicrobial-peptides-antigravity-2026-10-15]. It also published a global forest map at 10-meter resolution that separates natural, planted and farmed forests, with data from 2017 to 2025 [gdm-forest-types-map-2026-10-22, 2026-10-22].

**Where sources differ.** No divergent views were found. All items in this theme are industry self-reports, and no academic or evaluator response was collected this run.

---

## 5. Lab governance and government partnerships

This theme covers how labs organize themselves and how they work with governments. Singapore appears several times this week.

**Where sources agree.** Anthropic announced a Singapore office and an MOU (memorandum of understanding, a formal but usually non-binding agreement) with the Singapore government on responsible AI adoption [anthropic-2026-10-14-singapore, 2026-10-14]. Google DeepMind and Singapore's Ministry of Digital Development and Information (MDDI) describe a Gemma model trained on local scam conversations [gdm-singapore-scam-detection-2026-10-14, 2026-10-14]. It runs on-device, so private chats stay on the phone. In a related but separate item, Meta said it donated 1,000 Ray-Ban Meta AI glasses to four disability organizations in Singapore [meta-singapore-glasses-donation-2026-10, 2026-10-07]. That item falls outside the window and is context only.

Anthropic also published two governance updates. It says it will commit a portion of its shares to a new Public Benefit Fund, whose stake grows as the company grows [anthropic-2026-10-18-public-benefit-fund, 2026-10-18]. The share amount and governance details are unverified. In addition, physicist and former Harvard science dean Christopher Stubbs has joined Anthropic's Long-Term Benefit Trust [anthropic-2026-10-21-stubbs-ltbt, 2026-10-21].

**Where sources differ.** No divergent views were found. A Microsoft post on digital sovereignty touches on customer control, but it is mostly about enterprise cloud (see section 7).

---

## 6. AI compute and data-center infrastructure

Two items describe the physical build-out behind frontier AI. Both should be read with care.

**Where sources agree.** According to a search digest of Epoch AI's data hub, Colossus 2 is the largest tracked AI data center, at about 946 MW of IT power [epoch-2026-10-ai-data-centers-hub-update, collected 2026-10-24]. Anthropic-Amazon New Carlisle reportedly follows at about 910 MW. The database reportedly covers about 44% of global deployed AI compute, but with a wide uncertainty range of 30% to 79%. The date here is the collection date, not a release date. Meanwhile, Meta's engineering blog describes new AI-cluster networking hardware shown at OCP Summit 2026 [meta-ocp-summit-2026-networking, 2026-10-12]. This includes IcePack, its first liquid-cooled network rack, the IceCube 102.4T switch blade, and open-source MetaRoCE transport software.

**Where sources differ.** No divergent views were found. There are only two items, and the Epoch figures are secondary-source.

---

## 7. Miscellaneous developments

These items do not form a single clear theme. We group them loosely and do not claim any wider pattern.

**Work and accountability (academic).** Stanford HAI describes Digital Economy Lab dashboards that track how AI adoption relates to jobs and the economy [stanford-hai-2026-10-21-ai-labor-dashboards, 2026-10-21]. Early findings reportedly show employment among 22- to 25-year-olds in software development and customer service falling over 3% a year since late 2022. However, the researchers caution that the ADP data may not be fully representative. In a separate HAI Q&A, Deb Raji argues that accountability disappears when the link between actions and outcomes is hidden [stanford-hai-2026-10-14-who-is-responsible-ai-harm, 2026-10-14].

**Memory features.** Two unrelated products added user memory tools. Sakana Chat's "My Fish" feature shows users what the chatbot remembers about them, and memory can be switched off [sakana-my-fish-2026-10-15, 2026-10-15]. Meta's Muse Wonder includes a feature called Active Memory [meta-muse-wonder-2026-10]. This is only a loose overlap.

**Robot safety awards at CMU.** Andrea Bajcsy of the CMU Robotics Institute was named one of 20 Packard Fellows for 2026, with about $985,834 over five years [cmu-ri-bajcsy-packard-2026-10-15, 2026-10-15]. She was also named a 2026 AI2050 Early Career Fellow, a Schmidt Sciences program aimed at safer AI [cmu-ri-bajcsy-ai2050-2026-10-14, 2026-10-14]. These are awards, not research results. For context, the IROS robotics conference returned to Pittsburgh on 1 October, outside the window [cmu-iros-2026-facilities-tours, 2026-10-01].

**Other single-source items.**
- Sakana AI described QD-Rec, a quality-diversity method (one that seeks results that are both good and varied) for recommendations, and reports better ratings than baselines in many settings [sakana-qd-rec-2026-10-20, 2026-10-20].
- In an event report, Sakana AI said it plans to at least double its engineering headcount and pursue large-scale pretraining [sakana-open-house-2026-10-21, 2026-10-21].
- A search digest says Epoch AI released a Chess Puzzles v2 benchmark, but its contents are unconfirmed [epoch-2026-10-14-chess-puzzles-v2, 2026-10-14].
- Microsoft described digital-sovereignty options for customers who want more control over data, and GitHub Enterprise Local is reportedly expected at Microsoft Ignite [microsoft-digital-sovereignty-2026-10-20, 2026-10-20].
- Meta, Milan's Pinacoteca di Brera and EssilorLuxottica are piloting AI glasses for blind and low-vision museum visitors [meta-brera-ai-glasses-2026-10, 2026-10-14].
- The Alan Turing Institute has a funding call on non-terrestrial network vulnerabilities, reportedly closing on 27 October 2026 [turing-ntn-call-for-proposals-2026, publication date unknown].
- A secondary report says a Turing and University of Birmingham model can label satellite parts in radar images [turing-satellite-component-radar-ai-2026-10, 2026-10-09]. This is research-stage work, dated one day before the window.

---

> ## This week's divergent views
>
> **Who checks the checkers' findings?**
>
> METR reports that it stress-tested OpenAI's internal agent monitoring and found several vulnerabilities. According to METR's post, OpenAI says it has patched the problems that affected its production safeguards. However, METR says it has not verified OpenAI's claims about later coverage changes. In addition, the full report was shared only with OpenAI staff, and the public sees only a part of it. [metr-2026-10-22-redteam-openai-monitoring, 2026-10-22]
>
> More broadly, labs this week offered their own safety numbers, such as a 0.7% prompt-injection success rate and a 90%+ cut in distillation [gdm-gemini-4-argon-safety-2026-10-13; anthropic-2026-10-12-distillation-defenses]. None of these numbers has been checked by an outside party in our sources.
>
> We do not pick a side here. Both views in the METR case come from one item that we saw only through search excerpts. OpenAI's own statement was not collected.

---

## Fun corner

What happens when you ask coding agents to build a video game? Simon Willison found out. He describes Battle Drones, a browser-based real-time strategy game in the style of Command & Conquer [willison-battle-drones-2026-10-20, 2026-10-20]. He built it mainly with Claude Code, reportedly over about 12 major versions and 321 commits.

The best part is the multiplayer mode. Two nearby devices can reportedly play against each other by sending data through sound. For online games, he uses a small WebSocket relay (a simple server that passes messages between players). He estimates it costs only a couple of dollars a month.

It is a fun demo, not a polished product. The numbers come from search excerpts and have not been checked. Still, it is a nice reminder that people are already building real things with agents.

---

## Vocabulary corner

1. **red-teaming** — testing a system by acting like an attacker, in order to find its weak points.
2. **safeguard** — a measure designed to prevent harm or misuse.
3. **prompt injection** — an attack that hides instructions in text so that an AI model follows them by mistake.
4. **distillation** — training a new model by copying the outputs of an existing, stronger model.
5. **open-weight model** — an AI model whose trained parameters are publicly released for anyone to download.
6. **benchmark** — a standard test used to measure and compare performance.
7. **hedge (a claim)** — to use careful words like "reportedly" so you do not state something more strongly than the evidence allows.
8. **memorandum of understanding (MOU)** — a formal written agreement that describes shared goals but is usually not legally binding.

---

## References

All dates are publication dates as reported by collectors. Most are unverified (see the note at the top).

### Evaluation and safety institutes

**METR**
- METR Blog — Red-teaming OpenAI agent monitoring (2026-10-22): https://metr.org/blog/2026-10-22-red-teaming-openai-agent-monitoring/ [metr-2026-10-22-redteam-openai-monitoring]
- METR Risk Assessment page — review of Anthropic's August 2026 Risk Report (2026-10-20): https://metr.org/risk-assessment/ [metr-2026-10-20-anthropic-risk-report-review]
- METR Blog — Assessor proposals (2026-10-14) [metr-2026-10-14-assessor-proposals]:
  - https://metr.org/blog/2026-10-14-control-assessment-proposal/
  - https://metr.org/blog/2026-10-14-ai-rd-acceleration-assessment-proposal/
  - https://metr.org/blog/2026-10-14-better-informing-the-public-about-loss-of-control-risks/
  - https://metr.org/blog/2026-10-14-our-approach-to-risk-assessment/

**Epoch AI** (all secondary-source, via search digest)
- Chess Puzzles benchmark (2026-10-14): https://epoch.ai/benchmarks/chess-puzzles [epoch-2026-10-14-chess-puzzles-v2]
- Data Insights index, open vs. closed cyber gap (2026-10-16): https://epoch.ai/data-insights [epoch-2026-10-16-open-vs-closed-cyber-gap]
- AI data centers database (collected 2026-10-24): https://epoch.ai/data/ai-data-centers [epoch-2026-10-ai-data-centers-hub-update]

**UK AI Security Institute**
- Towards technical best practice for frontier AI development (2026-10-12, date unverified): https://www.aisi.gov.uk/blog/towards-technical-best-practice-for-frontier-ai-development [aisi-2026-10-12-technical-best-practice]

### Industry leaders

**OpenAI**
- Introducing the Rosalind Academic Plan (2026-10-15): https://openai.com/index/introducing-the-rosalind-academic-plan/ [openai-rosalind-academic-plan-2026-10-15]
- Sharing AI progress in mathematics (2026-10-15 update; possibly first published 2026-10-06): https://openai.com/index/sharing-ai-progress-in-mathematics/ [openai-ai-progress-mathematics-2026-10-15]

**Anthropic**
- Donating Agent Skills to the Agentic AI Foundation (2026-10-22): https://www.anthropic.com/news/donating-agent-skills-to-the-agentic-ai-foundation [anthropic-2026-10-22-agent-skills-aaif]
- Open call for guest investigators in the life sciences (2026-10-22): https://www.anthropic.com/news/open-call-guest-investigators-life-sciences [anthropic-2026-10-22-life-sciences-guest-investigators]
- Christopher Stubbs joins the Long-Term Benefit Trust (2026-10-21): https://www.anthropic.com/news/christopher-stubbs-joins-long-term-benefit-trust [anthropic-2026-10-21-stubbs-ltbt]
- Public Benefit Fund (2026-10-18): https://www.anthropic.com/news/public-benefit-fund [anthropic-2026-10-18-public-benefit-fund]
- An update on independent evaluators (2026-10-15): https://www.anthropic.com/news/an-update-on-independent-evaluators [anthropic-2026-10-15-independent-evaluators]
- Preparing for the 2026 US midterms (2026-10-14): https://www.anthropic.com/news/2026-us-midterms [anthropic-2026-10-14-us-midterms]
- Singapore office opening (2026-10-14): https://www.anthropic.com/news/singapore-office-opening [anthropic-2026-10-14-singapore]
- Strengthening defenses against distillation attacks (2026-10-12): https://www.anthropic.com/news/distillation-defenses [anthropic-2026-10-12-distillation-defenses]

**Google / Google DeepMind**
- Gemini 4 Argon model safety and security (2026-10-13): https://blog.google/innovation-and-ai/technology/safety-security/gemini-4-model-safety-security/ [gdm-gemini-4-argon-safety-2026-10-13]
- Powering European scientific discovery (2026-10-14): https://blog.google/innovation-and-ai/models-and-research/google-deepmind/were-powering-european-scientific-discovery-with-advanced-ai-compute-and-frontier-models/ [gdm-european-science-compute-2026-10-14]
- On-device AI scam detection with MDDI (2026-10-14): https://deepmind.google/blog/on-device-ai-scam-detection-mddi/ [gdm-singapore-scam-detection-2026-10-14]
- Accelerating antimicrobial discovery (2026-10-15): https://deepmind.google/blog/accelerating-antimicrobial-discovery/ [gdm-antimicrobial-peptides-antigravity-2026-10-15]
- Beyond tree cover: mapping the world's forest types (2026-10-22): https://deepmind.google/blog/beyond-tree-cover-mapping-the-worlds-forest-types/ [gdm-forest-types-map-2026-10-22]

**Microsoft**
- Advancing digital sovereignty with greater control and choice (2026-10-20): https://blogs.microsoft.com/blog/2026/10/20/advancing-digital-sovereignty-with-greater-control-and-choice [microsoft-digital-sovereignty-2026-10-20]
- Microsoft Foundry Blog listing, MAI-Code-1.1-Flash fine-tuning (around 2026-10-22): https://techcommunity.microsoft.com/category/azure-ai-foundry/blog/azure-ai-foundry-blog [microsoft-foundry-mai-code-1-1-flash-2026-10-22]

**Meta**
- Introducing Muse Wonder models (2026-10-12): https://about.fb.com/news/2026/10/introducing-muse-wonder-models/ [meta-muse-wonder-2026-10]
- OCP Summit 2026 networking (2026-10-12): https://engineering.fb.com/2026/10/12/open-source/ocp-summit-2026-powering-ai-with-open-innovations-in-scale-up-scale-out-and-scale-across-networks/ [meta-ocp-summit-2026-networking]
- Pinacoteca di Brera AI glasses pilot (2026-10-14): https://about.fb.com/news/2026/10/meta-milans-pinacoteca-di-brera-and-essilorluxottica-expand-access-to-art-through-ai-glasses/ [meta-brera-ai-glasses-2026-10]
- 1,000 AI glasses donated in Singapore (2026-10-07, outside window): https://about.fb.com/news/2026/10/meta-donates-1000-ai-glasses-to-singapores-disability-community/ [meta-singapore-glasses-donation-2026-10]

**Sakana AI**
- QD-Rec (2026-10-20): https://sakana.ai/qd-rec/ (technical page: https://pub.sakana.ai/qd-rec/) [sakana-qd-rec-2026-10-20]
- My Fish (2026-10-15): https://sakana.ai/my-fish/ [sakana-my-fish-2026-10-15]
- Engineer Open House 2026 report (2026-10-21): https://sakana.ai/open-house-2026/ [sakana-open-house-2026-10-21]

### Public research institutions

**Stanford HAI**
- Tracking AI's real-time footprint on the labor market (2026-10-21): https://hai.stanford.edu/news/tracking-ais-real-time-footprint-on-the-labor-market [stanford-hai-2026-10-21-ai-labor-dashboards]
- Measuring what medical AI can actually do (2026-10-19) — **URL MATCH UNCERTAIN; may be a different article**: https://hai.stanford.edu/news/stanford-develops-real-world-benchmarks-for-healthcare-ai-agents [stanford-hai-2026-10-19-measuring-medical-ai]
- Who is responsible when AI causes harm? (2026-10-14): https://hai.stanford.edu/news/who-is-responsible-when-ai-causes-harm [stanford-hai-2026-10-14-who-is-responsible-ai-harm]

**Carnegie Mellon University**
- Bajcsy awarded Packard Fellowship (2026-10-15): https://www.ri.cmu.edu/bajcsy-awarded-packard-fellowship-for-science-and-engineering/ [cmu-ri-bajcsy-packard-2026-10-15]
- AI2050 Fellows (2026-10-14): https://www.cs.cmu.edu/news/2026/ai2050-fellows [cmu-ri-bajcsy-ai2050-2026-10-14]
- IROS 2026 facilities tours (2026-10-01, outside window): https://www.cmu.edu/news/stories/archives/2026/october/cmu-robotics-expertise-and-facilities-attract-iros-2026-conference-attendees [cmu-iros-2026-facilities-tours]

**The Alan Turing Institute**
- CETaS commentary on AI agents and influence operations (2026-10, exact date and article URL unverified): https://cetas.turing.ac.uk/ [turing-cetas-agents-influence-ops-2026-10]
- Call for proposals: non-terrestrial network vulnerabilities (publication date unknown): https://www.turing.ac.uk/work-turing/call-proposals-2026-vulnerabilities-and-mitigation-non-terrestrial-networks [turing-ntn-call-for-proposals-2026]
- Satellite-component radar AI model (2026-10-09, secondary source): https://letsdatascience.com/news/turing-researchers-develop-ai-model-to-identify-satellite-co-838fd808 [turing-satellite-component-radar-ai-2026-10]

**MIT CSAIL** — no items collected (fetch failed; gap in collection, not absence of news).

**University of Tokyo / RIKEN AIP** — no items collected (access blocked; gap in collection, not absence of news).

### Wildcard (supplementary)
- Simon Willison's Weblog — Battle Drones (2026-10-20): https://simonwillison.net/2026/Oct/20/battledrones/ [willison-battle-drones-2026-10-20]
