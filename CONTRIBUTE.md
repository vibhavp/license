# Contributing

The `go-interpreter` project eagerly accepts contributions from the community.

## Introduction


The `go-interpreter` project provides libraries and tools in Go for the Go community to create interpreter(s) in Go, for Go, and we would like you to join us in improving `go-interpreter`'s quality and scope.
This document is for anyone who is contributing or interested in contributing.
Questions about `go-interpreter` or the use of its libraries can be directed to the [go-interpreter](mailto:go-interpreter@googlegroups.com) mailing list.

## Contributing

### Working Together

When contributing or otherwise participating, please:

- Be friendly and welcoming
- Be patient
- Be thoughtful
- Be respectful
- Be charitable
- Avoid destructive behavior

Excerpted from the [Go conduct document](https://golang.org/conduct).

### Reporting Bugs

When you encounter a bug, please open an issue on the corresponding repository.
Start the issue title with the repository/sub-repository name, like `bind: issue name`.
Be specific about the environment you encountered the bug in (_e.g.:_ operating system, Go compiler version, ...).
If you are able to write a test that reproduces the bug, please include it in the issue.
As a rule, we keep all tests OK and try to increase code coverage.

### Suggesting Enhancements

If the scope of the enhancement is small, open an issue.
If it is large, such as suggesting a new repository, sub-repository, or interface refactoring, then please start a discussion on [the go-interpreter list](https://groups.google.com/forum/#!forum/go-interpreter).

### Your First Code Contribution

If you are a new contributor, *thank you!*
Before your first merge, you will need to be added to the [CONTRIBUTORS](https://github.com/go-interpreter/license/blob/master/CONTRIBUTORS) and [AUTHORS](https://github.com/go-interpreter/license/blob/master/AUTHORS) files.
Open a pull request adding yourself to these files.
All `go-interpreter` code follows the BSD license in the [license document](https://github.com/go-interpreter/license/blob/master/LICENSE).
We prefer that code contributions do not come with additional licensing.
For exceptions, added code must also follow a BSD license.

### Code Contribution

If it is possible to split a large pull request into two or more smaller pull requests, please try to do so.
Pull requests should include tests for any new code before merging.
It is ok to start a pull request on partially implemented code to get feedback, and see if your approach to a problem is sound.
You don't need to have tests, or even have code that compiles to open a pull request, although both will be needed before merge.
When tests use magic numbers, please include a comment explaining the source of the number.
Benchmarks are optional for new features, but if you are submitting a pull request justified by performance improvement, you will need benchmarks to measure the impact of your change, and the pull request should include a report from [benchcmp](https://godoc.org/golang.org/x/tools/cmd/benchcmp) or, preferably, [benchstat](https://github.com/rsc/benchstat).

Commit messages also follow some rules.
They are best explained at the official [Go](https://golang.org) "Contributing guidelines" document:

[golang.org/doc/contribute.html](https://golang.org/doc/contribute.html#commit_changes)

For example:

```
wagon: add support for switch statements

This CL adds support for switch statements.
Previously, the wagon package was ignoring switch statements, leading to
a panic later on in the program execution.
Implement the switch statement and add some tests.

Fixes go-interpreter/wagon#42.
```

If the `CL` modifies multiple packages at the same time, include them in the commit message:

```
wagon,wagon/wasm: implement wrapping of Go interfaces

bla-bla

Fixes go-interpreter/wagon#40.
```

Please always format your code with [goimports](https://godoc.org/golang.org/x/tools/cmd/goimports).
Best is to have it invoked as a hook when you save your `.go` files.

Files in the `go-interpreter` repository don't list author names, both to avoid clutter and to avoid having to keep the lists up to date.
Instead, your name will appear in the change log and in the [CONTRIBUTORS](https://github.com/go-interpreter/license/blob/master/CONTRIBUTORS) and [AUTHORS](https://github.com/go-interpreter/license/blob/master/AUTHORS) files.

New files that you contribute should use the standard copyright header:

```
// Copyright 2017 The go-interpreter Authors.  All rights reserved.
// Use of this source code is governed by a BSD-style
// license that can be found in the LICENSE file.
```

Files in the repository are copyright the year they are added.
Do not update the copyright year on files that you change.

### Code Review

If you are a contributor, please be welcoming to new contributors.
[Here](http://sarah.thesharps.us/2014/09/01/the-gentle-art-of-patch-review/) is a good guide.

There are several terms code reviewers may use that you should become familiar with.

  * ` LGTM ` — looks good to me
  * ` SGTM ` — sounds good to me
  * ` CL ` — change list; a single commit in the repository
  * ` PTAL ` — please take another look
  * ` s/foo/bar/ ` — please replace ` foo ` with ` bar `; this is [sed syntax](http://en.wikipedia.org/wiki/Sed#Usage)
  * ` s/foo/bar/g ` — please replace ` foo ` with ` bar ` throughout your entire change

We follow the convention of requiring at least 1 reviewer to say LGTM before a merge.
When code is tricky or controversial, submitters and reviewers can request additional review from others and more LGTMs before merge.
You can ask for more review by saying PTAL in a comment in a pull request.
You can follow a PTAL with one or more @someone to get the attention of particular people.
If you don't know who to ask, and aren't getting enough review after saying PTAL, then PTAL @go-interpreter/developers will get more attention.
Also note that you do not have to be the pull request submitter to request additional review.

### What Can I Do to Help?

If you are looking for some way to help the `go-interpreter` project, there are good places to start, depending on what you are comfortable with.

- You can [search](https://github.com/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+user%3Ago-interpreter) for open issues in need of resolution.
- You can improve documentation, or improve examples.
- You can add and improve tests.
- You can improve performance, either by improving accuracy, speed, or both.
- You can suggest and implement new features that you think belong in `go-interpreter`.

### Style

We use [Go style](https://github.com/golang/go/wiki/CodeReviewComments).

---

This _"Contributing"_ guide has been extracted from the [Gonum](https://gonum.org) project.
Its guide is [here](https://github.com/gonum/license/blob/master/CONTRIBUTING.md).
