# Autonomous Multi-Agent Task Execution

**CORE PURPOSE**: Orchestrate intelligent parallel task execution with autonomous agent coordination and dependency management.

**UNIQUE SCOPE**: Task selection algorithms, parallel execution patterns, real-time progress tracking, and automatic conflict resolution.

## Usage
```
/start-tasks [--mode=autonomous|guided] [--agents=all|selected]
```

## Prerequisites
- **`/break-down`** completed: Task hierarchy with dependencies mapped
- **OPTIONAL `/design-session`** completed: Technical specifications available  
- **TodoWrite integration**: All tasks registered with agent assignments
- **Knowledge base**: Automatically loaded from `agent-docs/knowledge.md` and `agent-docs/try.md`
- **Simplified structure**: 2-file knowledge system for maximum efficiency

## Outputs
- Real-time execution dashboard
- Autonomous task progression with conflict resolution
- Performance metrics and bottleneck analysis
- Automatic handoffs and dependency management
- **OUTPUT FILES**: 
  - Progress Tracking: `agent-docs/EPIC-{ID}-{epic-name}/execution/progress-tracking.md`
  - Execution Logs: `agent-docs/EPIC-{ID}-{epic-name}/execution/execution-logs.md`

## Autonomous Task Orchestration System

**REFERENCE**: Complete agent definitions established in `/break-down`

### Core Execution Intelligence
- **Smart Task Selection**: AI-driven priority optimization with dependency analysis and knowledge pattern matching
- **Parallel Coordination**: Real-time conflict resolution and resource balancing  
- **Autonomous Communication**: Inter-agent messaging with automatic escalation
- **Performance Optimization**: Dynamic bottleneck detection and mitigation using historical patterns
- **Knowledge Integration**: Automatic application of proven solutions from knowledge base
- **Try Item Implementation**: Active tracking and validation of improvement proposals

## 自律的タスク選択アルゴリズム

### 優先度決定マトリックス
```
1. 緊急度 × ビジネス価値 = 基本優先度
2. 依存関係ブロック解除 = +50%重み
3. 他エージェント待機数 = +10% × 待機エージェント数
4. 専門適合度 = ×0.8〜1.2倍
5. 並列実行可能性 = +20%重み
```

### タスク選択フロー（全7エージェント対応）
```
INITIALIZATION:
  - 自動読み込み: agent-docs/knowledge.md（統合知識ベース）
  - 自動読み込み: agent-docs/try.md（改善提案バックログ）
  - エージェント内部での知識処理と適用

FOR EACH AGENT [backend-tdd-architect, frontend-architect, agile-test-strategist, 
                aws-infrastructure-architect, database-design-specialist, 
                product-code-comprehension-expert, agile-product-owner]:
  1. TodoWriteから自分の専門分野タスクを抽出
  2. 知識ベースから関連パターンを検索・適用
  3. 依存関係グラフを動的解析
  4. 優先度マトリックスを適用（Try項目実装にボーナス）
  5. 他6エージェントとの並列実行可能性を確認
  6. 最適タスクを自動選択
  7. in_progressステータスに更新
  8. 依存エージェント（最大6エージェント）に自動通知
  9. 協業パターンマッチングの実行
```

## エージェント間通信プロトコル

### 同期通信（即座応答必要）
```
MESSAGE_TYPE: BLOCKING_REQUEST
PROTOCOL:
  1. SEND_REQUEST(target_agent, request_type, payload)
  2. WAIT_RESPONSE(timeout=30s)
  3. IF timeout THEN escalate_to_coordinator
  4. PROCESS_RESPONSE(response)
  5. UPDATE_LOCAL_STATE(response)
```

### 非同期通信（バッチ処理可能）
```
MESSAGE_TYPE: ASYNC_NOTIFICATION
PROTOCOL:
  1. QUEUE_MESSAGE(target_agents[], message_type, payload)
  2. BATCH_SEND(interval=5min OR queue_size=10)
  3. RECIPIENTS_ACKNOWLEDGE()
  4. UPDATE_DELIVERY_STATUS()
```

### ブロードキャスト通信（全体通知）
```
MESSAGE_TYPE: BROADCAST
PROTOCOL:
  1. VALIDATE_CRITICAL_UPDATE()
  2. SEND_TO_ALL(exclude_sender=true)
  3. COLLECT_ACKNOWLEDGMENTS()
  4. RETRY_FAILED_DELIVERIES(max_retries=3)
```

## 並列実行管理システム

### 依存関係グラフ監視
```
DEPENDENCY_MANAGER:
  1. 動的依存関係マップ生成
  2. 循環依存の自動検出
  3. クリティカルパスの特定
  4. ボトルネック早期警告
  5. 代替実行パスの自動提案
```

