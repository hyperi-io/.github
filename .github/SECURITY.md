# Security policy

This policy covers every HyperI repository that has no SECURITY.md of its own.

## Report a vulnerability

Never in a public issue, pull request or comment.

- Public repository: use private vulnerability reporting. Open the repository's Security and quality tab, go to Advisories and choose Report a vulnerability.
- Anything else, or if that button is missing: email security@hyperi.io.
- Members working in a private repository: open an issue there with the `security` label.

Include what you found, the affected component and version, steps to reproduce, a proof of concept if you have one, and how to reach you.

## What happens next

- We acknowledge a report within 5 business days.
- We investigate and keep you informed.
- We fix confirmed vulnerabilities and agree a disclosure date with you.
- Fixes go into the latest release of each project. A repository's own policy can say more.

## Forks

Some repositories here are forks of other projects. Report a problem in the upstream code to the upstream project, and a problem in our changes to us.

## Safe harbour

We will not take legal action against researchers who:

- report in good faith
- make a reasonable effort to avoid privacy violations, data destruction and service disruption
- access or change no more data than they need to show the vulnerability
- give us reasonable time to fix it before public disclosure
- comply with applicable Australian law

## Out of scope

- Social engineering and phishing
- Denial of service
- Physical security
- Attacks that need access to a user's device or account
- Issues in third-party dependencies, which go to their maintainers
- Theoretical issues with no proof of exploitability
- Missing security headers or TLS settings that are not directly exploitable

## Recognition

With your permission we credit you for confirmed findings. We do not run a paid bounty.
