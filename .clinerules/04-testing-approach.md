# テスト手法

## テスト駆動開発（TDD）

1. **Red**：まず失敗するテストを書く
2. **Green**：テストが通るように最小限の実装をする
3. **Refactor**：コードをリファクタリングして改善する

## テスト構造

- すべてのテストはtestsディレクトリに配置する
- テストファイル名とテスト関数名はtest_で始める
- pytestフレームワークを使用する
- ユニットテスト、統合テスト、エンドツーエンドテストを適切に分ける

## テスト品質

- すべての公開関数とメソッドにはユニットテストを書く
- コードカバレッジは80%以上を目標とする
- 重要なビジネスロジックは100%のカバレッジを目指す
- 外部依存はモックを使用する
- 複数のケースをテストする場合はパラメータ化テストを使用する
