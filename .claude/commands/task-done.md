# Task Completion with Intelligent Handoffs

**CORE PURPOSE**: Execute comprehensive task validation, automatic dependency resolution, and seamless workflow transitions.

**UNIQUE SCOPE**: Quality gates, progress validation, automatic handoffs, and learning capture.

## Usage
```
/task-done "Completed task name" [--validation-level=strict|standard] [--auto-handoff=true]
```

## Prerequisites
- Task actively in `in_progress` status in TodoWrite
- Clear completion deliverables defined
- Agent roles established from `/break-down`

## Outputs
- Quality validation report
- Automatic dependency unblocking
- Next task recommendations
- Performance analytics
- Knowledge capture entries
- **OUTPUT FILES**: 
  - Quality Reports: `agent-docs/EPIC-{ID}-{epic-name}/validation/quality-reports.md`
  - Completion Status: `agent-docs/EPIC-{ID}-{epic-name}/validation/completion-status.md`

## Core Execution Flow

### 1. Multi-Level Quality Validation

**STREAMLINED APPROACH**: Leverages agent expertise defined in `/break-down`

#### Technical Quality Gates
```yaml
Code Quality:
  - ESLint/TSLint/SonarQube compliance
  - Test coverage ≥80% (critical paths 100%)
  - TypeScript strict mode conformance
  - Security vulnerability scan clearance
  - Performance benchmark achievement

Business Validation:
  - All Acceptance Criteria satisfied
  - Design system compliance
  - Accessibility WCAG 2.1 AA standards
  - Internationalization support (when required)
```

#### レベル2: 全7エージェント統合検証マトリックス
```yaml
統合検証マトリックス（全エージェント参加必須）:
  backend-tdd-architect:
    - API契約適合性チェック（frontend, product-comprehensionと連携）
    - データベーススキーマ整合性（database-designと検証）
    - 非機能要件達成（aws-infrastructure, agile-testと確認）
    - TDD原則実装度とテストカバレッジ品質

  frontend-architect:
    - コンポーネント設計原則準拠（product-ownerの要求との整合）
    - 状態管理アーキテクチャ整合性（backend APIとの統合）
    - ブラウザ互換性確認（agile-testシナリオと協調）
    - アクセシビリティ基準達成とUX品質

  agile-test-strategist:
    - テスト戦略実装完了度（全エージェント成果物への適用）
    - 回帰テスト影響分析（product-comprehensionと協調）
    - E2Eシナリオ検証（frontend, backendとの統合）
    - 品質ゲート達成とメトリクス収集

  aws-infrastructure-architect:
    - インフラ要件充足（全エージェント成果物のデプロイ要件）
    - CI/CDパイプライン統合（agile-test戦略との連携）
    - 監視・ログ設定（運用チームとproduct-ownerへの可視性）
    - セキュリティとコンプライアンス確保

  database-design-specialist:
    - データモデル整合性（backend, frontendアクセスパターンとの整合）
    - クエリパフォーマンス最適化（aws監視指標との連携）
    - データ移行戦略実装（product-comprehensionの分析活用）
    - データ整合性とトランザクション安全性

  product-code-comprehension-expert:
    - ドメインロジック正確性（agile-product-ownerとの業務整合性）
    - ビジネスルール実装検証（backend, frontendでの一貫性）
    - 技術負債評価（全エージェント成果物への影響分析）
    - アーキテクチャ品質と将来拡張性

  agile-product-owner:
    - ビジネス価値実現確認（全エージェント成果物の統合評価）
    - ユーザーストーリー完了度（frontend UX, backendロジック確認）
    - 市場適合性評価（agile-testシナリオとの整合性）
    - ステークホルダー要求への適合度とROI測定
```

#### レベル3: システム全体整合性検証
```yaml
総合品質ゲート:
  - 📋 全依存タスク完了確認
  - 🔄 統合テスト自動実行
  - 📊 メトリクス収集と分析
  - 🔍 セキュリティポスチャ評価
  - 🌐 本番環境類似環境での検証
```

