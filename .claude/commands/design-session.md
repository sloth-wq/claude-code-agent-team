# Visual Design Session

**CORE PURPOSE**: Create comprehensive visual designs and technical specifications for complex Epic/Stories requiring detailed upfront planning.

**UNIQUE SCOPE**: Architecture diagrams, component designs, data flows, and implementation blueprints.

## Usage
```
/design-session "Epic or Story requiring design"
```

## Prerequisites
- `/break-down` completed with Epic/Story/Task structure
- Agent roles and responsibilities established
- Complex technical requirements identified
- Knowledge base automatically loaded from `agent-docs/knowledge.md` and `agent-docs/try.md`

## Outputs
- Visual architecture diagrams
- Component interaction designs
- Data flow specifications
- Implementation blueprints
- Technical decision records
- **OUTPUT FILES**: 
  - Architecture Diagrams: `agent-docs/EPIC-{ID}-{epic-name}/design/architecture-diagrams.md`
  - Component Designs: `agent-docs/EPIC-{ID}-{epic-name}/design/component-designs.md`
  - Data Flows: `agent-docs/EPIC-{ID}-{epic-name}/design/data-flows.md`

## Design-Focused Collaboration Protocol

**COMPREHENSIVE 7-AGENT APPROACH**: All agents contribute specialized design expertise while referencing established roles from `/break-down`

**AUTOMATIC KNOWLEDGE INTEGRATION**: 
- Load `agent-docs/knowledge.md` for design patterns and technical solutions
- Apply `agent-docs/try.md` improvements to design decisions
- No user input required - autonomous pattern application
- Simplified 2-file structure for maximum efficiency

### Phase 1: Context Loading & Requirements Alignment (5 min)
```
自動知識ベース統合（簡素化）:
- agent-docs/knowledge.md: 統合知識ベースから関連設計パターンを自動抽出
- agent-docs/try.md: 改善提案から設計最適化機会を特定
- エージェント内部での知識処理（シェルスクリプト不要）

product-code-comprehension-expert: 「知識ベースと既存実装を統合分析：
- 現在のアーキテクチャ制約と統合ポイント
- 過去の成功パターンの適用機会
- 技術的負債と改善機会（Try項目参照）
- 既存システムとの依存関係」

agile-product-owner: 「ビジネス要求を設計観点で明確化：
- ユーザーストーリーの設計制約
- ビジネスルールの技術実装要件
- 優先度と段階的実装戦略
- 成功指標の技術的測定方法」

全エージェント: 設計コンテキストと制約事項の共通理解確立
```

### Phase 2: Parallel Specialized Design Creation (15 min)
```
知識ベース活用した並行設計作業 - 各エージェントが専門領域で設計図を作成：

backend-tdd-architect: 「APIとデータフロー設計（知識パターン適用）：
- RESTful/GraphQLエンドポイント仕様（API-First開発パターン適用）
- データ変換ロジックとビジネスルール
- テスト戦略に基づくモジュール設計（TDD自動化戦略適用）
- マイクロサービス間の契約定義（通信パターン適用）」

frontend-architect: 「UI/UXコンポーネント設計：
- コンポーネント階層と状態管理
- ユーザーフローと画面遷移
- レスポンシブデザインとアクセシビリティ
- パフォーマンス最適化設計」

database-design-specialist: 「データモデルと最適化設計：
- ER図とスキーマ定義
- インデックス戦略とクエリ最適化
- データ整合性とトランザクション設計
- スケーラビリティ考慮事項」

aws-infrastructure-architect: 「システム構成と運用設計：
- クラウドアーキテクチャ図
- CI/CDパイプラインとデプロイ戦略
- セキュリティと監視設計
- スケーリングとコスト最適化」

agile-test-strategist: 「テスト戦略と品質保証設計：
- テストピラミッドとカバレッジ戦略
- 自動化シナリオとデータ戦略
- パフォーマンステストとセキュリティテスト
- 品質ゲートと検証フロー」
```

