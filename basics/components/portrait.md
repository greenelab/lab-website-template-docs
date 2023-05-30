---
description: A portrait for a team member, with image, link, name, and role
---

# Portrait

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#portrait)

Typically you'd use this with the [list](list.md) component, which would automatically read from `members` and pass this component the parameters. But you can also use it stand-alone to manually display individual members:

```liquid
{%
  include portrait.html
  lookup="tim-member"
  style="small"
%}
```

<table><thead><tr><th width="140">Parameter</th><th>Description</th></tr></thead><tbody><tr><td><code>lookup</code></td><td>Lookup member details from <code>members</code> by filename, without the <code>.md</code> extension.</td></tr><tr><td><code>style</code></td><td>Visual style of the portrait. Set to <code>small</code> to make it a bit smaller, or set to <code>tiny</code> to make it very small and horizontal layout.</td></tr><tr><td><code>name</code> / etc.</td><td>The same parameters outlined in <a href="../team-members.md">team members</a>. Retrieved from lookup, or passed automatically from list component.</td></tr></tbody></table>
