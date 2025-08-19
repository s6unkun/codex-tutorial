# Codex CLI インストールと初期設定

> 日本語で書いてください（このフォルダー外は見ないでください）
> 想定環境: Windows 11 + Bash（Git Bash/WSL）。CLI の表示は日本語。

## 概要
- 目的: Codex CLI の導入と初期確認を最短で実施する。
- 対象/前提: Windows 11 で Bash が使えること（Git Bash/WSL）。Git 利用可。

## 手順
1. 前提確認
```sh
bash --version
git --version
node --version
npm --version
```
期待結果/確認: 各バージョンが表示される（エラーなし）。

2. Codex CLI をインストール（npm）
```sh
npm install -g @openai/codex
npx @openai/codex --version
```
期待結果/確認: Codex CLI のバージョンが表示される。

3. リポジトリ取得（必要時）
```sh
git clone <REPO_URL>
cd <REPO_DIR>
```
期待結果/確認: カレントに README.md, AGENTS.md, docs/ が存在する。

4. 改行・文字コードの確認
- 改行: LF を推奨（Bash 実行のため）。
- 文字コード: UTF-8 を推奨（CLI 表示の乱れを防ぐ）。

5. 初期確認
```sh
ls -la
```
期待結果/確認: `.git/`, `README.md`, `AGENTS.md`, `docs/` が表示される。

## 補足
- 表記は「Codex CLI」で統一する。
- 作成・編集・レビューは CLI が担当。ユーザーは最終確認のみ。

## 更新履歴
- 2025-08-18: 初版

