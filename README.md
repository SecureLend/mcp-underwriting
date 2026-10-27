# SecureLend Underwriting (MCP)

Public listing wrapper for SecureLend's **remote** underwriting MCP.

This repository does **not** run the server. The hosted Streamable HTTP endpoint is:

**https://mcp.securelend.ai/v1/lender/mcp**

## What it does

Open a credit file, chase missing documents, screen sanctions when configured, and draft a cited credit memo. A person makes the credit decision. No tool approves a loan or moves money.

## Connect

| | |
|---|---|
| MCP URL | `https://mcp.securelend.ai/v1/lender/mcp` |
| Docs | https://docs.securelend.ai/mcp/lender |
| Homepage | https://securelend.ai |
| Privacy | https://securelend.ai/legal/privacy |
| Terms | https://securelend.ai/legal/terms |
| Support | sales@securelend.ai |
| Trust / SOC 2 | https://securelend.trustshare.com/home |

`initialize`, `notifications/initialized`, `ping`, and `tools/list` work without a token. `tools/call` requires OAuth (`authorization_code` + PKCE S256, scope `lender`).

## Tools (11)

resolve_listed_company, read_listed_company, open_case, read_case, walk_credit_file, score_case_against_pack, chase_missing_documents, screen_sanctions, draft_memo_from_file, start_underwriting_package, read_package

## Official registry metadata

See [`server.json`](./server.json) (namespace `ai.securelend/lender` after domain verification).

## Not this product

- **Market / placement MCP** (consumer comparison): https://mcp.securelend.ai/mcp — sibling wrapper [mcp-market](https://github.com/SecureLend/mcp-market)
- Do **not** use `agents.securelend.ai` (shut down)

## License

MIT
