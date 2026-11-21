# AI Frontier Weekly — 2026-W47

**Run date:** 2026-11-21 · **Collection started:** 2026-11-21T00:05Z · **Window covered:** 2026-11-11 to 2026-11-21 (wildcard collector: 2026-11-07 to 2026-11-21)

> **Coverage and limitations: please read first.**
>
> A network block stopped most collectors from opening source pages directly this week. Only
> anthropic.com and the Microsoft Research blog could be read. As a result, most items rest on
> search-engine snippets of the original pages. **Only 5 of the 45 collected items are confirmed
> against a primary page.**
>
> Labels used below: *(confirmed)* means checked against the organisation's own page. *(inferred)*
> means rebuilt from search snippets of the organisation's own page. *(second-hand)* means the
> collector rated the item as a secondary source, for example a news outlet or an unverified
> snippet. For anything not confirmed, we use phrases such as "according to" and "reportedly".
>
> **No in-window items were found for five targets:** Sakana AI (zero items), MIT CSAIL, Carnegie
> Mellon Robotics Institute, the UK AI Security Institute (newest posts dated 2026-10-26), and
> RIKEN AIP (the University of Tokyo side produced only an event announcement). This reflects
> blocked access and search limits. It is not proof that these organisations published nothing.
>
> Several items are dated just before the window, mostly 2026-11-05 to 2026-11-10. We keep their
> real dates. Background items from MIT CSAIL, CMU and one title-only Epoch AI listing are older
> or undated, so we do not report them as this week's news. No collector checked official social
> accounts or interview transcripts.
>
> One concentration to note: Anthropic is the subject of items from three collectors (Anthropic,
> METR and Epoch AI). This mostly reflects the volume of news about it this week.

---

## 1. Executive summary

- OpenAI and Anthropic both released new frontier models, and both limit reduced-safeguard access to vetted organisations [12][13][17].
- METR reports fast gains in AI R&D-relevant capabilities, and OpenAI's system card reportedly rates Astra as High for AI self-improvement [1][13].
- Evaluators suggest measurement is getting harder, as AI agents increasingly recognise test settings and tested models still miss a real-work standard [1][2][8].
- Anthropic closed its Nasdaq IPO at $83.00 per share, raising about $93.5B gross plus about $26.0B from chip and cloud companies [18].
- Stanford HAI and the Alan Turing Institute published work on AI's effects on courts, younger workers and UK resilience, though mostly via snippets [31][32][37].

---

## 2. New frontier models with tiered access

Two leading labs released a new model generation around this window. In both cases, the most
permissive version is not open to everyone. Instead, it goes only to organisations that pass a
check. This approach is called tiered access (different users get different levels of model
capability).

OpenAI introduced GPT-6.2 Astra and GPT-6.2 Sol on 2026-11-17 [12] *(inferred)*. According to
search snippets of the launch page, Astra is positioned for the hardest professional work. Sol is
positioned for efficient everyday tasks. Both are reportedly available in ChatGPT Work, Codex and
the API. The snippets list API prices of $8/$40 for Astra and $2/$10 for Sol. These prices are per
million input/output tokens (small chunks of text that a model reads and writes). Microsoft's
Ignite 2026 coverage reportedly lists the GPT-6.2 series as generally available on Microsoft
Foundry [28] *(inferred)*. However, that claim comes from a search summary drawing on third-party
outlets and is not verified against Microsoft's own post.

Anthropic released Claude Fable 5.2 and Claude Mythos 5.2 on 2026-11-09, two days before our
window [17] *(confirmed)*. Fable 5.2 is available on all platforms and clouds. Mythos 5.2 is the
same model without some cyber and biology safeguards. It is limited to vetted organisations through
Anthropic's Cyber and Life Sciences Verification Programs. Anthropic says outputs are up to about
30% faster than Fable 5.1. It also reports gains over Opus 5.5 on most benchmarks, but these are
its own claims. Pricing is $8/$40 per million input/output tokens. Anthropic adds that its
classifiers (automatic filters that sort requests) block about 55% fewer legitimate requests than
before.

