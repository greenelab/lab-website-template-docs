---
description: A box with image, link, text, and tags
---

# Card

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#card)

```liquid
{%
  include card.html
  image="images/space.jpg"
  link="https://nasa.gov/"
  title="A Large Card"
  subtitle="A cool card"
  description="A cool description"
  tooltip="A cool tooltip"
  tags="tag A, tag B, tag C"
  repo="greenelab/lab-website-template"
  style="small"
%}
```

<table><thead><tr><th width="171">Parameter</th><th>Description</th></tr></thead><tbody><tr><td><code>image</code></td><td>URL to an image for the card.</td></tr><tr><td><code>link</code></td><td>URL to link to when clicking the image or the title of the card.</td></tr><tr><td><code>title</code></td><td>Title for the card.</td></tr><tr><td><code>subtitle</code></td><td>Subtitle for the card.</td></tr><tr><td><code>description</code></td><td>Text to show under the card name. Can contain Markdown. Accepts <a href="./#arbitrary-content">arbitrary content</a>.</td></tr><tr><td><code>tooltip</code></td><td>Text to show when hovering over the card.</td></tr><tr><td><code>tags</code></td><td><a href="tags.md">Tags</a> to show at the bottom of the card.</td></tr><tr><td><code>repo</code></td><td>GitHub repository to automatically fetch additional <a href="tags.md">tags</a> from.</td></tr><tr><td><code>style</code></td><td>Visual style of the card. Set to <code>small</code> to make the card a bit smaller.</td></tr></tbody></table>
