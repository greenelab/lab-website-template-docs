---
description: A list of clickable tags
---

# Tags

This component is automatically included in other components such as the [card](card.md) and [citation](citation.md).

```liquid
{%
  include tags.html
  tags="ovarian cancer, dataset, gene expression"
  repo="your-lab/some-repo"
  link="blog"
%}
```

| Parameter | Description                                                                                                                                              | Default      |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ |
| `tags`    | List of tags to display. Can be a comma-separated string or an array.                                                                                    |              |
| `repo`    | GitHub repository to automatically fetch additional ["tags"](https://github.com/topics) from. User/org name and repo name, e.g. `greenelab/deep-review`. |              |
| `link`    | What page of your site to go to when clicking on a tag. The template will go to this page and [search](search.md) for items that have that tag.          | Current page |
