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

# site social media and other links
links:
  email: jane.smith@your-lab.com
  google-scholar: ETJoidYAAAAJ
  github: your-lab
  twitter: YourLabHandle
  instagram: YourLabHandle
  youtube: YourLabChannel

### advanced settings to ignore
...
```

#### Parameters

| Parameter         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Default                 |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------- |
| `title`           | <p>Title of your site. Appears in the tab title, in the header, and in <a href="https://www.google.com/search?q=html+meta+tags">page metadata</a>.<br><br>Use a short version of your lab's name if you have one so it can fit nicely in these spots. Aim for &#x3C; about 20 characters. For example, the <a href="https://tislab.org/">Translational and Integrative Sciences Lab</a> shortens their name to "TIS Lab", then displays their full name at the top of their home page in bold.</p> |                         |
| `subtitle`        | Appears in the header below your site title, smaller and more subtle. This is useful if your lab has a slogan, e.g. "Where data meets biology!", or if you want to list the school/department/etc your lab is a part of, e.g. "at the University of Colorado Anschutz".                                                                                                                                                                                                                            |                         |
| `description`     | Default description of pages that will show under search engine results.                                                                                                                                                                                                                                                                                                                                                                                                                           |                         |
| `logo-text`       | Whether to show your site's title next to your logo in the header. Set to `false` if your logo image already contains the title of your lab.                                                                                                                                                                                                                                                                                                                                                       | `true`                  |
| `header`/`footer` | Default background images for the header/footer of pages.                                                                                                                                                                                                                                                                                                                                                                                                                                          | Solid color background. |
| `links`           | <p>Links to show in the footer of every page, <em>without</em> any prefixes like <code>@</code>, <code>www.</code>, etc.<br><br>See the link component.</p>                                                                                                                                                                                                                                                                                                                                        |                         |

