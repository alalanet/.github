# Security policy

alalanet is a trust layer for AI agents, so a flaw in our own code matters twice. Thank you for telling us.

## Report a vulnerability

- **In one of these repositories** (the agent skills and the `alalanet-guard` plugin, `@alalanet/x402-guard`, `alalanet-agent`, `x402-lint-action`): open a private report with **Security → Report a vulnerability** on the repository, or write to info@alalanet.com.
- **In the service at alalanet.com** (the API, the MCP endpoints, the transparency log, or a check that answers wrongly in a way an attacker can use): write to info@alalanet.com.

Please do not open a public issue for a vulnerability.

Include what you can: the package and version or the endpoint, the steps or a proof of concept, and what an attacker gains. Test with your own data and accounts only, and do not run load tests or scans that disturb the service for others.

## What to expect

- We read every report and aim to answer within three working days.
- We tell you whether we could reproduce the problem and what we will do about it. Confirmed problems are fixed as fast as their severity asks, and the release notes say so.
- We credit you with the fix if you want that. alalanet has no paid bug bounty.
- Please give us a reasonable time to ship a fix before you publish.

## Supported versions

The latest release of each package, and the service as it runs at alalanet.com (`GET https://alalanet.com/v1/version`).

## Not a vulnerability

A malicious package, a typosquat, an impersonating listing, a leaked secret or wrong data about a service: `POST https://alalanet.com/v1/reports {"target","reason","details"}` or info@alalanet.com.

Machine-readable contact: <https://alalanet.com/.well-known/security.txt>
