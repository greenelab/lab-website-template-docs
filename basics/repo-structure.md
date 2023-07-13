---
description: A brief explanation of the folders and files in the template
---

# Repo structure

{% hint style="info" %}
Most of this structure is enforced by Jekyll. See [this page of the Jekyll documentation](https://jekyllrb.com/docs/structure/) more thorough explanation of some of the items here.
{% endhint %}

## Template vs. user content

The most important distinction to make is between **template content** ("under-the-hood") and **user content** (for your specific website).

**In general**, here's how the files and folders in the template fall into these two categories. We've tried to keep these as separated as possible, within the limitations of Jekyll.

<table><thead><tr><th width="107.33333333333331"></th><th width="306">User content</th><th>Template content</th></tr></thead><tbody><tr><td><strong>Folders</strong></td><td><p><code>/blog</code><br><code>/images</code><br><code>/team</code><br>etc. (starting with letters)<br><br><code>/_data</code></p><p><code>/_members</code></p><p><code>/_posts</code><br>(<code>_</code> exceptions)</p></td><td><p><code>.github</code></p><p><code>.docker</code></p><p>etc. (starting with <code>.</code>)</p><p><br><code>_cite</code></p><p><code>_includes</code></p><p><code>_plugins</code></p><p>etc. (starting with <code>_</code>, except a few 👈)</p></td></tr><tr><td><strong>Files</strong></td><td><p><code>_config.yaml</code> (top portion of file)</p><p><code>/_styles/-theme.scss</code><br><code>404.md</code><br><code>index.md</code><br><code>README.md</code></p></td><td><p><code>_config.yaml</code> (bottom portion of file)<br><code>.gitignore</code><br><code>CITATION.cff</code></p><p><code>Gemfile</code></p><p><code>Gemfile.lock</code><br><code>LICENSE.md</code></p></td></tr></tbody></table>

### Template repo only content

There are a few files and folders that are needed for the `lab-website-template` repo itself, but don't belong in your generated/forked repo at all:

* `CHANGELOG.md`
* `testbed.md`
* `.github/ISSUE_TEMPLATE`
* `.github/workflows/versioning.yaml`
* `.github/pull_request_template.md` (rename `user_pull_request_template.md` in its place)

Keeping these files in your repo wont break anything per se, but they do increase clutter and confusion. The [first time setup](../getting-started/set-up-your-site.md) process automatically removes and renames these for you, but when [updating your template version](../advanced/update-your-template.md) be sure not to accidentally re-add them to your repo.

## Images and other assets

The template comes with a default `/images` folder to hold all your site's images, but you can organize your images however you'd like. For example, you could put photos of your team in `/team/photos/` and just refer to them like `team/photos/anna-sun.jpg`.

You could also create `/videos` or any other folders you need for static assets and refer to them in the same way.

{% hint style="info" %}
The only exception to this is your [logo files](use-your-logo.md) and [fallback image](components/figure.md), which the template expects to be in `/images`.
{% endhint %}

## Data and components

The template comes with a few placeholder [data lists](../advanced/data-and-collections.md) and matching [components](components/) for common needs:

| Data/collection                                         | Matching component |
| ------------------------------------------------------- | ------------------ |
| [Citations](citations.md) (`/_data/citations.yaml`)     | `citation`         |
| [Projects](components/card.md) (`/_data/projects.yaml`) | `card`             |
| [Team members](team-members.md) (`/_members`)           | `portrait`         |
| [Blog posts](blog-posts.md) (`/_posts`)                 | `post-excerpt`     |

## Full accounting

A piece-by-piece breakdown of the folders and files in the template. You don't have to [understand the inner workings of all of this](../advanced/background-knowledge.md), but it helps to know generally what each piece is for.

<table><thead><tr><th width="189">Folder or file</th><th>Description</th></tr></thead><tbody><tr><td><code>/_cite</code></td><td>Python code, plugins, and cache that perform the <a href="citations.md">cite process</a>.</td></tr><tr><td><code>/_data</code><br><code>/_members</code><br><code>/_posts</code></td><td><a href="../advanced/data-and-collections.md">Data and collections for large lists of items</a> on your site for things like your team and blog.</td></tr><tr><td><code>/_includes</code></td><td>Reusable, small snippets of code that can take parameters. This is where the code for <a href="components/">components</a> are, if you need to modify them.</td></tr><tr><td><code>/_layouts</code></td><td>The HTML templates that all pages are built upon. <code>default.html</code> is the default layout for all pages, and should never really be edited. Team member pages and blog post pages have their own layouts in <code>member.html</code> and <code>post.html</code>, which inherit from <code>default.html</code>, and can be edited to add/remove/rearrange sections.</td></tr><tr><td><code>/_plugins</code></td><td>Special Ruby files that extend the functionality of Jekyll and Liquid. These are essentially custom Jekyll plugins, where no <a href="../advanced/jekyll-plugins.md">existing plugins</a> could be found.</td></tr><tr><td><code>/_scripts</code></td><td>Script files that add interactive features to the website like search, GitHub tag import, tooltips, etc. These scripts have some configuration options, but edit with care. Any JavaScript file you add here will automatically be included in your site.</td></tr><tr><td><code>/_site</code></td><td>The "compiled" output from Jekyll, i.e. the actual content that gets published as your live site. You'll only see this if you've built/previewed your site locally. Changes to it will get overwritten every time the site is rebuilt, so don't edit it directly.</td></tr><tr><td><code>/_styles</code></td><td>Style files that determine how the site and <a href="components/">components</a> look. Any Sass or CSS files you add here will automatically be included in your site. Sass files must contain a <a href="edit-pages.md#edit-page-details">front matter</a> to be processed by Jekyll.</td></tr><tr><td><code>/.docker</code></td><td>Files needed for <a href="../getting-started/preview-your-site.md#on-your-computer-locally">previewing your site locally</a>.</td></tr><tr><td><code>/.github</code></td><td>Files related to GitHub, mostly Actions workflows that perform automated tasks when you make changes to your repo.</td></tr><tr><td><code>/blog</code><br><code>/contact</code><br><code>/research</code><br>etc.</td><td>The <a href="edit-pages.md">pages</a> of your site.</td></tr><tr><td><code>/images</code></td><td>The default folder for your site's <a href="repo-structure.md#images-and-other-assets">images</a>.</td></tr><tr><td><code>_config.yaml</code></td><td><a href="configure-your-site.md">Basic settings and configuration for your site</a>, along with some advanced Jekyll settings.</td></tr><tr><td><code>.gitignore</code></td><td>Files to not be tracked/included in your site's repo.</td></tr><tr><td><code>404.md</code></td><td>When a visitor goes to a page on your site that doesn't exist, this page gets loaded instead.</td></tr><tr><td><code>citation.cff</code><br><code>LICENSE.md</code></td><td>Metadata about the template itself.</td></tr><tr><td><code>Gemfile</code><br><code>Gemfile.lock</code></td><td>Files that specify Ruby package dependencies for Jekyll and its plugins.</td></tr><tr><td><code>index.md</code></td><td>The homepage of your site!</td></tr><tr><td><code>README.md</code></td><td>What people see when they go to your repo on GitHub.</td></tr></tbody></table>
