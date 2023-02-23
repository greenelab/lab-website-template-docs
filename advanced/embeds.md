# Embeds

The template is extendable with regular web-based plugins and libraries. If you find a library that is based on HTML/CSS/JS, you can probably use it in the template.

* Twitter timeline
* JavaScript calendar library
* JavaScript image carousel library
* [GitHub stats cards](https://github.com/anuraghazra/github-readme-stats)

## Comments section

Having comments on blog posts (or elsewhere) isn't a trivial feature to implement. There needs to be 1) a plugin on the page that lets users log in, read comments, and post new ones, and 2) a server running to receive, permanently store, and retrieve comments.

There are many services that offer this:

* [Disqus](https://disqus.com/)
* [Facebook Comments](https://developers.facebook.com/docs/plugins/comments/)
* [Hyvor Talk](https://talk.hyvor.com/)
* [Staticman](https://staticman.net/docs/)
* [Schnack](https://github.com/schn4ck/schnack)
* [Remark42](https://github.com/umputun/remark42)
* [Isso](https://github.com/posativ/isso)

...[to name a few](https://www.google.com/search?q=jekyll+comments). The decision is complex and [sometimes perilous](https://replyable.com/2017/03/disqus-is-your-data-worth-trading-for-convenience/), so we've elected to let you research the options carefully and not pre-package an opinionated choice in the template.

Some are full services that take care of the plugin and server for you. Usually for these, you just create an account the paste the code snippet they give you anywhere you want a comment section to appear, e.g. at the bottom of [`/_layouts/post.html`](https://github.com/greenelab/lab-website-template/blob/main/\_layouts/post.html). If the code snippet requires a unique page identifier, use `{{ page.url | absolute_url }}`.

Others just give you a plugin and the tools you need to run your own server, giving you greater privacy and security, but requiring more work to set up.
