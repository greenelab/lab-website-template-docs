# Customize your theme

Although this is a template, we don't want everyone's site to look exactly the same!

In the file `_styles/theme.scss` you'll find a palette of variables that are repeatedly used throughout the template's styling to achieve a consistent look.

## Picking colors

Picking good colors, especially ones that work well together is surprisingly hard! So don't do it without help! Here are some amazing color palettes we highly recommend:

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td>Tailwind</td><td><a href="https://tailwindcolor.com/">tailwindcolor.com</a></td><td></td><td><a href="../.gitbook/assets/tailwind.jpg">tailwind.jpg</a></td></tr><tr><td>Material UI</td><td><a href="https://www.materialpalette.com/colors">materialpalette.com/colors</a></td><td></td><td><a href="../.gitbook/assets/material.jpg">material.jpg</a></td></tr><tr><td>Coolor.co</td><td><a href="https://coolors.co/palettes/trending">coolors.co/palettes</a></td><td></td><td><a href="../.gitbook/assets/coolors.jpg">coolors.jpg</a></td></tr></tbody></table>

## Theme properties

Here are the theme variables you should try customizing to distinguish your site from others built on the template.

| Property                                                                                     | Description                                                                                                                                                                                               |
| -------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `$page`                                                                                      | When on large desktop screens, most websites limit the width of text content in the center of the screen to make it easier to read. This is the max width this center column of main page content can be. |
| <p><code>$accent</code></p><p><code>$accent-light</code></p><p><code>$accent-dark</code></p> | The "theme" colors for your site. Gets used in links, buttons, tags, etc. Typically you want these to be different shades of the same hue. Try matching this with your logo/branding.                     |
| <p><code>$title</code><br><code>$body</code><br><code>$code</code></p>                       | Fonts for certain types of text. "Body" is regular text, "title" is things like headings and titles, and "code" is code blocks.                                                                           |
| `$spacing`                                                                                   | Line spacing in paragraphs of text. 1 = single spaced, 2 = double space, etc.                                                                                                                             |
| `$rounded`                                                                                   | Border radius on buttons, cards, etc. 0 = completely square.                                                                                                                                              |
| `$box-shadow`                                                                                | Drop shadow around images, cards, etc. [See this reference](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow).                                                                                 |
