# CLAUDE.md — AI Frontier Weekly Report Harness Rules

This file defines the shared rules for every agent (main session and all
subagents) working in this repository. All agents must follow these rules
in addition to their own system prompt in `.claude/agents/`.

## 1. Purpose

Every week, this project collects primary-source information about frontier
AI research and produces a structured report in English (CEFR B2–C1) for the
reader, both as a briefing and as English-learning material. A human always
reviews and merges the final pull request — no agent publishes anything
directly.

## 2. Priority sources (in order)

1. AI evaluation/safety institutes: METR, UK AI Security Institute, Epoch AI,
   and comparable organizations — their own published reports only.
2. Industry leaders' official channels: OpenAI, Anthropic, Google DeepMind,
   Meta AI, Microsoft, Sakana AI — official blogs, official social accounts,
   direct interview/talk transcripts.
3. Public research institutions: MIT CSAIL, Stanford HAI, Carnegie Mellon RI,
   The Alan Turing Institute, The University of Tokyo / RIKEN AIP — press
   releases, faculty posts, linked preprints.
4. Everything else (including the Wildcard collector's informal sources) is
   supplementary and must still carry a real, named source URL.

## 3. MUST DO

1. Prioritize primary sources over secondary/aggregator sources.
2. Attach a source URL and publication date to every factual claim.
3. Record the collection timestamp for each run.
4. State explicitly when no primary source was found or when interpretations
   diverge — never fill a gap with invented content.
5. Present conflicting views from different sources side by side (no picking
   a winner).
6. Stay strictly within your assigned collection scope; if something belongs
   to another agent's scope, note it and let the Orchestrator reassign it.
7. Always output in the shared JSON schema defined in section 5 below —
   no free-form prose from collector or synthesis agents.

## 4. MUST NOT DO

1. Never fabricate a source, quote, or attribution.
2. Never scrape paywalled or login-required content.
3. Never reproduce long verbatim passages from copyrighted sources — summarize
   and paraphrase; direct quotes must be short (a few words) and rare.
4. Never merge or publish anything. Agents write files and open branches/PRs
   only; a human merges.
5. Never let a single agent both collect facts and judge/synthesize them —
   collection and synthesis are separate agents to reduce bias.
6. Never present speculation as fact. Use explicit hedging language
   ("likely", "according to X, this could suggest...") for anything not
   directly stated by a primary source.
7. Never report unpublished, private, or rumored information about
   individuals. Only public statements, papers, and talks are in scope.
8. Never rely on the same handful of sources every week without checking
   `config/sources.yml` for rotation/diversity notes.

## 5. Shared data schema

### 5.1 Collector agent output (`runs/<date>/collectors/<agent>-<target>.json`)

```json
{
  "collector": "industry-leader-collector",
  "target": "Anthropic",
  "run_date": "2026-08-13",
  "items": [
    {
      "id": "uuid-or-slug",
      "title": "Short factual headline",
      "summary_en": "2-3 sentence neutral summary, no long direct quotes",
      "source_url": "https://...",
      "source_name": "Anthropic Official Blog",
      "published_date": "2026-08-10",
      "category": "model-release | safety | policy | research | product | opinion",
      "tone": "neutral | playful | contrarian",
      "confidence": "primary-confirmed | primary-inferred | secondary-source",
      "notes": "any caveat, e.g. 'press release only, no paper yet'"
    }
  ],
  "coverage_note": "e.g. 'No new official statements found this week for this target.'"
}
```

### 5.2 Synthesis agent output (`runs/<date>/argument-map.json`)

```json
{
  "themes": [
    {
      "theme": "Agentic coding capability gains",
      "convergent_points": [
        {
          "claim": "Multiple labs report progress on long-horizon agentic tasks",
          "supporting_item_ids": ["...", "..."]
        }
      ],
      "divergent_points": [
        {
          "position_a": "Industry: rapid capability gains are near-term useful",
          "position_a_item_ids": ["..."],
          "position_b": "Evaluators: benchmark gains don't yet transfer to real-world reliability",
          "position_b_item_ids": ["..."]
        }
      ]
    }
  ]
}
```

### 5.3 Final report

Written by the reporting agent to `runs/<date>/report.md` and copied to
`reports/<iso-week>.md`. Structure: executive summary (bullets) → sections by
theme → "This week's divergent views" box → "Vocabulary corner" (5–8 terms
with short definitions) → full reference list with links.

## 6. Pipeline (what the Orchestrator does each run)

1. Read `config/sources.yml` for this week's target list and rotation notes.
2. Dispatch collector subagents in parallel, one call per target, per
   section 5.1's schema. Save each raw output under `runs/<date>/collectors/`.
3. Run `synthesis-agent` on the combined collector output.
4. Run `reporting-agent` on the synthesis output.
5. Run the quality checks in section 7.
6. Create a new branch, commit `runs/<date>/` and `reports/<iso-week>.md`,
   and open a pull request. Do not merge.

## 7. Quality gates (before opening the PR)

1. **Citation integrity**: every claim in the report must trace back to an
   `id` in a collector JSON file. Flag any sentence that doesn't.
2. **Deduplication**: the same news item should not appear twice from
   different collectors without being merged.
3. **CEFR level check**: rough heuristics (average sentence length, rare
   vocabulary ratio) should stay within a B2–C1 range; send back to the
   reporting agent if not.
4. **Diversity check**: compare against the last 4 weeks' sources in
   `config/sources.yml` history — flag over-reliance on the same handful of
   sources.

If any gate fails, note it in the PR description rather than silently fixing
it — the human reviewer should see what was flagged.
