# Edit your site

There are two main ways you can edit your site, each with benefits and limitations: on GitHub and on your computer. Choose which one best suits you, or you can mix and match as appropriate.

{% hint style="info" %}
For most content on your site, you just need change the contents of the appropriate file.

Citations have a special additional step. When you add new sources or authors to be cited, the template has to [run a special process to generate your full citations](../how-tos/citations.md). We call this process "automatic citations".
{% endhint %}

## On GitHub (remotely)

This is the easiest and most convenient method to edit your site. GitHub has a very nice and always-improving web interface. If you wanted to, you could edit and manage your site entirely from the GitHub website.

#### Editing

There is a [basic interface](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files) for changing single files at a time, and [a more advanced interface](https://docs.github.com/en/codespaces/the-githubdev-web-based-editor) with multiple files, syntax highlighting, sophisticated controls, etc. Use one of these interfaces to make the changes you want, then either commit directly to your `main` branch (to publish your changes immediately) or create a new branch and pull request (to preview your changes before publishing them).

#### Previewing

In pull requests, the template will build a live preview of the changes you are making to your site. A public link to the preview will be in a comment on the pull request. This way, reviewers and editors can see the tangible result of the changes conveniently.

#### Citations

For your convenience, the template tells GitHub to run the automatic citation process and commit the result whenever you push to `main` or make a pull request.

{% hint style="danger" %}
If you are making changes from a fork of your main website repo, the automatic citation process unfortunately won't work due to GitHub security limitations. We recommend making changes from a branch on the main repo instead, or running the automatic citation process locally.
{% endhint %}

## On your computer (locally)

This approach requires experience with Git, but is better for when you're doing larger edits, when you want to work on your changes privately before pushing them, and when you want to iterate rapidly and not wait for pull request previews to update.

#### Editing

[Make changes with Git](https://www.google.com/search?q=git+basics). In summary:

1. Decide how you'll be making changes:
   1. Make changes directly to the `main` branch of your website repo (_publishes changes immediately_).
   2. Make changes to a branch (e.g. `add-sarah-bio`) of your website repo (_allows previewing changes before publishing_).
   3. Make changes to a fork of your website repo (_allows previewing changes before publishing_).
2. [Clone](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/cloning-a-repository) the appropriate repo to your computer and switch to the appropriate branch.
3. Edit the cloned site on your computer with your favorite [text/code editor](https://code.visualstudio.com/).
4. Commit and push the changes.
5. If working from a branch, make a pull request to your main website repo and merge when ready to publish.

#### Previewing

1. Install Docker...

Running this preview also runs the automatic citation process.

{% hint style="info" %}
Building your site is (surprisingly) not deterministic, because some of the pre-installed [Jekyll plugins](../advanced/jekyll-plugins.md) always add the date-time when the site was built, regardless of whether any content changed. Be aware of this when building locally, or if tampering with the built-in GitHub Actions workflows.
{% endhint %}
