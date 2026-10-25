# .github

Organisation defaults for hyperi-io. GitHub shows these files in every repository that has no file of its own.

- `.github/` holds what GitHub reads: the issue forms, and the contributing, security, support and conduct policies.
- `labels/labels.yaml` is the issue label set. See [labels/README.md](labels/README.md).
- `workflow-templates/` holds starters for the Actions "New workflow" page. Each calls a hyperi-ci workflow and is saved as `.github/workflows/ci.yml`.
- `profile/README.md` is the organisation's public profile.

A repository overrides a file by adding its own. Issue forms are all or nothing: a repository with any file in its own `.github/ISSUE_TEMPLATE` gets none of these. None of these files reach clones, mirrors or packages, so every repository keeps its own LICENSE.

Changes go through a pull request, and CI checks the forms, the label set and the starters before merge.
