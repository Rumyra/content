### Pull request etiquette

Here are some important rules of etiquette to remember when working
with pull requests.

1. When you submit a pull request, a number of tests are automatically run
as GitHub Actions (see [.github/workflows](.github/workflows)). If
one or more of these tests fail, it is your responsibility to try and
resolve the underlying issue(s). If you don't know how to resolve the
underlying issue(s), you can ask for help. Your pull request will not be
approved and merged if these tests are failing.

1. If your pull request has merge conflicts with the `main` branch (GitHub
checks for this automatically and notifies you), you are responsible for
resolving them. You can do this by merging the `main` branch into your
branch (`git pull mdn main`), and then pushing the updated branch to
your fork (`git push`).

1. An alternative strategy is `git rebase` of `main` on your branch.
This will rewrite the git history and might confuse reviewers as notifications
from GitHub lead to nowhere. Your changes are replayed on top of the current
main branch at that point in time.

1. Each pull request should contain a single logical change, or related set
of changes that make sense to submit together. If a pull request becomes
too large or contains too many unrelated changes, it becomes too difficult
to review, and may begin to look suspicious (it is easier to hide malicious
changes in a large pull request). In such cases, the reviewer has the right
to close your pull request, and ask that you submit a separate pull request
for each logical set of changes that belong together.

1. If your pull request contains any kind of significant complexity
(it contains technical changes, and isn't just a typo fix, grammatical
improvement, or formatting/structural change), please describe why you're
making the change and anything else we need to know about it.
   - If the pull request is simple (it is really clear what has been
   changed and why, and the change is obviously a good thing), you can do
   this in your pull request's description.
   - If the pull request is complex (the changes and the reasoning behind
   them need a bit more explanation), then the requestor should file an
   issue describing the intended change first, and seek discussion/approval
   as needed. When the time is right to submit the PR, they should
   reference the issue (or an existing issue that describes the motivation
   for the change) in the PR. You can reference an existing issue
   using `#` followed by the issue's ID, for example `#1234`.
   - Pull requests should not contain large amounts of grammar updates.
   Seemingly insignificant changes can change the meaning of technical
   content, so these need a careful review. Keep in mind that MDN contains
   technical documentation; you should not report merely basic improvements
   in the grammar but only cases where the grammar is incorrect.

1. Do not re-open a pull request that a reviewer has closed.