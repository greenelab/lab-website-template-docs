# Preview your site

When you want to make changes to your website, you'll likely want a convenient way to preview and review the changes before publishing them.&#x20;

Just like [editing your site](change-your-site.md), there are two ways to preview your site: **on GitHub** and **on your computer**.

## On GitHub (remotely)

When you open or update a pull request on GitHub, the template will build a live preview of the changes you are making to your site. A public link to the preview will be in a comment on the pull request. This way, reviewers and editors can see the tangible result of the changes conveniently.

{% hint style="info" %}
Note: The comment on the PR will appear a little bit before (\~30 seconds) the the preview is actually finished deploying. Keep that in mind if you click on the link and see a 404 error or non-updated website.
{% endhint %}

The template will also tell GitHub to automatically run the [cite process](../basics/citations.md) and commit the resulting citations. This happens whenever you push to `main` or make a pull request.

If you're doing a pull request from a fork, make sure "[Allow edits from maintainers](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/allowing-changes-to-a-pull-request-branch-created-from-a-fork)" is checked in your pull request _before you open it_ so the cite process has permission to commit its results.

{% hint style="warning" %}
Due to an [unfortunate GitHub limitation](https://github.com/orgs/community/discussions/5634), if you're making changes from a fork under an _organization_, you wont see the "allow edits" option and the cite process wont work. You'll have to make changes from a branch instead, or run the cite process locally.
{% endhint %}

## On your computer (locally)

1. Install [Docker Desktop](https://www.docker.com/products/docker-desktop/) (recommended) or just [Docker](https://docs.docker.com/get-docker/) and start it.
2. Run `./.docker/run.sh`.
3. Wait for Docker to build a sandbox with all the languages and packages the template needs. Should take \~2 min the first time and be almost instant on subsequent runs.
4. Wait for Docker to start the preview. You should shortly get a `localhost` link that you can open in your browser to see your site preview.
5. When you make a change to a file in your repo folder, your preview should refresh/update automatically, except for changes to `_config.yaml` which require you to manually refresh.
6. When you make a change to your sources or metasources, the [cite process](../basics/citations.md) should automatically re-run, and when finished be reflected in your preview via the same behavior as above.

<details>

<summary>Non-Docker instructions</summary>

We made Docker the recommended approach for local previewing for a few reasons:

* You only need to install one thing
* You only need to remember and run a single command for both the site building and cite process.
* Everything installs properly and works consistently on any operating system, something that Jekyll/Ruby make very difficult, [especially on Windows](https://github.com/oneclick/rubyinstaller2/issues/96).

If you find the Docker approach to be too heavy, and if you can reliably run Ruby and Python on your system, you can locally preview your site using the manual, low-level approach:

Build site:

1. [Install Ruby](https://www.ruby-lang.org/en/documentation/installation/) v3+ (on Windows, use the [installer](https://rubyinstaller.org/downloads/) and the recommended version with the Devkit).
2. [Install Bundler](https://bundler.io/) by running `gem install bundler`.
3. Install needed Ruby packages by running `bundle install`.
4. Re-run the previous command if you ever add new [plugins](../advanced/jekyll-plugins.md).
5. Start the site by running `bundle exec jekyll serve --open-url --livereload --trace`.
6. Re-run the previous command if you make changes to `_config.yaml`.

Run [cite process](../basics/citations.md):

1. [Install Python 3](https://www.python.org/downloads/) (with PIP).
2. Install needed Python packages by running `python -m pip install --upgrade --requirement ./_cite/requirements.txt`.
3. Generate citations by running `python ./_cite/cite.py`.
4. Re-run the previous command when you make changes to your input sources and metasources.

</details>
