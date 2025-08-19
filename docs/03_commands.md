# Codex CLI コマンド集（統合版）

> 日本語で書いてください（このフォルダー外は見ないでください）

## 概要
- 目的: `docs/agents` 配下の資料（開始コマンド/起動オプション/ヘルプ参照）と `docs/help.txt` の要点を本資料へ統合し、参照先を一本化する。
- 対象/前提: Windows 11 + Bash（Git Bash/WSL 等）、Codex CLI。CLI 表示は日本語。

## 手順
1. ヘルプ表示
```sh
codex --help
```
期待結果/確認: 終了コード0。サブコマンドとオプション一覧が表示される。

2. バージョン表示
```sh
codex --version
```
期待結果/確認: 終了コード0。バージョン番号が表示される。

3. 対話モード起動
```sh
codex
```
期待結果/確認: 対話的なプロンプトが表示され入力を受け付ける。`Ctrl+C` で終了できる。

## サブコマンド（要約）
- `exec`: 非インタラクティブに Codex を実行（短縮: `e`）
- `login` / `logout`: 認証の管理と削除
- `mcp`: 実験的。MCP サーバーとして実行
- `proto`: 標準出力でプロトコルストリームを実行（短縮: `p`）
- `completion`: シェル補完スクリプトを生成
- `debug`: 内部デバッグ用
- `apply`: 生成した差分を `git apply` として適用（短縮: `a`）
- `help`: ヘルプ表示

## 起動オプション（要約）
- `-c, --config <キー=値>`: 一時上書き設定（例: `-c model="o3"`）。ドット区切りでネスト指定可。
- `-i, --image <ファイル>`: 現在のプロンプトに画像を添付（複数可）。
- `-m, --model <モデル>`: 使用モデル名を指定。
- `--oss`: ローカルの Ollama サーバーを使用（`-c model_provider=oss` 相当）。
- `-p, --profile <プロファイル名>`: `config.toml` 内の設定プロファイルを使用。
- `-s, --sandbox <モード>`: コマンド実行のサンドボックス
  - `read-only` / `workspace-write` / `danger-full-access`（危険）
- `-a, --ask-for-approval <ポリシー>`: 承認ポリシー
  - `untrusted` / `on-failure` / `on-request` / `never`
- `--full-auto`: `--ask-for-approval on-failure` + `--sandbox workspace-write` の簡易指定。
- `--dangerously-bypass-approvals-and-sandbox`: すべての確認とサンドボックスを無効化（非常に危険）。
- `-C, --cd <ディレクトリ>`: 作業ディレクトリを指定。
- `-h, --help` / `-V, --version`: ヘルプ/バージョン表示。

## 期待結果の確認方法
- コマンド実行後の終了コードを確認: `echo $?`（0 なら成功）。
- 出力は日本語で表示されること。

## 補足/注意
- 端末の文字コードで表示が乱れる場合がある。UTF-8 を推奨。
- 機密はプレースホルダーで表記する。

## 既知の制約
- 一部環境で日本語の記号が文字化けする可能性がある。

## 更新履歴
- 2025-08-19: agents 配下の資料を統合。

