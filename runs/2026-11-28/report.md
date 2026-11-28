# AI Frontier Weekly — 2026-W48

**Run date:** 2026-11-28 · **Window covered:** nominally 2026-11-18 to 2026-11-28 · **Collection started:** 2026-11-28T00:05Z

Citations appear in square brackets as collector item IDs, for example `[metr-2026-11-20-q4-capability-update]`. Each ID matches one entry in the References section and one item in `runs/2026-11-28/collectors/`.

> ### About this week's sources
>
> Please read this note before the rest of the report. Our collectors could read only Anthropic's three items directly from the official pages [anthropic-ipo-pricing-2026-11-18][anthropic-ipo-close-2026-11-20][anthropic-fable-mythos-5-2-2026-11-09]. Access to nearly every other source site was blocked. As a result, almost all other items were rebuilt from search-engine snippets.
>
> - **(inferred)**: items from METR, OpenAI, Microsoft, Meta and RIKEN come from search snippets of official pages. Nobody read the pages themselves.
> - **(second-hand)**: items from Google DeepMind, Sakana AI, Stanford HAI, the Alan Turing Institute and the Tokyo Forum come from search summaries or third-party reports.
> - Several items are dated before the 18–28 November window. We keep their real dates and do not suggest that everything happened this week.
> - Some items cite an index page (a list of posts) rather than the article itself.
> - Epoch AI, the UK AI Security Institute, MIT CSAIL and the CMU Robotics Institute returned no verifiable items. The wildcard collector also returned nothing. **This is a collection gap, not proof that these groups published nothing.**
>
> In the text, we use words like "reportedly" and "according to a search summary" for anything not confirmed at the source. Figures from snippets have not been checked against the original pages, so please treat them as unverified.

---

## 1. Executive summary

- Anthropic completed its stock-market listing and reports about $119.5 billion in combined gross proceeds from its IPO and a private placement [anthropic-ipo-close-2026-11-20].
- Five labs released, or reportedly released, new models, but only Anthropic's Fable 5.2 and Mythos 5.2 release was confirmed at the source [anthropic-fable-mythos-5-2-2026-11-09][openai-gpt-6-2-astra-sol-2026-11-17][msft-mai-seven-models-2026-11-17][gdm-gemini-robotics-2-5-2026-11][sakana-namazu-small-2026-11-25].
- According to search summaries of METR's pages, AI capabilities that matter for AI research are growing fast but becoming harder to measure [metr-2026-11-20-q4-capability-update][metr-2026-11-05-anthropic-ai-rd-acceleration-assessment].
- Microsoft and Meta reportedly put model weights in outside hands, while Anthropic offers its less-restricted Mythos 5.2 only to vetted organisations [msft-mai-seven-models-2026-11-17][meta-open-weight-medicine-2026-11][anthropic-fable-mythos-5-2-2026-11-09].
- Academic and policy groups, according to search summaries, describe AI as moving faster than governance and society's ability to respond [turing-2026-11-17-resilience-agenda][turing-2026-11-18-ai-disruption-roadmap][hai-2026-11-10-ai100-third-report].

---

## 2. New models, and how well we can measure them

November brought a wave of model announcements from industry labs. However, the evidence behind them varies a lot. Only one release was read directly at the source. Also, most capability figures come from the developers themselves.

**Anthropic** *(confirmed)*. Anthropic introduced Claude Fable 5.2 and Claude Mythos 5.2 on 9 November, just before our window [anthropic-fable-mythos-5-2-2026-11-09]. Fable 5.2 is available through the API and on major cloud platforms [anthropic-fable-mythos-5-2-2026-11-09]. It costs $8 per million input tokens and $40 per million output tokens (tokens are small pieces of text a model reads or writes) [anthropic-fable-mythos-5-2-2026-11-09]. Anthropic says Fable 5.2 beats Claude Opus 5.5 on nearly all evaluated capabilities and is about 30% faster than Fable 5.1 [anthropic-fable-mythos-5-2-2026-11-09]. Mythos 5.2 is the same underlying model, but with certain cyber and biology safeguards removed [anthropic-fable-mythos-5-2-2026-11-09]. These capability and safety claims are Anthropic's own, and this run did not check them independently [anthropic-fable-mythos-5-2-2026-11-09].

