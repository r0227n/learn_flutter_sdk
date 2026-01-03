# learn_flutter_sdk

[![Deploy to GitHub Pages](https://github.com/r0227n/learn_flutter_sdk/actions/workflows/deploy-pages.yml/badge.svg)](https://github.com/r0227n/learn_flutter_sdk/actions/workflows/deploy-pages.yml)
[![Weekly Automation](https://github.com/r0227n/learn_flutter_sdk/actions/workflows/weekly-automation.yml/badge.svg)](https://github.com/r0227n/learn_flutter_sdk/actions/workflows/weekly-automation.yml)

Flutter/Flutter SDK (v1.16.3) の学習リポジトリ

## 📖 概要

このリポジトリは、Flutter SDK のソースコードを体系的に学習するためのプロジェクトです。DeepWiki MCP と Slidev を活用し、コンポーネント単位でプログラムの内容を整理し、スライドや Markdown で説明することで、Flutter のコード実装を深く理解することを目指しています。

## 🎯 特徴

- **自動化された学習プロセス**: 毎週 GitHub Actions が起動し、TODO リストから1つのタスクを処理
- **包括的なドキュメント**: Markdown 形式で各ファイルの説明と依存関係を記述
- **インタラクティブなスライド**: Slidev を使用した視覚的な学習コンテンツ
- **GitHub Pages ホスティング**: スライドをオンラインで閲覧可能
- **PR プレビュー**: プルリクエストごとに専用のプレビューページを生成

## 🚀 セットアップ

### 必要な環境

- Node.js 20.x 以上
- npm または yarn

### インストール

```bash
# リポジトリのクローン
git clone https://github.com/r0227n/learn_flutter_sdk.git
cd learn_flutter_sdk

# 依存関係のインストール
npm install
```

### ローカルでの実行

```bash
# Slidev 開発サーバーの起動
npm run dev

# ビルド
npm run build
```

## 📁 ディレクトリ構造

```
learn_flutter_sdk/
├── .github/
│   └── workflows/           # GitHub Actions ワークフロー
│       ├── weekly-automation.yml  # 週次自動化
│       └── deploy-pages.yml       # GitHub Pages デプロイ
├── docs/                    # 生成された Markdown ドキュメント
├── slides/                  # Slidev スライド
│   └── index.md            # メインスライドファイル
├── todo.md                  # 学習タスクリスト
├── package.json            # Node.js 依存関係
└── README.md               # このファイル
```

## 🔄 運用フロー

### 週次自動化

1. **毎週日曜日 00:00 UTC (月曜日 09:00 JST)** に GitHub Actions が自動起動
2. `todo.md` から未完了の TODO を1つ取得
3. [Claude Code Action](https://github.com/anthropics/claude-code-action) を使用して:
   - Flutter SDK の指定ファイルを解析
   - 各ファイルの説明と依存関係を記載した Markdown を生成
   - Slidev スライドを作成/更新
4. 自動的にプルリクエストを作成
5. PR がマージされると GitHub Pages に自動デプロイ

### パス分岐

- **Main ブランチ**: `https://r0227n.github.io/learn_flutter_sdk/`
- **PR プレビュー**: `https://r0227n.github.io/learn_flutter_sdk/pr-{番号}/`

各プルリクエストには、変更内容をプレビューできる専用ページが自動生成されます。

## 📝 TODO リストの管理

`todo.md` ファイルで学習したいトピックを管理します:

```markdown
## TODO

- [ ] Flutter SDKの基本構造を理解する
- [ ] Flutterのレンダリングパイプラインを学ぶ
- [ ] Flutterの状態管理の仕組み
```

TODO が完了すると、自動的に「完了したTODO」セクションに移動されます。

## 🛠️ 手動実行

GitHub Actions は手動でもトリガーできます:

1. GitHub の「Actions」タブに移動
2. 「Weekly Flutter Learning Automation」を選択
3. 「Run workflow」ボタンをクリック

## 🔐 必要なシークレット

GitHub Actions を実行するには、以下のシークレットを設定する必要があります:

- `ANTHROPIC_API_KEY`: Anthropic API キー（Claude Code Action 用）

Settings > Secrets and variables > Actions から設定してください。

## 📚 学習リソース

- [Flutter SDK v1.16.3](https://github.com/flutter/flutter/tree/v1.16.3)
- [Slidev Documentation](https://sli.dev/)
- [Claude Code Action](https://github.com/anthropics/claude-code-action)

## 🤝 コントリビューション

学習したいトピックの提案は大歓迎です！

1. `todo.md` に新しい TODO を追加
2. プルリクエストを作成
3. レビュー後にマージ

## 📄 ライセンス

このプロジェクトは学習目的で作成されています。

## 🔗 リンク

- [GitHub Pages](https://r0227n.github.io/learn_flutter_sdk/)
- [Issues](https://github.com/r0227n/learn_flutter_sdk/issues)
- [Pull Requests](https://github.com/r0227n/learn_flutter_sdk/pulls)
