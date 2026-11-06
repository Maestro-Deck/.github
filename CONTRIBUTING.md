# Contributing to Maestro Deck

Thanks for contributing! This guide applies to every repository in the organization, unless a repository has its own `CONTRIBUTING.md`.

## Golden rules

1. **Never push directly to `main`.** Everything goes through a Pull Request (PR).
2. **One PR = one topic.** Keep it small and readable, reviewable in under 15 minutes.
3. **No secrets in the code**: no API keys, passwords, tokens or `.env` files. If it happens, tell an Owner right away: the secret must be revoked, deleting the commit is not enough.
4. **A PR can't be merged without at least one approval** from another member.
5. **CI must be green** before merging.

## Workflow

1. Get the latest changes:
   ```bash
   git checkout main && git pull
   ```
2. Create a branch from `main`:
   ```bash
   git checkout -b feat/short-name
   ```
3. Work and commit often (see conventions below).
4. Push your branch and open a PR against `main`.
5. Answer review comments, fix, push.
6. Once approved and CI is green, the PR is merged with **squash** (one clean commit on `main`).
7. Delete your branch.

## Branch names

`type/short-description`, lowercase, with hyphens.

| Type | Use |
|------|-----|
| `feat/` | new feature |
| `fix/` | bug fix |
| `docs/` | documentation |
| `refactor/` | refactoring without behavior change |
| `test/` | adding or fixing tests |
| `chore/` | tooling, dependencies, config |

Examples: `feat/device-farm-scheduler`, `fix/login-timeout`.

## Commit messages

[Conventional Commits](https://www.conventionalcommits.org/) format:

```
type(optional scope): short summary in the imperative

Optional body: why this change, not only what.
```

Examples:
- `feat(cli): add the test launch command`
- `fix(api): fix session token expiry`
- `docs: clarify macOS installation`

## Pull Requests

- Fill in the PR template (it appears automatically).
- Link the related issue (`Closes #123`).
- Add screenshots if the UI changes.
- If your PR isn't ready, open it as a **draft**.
- Review your own diff before asking for a review.

## Reviews

- Be precise and kind: critique the code, not the person.
- Separate what blocks from what is a suggestion (prefix details with `nit:`).
- Reply within a reasonable time, ideally under 48 hours.

## Code quality

- Follow the repository's formatter and linter (they run in CI).
- Add or update tests for what you change.
- Don't leave commented-out code or debug `console.log` / `print` statements.
- Document anything that isn't obvious.

## Need help?

Open an issue or ask in the team channel. It's better to ask early than to fix a big PR late.
