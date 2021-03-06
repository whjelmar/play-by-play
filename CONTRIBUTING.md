# How to Contribute

We're excited you're interested in contributing to play-by-play! We'd love your help.

We welcome all levels of expertise from novice to experts.

If you are `very new` to the open source contribution:
* `Fork` this repo
* `Star` this repo and your own fork
* In `Issues` tab, read some that interests you
* You can Follow us on `twitter`, https://twitter.com/whjelmar

TODO - project twitter??


Further, check the `Resources` section at the bottom of this page.


There are plenty of ways to contribute:

* Fix or [report](https://github.com/whjelmar/play-by-play/issues/new) a bug
* Fix or improve documentation
* Pick up a ["good first issue"](https://github.com/whjelmar/play-by-play/labels/good%20first%20issue), then send a pull request our way

We feel that a welcoming community is important and we ask that you follow the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md) in all interactions with the community.

# Development

To run the entire test suite:

TODO

You can also run individual tests using the flag `--tests`:

TODO

Or run tests by category:  

TODO

# Coding Style Guide

TODO


# Submitting a [Pull Request](https://help.github.com/articles/about-pull-requests)

1. [Fork](https://github.com/whjelmar/play-by-play/fork) and clone the repository
2. Make sure all tests pass locally: `./gradlew test`
3. Create a new [branch](#branching): `git checkout -b feature/my-cool-new-feature`
4. Make change on your cool new branch
5. Write a test for your change
6. Make sure source files are formatted: see Coding Style Guide above
7. Make sure to [sign you work](#sign-your-work)
8. Push change to your fork and [submit a pull request](https://github.com/whjelmar/play-by-play/compare)
9. Work with project maintainers to get your change reviewed and merged into the `main` branch
10. Delete your branch

To ensure your pull request is accepted, follow these guidelines:

* All changes should be accompanied by tests
* Do your best to have a [well-formed commit message](https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html) for your change
* [Keep diffs small](https://graysonkoonce.com/stacked-pull-requests-keeping-github-diffs-small) and self-contained
* If your change fixes a bug, please [link the issue](https://help.github.com/articles/closing-issues-using-keywords) in your pull request description
* Any changes to the API reference requires [regenerating](#docs) the static `openapi.html` file.

> **Note:** A pull request should generally contain only one commit (use `git commit --amend` and `git push --force` or [squash](http://gitready.com/advanced/2009/02/10/squashing-commits-with-rebase.html) existing commits into one).

# Branching

* Use a _group_ at the beginning of your branch names

  ```
  wip      Work on a feature is still in progress
  feature  Add or expand a feature
  bug      Fix a bug
  ```
  
  _For example_:
  
  ```
  wip/my-cool-new-wip-feature
  feature/my-cool-new-feature
  feature/my-other-cool-new-feature
  bug/my-bug-fix
  bug/my-other-bug-fix
  ```
  
* Choose _short_ and _descriptive_ branch names
* Use dashes (`-`) to separate _words_ in branch names
* Use _lowercase_ in branch names

# Sign Your Work

The _sign-off_ is a simple line at the end of the message for a commit. All commits needs to be signed. Your signature certifies that you wrote the patch or otherwise have the right to contribute the material (see [Developer Certificate of Origin](https://developercertificate.org)):

```
This is my commit message

Signed-off-by: Walter Hjelmar <walter@hjelmar.com>
```

Git has a [`-s`](https://git-scm.com/docs/git-commit#Documentation/git-commit.txt---signoff) command line option to append this automatically to your commit message:

```bash
$ git commit -s -m "This is my commit message"
```

# API [Docs](https://github.com/whjelmar/play-by-playcreation/tree/main/docs)

TODO 

To bundle:

```bash
$ redoc-cli bundle docs/openapi.yml -o docs/openapi.html  --title "play-by-playcreation API Reference"
```

To serve:  

```bash
$ redoc-cli serve docs/openapi.yml
```

Then browse to: http://localhost:8080

> **Note:** To bundle or serve the API docs, please install [redoc-cli](https://www.npmjs.com/package/redoc-cli).

# Resources

* [How to Contribute to Open Source](https://opensource.guide/how-to-contribute)
* [Using the Fork-and-Branch Git Workflow](https://blog.scottlowe.org/2015/01/27/using-fork-branch-git-workflow)
* [Keep a Changelog](https://keepachangelog.com)
* [Code Review Developer Guide](https://google.github.io/eng-practices/review)
* [Signing Commits](https://docs.github.com/en/github/authenticating-to-github/signing-commits)
