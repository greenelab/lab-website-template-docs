---
description: Colored box with icon and content
---

# Alert

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#alert)

```liquid
{% raw %}
{% capture lorem %}
_Lorem_ **ipsum**.
{% endcapture %}
{% endraw %}

{%
  include alert.html
  type="info"
  content=content
%}
```

<table><thead><tr><th width="132">Parameter</th><th>Description</th></tr></thead><tbody><tr><td><code>type</code></td><td>Type of alert. Determines the <a href="icon.md">icon</a> and color to show.<br><br>See <code>/_data/types.yaml</code> for what types of alerts are built-in or to add your own.</td></tr><tr><td><code>content</code></td><td>Content to show as main content of box. Can contain Markdown. Accepts <a href="./#arbitrary-content">arbitrary content</a>.</td></tr></tbody></table>