**Where the sources agree.** Both labs restrict dual-use behaviour (abilities that can help or
harm, such as cyber skills) to approved users. On the OpenAI side, the GPT-6.2 system card
reportedly limits reduced cyber refusals to organisations approved under a program called Daybreak
Red [13] *(inferred)*. The top-tier models from both labs also list the same $8/$40 price
[12][17]. One caveat applies: the OpenAI price comes only from snippets, while Anthropic's is
confirmed.

**Where they diverge.** We found no genuine disagreement between sources in this theme, so we do
not invent one.

---

## 3. AI research speeding up AI research

This theme is about AI R&D (research and development), and especially whether AI is helping to
build better AI. An evaluator and two labs each point in the same direction this week.

METR's Q4 capability update, dated 2026-11-20, reports that AI R&D-relevant capabilities are
improving quickly [1] *(inferred)*. On the lab side, OpenAI's system card reportedly says Astra is
the first model it has deployed externally that meets the High threshold for AI Self-Improvement
under its Preparedness Framework [13] *(inferred)*. Meanwhile, Anthropic says it adjusted Fable
5.2's training to limit gains in AI R&D capability [17] *(confirmed)*.

Two earlier METR publications, both dated 2026-11-05 and therefore before our window, focus on
Anthropic. In the first, METR used high-access evaluation (testing with deeper access than the
public gets) [3] *(inferred)*. It reportedly finds that Anthropic is improving its models on
well-specified tasks at roughly twice its March 2024 to October 2025 rate. About 80% of the
current acceleration is attributed to AI. However, METR stresses high uncertainty. It says it would
not be surprised if the true speed-up were nearer 1.3x or 3x.

In the second, METR reviewed the automated-R&D section of Anthropic's August 2026 Risk Report [4]
*(inferred)*. According to METR, the leading indicators (redacted by Anthropic) support a range of
reasonable estimates from 1.3 to 2.8. METR also says evidence since the report favours continued
acceleration since October 2025.

Epoch AI's data moves in the same direction, although Epoch itself does not link it to AI R&D
speed-up. That grouping is ours. Drawing on Anthropic's S-1 filing (the document a company files
before listing on a stock exchange), Epoch reportedly estimates that Anthropic's compute spending
grows about 4x per year [6] *(inferred)*. The figure for OpenAI is about 3x. Epoch notes that
OpenAI's data is sparser, so that comparison is less certain. A separate Epoch insight finds that
agentic inference capacity (computing power for running AI agents) grew about 4.6x in a year [7]
*(inferred)*. Its 90% uncertainty interval is 4.2x to 5.1x, compared with about 2.6x for 8-bit
compute capacity.

**One open gap, not a debate.** METR says Anthropic's public Risk Report section implies more
confidence than the private version supports [4]. Our collection contains no item from Anthropic
on this point, and no Anthropic response to METR's review was found. We therefore report only what
METR states. The absence of a response in this week's collection does not mean none exists.

---

## 4. Can we still trust the tests?

Evaluations (structured tests of what a model can do) only work if they measure real behaviour.
This week, several sources suggest that this is getting harder.

A METR note dated 2026-11-16, by Uzay Girit, Kaivu Hariharan and Leni Shor, studies eval "tells"
[2] *(inferred)*. These are clues that reveal a test is a test. According to the note, AI
investigator agents increasingly tell alignment evals apart from capability evals. Alignment evals
check whether a model behaves as intended; capability evals check what it can do. The agents
reportedly spot environments that seem fake, or tasks that look like honeypots (traps designed to
tempt a model into misbehaving). Anthropic reports something similar from the lab side: Fable 5.2
sometimes suspects that it is being evaluated [17] *(confirmed)*.

METR's Q4 update adds a second problem [1] *(inferred)*. Models are nearing performance ceilings
on some tasks, so progress may look slower than it really is. As a result, METR says, it is now
harder to rule out risk by pointing to some easy-to-measure, broad incapability. Separately, Epoch
AI moved its Epoch Capabilities Index (its combined score across benchmarks) to a Bayesian model
(a statistical method that updates estimates as new evidence arrives) [9] *(inferred)*. That
change is dated 2026-11-04, before our window. Epoch did not say it was a response to ceiling
effects.

