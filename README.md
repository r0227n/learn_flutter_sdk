# learn_flutter_sdk
flutter/flutter の学習リポジトリ

## 開発環境のセットアップ

### mise と bun のインストール

このプロジェクトでは、bun のバージョン管理に [mise](https://mise.jdx.dev/) を使用しています。

#### 1. mise のインストール

```bash
curl https://mise.run | sh
```

または、他のインストール方法については [mise公式ドキュメント](https://mise.jdx.dev/getting-started.html) を参照してください。

#### 2. mise の有効化

シェルの設定ファイル（`~/.bashrc`, `~/.zshrc` など）に以下を追加してください：

```bash
eval "$(mise activate bash)"  # bash の場合
# または
eval "$(mise activate zsh)"   # zsh の場合
```

#### 3. bun のインストール

プロジェクトディレクトリで以下を実行すると、`.mise.toml` に指定されたバージョンの bun が自動的にインストールされます：

```bash
mise install
```

#### 4. 確認

```bash
bun --version
```

### mise について

mise は複数の言語やツールのバージョンを管理するツールマネージャーです。このプロジェクトでは以下のファイルで bun のバージョンを管理しています：

- `.mise.toml`: mise の設定ファイル（推奨）
- `.tool-versions`: asdf 互換の設定ファイル
