# Contributing to C++ Micro Services

This page contains information about reporting issues as well as some tips and
guidelines useful to experienced open source contributors. Make sure you read
the contribution guideline before you start participating.

## Topics

* [Reporting Issues](#reporting-issues)
* [Contribution Guidelines](#contribution-guidelines)

## Reporting issues

A great way to contribute to the project is to send a detailed report when you
encounter an issue. We always appreciate a well-written, thorough bug report,
and will thank you for it!

Check that the [issue database](https://github.com/CppMicroServices/CppMicroServices/issues)
doesn't already include that problem or suggestion before submitting an issue.
If you find a match, add a quick "+1" or "I have this problem too." Doing this
helps prioritize the most common problems and requests.

When reporting issues, please include your host OS and compiler vendor and version.
Please also include the steps required to reproduce the problem if possible and
applicable.

## Contribution guidelines

This section gives the experienced contributor some tips and guidelines.

### Conventions

Fork the repository and make changes on your fork in a feature branch:

- If it's a bug fix branch, name it XXXX-something where XXXX is the number of
  the issue.
- If it's a feature branch, create an enhancement issue to announce
  your intentions, and name it XXXX-something where XXXX is the number of the
  issue.

Submit unit tests for your changes.

Update the documentation when creating or modifying features. Test your
documentation changes for clarity, concision, and correctness.

Pull request descriptions should be as clear as possible and include a reference
to all the issues that they address.

Commit messages must start with a capitalized and short summary (max. 50 chars)
written in the imperative, followed by an optional, more detailed explanatory
text which is separated from the summary by an empty line.

Code review comments may be added to your pull request. Discuss, then make the
suggested modifications and push additional commits to your feature branch. Post
a comment after pushing. New commits show up in the pull request automatically,
but the reviewers are notified only when you comment.

Pull requests must be cleanly rebased on top of *development* without multiple
branches mixed into the PR.

**Git tip**: If your PR no longer merges cleanly, use `rebase development` in your
feature branch to update your pull request rather than `merge development`.

Before you make a pull request, squash your commits into logical units of work
using `git rebase -i` and `git push -f`. A logical unit of work is a consistent
set of patches that should be reviewed together: for example, upgrading the
version of a vendored dependency and taking advantage of its now available new
feature constitute two separate units of work. Implementing a new function and
calling it in another file constitute a single logical unit of work. The very
high majority of submissions should have a single commit, so if in doubt: squash
down to one.

After every commit, make sure the test suite passes. Include documentation
changes in the same pull request so that a revert would remove all traces of
the feature or fix.

Include an issue reference like `Closes #XXXX` or `Fixes #XXXX` in commits that
close an issue. Including references automatically closes the issue on a merge.

If your change is large enough to warrant a copyright statement, add yourself
to the `COPYRIGHT` file, using the same style as the existing entries.

### Sign your work

The sign-off is a simple line at the end of the explanation for the patch. Your
signature certifies that you wrote the patch or otherwise have the right to pass
it on as an open-source patch. The rules are pretty simple: if you can certify
the below (from [developercertificate.org](http://developercertificate.org/)):

```
Developer Certificate of Origin
Version 1.1

Copyright (C) 2004, 2006 The Linux Foundation and its contributors.
660 York Street, Suite 102,
San Francisco, CA 94110 USA

Everyone is permitted to copy and distribute verbatim copies of this
license document, but changing it is not allowed.

Developer's Certificate of Origin 1.1

By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.
```

Then you just add a line to every git commit message:

    Signed-off-by: Joe Smith <joe.smith@email.com>

Use your real name (sorry, no pseudonyms or anonymous contributions).

If you set your `user.name` and `user.email` git configs, you can sign your
commit automatically with `git commit -s`.

### Code of Conduct

CppMicroServices.org welcomes developers with different backgrounds and a broad range of 
experience. A diverse and inclusive community will create more great ideas, provide more unique 
perspectives, and produce more outstanding code. Our aim is to make the CppMicroServices community 
welcoming to everyone.

To provide clarity of what is expected of our members, CppMicroServices has adopted the code 
of conduct defined by [contributor-covenant.org][contributor-covenant.org]. This document is used 
across many open  source communities, and we believe it articulates our values well. 

Please refer to the [Code of Conduct](./CodeOfConduct.md) for further details.

[contributor-covenant.org]: http://contributor-covenant.org
