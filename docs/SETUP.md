# GitHub Pages セットアップガイド

このガイドでは、リポジトリで GitHub Pages を有効にする手順を説明します。

## 前提条件

- GitHub リポジトリへの管理者アクセス
- Anthropic API キー（週次自動化用）

## 手順

### 1. GitHub Pages の有効化

1. リポジトリの **Settings** タブに移動
2. サイドバーから **Pages** を選択
3. **Source** セクションで:
   - Source: **GitHub Actions** を選択
4. **Save** をクリック

### 2. Secrets の設定

週次自動化ワークフローを実行するには、API キーが必要です：

1. リポジトリの **Settings** > **Secrets and variables** > **Actions** に移動
2. **New repository secret** をクリック
3. 以下のシークレットを追加：
   - Name: `ANTHROPIC_API_KEY`
   - Value: あなたの Anthropic API キー

### 3. Permissions の設定

GitHub Actions が適切に動作するよう、権限を設定します：

1. **Settings** > **Actions** > **General** に移動
2. **Workflow permissions** セクションで:
   - **Read and write permissions** を選択
   - **Allow GitHub Actions to create and approve pull requests** にチェック
3. **Save** をクリック

### 4. 初回デプロイ

ワークフローを手動でトリガーして初回デプロイを実行：

1. **Actions** タブに移動
2. **Deploy to GitHub Pages** ワークフローを選択
3. **Run workflow** > **Run workflow** をクリック
4. ワークフローの完了を待つ（通常 2-3 分）

### 5. デプロイの確認

1. **Settings** > **Pages** に戻る
2. **Your site is live at** の URL を確認
3. URL は通常: `https://r0227n.github.io/learn_flutter_sdk/`
4. リンクをクリックしてサイトを確認

## トラブルシューティング

### デプロイが失敗する

- **Actions** タブでエラーログを確認
- `package.json` の依存関係が正しくインストールされているか確認
- Node.js のバージョンが互換性があるか確認

### ページが表示されない

- GitHub Pages の設定が正しく有効になっているか確認
- デプロイワークフローが正常に完了しているか確認
- ブラウザのキャッシュをクリアして再試行

### 週次自動化が動作しない

- `ANTHROPIC_API_KEY` が正しく設定されているか確認
- API キーが有効で、適切な権限を持っているか確認
- ワークフロー権限が正しく設定されているか確認

## 手動実行

### 週次自動化を手動でトリガー

1. **Actions** タブに移動
2. **Weekly Flutter Learning Automation** を選択
3. **Run workflow** をクリック
4. **Run workflow** ボタンをクリックして確認

### Pages デプロイを手動でトリガー

1. **Actions** タブに移動
2. **Deploy to GitHub Pages** を選択
3. **Run workflow** をクリック
4. **Run workflow** ボタンをクリックして確認

## 次のステップ

セットアップが完了したら：

1. `todo.md` に学習したいトピックを追加
2. 週次自動化を待つか、手動でトリガー
3. 生成されたコンテンツをレビュー
4. GitHub Pages でスライドを確認

## サポート

問題が発生した場合は、GitHub Issues で報告してください：
https://github.com/r0227n/learn_flutter_sdk/issues
