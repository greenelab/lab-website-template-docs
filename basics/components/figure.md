---
description: An image with caption and link
---

# Figure

```liquid
{%
  include figure.html
  image="images/group-photo.jpg"
  caption="The team at our annual Christmas party, 2025"
  link="team"
  width="400px"
%}
```

| Parameter          | Description                                                                                                                                                 |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `image`            | URL to image for the figure.                                                                                                                                |
| `caption`          | Caption content. Can contain Markdown.                                                                                                                      |
| `link`             | URL to navigate to when clicking on the image.                                                                                                              |
| `width` / `height` | Dimensions of the image in `px` or `%`. Only specify one to maintain the original aspect ratio of the image. Image will shrink to fit smaller screen sizes. |

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

{% hint style="info" %}
Note: If you're trying to link to an image in a GitHub repo, make sure to link to the actual **raw image**, not the GitHub page for the image file in the repo.&#x20;

For example, use...

`raw.githubusercontent.com/greenelab/ponyo/master/logo.png`&#x20;

...instead of...

`github.com/greenelab/ponyo/blob/master/logo.png`
{% endhint %}

