# alalanet

**Check before you install, connect or pay.** alalanet is a free trust layer for AI agents. You need no account and no API key, and every answer is signed into a public transparency log.

| Before the agent… | Ask alalanet | Answer |
|---|---|---|
| installs an npm/PyPI package, a GitHub repo, a skill or an MCP server | `install_check` | allow / hold / block: known malicious (OSV), typosquats of official MCP servers, names that don't exist, install scripts, maintainer changes |
| connects to an MCP server or pays an x402 endpoint | `check_service` | live status, real price and payTo vs the listing, uptime, tool-set changes, open Trust Score |
| signs an x402 payment | `preflight_payment` | allow / hold / block, bound to the payment hash |
| retries after a timeout | `payment_status` | settled / pending / not settled, so it never pays twice |
| needs evidence after a bad paid call | `dispute_evidence` | signed evidence pack (x402 dispute shape) |

## Use it

- **Remote MCP server:** `https://alalanet.com/mcp` (22 tools, no auth)
- **Claude Code plugin:** `/plugin install alalanet-guard --marketplace alalanet/skills`. It checks every `npm i`, `npx`, `pip`, `uvx`, `claude mcp add` and `skills add` before it runs.
- **Agent skill:** `npx skills add alalanet/skills`
- **HTTP API:** [OpenAPI](https://alalanet.com/openapi.json) · [llms.txt](https://alalanet.com/llms.txt) · [skill.md](https://alalanet.com/skill.md)

## Repositories

- [skills](https://github.com/alalanet/skills): the signed agent skills and the `alalanet-guard` Claude Code plugin
- [x402-guard](https://github.com/alalanet/x402-guard): a fetch wrapper that asks alalanet before an x402 payment is signed, with budgets ([npm](https://www.npmjs.com/package/@alalanet/x402-guard))
- [alalanet-agent](https://github.com/alalanet/alalanet-agent): a local signer and MCP server for agent passports, receipts, purchase reports, mail and memory
- [x402-lint-action](https://github.com/alalanet/x402-lint-action): a GitHub Action that lints your x402 endpoints the way buyers' agents see them

[alalanet.com](https://alalanet.com) · [Transparency log](https://alalanet.com/transparency) · [Privacy](https://alalanet.com/privacy) · info@alalanet.com
