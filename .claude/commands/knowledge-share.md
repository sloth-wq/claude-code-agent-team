# Knowledge Sharing & Learning Capture

**CORE PURPOSE**: Systematically capture, structure, and share domain expertise gained during Epic development for team learning and knowledge base evolution.

**UNIQUE SCOPE**: Learning extraction, knowledge structuring, cross-agent insights, and continuous knowledge base improvement.

## Usage
```
/knowledge-share [--domain=technical|business|process] [--format=structured|freeform]
```

## Prerequisites
- Significant Epic or Sprint completion with lessons learned
- Agent experiences from full workflow execution
- Clear insights or discoveries worth sharing
- Access to implementation artifacts and outcomes

## Outputs
- Structured knowledge entries in searchable format
- Cross-domain learning recommendations
- Knowledge base updates and improvements
- Team learning facilitation materials
- Future project guidance and best practices
- **OUTPUT FILES**: 
  - Unified Knowledge Base: `agent-docs/knowledge.md` (統合知識ベースへの追加)
  - Try Items: `agent-docs/try.md` (新規改善提案の追加)
  - シンプルな2ファイル構造で最大効率を実現

## 知識共有プロンプト

## Knowledge Capture Framework

**COMPREHENSIVE 7-AGENT APPROACH**: All agents contribute knowledge while leveraging established roles from `/break-down`

You are systematically capturing and sharing valuable insights gained during Epic development to facilitate comprehensive team learning and knowledge base evolution across all 7 collaborative agents.

### 使命（全7エージェント参加による知識創造）
1. 専門領域での発見と学習を構造化して全エージェントと共有
2. 7エージェント間の知識クロスポリネーションの促進
3. 継続的な知識ベース進化への貢献（全エージェントの視点統合）
4. 実践的で再利用可能な知識の創造（Multi-agent協業パターン含む）
5. エージェント間のナレッジギャップ特定と解消
6. Cross-functional学習機会の最大化
7. 統合的問題解決アプローチの文書化

### 知識共有フレームワーク

#### 【STEP 1: 知識の特定と分類】
以下のカテゴリから該当するものを選択し、知識を整理してください：

**A. プロダクト情報・ドメイン知識**
- ビジネスルールと制約
- ユーザー行動パターン
- 市場要求と競合分析
- プロダクトロードマップインサイト

**B. ビジネスロジック理解・パターン**
- ビジネスプロセスフロー
- 意思決定ルール
- 例外処理パターン
- データ変換ロジック

**C. コードパターン・アーキテクチャ洞察**
- 設計パターン適用例
- リファクタリング戦略
- 技術的負債の対処法
- アーキテクチャ決定記録

**D. 技術的発見・ベストプラクティス**
- ツール活用方法
- パフォーマンス最適化技法
- セキュリティ実装パターン
- 開発効率化手法

**E. 統合課題・解決策**
- システム間連携パターン
- データ整合性確保手法
- API設計原則
- 依存関係管理

**F. パフォーマンス最適化発見**
- ボトルネック特定方法
- 最適化手法と効果測定
- リソース使用効率化
- レスポンス時間改善

**G. セキュリティ考慮事項・実装**
- 脆弱性対策パターン
- 認証・認可実装
- データ保護手法
- セキュリティテスト方法

**H. エージェント間協業パターン**
- 効果的な協業手法とコミュニケーションパターン
- クロスファンクショナル問題解決アプローチ
- 依存関係管理と同期ポイント最適化
- 知識移転と引き継ぎベストプラクティス

**I. Multi-agent意思決定プロセス**
- 複数視点での要求分析手法
- エージェント間の合意形成プロセス
- 技術的トレードオフの評価方法
- 統合的品質保証アプローチ

#### 【STEP 2: 知識テンプレート記入】

```markdown
## 知識エントリー: {知識タイトル}

### 基本情報
- **カテゴリ**: {A-I から選択}
- **優先度**: {高/中/低}
- **適用範囲**: {特定機能/全システム/プロセス全般/Multi-agent協業}
- **発見日**: {YYYY-MM-DD}
- **貢献エージェント**: {あなたの役割}
- **関連エージェント**: {協業・学習に関与した他のエージェント}
- **協業パターン**: {単独/ペア/チーム/全エージェント}

### 背景・コンテキスト
{なぜこの知識が重要か、どのような状況で発見されたか}

### 知識内容
{具体的な発見、手法、パターン、解決策}

### 実装例・コード例
```{language}
{実際のコード例や設定例}
```

### 影響・効果
- **技術的影響**: {システムへの影響}
- **ビジネス影響**: {ビジネス価値への影響}
- **チーム影響**: {開発効率やプロセスへの影響}

### 関連知識・依存関係
- **前提知識**: {この知識を理解するために必要な知識}
- **関連エントリー**: {関連する他の知識エントリー}
- **競合・代替案**: {他の解決策や手法}

### 検証・更新情報
- **検証方法**: {この知識の有効性を確認する方法}
- **更新履歴**: {知識の進化や修正履歴}
- **次のアクション**: {さらなる調査や改善点}

### タグ・キーワード
{検索性を高めるためのタグ}
```

#### 【STEP 3: 全7エージェント学習促進】

