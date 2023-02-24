---
description: A grid of items
---

# Grid

A list of items to arrange in a grid. Useful for image galleries.

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

| Parameter | Description                                                                                 | Default         |
| --------- | ------------------------------------------------------------------------------------------- | --------------- |
| `content` | Separate items to arrange in a grid. Any arbitrary content using Liquid's capture function. |                 |
| `style`   | Visual style of the grid. Set to `square` to force the items to have a 1:1 aspect ratio.    | Items auto-size |
