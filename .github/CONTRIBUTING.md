<!-- DO NOT EDIT. Published from hyperi-io/hyperi-licensing public/org-github/.github/CONTRIBUTING.md. Change it there: the next sync overwrites edits made here. -->
# Contributing

This guide covers every HyperI repository that has no CONTRIBUTING file of its own.

## Issues

- Open an issue and pick the form that fits: bug report, feature request or task.
- A maintainer triages it. You do not need to add labels.
- Security problems never go in a public issue. Follow the [security policy](SECURITY.md).

## Pull requests

1. Fork the repository and branch from `main`. Members of the organisation branch in the repository itself.
2. Keep one change per pull request, and name the issue it fixes, as in `Fixes #NNN`.
3. Title it as a Conventional Commit, such as `fix: handle an empty config file`. A squash merge of several commits uses the title as the commit subject.
4. The type sets the release. `fix:` ships a patch and `feat:` a minor, and most changes are `fix:`. Leave versions, tags and the changelog alone, because CI writes them.
5. Run the repository's own checks before you push. Repositories with a `.hyperi-ci.yaml` use `hyperi-ci check`.

In repositories that use hyperi-ci, pull requests from forks skip CI and every check reads as passed. A maintainer runs the full checks before merging.

## Sign-off and licence

- Sign off every commit with `git commit --signoff`. It certifies the [Developer Certificate of Origin 1.1](https://developercertificate.org/).
- Your contribution is licensed under the terms in the repository's LICENSE file.
