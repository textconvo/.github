<!--
README template for TextConvo public repositories.

How to use it:
  1. Copy this file to README.md in the new repository.
  2. Replace every {{PLACEHOLDER}}.
  3. Delete sections that do not apply. A short honest README beats a long padded one.
  4. Link to textconvo.ai/docs rather than restating reference documentation.
-->

<h1 align="center">{{REPOSITORY_TITLE}}</h1>

<p align="center"><strong>{{ONE_LINE_DESCRIPTION}}</strong></p>

<p align="center">
  <a href="https://textconvo.ai">Website</a> &nbsp;&middot;&nbsp;
  <a href="https://textconvo.ai/docs">Developer Docs</a> &nbsp;&middot;&nbsp;
  <a href="https://textconvo.ai/docs#lead-ingestion-api">API Reference</a> &nbsp;&middot;&nbsp;
  <a href="https://textconvo.ai/blog">Blog</a> &nbsp;&middot;&nbsp;
  <a href="https://textconvo.ai/contact-us">Support</a>
</p>

<p align="center">
  <a href="https://textconvo.ai/docs"><img alt="Docs" src="https://img.shields.io/badge/docs-textconvo.ai%2Fdocs-1f6feb?style=flat-square"></a>
  <a href="LICENSE"><img alt="License" src="https://img.shields.io/badge/license-MIT-2ea043?style=flat-square"></a>
  <img alt="Status" src="https://img.shields.io/badge/status-{{STATUS}}-8957e5?style=flat-square">
  <a href="https://github.com/textconvo/{{REPOSITORY_NAME}}/issues"><img alt="Issues" src="https://img.shields.io/github/issues/textconvo/{{REPOSITORY_NAME}}?style=flat-square"></a>
</p>

---

## What this is

{{TWO_OR_THREE_SENTENCES}} Part of the public developer surface for [TextConvo](https://textconvo.ai), the AI orchestration platform for customer conversations across SMS, RCS, Voice AI, Email, and WhatsApp.

## What this is not

This repository contains no platform implementation, no orchestration logic, and no infrastructure or credentials. Reference documentation lives at [textconvo.ai/docs](https://textconvo.ai/docs) and is not duplicated here.

## Requirements

- A TextConvo account with API access &mdash; [contact us](https://textconvo.ai/contact-us) to get one
- An API key and a source key ([Authentication](https://textconvo.ai/docs#authentication))
- {{RUNTIME_REQUIREMENT}}

## Quick start

    {{INSTALL_OR_CLONE_COMMAND}}
    {{RUN_COMMAND}}

Set credentials as environment variables. Never commit them.

    export TEXTCONVO_API_KEY="YOUR_API_KEY"
    export TEXTCONVO_SOURCE_KEY="YOUR_SOURCE_KEY"

## Contents

| Path | What it covers |
| --- | --- |
| {{PATH}} | {{DESCRIPTION}} |

## Documentation

| Topic | Link |
| --- | --- |
| Quick start | [textconvo.ai/docs#quick-start](https://textconvo.ai/docs#quick-start) |
| Authentication | [textconvo.ai/docs#authentication](https://textconvo.ai/docs#authentication) |
| HMAC request signing | [textconvo.ai/docs#hmac-authentication](https://textconvo.ai/docs#hmac-authentication) |
| Lead ingestion | [textconvo.ai/docs#lead-ingestion-api](https://textconvo.ai/docs#lead-ingestion-api) |
| Webhooks | [textconvo.ai/docs#webhooks](https://textconvo.ai/docs#webhooks) |
| Rate limits | [textconvo.ai/docs#rate-limits](https://textconvo.ai/docs#rate-limits) |
| Error codes | [textconvo.ai/docs#error-codes](https://textconvo.ai/docs#error-codes) |
| CRM integrations | [textconvo.ai/docs#crm-integrations](https://textconvo.ai/docs#crm-integrations) |

## Roadmap

- [ ] {{NEXT_THING}}
- [ ] {{THING_AFTER_THAT}}

## Contributing

Issues and pull requests are welcome. Read [CONTRIBUTING.md](https://github.com/textconvo/.github/blob/main/CONTRIBUTING.md) and the [Code of Conduct](https://github.com/textconvo/.github/blob/main/CODE_OF_CONDUCT.md) first.

## Security

Do not open a public issue for a vulnerability. Follow [SECURITY.md](https://github.com/textconvo/.github/blob/main/SECURITY.md).

## Support

Questions about this repository belong in [issues](https://github.com/textconvo/{{REPOSITORY_NAME}}/issues). Account, billing, and production questions go to [textconvo.ai/contact-us](https://textconvo.ai/contact-us).

## License

[MIT](LICENSE) &copy; TextConvo
