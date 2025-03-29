# Python Boilerplate

Python プロジェクトのボイラープレート（テンプレート）です。devcontainer を使用した開発環境の標準化と、コード品質ツールの設定が含まれています。

## 特徴

- **devcontainer による開発環境の標準化**
  - Python 3.12
  - uv パッケージマネージャー
  - Chromium & 日本語フォントのサポート

- **コード品質ツール**
  - Ruff によるリンティングとフォーマット
  - mypy による静的型チェック
  - pytest によるテスト

- **.clinerules によるコーディングスタイルの定義**
  - AI アシスタント用のルール定義

## セットアップ

このリポジトリは VS Code の devcontainer 機能を使用しています。VS Code と Docker がインストールされていれば、自動的に開発環境がセットアップされます。

1. リポジトリをクローン
   ```bash
   git clone https://github.com/yourusername/python-boilerplate.git
   cd python-boilerplate
   ```

2. VS Code で開く
   ```bash
   code .
   ```

3. VS Code が devcontainer を検出し、「Reopen in Container」を提案するので、それをクリックします。

4. 開発用依存関係をインストール
   ```bash
   uv pip install -e ".[dev]"
   ```

## 使用方法

### 新しいプロジェクトの作成

1. このリポジトリをテンプレートとして使用
2. プロジェクト名や説明を変更（pyproject.toml）
3. 必要な依存関係を追加
   ```bash
   uv add package_name
   ```

### コードスタイル

- コードは Ruff によって自動的にフォーマットされます（保存時）
- mypy による型チェックが強制されます
- テストは pytest で実行します
  ```bash
  pytest
  ```

## ディレクトリ構造

```
python-boilerplate/
├── src/              # メインのソースコード
├── tests/            # テストコード
├── .clinerules/      # Cline AI のルール定義
├── .devcontainer/    # devcontainer の設定
├── .vscode/          # VS Code の設定
├── .gitignore        # Git の除外設定
├── .env.example      # 環境変数の例
├── .python-version   # Python バージョン指定
├── pyproject.toml    # プロジェクト設定
└── README.md         # このファイル
