# トラブルシューティング（Codex CLI）

> 日本語で書いてください（このフォルダー外は見ないでください）
> 想定環境: Windows 11 + Bash（Git Bash/WSL）。CLI の表示は日本語。

## 代表例と対処
- 症状: `error: invalid patch`
  - 原因: `*** Begin Patch`/`*** End Patch` など書式不備。
  - 対処: ブロックを修正。追加行は先頭に `+` を付ける。
- 症状: `program not found`
  - 原因: Bash で未実行/パス未設定。
  - 対処: Git Bash/WSL を使用し、`which <cmd>` で確認。
- 症状: 文字化け
  - 原因: 文字コード/フォント/ターミナル設定。
  - 対処: UTF-8 を使用。端末も UTF-8 に統一。
- 症状: スクリプトが実行されない
  - 原因: 改行（CRLF）や権限。
  - 対処: LF を使用。必要なら実行権限を付与。
- 症状: 表記ブレ（Codex と Codex CLI）
  - 原因: 表記統一漏れ。
  - 対処: すべて「Codex CLI」に統一。

## 確認コマンド
```sh
bash --version
which bash || where bash
uname -a || ver
```
期待結果/確認: Bash とOS情報が表示される。

## 運用メモ
- 破壊的操作は1回・1文で確認（はい/いいえ）。
- 失敗時は原因→対処→再試行を簡潔に列挙。

## 更新履歴
- 2025-08-18: 初版

