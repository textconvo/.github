<!--
Release notes template for TextConvo public repositories.

Tag format: v{MAJOR}.{MINOR}.{PATCH}
Title format: v1.4.0 &mdash; short human summary

Write for an integrator who has to decide whether to upgrade this afternoon.
Lead with impact, not with commit messages.
-->

## Summary

{{ONE_PARAGRAPH: what changed and why an integrator should care}}

## Highlights

- {{The single most useful change}}
- {{The second}}
- {{The third}}

## Breaking changes

> Delete this section if there are none. Never bury a breaking change.

| Change | Who is affected | What to do |
| --- | --- | --- |
| {{WHAT_BROKE}} | {{WHO}} | {{MIGRATION_STEP}} |

## Added

- {{NEW_CAPABILITY}} ({{PR_LINK}})

## Changed

- {{BEHAVIOUR_CHANGE}} ({{PR_LINK}})

## Fixed

- {{BUG_FIX}} ({{PR_LINK}})

## Deprecated

- {{WHAT}} &mdash; still works, will be removed in {{VERSION}}. Use {{ALTERNATIVE}} instead.

## Removed

- {{WHAT}} &mdash; deprecated in {{VERSION}}.

## Security

- {{FIX_DESCRIPTION}}. No customer action required, or: rotate {{CREDENTIAL}} and redeploy.

## Upgrade notes

    {{UPGRADE_COMMAND}}

Minimum supported {{RUNTIME}}: {{VERSION}}.

## Documentation

- {{Any doc page updated for this release}} &mdash; [textconvo.ai/docs](https://textconvo.ai/docs)

## Verification

{{How the release was tested: examples executed, spec validated, sandbox account used}}

## Contributors

Thanks to {{@handles}} for contributions in this release.

---

**Full changelog:** {{PREVIOUS_TAG}}...{{THIS_TAG}}
**Documentation:** [textconvo.ai/docs](https://textconvo.ai/docs) &middot; **Support:** [textconvo.ai/contact-us](https://textconvo.ai/contact-us)
