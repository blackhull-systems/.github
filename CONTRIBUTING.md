# Contributing to Blackhull's public repositories

Thank you for taking the time. These repositories are small on purpose: an AgentKit action provider, runnable x402
examples and the published methodology. Every change to them is reviewed and signed by Blackhull's owner before it
reaches `main`.

## Reporting a problem

- **A bug in the code or an example:** open an issue with the bug report form. Include what you ran, what you expected
  and what happened, with the full output.
- **A finding you think is wrong** (a token or service check result): use the free dispute process at
  <https://blackhullsystems.com/disputes>, not an issue. Every dispute and its outcome is public.
- **A security issue:** do not open an issue. Follow [SECURITY.md](SECURITY.md).

## Proposing a change

1. Open an issue first for anything larger than a small fix, so we can agree on the approach before you write it.
2. Keep the pull request to one change, with a test that fails without it.
3. Run the same checks CI runs before you push:
   - **agentkit:** `npm ci && npm run check` (format, lint, types, tests with coverage, package checks).
   - **x402-examples:** `npm ci && npm run format:check && npm run lint` at the root, `npm ci && npm test` in each
     Node example, and `pip install -r python/requirements-dev.txt && ruff check . && (cd python && pytest -q)` for Python.
4. No test may spend money or need a funded wallet. Use the free sample (`?sample=1`), or a fresh, never-funded key
   with a spend cap below the price, as the existing tests do.
5. Commits on `main` must be signed, and CI must be green.

By contributing you agree that your contribution is licensed under the repository's license (Apache-2.0), and to
follow our [Code of Conduct](CODE_OF_CONDUCT.md).
