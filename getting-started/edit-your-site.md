# Edit your site

There are two main ways you can make changes to your site, each with benefits and limitations: on GitHub and on your computer. Choose which one best suits you, or you can mix and match as appropriate.

{% hint style="info" %}
For most content on your site, you just need change the contents of the appropriate file.

Citations have a special additional step. When you add new sources or metasources (authors) to be cited, the template has to [run a special process to generate your full citations](../basics/citations.md).
{% endhint %}

## On GitHub (remotely)

This is the easiest and most convenient method to edit your site. GitHub has a very nice and always-improving web interface. If you wanted to, you could edit and manage your site entirely from the GitHub website.

### Editing

There is a [basic interface](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files) for changing single files at a time, and [a more advanced interface](https://docs.github.com/en/codespaces/the-githubdev-web-based-editor) with multiple files, syntax highlighting, sophisticated controls, etc. Use one of these interfaces to make the changes you want, then either commit directly to your `main` branch (to publish your changes immediately) or create a new branch and pull request (to preview your changes before publishing them).

### Previewing

In pull requests, the template will build a live preview of the changes you are making to your site. A public link to the preview will be in a comment on the pull request. This way, reviewers and editors can see the tangible result of the changes conveniently.

### Citations

For your convenience, the template tells GitHub to run the [cite process](edit-your-site.md#citations) and commit the result whenever you push to `main` or make a pull request.

If you're doing a pull request from a fork, make sure "[Allow edits from maintainers](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/allowing-changes-to-a-pull-request-branch-created-from-a-fork)" is checked in your pull request so the cite process has permission to commit its results.

{% hint style="warning" %}
Due to an [unfortunate GitHub limitation](https://github.com/orgs/community/discussions/5634), if you're making changes from a fork under an _organization_, you wont see the "allow edits" option and the cite process wont work. You'll have to make changes from a branch instead, or run the cite process locally.
{% endhint %}

## On your computer (locally)

This approach requires experience with Git, but is better for when you're doing larger edits, when you want to work on your changes privately before pushing them, and when you want to iterate rapidly and not wait for pull request previews to update.

### Editing

[Make changes with Git](https://www.google.com/search?q=git+basics). In summary:

1. Decide how you'll be making changes:
   1. Make changes directly to the `main` branch of your website repo (_publishes changes immediately_).
   2. Make changes to a branch (e.g. `add-sarah-bio`) of your website repo (_allows previewing changes before publishing_).
   3. Make changes to a fork of your website repo (_allows previewing changes before publishing_).
2. [Clone](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/cloning-a-repository) the appropriate repo to your computer and switch to the appropriate branch.
3. Edit the cloned site on your computer with your favorite [text/code editor](https://code.visualstudio.com/).
4. Commit and push the changes.
5. If working from a branch or fork, make a pull request to your main website repo and merge when ready to publish.

### Previewing

To build a preview of your site locally:

1. [Install Ruby](https://www.ruby-lang.org/en/documentation/installation/) v3+ (on Windows, use the [installer](https://rubyinstaller.org/downloads/) and the recommended version with the Devkit).
2. [Install Bundler](https://bundler.io/) by running `gem install bundler`.
3. [Install Jekyll](https://jekyllrb.com/) by running `gem install jekyll`.
4. Go to the folder where you cloned your site, e.g. `cd your-lab-website`.
5. Bundle the site by running `bundle`.
6. Start the site by running `bundle exec jekyll serve --open-url --livereload --trace`

Your site should automatically open in a browser, and any changes you make should automatically rebuild the site and refresh the page, except for changes to `_config.yaml` which require re-running the start command.

{% hint style="warning" %}
Unfortunately, the `livereload` feature is difficult to get working on Windows. You can either remove the flag from the start command, or [see this thread](https://github.com/oneclick/rubyinstaller2/issues/96) to find solutions.
{% endhint %}

{% hint style="info" %}
Building your site is (surprisingly) not deterministic, because some of the pre-installed [Jekyll plugins](../advanced/jekyll-plugins.md) always add the date-time when the site was built, regardless of whether any content changed. Be aware of this when building locally, or if tampering with the built-in GitHub Actions workflows.
{% endhint %}

### Citations

To run the [cite process](../basics/citations.md) locally:

1. [Install Python](https://www.python.org/downloads/) (with PIP).
2. Go to the folder where you cloned your site, e.g. `cd your-lab-website`.
3. Install needed Python packages by running `python -m pip install --upgrade --requirement ./_cite/requirements.txt`.
4. Add or change the desired sources/papers in `/_data/sources.yaml`.
5. Generate citations by running `python ./_cite/cite.py`.

Citations should be automatically generated and output to `/_data/citations.yaml`.