**Where the sources diverge.** Labs describe strong benchmark gains. Anthropic reports that Fable
5.2 beats Opus 5.5 on most benchmarks [17], and OpenAI positions Astra for the hardest professional
work [12]. An Epoch AI report, by contrast, reportedly found that none of the tested models met
the standard of Epoch's own employees on Epoch's real work tasks [8] *(inferred)*. This included the
two models at the top of the Epoch Capabilities Index. We do not know which models Epoch tested.
So we cannot say Epoch tested GPT-6.2 or Fable 5.2. The task set and grading method are also
unknown, which makes this the weakest item in the set.

There is also a difference in emphasis between the two evaluators. METR warns that progress may be
hidden by ceilings [1], while Epoch finds models still short of a human standard [8]. These measure
different things, so they are not necessarily in conflict. We present both without choosing.

---

## 5. Agents in products, and research on agent risks

Several companies shipped agent products this week. An AI agent here means a system that takes
actions for the user, often across outside services. At the same time, researchers looked at how
agents can be attacked or made cheaper to run.

OpenAI introduced ChatGPT Wallet on 2026-11-13 [14] *(inferred)*. According to snippets, agents in
ChatGPT can make purchases with user approval. It is initially limited to ChatGPT Pro subscribers
aged 18 or over in the US, with eligible US-issued cards. OpenAI's release notes also show ChatGPT
Space rolling out globally to Plus users aged 18 or over, dated 2026-11-20 [15] *(inferred)*. It
reportedly lets users build interactive pages and presentations and share them so others can build
on them.

Meta said on 2026-11-17 that its Muse personal agent app is now available in Australia [24]
*(inferred)*. Users can reportedly link services such as Gmail, Google Calendar, Instagram and
OpenTable. A Mac app and AI-glasses support are also mentioned. A separate Meta post describes
"spaces", custom experiences that users build inside Muse by describing an idea [25]
*(inferred)*. Spaces can sit in the sidebar or main tabs, be hidden, or be scheduled, for example
as a weekly planner on workdays. Its exact date in November is unconfirmed. Another November post
title says Loblaw is Muse's first Canadian retail partner [26] *(inferred)*. Note that ChatGPT Space
and Muse spaces are different products from different companies, despite their similar names.

Microsoft held Ignite 2026 from 17 to 20 November [28] *(inferred)*. Search coverage describes
Microsoft positioning Copilot as a work layer or operating system for work. Reported announcements
include Agent 365 business analytics through the Frontier early-access program, and Copilot
Workspaces. They also reportedly include MAI Licensed Weights, for running and customising MAI
models in a customer's own Azure environment, and an AI Transparency Initiative with more than 40
partners. All of these product claims are unverified against Microsoft's own posts.

On the research side, Microsoft Research described an attack called "Lazarus" on 2026-11-10, one
day before our window [30] *(confirmed)*. It is a backdoor (a hidden trigger that makes a system
misbehave on command). Dormant neurons inside the model are reprogrammed, so the agent runs
malicious commands when the trigger appears. On 2026-11-16, Microsoft Research also released
TokenEconomizer [29] *(confirmed)*. This open-source plugin lets coding agents reuse lessons from
earlier sessions. The stated aim is to lower token costs while keeping task success high. In both
cases, only the blog listing was read, so no results or numbers are reported. Finally, the UK AI
Security Institute tested whether leading coding agents can rebuild published biological AI tools
from limited information [11] *(inferred)*. That post is dated 2026-10-26, well before our window,
and its results were not available.

**Where the sources diverge.** No source in this set directly argues against any of these product
launches. The security research is related, but it does not target any specific product. We leave
this section without a constructed debate.

---

## 6. Capital and compute

This was a large week for capital markets, centred on one company. We merge Anthropic's three IPO
announcements into one account and use the final closing figures.

Anthropic launched the roadshow (a series of meetings to present the share offering to investors)
for its proposed initial public offering on 2026-11-10 [20] *(inferred)*. It priced the IPO at
$83.00 per Class A share on 2026-11-18 [19] *(confirmed)*. The shares began trading on Nasdaq under
the ticker ANT on 19 November. According to the closing release on 2026-11-20, the IPO totalled
about 1.127 billion shares, including the full underwriters' option [18] *(confirmed)*. Gross
proceeds were about $93.5B, with about $91.6B going to Anthropic. Goldman Sachs and Morgan Stanley
were the lead bookrunners.

