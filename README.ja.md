# Codex・Claude Codeで使うLayeris

[English](README.md)

ChatGPT・Geminiが自社をどう紹介し、どのページを引用しているかをLayerisで確認できます。ページ診断が使えるプランでは、登録済みページの改善案を根拠とともに確認できます。

両プラグインは共通MCPの `https://layeris.net/api/mcp` に接続します。CodexとClaude Codeで同じLayerisアカウントを選んで接続すると、登録サイト、観測履歴、利用枠を共有できます。

## 登録なしで試す

### Codex

Layerisマーケットプレイスを追加すると、プラグイン一覧からLayerisを選べます。ターミナルからもインストールできます。

```sh
codex plugin marketplace add oranque-llc/layeris-plugins
codex plugin add layeris-service@layeris
```

新しいチャットで「Layerisの初回体験をサンプルで始める」を選びます。

### Claude Code

```sh
claude plugin marketplace add oranque-llc/layeris-plugins
claude plugin install layeris-service@layeris
```

新しいセッションで `/layeris-service:try-layeris` を実行します。

回答と引用、ページの改善案、再観測の差分を、同じ架空のサイトで3ステップ体験できます。

## 自社サイトで始める

[観測設定](https://layeris.net/ja/mcp/workspace)からFreeアカウントを作成し、自社サイトを登録できます。Codexでは `codex mcp login layeris-service`、Claude Codeでは `/mcp` からLayerisへの接続を許可します。

## チャットで試す

- 「Layerisで登録サイトと利用枠の残数を教えて」
- 「Layerisで自社サイトに関するChatGPT・Geminiの保存済み回答と引用URLを見せて」
- 「Layerisでこの登録済みページを診断し、修正箇所とその根拠を示して」

同梱のSkillが、これらの依頼で使うツールを案内します。新規観測と診断の利用可否は、アカウントの機能と利用枠に応じます。

[Layeris公式サイト](https://layeris.net/ja/) · [プライバシーポリシー](https://oranque.jp/ja/legal/privacy)
