# Security Policy

WhiteDragon-software takes the security of its projects seriously. This document explains which versions receive fixes, how to report a vulnerability, and what is in scope.

## Supported Versions

Our projects are deployed directly from the `main` branch and do not maintain separate release branches. Only the latest code on `main` receives security fixes. If you run a fork or a pinned older commit, pull regularly to stay patched.

| Version                | Supported |
| ---------------------- | --------- |
| `main` (latest)        | ✅        |
| Older commits and forks | ❌        |

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public issues, discussions, or pull requests.**

Use one of these private channels:

1. **GitHub private vulnerability reporting** (preferred): open the **Security** tab of the affected repository and choose **Report a vulnerability**.
2. **Email:** info@whitedragon.software, with a subject starting with `[SECURITY]`.

Please include as much of the following as you can:

- the affected project and commit or version;
- a description of the vulnerability and its impact;
- steps to reproduce, or a proof of concept;
- any suggested fix or mitigation.

### What to expect

- **Acknowledgement** within 5 business days.
- **Assessment and a status update** within 14 days of acknowledgement, including whether we consider the report valid.
- **A fix or mitigation** as soon as reasonably possible, depending on severity and complexity.
- **Credit** in the fix notes if you want it. Tell us how you would like to be named, or that you prefer to stay anonymous.

These are targets, not guarantees; this is a small, volunteer-run organization. Please allow a reasonable period for a fix to be released and deployed before any public disclosure, and we will keep you informed.

## Scope

This policy covers all repositories in the WhiteDragon-software organization. Notes on the main projects:

| Project | Things we especially want to hear about |
| ------- | --------------------------------------- |
| `relay` | Ways to bypass intended restrictions, server-side request forgery against internal or private addresses, header or cookie leakage between proxied origins, cache poisoning, injected-script escapes. |
| `webcore` | Cross-site scripting through rendered chat content or search results, injection in the D1 data layer, leakage of API keys (for example search provider keys), bypass of the daily neuron budget guardrail. |
| `whitedragon-authenticator` | Anything that exposes stored TOTP secrets or the account data blob, authentication bypass of the password gate, weaknesses in the PIN lock or backup encryption. |
| `whitedragon-forum` | XSS or HTML injection through forum content, token leakage, OAuth flow weaknesses, and CI/CD workflow compromise. This repository also has its own `SECURITY.md`, which takes precedence for that project. |
| `daybreak` | Escapes from per-tab browsing contexts, abuse of the `daybreak://` protocol or internal pages, unsafe exposure of Electron or Node.js APIs to web content. |
| Website and license documentation | Script injection or content tampering. |

## Known Limitations Are Documented

Some projects are intentionally minimal and document their limitations in their README. For example:

- `relay` is a general-purpose forwarding proxy; anyone with the Worker's URL can route traffic through it unless the operator adds an allow-list and rate limiting.
- `webcore` has no authentication; anyone with the Worker's URL can use it and read its conversations unless the operator puts it behind access control.
- `whitedragon-authenticator` uses a single shared password with no built-in rate limiting.

Reports that only restate a documented limitation, without showing a way to defeat a protection the project claims to provide, are generally treated as hardening suggestions rather than vulnerabilities. We still welcome them as regular issues or pull requests.

## Out of Scope

- Vulnerabilities in GitHub, Cloudflare, Electron, Node.js, or other third-party platforms themselves; please report those to the respective vendors.
- Issues that require an already-compromised device, browser, or account.
- Denial-of-service through volume alone, and rate limiting on third-party APIs.
- Social engineering of maintainers or users.
- Reports from automated scanners without a demonstrated, realistic impact.
- Findings in a deployment that the operator has misconfigured contrary to the project's README.

## Safe Harbor

If you make a good-faith effort to follow this policy, avoid privacy violations, avoid degrading service for others, and do not access or modify data that is not yours, we will treat your research as authorized and will not pursue action against you. Please test only against your own deployments or local copies, never against other people's instances.

## Operators

If you deploy these projects yourself, you are responsible for securing your deployment: protect secrets with Cloudflare secrets (never commit them), restrict access to anything that should not be public, and keep your copy up to date.
