---
description: An image, title, some text, and link
---

# Feature

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#feature)

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

| Parameter | Description                                                                                              | Default                      |
| --------- | -------------------------------------------------------------------------------------------------------- | ---------------------------- |
| `image`   | URL to an image for the feature.                                                                         |                              |
| `link`    | URL to link to when clicking on the image.                                                               |                              |
| `title`   | "Headline" for the feature. A few words work best.                                                       |                              |
| `text`    | Text to show below the heading. Can contain markdown. Accepts [arbitrary content](./#arbitrary-content). |                              |
| `flip`    | Flip the order of icon and text.                                                                         | `false` (image left of text) |

