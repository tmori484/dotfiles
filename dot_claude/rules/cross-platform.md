# 全OS共通のルール

## Python

Python の実行には必ず uv を使う。

- スクリプトやツールは `uv run` で実行する。`python` / `python3` を直接呼ばない。
- 依存の追加・削除は `uv add` / `uv remove` で行う。`pip install` は使わない。

## `.context/` ディレクトリ

`<PROJECT_ROOT>/.context/` は、人間が AI エージェント向けの参考資料を置く場所。

- 必要に応じて読んでよいが、編集はしない。
- Git で管理しない（`.gitignore` に含まれていなければ追加する）。

## 便利な CLI ツール

以下のツールがインストール済み。標準コマンドより適している場合は積極的に使う（例: grep より `rg`、find より `fd`）。

- 検索・ファイル操作: `rg`, `fd`, `eza`, `bat`, `sd`, `ast-grep`
- データ処理: `jq`, `yq`, `mlr`, `datamash`, `duckdb`, `sqlite3`
- 日付処理: dateutils（`dateadd`, `datediff`, `dateconv` など）
- 開発補助: `delta`（git-delta）, `shellcheck`, `hyperfine`, `tldr`

ほかに必要なツールがあれば提案して。
