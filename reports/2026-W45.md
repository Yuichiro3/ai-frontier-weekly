# AI Frontier Weekly — 2026-W45

**Run date:** 2026-11-07
**Target window:** 2026-10-31 to 2026-11-07
**Sources:** `runs/2026-11-07/argument-map.json` and the 15 collector files in `runs/2026-11-07/collectors/`

> **Read this first: a weak evidence week**
>
> - **Most collection was blocked.** 8 of the 15 collectors returned no items at all, because of DNS or fetch failures. These were Google DeepMind, Meta AI, Microsoft, Sakana AI, UK AI Security Institute, Stanford HAI, UTokyo/RIKEN AIP and the wildcard collector. Each collector says this is an access gap, not proof that nothing was published.
> - **Most items are based on snippets.** Even where items exist, most come from search snippets or search summaries, not from the original pages. Only 4 items (all from Anthropic) are marked "primary-confirmed" (checked directly on the original page). Every figure below should be treated as unverified until a human checks it.
> - **Several items are older than the window.** Five Anthropic items (dated 2026-10-08 to 2026-10-28) and one METR item (2026-10-22) fall before 2026-10-31. Collectors included them as the latest available material or as context. They are marked "(pre-window)" below.
> - **No divergent views could be supported.** The synthesis step found no disagreement between sources that it could back with item IDs. See the "divergent views" box for details.

Item IDs from the collector files appear in square brackets after each claim, for example [openai-images-2-6].

---

## Executive summary

- METR, an AI evaluation organization, estimates that AI is speeding up Anthropic's capability research, but it calls the figures highly uncertain [metr-2026-11-05-anthropic-ai-rd-acceleration, metr-2026-11-05-review-anthropic-risk-report-rd].
- OpenAI and Epoch AI both published material on AI data centers and compute, though their claims are of very different kinds [openai-responsible-infrastructure, epoch-tpu-production-doubling-2026-11-04, epoch-largest-ai-data-centers-2026-11].
- OpenAI and Anthropic both described work on AI for life science, but no evaluator or university item on this topic was collected [openai-biobasicsbench, anthropic-drug-development-2026-10-27, anthropic-ai-for-science-2026-10-28].
- Anthropic filed for a proposed stock market listing on 26 October, which is before this week's window [anthropic-s1-sec-2026-10-26].
- Collection failed for 8 of 15 sources, so this report covers only part of the week's frontier AI news (argument-map caveats).

---

## 1. Measuring how fast AI speeds up AI research (METR on Anthropic)

This theme is about "AI R&D acceleration" (how much AI systems speed up the work of building better AI). Both items come from one evaluator, METR, and both discuss a single lab, Anthropic. As a result, the agreement below is agreement within one source, not across sources. Both items are based on search summaries, because metr.org could not be fetched.

**What METR reports.** METR ran a "high-access evaluation" (an assessment where the evaluator gets deeper access than the public) of Anthropic between 12 August and 29 October 2026 [metr-2026-11-05-anthropic-ai-rd-acceleration]. Its main estimate is that Anthropic is improving model capabilities on well-specified tasks at roughly twice the rate seen from March 2024 to October 2025 [metr-2026-11-05-anthropic-ai-rd-acceleration]. METR suggests that perhaps about 80% of this current speed-up is due to AI [metr-2026-11-05-anthropic-ai-rd-acceleration]. It also reports no evidence of significant bottlenecks over the next 12 months [metr-2026-11-05-anthropic-ai-rd-acceleration]. However, METR calls the estimate highly uncertain, and it says Anthropic redacted some of the analysis [metr-2026-11-05-anthropic-ai-rd-acceleration].

**A companion review.** In a second post on the same day, METR reviewed the "Risks from automated R&D" section of Anthropic's August 2026 Risk Report [metr-2026-11-05-review-anthropic-risk-report-rd]. METR broadly agrees that direct catastrophic risk from automated R&D by Anthropic models, as of 15 July 2026, was low [metr-2026-11-05-review-anthropic-risk-report-rd]. Reusing the Risk Report's own data, METR gets an acceleration estimate of about 1.5x; adding more benchmarks raises it to about 1.9x [metr-2026-11-05-review-anthropic-risk-report-rd].

**Convergent points.** Both METR posts estimate that AI is speeding up Anthropic's capability research, with figures above 1x [metr-2026-11-05-anthropic-ai-rd-acceleration, metr-2026-11-05-review-anthropic-risk-report-rd]. Both also stress uncertainty.