### 2. Intelligent Dependency Resolution

#### 高度な依存関係解析エンジン
```typescript
interface DependencyGraph {
  directDependencies: TaskDependency[];
  transitiveDependencies: TaskDependency[];
  criticalPath: Task[];
  parallelizableGroups: Task[][];
  riskAssessment: RiskLevel;
}

// 自動ブロック解除の例
完了: "ユーザー認証APIエンドポイント作成"
↓ AI駆動の影響分析
解除対象の分析:
  - 直接依存: [
      "ログインフォームUI実装" [frontend-architect],
      "認証ミドルウェア統合テスト" [agile-test-strategist],
      "JWT設定とデプロイ" [aws-infrastructure-architect]
    ]
  - 間接的影響: [
      "ユーザープロファイル管理" [backend-tdd-architect],
      "権限制御UI" [frontend-architect],
      "認証データベース最適化" [database-design-specialist]
    ]
  - 並列実行可能: [
      "商品カタログAPI" [backend-tdd-architect],
      "検索UI実装" [frontend-architect]
    ]
```

#### 全7エージェント統合通知システム
```yaml
自動通知マトリックス（相互連携パターン）:
  backend-tdd-architect → [6エージェント]:
    → frontend: 新しいAPI契約・エンドポイント仕様
    → database: スキーマ変更要求・データアクセスパターン
    → aws-infra: デプロイ要件・非機能要件更新
    → agile-test: APIテスト要件・パフォーマンス基準
    → product-comprehension: ビジネスロジック実装・ドメインモデル変更
    → agile-product: 機能実装状況・ビジネス価値実現度

  frontend-architect → [6エージェント]:
    → backend: UIデータ要求・API仕様要件
    → database: フロントエンド表示データ要件
    → aws-infra: 静的アセット配信・CDN要件
    → agile-test: UIテストシナリオ・ユーザビリティテスト
    → product-comprehension: UI/UXパターン・コンポーネント設計
    → agile-product: ユーザーエクスペリエンス・UI改善提案

  agile-test-strategist → [6エージェント]:
    → backend: APIテスト結果・パフォーマンステスト要求
    → frontend: UIテスト結果・アクセシビリティ評価
    → database: データ整合性テスト・パフォーマンス評価
    → aws-infra: 負荷テスト・セキュリティテスト結果
    → product-comprehension: テスト戦略・品質評価
    → agile-product: 品質ゲート状況・リリース準備度

  aws-infrastructure-architect → [6エージェント]:
    → backend: インフラ制約・スケーリング設定
    → frontend: CDN設定・デプロイ環境
    → database: データベースインフラ・バックアップ戦略
    → agile-test: テスト環境・CI/CDパイプライン
    → product-comprehension: 運用制約・技術選択影響
    → agile-product: コスト影響・運用可能性

  database-design-specialist → [6エージェント]:
    → backend: スキーマ変更・クエリ最適化提案
    → frontend: データ構造・表示用データ形式
    → aws-infra: データベースリソース要件・バックアップ要求
    → agile-test: データテスト要件・整合性チェック
    → product-comprehension: データモデル影響・ビジネスルール整合性
    → agile-product: データ品質・分析要件

  product-code-comprehension-expert → [6エージェント]:
    → backend: アーキテクチャガイダンス・技術負債評価
    → frontend: コンポーネント設計・実装パターン提案
    → database: データモデル最適化・アクセスパターン分析
    → aws-infra: アーキテクチャ決定・技術選択推奨
    → agile-test: コード品質評価・テスト戦略連携
    → agile-product: 技術実現可能性・実装コスト評価

  agile-product-owner → [6エージェント]:
    → backend: ビジネス要求明確化・優先度調整
    → frontend: UX要求・ユーザーフィードバック
    → database: データ要件・ビジネスルール
    → aws-infra: 運用要求・SLA・コスト制約
    → agile-test: 受け入れ基準・品質基準
    → product-comprehension: ドメイン知識・業務要求詳細
```

