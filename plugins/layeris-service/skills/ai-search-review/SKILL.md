---
name: ai-search-review
description: Layerisのサービス用MCPでChatGPT・Geminiの観測回答と引用URLを確認し、登録済みページの診断結果を読み解く。
---

# Layerisの観測とページ診断

- 初回体験や架空データのデモには `try-layeris` を使う。自社サイトの実データを扱うときは、利用者がLayerisのサービス用MCPに接続してからこのSkillを使う。
- 接続が必要な場合はLayerisのアカウント認可を案内する。サンプルは認可前から体験できる。
- 観測の確認には `list_observations` を使う。質問・対象サービス・取得日時を示し、本文の欠測と引用0件を区別する。
- ページ診断には登録済みURLを指定する。残数は `get_usage` で確認し、`diagnose_url` には診断ごとに新しい依頼IDを付ける。通信エラーから再試行する場合は同じIDを使う。
- Freeで `get_usage` が `trial` を返す場合、観測の残り送信数は `trial.sends.remaining`、期限は `trial.expiresAt` を使う。本文が取得できない送信も枠に含まれる。新規観測を停止している場合も、保存済みの履歴は `list_observations` で確認できる。
- 診断の原文と引用URLを根拠として提示する。ページの公開や修正は利用者が承認した手順で進める。

## 契約の確認とProの案内

- プランや残数を聞かれたら `get_usage` の `plan` と利用枠を確認する。Freeの利用枠を使い切った場合や試用期限に達した場合は、該当する理由と現在のプランを伝え、料金ページを案内する。
- Proを申し込みたい利用者には、`get_usage` の `planInformationUrl` を案内する。URLが返らない場合は `try-layeris` にある料金ページを案内する。利用者がMCPに接続したときと同じLayerisアカウントでログインし、Webで決済する。購入受付の状態は購入画面に従う。カード情報の入力はStripe Checkoutで行う。
- 購入後は `get_usage` を再取得して `plan` が `pro` か、月500回答・50診断・3サイトの枠が表示されるかを確認する。CodexとClaude Codeは、同じLayerisアカウントに接続すると契約・残数を共有する。
- 決済後もFreeと表示される場合は、Webの購入結果と接続したLayerisアカウントを確認する。反映待ちの場合は後で `get_usage` を再確認する。再購入は案内しない。