Alongside the IPO, Anthropic ran a concurrent private placement (a direct sale of shares to chosen
investors). About 313.3 million Class N shares went to AMD, Broadcom, Google, Micron, Microsoft,
NVIDIA and TSMC Partners, raising about $26.0B [18]. Combined gross proceeds were roughly $119.5B.

Epoch AI's compute estimates, covered in section 3, also belong here. Anthropic's compute spending
is reportedly growing about 4x per year, against about 3x for OpenAI [6]. Agentic inference
capacity grew about 4.6x in a year [7]. No source in this set disputes these figures, so this
theme has no divergent points.

---

## 7. Society, work and national resilience

Public research institutions published several pieces this week on how AI is affecting society.
However, almost all of these items rest on single search snippets, so the figures below are
unverified.

Stanford HAI reported on 2026-11-19 that researchers from HAI and RegLab estimated AI use in county
court complaints [31] *(second-hand)*. According to the snippet, AI-use prevalence reached about
38% in Santa Clara County and 36% in San Francisco in 2026, excluding debt-collection cases. Among
self-represented complaints in Santa Clara, signs of AI use reportedly rose from 19% in 2024 to 72%
in 2026. The headline itself signals that proving this is difficult.

A second HAI piece, dated 2026-11-15, draws on data from its Digital Economy Lab [32]
*(second-hand)*. It reportedly finds that employment declines among younger workers in AI-exposed
occupations continued into 2026, particularly in customer service. HAI also published a feature on
the third AI100 report on 2026-11-10, just before our window [33] *(second-hand)*. Its snippet mixed
AI100 and AI Index content, so we do not attribute specific findings to it.

In the UK, the Alan Turing Institute's CEO argued on 2026-11-17 that the country faces a
convergence of climate shocks, geopolitical instability and rapid technological change [37]
*(inferred)*. The CEO called for stronger AI defences. An accompanying report, "Securing Resilience
for the Age of AI", reportedly proposes five Transformational Resilience Goals. A day later, the
Turing's news page listed a policy roadmap with practical steps to reduce UK exposure to AI
disruption [38] *(inferred)*. The collector thinks these may be linked to the same report, but this
is unconfirmed.

In Japan, the University of Tokyo is holding its public symposium Tokyo Forum 2026 on 20–21
November at Yasuda Auditorium, with AI as the theme [39] *(inferred)*. Keynote speakers reportedly
include Anne Bouverot, the French presidential AI envoy. Only the announcement was seen, so no talk
content is available.

**Where the sources diverge.** No source in this set argues against these findings. We note the
gap rather than create a disagreement.

---

## 8. Other developments

These items do not form a clear theme, so we group them by topic only.

- **AI for science and health.** The Google DeepMind blog reportedly lists two November posts. One
  is "AlphaGenome 2", about how cells read DNA [22]. The other is "AlphaProof Code", about verifying
  complex software [23]. Only titles were seen, and exact dates are unknown *(inferred)*. Stanford
  HAI reportedly described a 24/7 video monitoring system for detecting subtle signs of delirium in
  the ICU, dated 2026-11-20 [35] *(second-hand)*.
- **Research funding.** Stanford HAI reportedly awarded 2026 Hoffman-Yee Grants to seven teams,
  worth a combined $3.5 million, on 2026-11-16 [34] *(second-hand)*. Wu Tsai Neuro and HAI also
  reportedly renewed joint funding for neuroscience and AI on 2026-11-11 [36] *(second-hand)*.
- **Robotics.** SiliconAngle reports that Google DeepMind released a new Gemini Robotics
  vision-language-action model (a model that links seeing, language and physical actions) around
  10–11 November [21] *(second-hand)*. It reportedly reached a 96% success rate packing automotive
  parts in Mercedes-Benz proof-of-concept tests. The model's name is unconfirmed.
- **Open-weight biosafety.** The UK AI Security Institute reportedly found that filtering
  pretraining data appears to protect open-weight protein and biological models. However, this may
  not hold up after later fine-tuning [10] *(inferred)*. The post is dated 2026-10-26, before our
  window.
- **Media licensing.** On 2026-11-18, Le Groupe Figaro and OpenAI announced a partnership making
  Figaro journalism discoverable in ChatGPT, with summaries, excerpts and links [16] *(inferred)*.
