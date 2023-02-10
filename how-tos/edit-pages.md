---
description: How to add, remove, and edit details of pages on your site
---

# Edit pages

## Add/remove pages

The pages and sub-pages on your site come from the folder and file structure of your repo. [This behavior comes from Jekyll](https://jekyllrb.com/docs/structure/).

Examples:

|          | URL you want             | Folders and files to create |
| -------- | ------------------------ | --------------------------- |
| Homepage | `yoursite.com/`          | `index.md`                  |
| Page     | `yoursite.com/awards`    | `/awards/index.md`          |
| Sub-page | `yoursite.com/team/join` | `/team/join/index.md`       |

To add or remove a page, simply create or delete the corresponding folder and Markdown files in your repo.

As such, the pages that come with this template – `/blog`, `/contact`, etc. – can be freely removed or renamed at your discretion.

{% hint style="info" %}
"Index" is a [naming convention](https://stackoverflow.com/questions/32408259/why-do-people-name-their-files-index-html) for referring to the "default" page of a particular folder. Navigating to `yoursite.com/awards` would actually load `yoursite.com/awards/index.html` (generated from `/awards/index.md`).
{% endhint %}

## **Edit page details**

Markdown files can also have a section at the top called the "[front matter](https://assemble.io/docs/YAML-front-matter.html)" to hold metadata about the page in YAML format. This is how you can pass special per-page details to Jekyll and the template.

Example `index.md` page file:

```markdown
---
title: Awards
description: Our lab.
nav:
  order: 1
  tooltip: Praise and laurels
---

Regular Markdown content.
```

#### Parameters

| Parameter          | Description                                                                                                                | Default                                   |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------- |
| `title`            | Title of the page. Shown in the tab name along with your [site title](site-settings.md), e.g. "Awards \| Your Lab Website" |                                           |
| `description`      | Description of the page that will show under search engine results.                                                        | [Site-wide description](site-settings.md) |
| `nav`              | If this field is present, the page will appear in the header navigation bar, with the same name as the page's folder.      |                                           |
| `nav` -> `order`   | How the page should be ordered in the nav bar. Number value, lowest to highest -> left to right.                           |                                           |
| `nav` -> `tooltip` | Text to show when hovering over the page's nav bar link.                                                                   |                                           |

{% hint style="info" %}
If you have a `.md` file without a front matter, Jekyll will ignore it and not convert it to an `.html` file, and thus it won't end up in your site. If you don't need any page details, just leave the two lines of `---` with nothing in between.
{% endhint %}