### Phase 3: Integration Review & Cross-Validation (10 min)
```
agile-product-owner: 「ビジネス要求との整合性確認：
- 各設計がユーザー価値を実現するか
- 優先度と実装順序の妥当性
- リスクと緩和策の評価
- ROIと実装コストのバランス」

全エージェント による統合設計レビュー：
- backend-tdd-architect ↔ database-design-specialist: データフロー整合性
- frontend-architect ↔ backend-tdd-architect: API契約とUIデータ要件
- aws-infrastructure-architect ↔ 全エージェント: 運用制約と技術選択
- agile-test-strategist ↔ 全エージェント: テスト可能性とカバレッジ
- product-code-comprehension-expert: 既存システムとの統合可能性
- agile-product-owner: ビジネス価値実現への最終確認

統合ポイントと引き継ぎ要件の特定と文書化
```

## Specialized Design Deliverables

**REFERENCE**: Agent roles defined in `/break-down` - focus on design artifacts only

### Visual Design Outputs by Domain
- **System Architecture**: Component interaction & deployment topology
- **API Contracts**: Endpoint specifications & data schemas  
- **UI/UX Flows**: Component hierarchies & user journeys
- **Data Models**: Entity relationships & query patterns
- **Test Strategies**: Validation flows & coverage maps
- **Business Processes**: Value flows & decision points

## 協業による設計プロセス

### フェーズ1: 既存コード分析（5分）
```
product-code-comprehension-expert: 「既存実装を分析します：
- 現在のアーキテクチャ: [分析結果]
- 再利用可能なコンポーネント: [リスト]
- 制約事項: [リスト]」

全エージェント: 既存コードの制約を理解
```

### フェーズ2: 並行設計作業（15分）
```
並行して全7エージェントが専門領域の設計図を作成：

backend-tdd-architect: APIとデータフロー設計
- エンドポイント仕様とビジネスロジック
- テスト駆動設計アプローチ

frontend-architect: UI階層と画面遷移設計
- コンポーネント設計とユーザーフロー
- レスポンシブ・アクセシビリティ配慮

database-design-specialist: データモデルとER図作成
- スキーマ設計とクエリ最適化
- データ整合性とパフォーマンス

aws-infrastructure-architect: システム構成図作成
- クラウドアーキテクチャとCI/CD
- セキュリティと運用設計

agile-test-strategist: テストシナリオ設計
- テスト戦略とカバレッジ計画
- 品質保証フローとメトリクス

product-code-comprehension-expert: アーキテクチャ分析設計
- 既存システム統合パターン
- 技術的負債と改善戦略

agile-product-owner: ビジネス価値設計
- ユーザージャーニーとビジネスフロー
- 価値実現指標と測定方法
```

### フェーズ3: 統合レビュー（10分）
```
agile-product-owner: 「各設計を統合確認：
- 要件との整合性: [確認]
- ビジネス価値実現度: [確認]
- 実装優先度と段階: [確認]」

全7エージェント による相互検証：
- backend-tdd-architect: API仕様とテスト戦略の整合性確認
- frontend-architect: UIコンポーネントとAPIの統合確認
- database-design-specialist: データモデルと全体アーキテクチャの整合性
- aws-infrastructure-architect: インフラ制約と技術選択の妥当性
- agile-test-strategist: テスト可能性と品質保証の実現性
- product-code-comprehension-expert: 既存システムとの統合リスク評価
- agile-product-owner: ビジネス要求と技術実装の最終調整

統合設計の最終確認とフィードバック反映
```

## 設計テンプレート集

### 1. システムアーキテクチャ図（aws-infrastructure-architect担当）

```
【全体システム構成図】
┌─────────────────────────────────────────────────────────┐
│                    クライアント層                         │
├──────────────────┬────────────────┬────────────────────┤
│   Web (React)    │ Mobile (RN)    │   Admin (Next.js)  │
└────────┬─────────┴───────┬────────┴────────┬──────────┘
         │                 │                  │
         └─────────────────┼──────────────────┘
                           │
                  ┌────────▼────────┐
                  │  API Gateway    │
                  │  (認証・認可)    │
                  └────────┬────────┘
                           │
         ┌─────────────────┼─────────────────┐
         │                 │                 │
    ┌────▼─────┐    ┌─────▼─────┐    ┌─────▼─────┐
    │  Service  │    │  Service  │    │  Service  │
    │     A     │    │     B     │    │     C     │
    └────┬─────┘    └─────┬─────┘    └─────┬─────┘
         │                 │                 │
         └─────────────────┼─────────────────┘
                           │
                  ┌────────▼────────┐
                  │   データ層       │
                  │  (DB + Cache)   │
                  └─────────────────┘

【記入項目】
- Service A: [サービス名と責任]
- Service B: [サービス名と責任]
- Service C: [サービス名と責任]
- データ層の技術: [PostgreSQL/Redis等]
```

