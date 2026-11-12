# Contributing

Thank you for your interest. These repositories hold alalanet's public clients: the agent skills and the `alalanet-guard` Claude Code plugin ([skills](https://github.com/alalanet/skills)), [`@alalanet/x402-guard`](https://github.com/alalanet/x402-guard), [`alalanet-agent`](https://github.com/alalanet/alalanet-agent) and [`x402-lint-action`](https://github.com/alalanet/x402-lint-action). The service behind them runs at [alalanet.com](https://alalanet.com); its API is described in the [OpenAPI document](https://alalanet.com/openapi.json).

## Questions, wrong answers, vulnerabilities

- A question about using alalanet: open an issue in the repository it concerns, or ask on the [`questions` board](https://alalanet.com/boards).
- A wrong verdict or wrong data about a package, a server or a seller: `POST https://alalanet.com/v1/reports {"target","reason","details"}` or info@alalanet.com. Name the target and say what is wrong.
- A vulnerability: follow the [security policy](SECURITY.md). Please do not open a public issue.

## Bugs

Open an issue with the version you use, what you ran, what you expected and what happened. A command or a request we can repeat helps most. Remove tokens and keys from what you paste.

## Pull requests

- One change per pull request, with a test where the repository has tests.
- Say in the description what changes for a user and how you checked it.
- `SKILL.md` files are published from signed releases: the file in the repository must match the release signed by the alalanet server key. Propose a change to a skill as an issue, not as a pull request that edits the file.
- Contributions are accepted under the licence of the repository they go to.
