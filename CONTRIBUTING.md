# Contributing to WhiteDragon-software

Thank you for your interest in contributing to WhiteDragon-software.

We build minimal software for the open web, on Cloudflare Workers and Node.js: few dependencies, no build step, and small enough to read in full. Contributions are welcome when they improve a project while keeping it simple, clear, and true to its purpose.

## Before Contributing

Please read the repository's:

- `README.md`, including its *How it works* and *Known limitations* sections;
- `LICENSE`;
- any project-specific documentation.

For substantial changes (new features, new dependencies, changes to architecture or behavior), open an issue or discussion first so we can agree on direction before you invest time. Small fixes, documentation improvements, and obvious bug fixes can go straight to a pull request.

## Our Principles

### Keep it minimal

Prefer simple solutions over unnecessary frameworks, dependencies, abstractions, or infrastructure. If a single file is enough, keep it a single file. Do not introduce a build step to a project that does not have one.

### Keep it clear

Code should be readable, maintainable, and consistent with the existing project. Someone should still be able to read the whole project in one sitting.

### Keep it focused

A pull request should address one coherent change. Avoid unrelated refactoring or formatting changes.

### Respect the project

Each repository may have different goals, architecture, and licensing. Follow the conventions and requirements of the project you are contributing to.

## Pull Requests

A pull request should:

- describe clearly what was changed and why;
- include appropriate testing or verification (see below);
- update documentation, including the README, when behavior changes;
- avoid unnecessary dependencies or complexity;
- contain no secrets, credentials, API keys, or unrelated changes.

Maintainers may request changes, defer a proposal, or decline contributions that do not fit a project's purpose or maintenance requirements. A declined pull request is not a judgment of you; it usually means the change does not fit the project's scope.

### Testing and verification

Several projects (for example `relay` and `webcore`) ship a numbered testing checklist in their README. If your change touches a layer covered by the checklist, work through the relevant steps and say in the pull request which ones you ran and what you saw. For projects with automated tests (for example `whitedragon-forum`), run the test suite before submitting.

If you cannot test something, say so in the pull request.

## Dependencies

New dependencies need a clear justification. Before adding one, consider whether the need can reasonably be met with existing project code or platform capabilities (Cloudflare Workers APIs, Node.js built-ins, browser APIs).

## Licensing

Repositories in this organization are licensed individually. Check the `LICENSE` file of the repository you are contributing to; do not assume that one project's license applies to another.

By submitting a contribution, you agree that it may be distributed under that repository's license.

Do not submit code, assets, documentation, or other material that you do not have the right to contribute. This includes code copied from other projects whose licenses are incompatible with the repository's license.

## Security

Do not report security vulnerabilities through public issues or pull requests. Follow [SECURITY.md](SECURITY.md) instead.

## Getting Help

If you are unsure where to start or have a question about a project, see [SUPPORT.md](SUPPORT.md).

## Code of Conduct

All contributors and maintainers are expected to follow [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).

---

> **Prefer the smallest clear solution that solves the real problem.**

Thank you for contributing to WhiteDragon-software.
