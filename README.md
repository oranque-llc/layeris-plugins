# Layeris for Codex and Claude Code

[日本語](README.ja.md)

Use Layeris to see how ChatGPT and Gemini describe your business, review the pages they cite, and get evidence-backed recommendations for registered pages when diagnosis is available on your plan.

Both plugins connect to the hosted Layeris MCP at `https://layeris.net/api/mcp`. Authorize the same Layeris account in both clients to share registered sites, observations, and usage limits.

## Try the sample without a Layeris account

### Codex

Add the marketplace to find Layeris in the plugin list, or install it from the terminal.

```sh
codex plugin marketplace add oranque-llc/layeris-plugins
codex plugin add layeris-service@layeris
```

In a new chat, choose “Start the Layeris sample walkthrough.”

### Claude Code

```sh
claude plugin marketplace add oranque-llc/layeris-plugins
claude plugin install layeris-service@layeris
```

In a new session, run `/layeris-service:try-layeris in English`.

Explore answers and citations, a suggested page edit, and a follow-up comparison in three steps using the same fictional site.

## Get started with your own site

Create a Free account and register your site in [Observation settings](https://layeris.net/en/mcp/workspace). Authorize Layeris with `codex mcp login layeris-service` in Codex or `/mcp` in Claude Code.

## Try it in a chat

- “Use Layeris to show my registered sites and remaining usage.”
- “Use Layeris to show the saved ChatGPT and Gemini answers and cited URLs for my site.”
- “Use Layeris to diagnose this registered page and show the evidence behind each suggested edit.”

The included skill guides the agent through these requests. New observations and diagnoses depend on your account's available features and limits.

[Layeris website](https://layeris.net/en/) · [Privacy policy](https://oranque.jp/en/legal/privacy)