**OpenAI** *(inferred)*. According to search snippets of OpenAI's release notes, GPT-6.2 Astra and Sol launched on 17 November in ChatGPT Work, Codex and the API [openai-gpt-6-2-astra-sol-2026-11-17]. Astra is reportedly positioned for complex work, while Sol targets reasoning with speed and efficiency [openai-gpt-6-2-astra-sol-2026-11-17]. A GPT-6.2 version for the chat tab reportedly followed on 23 November for Plus, Pro, Business and Enterprise users [openai-gpt-6-2-astra-sol-2026-11-17].

**Microsoft** *(inferred)*. Around its Ignite 2026 conference, Microsoft AI reportedly launched seven new MAI models for coding, security, image editing and voice [msft-mai-seven-models-2026-11-17][msft-ignite-2026-mai-keynote]. Snippets name MAI Code 2, Code 2 Flash, MAI Cyber 2 Flash, MAI Image 2.7 and MAI Realtime 1 [msft-mai-seven-models-2026-11-17]. Microsoft also compares cost and performance against GPT 6 Astra, but these are unverified vendor claims [msft-mai-seven-models-2026-11-17].

**Google DeepMind** *(second-hand)*. Third-party reports say DeepMind released Gemini Robotics 2.5, a vision-language-action model (a model that links what it sees and reads to physical actions) [gdm-gemini-robotics-2-5-2026-11]. One report claims 30% to 100% higher success rates across 200 manipulation tasks, but no DeepMind page was read to confirm this [gdm-gemini-robotics-2-5-2026-11]. The reports also disagree on whether the release date was 10 or 11 November [gdm-gemini-robotics-2-5-2026-11].

**Sakana AI** *(second-hand)*. A search summary of Sakana's blog lists a Namazu Small release dated 25 November [sakana-namazu-small-2026-11-25]. Namazu is described as Sakana's Japanese-focused language model, but no size, benchmark or licence details could be read [sakana-namazu-small-2026-11-25].

**Where the sources agree.** Two labs released models aimed at cybersecurity this period. These were Anthropic's Mythos 5.2 and, reportedly, Microsoft's MAI Cyber 2 Flash [anthropic-fable-mythos-5-2-2026-11-09][msft-mai-seven-models-2026-11-17]. An evaluator and a lab also both describe continued capability growth. According to a search summary, METR's Q4 update covers models up to Opus 5.5 and GPT-6 Astra [metr-2026-11-20-q4-capability-update]. The same summary says time horizons (roughly, how long a task an AI model can handle) double about every 3.6 months [metr-2026-11-20-q4-capability-update]. It also reportedly says models do worse on tasks that are costlier to turn into training environments [metr-2026-11-20-q4-capability-update]. The 3.6-month figure still needs checking against METR's original page [metr-2026-11-20-q4-capability-update].

