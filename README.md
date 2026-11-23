# Layeris for Codex and Claude Code

[日本語](README.ja.md)

Use Layeris to see how ChatGPT and Gemini describe your business, review the pages they cite, and get evidence-backed recommendations for registered pages when diagnosis is available on your plan.

Both plugins connect to the hosted Layeris MCP at `https://layeris.net/api/mcp`. Authorize the same Layeris account in both clients to share registered sites, observations, and usage limits.

## Install in Codex

```sh
codex plugin marketplace add Oranquelui/layeris-plugins
codex plugin add layeris-service@layeris
codex mcp login layeris-service
```

Sign in to Layeris in the browser and authorize the connection. Then start a new Codex session to load the plugin and its skill.

## Install in Claude Code

```sh
claude plugin marketplace add Oranquelui/layeris-plugins
claude plugin install layeris-service@layeris
```

Start a new Claude Code session. Open `/mcp`, select the Layeris server, and complete the browser sign-in and authorization.

## Try it in a chat

- “Use Layeris to show my registered sites and remaining usage.”
- “Use Layeris to show the saved ChatGPT and Gemini answers and cited URLs for my site.”
- “Use Layeris to diagnose this registered page and show the evidence behind each suggested edit.”

The included skill guides the agent through these requests. New observations and diagnoses depend on your account's available features and limits.

[Layeris website](https://layeris.net/en/) · [Privacy policy](https://oranque.jp/en/legal/privacy)
