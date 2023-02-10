# Use your logo

One of the first and most important things to do is replace the template's logo with your own logo.

There are three files in `/images` you need to update:

| Filename | Acceptable formats       | Purpose                                                                  | Tips for best appearance                                                                                                                                                                                                                 |
| -------- | ------------------------ | ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `logo`   | **`.svg`** `.png` `.jpg` | Displayed in the header of your site on every page.                      | <ul><li>SVG with transparent background</li><li>No text¹</li><li>Very tight cropping (&#x3C; ~5%); template already adds margins</li></ul>                                                                                               |
| `icon`   | **`.png`**               | Your site's [favicon](https://en.wikipedia.org/wiki/Favicon).            | <ul><li>512 x 512 px</li><li>Very tight cropping (&#x3C; ~5%).</li><li>Discernable at very small size (16px)</li><li>If transparent, discernable on light or dark background</li></ul>                                                   |
| `jpg`    | **`.jpg`** `.png`        | Preview image when you share a link to your site on Twitter, Slack, etc. | <ul><li>Logo and text, centered</li><li>~2:1 aspect ratio</li><li>1000 x 500 px</li><li>Enough margins to allow <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit">cover fit</a> for varying aspect ratios.</li></ul> |

The tool [realfavicongenerator](https://realfavicongenerator.net/) can generate tons of variations of your logo for things like: iOS/android homepage bookmarks, Windows start menu bookmarks, Safari pinned tabs, and Internet Explorer fallbacks. However, in our opinion, this goes a bit overboard into super specific/niche use cases that most people will never encounter. We've elected to build-in a simpler subset of these that we think will be appropriate for most people.

{% hint style="info" %}
¹ Separating the text from your logo shape can look better, because then the template can wrap the text to a new line dynamically depending on the screen size. If you don't have or don't want to use a version of your logo with just the shape, you can tell the template not to display your site title again in your [site settings](site-settings.md).
{% endhint %}
