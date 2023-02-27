---
description: A grid of items
---

# Grid

A list of items to arrange in a grid. Wraps on smaller screen sizes. Compared to the [cols](cols.md) component, use this when you have 3 or more individual items that are roughly the same proportions, for example for image galleries.

```
{% raw %}
{% capture content %}
  {% include figure.html ... %}
  {% include figure.html ... %}
  {% include figure.html ... %}
  {% include figure.html ... %}
  {% include figure.html ... %}
{% endcapture %}
{% endraw %}

{%
  include grid.html
  content=content
  style="square"
%}
```

| Parameter | Description                                                                                        | Default         |
| --------- | -------------------------------------------------------------------------------------------------- | --------------- |
| `content` | Separate items to arrange in a grid. Can be any arbitrary content using Liquid's capture function. |                 |
| `style`   | Visual style of the grid. Set to `square` to force the items to have a 1:1 aspect ratio.           | Items auto-size |
