# Repository standards

Every public TextConvo repository follows the conventions below. They exist so the account reads as one deliberate engineering surface rather than a pile of side projects.

## The one rule that outranks the others

Public repositories contain **examples, specifications, SDK surfaces, and documentation links**. They never contain platform implementation, orchestration logic, model prompts, database or infrastructure detail, or credentials of any kind. Reference documentation is linked, not duplicated: [textconvo.ai/docs](https://textconvo.ai/docs) is the single source of truth.

## Naming

| Pattern | Use |
| --- | --- |
| textconvo-&lt;surface&gt; | Official artefacts: textconvo-openapi, textconvo-postman, textconvo-webhooks |
| textconvo-&lt;language&gt;-sdk | Official SDKs: textconvo-node-sdk, textconvo-python-sdk |
| textconvo-&lt;plural-noun&gt; | Collections: textconvo-api-examples, textconvo-sample-apps |
| awesome-textconvo | The curated community list, matching the awesome-list convention |

Lowercase, hyphenated, no abbreviations, no version numbers in names.

## Descriptions

One sentence, sentence case, no trailing period needed, front-loaded with the noun. Say what it is and who it is for. Prefix with "Official" only where TextConvo maintains the artefact.

| Repository | Description |
| --- | --- |
| textconvo-api-examples | Official TextConvo API examples in cURL, JavaScript, TypeScript, Node.js, Python, Go, Java, C#, and PHP |
| textconvo-postman | Official TextConvo Postman collection and environment |
| textconvo-openapi | Official OpenAPI specification for the TextConvo API |
| textconvo-webhooks | TextConvo webhook payloads, signature verification, and sample receivers |
| textconvo-sample-apps | Demo applications built on the TextConvo API |
| textconvo-node-sdk | Official TextConvo SDK for Node.js and TypeScript |
| awesome-textconvo | Curated tutorials, videos, articles, and community projects for TextConvo |
| terraform-examples | Terraform examples for teams deploying TextConvo integrations |

## Topics

Apply the shared set, then two or three that are specific to the repository. Topics are how developers find you from GitHub search.

**Shared:** textconvo, ai-orchestration, conversational-ai, sms, rcs, voice-ai, email, whatsapp, customer-engagement, api

**Add per repository:** api-examples, openapi, openapi3, postman, postman-collection, webhooks, hmac, sdk, nodejs, typescript, python, golang, java, dotnet, php, sample-apps, terraform, awesome-list

Rules: lowercase, hyphenated, no more than 20 topics, no duplicates of the repository name, no marketing words.

## Required files

| File | Every repo | Notes |
| --- | --- | --- |
| README.md | Yes | Start from templates/README_TEMPLATE.md |
| LICENSE | Yes | MIT for examples, specifications, and SDKs |
| CONTRIBUTING.md | Inherited | Provided by textconvo/.github |
| CODE_OF_CONDUCT.md | Inherited | Provided by textconvo/.github |
| SECURITY.md | Inherited | Provided by textconvo/.github |
| SUPPORT.md | Inherited | Provided by textconvo/.github |
| .github/CODEOWNERS | Yes | Start from the CODEOWNERS template |
| .gitignore | Where code exists | Language appropriate |

## Branches and merges

- Default branch is main. Work happens on short-lived branches: fix/, feat/, docs/, chore/.
- Squash merge only. The pull request title becomes the changelog entry, so write it in Conventional Commits form.
- Delete branches after merge.

### Recommended protection for main

- Require a pull request before merging, with at least one approving review.
- Require review from Code Owners.
- Require conversation resolution before merging.
- Require status checks to pass, once checks exist.
- Block force pushes and deletions.
- Apply the rules to administrators too.

## Discussions

Enable Discussions on textconvo-api-examples, textconvo-webhooks, textconvo-sample-apps, and awesome-textconvo. Use these categories:

| Category | Format | Purpose |
| --- | --- | --- |
| Announcements | Announcement | Releases, deprecations, and specification changes. Maintainers post, everyone comments. |
| Q&amp;A | Question and answer | Integration questions that are not bugs. Answers get marked. |
| Ideas | Open discussion | Proposals for examples, SDK surface, and developer experience. |
| Show and tell | Open discussion | What the community built. Feeds awesome-textconvo. |
| Channels and compliance | Question and answer | SMS, RCS, Voice AI, Email, WhatsApp, 10DLC, and consent questions. |
| Integrations | Question and answer | CRM and workflow tooling: HubSpot, GoHighLevel, Zoho, Pipedrive, Zendesk, Salesforce. |
| Roadmap | Announcement | What is coming next on the public developer surface. |

Pin one welcome post per repository explaining that account-specific issues go to [textconvo.ai/contact-us](https://textconvo.ai/contact-us) and security reports follow SECURITY.md.

## Releases

Semantic versioning, tags in the form v1.4.0, and release notes written from templates/RELEASE_TEMPLATE.md. Pre-launch SDKs stay on 0.x and say so plainly in the README.

## Repository hygiene

- Enable secret scanning and push protection.
- Enable Dependabot alerts, and version updates where dependencies exist.
- Enable private vulnerability reporting so SECURITY.md has somewhere to point.
- Disable wikis and projects unless a repository actively uses them.
- Add the repository to the account profile README table when it goes public.
