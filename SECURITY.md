# Security Policy

TextConvo moves customer conversations across SMS, RCS, Voice AI, Email, and WhatsApp. We take reports about our platform and our public code seriously, and we would rather hear from you early than read about it later.

## Reporting a vulnerability

**Do not open a public issue, pull request, or discussion for a security report.**

Use one of these channels instead:

1. **GitHub private vulnerability reporting** &mdash; on the affected repository, open the **Security** tab and choose **Report a vulnerability**. This keeps the thread private between you and the maintainers.
2. **Email** &mdash; [security@textconvo.ai](mailto:security@textconvo.ai). This inbox is monitored by the engineering team. Ask for an encrypted channel if you need one before sharing details.
3. **Contact form** &mdash; [textconvo.ai/contact-us](https://textconvo.ai/contact-us) with the subject line **Security Report**, if email is not an option for you.

## What to include

A good report lets us reproduce the issue without guessing:

- A clear description of the issue and its impact.
- The affected repository, file, endpoint, or SDK version.
- Step-by-step reproduction, including requests and responses with secrets redacted.
- Proof-of-concept code, if you have it.
- Your assessment of severity, and whether the issue is already public.

Redact real API keys, phone numbers, message bodies, and any personal data before sending anything. If you accessed customer data accidentally, tell us &mdash; and do not retain, share, or publish it.

## Our commitments

| Stage | Target |
| --- | --- |
| Acknowledgement | Within 2 business days |
| Initial assessment and severity | Within 5 business days |
| Remediation plan shared with reporter | Within 10 business days |
| Fix for critical platform issues | As fast as safely possible, ahead of other work |

We will keep you updated while we work, credit you when a fix ships if you want the credit, and tell you plainly if we decide something is not a vulnerability.

## Coordinated disclosure

Please give us a reasonable window to ship a fix before publishing. We aim for 90 days from acknowledgement, and we are happy to agree a shorter timeline for low-risk issues or a longer one for anything that needs coordination with a carrier or downstream provider.

## Scope

**In scope**

- The TextConvo platform, API, and webhook delivery.
- Authentication, HMAC request signing, and webhook signature verification.
- Any code published in a public TextConvo repository.

**Out of scope**

- Reports generated entirely by automated scanners with no demonstrated impact.
- Missing hardening headers or best-practice suggestions with no exploit path.
- Social engineering of TextConvo staff or customers, physical attacks, and denial-of-service testing.
- Vulnerabilities in third-party services we integrate with &mdash; report those to the vendor.
- Spam, phishing, or content-policy complaints. Report those through [textconvo.ai/contact-us](https://textconvo.ai/contact-us).

Do not test against production traffic, other customers’ accounts, or real phone numbers you do not own.

## Safe harbour

If you make a good-faith effort to follow this policy, we will not pursue or support legal action against you for your research. Act only against your own account and data, avoid privacy violations and service degradation, and stop as soon as you have proof of a finding.

## Secrets in public code

If you find a credential, key, token, or connection string committed anywhere in this account, report it through the private channels above and treat it as compromised. It is a security issue, not a bug report.

## Hardening guidance for integrators

- Verify every webhook signature before trusting a payload &mdash; see [Webhook security](https://textconvo.ai/docs#webhooks).
- Reject webhook timestamps outside the documented skew window and use a constant-time comparison for signatures.
- Store API keys, source keys, and webhook secrets in a secret manager, never in source control or client-side code.
- Rotate keys on a schedule and on staff changes, and use a distinct key per integration.
- Treat `X-Request-Id` as an idempotency key so retries cannot double-ingest a lead.
