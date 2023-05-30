---
description: A list of clickable tags
---

# Tags

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#tags)

This component is automatically included in other components such as the [card](card.md) and [citation](citation.md). But you can also use it stand-alone to manually list a set of tags that a visitor can [filter the page by](search.md).

```liquid
{%
  include tags.html
  tags="ovarian cancer, dataset, gene expression"
  repo="your-lab/some-repo"
  link="blog"
%}
```

<table><thead><tr><th width="137">Parameter</th><th width="461">Description</th><th>Default</th></tr></thead><tbody><tr><td><code>tags</code></td><td>List of tags to display. Can be a comma-separated string or an array.</td><td></td></tr><tr><td><code>repo</code></td><td>GitHub repository to automatically fetch additional <a href="https://github.com/topics">"tags"</a> from. Just user/org name and repo name, e.g. <code>greenelab/deep-review</code>.</td><td></td></tr><tr><td><code>link</code></td><td>What page of your site to go to when clicking on a tag. The template will go to this page and <a href="search.md">search</a> for items that have that tag.</td><td>Current page</td></tr></tbody></table>
