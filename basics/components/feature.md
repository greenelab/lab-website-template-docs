---
description: An image, title, some text, and link
---

# Feature

Useful for your home page, where you want to highlight key points about your lab.

```liquid
{%
  include feature.html
  image="images/group-photo.jpg"
  link="team"
  title="Meet our team"
  text="Our team is made up of people all around the globe"
  flip=true
%}
```

| Parameter | Description                                                                                                                                                                                                    | Default                      |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------- |
| image     | URL to an image for the feature.                                                                                                                                                                               |                              |
| link      | URL to link to when clicking on the image.                                                                                                                                                                     |                              |
| title     | "Headline" for the feature. A few words work best.                                                                                                                                                             |                              |
| text      | Text to show below the heading. Using [Liquid's `capture` function](https://shopify.github.io/liquid/tags/variable/#capture), you can also give it markdown, other components, or any other arbitrary content. |                              |
| flip      | Flip the order of icon and text.                                                                                                                                                                               | `false` (image left of text) |

