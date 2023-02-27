# Configure your site

The basic settings and configuration for your site reside in the `_config.yaml` file.

Example:

```yaml
### basic settings

# site properties and page defaults
title: Lab Website Template
subtitle: A template by the Greene Lab
description: An easy-to-use, flexible website template for labs, with automatic citations, GitHub tag imports, pre-built components, and more.
logo-text: false
header: images/background.jpg
footer: images/background.jpg
header-dark: false
footer-dark: false

# site social media and other links
links:
  email: jane.smith@your-lab.com
  orcid: 0000-0001-8713-9213
  google-scholar: ETJoidYAAAAJ
  github: your-lab
  twitter: YourLabHandle
  instagram: YourLabHandle
  youtube: YourLabChannel

### Jekyll settings to ignore
...
```

| Parameter                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                     | Default                |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------- |
| `title`                       | <p>Title of your site. Appears in the tab title, in the header, and in <a href="https://www.google.com/search?q=html+meta+tags">page metadata</a>.<br><br>Use a short version of your lab's name if you have one so it can fit nicely in these spots. Aim for less than 20 characters.</p><p></p><p>Tip: If your lab name is long, use an abbreviated version here, then display the full name at the top of your homepage.</p> |                        |
| `subtitle`                    | Appears in the header next to your site title, smaller and more subtle. Useful for slogans or affiliations.                                                                                                                                                                                                                                                                                                                     |                        |
| `description`                 | Default description that will show under search engine results. Can be overridden on [individual pages](edit-pages.md).                                                                                                                                                                                                                                                                                                         |                        |
| `logo-text`                   | Whether to show your title and subtitle next to your logo in the header. Set to `false` if your logo image already contains the title of your lab.                                                                                                                                                                                                                                                                              | `true`                 |
| `header`/`footer`             | Default background image for the header/footer. Can be overridden on [individual pages](edit-pages.md).                                                                                                                                                                                                                                                                                                                         | Solid color background |
| `header-dark` / `footer-dark` | Default header/footer dark/light mode. Can be overridden on [individual pages](edit-pages.md).                                                                                                                                                                                                                                                                                                                                  | `true`                 |
| `links`                       | <p>Social media links for your lab to show in the footer of every page, without any prefixes like <code>@</code>, <code>www.</code>, etc.<br><br>See <code>/_data/types.yaml</code> for what types of links are built-in or to add your own.</p>                                                                                                                                                                                |                        |

{% hint style="info" %}
Headers/footers/sections have a solid color that overlays any background image to always maintain readability of text.
{% endhint %}
