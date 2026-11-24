# Contributing

These rules apply to every VCSWBV repository. A repository's own CONTRIBUTING.md or README adds its setup, commands and checks.

## Branches and titles

Branch from `main` and keep each pull request to one purpose. Name the branch after its type and ticket, for example
`feat/VF-1234-short-description`.

Commits and pull request titles follow [Conventional Commits](https://www.conventionalcommits.org/). Add the Jira ticket as the scope when there is one:

```text
feat(VF-1234): add a CSV export
fix(VF-1234,VF-1235): keep the filter after paging
docs: clarify the setup steps
```

The accepted ticket prefixes are VF, DH and DO. A repository's own CONTRIBUTING.md says which one it uses. Valid types are `feat`, `fix`, `chore`, `refactor`, `docs`, `test`, `ci`,
`perf`, `style`, `build` and `revert`. A breaking change adds `!` before the colon.

Pull requests are squash merged. The title and body become the commit on `main`, so fill in the pull request template and keep the body short and
factual.

## Review

1. Open a draft pull request early and mark it ready when CI is green. Never merge past red CI.
2. Let the automated reviewers finish their rounds. Address or answer each comment, and resolve every conversation.
3. Move the Jira issue to Code Review and request a human reviewer yourself, preferably someone who knows the area. Code owners are requested
   automatically only for sensitive paths, such as deployment and security workflows, so most pull requests have no automatic reviewer.
4. A colleague who did not write the change reviews it substantively and approves it. Automated review is advisory and never counts as that
   approval. Aim to review on the same working day.

Reviewers check correctness and tests, fit with existing patterns, security and data protection, readability, migrations and backwards
compatibility, and the ticket's acceptance criteria. Work is only done when it meets the Definition of Done, which the pull request template
summarises.

## Data and secrets

Use synthetic or factory data in code, tests and local development. Never commit `.env` files, keys, tokens, production data or personal data. If a
secret or personal data is committed, follow [SECURITY.md](SECURITY.md).

## Updates

Dependency and action updates arrive as Renovate pull requests. Pin exact versions and full action SHAs.
