# Use your logo

One of the first and most important things to do is replace the template's logo with your own logo.

There are three files in `/images` you need to update:

| Filename | Acceptable formats       | Purpose                                                                                                | Tips for best appearance                                                                                                                                                                                                                 |
| -------- | ------------------------ | ------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `logo`   | **`.svg`** `.png` `.jpg` | Displayed in the header of your site on every page.                                                    | <ul><li>SVG with transparent background</li><li>No text¹</li><li>Very tight cropping (template already adds margins)</li></ul>                                                                                                           |
| `icon`   | **`.png`**               | Your site's [favic](https://en.wikipedia.org/wiki/Favicon)[on](https://en.wikipedia.org/wiki/Favicon). | <ul><li>1:1 square aspect ratio</li><li>512 x 512 px</li><li>Very tight cropping</li><li>Discernable at very small size</li><li>Discernable on light or dark background</li></ul>                                                        |
| `jpg`    | **`.jpg`** `.png`        | Preview image when you share a link to your site on Twitter, Slack, etc.                               | <ul><li>~2:1 aspect ratio</li><li>1000 x 500 px</li><li>Logo and text, centered</li><li>Enough margins to allow <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit">cover fit</a> for varying aspect ratios.</li></ul> |

{% hint style="info" %}
The tool [realfavicongenerator](https://realfavicongenerator.net/) can generate tons of variations of your logo for things like: iOS/android homepage bookmarks, Windows start menu bookmarks, Safari pinned tabs, and Internet Explorer fallbacks. However, in our opinion, these are very niche use cases that most people will never encounter, so we've elected to only include a simple subset.
{% endhint %}

{% hint style="info" %}
¹ Separating the text from your logo shape can look nicer, because then the template can wrap the text to a new line dynamically depending on the screen size. If you can't or don't want to do this, tell the template in your [site settings](configure-your-site.md).
{% endhint %}
