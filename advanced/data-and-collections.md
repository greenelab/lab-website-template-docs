# Data and collections

Jekyll provides two main ways to create and maintain large lists/sets of items: **data** and **collections**.&#x20;

The template already includes [a few of these for commonly needed things](../basics/components/list.md#data-and-components), but if you need to create more/different ones, here's how.

{% hint style="info" %}
This page just explains how to make these lists. To actually display them on your site, use the [list component](../basics/components/list.md).
{% endhint %}

## **Data**

If you want to have a large set of structured or nested items in a single file, use a [data file](https://jekyllrb.com/docs/datafiles/).

Put a `.yaml` file in the `/_data` folder with any name, and fill it with data. The structure of the data can be arbitrary.

Example:

{% code title="/_data/some-list.yaml" %}
```yaml
# some item
- title: Some name
  tags:
    - tag A
    - tag B
  description: Some description

# another item
...
```
{% endcode %}

## **Collections**

If you want to have a large set of items in separate files that can also generate their own separate pages on your site, use [collections](https://jekyllrb.com/docs/collections).&#x20;

Put `.md` files in a folder prefixed with a `_`, and fill their [front matters](../basics/edit-pages.md#edit-page-details) with data. To generate a separate page for each item in the collection, set `output: true` in your config file [as described here](https://jekyllrb.com/docs/collections).

Example:

{% code title="/_some-list/some-file.md" %}
```markdown
---
title: Some name
tags:
  - tag A
  - tag B
description: Some description
---

Some Markdown content
```
{% endcode %}

{% code title="/_some-list/another-file.md" %}
```markdown
---
title: Another name
---

Some Markdown content
```
{% endcode %}
