---
description: A left or right "floated" piece of content
---

# Float

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#float)

A piece of floating content that the main page content will [flow around](https://developer.mozilla.org/en-US/docs/Web/CSS/float). Useful for putting a figure to the side in a long page of paragraphs.

```liquid
{% capture content %}
  {% include figure.html ... %}
{% endcapture %}

{%
  include float.html
  content=content
  flip=true
%}

Several paragraphs of text.

{% include float.html clear=true %}
```

<table><thead><tr><th width="136">Parameter</th><th width="436">Description</th><th>Default</th></tr></thead><tbody><tr><td><code>content</code></td><td><a href="./#arbitrary-content">Arbitrary content</a> to flow around.</td><td></td></tr><tr><td><code>flip</code></td><td>Whether to flip side of page content floats to.</td><td><code>false</code> (floats to left)</td></tr><tr><td><code>clear</code></td><td>Set to <code>true</code> to "<a href="https://developer.mozilla.org/en-US/docs/Web/CSS/clear">stop</a>" the current float, i.e. content after this will no longer flow around the previous float component, and will instead go below it.</td><td></td></tr></tbody></table>

{% hint style="info" %}
In general, you shouldn't need the `clear` parameter, because you should be using this component when the content flowing around is much taller/longer than the floating content (thus the floating content will never push and interfere with undesired things like headings). If you need two roughly equal height things next to each other, you can use the [cols](cols.md) or even the [feature](feature.md) component instead (as long as you're okay with equal width).
{% endhint %}
