---
description: Optional cleanup
---

# Tidy up your repo

The following is recommended to provide the cleanest experience for the maintainers and editors of your site. Much of this is just disabling unneeded features that GitHub enables by default to declutter the web interface.

* On the main page of your repo, click the ⚙️ next to "About".
  * Enter a short description, like "Source code for \[YOUR LAB] website".
  * Enter the link to your homepage, so people see it right at the top. Check your readme; it should've been automatically updated when you set up your URL!
  * Uncheck all boxes under "Include in the homepage". You likely don't need releases, packages, etc.
* In your repo's "⚙️ Settings":
  * Uncheck "template repository" so people don't accidentally use your copy of the template instead of the template itself.
  * Uncheck "Wikis", "Discussions", and "Projects". You likely don't need these.

## Add rules

We can't provide a deep-dive into all the features GitHub offers, but here are some things you may also consider setting up at this point:

* [Add branch protection rules](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/managing-a-branch-protection-rule) for `main` to prevent people committing directly to `main` and to require reviews and passing checks before merging pull requests.
* [Choose your collaborators](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository) (who has permissions to view, write, change settings, etc.).
* [Automatically delete pull request branches after merge](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/managing-the-automatic-deletion-of-branches) to prevent build-up of irrelevant branches in your repo.
* Disable all [pull request merge strategies](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/configuring-commit-squashing-for-pull-requests) except for squash merging to keep your `main` branch's commit history clean (opinionated).

