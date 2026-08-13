# AI研究フロンティア Weekly Report — マルチエージェント・ハーネス設計書

対象環境: Claude Code（週次実行、GitHub Actions想定、人間が最終PRレビュー）

---

## 1. 目的とゴール

- 毎週、AI研究の最前線に関する情報を一次情報源から収集し、構造化された英語（CEFR B2–C1）レポートとして出力する。
- レポートは「情報収集」と「英語学習」の二重目的を持つ。したがって、単なる要約ではなく、**読みやすい構文・語彙レベルに統制された英文**であることが品質基準に含まれる。
- 最終成果物は人間が確認・修正できる形（PR）で提示され、AIが自動でpublishすることはない。

---

## 2. 全体アーキテクチャ

```
                         ┌─────────────────────┐
                         │   Orchestrator       │
                         │  (main Claude Code    │
                         │   session / workflow) │
                         └──────────┬───────────┘
                                    │ fan-out (parallel Task/subagent calls)
        ┌────────────┬─────────────┼─────────────┬────────────────┐
        ▼            ▼             ▼             ▼                ▼
 ┌───────────┐ ┌───────────┐ ┌───────────┐ ┌───────────┐   ┌───────────────┐
 │ Evaluator  │ │ Industry  │ │ Academia  │ │ Wildcard/  │   │ (必要に応じて  │
 │ /Institute │ │  Leader   │ │  Agent    │ │  Offbeat   │   │  追加コレクタ) │
 │  Agent     │ │  Agent(s) │ │           │ │  Agent     │   │               │
 │ (METR等)   │ │ (OpenAI,  │ │(MIT CSAIL,│ │(実験・独自  │   │               │
 │            │ │ Anthropic,│ │ Stanford  │ │ 視点・面白  │   │               │
 │            │ │ Google,   │ │ HAI, CMU  │ │ 実験)      │   │               │
 │            │ │ Meta, MS, │ │ RI, Turing│ │            │   │               │
 │            │ │ Sakana AI)│ │ Inst, UTo-│ │            │   │               │
 │            │ │           │ │ kyo/RIKEN)│ │            │   │               │
 └─────┬──────┘ └─────┬─────┘ └─────┬─────┘ └─────┬──────┘   └───────┬───────┘
       └──────────────┴──────┬──────┴──────────────┴──────────────────┘
                              ▼
                  ┌─────────────────────────┐
                  │   Synthesis Agent        │
                  │  (Convergence/Divergence)│
                  │  共通論点／対立論点の整理  │
                  └────────────┬─────────────┘
                               ▼
                  ┌─────────────────────────┐
                  │   Reporting Agent         │
                  │  英語B2-C1整形、構造化、   │
                  │  Reference付与、           │
                  │  用語解説（学習支援）      │
                  └────────────┬─────────────┘
                               ▼
                    draft branch → PR作成 → 人間レビュー
```

**設計思想**: Orchestratorは「意思決定・調整」のみを担い、実際の情報収集や執筆は専門化されたサブエージェントに委譲する。各サブエージェントは独立したコンテキストウィンドウを持ち、収集ノイズ（検索結果の生データなど）は自分のコンテキスト内に留め、要約された成果物のみをOrchestratorに返す（Claude Codeのsubagent設計思想に準拠）。

---

## 3. ハーネス設計原則（Do's / Don'ts）

これは各エージェントのシステムプロンプト（`.claude/agents/*.md`）とプロジェクト共通ルール（`CLAUDE.md`）の両方に埋め込む「ガードレール」です。

### してよいこと（MUST DO）

1. **一次情報源を最優先する。** 公式ブログ、公式X/技術ノート、機関の公開レポート・論文、規制当局への提出資料などを優先し、二次情報（ニュースサイトのまとめ記事）は一次情報が見つからない場合の補助として使う。
2. **すべての主張にURL付きの出典を紐付ける。** 「誰が・いつ・どこで言ったか」を明記する。
3. **収集日時（タイムスタンプ）を記録する。** 週次実行の再現性・監査性のため。
4. **一次情報が存在しない、または解釈が分かれる場合はその旨を明記する。**（"as of [date], no official statement was found regarding X"）
5. **相反する意見・データがある場合は両論併記する。**（Synthesis Agentの役割）
6. **各エージェントの担当範囲を厳格に守る。** 越境した収集はOrchestratorが再割り当てする。
7. **出力は必ず共通スキーマ（第5章）に従う。** 自由記述にしない。

### してはいけないこと（MUST NOT DO）