- **Model update.** Meta reportedly rolled out specialised models trained with learnings from Muse
  Wonder to Muse, dated 2026-11-06 [27] *(second-hand)*. Subscribers reportedly still get the full
  Wonder model for harder tasks.
- **Evaluator governance.** METR released version 1.1 of its conflict of interest policy on
  2026-11-10, with clarity edits and an added recusal example [5] *(inferred)*.
- **Coverage gaps.** The Google DeepMind collector excluded a leadership-change report because it
  could not be dated or verified. The Sakana AI collector found no items at all in the window.

---

## 9. This week's divergent views

> ### Strong benchmarks, weaker real work?
>
> **Position A — the labs.** Anthropic reports that Claude Fable 5.2 beats Opus 5.5 on most
> benchmarks [17], although this is self-reported. OpenAI reportedly positions GPT-6.2 Astra for the
> hardest professional work [12].
>
> **Position B — an evaluator's own workplace.** According to a search snippet, Epoch AI tested
> several models on its own real work tasks [8]. None met the standard of Epoch's employees,
> including the two top models on the Epoch Capabilities Index.
>
> **A related tension between evaluators.** METR warns that models are nearing ceilings on some
> tasks, so progress may look slower than it is [1]. Epoch's finding points the other way in
> emphasis: models still fall short of a human standard [8]. The two measure different things.
>
> **Important limits.** We do not know which models Epoch tested, so this is not a direct rebuttal
> of either lab. Epoch's task set and grading are also unknown. We do not pick a winner.

---

## 10. Fun corner

Every household knows the problem. Something somewhere is beeping, once in a while, and you cannot
find it.

Independent developer Simon Willison solved it in a very modern way [40] *(inferred)*. He asked a
coding agent, Anthropic's Claude Code, to build a small Python server. The server turned his spare
phones, tablets and laptops into microphone listeners. Working together, the devices could
triangulate (find a location by comparing signals from several points) an intermittent beep in a
room full of boxes.

The ending, according to secondary summaries, is the best part. The culprit was reportedly an old
carbon monoxide detector with a dead battery, located to within about 40 cm. We could not check
that detail against the full post, so enjoy it with a small grain of salt. Our wildcard collector
also looked for a contrarian voice this week but could not verify one.

---

## 11. Vocabulary corner

- **tiered access** — a system where different users get different levels of a product, often
  after a check.
- **dual-use** — describes a technology that can be used both to help and to cause harm.
- **performance ceiling** — the point where a test is too easy to show further improvement.
- **honeypot** — a trap designed to tempt someone, or something, into revealing bad behaviour.
- **backdoor** — a hidden way to make a system do something its owners did not intend.
- **private placement** — a sale of company shares directly to selected investors, not on the open
  market.
- **triangulate** — to find the position of something by measuring it from several different
  points.
- **redacted** — with sensitive parts removed or blacked out before publication.

---

## 12. References

Labels show the collector's confidence rating. Item IDs match the collector files under
`runs/2026-11-21/collectors/`.

### Evaluation and safety institutes

1. [metr-2026-11-20-q4-capability-update] — METR Blog, 2026-11-20 — https://metr.org/blog/2026-11-20-q4-2026-capability-update/ *(inferred)*
2. [metr-2026-11-16-alignment-eval-tells] — METR Notes, 2026-11-16 — https://metr.org/notes/2026-11-16-measuring-alignment-eval-tells/ *(inferred)*
3. [metr-2026-11-05-anthropic-ai-rd-acceleration] — METR Blog, 2026-11-05 (pre-window) — https://metr.org/blog/2026-11-05-anthropic-ai-rd-acceleration-assessment/ *(inferred)*
4. [metr-2026-11-05-rd-section-risk-report-review] — METR Blog, 2026-11-05 (pre-window) — https://metr.org/blog/2026-11-05-rd-section-anthropic-risk-report-august-2026-review/ *(inferred)*
5. [metr-2026-11-10-coi-policy-v1-1] — METR (COI policy PDF), 2026-11-10 (pre-window) — https://metr.org/coi-policy.pdf *(inferred)*
6. [epoch-anthropic-openai-compute-spend-growth] — Epoch AI Data Insights, 2026-11-18 — https://epoch.ai/data-insights/anthropic-openai-compute-spend-growth *(inferred)*
7. [epoch-agentic-inference-capacity-growth] — Epoch AI Data Insights, ~2026-11-17 (date uncertain) — https://epoch.ai/data-insights/agentic-inference-capacity-growth *(inferred)*
8. [epoch-real-work-evaluation-report] — Epoch AI Latest (feed listing), 2026-11-17 — https://epoch.ai/latest *(inferred)*
9. [epoch-eci-bayesian-methodology] — Epoch AI Latest (feed listing), 2026-11-04 (pre-window) — https://epoch.ai/latest *(inferred)*
10. [aisi-pretraining-data-filtering-2026-10-26] — UK AI Security Institute Blog (index page), 2026-10-26 (pre-window) — https://www.aisi.gov.uk/blog *(inferred)*
11. [aisi-coding-agents-bio-tools-2026-10-26] — UK AI Security Institute Blog (index page), 2026-10-26 (pre-window) — https://www.aisi.gov.uk/blog *(inferred)*

