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

| Parameter | Description                                                                                                                                                                            |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `type`    | <p>Type of alert. Determines the <a href="icon.md">icon</a> and color to show.<br><br>See <code>/_data/types.yaml</code> for what types of alerts are built-in or to add your own.</p> |
| `content` | Content to show as main content of box. Can contain Markdown. Accepts [arbitrary content](./#arbitrary-content).                                                                       |
