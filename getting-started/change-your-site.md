# Change your site

There are two main ways you can save changes to your site: **on GitHub** and **on your computer**. Choose which one best suits you, or you can mix and match as appropriate.

Since the template is [based on Git](../introduction/is-this-right-for-me.md), this page really just describes the different ways to make Git changes (commits).

## On GitHub (remotely)

This is the easiest and most convenient method to edit your site. GitHub has a very nice and always-improving graphical web interface. If you wanted to, you could edit and manage your site entirely from the GitHub website.

There is a [basic interface](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files) for changing single files at a time, and [more advanced interfaces](https://docs.github.com/en/codespaces/the-githubdev-web-based-editor) with multiple files, syntax highlighting, sophisticated controls, etc. Use one of these interfaces to make the changes you want, then either commit directly to your `main` branch (to publish your changes immediately) or create a new branch and pull request (to preview/review your changes before publishing them).

## On your computer (locally)

This approach requires experience with Git and using command-line interfaces, but is better for when you're doing larger edits, when you want to work on your changes privately before pushing them, and when you want to iterate rapidly and not wait for pull request previews to update.

[Make changes with Git](https://www.google.com/search?q=git+basics) on your command line. In summary:

1. Decide how you'll be making changes:
   1. Make changes directly to the `main` branch of your website repo (_publishes changes immediately_).
   2. Make changes to a branch (e.g. `add-sarah-bio`) of your website repo (_allows previewing changes before publishing_).
   3. Make changes to a fork of your website repo (_allows previewing changes before publishing_).
2. [Clone](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/cloning-a-repository) the appropriate repo to your computer and switch to the appropriate branch.
3. Edit the cloned site on your computer with your favorite [text/code editor](https://code.visualstudio.com/).
4. Commit and push the changes.
5. If working from a branch or fork, make a pull request to your main website repo and merge when ready to publish.