### 3. 次世代タスク選択とシームレス引き継ぎ

#### AI駆動の最適タスク選択アルゴリズム
```python
def intelligent_task_selection():
    factors = {
        'dependency_unblocking': 0.4,    # 他の待機解消
        'context_preservation': 0.25,   # コンテキスト維持
        'business_value': 0.2,          # ビジネス価値
        'risk_mitigation': 0.1,         # リスク軽減
        'team_capacity': 0.05           # チーム負荷分散
    }
    
    scores = calculate_weighted_scores(available_tasks, factors)
    return optimize_with_constraints(scores, team_constraints)
```

#### エージェント間引き継ぎプロトコル
```yaml
引き継ぎシーケンス:
  1. 完了エージェント:
     - 成果物サマリー生成
     - 実装詳細ドキュメント作成
     - 知識移転ポイント抽出
     - 潜在課題・改善点記録

  2. 次エージェント:
     - コンテキスト自動受信
     - 依存情報の確認
     - 作業環境セットアップ
     - 継続タスクの優先順位設定

  3. 全エージェント:
     - 進捗状況の共有
     - ブロッカー・リスクの更新
     - 協業機会の特定
```

### 4. リアルタイムTodoWrite統合とプログレス追跡

#### 高度なタスク状態管理
```typescript
interface EnhancedTaskStatus {
  id: string;
  status: 'pending' | 'in_progress' | 'review' | 'testing' | 'completed';
  owner: AgentType;
  progress: {
    percentage: number;
    milestones: Milestone[];
    blockers: Blocker[];
    estimatedCompletion: Date;
  };
  qualityGates: QualityGateResult[];
  dependencies: {
    blocking: Task[];
    blocked_by: Task[];
    parallel_with: Task[];
  };
  metrics: {
    startTime: Date;
    actualEffort: Duration;
    complexityScore: number;
    reworkCount: number;
  };
}
```

#### リアルタイム進捗ダッシュボード（全7エージェント統合）
```yaml
プロジェクト状況:
  全体進捗: 67% (34/51 tasks completed)
  7エージェント協業効率: 89% (目標85%超過達成)
  
  エージェント別状況:
    backend-tdd-architect: 🟢 進行中 (8/12 completed, 協業度: 95%)
    frontend-architect: 🟡 待機中 (5/9 completed, 2 blocked, 協業度: 87%)
    agile-test-strategist: 🟢 進行中 (6/8 completed, 協業度: 91%)
    aws-infrastructure-architect: 🟢 進行中 (4/6 completed, 協業度: 83%)
    database-design-specialist: ✅ 完了 (5/5 completed, 協業度: 98%)
    product-code-comprehension-expert: 🟢 進行中 (3/5 completed, 協業度: 92%)
    agile-product-owner: 🟡 レビュー中 (3/6 completed, 協業度: 85%)

  エージェント間協業マトリクス:
    - backend ↔ database: 🟢 最高効率 (98%)
    - frontend ↔ agile-product: 🟢 良好 (88%)
    - agile-test ↔ 全エージェント: 🟢 品質連携 (90%)
    - aws-infra ↔ backend/database: 🟡 改善余地 (81%)
    - product-comprehension ↔ 全エージェント: 🟢 優秀 (92%)

  クリティカルパス（7エージェント視点）:
    - 🔥 ユーザー認証統合 (2日遅延リスク, 3エージェント影響)
    - ⚡ 決済システム連携 (優先度高, 5エージェント参加)
    - 📊 分析ダッシュボード (依存関係複雑, 全7エージェント連携要)
```

### 5. 自動ドキュメント生成と知識共有

