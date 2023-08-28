---
description: How to add, remove, and edit details of pages on your site
---

# Edit pages

## Add/remove pages

The pages and sub-pages on your site [come from the folder and file structure of your repo](https://jekyllrb.com/docs/structure/).

Examples:

<table><thead><tr><th width="139">Type</th><th width="267.3333333333333">URL you want</th><th>Folders and files to create</th></tr></thead><tbody><tr><td>Homepage</td><td><code>yoursite.com/</code></td><td><code>index.md</code></td></tr><tr><td>Page</td><td><code>yoursite.com/awards</code></td><td><code>/awards/index.md</code></td></tr><tr><td>Sub-page</td><td><code>yoursite.com/team/join</code></td><td><code>/team/join/index.md</code></td></tr></tbody></table>

To add or remove a page, simply create or delete the corresponding folder and Markdown file in your repo.

The pages that come with this template – `/blog`, `/contact`, etc. – can be freely removed or renamed at your discretion.

{% hint style="info" %}
"Index" is a [naming convention](https://stackoverflow.com/questions/32408259/why-do-people-name-their-files-index-html) for referring to the "default" page of a particular folder. Navigating to `yoursite.com/awards` would actually load `yoursite.com/awards/index.html` (generated from `/awards/index.md`).
{% endhint %}

## **Edit page details**

Markdown files can have a section at the top called a "front matter" to hold metadata about the page in YAML format. This is how you can pass special per-page details to the template.

Example `index.md` page file:

```markdown
---
title: Awards
description: Our lab has received international praise for our contributions to science.
nav:
  order: 1
  tooltip: Praise and laurels
header: images/header-for-this-page.jpg
footer: images/footer-for-this-page.jpg
header-dark: false
footer-dark: false
redirect_from:
  - accolades
---

Page content.
```

<table><thead><tr><th width="185">Parameter</th><th width="374.3333333333333">Description</th><th>Default</th></tr></thead><tbody><tr><td><code>title</code></td><td>Title of the page. Shown in the tab name along with your <a href="configure-your-site.md">site title</a>, e.g. "Awards | Your Lab Website"</td><td></td></tr><tr><td><code>description</code></td><td>Description of the page that will show under search engine results.</td><td><a href="configure-your-site.md">Site-wide description</a></td></tr><tr><td><code>nav</code></td><td>If this field is present, the page will appear in the header navigation bar, with the same name as the page's title.</td><td></td></tr><tr><td><code>nav</code> -> <code>order</code></td><td>How the page should be ordered in the nav bar. Number value, lowest to highest -> left to right.</td><td></td></tr><tr><td><code>nav</code> -> <code>tooltip</code></td><td>Text to show when hovering over the page's nav bar link.</td><td></td></tr><tr><td><code>header</code>/<code>footer</code></td><td>Background image for the header/footer of the page.</td><td><a href="configure-your-site.md">Site-wide header/footer image</a></td></tr><tr><td><code>header-dark</code> / <code>footer-dark</code></td><td>Header/footer dark/light mode of the page. </td><td><a href="configure-your-site.md">Site-wide header/footer mode</a></td></tr><tr><td><code>redirect_from</code></td><td>When a user visits one of the URLs listed, they'll be redirected to this page instead.</td><td></td></tr></tbody></table>

{% hint style="info" %}
Headers/footers/sections have a solid color that overlays any background image to always maintain readability of text.
{% endhint %}

{% hint style="info" %}
If you have a `.md` file without a front matter, Jekyll will ignore it and not convert it to an `.html` file, and thus it won't end up in your site. If you don't need any page details, just leave the two lines of `---` with nothing in between.
{% endhint %}
