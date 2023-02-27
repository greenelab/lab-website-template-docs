---
description: A left or right "floated" piece of content
---

# Float

A piece of content that the main page content will [flow around](https://developer.mozilla.org/en-US/docs/Web/CSS/float). Useful for putting a figure to the side in a long page of paragraphs.

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

| Parameter | Description                                                                                          | Default                  |
| --------- | ---------------------------------------------------------------------------------------------------- | ------------------------ |
| `content` | Content to flow around. Can be plain text, or any arbitrary content using Liquid's capture function. |                          |
| `flip`    | Whether to flip side of page content floats to.                                                      | `false` (floats to left) |
| `clear`   | Stop flowing around the previous float component.                                                    |                          |

{% hint style="info" %}
In general, you shouldn't need the `clear` parameter, because you should be using this component when the flowing content is much taller/longer than the floating content (thus the floating content will never push and interfere with undesired things like headings). If you need two relatively equal height things next to each other, you can use the [cols](cols.md) or even the [feature](feature.md) component.
{% endhint %}
