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

<table><thead><tr><th width="189">Parameter</th><th>Description</th></tr></thead><tbody><tr><td><code>image</code></td><td>URL to image for the figure.</td></tr><tr><td><code>caption</code></td><td>Caption content. Can contain Markdown.</td></tr><tr><td><code>link</code></td><td>URL to navigate to when clicking on the image.</td></tr><tr><td><code>width</code> / <code>height</code></td><td>Dimensions of the image in <code>px</code> or <code>%</code>. You should only specify either width OR height, to maintain the original aspect ratio of the image. Image will shrink to fit smaller screen sizes.</td></tr></tbody></table>

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

