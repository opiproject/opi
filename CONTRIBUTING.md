# Contributing

OPI uses GitHub to manage reviews of pull requests.

* If you are a new contributor see: [Steps to Contribute](#steps-to-contribute) and [GitHub Basic Process](Policies/doc-github-rules.md) for more details.

* If you have a trivial fix or improvement, go ahead and create a pull request,
  addressing (with `@...`) a suitable maintainer of this repository (see
  [MAINTAINERS.md](Policies/MAINTAINERS.md)) in the description of the pull request.

* Be sure to sign off on the [DCO](https://github.com/probot/dco#how-it-works).

## Architecture Changes

Changes to project wide goals or scope, subgroup goals or scope, or major
architectural changes shall be:

* Submitted via PR to the appropriate repo
* Labeled with the `architecture` label
  * Submitters may apply the `architecture` label, but maintainers for the repo
    involved have final say on whether a given PR requires the `architecture`
    label.
* Broadcast to the `opi-dev` mailing list
* Left open for review for at least 4 days
  * Maintainers are expected to give a reasonable amount of time for review,
    taking into account weekends and holidays.  This may mean PRs require longer
    than 4 calendar days.
* Approved by at least 2 maintainers for the repo involved

## Steps to Contribute

Should you wish to work on an issue, please claim it first by commenting on the
GitHub issue that you want to work on it. This is to prevent duplicated efforts
from contributors on the same issue.

## Pull Request Checklist

* Branch or fork (preferred) from the main branch and, if needed, rebase to the current main branch
  before submitting your pull request. If it doesn't merge cleanly with main
  you may be asked to rebase your changes.

* Commits should be as small as possible, while ensuring that each commit is
  correct independently (i.e., each commit should compile and pass tests).

* If your patch is not getting reviewed or you need a specific person to review
  it, you can @-reply a reviewer asking for a review in the pull request or a
  comment. The project will soon have an IRC and/or Slack channel setup, which
  will also become a useful way to notify a maintainer.

* Add tests relevant to the fixed bug or new feature.
