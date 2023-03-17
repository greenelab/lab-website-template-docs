---
description: How to write fancier content for your site with components
---

# Components

Markdown is meant for [basic content](../write-basic-content.md), but sometimes you need something more. **Components** are building blocks for more complex visual and interactive elements on your site. You can also think of them as "widgets".

The template comes with many pre-made components so you can assemble your website however you want with ease.

Simply place the code for a component in one of your markdown files, and it will appear in your site. The basic syntax for including a component is:

```liquid
...some content...

{% raw %}
{% include some-component.html parameter="value" %}
{% endraw %}

...more content...
```

{% hint style="info" %}
Unless noted otherwise, all component parameters are optional and have graceful fallbacks if not specified.
{% endhint %}

## Arbitrary content

Some component parameters allow you to pass complex, arbitrary content to them, such as plain text, multiple paragraphs, Markdown, and even other components.

To do this, you have to use [Liquid's capture tag](https://shopify.github.io/liquid/tags/variable/#capture) first. Example:

```liquid
{% raw %}
{% capture some-content %}
  Some text.
  _Some_ **Markdown**.
  {% include another-component.html %}
{% end capture %}

{% include some-component.html some-param=some-content %}
{% endraw %}
```