### 並列実行パターン（全7エージェント）
```
PATTERN_1: 完全並列（独立性最大化）
├─ backend-tdd-architect: API Layer A
├─ frontend-architect: UI Component X  
├─ database-design-specialist: Schema Y
├─ aws-infrastructure-architect: Environment Z
├─ agile-test-strategist: Test Framework W
├─ product-code-comprehension-expert: Architecture Analysis V
└─ agile-product-owner: Requirements Validation U

PATTERN_2: パイプライン並列（依存関係最適化）
product-code-comprehension → database-design → backend-tdd → 
frontend → aws-infrastructure → agile-test → agile-product-owner

PATTERN_3: 段階的並列（機能別フェーズ）
Phase1: [product-comprehension, agile-product-owner] → 
Phase2: [database-design, backend-tdd, aws-infrastructure] → 
Phase3: [frontend-architect, agile-test-strategist] → 
Phase4: [All agents integration]

PATTERN_4: クロスファンクショナル並列（協業最適化）
Cluster1: [backend-tdd ↔ database-design ↔ product-comprehension]
Cluster2: [frontend ↔ agile-product-owner ↔ agile-test]
Cluster3: [aws-infrastructure ↔ All clusters integration]
```

### 同期ポイント管理
```
SYNC_POINTS:
  1. API仕様確定 → フロントエンド実装開始
  2. データベーススキーマ確定 → バックエンド実装開始
  3. インフラ準備完了 → デプロイ可能
  4. 全コンポーネント完了 → 統合テスト開始
```

## 競合解決と自動調停システム

### 競合検出パターン
```
CONFLICT_TYPE_1: リソース競合
例: 同じAPIエンドポイントを複数エージェントが変更
解決: 最終更新時刻によるマージ + 自動テスト実行

CONFLICT_TYPE_2: 設計方針競合
例: フロントエンドとバックエンドのデータ形式不一致
解決: product-ownerによる自動裁定 + 影響範囲最小化

CONFLICT_TYPE_3: 優先度競合
例: 複数のクリティカルタスクの同時発生
解決: ビジネス価値マトリックス自動適用
```

### ボトルネック自動検出
```
BOTTLENECK_DETECTION:
  1. エージェント待機時間監視（閾値: 10分）
  2. 依存関係チェーン長分析（閾値: 5段階）
  3. クリティカルパス遅延検出（閾値: 予定の150%）
  4. リソース使用率監視（閾値: 80%）

AUTOMATIC_RESOLUTION:
  1. タスク並列化可能性の再評価
  2. 依存関係の一時的なモック化
  3. リソースの動的再配置
  4. 優先度の自動調整
```

## TodoWrite統合とプログレス管理

### 自動ステータス更新
```
TASK_LIFECYCLE_AUTOMATION:
  1. タスク選択 → status: 'in_progress' + assignee設定
  2. 作業開始 → 自動進捗率計算開始
  3. ブロック検出 → status: 'blocked' + blocker_info設定
  4. 依存解決 → status: 'in_progress'復帰
  5. 完了 → status: 'completed' + validation実行
  6. 次タスク → 自動選択・開始
```

### 進捗可視化ダッシュボード（全7エージェント）
```
REAL_TIME_DASHBOARD:
┌─ Agent Status (7 Agents) ──────┐ ┌─ Task Pipeline ───────────────┐
│ 🟢 backend-tdd: API Auth       │ │ ⏳ Pending: 12 tasks         │
│ 🟢 frontend: LoginForm         │ │ 🔄 In Progress: 7 tasks       │
│ 🟡 agile-test: Wait API        │ │ ✅ Completed: 23 tasks        │
│ 🟢 aws-infra: VPC Setup        │ │ 🚫 Blocked: 2 tasks           │
│ 🟢 database: User Schema       │ │ 📊 Overall: 67% complete      │
│ 🔵 product-comprehension: Code │ │ 🔄 Active Agents: 6/7         │
│ 🟢 agile-product: Story Review │ │ ⚡ Collaboration Score: 89%   │
└─────────────────────────────────┘ └─────────────────────────────────┘

┌─ Dependency Graph ─────────────┐ ┌─ Performance Metrics ─────────┐
│     UserSchema                  │ │ Avg Task Duration: 23min       │
│         ↓                       │ │ Bottleneck Time: 8min          │
│    API Endpoints                │ │ Parallel Efficiency: 85%       │
│         ↓                       │ │ Communication Overhead: 12%    │
│   Frontend Forms                │ │ Auto-Resolution Rate: 91%      │
│         ↓                       │ └─────────────────────────────────┘
│  Integration Tests              │
└─────────────────────────────────┘
```

## 実行フェーズと自動化フロー

