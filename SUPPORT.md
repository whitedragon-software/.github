# Support

Thanks for using WhiteDragon-software projects. This page explains where to get help.

WhiteDragon-software is a small organization and support is provided on a best-effort basis, with no guaranteed response time. Clear, specific questions get faster and better answers.

## Where to Go

| I want to... | Go here |
| ------------ | ------- |
| Ask a question or get help using a project | [GitHub Discussions](https://github.com/orgs/whitedragon-software/discussions), or the [community forum](https://whitedragon-software.github.io/whitedragon-forum) |
| Report a bug | An issue in the affected repository |
| Suggest a feature | A discussion first; an issue if it is already well-defined |
| Contribute code or documentation | [CONTRIBUTING.md](CONTRIBUTING.md) |
| Report a security vulnerability | [SECURITY.md](SECURITY.md) (**not** a public issue) |
| Report a Code of Conduct violation | [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) |
| Ask about commercial use or licensing | info@whitedragon.software |
| Reach us about anything else | info@whitedragon.software |

Note that the community forum is built on GitHub Discussions, so reading and posting there requires signing in with a GitHub account.

## Before You Ask

1. **Read the README** of the project. Each one documents how it works, how to deploy it, and its known limitations, and several include a testing checklist that helps narrow down where a problem is.
2. **Search existing issues and discussions.** Your question may already be answered.
3. **Check your deployment.** Most of our projects are single-file Cloudflare Workers or small Node.js apps; many problems come from missing bindings (for example the `DB` or `AI` binding for `webcore`, or the KV namespace for `whitedragon-authenticator`), missing secrets, or an outdated copy.

## Reporting a Bug

A good bug report includes:

- the project and the commit or version you are running;
- how you run it (Cloudflare Workers, `wrangler dev`, Electron on which OS, and so on);
- what you did, what you expected, and what happened instead;
- relevant logs or error messages, with **secrets, tokens, and passwords removed**;
- for `relay` and `webcore`, the number of the testing-checklist step that first fails, if applicable.

## What We Can and Cannot Help With

We can help with:

- understanding how a project works and how to deploy it;
- bugs and unexpected behavior in our code;
- documentation gaps.

We generally cannot help with:

- general Cloudflare, Electron, Node.js, or JavaScript questions unrelated to our code;
- custom modifications or forks;
- deployments we cannot see or reproduce;
- using the projects in ways that conflict with their licenses.

## Licensing and Commercial Use

Each repository states its own license. Some projects and licenses in the organization are non-commercial or source-available. If you want to use a project commercially, or are unsure whether your use is allowed, email info@whitedragon.software before you start.

## Staying Up to Date

- Watch the repositories you use on GitHub.
- Follow the organization's writing on [DEV](https://dev.to/whitedragon).
- Visit [whitedragon.software](https://whitedragon.software).

## Please Be Kind

Everyone here is a volunteer or a user trying to get something done. Please follow our [Code of Conduct](CODE_OF_CONDUCT.md) in all support channels.
