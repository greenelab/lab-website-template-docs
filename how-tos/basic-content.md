---
description: How to write basic content for your site in Markdown
---

# Basic content

[👁️ Preview result](https://lab-website-template.netlify.app/testbed#basic-formatting)

**Basic text styles**

```markdown
_italic text_
```

```markdown
**bold text**
```

```markdown
~~strike-through text~~
```

**Line breaks**

```html
<br>
<br>
Text with extra blank lines above and below
<br>
<br>
```

**Comments**

```markdown
<!-- a comment in HTML -->

{% raw %}
{% comment %}
A comment in Liquid
{% endcomment %}
{% endraw %}
```

**Lists**

```markdown
- list item a
- list item b
- list item c
```

```markdown
1. ordered list item 1
2. ordered list item 2
3. ordered list item 3
```

**Links**

```markdown
External link:
[Link text](https://some-website.org/)

Link to a page within your site:
[Meet our team!](team)
```

{% hint style="info" %}
Unless noted otherwise, all links (in `/_data` files, `.md` files, [components](use-components.md), etc.) can be absolute links (e.g. `https://google.com/`) or relative links to items within your repo (e.g. `images/group-photo.jpg`).
{% endhint %}

**Centered element**

```markdown
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
{:.center}
```

Most things in the template are centered by default where appropriate. But sometimes you may need to attach this `center` utility class to an element to center it. Depending on what you're trying to center, the `{:.center}` code may have to go on the same line or on the next line.

**Headings**

```markdown
# Top level heading
## Secondary heading
### Very specific heading
#### Even more specific heading
```

**Horizontal rule**

```markdown
---
```

**Table**

With left-aligned, centered, and right-aligned columns.

```markdown
| TABLE | Game 1 | Game 2 | Game 3 | Total |
| :---- | :----: | :----: | :----: | ----: |
| Anna  |  144   |  123   |  218   |  485  |
| Bill  |   90   |  175   |  120   |  385  |
| Cara  |  102   |  214   |  233   |  549  |
```

**Block quote**

```markdown
> It was the best of times it was the worst of times.
> It was the age of wisdom, it was the age of foolishness.
> It was the spring of hope, it was the winter of despair.
```

**Code block**

With syntax highlighting.

````markdown
```javascript
// a comment
const popup = document.querySelector("#popup");
popup.style.width = "100%";
popup.innerText = "Lorem ipsum dolor sit amet.";
```
````

**Inline code**

```markdown
This sentence has `inline code`, useful for making references to variables, packages, versions, etc. within a sentence.
```