**Where they pull apart.** Anthropic reports low alignment risk (the risk that a model acts against its developers' intentions) in high-stakes settings [anthropic-fable-mythos-5-2-2026-11-09]. Meanwhile, METR's research reportedly raises a general question about how reliable such tests can be [metr-2026-11-16-alignment-eval-tells]. We explore this tension in the "divergent views" box below.

---

## 3. The pace of progress, and AI that speeds up AI research

This theme rests almost entirely on METR's work, seen only through search summaries. The picture is consistent: progress is fast, and part of the speed may come from AI helping to build AI.

According to a search summary, METR estimates that Anthropic's progress on well-specified tasks runs at roughly twice its pre-October-2025 pace [metr-2026-11-05-anthropic-ai-rd-acceleration-assessment]. METR reportedly attributes most of this speed-up to Anthropic's own use of AI in research and development [metr-2026-11-05-anthropic-ai-rd-acceleration-assessment]. It reportedly sees no convincing bottlenecks over the next 12 months [metr-2026-11-05-anthropic-ai-rd-acceleration-assessment]. However, METR stresses high uncertainty, and the public version of the report is redacted [metr-2026-11-05-anthropic-ai-rd-acceleration-assessment].

On the same day, METR reportedly published an external review of the automated-R&D section in Anthropic's August 2026 Risk Report [metr-2026-11-05-review-anthropic-risk-report-rd-section]. Per the snippet, METR judged this risk "low" for the models available at the time, although this still needs verification [metr-2026-11-05-review-anthropic-risk-report-rd-section]. The Q4 update's reported 3.6-month doubling time points in the same direction [metr-2026-11-20-q4-capability-update].

An academic voice reportedly agrees that progress has been unexpectedly fast. According to a search snippet, the third AI100 report, covered by Stanford HAI, describes AI as outrunning both expectations and governance [hai-2026-11-10-ai100-third-report]. That coverage is dated 10 November, before our window [hai-2026-11-10-ai100-third-report].

We found no opposing view on this theme in this week's material. Given the thin evaluator coverage, that absence should not be read as agreement.

---

## 4. Who gets the weights? Open access versus gated access

Labs are making different choices about who can hold and run their models. Model weights (the learned numbers inside a model) are at the centre of this choice.

On one side, several organisations reportedly give weights to others. Microsoft's MAI Licensed Weights lets customers customise a frontier MAI model with their own data [msft-mai-seven-models-2026-11-17]. Customers then run the model in their own Azure environment [msft-mai-seven-models-2026-11-17]. A Meta newsroom post title says researchers are using Meta's open-weight models (models whose weights anyone can download) to transform medicine [meta-open-weight-medicine-2026-11]. Only the title was seen, so the details are unknown [meta-open-weight-medicine-2026-11]. Sakana's Namazu is also described as post-trained from an open model [sakana-namazu-small-2026-11-25].

On the other side, Anthropic uses gated access (access limited to approved users). It restricts Mythos 5.2 to vetted cybersecurity and life-sciences organisations [anthropic-fable-mythos-5-2-2026-11-09]. Meanwhile, Fable 5.2, which keeps those safeguards, is offered more widely through the API and cloud platforms [anthropic-fable-mythos-5-2-2026-11-09].

One caveat matters here. These are different products with different risk profiles, so this is a contrast in strategy rather than a direct debate. None of the companies is responding to the others in the collected material.

---

## 5. AI agents for consumers and businesses

Several labs launched or extended agent products this period. An AI agent is a system that carries out multi-step tasks for a user, often with some independence.

According to search snippets, OpenAI's Businesses in ChatGPT is a beta hub where companies claim a listing and talk to users through Business Agents [openai-businesses-chatgpt-intl-2026-11-19]. A 19 November update reportedly made ecommerce and online service businesses outside the US eligible [openai-businesses-chatgpt-intl-2026-11-19]. Meta's newsroom has a post titled "Introducing Muse in the UK: A Personal AI Agent You Control" [meta-muse-uk-2026-11]. This suggests Meta is extending Muse to UK users, but the post body could not be read [meta-muse-uk-2026-11].

Microsoft's Ignite announcements reportedly included Copilot Workspaces, a shared space for people and agents [msft-ignite-2026-nadella-keynote]. Secondary summaries also mention Project Perception security agents, Agent 365 Business Analytics and Microsoft IQ [msft-ignite-2026-nadella-keynote]. In addition, they mention an AI Transparency Initiative with more than 40 organisations [msft-ignite-2026-nadella-keynote]. Note that Nadella's keynote transcript itself was not read [msft-ignite-2026-nadella-keynote].

Sakana's Marlin is its first commercial product, an autonomous research assistant [sakana-marlin-update-2026-11-26]. A search summary reports a 26 November update with new research modes and a revised slide output [sakana-marlin-update-2026-11-26].

Slides were a small shared trend. According to OpenAI's release notes, ChatGPT Space, a tool for interactive pages and presentations, reached Plus users on 20 November [openai-chatgpt-space-plus-2026-11-20]. Together with Marlin's revised slide output, two labs shipped presentation tools in the same week [openai-chatgpt-space-plus-2026-11-20][sakana-marlin-update-2026-11-26].

---

## 6. AI in science, medicine and checking outputs

Both industry and academia reported work in health and biology this period. However, most items rest on titles or short snippets, so the details are thin.

DeepMind's blog index reportedly lists a November post titled "AlphaGenome 2" [gdm-alphagenome-2-2026-11]. According to the index title, it is about how cells read DNA, to better understand disease [gdm-alphagenome-2-2026-11]. According to a single search snippet, healthcare model configurations became available in the OpenAI API on 24 November [openai-healthcare-api-configs-2026-11-24]. Meta's post on open-weight models in medicine also belongs here, although only its title was seen [meta-open-weight-medicine-2026-11].

From academia, Stanford HAI reportedly covered a computer-vision system that monitors intensive-care patients 24 hours a day [hai-2026-11-20-icu-delirium-monitoring]. The system tracks patient activity and helps clinicians spot subtle signs of delirium [hai-2026-11-20-icu-delirium-monitoring]. Its peer-review status is unknown [hai-2026-11-20-icu-delirium-monitoring].

A second thread is about checking what AI and software produce. DeepMind's blog index reportedly lists a post called "AlphaProof Code", about verifying complex software [gdm-alphaproof-code-2026-11]. Only the title is known [gdm-alphaproof-code-2026-11]. Meanwhile, a Stanford-covered study built a benchmark from documented cases of AI hallucination (when an AI states false information as if it were true) [hai-2026-11-19-court-ai-hallucination-study]. The researchers reportedly used it to calibrate detectors and track generative AI use in four US state courts [hai-2026-11-19-court-ai-hallucination-study].

No disagreement appears in this theme.

---

## 7. Big money versus societal resilience

This theme shows a difference in focus rather than a direct argument. Industry announcements talked about capital and scale. Meanwhile, academic and policy groups talked about risk and readiness.

**The industry side.** Anthropic priced its IPO on 18 November at $83.00 per share [anthropic-ipo-pricing-2026-11-18]. Trading was set to begin on 19 November on the Nasdaq Global Select Market under the ticker ANT [anthropic-ipo-pricing-2026-11-18]. On 20 November, Anthropic reported that the IPO had closed with 1.127 billion shares sold [anthropic-ipo-close-2026-11-20]. That total includes the underwriters' full option of 147 million shares, and it raised about $93.5 billion gross [anthropic-ipo-close-2026-11-20]. The earlier figure of 980 million shares did not include that option, so the two numbers do not contradict each other [anthropic-ipo-pricing-2026-11-18][anthropic-ipo-close-2026-11-20].

Anthropic also ran a private placement (a sale of shares directly to selected investors) of about 313 million Class N shares [anthropic-ipo-close-2026-11-20]. The buyers were AMD, Broadcom, Google, Micron, Microsoft, NVIDIA and TSMC Partners, for about $26.0 billion [anthropic-ipo-close-2026-11-20]. Combined gross proceeds came to about $119.5 billion, according to Anthropic [anthropic-ipo-close-2026-11-20]. At Ignite, Mustafa Suleyman reportedly framed Microsoft AI's strategy as frontier capability at a price organisations can afford at scale [msft-ignite-2026-mai-keynote].

**The academic and policy side.** According to a search listing, the Alan Turing Institute published an agenda called "Securing Resilience for the Age of AI" [turing-2026-11-17-resilience-agenda]. It reportedly proposes five Transformational Resilience Goals [turing-2026-11-17-resilience-agenda]. CEO George Williamson reportedly warned that the UK faces growing risks of cascading disruption and needs new AI capabilities [turing-2026-11-17-resilience-agenda]. A separate listing mentions a Turing policy roadmap: the UK will reportedly be increasingly exposed to AI disruption unless it takes practical steps [turing-2026-11-18-ai-disruption-roadmap]. These two Turing items may describe the same story [turing-2026-11-18-ai-disruption-roadmap]. As noted above, the AI100 report reportedly says AI has outrun governance [hai-2026-11-10-ai100-third-report].

Public forums also discussed AI's direction. Stanford HAI recapped its 28 October fall conference, "AI's Future Is Still a Choice" [hai-2026-11-18-ais-future-is-still-a-choice]. The event was organised around the tension between hope and fear about AI [hai-2026-11-18-ais-future-is-still-a-choice]. According to a search summary, the University of Tokyo and Korea's Choi Jong-hyun Academy planned a public AI symposium for 20–21 November [utokyo-tokyo-forum-2026-ai]. The Tokyo Forum was reportedly set for Yasuda Auditorium, with AI as a transformative technology for humans, knowledge and civilisation as its theme [utokyo-tokyo-forum-2026-ai].

**How to read this.** The two sides do not respond to each other in our material. We present them side by side as a difference in framing, not as a debate with a winner.

---

## 8. Other developments and coverage gaps

- METR published a post titled "Interpreting a recent acceleration in pretraining loss" on 24 November [metr-2026-11-24-pretraining-loss-acceleration]. Only the title was visible, so we make no claim about its findings [metr-2026-11-24-pretraining-loss-acceleration].
- According to search summaries, Sakana's 26 October symposium set out three AI sovereignty pillars: pre-training, post-training through Namazu, and orchestration through Fugu [sakana-sawara-timeline-2026-10-26]. A homegrown model, provisionally named Sawara, is reportedly due to start pre-training around late 2026 [sakana-sawara-timeline-2026-10-26]. The searches disagree on whether that start is November or December [sakana-sawara-timeline-2026-10-26].
- A RIKEN feature from 19 October reportedly describes how RIKEN AIP entered a new phase in April 2026 under Director Masashi Sugiyama [riken-aip-closeup-20261019]. The new phase reportedly focuses on understanding the principles of AI [riken-aip-closeup-20261019].
- The Alan Turing Institute announced that Adrian Belton is the new Chair of its Board of Trustees [turing-2026-11-03-new-board-chair].
- Stanford HAI announced 12 new student affinity groups, with topics including accessibility, healthcare and journalism [hai-2026-11-20-student-affinity-groups].
- **Coverage gaps.** Epoch AI, the UK AI Security Institute, MIT CSAIL and the CMU Robotics Institute returned no verifiable items this week. In each case the collector could not reach the site. **This does not show that these groups published nothing.** Evaluator coverage again rests on METR alone, which matches a pattern already noted in our source-rotation history.
- **One open gap, not a disagreement.** Anthropic says the UK AI Security Institute and METR tested Fable 5.2 before release [anthropic-fable-mythos-5-2-2026-11-09]. This run collected no public report from either evaluator about that testing. For now, the claim rests on Anthropic's statement alone.

---

## 9. This week's divergent views

> ### Can safety tests still tell us what we need to know?
>
> **Position A — the lab.** Anthropic reports low alignment risk for Fable 5.2 and Mythos 5.2 in high-stakes settings [anthropic-fable-mythos-5-2-2026-11-09]. It says this rests on pre-release testing that included external evaluators, the UK AI Security Institute and METR [anthropic-fable-mythos-5-2-2026-11-09].
>
> **Position B — the evaluator.** A METR note reportedly finds that investigator agents increasingly tell alignment tests apart from capability tests [metr-2026-11-16-alignment-eval-tells]. According to the search summary, they often do this by spotting test environments that look fake [metr-2026-11-16-alignment-eval-tells]. METR's Q4 update title also says relevant capabilities are getting harder to measure [metr-2026-11-20-q4-capability-update].
>
> **Why this matters, carefully stated.** If models can recognise a test, a test result could, according to this line of reasoning, say less about real behaviour. However, METR's point is general and does not mention Fable 5.2. Also, the METR items come from search snippets only. So this is a tension between two sources, not a direct dispute, and we do not pick a winner.

---

## 10. Fun corner

This week the Fun corner is, honestly, empty.

Our wildcard collector usually brings back lighter items from independent writers and experimenters. This time it returned zero items. It could not confirm any candidate as published inside our window, and the sites it tried to check could not be reached. We follow a simple rule: no source, no story. So instead of inventing something cheerful, we are leaving the corner open. We hope to have more to share next week.

---

## 11. Vocabulary corner

- **time horizon** — in AI evaluation, roughly how long a task an AI model can handle; here, a measure that reportedly doubles every few months.
- **open-weight model** — a model whose learned numbers (weights) are published, so others can download, adapt and run it.
- **gated access** — access that is limited to approved or vetted users rather than open to everyone.
- **alignment risk** — the chance that an AI system acts in ways its developers did not intend.
- **hallucination** — when an AI system states false information confidently, as if it were true.
- **private placement** — a sale of company shares directly to selected investors instead of on the open market.
- **resilience** — the ability of a system or society to absorb a shock and recover from it.
- **redacted** — with some parts removed or hidden before publication, usually for safety or confidentiality.

---

## 12. References

Confidence labels: *(confirmed)* = read at the official page; *(inferred)* = search snippet of an official page; *(second-hand)* = search summary or third-party report. "Index page" means the URL is a list of posts, not the article itself.

### Evaluation and safety institutes

**METR**

1. `metr-2026-11-20-q4-capability-update` — METR Blog, 2026-11-20 *(inferred)* —
   https://metr.org/blog/2026-11-20-q4-2026-capability-update/
2. `metr-2026-11-24-pretraining-loss-acceleration` — METR Blog, 2026-11-24 *(inferred, title only)* —
   https://metr.org/blog/2026-11-24-interpreting-a-recent-acceleration-in-pretraining-loss/
3. `metr-2026-11-16-alignment-eval-tells` — METR Notes, 2026-11-16 *(inferred)* —
   https://metr.org/notes/2026-11-16-measuring-alignment-eval-tells/
4. `metr-2026-11-05-anthropic-ai-rd-acceleration-assessment` — METR Blog, 2026-11-05 *(inferred)* —
   https://metr.org/blog/2026-11-05-anthropic-ai-rd-acceleration-assessment/
5. `metr-2026-11-05-review-anthropic-risk-report-rd-section` — METR Blog, 2026-11-05 *(inferred)* —
   https://metr.org/blog/2026-11-05-rd-section-anthropic-risk-report-august-2026-review/

**Epoch AI** — no verifiable items this run (collection gap).

**UK AI Security Institute** — no verifiable items this run (collection gap).

### Industry leaders

**Anthropic**

6. `anthropic-ipo-pricing-2026-11-18` — Anthropic Official Newsroom, 2026-11-18 *(confirmed)* —
   https://www.anthropic.com/news/anthropic-prices-initial-public-offering
7. `anthropic-ipo-close-2026-11-20` — Anthropic Official Newsroom, 2026-11-20 *(confirmed)* —
   https://www.anthropic.com/news/ipo-close
8. `anthropic-fable-mythos-5-2-2026-11-09` — Anthropic Official Newsroom, 2026-11-09 *(confirmed)* —
   https://www.anthropic.com/claude-fable-and-mythos-5-2

**OpenAI**

9. `openai-gpt-6-2-astra-sol-2026-11-17` — OpenAI Help Center, Model Release Notes, 2026-11-23 (launch 2026-11-17) *(inferred)* —
   https://help.openai.com/en/articles/9624314-model-release-notes
10. `openai-chatgpt-space-plus-2026-11-20` — OpenAI Help Center, ChatGPT Release Notes, 2026-11-20 *(inferred)* —
    https://help.openai.com/en/articles/6825453-chatgpt-release-notes
11. `openai-businesses-chatgpt-intl-2026-11-19` — OpenAI, Introducing Businesses in ChatGPT, 2026-11-19 (update date) *(inferred)* —
    https://openai.com/index/introducing-businesses-chatgpt/
12. `openai-healthcare-api-configs-2026-11-24` — OpenAI Help Center, Model Release Notes, 2026-11-24 *(inferred, single snippet)* —
    https://help.openai.com/en/articles/9624314-model-release-notes

**Microsoft**

13. `msft-mai-seven-models-2026-11-17` — Microsoft AI news, 2026-11-17 (date inferred) *(inferred)* —
    https://microsoft.ai/news/building-a-hillclimbing-machine-launching-seven-new-mai-models/
14. `msft-ignite-2026-mai-keynote` — Microsoft AI news, 2026-11-17 (date inferred) *(inferred)* —
    https://microsoft.ai/news/microsoft-ignite-2026-mai-keynote/
15. `msft-ignite-2026-nadella-keynote` — Microsoft News, Ignite 2026 transcript PDF, 2026-11-17 (date inferred) *(inferred)* —
    https://news.microsoft.com/events/wp-content/uploads/2026/11/Nadella_TRANSCRIPT_Ignite-Keynote_Nov-2026.pdf

**Google DeepMind**

16. `gdm-alphagenome-2-2026-11` — Google DeepMind Blog, Science category index, 2026-11 (month only) *(second-hand, index page)* —
    https://deepmind.google/blog/?category=Science
17. `gdm-gemini-robotics-2-5-2026-11` — Silicon Report (third party), ~2026-11-10 *(second-hand)* —
    https://www.siliconreport.com/google-deepmind-introduces-gemini-robotics-2-5
18. `gdm-alphaproof-code-2026-11` — Google DeepMind Blog index, 2026-11 (month only) *(second-hand, index page, title only)* —
    https://deepmind.google/blog/?category=Science

**Meta AI**

19. `meta-muse-uk-2026-11` — Meta Newsroom, 2026-11 (month only) *(inferred, title only)* —
    https://about.fb.com/news/2026/11/introducing-muse-in-the-uk-a-personal-ai-agent-you-control/
20. `meta-open-weight-medicine-2026-11` — Meta Newsroom, 2026-11 (month only) *(inferred, title only)* —
    https://about.fb.com/news/2026/11/researchers-using-meta-open-weight-ai-models-medical-breakthroughs

**Sakana AI**

21. `sakana-namazu-small-2026-11-25` — Sakana AI Blog index, 2026-11-25 *(second-hand, index page)* —
    https://sakana.ai/blog/
22. `sakana-marlin-update-2026-11-26` — Sakana AI, Marlin launch page (not the update post), 2026-11-26 *(second-hand)* —
    https://sakana.ai/marlin-release/
23. `sakana-sawara-timeline-2026-10-26` — Sakana AI Blog index, 2026-10-26 *(second-hand, index page)* —
    https://sakana.ai/blog/

### Public research institutions

**The Alan Turing Institute**

24. `turing-2026-11-17-resilience-agenda` — The Alan Turing Institute News, 2026-11-17 *(second-hand)* —
    https://www.turing.ac.uk/news/uk-needs-new-ai-capabilities-threats-evolve-faster-our-ability-respond-turing-ceo-warns
25. `turing-2026-11-18-ai-disruption-roadmap` — The Alan Turing Institute News index, 2026-11-18 *(second-hand, index page)* —
    https://www.turing.ac.uk/news
26. `turing-2026-11-03-new-board-chair` — The Alan Turing Institute News index, 2026-11-03 *(second-hand, index page)* —
    https://www.turing.ac.uk/news

**Stanford HAI**

27. `hai-2026-11-18-ais-future-is-still-a-choice` — Stanford HAI News, 2026-11-18 *(second-hand)* —
    https://hai.stanford.edu/news/ais-future-is-still-a-choice
28. `hai-2026-11-19-court-ai-hallucination-study` — Stanford HAI News index, 2026-11-19 *(second-hand, index page)* —
    https://hai.stanford.edu/news
29. `hai-2026-11-20-icu-delirium-monitoring` — Stanford HAI News index, 2026-11-20 *(second-hand, index page)* —
    https://hai.stanford.edu/news
30. `hai-2026-11-20-student-affinity-groups` — Stanford HAI News index, 2026-11-20 *(second-hand, index page)* —
    https://hai.stanford.edu/news
31. `hai-2026-11-10-ai100-third-report` — Stanford HAI News, 2026-11-10 *(second-hand)* —
    https://hai.stanford.edu/news/the-world-has-changed-insights-from-the-new-ai100-report

**University of Tokyo / RIKEN AIP**

32. `riken-aip-closeup-20261019` — RIKEN Press/Closeup (Japanese), 2026-10-19 *(inferred)* —
    https://www.riken.jp/pr/closeup/2026/20261019_1/index.html
33. `utokyo-tokyo-forum-2026-ai` — University of Tokyo (DUCR) announcement PDF, event date 2026-11-20 *(second-hand)* —
    https://www.ducr.u-tokyo.ac.jp/content/400105048.pdf

**MIT CSAIL** — no verifiable items this run (collection gap).

**Carnegie Mellon University Robotics Institute** — no verifiable items this run (collection gap).

### Wildcard

No items this run. The wildcard collector found no candidates it could verify inside the window.

---

*Sources for this issue: `runs/2026-11-28/argument-map.json` and the 15 collector files under `runs/2026-11-28/collectors/`. No outside knowledge was added.*
