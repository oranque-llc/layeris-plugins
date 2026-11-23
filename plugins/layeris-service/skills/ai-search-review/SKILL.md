---
name: ai-search-review
description: Layerisのサービス用MCPでChatGPT・Geminiの観測回答と引用URLを確認し、登録済みページの診断結果を読み解く。
---

# Layerisの観測とページ診断

- Layerisのサービス用MCPに接続済みの場合に使う。接続や認証が必要な場合は、その状態を伝えて処理を止める。
- 観測の確認には `list_observations` を使う。質問・対象サービス・取得日時を示し、本文の欠測と引用0件を区別する。
- ページ診断には登録済みURLを指定する。残数は `get_usage` で確認し、`diagnose_url` には診断ごとに新しい依頼IDを付ける。通信エラーから再試行する場合は同じIDを使う。
- 枠を使い切った場合は現在の利用状況を示し、MCPが返したプラン情報ページがあれば案内する。
- Freeで `get_usage` が `trial` を返す場合、観測の残り送信数は `trial.sends.remaining`、期限は `trial.expiresAt` を使う。本文が取得できない送信も枠に含まれる。新規観測を停止している場合も、保存済みの履歴は `list_observations` で確認できる。
- 診断の原文と引用URLを根拠として提示する。ページの公開や修正は利用者が承認した手順で進める。
