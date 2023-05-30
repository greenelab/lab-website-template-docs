# Use your logo

One of the first and most important things to do is replace the template's logo with your own logo.

There are three files in `/images` you need to update:

<table><thead><tr><th width="123.33333333333331">Filename</th><th width="193">Acceptable formats</th><th width="134">Purpose</th><th>Tips for best appearance</th></tr></thead><tbody><tr><td><code>logo</code></td><td><strong><code>.svg</code></strong> <code>.png</code> <code>.jpg</code></td><td>Displayed in the header of your site on every page.</td><td><ul><li>SVG with transparent background</li><li>No text¹</li><li>Very tight cropping (template already adds margins)</li></ul></td></tr><tr><td><code>icon</code></td><td><strong><code>.png</code></strong> <code>.jpg</code></td><td>Your site's <a href="https://en.wikipedia.org/wiki/Favicon">favic</a><a href="https://en.wikipedia.org/wiki/Favicon">on</a>.</td><td><ul><li>PNG</li><li>1:1 square aspect ratio</li><li>512 x 512 px</li><li>Very tight cropping</li><li>Discernable at very small size</li><li>Discernable on light or dark background</li></ul></td></tr><tr><td><code>share</code></td><td><strong><code>.jpg</code></strong> <code>.png</code></td><td>Preview image when you share a link to your site on Twitter, Slack, etc.</td><td><ul><li>JPG</li><li><a href="https://iamturns.com/open-graph-image-size/">~2:1 aspect ratio</a></li><li>1000 x 500 px</li><li>Logo and text, centered</li><li>Enough margins to allow <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit">cover fit</a> for varying aspect ratios</li></ul></td></tr></tbody></table>

{% hint style="info" %}
¹ Separating the text from your logo shape can look nicer, because then the template can wrap the text to a new line dynamically depending on the screen size. If you can't or don't want to do this, tell the template in your [site settings](configure-your-site.md).
{% endhint %}

## Favicon variations

The tool [realfavicongenerator](https://realfavicongenerator.net/) can generate tons of variations of your logo for things like: iOS/Android homepage bookmarks, Windows start menu bookmarks, Safari pinned tabs, and Internet Explorer fallbacks. In our opinion, these are pretty rarely used/encountered by visitors, so we elected to reduce this to a simple subset that covers most common use cases.

However, you can still easily include them in the template. Just follow the tool's process, and put the images it gives you in your repo, and paste the code it gives you in place of `<link rel="icon">` in `/_includes/meta.html`, and that's it!
