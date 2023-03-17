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

| User content                                                                                                                | Template content                                                                                                                                                                        |
| --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><code>/_data</code></p><p><code>/_members</code></p><p><code>/_posts</code></p><p><code>/_styles/-theme.scss</code></p>  | <p>Folders that start with <code>_</code><br><span data-gb-custom-inline data-tag="emoji" data-code="1f448">👈</span> ...except these</p>                                               |
| <p>Folders that start with letters, like...<br><code>/blog</code><br><code>/images</code><br><code>/team</code><br>etc.</p> | Folders that start with `.`                                                                                                                                                             |
| <p><code>_config.yaml</code> (top)<br><code>404.md</code><br><code>index.md</code><br><code>README.md</code></p>            | <p><code>_config.yaml</code> (bottom)<br><code>.gitignore</code><br><code>CITATION.cff</code></p><p><code>Gemfile</code></p><p><code>Gemfile.lock</code><br><code>LICENSE.md</code></p> |

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

| Folder or file                                                                       | Description                                                                                                                                                                                                                                                                                                                    |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `/_cite`                                                                             | Python code, plugins, and cache that perform the [cite process](citations.md).                                                                                                                                                                                                                                                 |
| <p><code>/_data</code><br><code>/_members</code><br><code>/_posts</code></p>         | [Data and collections for large lists of items](../advanced/data-and-collections.md) on your site for things like your team and blog.                                                                                                                                                                                          |
| `/_includes`                                                                         | Reusable, small snippets of code that can take parameters. This is where the code for [components](components/) are, if you need to modify them.                                                                                                                                                                               |
| `/_layouts`                                                                          | The HTML templates that all pages are built upon. `default.html` is the default layout for all pages, and should never really be edited. Team member pages and blog post pages have their own layouts in `member.html` and `post.html`, which inherit from `default.html`, and can be edited to add/remove/rearrange sections. |
| `/_plugins`                                                                          | Special Ruby files that extend the functionality of Jekyll and Liquid. These are essentially custom Jekyll plugins, where no [existing plugins](../advanced/jekyll-plugins.md) could be found.                                                                                                                                 |
| `/_scripts`                                                                          | Script files that add interactive features to the website like search, GitHub tag import, tooltips, etc. These scripts have some configuration options, but edit with care. Any JavaScript file you add here will automatically be included in your site.                                                                      |
| `/_site`                                                                             | The "compiled" output from Jekyll, i.e. the actual content that gets published as your live site. You'll only see this if you've built/previewed your site locally. Changes to it will get overwritten every time the site is rebuilt, so don't edit it directly.                                                              |
| `/_styles`                                                                           | Style files that determine how the site and [components](components/) look. Any Sass or CSS files you add here will automatically be included in your site. Sass files must contain a [front matter](edit-pages.md#edit-page-details) to be processed by Jekyll.                                                               |
| `/.docker`                                                                           | Files needed for [previewing your site locally](../getting-started/preview-your-site.md#on-your-computer-locally).                                                                                                                                                                                                             |
| `/.github`                                                                           | Files related to GitHub, mostly Actions workflows that perform automated tasks when you make changes to your repo.                                                                                                                                                                                                             |
| <p><code>/blog</code><br><code>/contact</code><br><code>/research</code><br>etc.</p> | The [pages](edit-pages.md) of your site.                                                                                                                                                                                                                                                                                       |
| `/images`                                                                            | The default folder for your site's [images](repo-structure.md#images-and-other-assets).                                                                                                                                                                                                                                        |
| `_config.yaml`                                                                       | [Basic settings and configuration for your site](configure-your-site.md), along with some advanced Jekyll settings.                                                                                                                                                                                                            |
| `.gitignore`                                                                         | Files to not be tracked/included in your site's repo.                                                                                                                                                                                                                                                                          |
| `404.md`                                                                             | When a visitor goes to a page on your site that doesn't exist, this page gets loaded instead.                                                                                                                                                                                                                                  |
| <p><code>citation.cff</code><br><code>LICENSE.md</code></p>                          | Metadata about the template itself.                                                                                                                                                                                                                                                                                            |
| <p><code>Gemfile</code><br><code>Gemfile.lock</code></p>                             | Files that specify Ruby package dependencies for Jekyll and its plugins.                                                                                                                                                                                                                                                       |
| `index.md`                                                                           | The homepage of your site!                                                                                                                                                                                                                                                                                                     |
| `README.md`                                                                          | What people see when they go to your repo on GitHub.                                                                                                                                                                                                                                                                           |
