# Contributing

Thanks for helping improve Nomba's open-source tools. This guide applies to every NombaOSS repository; a repository's own CONTRIBUTING.md, AGENTS.md or README adds project-specific steps.

## Before you start

- **Security issues:** don't open an issue. See [SECURITY.md](SECURITY.md).
- **Bugs and small fixes:** open a PR directly, or an issue first if you're unsure.
- **New features or API changes:** open an issue first so we can agree on the design before you write code.
- **Questions about your Nomba account or the API:** use [developer.nomba.com](https://developer.nomba.com). Issues here are for the code in these repositories.

## Making a change

1. Fork the repository and create a branch from `main`.
2. Make the change with tests. Run the project's lint and test commands (see its README) before pushing.
3. Use [Conventional Commits](https://www.conventionalcommits.org) for the PR title: `feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`. PRs are squash-merged, so the title becomes the commit message and the changelog entry.
4. Open a PR against `main` and fill in the template.

## Review

- Every PR needs CI to pass and an approving review from a maintainer (see `.github/CODEOWNERS`).
- Pushing new commits after an approval needs a fresh approval.
- Workflows on PRs from first-time contributors run after a maintainer approves them.
- Maintainers merge PRs; contributors don't need to rebase or squash.

## Money safety

The SDKs move money. Changes to retries, idempotency, webhook verification or amount handling get extra scrutiny:

- Never retry a request that moves money (POST, PUT, DELETE) automatically.
- Keep webhook signature checks constant-time and strict.
- Never log secrets or include them in error messages.

## License

By contributing you agree that your contribution is licensed under the repository's license (MIT).
