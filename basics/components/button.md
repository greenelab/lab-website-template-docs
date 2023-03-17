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

| Parameter | Description                                                                                           | Default                     |
| --------- | ----------------------------------------------------------------------------------------------------- | --------------------------- |
| `type`    | When specified, looks up default/fallback values for unspecified parameters from `/_data/types.yaml`. |                             |
| `link`    | URL to link to, without any prefixes like @, www., etc.                                               | From `type`                 |
| `icon`    | [Icon](icon.md) to show.                                                                              | From `type`                 |
| `text`    | Text next to icon.                                                                                    | From `type`                 |
| `tooltip` | Text to show when hovering over the button.                                                           | From `type`                 |
| `flip`    | Flip the order of icon and text.                                                                      | `false` (icon left of text) |
| `style`   | Visual style of the button. Set to `bare` for a more plain style.                                     | Typical button appearance   |

{% hint style="info" %}
Tip: Prefer starting with just `type`, and only specify the parameters you need to override.
{% endhint %}

{% hint style="info" %}
Defaults with `type` only get applied to completely unspecified parameters. If you need to force no text, for example, just set `text=""`.
{% endhint %}
