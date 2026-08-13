# AI Frontier Weekly Report

A Claude Code multi-agent pipeline that collects primary-source AI research
news weekly and produces a structured English (CEFR B2–C1) report — both a
briefing and English-study material.

## How it works

See `CLAUDE.md` for the full harness rules (sources, do's/don'ts, data
schema, pipeline, quality gates) and the design document
`ai-frontier-weekly-harness-design.md` (if included) for the rationale.

Short version:

1. `config/sources.yml` lists this week's targets.
2. Collector subagents (`.claude/agents/*-collector.md`) gather primary-source
   items in parallel, one call per target, into
   `runs/<date>/collectors/*.json`.
3. `synthesis-agent` builds an argument map
   (`runs/<date>/argument-map.json`) showing where sources agree and
   disagree.
4. `reporting-agent` writes the final report to `runs/<date>/report.md` and
   `reports/<iso-week>.md`.
5. The Orchestrator opens a pull request. **A human always reviews and
   merges** — no agent publishes automatically.

## Setup

1. Add `ANTHROPIC_API_KEY` to this repository's secrets
   (Settings → Secrets and variables → Actions).
2. The workflow in `.github/workflows/weekly-report.yml` runs every Sunday
   (adjust the cron schedule as needed) and can also be triggered manually
   from the Actions tab (`workflow_dispatch`).
3. Review each week's PR: check `runs/<date>/collectors/*.json` for the raw
   collected items, `runs/<date>/argument-map.json` for how conflicts were
   resolved, and `reports/<iso-week>.md` for the final text.

## Editing coverage

To change which companies, institutes, or people are covered, edit
`config/sources.yml` (via PR, like everything else). The Orchestrator will
pick up the new target list on the next scheduled run.

## Directory structure

```
.
├── CLAUDE.md                      # shared harness rules for all agents
├── .claude/agents/                # subagent definitions
├── .github/workflows/             # weekly cron trigger
├── config/sources.yml             # target source list
├── runs/<date>/                   # raw per-run intermediate output (audit trail)
└── reports/<iso-week>.md          # final published-ready report
```
