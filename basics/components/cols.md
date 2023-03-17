---
description: Columns of content
---

# Cols

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#cols)

A set of equal-width columns with content, up to a maximum of 3. Columns are vertically aligned to the top, and wrap on smaller screen sizes. Compared to the [grid](grid.md) component, use this when you want to put multiple items per column or have long arbitrary content.

```liquid
{% raw %}
{% capture col1 %}lorem{% endcapture %}
{% capture col2 %}ipsum{% endcapture %}
{% capture col3 %}dolor{% endcapture %}
{% endraw %}

{%
  include cols.html
  col1=col1
  col2=col2
  col3=col3
%}
```

| Parameter       |                                                                                                                                                                                                 |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `col1` / or any | The content of the column. Param names can be anything. Up to 3 columns will be displayed in same order as parameters. Can contain Markdown. Accepts [arbitrary content](./#arbitrary-content). |
