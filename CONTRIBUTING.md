# Contributing to TextConvo

Thank you for helping improve the TextConvo developer experience. Every public repository in this account is maintained by the TextConvo engineering team and is open to community contributions.

## Ways to contribute

| Contribution | Where |
| --- | --- |
| Fix or improve an example | [textconvo-api-examples](https://github.com/textconvo/textconvo-api-examples) |
| Report an inaccuracy in the OpenAPI spec | [textconvo-openapi](https://github.com/textconvo/textconvo-openapi) |
| Improve a webhook receiver | [textconvo-webhooks](https://github.com/textconvo/textconvo-webhooks) |
| Add a demo app or improve one | [textconvo-sample-apps](https://github.com/textconvo/textconvo-sample-apps) |
| Share a tutorial, video, or project | [awesome-textconvo](https://github.com/textconvo/awesome-textconvo) |
| Report a documentation error | Open an issue on the relevant repository |

Product bugs, billing questions, and account issues are **not** handled on GitHub. Use [textconvo.ai/contact-us](https://textconvo.ai/contact-us).

## What we can accept

We can accept changes that:

- Fix a bug, typo, or broken link in an example, specification, or document.
- Add an example in a language or framework we already support.
- Improve clarity, error handling, retry behaviour, or security practice in sample code.
- Add tests or linting that make examples easier to verify.

We cannot accept changes that:

- Add or infer platform implementation, orchestration logic, or infrastructure details.
- Duplicate reference documentation that belongs on [textconvo.ai/docs](https://textconvo.ai/docs).
- Introduce dependencies without a clear, stated reason.
- Include real credentials, API keys, phone numbers, customer data, or personal data of any kind.

## Before you open a pull request

1. **Open an issue first** for anything larger than a typo, so we can agree on the approach before you invest time.
2. **Keep it focused.** One logical change per pull request.
3. **Use placeholders.** Never commit a real key. Use `YOUR_API_KEY`, `YOUR_SOURCE_KEY`, and `+15035551234`.
4. **Verify it runs.** Examples must execute against the documented API surface described at [textconvo.ai/docs](https://textconvo.ai/docs).

## Development workflow

1. Fork the repository and create a branch from `main`.
2. Name the branch by intent: `fix/python-retry-backoff`, `feat/go-webhook-receiver`, `docs/openapi-error-codes`.
3. Commit using [Conventional Commits](https://www.conventionalcommits.org/): `feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`, `ci:`.
4. Push your branch and open a pull request against `main`.
5. Fill in the pull request template and link the issue it resolves.

Example commit message:

    fix(python): honour Retry-After header on 429 responses

## Review and merge

- A code owner reviews every pull request. We aim for a first response within two business days.
- Discussion happens in the pull request. Force-pushes are fine before review starts, less welcome after.
- We squash-merge. Your commit history does not need to be perfect, but your pull request title does &mdash; it becomes the changelog entry.

## Style

- Prefer clarity over cleverness. These are teaching examples first and utilities second.
- Handle errors explicitly. Show the reader what a failed request looks like.
- Read configuration from environment variables, never from literals in source.
- Comment the intent, not the syntax.

## Security

Do not report vulnerabilities in issues or pull requests. Follow [SECURITY.md](SECURITY.md).

## Code of conduct

Participation is governed by our [Code of Conduct](CODE_OF_CONDUCT.md).

## Licensing

By submitting a contribution you confirm that you wrote it or have the right to submit it, and you agree that it is licensed under the same license as the repository you are contributing to.
