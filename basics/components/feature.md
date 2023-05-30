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

<table><thead><tr><th width="127">Parameter</th><th width="467">Description</th><th>Default</th></tr></thead><tbody><tr><td><code>image</code></td><td>URL to an image for the feature.</td><td></td></tr><tr><td><code>link</code></td><td>URL to link to when clicking on the image.</td><td></td></tr><tr><td><code>title</code></td><td>"Headline" for the feature. A few words work best.</td><td></td></tr><tr><td><code>text</code></td><td>Text to show below the heading. Can contain markdown. Accepts <a href="./#arbitrary-content">arbitrary content</a>.</td><td></td></tr><tr><td><code>flip</code></td><td>Flip the order of icon and text.</td><td><code>false</code> (image left of text)</td></tr></tbody></table>

