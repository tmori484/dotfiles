# dotfiles

[chezmoi](https://www.chezmoi.io/) で管理している個人用 dotfiles。

## 管理しているファイル

| ソース | 展開先 | 内容 |
| --- | --- | --- |
| `dot_claude/rules/cross-platform.md` | `~/.claude/rules/cross-platform.md` | Claude Code の全 OS 共通ルール（uv の利用、`.context/` の扱い、利用可能な CLI ツール） |

## セットアップ

新しいマシンでは、chezmoi をインストールしてから次を実行する。

```sh
chezmoi init --apply tmori484/dotfiles
```

## 日常の操作

```sh
# ホームのファイルを編集して反映
chezmoi edit ~/.claude/rules/cross-platform.md
chezmoi apply

# 新しいファイルを管理対象に追加
chezmoi add ~/.some/config

# 適用前に差分を確認
chezmoi diff

# リモートの変更を取り込んで反映
chezmoi update
```

ソースディレクトリ（`~/.local/share/chezmoi`）へは `chezmoi cd` で移動できる。変更はそこで通常どおり git commit / push する。