**Why the numbers differ.** The two posts give different figures: about 2x in one, and about 1.5x to 1.9x in the other. However, the collector notes that the posts use different data and methods. It warns readers not to treat them as contradictory without reading both [metr-2026-11-05-review-anthropic-risk-report-rd]. For this reason, the difference is not presented as a divergent view.

**Divergent points.** None could be supported this week. METR says Anthropic's public and private reports sometimes describe the AI contribution differently [metr-2026-11-05-review-anthropic-risk-report-rd]. However, Anthropic's own Risk Report was not collected as an item, so we only have one side of this.

---

## 2. AI compute and data-center infrastructure

This theme links one industry item with two evaluator items. The overlap is in topic only. OpenAI writes about standards for its own data-center campuses, while Epoch AI publishes estimates about compute and power. All three items are snippet-based, and the two Epoch items are rated "secondary-source" (not confirmed on the original page).

**OpenAI's community standards.** OpenAI published a National Community Compact that covers its own data-center campuses [openai-responsible-infrastructure]. It also published a Compute Campus Policy Blueprint, which proposes public reporting on water, energy, noise and hiring [openai-responsible-infrastructure].

**Epoch's compute estimates.** An Epoch data insight estimates that Broadcom's TPU-related compute shipments reached about 2 million "H100-equivalents" (a way of counting chips in units of one common Nvidia chip) [epoch-tpu-production-doubling-2026-11-04]. According to the search summary, this is double the earlier level, and it is based on Broadcom's Q3 hardware revenue after removing VMware license revenue [epoch-tpu-production-doubling-2026-11-04]. The collector stresses that this is Epoch's estimate, not a figure reported by the company [epoch-tpu-production-doubling-2026-11-04].

**Epoch's data-center ranking.** Epoch's ranking of AI data centers by power capacity was reportedly updated in early November [epoch-largest-ai-data-centers-2026-11]. According to the search summary, the Anthropic-Amazon New Carlisle site is now the largest tracked facility, at about 1,037 MW of current IT power [epoch-largest-ai-data-centers-2026-11]. This is a living dataset, so the date is an update date, and the figure is unverified [epoch-largest-ai-data-centers-2026-11].

**Convergent points.** An industry lab and an evaluator both published on large-scale AI compute this week [openai-responsible-infrastructure, epoch-tpu-production-doubling-2026-11-04, epoch-largest-ai-data-centers-2026-11]. However, they make different kinds of claims, so this is shared attention rather than shared conclusions.

**Divergent points.** None were identified.

---

## 3. AI applied to science and life-science work

Two industry labs described work on using AI in scientific research. No evaluator or university item on this topic was collected, so this theme reflects industry voices only. Two of the three items are from before the window.

**OpenAI's wet-lab benchmark.** OpenAI published a 100-task benchmark, described as BioBasicsBench, for AI agents doing everyday "wet-lab" science (hands-on laboratory work with chemicals and biological samples) [openai-biobasicsbench]. This item is based on a search snippet, because openai.com could not be fetched [openai-biobasicsbench].

**Anthropic's drug-development work (pre-window).** Anthropic says its scientists have spent several months in research partnerships with six organizations that develop new medicines [anthropic-drug-development-2026-10-27]. The collector read only the listing blurb, not the full post [anthropic-drug-development-2026-10-27].

**Anthropic's AI for Science program (pre-window).** Anthropic highlights 20 scientific foundations, institutions and research groups that it has partnered with, as part of an expansion of its AI for Science program [anthropic-ai-for-science-2026-10-28]. This also comes from a listing blurb only [anthropic-ai-for-science-2026-10-28].

**Convergent points.** Both labs are publicly positioning AI as a tool for scientific and medical research [openai-biobasicsbench, anthropic-drug-development-2026-10-27, anthropic-ai-for-science-2026-10-28]. However, one item is a measurement tool and the others describe partnerships, so they are not directly comparable.

**Divergent points.** None were identified.

---

## 4. Other developments

These items did not fit a clear theme. They are grouped here by source.

**OpenAI (all snippet-based).** OpenAI introduced Images 2.6, which it describes as offering faster image generation, GIF creation, more precise editing and new API controls [openai-images-2-6]. It also added the GPT-6.1 Terra model to the models that power dots, its proactive assistants [openai-dots-update]. In addition, OpenAI raised its bug bounty (a reward paid to people who report security flaws), with up to $30,000 for critical findings in core products [openai-bug-bounty].