### 2. データフロー図（backend-tdd-architect担当）

```
【APIデータフロー図】

[クライアント] ──POST /api/auth/login──▶ [認証API]
                                          │
                                          ▼
                                    [認証サービス]
                                          │
                        ┌─────────────────┼─────────────────┐
                        ▼                 ▼                 ▼
                  [ユーザー検証]    [トークン生成]    [セッション管理]
                        │                 │                 │
                        ▼                 ▼                 ▼
                  [ユーザーDB]      [JWT生成]         [Redis Cache]
                        │                 │                 │
                        └─────────────────┼─────────────────┘
                                          ▼
                                    [レスポンス]
                                          │
                                          ▼
                                    [クライアント]

【記入項目】
- 認証API: [エンドポイント詳細]
- 認証サービス: [ビジネスロジック]
- データベース: [テーブル名]
- レスポンス形式: [JSON構造]
```

### 3. コンポーネント階層図（frontend-architect担当）

```
【React コンポーネント階層図】

                    ┌─────────────┐
                    │     App     │
                    └─────┬───────┘
                          │
            ┌─────────────┼─────────────┐
            │             │             │
     ┌──────▼──────┐ ┌───▼───┐ ┌──────▼──────┐
     │  AuthGuard  │ │Layout │ │  ErrorBound │
     └─────────────┘ └───┬───┘ └─────────────┘
                         │
            ┌────────────┼────────────┐
            │            │            │
     ┌──────▼──────┐ ┌──▼──┐ ┌──────▼──────┐
     │   Header    │ │Main │ │   Footer    │
     └─────────────┘ └──┬──┘ └─────────────┘
                        │
         ┌──────────────┼──────────────┐
         │              │              │
  ┌──────▼──────┐ ┌────▼────┐ ┌──────▼──────┐
  │ LoginForm   │ │HomePage │ │ProfilePage  │
  └─────────────┘ └─────────┘ └─────────────┘

【記入項目】
- 各コンポーネントの責任: [説明]
- Props: [親から子への データ]
- State: [各コンポーネントの状態]
```

### 4. データベース設計図（database-design-specialist担当）

```
【ER図】

┌─────────────┐      ┌─────────────┐      ┌─────────────┐
│   users     │      │  sessions   │      │  products   │
├─────────────┤      ├─────────────┤      ├─────────────┤
│ id (PK)     │──┐   │ id (PK)     │      │ id (PK)     │
│ email       │  │   │ user_id(FK) │      │ name        │
│ password    │  └──▶│ token       │      │ price       │
│ name        │      │ expires_at  │      │ category_id │
│ created_at  │      │ created_at  │      │ created_at  │
└─────────────┘      └─────────────┘      └─────────┬───┘
                                                     │
                                              ┌──────▼──────┐
                                              │ categories  │
                                              ├─────────────┤
                                              │ id (PK)     │
                                              │ name        │
                                              │ parent_id   │
                                              └─────────────┘

【記入項目】
- 各テーブルの目的: [説明]
- インデックス: [パフォーマンス最適化]
- 制約: [データ整合性]
```

### 5. テストシナリオ図（agile-test-strategist担当）

```
【テストフロー図】

[テスト開始]
     │
     ▼
┌─────────────┐    Pass    ┌─────────────┐
│ ユニット    │ ──────────▶│ 統合テスト   │
│ テスト      │            │             │
└─────┬───────┘            └─────┬───────┘
      │ Fail                     │ Pass
      ▼                          ▼
┌─────────────┐            ┌─────────────┐
│ バグ修正    │            │ E2Eテスト   │
└─────────────┘            └─────┬───────┘
                                 │ Pass
                                 ▼
                           ┌─────────────┐
                           │ リリース    │
                           └─────────────┘

【記入項目】
- ユニットテスト: [対象コンポーネント]
- 統合テスト: [API連携テスト]
- E2Eテスト: [ユーザーシナリオ]
```

## 設計品質チェックリスト