全7エージェントとの知識共有のために、以下を含めてください：

1. **全エージェントへの知識価値提示**
   - backend-tdd-architect: "この知識がAPI設計・テスト戦略に与える影響"
   - frontend-architect: "UI/UXコンポーネント設計への適用可能性"  
   - agile-test-strategist: "品質保証・テスト戦略への組み込み方法"
   - aws-infrastructure-architect: "インフラ設計・運用への影響"
   - database-design-specialist: "データモデル・パフォーマンスへの効果"
   - product-code-comprehension-expert: "アーキテクチャ・技術負債への影響"
   - agile-product-owner: "ビジネス価値・ユーザー価値への貢献"

2. **Multi-agent協業提案**
   - "この知識を活用した7エージェント協業の最適パターン"
   - "統合的解決策開発のための具体的協業プロセス"
   - "エージェント間知識移転の効率化方法"

3. **知識ギャップ分析（全エージェント視点）**
   - "各エージェントの専門領域からの補完が必要な部分"
   - "Cross-functional視点で不足している情報"
   - "統合的理解のために必要な他エージェントの知見"

#### 【STEP 4: 全7エージェント知識品質保証】

全エージェントの品質基準を統合した以下の基準を適用：

**必須チェックリスト（Multi-agent品質保証）:**
- [ ] 知識の再現可能性が確保されている（agile-test-strategist基準）
- [ ] 具体的な実装例が含まれている（backend-tdd + frontend基準）
- [ ] ビジネス価値との関連が明確（agile-product-owner基準）
- [ ] 全7エージェントが理解・活用可能な形式
- [ ] 検索・発見しやすいタグ付け（product-code-comprehension基準）
- [ ] 継続的更新の仕組みが含まれている
- [ ] 運用・インフラ観点での実現可能性（aws-infrastructure基準）
- [ ] データ整合性・パフォーマンス考慮（database-design基準）
- [ ] Cross-agent協業パターンが明確化されている

**品質向上のための追加質問（全7エージェント視点）:**
1. この知識は他のプロジェクトでも活用できますか？（再利用性）
2. 新しいチームメンバーや他エージェントが理解できる説明になっていますか？（理解性）
3. 知識の適用条件や制約は明確ですか？（適用性）
4. 失敗例や注意点も含まれていますか？（安全性）
5. 定量的な効果測定方法は提示されていますか？（測定可能性）
6. 全7エージェントの専門視点が考慮されていますか？（包括性）
7. エージェント間協業での活用方法が明確ですか？（協業性）
8. 知識の進化・更新プロセスが定義されていますか？（継続性）

### 出力形式

最終的な知識共有は以下の構造で出力してください：

```markdown
# 知識ベースエントリー

## エグゼクティブサマリー
{この知識の価値と適用可能性を3行で要約}

## 詳細知識内容
{上記テンプレートに従った完全な知識記録}

## クロスエージェント推奨事項
{他エージェントとの協力可能性と次のステップ}

## 知識進化ロードマップ
{この知識の将来的な発展方向性}
```

### 継続的改善メカニズム

1. **定期レビュー**: 月次で知識エントリーの有効性確認
2. **使用状況追跡**: 知識の活用頻度と効果測定
3. **フィードバック収集**: 他エージェントからの改善提案
4. **知識統合**: 関連知識の統合と重複解消
5. **新技術適応**: 技術進歩に合わせた知識更新

### 成功指標

- **知識品質**: 
  - 再利用率 (目標: >60%)
  - 問題解決効果 (時間短縮率)
  - 有用性評価平均 (★★★★☆以上)
- **知識活用**:
  - 参照回数/エントリ
  - タスク実行中の活用率
  - 知識ギャップの削減
- **継続的改善**:
  - 知識ベース成長率
  - 古い知識の削除率
  - Try項目の成功率

### 重要：出力ファイル作成指示（簡素化）
**実行時には必ず以下を実行してください：**
1. Epic実行中の知識や学習を特定
2. `agent-docs/knowledge.md` への直接更新：
   - 新規知識エントリの追加
   - 使用統計と有用性評価の更新
   - 実際の活用例と改善提案の記録
3. `agent-docs/try.md` への直接更新：
   - 新規改善提案の追加
   - 既存Try項目の進捗更新
4. シンプルな2ファイル構造での管理
5. 複雑なディレクトリ操作の排除

## Workflow Integration & Handoffs

### FROM Previous Commands
- **`/retrospective`**: Performance insights and improvement opportunities
- **`/task-done`**: Individual learning points and knowledge usage feedback
- **Entire workflow**: Cross-functional collaboration learnings

### TO Future Development
- **Next `/break-down`**: Enhanced processes based on knowledge base insights
- **Knowledge base**: Continuously evolving single-file repository
- **Try items**: Actionable improvement proposals with tracking

### Output Integration
- **Unified Knowledge Base**: Single source of truth in `agent-docs/knowledge.md`
- **Try Items Backlog**: Improvement proposals in `agent-docs/try.md`
- **Simplified Structure**: 2-file system without complex directory hierarchies
- **Usage Tracking**: Comprehensive metrics on knowledge effectiveness
- **Continuous Improvement**: Self-optimizing through usage evaluation