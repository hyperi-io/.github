<!-- DO NOT EDIT. Published from hyperi-io/hyperi-licensing public/org-github/.github/CONTRIBUTING.md. Change it there: the next sync overwrites edits made here. -->
# Contributing

This guide covers every HyperI repository that has no CONTRIBUTING file of its own. A fork of someone else's project follows that project's guide, not this one.

## Issues

- Pick the form that fits: bug report, feature request or task. A maintainer triages it, so leave labels alone.
- Search open and closed issues first. Add to an existing one rather than opening a duplicate.
- Security problems never go in a public issue. Follow the [security policy](SECURITY.md).

## Pull requests

1. Open or find the issue first. One issue, one pull request. No drive-by changes alongside it.
2. Fork and branch from `main`. Members of the organisation branch in the repository itself.
3. Name the issue it fixes, as in `Fixes #NNN`.
4. Title it as a Conventional Commit, such as `fix: handle an empty config file`. A squash merge uses the title as the commit subject.
5. The type sets the release. `fix:` ships a patch and `feat:` a minor, and most changes are `fix:`. Leave versions, tags and the changelog alone, because CI writes them.
6. Don't add a dependency unless the issue asked for one.
7. Run the repository's own checks before you push. Repositories with a `.hyperi-ci.yaml` use `hyperi-ci check`. Read the workflow files too, as some repos add their own steps.

In repositories that use hyperi-ci, pull requests from forks skip CI and every check reads as passed. A maintainer runs the full checks before merging.

## Tests

Change the fewest tests that prove the fix, in this order.

1. Run the existing tests and find the one that should have caught it.
2. Amend that test, or add a case to its table.
3. Write a new test only when nothing existing covers the behaviour.

Test the failure cases, not only the happy path: bad input, empty input, the boundary. Test data is made up or scrubbed. No real hostnames, addresses, tokens, customer names or log lines.

## Using AI tools

You can use AI tools here. Most of us do. But a person opens the issue or pull request, and that person answers for every line of it. An agent never files, comments or pushes on its own.

Agents get the cause wrong far more often than they get the code wrong. They see a symptom, find something nearby that looks guilty, and fix that. So whether you are a person or an agent, the rules below are the same.

**Reproduce it first.** Run it on the latest release or `main`, and write down the version or commit you ran. If you can't reproduce it, say so.

**Write the root cause out step by step.** From the input to the wrong output, one step a line, each pointing at a file and line or a command you ran. "Probably a race in X" is a guess, not a cause.

**Keep facts and guesses apart.** Facts are things you ran or read, with the output. Guesses are labelled as guesses, with how confident you are and what result would prove them wrong.

**Review your own change before anyone else sees it.** Assume it is wrong. Re-read the diff and every caller of every function you changed, then run the checks again. With an agent, start a fresh session for this, so it isn't marking its own homework.

**Don't push straight away.** Open the pull request only once the cause is written out, the checks pass and the review is done. A draft pull request is fine for asking a question.

**Say what the AI did.** Say in the pull request which tool you used, for what, and what you checked yourself. "Claude wrote the fix, I reproduced the bug and read every line" is enough.

Pull requests that skip these get closed without review. Not personal. Reviewer time is the scarce part.

## Sign-off and licence

- Sign off every commit with `git commit --signoff`. It certifies the [Developer Certificate of Origin 1.1](https://developercertificate.org/), and you can only certify it if you have checked where AI-written code came from.
- Your contribution is licensed under the terms in the repository's LICENSE file.
