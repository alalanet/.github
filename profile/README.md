# alalanet

**Check before your agent installs, connects or pays.** alalanet is a free trust layer for AI agents: no account, no API key. Verdicts, live checks and status changes are signed and written to a public transparency log.

| Before the agent… | Ask alalanet | Answer |
|---|---|---|
| installs an npm/PyPI package, a GitHub repo, a skill, an IDE extension or an MCP server | `install_check` | allow / hold / block: known malicious (OSV), typosquats of official MCP servers, names that don't exist, install scripts, maintainer changes |
| opens a repository someone sent it | `check_repo_config` | allow / hold / block for the agent configuration the repository carries: MCP servers, hooks, permissions, editor tasks, instruction files |
| connects to an MCP server or pays an x402 endpoint | `check_service` | live status, real price and payTo vs the listing, uptime, tool-set changes, open Trust Score |
| uses the tools an MCP server gave it | `verify_tools` | whether these are the tools the server serves everyone, and what changed since they were approved |
| signs an x402 payment | `preflight_payment` | allow / hold / block, bound to the payment hash |
| retries after a timeout | `payment_status` | settled / pending / not settled, so it never pays twice |
| has paid | `report_purchase` | the outcome (delivered, partial, wrong content, not delivered), verified on chain and signed into the log |
| needs a service for a task | `find_service` | working x402 endpoints and MCP servers, ranked by the open Trust Score |

## Use it

- **Remote MCP server:** `https://alalanet.com/mcp` — the eight checks above, no auth
- **Install and MCP-server checks only, no payment tools:** `https://alalanet.com/mcp/guard` — seven read-only tools, with `connect_check` (will this MCP server connect from my client?), `check_artifact` and `get_attestation`
- **Every tool** (also agent identities, receipts, mail, boards, evidence packs, watches and plans): `https://alalanet.com/mcp/full` — 25 tools
- **Claude Code plugin:** `/plugin install alalanet-guard --marketplace alalanet/skills`. A hook checks every install command before it runs (`npm i`, `npx`, `pnpm`/`yarn`/`bun add`, `pip`/`uv` install, `uvx`, `pipx`, `claude mcp add`, `codex mcp add`, `skills add`, `clawhub install`, IDE extension installs): block denies, hold asks.
- **Agent skills:** `npx skills add alalanet/skills`
- **HTTP API:** [OpenAPI](https://alalanet.com/openapi.json) · [llms.txt](https://alalanet.com/llms.txt) · [skill.md](https://alalanet.com/skill.md)
- **Block feed for admins and caches:** [`/v1/blocklist`](https://alalanet.com/v1/blocklist)

## Repositories

- [skills](https://github.com/alalanet/skills): the signed agent skills and the `alalanet-guard` Claude Code plugin
- [x402-guard](https://github.com/alalanet/x402-guard): a fetch wrapper that asks alalanet before an x402 payment is signed, with budgets ([npm](https://www.npmjs.com/package/@alalanet/x402-guard))
- [alalanet-agent](https://github.com/alalanet/alalanet-agent): a local signer and MCP server for agent passports, receipts, purchase reports, mail and memory
- [x402-lint-action](https://github.com/alalanet/x402-lint-action): a GitHub Action that lints your x402 endpoints the way buyers' agents see them

[alalanet.com](https://alalanet.com) · [Transparency log](https://alalanet.com/transparency) · [Privacy](https://alalanet.com/privacy) · info@alalanet.com
