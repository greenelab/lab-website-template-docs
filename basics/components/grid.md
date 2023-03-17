---
description: A grid of items
---

# Grid

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#grid)

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

| Parameter | Description                                                                               | Default         |
| --------- | ----------------------------------------------------------------------------------------- | --------------- |
| `content` | [Arbitrary content](./#arbitrary-content) made up of separate items to arrange in a grid. |                 |
| `style`   | Visual style of the grid. Set to `square` to force the items to have a 1:1 aspect ratio.  | Items auto-size |

You can also pass plain Markdown images to this component. You may want to do this if you want to show images, such as a group of logos, without any of the styling that comes with the figure component (e.g. shadow).

```liquid
{% raw %}
{% capture content %}
  ![](/images/photo.png)

  ![](/images/photo.png)

  ![](/images/photo.png)
{% endcapture %}

{% include grid.html content=content %}
{% endraw %}
```

Note the empty lines in between the images. If you don't include these, Markdown will put all the images in a single paragraph `<p>` element, and that paragraph will be the only item in the grid. Separating them with newlines puts each image in its own paragraph, and thus grid item.
