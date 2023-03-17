---
description: An excerpt and info from a blog post
---

# Post Excerpt

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#post-excerpt)

Typically you'd use this with the [list](list.md) component, which would automatically read from `posts` and pass this component the parameters. But you can also use it stand-alone to manually display individual posts:

```liquid
{%
  include post-excerpt.html
  lookup="example-blog-post-1"
%}
```

| Parameter      | Description                                                                                                                         |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| `lookup`       | Lookup post details from `posts` by filename, without the `YYYY-MM-DD-` date prefix or `.md` extension.                             |
| `title` / etc. | The same parameters outlined in [blog posts](../blog-posts.md). Retrieved from lookup, or passed automatically from list component. |