### フェーズ1: 初期化と調整（0-5分）
```
1. 知識ベース自動読み込み（簡素化）
   - agent-docs/knowledge.md: 統合知識ベース
   - agent-docs/try.md: Try項目バックログ
   - エージェントによる内部処理（シェルスクリプト不要）

2. TodoWriteからタスクリスト取得
3. エージェント間の初期通信テスト
4. 依存関係グラフの構築
5. 初期タスク分散の最適化（知識パターン適用）
6. 各エージェントの作業環境準備確認
7. Try項目実装機会の特定
```

### フェーズ2: 並列実行開始（5分-完了）
```
WHILE tasks_remaining > 0:
  FOR EACH AGENT IN parallel:
    1. 利用可能タスクの自動スキャン
    2. 知識ベースから関連パターンを自動適用
       - 技術パターン: JWT認証、API-First、マイクロサービス等
       - ビジネスインサイト: ユーザーエンゲージメント等
       - プロセス改善: 協業パターン、CI/CD等
    3. Try項目実装の統合
       - OpenAPI Contract-Firstの適用
       - Parallel DB Migrationの実行
       - Infrastructure Templateの活用
    4. 最適タスクの選択と開始
    5. 進捗状況の定期報告
    6. ブロック・完了の即座通知
    7. 知識活用の記録（使用回数、有用性評価）
    8. 次タスクの自動開始
  
  COORDINATOR_ACTIONS:
    1. 全体進捗の監視
    2. ボトルネック自動検出
    3. 競合の自動解決
    4. リソース再配置の実行
    5. 知識ギャップの識別
```

### フェーズ3: 統合と検証（自動トリガー）
```
WHEN all_implementation_tasks_completed:
  1. 自動統合テスト実行
  2. パフォーマンステスト自動実行
  3. セキュリティスキャン自動実行
  4. 品質ゲート自動チェック
  5. デプロイ準備状況確認
```

## 緊急時対応プロトコル

### 全エージェントブロック状態
```
EMERGENCY_PROTOCOL_1:
  1. 循環依存の強制解決（最小影響タスクの一時スキップ）
  2. モック・スタブによる依存関係迂回
  3. タスク分割の緊急実行
  4. 手動介入要求の自動発行
```

### クリティカルエラー発生
```
EMERGENCY_PROTOCOL_2:
  1. 影響範囲の自動分析
  2. ロールバック可能性の確認
  3. 関連タスクの自動一時停止
  4. エラー修正の優先タスク化
  5. 復旧後の自動再開
```

### パフォーマンス劣化検出
```
EMERGENCY_PROTOCOL_3:
  1. リソース使用量の自動分析
  2. 非効率タスクの特定と最適化
  3. 並列度の動的調整
  4. メモリ・CPU使用量の監視強化
```

## 成功指標と自動評価

### リアルタイム指標
```
REAL_TIME_METRICS:
  - タスク完了率: X% (目標: >90%)
  - 平均待機時間: X分 (目標: <5分)
  - 自動解決率: X% (目標: >85%)
  - 並列効率: X% (目標: >80%)
  - 通信オーバーヘッド: X% (目標: <15%)
  - 知識活用率: X% (目標: >70%)
  - Try項目実装率: X% (アクティブ項目中)
  - パターン適用成功率: X% (目標: >80%)
```

### 完了時評価
```
POST_COMPLETION_ANALYSIS:
  1. 総実行時間 vs 予測時間
  2. エージェント個別パフォーマンス
  3. ボトルネック発生パターン
  4. 自動解決の効果測定
  5. 次回最適化提案の自動生成
```

## Execution Success Metrics

### Real-Time KPIs
- **Task Completion Rate**: >90% autonomous success
- **Average Wait Time**: <5 minutes between tasks
- **Parallel Efficiency**: >80% concurrent execution
- **Auto-Resolution Rate**: >85% conflicts resolved without intervention
- **Communication Overhead**: <15% of total execution time

### Performance Dashboard
```
Agent Status        │ Task Pipeline        │ Dependencies
🟢 backend: API     │ ⏳ Pending: 12       │ Critical Path: 67%
🟢 frontend: UI     │ 🔄 Progress: 7       │ Parallel Ready: 8
🟡 test: Waiting    │ ✅ Complete: 23      │ Blocked: 2
🟢 aws: Deploy      │ 📊 Overall: 67%      │ Auto-resolved: 15
```

## 標準化されたファイル出力仕様

