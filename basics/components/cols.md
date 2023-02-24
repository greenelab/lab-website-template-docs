---
description: Columns of content
---

# Cols

A set of equal-width columns with content.

```liquid
{% raw %}
{% capture col1 %}lorem{% endcapture %}
{% capture col2 %}ipsum{% endcapture %}
{% endraw %}
...etc.

{%
  include grid.html
  col1=col1
  col2=col2
  col3=col3
  col4=col4
%}
```

| Parameter       |                                                                                                                                                                           |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `col1` / or any | The content of the column. Param names can be anything. Up to 4 columns will be displayed in same order as params. Any arbitrary content using Liquid's capture function. |
