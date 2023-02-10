# Is this right for me?

Not every tool is right for every person or team. This template is built on the following major assumptions:

* Using a [text/code editor](https://code.visualstudio.com/) (not a [GUI editor](https://en.wikipedia.org/wiki/WYSIWYG)) to author content in [Markdown](https://www.google.com/search?q=markdown).
* Using [Git](https://www.google.com/search?q=git) and repositories to store and change your code and content.
* Using [GitHub](https://github.com/) (the web interface, pull requests, [Actions](https://github.com/features/actions), etc.) as the main workflow for working on your website.
* Using [GitHub Pages](https://www.google.com/search?q=github+pages) for hosting your website.
* Using [Jekyll](https://jekyllrb.com/) as a [static site generator](https://www.google.com/search?q=static+site+generator).

If you're not comfortable with or at least familiar with the above, this template may not be right for you. If you want to learn more, see this [crash course on the tech used in this template](../advanced/background-knowledge.md).

{% hint style="warning" %}
The GitHub Pages hosting service is free, but _only for public repos_. If you want the source code of your website to be private, [you'll have to pay for it](https://docs.github.com/en/enterprise-cloud@latest/pages/getting-started-with-github-pages/changing-the-visibility-of-your-github-pages-site).
{% endhint %}

## Alternatives

There are other tools available to make your lab website. Here are some of them to investigate:

### GUI-based (no code)

* [Wowchemy](https://wowchemy.com/) and [wowchemy/starter-hugo-academic](https://github.com/wowchemy/starter-hugo-academic)
* [Squarespace](https://www.squarespace.com/)
* [Wix](https://www.wix.com/)
* [Webflow](https://webflow.com/)

| ✔️ Pros of GUI-based                                        | ❌ Cons GUI-based                                                                         |
| ----------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| Easy to learn. No special knowledge needed.                 | Customizable, but only to an extent. No bespoke functionality, like automatic citations! |
| Quick and convenient to edit. WYSIWYG in-browser editors.   | Usually not free.                                                                        |
| Integrated services like domain names and customer support. | Harder to track revisions, authorship, reviews, collaboration, issues, etc.              |

### Code-based

* [alshedivat/al-folio](https://github.com/alshedivat/al-folio)
* [academicpages/academicpages.github.io](https://github.com/academicpages/academicpages.github.io)
* [photonlines/Research-Lab-Website](https://github.com/photonlines/Research-Lab-Website)

| ✔️ Pros of code-based                                                                             | ❌ Cons of code-based                                                                                    |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| Offer 100% control and flexibility, with coding knowledge.                                        | Harder to learn. [Special knowledge](is-this-right-for-me.md) required.                                 |
| Git and GitHub benefits. Easily track revisions, authorship, reviews, collaboration, issues, etc. | Less convenient to edit. Need to make changes in a text/code-based way. Feedback less immediate/direct. |
| Open source and free. Maintainers more receptive to changes and new features.                     | Harder to setup and troubleshoot.                                                                       |

## Comparison with other code-based solutions

The main benefit of this template is its [automatic citations](../how-tos/citations.md) from _just simple identifiers_. Other academic templates allow you to enter in a full bibliography manually, but this template is unique in that it uses [Manubot](https://manubot.org/) to fill in as many details as possible _automatically_. You can provide just a publication id, and get everything else filled in for you. You can even enter in an author id and get a list of publications. If you only need a few citations, this isn't a big difference, but if you have [hundreds](https://greenelab.com/), this can be an enormous time saver.

There are things that other academic templates have that are not included in this template, but we are constantly assessing these differences and looking for ways we can improve. Ideally, the template will eventually be able to do most or everything that the other templates do, and more.

Notably we are working to make sure site layout, theming/styling, components, and interactive features are all comprehensive and flexible.

{% hint style="success" %}
If you feel something is missing from the template, please don't hesitate to [ask for it](support.md). We are very receptive to feature requests and other community feedback!&#x20;
{% endhint %}
