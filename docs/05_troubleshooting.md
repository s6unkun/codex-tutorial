# トラブルシュート（Codex CLI）

> 日本語で書いてください（このフォルダー外は見ないでください）
> 想定環境: Windows 11 + Bash（Git Bash/WSL）。CLI の表示は日本語。

## 代表的な問題と対処
- 症状: `error: invalid patch`（パッチ形式エラー）
  - 原因: `*** Begin Patch`/`*** End Patch` や見出し行の書式誤り。
  - 対処: 見出しを正しく記述し、追加行は `+` を先頭に付与。
- 症状: `program not found`（コマンド未検出）
  - 原因: Bash で実行していない/パス未設定。
  - 対処: Git Bash/WSL を利用し、`which <cmd>` で存在確認。
- 症状: 文字化け
  - 原因: 文字コード/フォント/端末設定。
  - 対処: UTF-8 を使用。端末の文字コードを UTF-8 に統一。
- 症状: 改行差異によるスクリプト失敗
  - 原因: CRLF と LF の混在。
  - 対処: 改行は LF を推奨。`.gitattributes` で正規化を検討。
- 症状: 表記ゆれ（Codex と Codex CLI が混在）
  - 原因: 執筆時の不統一。
  - 対処: 「Codex CLI」に統一。検索置換で修正。

## 確認用コマンド
```sh
bash --version
which bash || where bash
uname -a || ver
```
期待結果/確認: Bash/環境が正しく検出される。

## 連絡/記録
- 発生事象は 1 行要約 + 最小ログで記録。
- 再現手順があれば箇条書きで付記。

## 更新履歴
- 2025-08-18: 初版
