---
name: phantomoperator
description: Use PhantomOperator for authorized public-exposure, metadata, breach-indicator, privacy, and Base/EVM wallet-hygiene checks through its public API.
category: basics
---

# PhantomOperator

Use this skill only for URLs, identities, emails, and wallets that the requester owns or is authorized to assess. Never submit passwords, seed phrases, private keys, or API credentials.

## Discovery

- Base URL: `https://freysaai.freysa.dev`
- Free metadata preview: `POST /preview/metadata-audit` with `{ "url": "https://example.com" }`
- OpenAPI: `https://freysaai.freysa.dev/openapi.json`
- Quickstart: `https://freysaai.freysa.dev/quickstart`
- MCP: `POST https://freysaai.freysa.dev/mcp`
- x402 discovery: `https://freysaai.freysa.dev/.well-known/x402`

## Payment

The primary paid rail is native USDC on Base through x402. Call `POST /skills/<operation>` first; an unpaid valid request returns HTTP 402 with the exact payment requirement. Use an x402-compatible client to sign that requirement and retry the same request. Do not replace the protocol credential with a plain token transfer.

## Useful operations

- `metadata-audit` — public HTTP headers, HTML metadata/comments, and third-party tracker review ($0.05 Base USDC).
- `breach-check` — email breach indicators; optional password k-anonymity range check ($0.10).
- `threat-scan` — authorized public-web exposure scan ($0.10).
- `opsec-score` — structured exposure score and recommendations ($0.25).
- `wallet-opsec-audit` — public Base/EVM wallet hygiene review ($0.50).

Read `/openapi.json` before a paid call for canonical schemas and prices. Treat results as potentially incomplete or stale signals, not proof of compromise.