#### インテリジェント文書化
```yaml
自動生成ドキュメント:
  技術ドキュメント:
    - API仕様書 (OpenAPI 3.0)
    - データベーススキーマ図
    - アーキテクチャ決定記録 (ADR)
    - 設定・デプロイメントガイド

  業務ドキュメント:
    - 機能仕様書
    - ユーザーガイド
    - テストシナリオ
    - 運用手順書

  知識ベース:
    - 技術Tips集
    - トラブルシューティングガイド
    - ベストプラクティス集
    - 学習リソース
```

#### エージェント間知識共有プラットフォーム
```yaml
知識共有システム:
  即時共有:
    - Slack/Teams統合
    - コードコメント自動同期
    - 設計判断の履歴管理

  構造化知識:
    - Confluence/Notion統合
    - 検索可能な技術Q&A
    - プロジェクト固有の用語集

  学習促進:
    - ペアプログラミング推奨
    - コードレビュー強化
    - 定期的な技術共有会
```

### 6. パフォーマンス測定と継続的改善ループ

#### 包括的メトリクス収集
```yaml
効率性指標:
  開発速度:
    - ストーリーポイント/Sprint
    - リードタイム短縮率
    - デプロイ頻度向上

  品質指標:
    - バグ検出率低下
    - カスタマー満足度向上
    - 技術負債削減

  協業指標:
    - エージェント間待機時間
    - 依存関係解決時間
    - 知識共有頻度

  ビジネス指標:
    - 機能利用率
    - ユーザー価値実現時間
    - ROI改善
```

#### AI駆動の改善提案エンジン
```python
class ContinuousImprovementEngine:
    def analyze_patterns(self):
        return {
            'bottlenecks': identify_workflow_bottlenecks(),
            'optimization_opportunities': find_optimization_points(),
            'best_practices': extract_successful_patterns(),
            'risk_factors': assess_project_risks()
        }
    
    def generate_recommendations(self):
        return {
            'process_improvements': suggest_workflow_changes(),
            'tool_recommendations': recommend_productivity_tools(),
            'skill_development': identify_learning_opportunities(),
            'architectural_enhancements': propose_tech_improvements()
        }
```

### 7. 高度な報告フォーマットとダッシュボード

#### エグゼクティブサマリー（ステークホルダー向け）
```
🎯 プロジェクト状況: 順調 (67%完了、スケジュール通り)
💰 予算効率: 103% (想定より3%効率良好)
🚀 主要成果: ユーザー認証システム本日完了、次はコア機能開発
⚠️ 注意事項: 外部API統合で軽微な遅延可能性、対策済み
📈 改善実績: 開発効率15%向上、バグ率30%削減
```

#### 技術詳細レポート（開発者向け）
```yaml
✅ タスク完了: "ユーザー認証APIエンドポイント群実装"
  
技術成果物:
  - 変更: 247行 (src/api/auth/*)
  - 新規API: 5エンドポイント
  - テスト: 45件追加 (カバレッジ92%)
  - ドキュメント: OpenAPI仕様更新

品質検証:
  - ✅ セキュリティ: JWT実装、OWASP準拠
  - ✅ パフォーマンス: レスポンス時間<100ms
  - ✅ 可用性: エラーハンドリング完備
  - ✅ 拡張性: マイクロサービス対応

影響分析:
  🔓 即時解除: [
    "フロントエンド認証状態管理" [frontend-architect],
    "認証フロー統合テスト" [agile-test-strategist],
    "本番環境認証設定" [aws-infrastructure-architect]
  ]
  
  📋 関連タスク更新: [
    "ユーザープロファイル管理" → 優先度UP,
    "権限ベースルーティング" → 依存解消,
    "SSO統合準備" → 開始可能
  ]

自動引き継ぎ:
  → frontend-architect: "認証状態管理実装"
    コンテキスト: JWT構造、エラーパターン、APIエンドポイント仕様
    推定工数: 3時間、完了予定: 今日 17:00
```