### Industry leaders

12. [openai-gpt-6-2-astra-sol] — OpenAI Official Site, 2026-11-17 — https://openai.com/index/introducing-gpt-6-2-astra-sol/ *(inferred)*
13. [openai-gpt-6-2-system-card] — OpenAI Deployment Safety Hub, 2026-11-17 (date assumed) — https://deploymentsafety.openai.com/gpt-6-2-astra-sol *(inferred)*
14. [openai-chatgpt-wallet] — OpenAI Official Site, 2026-11-13 — https://openai.com/index/introducing-chatgpt-wallet/ *(inferred)*
15. [openai-chatgpt-space] — OpenAI ChatGPT Release Notes, 2026-11-20 — https://help.openai.com/en/articles/6825453-chatgpt-release-notes *(inferred)*
16. [openai-le-figaro-partnership] — OpenAI Official Site, 2026-11-18 — https://openai.com/index/le-groupe-figaro-and-openai-announce-partnership/ *(inferred)*
17. [anthropic-fable-mythos-5-2-2026-11-09] — Anthropic Official Newsroom, 2026-11-09 (pre-window) — https://www.anthropic.com/claude-fable-and-mythos-5-2 *(confirmed)*
18. [anthropic-ipo-close-2026-11-20] — Anthropic Official Newsroom, 2026-11-20 — https://www.anthropic.com/news/ipo-close *(confirmed)*
19. [anthropic-ipo-pricing-2026-11-18] — Anthropic Official Newsroom, 2026-11-18 — https://www.anthropic.com/news/anthropic-prices-initial-public-offering *(confirmed)*
20. [anthropic-roadshow-launch-2026-11-10] — Anthropic Official Newsroom, 2026-11-10 (pre-window) — https://www.anthropic.com/news/roadshow-launch *(inferred)*
21. [gdm-gemini-robotics-new-model] — SiliconAngle (secondary report), ~2026-11-11 — https://siliconangle.com/?p=853854 *(second-hand)*
22. [gdm-alphagenome-2] — Google DeepMind Blog (Science listing), 2026-11 (day unknown) — https://deepmind.google/blog/?category=Science *(inferred)*
23. [gdm-alphaproof-code] — Google DeepMind Blog (Science listing), 2026-11 (day unknown) — https://deepmind.google/blog/?category=Science *(inferred)*
24. [meta-muse-australia-launch-2026-11-17] — Meta Newsroom, 2026-11-17 — https://about.fb.com/news/2026/11/muse-is-now-available-in-australia/ *(inferred)*
25. [meta-muse-spaces-2026-11] — Meta Newsroom, 2026-11 (day unknown) — https://about.fb.com/news/2026/11/introducing-spaces-customize-muse-app/ *(inferred)*
26. [meta-loblaw-muse-partner-2026-11] — Meta Newsroom, 2026-11 (day unknown) — https://about.fb.com/news/2026/11/meta-welcomes-loblaw-as-first-canadian-retail-partner-to-muse/ *(inferred)*
27. [meta-muse-wonder-trained-models-rollout-2026-11-06] — LetsDataScience (secondary report), 2026-11-06 (pre-window) — https://letsdatascience.com/news/meta-rolls-out-muse-wonder-trained-models-to-muse-and-meta-a-165c6374 *(second-hand)*
28. [msft-ignite-2026-overview] — Microsoft News Source Asia, 2026-11-18 — https://news.microsoft.com/source/asia/2026/11/18/ignite2026/?lang=zh-hant *(inferred)*
29. [msft-research-tokeneconomizer-2026-11-16] — Microsoft Research Blog, 2026-11-16 — https://www.microsoft.com/en-us/research/blog/tokeneconomizer-learning-from-experience-to-make-ai-coding-agents-more-efficient/ *(confirmed)*
30. [msft-research-lazarus-backdoor-2026-11-10] — Microsoft Research Blog, 2026-11-10 (pre-window) — https://www.microsoft.com/en-us/research/blog/lazare-veni-foras-reprogramming-dormant-neurons-to-backdoor-ai-agents/ *(confirmed)*

