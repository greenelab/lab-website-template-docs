# Custom components

The template comes with a [few placeholder data lists and matching components for common needs](../basics/repo-structure.md#data-and-components), but advanced users can make their own. Here's an example of doing that.

Let's say we want to have a page that lists the talks we've given at various places.

1. We'll start with a [data file](data-and-collections.md) to cleanly list and manage the key details of each talk. Notice that these field names aren't something you'll see in any of the included components.

{% code title="/_data/talks.yaml" %}
```yaml
- title: A new way to analyze data
  venue: University of London
  length: 45
  
- title: Utilizing AI in research
  venue: University of Colorado
  length: 30

...etc.
```
{% endcode %}

2. Now let's make a new component with matching parameters. In the future we could make this nicer by having a little clock [icon](../basics/components/icon.md) next to minutes and maybe a link to the venue's website or location on Google Maps.

{% code title="/_include/talk.html" %}
```html
<div class="talk">
  <strong>{{ include.title }}</strong>
  <span>{{ include.venue }}</span>
  <em>{{ include.length }} minutes</em>
</div>
```
{% endcode %}

3. We already included some bold and italics right in the HTML, but let's add a little bit more style with CSS/Sass. We'll reference the `talk` class we put in the HTML.

{% code title="/_styles/talk.scss" %}
```css
---
---

.talk {
    display: inline-flex;
    flex-wrap: wrap;
    gap: 10px;
    margin: 20px 0;
    padding: 20px;
    box-shadow: var(--shadow);
}
```
{% endcode %}

4. Now we can use the [list](../basics/components/list.md) component to easily loop through our new data and display each item with our custom component.

{% code title="/talks/index.md" %}
```liquid
# Talks

{% raw %}
{% include list.html data="talks" component="talk" %}
{% endraw %}
```
{% endcode %}

5. Hmm but wait, it didn't work completely right. Only the title shows. Unfortunately, due to a limitation of Jekyll/Liquid, any new parameters that you want to pass from `data` to `component` in the list component must be explicitly named in `/_includes/list.html`. The title works because there are already other components that take that parameter name, and `title` was already included. Just add the other two like this.

{% code title="/_includes/list.html" %}
```liquid
  ..
  venue=d.venue
  length=d.length
  ...
```
{% endcode %}

6. It's finally working! We've now created a custom page that uses the list component to show a custom set of data (written in human-readable form) with a custom component with custom styling.
