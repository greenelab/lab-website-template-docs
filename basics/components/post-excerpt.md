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

<table><thead><tr><th width="171.33333333333331">Parameter</th><th>Description</th></tr></thead><tbody><tr><td><code>lookup</code></td><td>Lookup post details from <code>posts</code> by filename, without the <code>YYYY-MM-DD-</code> date prefix or <code>.md</code> extension.</td></tr><tr><td><code>title</code> / etc.</td><td>The same parameters outlined in <a href="../blog-posts.md">blog posts</a>. Retrieved from lookup, or passed automatically from list component.</td></tr></tbody></table>
