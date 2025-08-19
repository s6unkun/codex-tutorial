# Codex CLI インストールと初期設定

> 日本語で書いてください（このフォルダー外は見ないでください）
> 想定環境: Windows 11 + Bash（Git Bash/WSL）。CLI の表示は日本語。

## 概要
- 目的: Codex CLI を使い、.md 資料を再現可能に作成できる状態にする。
- 対象/前提: Windows 11 で Bash が使えること（Git Bash/WSL）。Git が利用可能。

## 手順
1. 環境確認
```sh
bash --version
git --version
node --version
npm --version
```
期待結果/確認: バージョンが表示される（エラーが出ない）。

2. Codex CLI のインストール（npm）
```sh
npm install -g @openai/codex
npx @openai/codex --version
```
期待結果/確認: Codex CLI のバージョンが表示される。

3. リポジトリ取得（未取得の場合）
```sh
git clone <your-repo-url>
cd <your-repo-folder>
```
期待結果/確認: カレントに README.md, AGENTS.md, docs/ が存在する。

4. 改行コード/文字コードの注意
- 改行: LF を推奨（Bash 実行の互換性のため）。
- 文字コード: UTF-8（CLI 表示を日本語に統一）。

5. 動作確認（最小）
```sh
ls -la
```
期待結果/確認: `.git/`, `README.md`, `AGENTS.md`, `docs/` などが一覧に出る。

## 補足
- 表記は「Codex CLI」で統一。
- 作成・編集・レビューは CLI が担当。ユーザーは内容確認のみ。

## 更新履歴
- 2025-08-18: 初版
