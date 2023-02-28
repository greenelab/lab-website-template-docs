# Search

The template can dynamically (when a visitor comes to your site) filter items on a page based on a search.

## How can a search happen?

* A visitor types in a search box component (see below).
* A visitor clicks on a link with e.g. `?search=some search` in the URL, like a [tag](tags.md) or a [team member page research link](../team-members.md) (see `aliases`).

## What items are filtered?

By default, the only items on the page that are filtered the [card](card.md), [citation](../citations.md), and [post excerpt](post-excerpt.md) components.

You could customize this in `/_scripts/search.js` to filter any kind of item that is selectable with a [CSS selector](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS\_Selectors), for example `p` for paragraph elements.

## How are items filtered?

You can search for terms, phrases, and tags:

`term1 term2 "full phrase 1" "full phrase 2" "tag: some tag" "tag: another tag"`.

Items that contain **all of the terms**, **at least one of the phrases**, and **at least one of the tags** will be considered a match. Matching is case insensitive. Tags are also insensitive to hyphens, e.g. `open science` is considered the same as `open-science`.

Search words will be highlighted in the results (if they're longer than 2 characters). In addition to the visible text content of the item, tooltip and other content are also searched (via the `data-tooltip` and `data-search` attributes).

## Relevant components

You can put a search box component on the page to let visitors type in their own search:

```liquid
{% raw %}
{% include search-box.html %}
{% endraw %}
```

This also updates the URL so they can conveniently link to that page with that search.

To show info about what items are being filtered, e.g. _Showing 12 of 60_, you can put a search info component on a page:

```liquid
{% raw %}
{% include search-info.html %}
{% endraw %}
```

Only visible if something is being searched.
