---
description: A left or right "floated" piece of content
---

# Float

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#float)

A piece of floating content that the main page content will [flow around](https://developer.mozilla.org/en-US/docs/Web/CSS/float). Useful for putting a figure to the side in a long page of paragraphs.

```liquid
{% raw %}
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
{% endraw %}
```

| Parameter | Description                                                                                                                                                                                                         | Default                  |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------ |
| `content` | [Arbitrary content](./#arbitrary-content) to flow around.                                                                                                                                                           |                          |
| `flip`    | Whether to flip side of page content floats to.                                                                                                                                                                     | `false` (floats to left) |
| `clear`   | Set to `true` to "[stop](https://developer.mozilla.org/en-US/docs/Web/CSS/clear)" the current float, i.e. content after this will no longer flow around the previous float component, and will instead go below it. |                          |

{% hint style="info" %}
In general, you shouldn't need the `clear` parameter, because you should be using this component when the content flowing around is much taller/longer than the floating content (thus the floating content will never push and interfere with undesired things like headings). If you need two roughly equal height things next to each other, you can use the [cols](cols.md) or even the [feature](feature.md) component instead (as long as you're okay with equal width).
{% endhint %}
