---
description: A left or right "floated" piece of content
---

# Float

A piece of content that the main page content will [wrap/flow around](https://developer.mozilla.org/en-US/docs/Web/CSS/float). Useful for putting a figure to the side in a long page of paragraphs.

```liquid
{% raw %}
{% capture content %}
  {% include figure.html ... %}
{% endcapture %}
{% endraw %}

{%
  include float.html
  content=content
  flip=true
%}
```

| Parameter | Description                                                                                                                                                                                                         | Default                  |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------ |
| `content` | Content to wrap/flow around. Can be plain text, or any arbitrary content using Liquid's capture function. Be sure to use an item with a limited width, such as a [figure](figure.md) with a set width e.g. `300px`. |                          |
| `flip`    | Whether to flip side of page content floats to.                                                                                                                                                                     | `false` (floats to left) |
