# Contributing to Steamdeckdocs

We're glad you want to contribute steamdeckdocs! This document will help answer
common questions you may have during your first contribution. Please, try to
follow these guidelines when you do so.

## Issue Reporting

Not every contribution comes in the form of code. Submitting, confirming, and
triaging issues is an important task for any project. We use GitHub to track
all project issues. If you discover bugs, have ideas for improvements or new
features, please start by [opening an
issue](https://github.com/tuxx/steamdeckdocs/issues) on this repository.
We use issues to centralize the discussion and agree on a plan of action before
spending time and effort writing code that might not get used.

### Submitting An Issue

* Check that the issue has not already been reported
* Select the appropriate issue type and open an issue with a descriptive title
* Be clear, concise, and precise using grammatically correct, complete sentences
  in your summary of the problem

## Contributions

Steamdeckdocs follows a [forking
workflow](https://guides.github.com/activities/forking/), and we have a simple
process for contributions:

1. Open an issue on the [project
   repository](https://github.com/tuxx/steamdeckdocs/issues), if
   appropriate
1. Follow the [forking workflow](https://guides.github.com/activities/forking/)
   steps:
   1. Fork the project ( <https://github.com/tuxx/steamdeckdocs/fork> )
   1. Create your feature branch (`git checkout -b my-new-feature`)
   1. Commit your changes (`git commit -am 'Add some feature'`)
   1. Push to the branch (`git push origin my-new-feature`)
1. Create a [GitHub Pull
   Request](https://help.github.com/articles/about-pull-requests/) for your
   change, following all [pull request
   requirements](#pull-request-requirements) and any instructions in the pull
   request template
1. Participate in a [Code Review](#code-review-process) with the project
   maintainers on the pull request

### Pull Request Requirements

Steamdeckdocs strives to ensure high quality for the project. In order to
promote this, we require that all pull requests to meet these specifications:

* **Green CI Tests:** We use [GitHub
  Actions](https://github.com/tuxx/steamdeckdocs/actions) to test all pull
  requests. We require these test runs to succeed on every pull request before
  being merged.

### Code Review Process

Code review takes place in GitHub pull requests. See [this
article](https://help.github.com/articles/about-pull-requests/) if you're not
familiar with GitHub Pull Requests.

Once you open a pull request, project maintainers will review your code and
respond to your pull request with any feedback they might have. The process at
this point is as follows:

1. A review is required from at least one of the project maintainers.
1. Your change will be merged into the project's `master` branch, and all
   [commits will be
   squashed](https://help.github.com/en/articles/about-pull-request-merges#squash-and-merge-your-pull-request-commits)
   during the merge.
