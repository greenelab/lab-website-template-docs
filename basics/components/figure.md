---
description: An image with caption and link
---

# Figure

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#figure)

```liquid
{%
  include figure.html
  image="images/group-photo.jpg"
  caption="The team at our annual Christmas party, 2025"
  link="team"
  width="400px"
%}
```

| Parameter          | Description                                                                                                                                                                                |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `image`            | URL to image for the figure.                                                                                                                                                               |
| `caption`          | Caption content. Can contain Markdown.                                                                                                                                                     |
| `link`             | URL to navigate to when clicking on the image.                                                                                                                                             |
| `width` / `height` | Dimensions of the image in `px` or `%`. You should only specify either width OR height, to maintain the original aspect ratio of the image. Image will shrink to fit smaller screen sizes. |

{% hint style="info" %}
`images/fallback.svg` is an image that will be shown in place of images (in any component) that fail to load. This is useful because you may often be linking to external image URLs that can become broken without notice.
{% endhint %}

Example of using with the [section](section.md) component to make a full width banner:

```liquid
{% raw %}
{% include section.html size="full" %}

{% include figure.html image="images/banner.jpg" width="100%" %}

{% include section.html %}
{% endraw %}

Continued content
```

