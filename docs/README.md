# Flutter SDK Learning - Documentation

このディレクトリには、Flutter SDK の学習過程で生成されたドキュメントが格納されます。

## ドキュメントの構造

各ドキュメントは以下の構造を持ちます：

### 1. ファイル概要
- ファイルの目的と役割
- Flutter SDK 内での位置づけ

### 2. 主要なクラスと機能
- 重要なクラスの説明
- 主要なメソッドとその役割
- コード例

### 3. 依存関係
- 他のファイルとの関係
- import される主要なモジュール
- 依存関係の図解

### 4. 使用パターン
- 実際の使用例
- ベストプラクティス
- 注意点

## 自動生成について

これらのドキュメントは GitHub Actions により自動生成されます：

1. `todo.md` から学習タスクを取得
2. Claude Code Action を使用してソースコードを解析
3. 包括的なドキュメントを生成
4. Slidev スライドと連携

## ドキュメントの命名規則

ドキュメントファイル名は以下の形式に従います：

```
{component-name}-{topic}.md
```

例：
- `widget-framework-basics.md`
- `rendering-pipeline-overview.md`
- `state-management-deep-dive.md`

## 貢献

ドキュメントの改善提案は Issues または Pull Requests でお願いします。
