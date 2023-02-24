---
description: How to add, remove, and edit details of pages on your site
---

# Edit pages

## Add/remove pages

The pages and sub-pages on your site [come from the folder and file structure of your repo](https://jekyllrb.com/docs/structure/).

Examples:

| Type     | URL you want             | Folders and files to create |
| -------- | ------------------------ | --------------------------- |
| Homepage | `yoursite.com/`          | `index.md`                  |
| Page     | `yoursite.com/awards`    | `/awards/index.md`          |
| Sub-page | `yoursite.com/team/join` | `/team/join/index.md`       |

To add or remove a page, simply create or delete the corresponding folder and Markdown file in your repo.

The pages that come with this template – `/blog`, `/contact`, etc. – can be freely removed or renamed at your discretion.

{% hint style="info" %}
"Index" is a [naming convention](https://stackoverflow.com/questions/32408259/why-do-people-name-their-files-index-html) for referring to the "default" page of a particular folder. Navigating to `yoursite.com/awards` would actually load `yoursite.com/awards/index.html` (generated from `/awards/index.md`).
{% endhint %}

## **Edit page details**

Markdown files can have a section at the top called a "[front matter](https://assemble.io/docs/YAML-front-matter.html)" to hold metadata about the page in YAML format. This is how you can pass special per-page details to the template.

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

| Parameter                     | Description                                                                                                                                                       | Default                                                 |
| ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------- |
| `title`                       | Title of the page. Shown in the tab name along with your [site title](configure-your-site.md), e.g. "Awards \| Your Lab Website"                                  |                                                         |
| `description`                 | Description of the page that will show under search engine results.                                                                                               | [Site-wide description](configure-your-site.md)         |
| `nav`                         | If this field is present, the page will appear in the header navigation bar, with the same name as the page's title.                                              |                                                         |
| `nav` -> `order`              | How the page should be ordered in the nav bar. Number value, lowest to highest -> left to right.                                                                  |                                                         |
| `nav` -> `tooltip`            | Text to show when hovering over the page's nav bar link.                                                                                                          |                                                         |
| `header`/`footer`             | Background image for the header/footer of the page.                                                                                                               | [Site-wide header/footer image](configure-your-site.md) |
| `header-dark` / `footer-dark` | Header/footer dark/light mode of the page. Headers/footers/sections have a solid color that overlays any background image to always maintain readability of text. | [Site-wide header/footer mode](configure-your-site.md)  |
| `redirect_from`               | When a user visits one of the URLs listed, they'll be redirected to this page instead.                                                                            |                                                         |

{% hint style="info" %}
If you have a `.md` file without a front matter, Jekyll will ignore it and not convert it to an `.html` file, and thus it won't end up in your site. If you don't need any page details, just leave the two lines of `---` with nothing in between.
{% endhint %}
