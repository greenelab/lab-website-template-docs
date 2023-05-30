---
description: >-
  A citation for a particular source, with regular citation details and extra
  "rich" details
---

# Citation

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#citation)

Typically you'd use this with the [list](list.md) component, which would automatically read from `citations.yaml` and pass this component the appropriate parameters. But you can also use it stand-alone to manually display individual citations:

```liquid
{%
  include citation.html
  lookup="doi:10.1016/j.csbj.2020.05.017"
  style="rich"
%}
```

<table><thead><tr><th width="160.33333333333331">Parameter</th><th width="401">Description</th><th>Default</th></tr></thead><tbody><tr><td><code>lookup</code></td><td>Lookup citation details from <code>citations.yaml</code> by <code>id</code> or <code>title</code>.</td><td></td></tr><tr><td><code>style</code></td><td>Visual style of citation. Set to <code>rich</code> to show image and more <a href="../citations.md#rich-details">rich details</a>.</td><td>Plain card with basic info</td></tr><tr><td><code>title</code> / etc.</td><td>The same basic and rich citation parameters outlined in the <a href="../citations.md#examples">citation examples.</a> Retrieved from lookup, or passed automatically from list component.</td><td></td></tr></tbody></table>

