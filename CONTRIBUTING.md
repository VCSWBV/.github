# Contributing

These rules apply to every VCSWBV repository. A repository's own CONTRIBUTING.md or README adds its setup, commands and checks.

## Branches and titles

Branch from `main` and keep each pull request to one purpose. Name the branch after its type and ticket, for example
`feat/VF-1234-short-description`.

Commits and pull request titles follow [Conventional Commits](https://www.conventionalcommits.org/), with the Jira ticket as the scope:

```text
feat(VF-1234): add the LKV forecast export
fix(DH-567): keep the sync status for invitees without activity
```

Use VF tickets, or DH tickets in the repositories the Datahub team owns. Valid types are `feat`, `fix`, `chore`, `refactor`, `docs`, `test`, `ci`,
`perf`, `style`, `build` and `revert`. A breaking change adds `!` before the colon.

Pull requests are squash merged. The title and body become the commit on `main`, so fill in the pull request template and keep the body short and
factual.

## Review

1. Run the repository's checks locally before you push. CI must pass before a merge.
2. Let the automated reviewers finish their rounds. Address or answer each comment and resolve the conversation.
3. Then request a human reviewer yourself. Code owners are requested automatically only for sensitive paths, such as deployment and security
   workflows, so most pull requests have no automatic reviewer.
4. A colleague who did not write the change reviews it substantively and approves it. Automated review is advisory and never counts as that
   approval.

## Data and secrets

Use synthetic or factory data in code, tests and local development. Never commit `.env` files, keys, tokens, production data or personal data. If a
secret or personal data is committed, follow [SECURITY.md](SECURITY.md).

## Updates

Dependency and action updates arrive as Renovate pull requests. Pin exact versions and full action SHAs.
