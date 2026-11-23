---
name: try-layeris
description: Use when someone wants to start with Layeris, try it without signing in, or continue its three-step AI search sample. Layerisの初回体験やサンプルの続きに使う。
---

# Layerisをサンプルで試す / Try the Layeris sample

Start at step 1 and show the result immediately. A request for a specific step can open it directly. If the user says “続ける” or “next,” show the next step in this chat. Reply in the user's language, using the matching copy and links below. If the language is unclear, use Japanese.

Each step uses the same fictional site, `workspace.example`. Label every response 「架空データのサンプル」 or “Fictional sample.” Use only the evidence below. The sample needs no Layeris login, site URL, question, MCP calls, or web lookups. Show one step at a time and end with the named next action. The sample can be revisited at any time.

## 1. 回答と引用 / Answers and citations

- 質問「プラン変更はいつ反映されますか？」／ “When does a plan change take effect?”
- ChatGPTの例「管理画面から変更できます。」／ ChatGPT example: “You can change your plan in the dashboard.”
- Geminiの例「変更方法は確認できますが、適用時期は分かりません。」／ Gemini example: “The site explains how to change plans, but gives no effective date.”
- 両方の引用先は `workspace.example/pricing`。公開ページには変更手続きが書かれているが、適用日はない。／ Both cite `workspace.example/pricing`, which explains the procedure and omits the effective date.
- 次は「改善案を見る」／ Next: “Show the suggested edit.”

## 2. ページ診断と改善案 / Diagnosis and suggested edit

- 料金ページの原文「プランは管理画面から変更できます。」／ Original: “You can change your plan in the dashboard.”
- 調べる箇所は料金ページの「プラン変更」。手続きの直後に適用日があると、顧客はいつ変わるかをその場で確認できる。／ Add the effective date to the pricing page’s plan-change section so customers can find the timing next to the instructions.
- 架空の契約条件を使った文案「プラン変更は次回の請求日から適用されます。」／ Sample edit for this fictional policy: “Plan changes take effect on your next billing date.”
- 次は「再観測の差分を見る」／ Next: “Show the follow-up comparison.”

## 3. 再観測の差分 / Follow-up comparison

- 同じ質問で比較する。架空の変更前は2回答とも適用日の記載なし。架空の変更後は2回答とも「次回の請求日」と答え、更新した `workspace.example/pricing` を引用。／ For the same question, neither of the two fictional before answers gave an effective date. Both fictional follow-up answers say “next billing date” and cite the updated `workspace.example/pricing`.
- 最後に [Freeで自社サイトを設定](https://layeris.net/ja/mcp/workspace) または [Set up your site on Free](https://layeris.net/en/mcp/workspace) のうち、利用者の言語に合うリンクを表示する。サイト登録と履歴保存にはLayerisアカウントを使う。実データの観測はアカウントで利用可能な場合に実行できる。／ End with the Free setup link in the user's language. A Layeris account saves the site and history. Live observations are available according to the account's access.
- 料金を聞かれたときは [料金プラン](https://layeris.net/ja/pricing) または [Pricing](https://layeris.net/en/pricing) を案内する。／ Link to pricing when the user asks about paid plans.

If the user asks to set up their own site earlier, provide the Free link then. For account data or live work, hand off to `ai-search-review` once the user chooses to connect their Layeris account.