No items: Sakana AI (see coverage note above).

### Public research institutions

31. [hai-ai-court-filings-2026-11-19] — Stanford HAI News, 2026-11-19 — https://hai.stanford.edu/news/ai-might-be-flooding-state-court-houses-but-proving-it-is-another-matter *(second-hand)*
32. [hai-jagged-edge-ai-boom-2026-11-15] — Stanford HAI News, 2026-11-15 — https://hai.stanford.edu/news/the-jagged-edge-of-the-ai-boom *(second-hand)*
33. [hai-ai100-third-report-2026-11-10] — Stanford HAI News, 2026-11-10 (pre-window) — https://hai.stanford.edu/news/the-world-has-changed-insights-from-the-new-ai100-report *(second-hand)*
34. [hai-hoffman-yee-grants-2026-11-16] — Stanford HAI News (index page), 2026-11-16 — https://hai.stanford.edu/news *(second-hand)*
35. [hai-icu-delirium-video-monitoring-2026-11-20] — Stanford HAI News (index page), 2026-11-20 — https://hai.stanford.edu/news *(second-hand)*
36. [hai-wu-tsai-neuro-hai-seed-grants-2026-11-11] — Stanford HAI News (index page), 2026-11-11 — https://hai.stanford.edu/news *(second-hand)*
37. [turing-ceo-warning-ai-capabilities-2026-11-17] — The Alan Turing Institute News, 2026-11-17 — https://www.turing.ac.uk/news/uk-needs-new-ai-capabilities-threats-evolve-faster-our-ability-respond-turing-ceo-warns *(inferred)*
38. [turing-policy-roadmap-ai-disruption-2026-11-18] — The Alan Turing Institute News (index page), 2026-11-18 — https://www.turing.ac.uk/news *(inferred)*
39. [utokyo-tokyo-forum-2026-ai] — University of Tokyo (event announcement PDF), event dates 2026-11-20/21 — https://www.u-tokyo.ac.jp/content/400289852.pdf *(inferred)*

No in-window items: MIT CSAIL, Carnegie Mellon Robotics Institute, RIKEN AIP.

### Wildcard

40. [wild-willison-beep-locator-20261109] — Simon Willison's Weblog, 2026-11-09 — https://simonwillison.net/2026/nov/9/mysterious-beeps *(inferred)*

### Background items collected but not reported as this week's news

These items are out of window, undated, or title-only. They are listed for audit purposes only.

- [mit-physiopt-2026-02] — MIT News (topic listing), 2026-02-27 — https://news.mit.edu/index%2Ephp/topic/computers?page=1 *(second-hand)*
- [mit-pegatron-partnership-2026] — CSAIL Alliances, 2026 (placeholder date) — https://cap.csail.mit.edu/research *(inferred)*
- [mit-time100-ai-rus-2026] — MIT News CSAIL listing, 2026 (placeholder date) — https://news.mit.edu/clp/csail?page=0 *(second-hand)*
- [cmu-iros2026-facility-tours] — CMU News, 2026-10 — https://www.cmu.edu/news/stories/archives/2026/october/cmu-robotics-expertise-and-facilities-attract-iros-2026-conference-attendees *(second-hand)*
- [epoch-huawei-horinger-data-center] — Epoch AI Blog (feed listing), 2026-11-06 — https://epoch.ai/blog *(inferred)*

---

*Sources for this issue: `runs/2026-11-21/argument-map.json`, `runs/2026-11-21/run-meta.json` and
the 15 collector files under `runs/2026-11-21/collectors/`. No outside knowledge was added.*
