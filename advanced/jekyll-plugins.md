# Jekyll plugins

One main reason we chose to build this template on top of Jekyll is that it is probably the most heavily adopted static site generation tool. A benefit of that is that there is a large ecosystem of plugins to choose from for additional functionality.

If there already exists a Jekyll plugin to achieve a feature (properly and reliably), we elect to not build it into the template.

## Pre-installed

These plugins are so useful that we've chosen to bundle them in the template by default. Some of the features in the template rely on these plugins, and these docs assumed they are installed.

<table><thead><tr><th width="224">Plugin</th><th>Description</th></tr></thead><tbody><tr><td><a href="https://github.com/jeffreytse/jekyll-spaceship">jekyll-spaceship</a></td><td>A Jekyll "Swiss Army Knife". Provides support for table, mathjax, plantuml, mermaid, emoji, video, audio, youtube, vimeo, dailymotion, soundcloud, spotify, etc. See its docs for more info.</td></tr><tr><td><a href="https://github.com/gjtorikian/html-proofer">html-proofer</a></td><td>Not a Jekyll-specific plugin, but very useful. Checks for broken links, images, and more. It is <strong>installed</strong> by default, but not <strong>enabled</strong> by default. <a href="../basics/configure-your-site.md">See how to enable it</a>.</td></tr><tr><td><a href="https://github.com/jekyll/jekyll-sitemap">jekyll-sitemap</a></td><td>Generates a sitemap file and puts it in your website (hidden) for search engines to see.</td></tr><tr><td><a href="https://github.com/jekyll/jekyll-redirect-from">jekyll-redirect-from</a></td><td>Allows you to add a <code>redirect_from</code> field to a page's front matter. When a user visits one of the URLs listed, they'll be redirected to the page instead.</td></tr><tr><td><a href="https://github.com/jekyll/jekyll-feed">jekyll-feed</a></td><td>Generates an RSS-like feed of your blog posts and puts it in your website (hidden) for RSS tools to see.</td></tr><tr><td><a href="https://github.com/gjtorikian/jekyll-last-modified-at">jekyll-last-modified-at</a></td><td>Allows you to access the last time a file on your site was changed.</td></tr></tbody></table>

Usage of each of these plugins is either passive, or documented on another page where appropriate.

## Others

These plugins will be very useful to some, but weren't or couldn't be included in the template for various reasons.

<table><thead><tr><th width="225">Plugin</th><th>Description</th></tr></thead><tbody><tr><td><a href="https://github.com/kurtsson/jekyll-multiple-languages-plugin">jekyll-multiple-languages-plugin</a></td><td>Allows authoring you site content in multiple languages. Very valuable, but a very involved setup and effort.</td></tr><tr><td><a href="https://github.com/inukshuk/jekyll-scholar">jekyll-scholar</a></td><td>An alternative or supplement to the <a href="../basics/citations.md">built-in citation capabilities of the template</a>.</td></tr><tr><td><a href="https://github.com/jekyll/github-metadata">jekyll-github-metadata</a></td><td>Populates site-wide fields like title and description from your GitHub repo if not set.</td></tr><tr><td><a href="https://github.com/jekyll/jekyll-avatar">jekyll-avatar</a></td><td>Imports a GitHub avatar image from a user name, which you can size and style as you wish.</td></tr><tr><td><a href="https://github.com/jekyll/jekyll-gist">jekyll-gist</a></td><td>Imports a GitHub Gist and displays its text.</td></tr></tbody></table>

To install a plugin, follow [the instructions here](https://jekyllrb.com/docs/plugins/installation/). In summary:

1. Add `- jekyll-some-plugin` under `plugins:` in your `_config.yaml` file.
2. Add `gem "jekyll-some-plugin"` under `group :jekyll_plugins do` in your `Gemfile` file.