#### パフォーマンス分析レポート
```yaml
📊 今回タスクの分析:
  効率性:
    - 実施時間: 2.5時間 (見積り3時間より30分短縮)
    - 集中度: 87% (平均85%を上回る)
    - 中断回数: 1回 (平均3回より大幅改善)

  品質:
    - 一発合格率: 95% (レビュー指摘軽微)
    - テストカバレッジ: 92% (目標80%を大幅超過)
    - 技術負債: 追加なし

  協業:
    - 他エージェント待機解消: 3件
    - 知識共有: 2件
    - ブロッカー報告: 0件

  知識ベース活用:
    - 参照した知識: "パターン1: JWT認証実装"
    - 有用性: ★★★★☆ (実装時間30%短縮)
    - 改善点: リフレッシュトークンの例があるとより良い

💡 学習・改善ポイント:
  成功要因:
    - 事前のAPI設計レビューが効果的
    - テスト駆動開発により品質向上
    - 依存関係の早期特定で並列化実現
    - 知識ベースのJWTパターンが役立った

  次回への提案:
    - 類似タスクの見積り: 2.5時間に調整
    - セキュリティレビューを開発初期に組み込み
    - フロントエンドとのAPI仕様事前合意を強化
    - JWTパターンにリフレッシュトークン例を追加
```

## エラーケースと高度な対応

### 品質ゲート不合格時の対応
```yaml
❌ 品質ゲート失敗: テストカバレッジ不足 (67% < 80%)
🔧 自動対応:
  1. タスクステータス: completed → testing_required
  2. 責任エージェント: agile-test-strategist に自動アサイン
  3. 優先度: 高 (ブロッカー解消のため)
  4. 期限: 明日12:00 (依存タスクスケジュール考慮)

💡 推奨アクション:
  - 重要なビジネスロジックのユニットテスト追加
  - エッジケースの統合テスト作成
  - モックデータの充実化
```

### 依存関係循環検出時
```yaml
⚠️ 依存関係循環検出:
  ループ: TaskA → TaskB → TaskC → TaskA
  
🤖 AI提案の解決策:
  1. タスク分割: TaskBを2つに分割して循環を切断
  2. インターフェース定義: 仮のAPI契約を先行定義
  3. 段階的実装: MVP版を先行リリース

👥 協議必要:
  影響エージェント: [backend-tdd-architect, frontend-architect]
  推奨会議: 明日9:00、30分、オンライン
```

### クリティカルパス遅延リスク
```yaml
🚨 クリティカルパス遅延アラート:
  影響: プロジェクト全体が2日遅延の可能性
  
⚡ 緊急対応プラン:
  1. リソース再配置: 他タスクからの人員シフト
  2. スコープ調整: 非必須機能の次フェーズ移行
  3. 並列化強化: 依存関係の仮実装による前倒し
  4. 外部支援: 専門コンサルタントの投入検討

📞 即座に通知:
  - プロジェクトマネージャー
  - ステークホルダー
  - 全エージェント
```

## 高度な実行後フロー

### 完了後の自動化シーケンス
```yaml
1. 品質保証 (0-5分):
   - 全品質ゲートの最終確認
   - 統合テスト実行
   - セキュリティスキャン
   - パフォーマンステスト

2. 知識化・文書化 (5-10分):
   - 実装知識の構造化
   - ドキュメント自動更新
   - ベストプラクティス抽出
   - 学習ポイント記録

3. 依存関係管理 (10-15分):
   - 依存タスクの自動解除
   - 次タスクの優先順位更新
   - エージェント間の負荷調整
   - リソース最適化

4. 次フェーズ準備 (15-20分):
   - 最適次タスクの選択・割り当て（知識パターン適合度考慮）
   - 作業環境の自動セットアップ
   - コンテキスト情報の移行
   - 成功条件の定義

5. 継続改善 (20-25分):
   - パフォーマンスメトリクス更新
   - 改善提案の生成
   - プロセス最適化の実施
   - 次回への学習記録
   - 知識ベース・Try項目の更新
```