1. **出典の捏造・推測での引用付与を禁止。** 見つからない情報は「見つからなかった」と正直に書く。ハルシネーションで埋めない。
2. **有料/ログイン必須コンテンツのスクレイピング禁止。** 公開情報のみを対象とする。
3. **著作権保護されたテキストの長文引用禁止。** 要約・パラフレーズを基本とし、引用は短い一文まで。
4. **エージェントが単独でPRをマージ・公開することを禁止。** 必ず人間のレビュー・承認を経る（`--permission-mode`や`allowed-tools`でwrite権限を制限）。
5. **一つのエージェントに全工程を担わせない。** 収集と評価（論点整理）を同一エージェントに混在させない（バイアス低減のため）。
6. **speculationを事実として書かない。** 予測・推測には "likely", "according to X, this could mean..." のような明示的なヘッジ表現を使う。
7. **個人（研究者・エンジニア）のセンシティブな未公開情報や噂を扱わない。** 公開された発言・論文・登壇内容に限定する。
8. **同じソースを毎週使い回して多様性を失わない。** 収集エージェントは「新着」を優先するロジックを持つ（後述）。

---

## 4. エージェント仕様

| エージェント | 役割 | 主な情報源 | 出力 |
|---|---|---|---|
| **Orchestrator** | 週次実行のオーケストレーション、サブエージェントへの並列委譲、失敗時のリトライ、最終成果物の組み立て指示、PR作成 | — | 実行ログ、最終PR |
| **Evaluator/Institution Agent** | AIモデルの能力評価・安全性評価に関する最新知見の収集 | METR、UK AISI、Epoch AI、他評価専門機関の公開レポート | 構造化JSON（第5章） |
| **Industry Leader Agent(s)** | 主要AI企業のリーダー・公式発表の収集。**柔軟に人物/企業単位で分割可能** | OpenAI, Anthropic, Google DeepMind, Meta AI, Microsoft, Sakana AI の公式ブログ・経営陣の公開インタビュー/登壇/X投稿 | 同上 |
| **Academia Agent** | 学術機関発の研究成果・所感の収集 | MIT CSAIL, Stanford HAI, CMU RI, Alan Turing Institute, 東京大学/RIKEN AIP の公式発表・プレプリント | 同上 |
| **Wildcard/Offbeat Agent** | ちょっと変わった視点、面白い実験、逆張り的議論、DIY検証などを拾う | Hacker News上位、個人研究者のブログ、独立系AI実験プロジェクトなど（一次情報源の質は他エージェントより緩めるが、出典は必須） | 同上（"tone: playful"フラグ付き） |
| **Synthesis Agent** | 全コレクタの出力を横断し、共通する論点（convergence）と対立する論点（divergence）を整理 | 各コレクタの構造化出力 | 論点マップ（JSON） |
| **Reporting Agent** | 最終レポートをB2-C1レベルの英語で執筆。構造化、参考文献リスト、学習用語彙注釈を付与 | Synthesis Agentの出力＋各コレクタの出典 | Markdown/HTMLレポート |

### 4.1 Industry Leader Agentの柔軟な分割について

要望にあった「OpenAI CEOとAnthropic CEOを分ける」といった粒度は、**Orchestratorがその週のニュース量に応じて動的に決定**するのが良い設計です。固定で6エージェントに分けると、話題が少ない週は無駄が多く、逆に大きな発表が重なる週（例：複数社が同時に新モデルを発表）は1エージェントでは処理しきれません。

推奨方式:
- ベースは「Industry Leader Agent」1種類を**汎用テンプレート**として`.claude/agents/industry-leader.md`に定義。
- Orchestratorがその週の対象リストを動的にプロンプトへ注入する（例: `target: "Anthropic (Dario Amodei, official blog)"` を1回の呼び出しごとに変えて並列実行）。
- こうすることで「6社まとめて1エージェント」も「人物ごとに6並列」も同じ定義ファイルで実現できる。

### 4.2 各エージェント定義ファイルの例

`.claude/agents/industry-leader-collector.md`:

```markdown
---
name: industry-leader-collector
description: Collects primary-source statements from a specified AI industry leader or company for the weekly frontier report. Invoke once per target with the target name injected in the prompt.
tools: WebSearch, WebFetch
model: sonnet
---
You are a primary-source research collector focused on ONE assigned AI industry
target for this run (the target is given in the user prompt, e.g. "Anthropic" or
"Sam Altman / OpenAI").

Rules:
- Only use official company blogs/newsrooms, official social accounts, direct
  interview transcripts, or conference talks. No tabloid/aggregator sources.
- Every claim must carry a source URL and a publication date within the last 10 days.
- If nothing new was published by this target this week, say so explicitly —
  do not stretch older news to fill space.
- Do not editorialize. Report what was said/published, not what you think it means.
- Output strictly in the shared JSON schema (see CLAUDE.md §5). No prose outside the schema.
```

`.claude/agents/evaluator-institute-collector.md`:

```markdown
---
name: evaluator-institute-collector
description: Collects the latest public findings, evaluations, or statements from AI model evaluation/safety institutes such as METR, UK AISI, Epoch AI.
tools: WebSearch, WebFetch
model: sonnet
---
You are a research collector specialized in AI evaluation/benchmarking institutions.
Prioritize: METR, UK AI Security Institute, Epoch AI, and comparable evaluation bodies.
Only cite their own published reports, blog posts, or dataset releases — never
third-party summaries of their work unless the original is unavailable.
Flag methodology caveats the institute itself states (e.g. "small sample size").
Output strictly in the shared JSON schema.
```

`.claude/agents/academia-collector.md`:

```markdown
---
name: academia-collector
description: Collects new public research output and statements from a specified academic AI research institution.
tools: WebSearch, WebFetch
model: sonnet
---
You are a research collector focused on ONE assigned academic institution
(target given in the prompt, e.g. "MIT CSAIL" or "RIKEN AIP").
Prioritize: institution press releases, faculty blog posts, arXiv preprints
officially linked from the institution's site, and public talks/recordings.
Distinguish clearly between peer-reviewed results and preprints (label as [preprint]).
Output strictly in the shared JSON schema.
```

`.claude/agents/wildcard-collector.md`:

```markdown
---
name: wildcard-collector
description: Surfaces unusual, playful, or contrarian AI experiments and takes worth including as a "fun corner" in the weekly report.
tools: WebSearch, WebFetch
model: sonnet
---
You are the "wildcard" collector. Look for offbeat but credible AI experiments,
demos, or contrarian arguments from researchers/engineers (personal blogs,
open-source repos, conference lightning talks). Source quality can be more
informal than other collectors, but every item still needs a real URL and a
real named author — never invent an example. Mark tone as "playful" or
"contrarian" in the schema's `tone` field.
```

`.claude/agents/synthesis-agent.md`:

```markdown
---
name: synthesis-agent
description: Reads all collector outputs and identifies convergent and divergent arguments across industry, academia, and evaluators.
tools: Read
model: opus
---
You receive the combined JSON outputs of all collector agents for this week.
Your job:
1. Group items by topic/theme.
2. For each theme, identify where sources AGREE (convergence) and where they
   DISAGREE or present tension (divergence) — e.g. industry optimism vs.
   evaluator caution.
3. Never resolve a disagreement by picking a side — present both with attribution.
4. Output a structured "argument map" (see CLAUDE.md §5.2). Do not draft
   reader-facing prose — that is the Reporting Agent's job.
```

`.claude/agents/reporting-agent.md`:

```markdown
---
name: reporting-agent
description: Produces the final weekly report in English (CEFR B2-C1), structured for readability and English-learning value, with full references.
tools: Read, Write
model: opus
---
You write the final weekly report in English, CEFR B2-C1 level:
- Sentences: mostly 12-22 words, mostly simple/compound structures; avoid
  rare idioms; when a technical term is unavoidable, gloss it briefly in
  parentheses on first use.
- Structure: Executive summary (5 bullets) → sections by theme → "This week's
  divergent views" box → "Vocabulary corner" (5-8 useful terms with short
  definitions, for the reader's English study) → full reference list with links.
- Every factual sentence must trace back to a source in the collector JSON —
  do not add outside knowledge.
- Do not publish or merge anything yourself; write the file and stop.
```

---

## 5. エージェント間のデータ契約

### 5.1 収集エージェントの出力スキーマ（共通）

