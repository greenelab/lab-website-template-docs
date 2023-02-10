---
description: How to write complex content for your site with components
---

# Use components

Markdown is meant for authoring [basic content](basic-content.md) in a quick and intuitive way, but sometimes you need something more complex. **Components** are building blocks for visual and interactive elements on your site. Some people/services call them "widgets".

The template comes with many pre-made components so you can assemble your website however you want with ease.&#x20;

{% hint style="success" %}
**See a list of all the components you can use in the side menu.**
{% endhint %}

Simply place the code for a component in one of your markdown files, and it will appear in your site. The basic syntax for including a component is:

```liquid
{% raw %}
{% include some-component.html parameter="value" %}
{% endraw %}
```

Example of including an image with a caption:

```liquid
Some regular Markdown content. Lorem ipsum dolor sit amet.

{%
  include figure.html
  image="images/group-photo.jpg"
  caption="The team at our annual Christmas party, 2025"
  link="team-page"
  width="400px"
%}
```

{% hint style="info" %}
Unless noted otherwise, all component parameters are optional and have graceful fallbacks if not specified.
{% endhint %}
