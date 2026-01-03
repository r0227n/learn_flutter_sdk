---
theme: default
background: https://source.unsplash.com/collection/94734566/1920x1080
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Flutter SDK Learning Repository
  
  Learning Flutter SDK v1.16.3 through component analysis
drawings:
  persist: false
transition: slide-left
title: Flutter SDK Learning
mdc: true
---

# Flutter SDK Learning

Learning Flutter SDK v1.16.3 through component analysis

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

---

# Welcome to Flutter SDK Learning

このリポジトリについて

- 📚 **Flutter SDK v1.16.3** - Flutter フレームワークのソースコードを学習
- 🎨 **Component Analysis** - コンポーネント単位でコードを理解
- 📝 **Documentation** - Markdown形式での詳細な説明
- 🎬 **Slidev Presentations** - インタラクティブなスライドで学習

<br>
<br>

詳細は [GitHub Repository](https://github.com/r0227n/learn_flutter_sdk) をご覧ください。

---

# Getting Started

このリポジトリの使い方

1. **TODO リストの確認**
   - `todo.md` で学習したいトピックを確認

2. **自動生成されたドキュメント**
   - `docs/` ディレクトリ内のMarkdownファイルを参照

3. **スライドで学習**
   - GitHub Pages でホストされたスライドを閲覧

4. **週次更新**
   - GitHub Actions が毎週自動的に新しいコンテンツを生成

---

# Repository Structure

```
learn_flutter_sdk/
├── todo.md              # 学習タスクリスト
├── docs/                # 生成されたMarkdownドキュメント
├── slides/              # Slidevスライド
│   └── index.md        # メインスライド
├── .github/
│   └── workflows/      # GitHub Actionsワークフロー
└── package.json        # Node.js依存関係
```

---

# Next Steps

今後の学習予定

- Widget システムの理解
- Rendering パイプラインの解析
- State 管理の仕組み
- Build プロセスの詳細
- Layout システムの学習

<br>

詳細は `todo.md` をご覧ください。

---
layout: center
class: text-center
---

# Learn More

[Documentation](https://github.com/r0227n/learn_flutter_sdk) · [GitHub](https://github.com/r0227n/learn_flutter_sdk) · [Flutter](https://github.com/flutter/flutter)
