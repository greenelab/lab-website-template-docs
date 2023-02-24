---
description: High-level primer of the tech used in the template (optional reading)
---

# Background knowledge

Here are some very basic explanations of terminology and technologies used in this template to help you interpret the rest of the documentation.

* A **repository** (or _repo_ for short) is a place to store code and other content for a project.
* [**Git**](https://try.github.io/) is a way of tracking and making changes to code and other content in repos, typically using a [command line](https://en.wikipedia.org/wiki/Command-line\_interface).
* [**GitHub**](https://github.com/) is an online place to store, view, track, share, and collaborate on code and other content in repos based around Git. You can make simple changes to your code on the GitHub website itself, but for other changes you'll need to use [Git](https://git-scm.com/) directly. [Here is a handy guide](https://guides.github.com/introduction/flow/) that explains the basics of how Git and GitHub are typically used together to effectively develop projects.
* [**GitHub Pages**](https://pages.github.com/) (or _gh-pages_ for short) is a service built-in to GitHub that can host a website for you, for free. No need to buy monthly hosting from GoDaddy! Put the source code for your website in a repo, turn on GitHub Pages, and the site will go live. Any changes you make to the code will update on the site automatically.
* [**GitHub Actions**](https://github.com/features/actions) (or _gh-actions_ for short) is a feature of GitHub that can (among other things) automatically run scripts and other actions when changes are made to a repo. Setting up GitHub Actions is only needed for certain specific tasks that aren't handled automatically by Jekyll or other parts of the template.
* [**YAML**](https://en.wikipedia.org/wiki/YAML) is a format for writing large structured sets/lists of data. The template uses this format as an easy way to input papers and resources for your site.
* [**HTML**](https://developer.mozilla.org/en-US/docs/Web/HTML) is how you write the main content of a web page. It tells the browser what to show, like paragraphs of text, tables of numbers, images with captions, etc.
* [**Markdown**](https://en.wikipedia.org/wiki/Markdown) is a easier way to write certain [basic text, formatting, and other things from HTML](https://commonmark.org/help/). But browsers can't display markdown directly; it has to be converted to HTML first.
* [**Jekyll**](https://jekyllrb.com/) is a tool that can automatically generate large HTML sites from much simpler markdown, and with less grunt work and code duplication, allowing you to just focus on the content. It does all this fancy work in a "pre-process" step. When you make a change, Jekyll compiles everything together into the final product which can then be viewed or uploaded. Jekyll is the main tool that makes this template possible.
* [**Liquid**](https://shopify.github.io/liquid/) is a [templating language](https://en.wikipedia.org/wiki/Template\_processor) built-in to Jekyll that allows you to insert repetitive chunks of content automatically and define logic for how your site is built by Jekyll. For example, you could provide Jekyll with a simple list of items, then use Liquid to sort them and [automatically](https://shopify.github.io/liquid/tags/iteration/) put each one in their own formatted table row.
* [**Sass**](https://sass-lang.com/) (a superset of [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)) is how you get a web page to look the way you want. You can set [positions, margins, colors, fonts, etc.](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Keyword\_index), and apply them to certain elements (tables, images, etc.) in the HTML with [selectors](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building\_blocks/Selectors). You only need to know this if you want to significantly change the way the template looks.
* [**Python**](https://www.python.org/) is a general-purpose programming language. You only need to know this if you want to modify the behavior of the [automatic citations](../basics/citations.md).
* [**JavaScript**](https://developer.mozilla.org/en-US/docs/Glossary/JavaScript) (or _js_ for short) is a programming language to make web pages more interactive. HTML is static/unchanging, but JavaScript allows the page to change dynamically as the user is viewing it. For example, JavaScript can be used to hide/show certain paragraphs in the HTML based on what the user types into a search box. You only need to know this if you want to modify the behavior of the template's interactive features.
* [**Ruby**](https://www.ruby-lang.org/en/) is a general-purpose programming language. You don't need to know Ruby to use this template, but you'll encounter a few [Ruby-related files](https://www.rubyguides.com/2018/09/ruby-gems-gemfiles-bundler/) in the template, because Jekyll is written in Ruby.

{% hint style="info" %}
**Remember:** A website ultimately consists of _only three things_: **HTML, CSS, and JavaScript** (and any asset files like images/videos/etc). These are the only things a browser can understand and execute, and they are what gets uploaded to publish your site. Any other technology is just an intermediate step to get to a final, "compiled" website consisting of just these three things.
{% endhint %}

