---
description: A section break with customizable styling
---

# Section

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#section)

Use this component to create a section break – i.e. end the previous section of content and start a new one – and style the next section. If you want to style the first section on a page, just put this component before any other content.

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

<table><thead><tr><th width="155">Parameter</th><th width="372.3333333333333">Description</th><th>Default</th></tr></thead><tbody><tr><td><code>background</code></td><td>URL to background image, <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit">scaled to cover</a> the section based on its contents.</td><td>Solid color background</td></tr><tr><td><code>dark</code></td><td>Whether the section should be forced to dark (<code>true</code>) or light (<code>false</code>) mode.</td><td>Match visitor's currently selected dark/light mode</td></tr><tr><td><code>size</code></td><td>Width/padding of the section. Set to <code>wide</code> to make section take up entire page width, e.g. for large tables of data. Set to <code>full</code> to make section take up entire screen width, with no margins, e.g. for use with 100% width <a href="figure.md">figures</a> to make banner images.</td><td>Limited width</td></tr></tbody></table>

{% hint style="info" %}
Tip: Put a section break before every `# Heading 1` and `## Heading 2` to visually break up your content and make it more readable.
{% endhint %}

{% hint style="info" %}
Sections also have a solid color that overlays any background image to always maintain readability of text.
{% endhint %}

{% hint style="info" %}
`section.scss` style has an editable variable for the width limit. When on large desktop screens, most websites limit the width of text content in the center of the screen to make it [easier to read](https://ux.stackexchange.com/questions/14928/why-do-websites-not-use-entire-width-of-browser).
{% endhint %}

