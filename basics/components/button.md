---
description: A button with icon and text
---

# Button

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#button)

```liquid
{%
  include button.html
  type="github"
  link="some_github_handle"
  icon="fa-brands fa-github"
  text="Follow us on GitHub"
  tooltip="Follow us on GitHub for new releases"
  flip=true
  style="bare"
%}
```

<table><thead><tr><th width="132.33333333333331">Parameter</th><th width="454">Description</th><th>Default</th></tr></thead><tbody><tr><td><code>type</code></td><td>When specified, looks up default/fallback values for unspecified parameters from <code>/_data/types.yaml</code>.</td><td></td></tr><tr><td><code>link</code></td><td>URL to link to, without any prefixes like @, www., etc.</td><td>From <code>type</code></td></tr><tr><td><code>icon</code></td><td><a href="icon.md">Icon</a> to show.</td><td>From <code>type</code></td></tr><tr><td><code>text</code></td><td>Text next to icon.</td><td>From <code>type</code></td></tr><tr><td><code>tooltip</code></td><td>Text to show when hovering over the button.</td><td>From <code>type</code></td></tr><tr><td><code>flip</code></td><td>Flip the order of icon and text.</td><td><code>false</code> (icon left of text)</td></tr><tr><td><code>style</code></td><td>Visual style of the button. Set to <code>bare</code> for a more plain style.</td><td>Typical button appearance</td></tr></tbody></table>

{% hint style="info" %}
Tip: Prefer starting with just `type`, and only specify the parameters you need to override.
{% endhint %}

{% hint style="info" %}
Defaults with `type` only get applied to completely unspecified parameters. If you need to force no text, for example, just set `text=""`.
{% endhint %}