### Epic/Sprint完了時の包括評価
```yaml
Epic完了時の自動実行:
  - /retrospective --comprehensive
  - /metrics-analysis --full-scope
  - /knowledge-consolidation
  - /next-sprint-planning --ai-optimized
  - /stakeholder-report --executive-summary
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
│   │   ├── progress-tracking.md     ← /start-tasks 出力
│   │   └── execution-logs.md        ← /start-tasks 出力
│   ├── validation/
│   │   ├── quality-reports.md       ← このコマンドの出力
│   │   └── completion-status.md     ← このコマンドの出力
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
1. Epic IDとepic-nameを既存の execution/progress-tracking.md から取得
2. 同じ `agent-docs/EPIC-{ID}-{epic-name}/validation/` ディレクトリを使用
3. 2つのファイルにタスク完了情報を構造化出力：
   - quality-reports.md: 品質検証結果、テストカバレッジ、コード品質
   - completion-status.md: タスク完了ステータス、依存関係解除、引き継ぎ
4. execution/ と breakdown/ ディレクトリとの相互参照リンクを含める
5. 各タスク完了時に継続的に両ファイルを更新
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
  source_execution: "execution/"
  
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
  execution:
    progress_tracking: "execution/progress-tracking.md"
    execution_logs: "execution/execution-logs.md"
  analysis:
    retrospective_data: "analysis/retrospective-data.md"
    metrics: "analysis/metrics.md"
  knowledge:
    learnings: "knowledge/learnings.md"
    best_practices: "knowledge/best-practices.md"
  
completion_context:
  task_source: "breakdown/tasks.md で定義された7エージェントタスク"
  design_validation: "design/ ディレクトリの設計仕様との適合性"
  execution_tracking: "execution/progress-tracking.md の進捗追跡と連動"
  continuous_validation: "各タスク完了時に継続的に更新される検証ログ"
```

### Incremental Logging Strategy
```yaml
log_structure:
  format: "追記形式（新しい完了タスクが上部に追加）"
  entry_template:
    - 完了日時
    - タスクID・名称
    - 担当エージェント
    - 品質検証結果
    - 依存関係解除状況
    - パフォーマンスメトリクス
    - 学習ポイント
    - 次タスク推奨
  
cross_references:
    - requirements-breakdown.md の該当タスク
    - technical-design.md の実装仕様
    - execution-dashboard.md の進捗更新
```

## Workflow Integration & Handoffs

### FROM Previous Commands
- **`/start-tasks`**: Task execution with progress tracking
- **Agent roles**: Established validation patterns from `/break-down`

### TO Next Commands
- **`/retrospective`**: Performance data and improvement insights
- **`/knowledge-share`**: Learning capture and best practices
- **Continuous**: Next task selection and automatic progression

### Output Integration
- **TodoWrite Updates**: Automatic status transitions and dependency unlocking
- **Performance Analytics**: Efficiency metrics and bottleneck identification
- **Quality Reports**: Comprehensive validation results and recommendations

### 重要：出力ファイル作成指示
**実行時には必ず以下を実行してください：**
1. 既存の execution/progress-tracking.md からEpic ID と名前を特定
2. 同じ Epic ディレクトリの `validation/` フォルダを作成（なければ）
3. 2つのファイルにタスク完了情報を構造化記録：
   - quality-reports.md: 品質検証結果、テスト結果、コード品質評価
   - completion-status.md: タスク完了状況、依存関係解除、引き継ぎ情報
4. execution/progress-tracking.md の進捗状況と同期更新
5. breakdown/dependencies.md の依存関係情報を参照して解除状況を記録
6. 各ファイル先頭にメタデータとcross-reference情報を含める（初回のみ）
7. **知識ベース更新**:
   - agent-docs/knowledge.md への使用統計更新
   - agent-docs/try.md への進捗反映
   - 新たな学習の直接記録