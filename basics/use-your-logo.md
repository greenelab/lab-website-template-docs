# Use your logo

One of the first and most important things to do is replace the template's logo with your own logo.

There are three files in `/images` you need to update:

| Filename | Acceptable formats       | Purpose                                                                                                | Tips for best appearance                                                                                                                                                                                                                                                                                      |
| -------- | ------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `logo`   | **`.svg`** `.png` `.jpg` | Displayed in the header of your site on every page.                                                    | <ul><li>SVG with transparent background</li><li>No text¹</li><li>Very tight cropping (template already adds margins)</li></ul>                                                                                                                                                                                |
| `icon`   | **`.png`** `.jpg`        | Your site's [favic](https://en.wikipedia.org/wiki/Favicon)[on](https://en.wikipedia.org/wiki/Favicon). | <ul><li>PNG</li><li>1:1 square aspect ratio</li><li>512 x 512 px</li><li>Very tight cropping</li><li>Discernable at very small size</li><li>Discernable on light or dark background</li></ul>                                                                                                                 |
| `share`  | **`.jpg`** `.png`        | Preview image when you share a link to your site on Twitter, Slack, etc.                               | <ul><li>JPG</li><li><a href="https://iamturns.com/open-graph-image-size/">~2:1 aspect ratio</a></li><li>1000 x 500 px</li><li>Logo and text, centered</li><li>Enough margins to allow <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit">cover fit</a> for varying aspect ratios</li></ul> |

{% hint style="info" %}
¹ Separating the text from your logo shape can look nicer, because then the template can wrap the text to a new line dynamically depending on the screen size. If you can't or don't want to do this, tell the template in your [site settings](configure-your-site.md).
{% endhint %}

## Favicon variations

The tool [realfavicongenerator](https://realfavicongenerator.net/) can generate tons of variations of your logo for things like: iOS/Android homepage bookmarks, Windows start menu bookmarks, Safari pinned tabs, and Internet Explorer fallbacks. In our opinion, these are pretty rarely used/encountered by visitors, so we elected to reduce this to a simple subset that covers most common use cases.

However, you can still easily include them in the template. Just follow the tool's process, and put the images it gives you in your repo, and paste the code it gives you in place of `<link rel="icon">` in `/_includes/meta.html`, and that's it!
