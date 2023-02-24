# Jekyll plugins

One main reason we chose to build this template on top of Jekyll is that it is probably the most heavily adopted static site generation tool. A benefit of that is that there is a large ecosystem of plugins to choose from for additional functionality.

If there already exists a Jekyll plugin to achieve a feature (properly and reliably), we elect to not build it into the template.

## Pre-installed

These plugins are so useful that we've chosen to bundle them in the template by default. Some of the features in the template rely on these plugins, and these docs assumed they are installed.

| Plugin                                                                           | Description                                                                                                                                                                                  |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [jekyll-spaceship](https://github.com/jeffreytse/jekyll-spaceship)               | A Jekyll "Swiss Army Knife". Provides support for table, mathjax, plantuml, mermaid, emoji, video, audio, youtube, vimeo, dailymotion, soundcloud, spotify, etc. See its docs for more info. |
| [jekyll-sitemap](https://github.com/jekyll/jekyll-sitemap)                       | Generates a sitemap file and puts it in your website (hidden) for search engines to see.                                                                                                     |
| [jekyll-redirect-from](https://github.com/jekyll/jekyll-redirect-from)           | Allows you to add a `redirect_from` field to a page's front matter. When a user visits one of the URLs listed, they'll be redirected to the page instead.                                    |
| [jekyll-feed](https://github.com/jekyll/jekyll-feed)                             | Generates an RSS-like feed of your blog posts and puts it in your website (hidden) for RSS tools to see.                                                                                     |
| [jekyll-last-modified-at](https://github.com/gjtorikian/jekyll-last-modified-at) | Allows you to access the last time a file on your site was changed.                                                                                                                          |

Usage of each of these plugins is either passive, or documented on another page where appropriate.

## Others

These plugins will be very useful to some, but weren't or couldn't be included in the template for various reasons.

| Plugin                                                                                           | Description                                                                                                   |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- |
| [jekyll-multiple-languages-plugin](https://github.com/kurtsson/jekyll-multiple-languages-plugin) | Allows authoring you site content in multiple languages. Very valuable, but a very involved setup and effort. |
| [jekyll-scholar](https://github.com/inukshuk/jekyll-scholar)                                     | An alternative or supplement to the [built-in citation capabilities of the template](../basics/citations.md). |
| [jekyll-github-metadata](https://github.com/jekyll/github-metadata)                              | Populates site-wide fields like title and description from your GitHub repo if not set.                       |
| [jekyll-avatar](https://github.com/jekyll/jekyll-avatar)                                         | Imports a GitHub avatar image from a user name, which you can size and style as you wish.                     |
| [jekyll-gist](https://github.com/jekyll/jekyll-gist)                                             | Imports a GitHub Gist and displays its text.                                                                  |

To install a plugin, follow [the instructions here](https://jekyllrb.com/docs/plugins/installation/). In summary:

1. Add `- jekyll-some-plugin` under `plugins:` in your `_config.yaml` file.
2. Add `gem "jekyll-some-plugin"` under `group :jekyll_plugins do` in your `Gemfile` file.