**Anthropic (pre-window, primary-confirmed).** On 26 October, Anthropic filed a Form S-1 with the SEC for a proposed IPO (initial public offering, a company's first sale of shares to the public) [anthropic-s1-sec-2026-10-26]. It plans to list on the Nasdaq Global Select Market under the ticker ANT, but the share count and price range are not yet set [anthropic-s1-sec-2026-10-26]. On 27 October, a new agreement with the US General Services Administration gave government partners 40% off several Claude products, with no minimum spend [anthropic-gsa-partnership-2026-10-27]. Anthropic estimates $1 billion in savings, but this is the company's own estimate [anthropic-gsa-partnership-2026-10-27]. Finally, Anthropic's updated Usage Policy, published on 8 October, takes effect on 12 November 2026 [anthropic-usage-policy-2026-10-08]. It adds sections on deceptive activity and influence operations, and requirements for hardware that takes autonomous physical actions [anthropic-usage-policy-2026-10-08].

**METR (pre-window).** On 22 October, METR published a post on red-teaming (deliberately attacking a system to find weaknesses) OpenAI's internal agent monitoring systems [metr-2026-10-22-red-teaming-openai-agent-monitoring]. Only the title and date were seen, so its findings are not summarized here [metr-2026-10-22-red-teaming-openai-agent-monitoring].

**Epoch AI (secondary-source).** Epoch moved its Capabilities Index to a Bayesian model (a statistical method that updates estimates as new evidence arrives), aiming for better-calibrated uncertainty [epoch-eci-bayesian-2026-11-04]. According to the search summary, every model's new score falls inside its previous 90% confidence interval [epoch-eci-bayesian-2026-11-04].

**Universities and research institutes.** A CSAIL news listing describes InstructMesh, a tool for editing AI-generated 3D models and preparing them for fabrication; its methods and authors are unverified [csail-instructmesh-2026-11-02]. A CMU Robotics Institute feature describes the university's new 150,000-square-foot Robotics Innovation Center in Pittsburgh's Hazelwood neighborhood [cmu-ri-robotics-innovation-center-2026-11-02]. Another CMU story covers the university's Florida ties, including Space Coast rovers such as Iris [cmu-news-florida-connections-2026-11-03]. Meanwhile, the Alan Turing Institute's homepage lists Adrian Belton as the new Chair of its Board of Trustees [turing-2026-11-03-new-chair-adrian-belton]. Note that these are mostly facilities and governance news, not research results.

**Sources with no items.** No items were collected from Google DeepMind, Meta AI, Microsoft, Sakana AI, the UK AI Security Institute, Stanford HAI or UTokyo/RIKEN AIP. In each case, the collector reports a DNS or fetch failure, not a confirmed absence of news. The UTokyo/RIKEN AIP collector notes that this is the fourth run in a row affected.

---

> ## This week's divergent views
>
> **No divergent views could be supported this week.**
>
> The synthesis step found no case where two different sources disagreed and both sides were backed by collected items. Two possible tensions were noted but deliberately not treated as disagreements:
>
> 1. **METR vs. Anthropic's own reporting.** METR says Anthropic's public and private reports sometimes describe the AI contribution to research differently [metr-2026-11-05-review-anthropic-risk-report-rd]. However, Anthropic's August 2026 Risk Report was not collected, so only METR's side is available.
> 2. **METR's two acceleration figures.** One post gives about 2x [metr-2026-11-05-anthropic-ai-rd-acceleration], and the other gives about 1.5x to 1.9x [metr-2026-11-05-review-anthropic-risk-report-rd]. However, they use different data and methods, and both come from the same organization.
>
> With 8 of 15 collectors blocked, the lack of disagreement most likely reflects missing coverage, not real consensus.

---

## Fun corner

The wildcard collector usually brings us something lighter, but this week it came back empty-handed. It found a few promising leads, including a Latent Space digest from around 3 November that quotes Lucas Beyer on scaling extrapolation (predicting future AI progress by extending current trends) [wildcard coverage note]. Unfortunately, latent.space and simonwillison.net did not resolve, so nothing could be checked against the original pages. Our rule is simple: no verified source, no story. So the fun corner is taking a week off, and we hope it returns with better network luck next time.

---

## Vocabulary corner

- **snippet** — a short piece of text, such as the preview a search engine shows under a link.
- **primary source** — the original publisher of information, such as a company's own blog, rather than a report about it.
- **acceleration** — an increase in speed; here, how much faster research moves with AI help.
- **bottleneck** — a single point that slows down a whole process.
- **redact** — to hide or remove parts of a document before sharing it.
- **benchmark** — a standard set of tests used to measure and compare performance.
- **confidence interval** — a range of values that likely contains the true number.
- **convergent / divergent** — moving toward the same point / moving apart; used here for agreeing and disagreeing views.

---

## References

Publication dates are as reported by collectors. Items marked (pre-window) are older than 2026-10-31.

### Industry leaders

**OpenAI** (all primary-inferred, from search snippets)
- [openai-images-2-6] Introducing Images 2.6 — 2026-11-04 — https://openai.com/index/introducing-images-2-6/
- [openai-responsible-infrastructure] Community compact and compute campus blueprint — 2026-11-05 — https://openai.com/index/setting-new-standard-responsible-ai-infrastructure/
- [openai-bug-bounty] Bigger bug bounties — 2026-11-02 — https://openai.com/index/rewarding-defenders-with-bigger-bug-bounties/
- [openai-biobasicsbench] Measuring how AI agents handle wet-lab science — 2026-11-06 — https://openai.com/index/measuring-how-ai-agents-handle-wet-lab-science/
- [openai-dots-update] GPT-6.1 Terra added to dots — 2026-11-03 — https://openai.com/index/introducing-dots/

**Anthropic** (all pre-window)
- [anthropic-s1-sec-2026-10-26] S-1 filing with the SEC — 2026-10-26 — primary-confirmed — https://www.anthropic.com/news/s1-sec
- [anthropic-gsa-partnership-2026-10-27] Expanded GSA partnership — 2026-10-27 — primary-confirmed — https://www.anthropic.com/news/expanding-partnership-gsa
- [anthropic-drug-development-2026-10-27] Early progress on drug development — 2026-10-27 — primary-inferred — https://www.anthropic.com/research/early-progress-drug-development
- [anthropic-ai-for-science-2026-10-28] AI for Science program expands — 2026-10-28 — primary-inferred — https://www.anthropic.com/news/ai-for-science-expands-foundations-research-institutions
- [anthropic-usage-policy-2026-10-08] 2026 Usage Policy update — 2026-10-08 — primary-confirmed — https://www.anthropic.com/news/2026-usage-policy-update

**Google DeepMind, Meta AI, Microsoft, Sakana AI** — no items (access failures).

### Evaluation and safety institutes

**METR** (all primary-inferred, from search summaries)
- [metr-2026-11-05-anthropic-ai-rd-acceleration] AI R&D acceleration assessment at Anthropic — 2026-11-05 — https://metr.org/blog/2026-11-05-anthropic-ai-rd-acceleration-assessment/
- [metr-2026-11-05-review-anthropic-risk-report-rd] Review of Anthropic's Risk Report R&D section — 2026-11-05 — https://metr.org/blog/2026-11-05-rd-section-anthropic-risk-report-august-2026-review/
- [metr-2026-10-22-red-teaming-openai-agent-monitoring] Red-teaming OpenAI agent monitoring (pre-window) — 2026-10-22 — https://metr.org/blog/2026-10-22-red-teaming-openai-agent-monitoring/

**Epoch AI** (all secondary-source, from search summaries)
- [epoch-eci-bayesian-2026-11-04] ECI Bayesian methodology — 2026-11-04 — https://epoch.ai/publications/eci-bayesian-methodology
- [epoch-tpu-production-doubling-2026-11-04] TPU production doubling — 2026-11-04 — https://epoch.ai/data-insights/tpu-production-doubling
- [epoch-largest-ai-data-centers-2026-11] Largest AI data centers by power capacity — 2026-11-05 (update date) — https://epoch.ai/graphs/largest-ai-data-centers-by-power-capacity

**UK AI Security Institute** — no items (access failure).

### Public research institutions

- [csail-instructmesh-2026-11-02] MIT CSAIL news listing (InstructMesh) — 2026-11-02 — secondary-source; article URL not obtained — https://www.csail.mit.edu/news
- [cmu-ri-robotics-innovation-center-2026-11-02] Inside CMU's Robotics Innovation Center — 2026-11-02 — primary-inferred — https://www.ri.cmu.edu/inside-cmus-robotics-innovation-center/
- [cmu-news-florida-connections-2026-11-03] CMU's Florida connections — 2026-11-03 — primary-inferred — https://www.cmu.edu/news/stories/archives/2026/november/exploring-cmus-florida-connections-from-space-coast-rovers-to-new-campus
- [turing-2026-11-03-new-chair-adrian-belton] Alan Turing Institute homepage (new board chair) — 2026-11-03 — secondary-source; article URL not found — https://www.turing.ac.uk/

**Stanford HAI, UTokyo / RIKEN AIP** — no items (access failures).

### Wildcard

- No items. Leads could not be verified (see `runs/2026-11-07/collectors/wildcard.json`).