```json
{
  "collector": "industry-leader-collector",
  "target": "Anthropic",
  "run_date": "2026-08-13",
  "items": [
    {
      "id": "uuid-or-slug",
      "title": "Short factual headline",
      "summary_en": "2-3 sentence neutral summary, no direct long quotes",
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

### 5.2 Synthesis Agentの出力（argument map）

```json
{
  "themes": [
    {
      "theme": "Agentic coding capability gains",
      "convergent_points": [
        {"claim": "Multiple labs report progress on long-horizon agentic tasks",
         "supporting_item_ids": ["...", "..."]}
      ],
      "divergent_points": [
        {"position_a": "Industry: rapid capability gains are near-term useful",
         "position_a_item_ids": ["..."],
         "position_b": "Evaluators: gains on benchmarks don't yet transfer to real-world reliability",
         "position_b_item_ids": ["..."]}
      ]
    }
  ]
}
```

この契約により、Reporting Agentは「事実の再収集」をせず、既存の構造化データを英語B2-C1に整形することだけに集中できる。

---

## 6. プロジェクトディレクトリ構成（案）

```
ai-frontier-weekly/
├── CLAUDE.md                      # 共通ハーネスルール（第3章の内容を集約）
├── .claude/
│   └── agents/
│       ├── industry-leader-collector.md
│       ├── evaluator-institute-collector.md
│       ├── academia-collector.md
│       ├── wildcard-collector.md
│       ├── synthesis-agent.md
│       └── reporting-agent.md
├── .github/
│   └── workflows/
│       └── weekly-report.yml      # cronトリガー
├── config/
│   └── sources.yml                # 対象企業・機関のリスト、優先度
├── runs/
│   └── 2026-08-13/
│       ├── collectors/*.json      # 各コレクタの生出力（監査用に保存）
│       ├── argument-map.json
│       └── report.md              # Reporting Agentの最終出力
└── reports/
    └── 2026-W33.md                # PRとして提示される最終レポート
```

`runs/`配下に毎回の中間出力を保存しておくと、後から「なぜこの結論になったか」を人間が検証できる（トレーサビリティ）。

---

## 7. 週次実行フロー（GitHub Actions）

Claude Code GitHub Action（`anthropics/claude-code-action@v1`）は、プロンプトを渡す「自動化モード」で `schedule` トリガーからも実行できます。スケジュール実行はデフォルトブランチからのみ動き、パブリックリポジトリでは60日間動きがないと自動停止する点に注意してください。

```yaml
name: Weekly AI Frontier Report

on:
  schedule:
    - cron: "0 22 * * 0"   # 毎週日曜 07:00 JST 目安（UTC指定に注意）
  workflow_dispatch: {}     # 手動トリガーも残す

permissions:
  contents: write
  pull-requests: write

jobs:
  weekly-report:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - uses: anthropics/claude-code-action@v1
        with:
          anthropic_api_key: ${{ secrets.ANTHROPIC_API_KEY }}
          prompt: |
            Run this week's AI frontier report pipeline:
            1. Read config/sources.yml for target list.
            2. Dispatch collector subagents in parallel per §4 of CLAUDE.md.
            3. Run synthesis-agent, then reporting-agent.
            4. Write output to runs/<today>/ and reports/<iso-week>.md.
            5. Create a branch and open a PR — do NOT merge.
          claude_args: |
            --allowedTools "WebSearch,WebFetch,Read,Write,Bash(git *)"
            --max-turns 60
            --model claude-opus-4-6
```

**重要**: `contents: write` / `pull-requests: write` は付与するが、マージ権限は与えない。マージは常に人間が行う。また、フォークからのPRイベントは書き込みトークンが読み取り専用になる点にも注意（今回はscheduleトリガーなので該当しないが、将来Issueベースのトリガーを足す場合は要考慮）。

---

## 8. 品質ゲート（Reporting前後のチェック）

Reporting Agentの前後に軽量な「チェッカー」ステップを挟むことを推奨します（別サブエージェントでも、Orchestratorの後処理スクリプトでも可）:

1. **出典整合性チェック**: レポート中の全主張が`collectors/*.json`のitem idに紐づいているか機械的に検証。紐づかない文があればビルド失敗として人間に知らせる。
2. **重複排除**: 同一ニュースが複数コレクタから重複報告されていないか。
3. **CEFRレベルチェック**: 平易な指標（平均文長、稀語彙率など）でB2-C1レンジから外れていないか簡易チェック。外れていればReporting Agentに差し戻す。
4. **多様性チェック**: 直近4週間で同じソースだけに偏っていないか（`config/sources.yml`にローテーション履歴を記録）。

---

## 9. 拡張・カスタマイズのポイント

- **Industry Leader Agentの粒度**: `config/sources.yml`で対象リストと「今週分割するか統合するか」をOrchestratorに指示できるようにしておくと、ニュース量に応じた柔軟な運用が可能。
- **Wildcard Agentのトーン管理**: 面白さを狙うあまり不正確にならないよう、Wildcard Agentも他と同じ出典必須ルールは緩めない（トーンだけ緩める）。
- **将来的な拡張**: 政策・規制動向（EU AI Act実施状況など）を扱う「Policy Agent」を同じテンプレートで追加可能。
- **人間フィードバックループ**: PRコメントで「このソースは信頼できない」「この論点整理はズレている」といったフィードバックを`config/sources.yml`や各エージェント定義にfeedbackとして反映し、週を追うごとに精度を上げる運用が望ましい。

---

## 10. まとめ：責任分担の一覧

| 判断 | 誰が行うか |
|---|---|
| どの情報を「事実」として採用するか | 各Collector Agent（出典必須） |
| 対立する意見をどう扱うか | Synthesis Agent（両論併記、判定しない） |
| 読みやすい英語にする | Reporting Agent |
| 公開する/しない | 人間（PRレビュー） |
| ハーネスのルール違反がないかの最終監督 | 人間（週次で`runs/`を抜き打ちチェック推奨） |

このように「収集」「統合」「執筆」「公開判断」を明確に分離することで、各エージェントの役割が単純化され、バイアスの混入や無断公開のリスクを構造的に減らせます。
