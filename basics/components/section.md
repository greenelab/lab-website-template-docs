---
description: A section break with customizable styling
---

# Section

Use this component to create a section break (i.e. end the previous section of content and start a new one) and style the next section. If you want to style the first section on a page, just put this component before any other content.

```liquid
Previous section of content

{%
  include section.html
  background="images/some-bg-image.jpg"
  dark=true
  size=full
%}

Next section of content
```

| Parameter    | Description                                                                                                                                                                                                                                                                | Default                                             |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------- |
| `background` | URL to background image, scaled to cover the section based on its contents. Sections also have a solid color that overlays any background image to always maintain readability of text.                                                                                    | No image                                            |
| `dark`       | Whether the section should be forced to dark (`true`) or light (`false`) mode.                                                                                                                                                                                             | Match visitor's currently selected dark/light mode. |
| `size`       | Width/padding of the section. Set to `wide` to make section take up entire page width, e.g. for large tables of data. Set to `full` to make section take up entire screen width, with no margins, e.g. for use with 100% width [figures](figure.md) to make banner images. | Limited width                                       |

{% hint style="info" %}
Put a section break before every `# Heading 1` and `## Heading 2` to visually break up your content and make it more readable.
{% endhint %}
