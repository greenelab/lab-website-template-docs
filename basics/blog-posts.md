# Blog posts

## Add/remove posts

To add or remove a blog post, create or delete a Markdown file in `/_posts`.  The filename should be in the format `YYYY-MM-DD-your-post-title.md`, which Jekyll uses for the post's URL and date (among other things).

Each file will automatically generate its own page based on its filename.

{% hint style="info" %}
After adding post, you can display them on your site with the [list](../components/list.md) and [post excerpt](../components/post-excerpt.md) components.
{% endhint %}

Example:

```
---
title: An ordinary day in the life of me
author: tim-member
tags:
  - biology
  - big data
  - medicine
---

<!-- excerpt start -->
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
<!-- excerpt end -->
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
```

| Parameter                                                                                                    | Description                                                                                                                                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `title`                                                                                                      | Title of post.                                                                                                                                                                                                                                              |
| `author`                                                                                                     | Filename of author's team member page (without the extension). If found, the portrait and name of the member is displayed automatically. If not found, the template assumes you provided a raw name to display, e.g. "Tim Member".                          |
| `tags`                                                                                                       | List of topics/themes for post.                                                                                                                                                                                                                             |
| <p><code>&#x3C;!-- excerpt start/end --></code> in body<br>OR</p><p><code>excerpt</code> in front matter</p> | Manually specify what should be used as the excerpt (preview of post content) when displaying the post with the [post excerpt](../components/post-excerpt.md) component. [Defaults to the first paragraph](https://jekyllrb.com/docs/posts/#post-excerpts). |