### 知識ベース活用
- [ ] 関連する技術パターンが適用されている
- [ ] Try項目の実装機会が検討されている
- [ ] 過去の学習が設計に反映されている
- [ ] 新たな発見が記録準備されている

### 視覚的明確性
- [ ] 図に【タイトル】が明記されている
- [ ] 矢印の方向が明確
- [ ] コンポーネント名が実装と一致している
- [ ] 依存関係が理解しやすい

### 実装可能性
- [ ] 技術的制約が考慮されている
- [ ] 既存コードとの統合が可能
- [ ] 各エージェントのタスクが明確

### エージェント協業
- [ ] 各エージェントの設計が整合している
- [ ] インターフェースが明確に定義されている
- [ ] 責任範囲が重複していない

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
│   │   ├── architecture-diagrams.md ← このコマンドの出力
│   │   ├── component-designs.md     ← このコマンドの出力
│   │   └── data-flows.md            ← このコマンドの出力
│   ├── execution/
│   │   ├── progress-tracking.md     ← /start-tasks 出力
│   │   └── execution-logs.md        ← /start-tasks 出力
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
2. 同じ `agent-docs/EPIC-{ID}-{epic-name}/design/` ディレクトリを使用
3. 3つのファイルとして設計結果を構造化出力：
   - architecture-diagrams.md: システム全体構成図と技術アーキテクチャ
   - component-designs.md: コンポーネント設計とUI/UX仕様
   - data-flows.md: データフローとAPI仕様
4. breakdown/ ディレクトリとの相互参照リンクを含める
```

### Cross-Reference Integration
```yaml
ファイルヘッダーに含める参照情報:
epic_info:
  id: "EPIC-{ID}"
  name: "{epic-name}"
  directory: ".claude/agent-docs/EPIC-{ID}-{epic-name}/"
  source_breakdown: "breakdown/"
  
related_files:
  breakdown:
    epic_definition: "breakdown/epic-definition.md"
    stories: "breakdown/stories.md"
    tasks: "breakdown/tasks.md"
    dependencies: "breakdown/dependencies.md"
  execution:
    progress_tracking: "execution/progress-tracking.md"
    execution_logs: "execution/execution-logs.md"
  validation:
    quality_reports: "validation/quality-reports.md"
    completion_status: "validation/completion-status.md"
  analysis:
    retrospective_data: "analysis/retrospective-data.md"
    metrics: "analysis/metrics.md"
  knowledge:
    learnings: "knowledge/learnings.md"
    best_practices: "knowledge/best-practices.md"
  
design_context:
  based_on_epic: "詳細は breakdown/epic-definition.md を参照"
  implements_stories: "breakdown/stories.md で定義されたユーザーストーリーの技術実装設計"
  builds_tasks: "breakdown/tasks.md のタスク分解に基づく詳細設計"
  considers_dependencies: "breakdown/dependencies.md の依存関係を考慮した設計"
```

## Design Session Completion & Handoffs

### Immediate Outputs
1. **Consolidated Design Document**: All visual diagrams in unified format
2. **Implementation Guidelines**: Technical specifications for task execution
3. **Design Decision Records**: Rationale for architectural choices

### Workflow Transitions
- **TO `/start-tasks`**: Design blueprints inform parallel implementation
- **TO `/task-done`**: Design validation during task completion
- **ITERATIVE**: Design updates fed back during implementation

### Design Quality Gates
- Technical feasibility confirmed
- Business requirements mapped
- Integration points defined
- Implementation effort validated

### 重要：出力ファイル作成指示
**実行時には必ず以下を実行してください：**
1. 既存の breakdown/epic-definition.md からEpic ID と名前を特定
2. 同じ Epic ディレクトリに `design/` フォルダを作成
3. 3つのファイルに設計結果を構造化保存：
   - architecture-diagrams.md: 全体システム構成とインフラ設計、適用パターン
   - component-designs.md: UI/UXコンポーネントと機能設計、再利用パターン
   - data-flows.md: データフローとAPI契約設計、統合パターン
4. breakdown/ ディレクトリとの関連性を各ファイルで明記
5. 各ファイル先頭にメタデータとcross-reference情報を含める
6. **知識ベース更新**:
   - agent-docs/knowledge.md への使用統計更新
   - agent-docs/try.md への進捗反映
   - 新たな設計発見の直接記録