### Epic-Based Directory Organization
```
agent-docs/
├── EPIC-{ID}-{epic-name}/
│   ├── breakdown/
│   │   ├── epic-definition.md       ← /break-down 出力
│   │   ├── stories.md               ← /break-down 出力
│   │   ├── tasks.md                 ← /break-down 出力
│   │   └── dependencies.md          ← /break-down 出力
│   ├── design/
│   │   ├── architecture-diagrams.md ← /design-session 出力
│   │   ├── component-designs.md     ← /design-session 出力
│   │   └── data-flows.md            ← /design-session 出力
│   ├── execution/
│   │   ├── progress-tracking.md     ← このコマンドの出力
│   │   └── execution-logs.md        ← このコマンドの出力
│   ├── validation/
│   │   ├── quality-reports.md       ← /task-done 出力
│   │   └── completion-status.md     ← /task-done 出力
│   ├── analysis/
│   │   ├── retrospective-data.md    ← /retrospective 出力
│   │   └── metrics.md               ← /retrospective 出力
│   └── knowledge/
│       ├── learnings.md             ← /knowledge-share 出力
│       └── best-practices.md        ← /knowledge-share 出力
```

### 自動ディレクトリ作成とファイル出力
```
出力実行時に以下を自動実行：
1. Epic IDとepic-nameを既存の breakdown/epic-definition.md から取得
2. 同じ `agent-docs/EPIC-{ID}-{epic-name}/execution/` ディレクトリを使用
3. 2つのファイルとして実行状況を構造化出力：
   - progress-tracking.md: リアルタイム進捗状況ダッシュボード
   - execution-logs.md: タスク実行ログとボトルネック分析
4. breakdown/ と design/ ディレクトリとの相互参照リンクを含める
5. 実行中は継続的に更新（進捗・ボトルネック・メトリクス）
```

### Cross-Reference Integration
```yaml
ファイルヘッダーに含める参照情報:
epic_info:
  id: "EPIC-{ID}"
  name: "{epic-name}"
  directory: ".claude/agent-docs/EPIC-{ID}-{epic-name}/"
  source_breakdown: "breakdown/"
  source_design: "design/"
  
related_files:
  breakdown:
    epic_definition: "breakdown/epic-definition.md"
    stories: "breakdown/stories.md"
    tasks: "breakdown/tasks.md"
    dependencies: "breakdown/dependencies.md"
  design:
    architecture_diagrams: "design/architecture-diagrams.md"
    component_designs: "design/component-designs.md"
    data_flows: "design/data-flows.md"
  validation:
    quality_reports: "validation/quality-reports.md"
    completion_status: "validation/completion-status.md"
  analysis:
    retrospective_data: "analysis/retrospective-data.md"
    metrics: "analysis/metrics.md"
  knowledge:
    learnings: "knowledge/learnings.md"
    best_practices: "knowledge/best-practices.md"
  
execution_context:
  task_source: "breakdown/tasks.md で定義された7エージェント別タスク"
  dependency_management: "breakdown/dependencies.md の依存関係グラフに基づく実行"
  design_reference: "design/ ディレクトリの設計仕様に基づく実装"
  continuous_updates: "実行中は進捗状況を継続的に更新"
```

### Real-Time Update Strategy
```yaml
dashboard_updates:
  frequency: "5分間隔"
  trigger_events:
    - タスク開始・完了
    - ボトルネック検出
    - エージェント間通信
    - 依存関係解除
    - 品質ゲート通過/失敗
  
content_sections:
    - 全7エージェント実行状況
    - タスクパイプライン状況  
    - 依存関係グラフ更新
    - パフォーマンスメトリクス
    - ボトルネック分析
    - 自動解決アクション
```

## Workflow Integration & Handoffs

### FROM Previous Commands
- **`/break-down`**: Task hierarchy with agent assignments
- **`/design-session`**: Technical specifications (if complex)

### TO Next Commands  
- **`/task-done`**: Individual task completion notifications
- **Continuous**: Real-time progress updates and conflict resolution

### Output Integration
- **TodoWrite Updates**: Automatic status progression
- **Performance Analytics**: Efficiency metrics for `/retrospective`
- **Knowledge Capture**: Learning points for `/knowledge-share`

### 重要：出力ファイル作成指示
**実行時には必ず以下を実行してください：**
1. 既存の breakdown/epic-definition.md からEpic ID と名前を特定
2. 同じ Epic ディレクトリに `execution/` フォルダを作成
3. 2つのファイルに実行状況を構造化記録：
   - progress-tracking.md: 7エージェント別進捗、知識活用状況、Try項目実装
   - execution-logs.md: 詳細実行ログ、ボトルネック、メトリクス
4. breakdown/ と design/ ディレクトリとの関連性を各ファイルで明記
5. 各ファイル先頭にメタデータとcross-reference情報を含める
6. 実行完了まで継続的に両ファイルを更新
7. **知識ベース更新**:
   - agent-docs/knowledge.md への使用統計更新
   - agent-docs/try.md への進捗状況反映
   - 新たな発見の直接記録（複雑なディレクトリ構造なし）