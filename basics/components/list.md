---
description: A generic and flexible way to automatically list large sets of items
---

# List

:eye: [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#list)

Takes a list of data, filters it, loops through it, and displays each item with some component.

```liquid
{%
  include list.html
  data="citations"
  component="citation"
  filters="group: featured"
  style="rich"
%}
```

<table><thead><tr><th width="162">Parameter</th><th>Description</th></tr></thead><tbody><tr><td><code>data</code></td><td>The <a href="../../advanced/data-and-collections.md">set of items</a> to loop through, e.g. <code>citations</code>, <code>posts</code>, <code>members</code>, etc. If your list has <code>date</code> fields, it is also sorted from newest to oldest, and grouped into sections by year.</td></tr><tr><td><code>component</code></td><td>The component to show for each item in the list. The fields in your <code>data</code> should match what this component takes as parameters (except for <code>style</code>, see below).</td></tr><tr><td><code>filters</code></td><td>Filter your <code>data</code> by arbitrary fields and values. See detailed explanation below.</td></tr><tr><td><code>style</code></td><td>A <code>style</code> parameter to pass through to every component in the list, so you don't have to repetitively set it on every <code>data</code> item. This is the only field that works this way, because all other fields are likely to be different for each item, but you'll likely always want the same <code>style</code> parameter.</td></tr></tbody></table>

Technically you can use [any](../../advanced/custom-components.md) structure of `data` and any `component` with the list component, but by default, the template comes with a [few placeholder data lists and matching components for common needs](../repo-structure.md#data-and-components).

## Filters

The `filters` parameter is a comma separated list of field/value filters, like `field: value, field: value, field: value`. An item is considered a match only if all the filters match.&#x20;

The `field` is the particular field/key of the data item to check. The `value` is the value to compare against. `value` can be:

* A plain string for an exact match.
* Blank to match unspecified fields.
* [Ruby-flavored regex](https://docs.ruby-lang.org/en/master/Regexp.html) string for more complex matching.

### Examples

| Filter string                    | Show items with...                                        |
| -------------------------------- | --------------------------------------------------------- |
| `role: programmer, alumni: true` | `role` equal to `programmer` AND `alumni` equal to `true` |
| `category:`                      | no specified `category`                                   |
| `description: .+`                | some specified/defined `description`                      |
| `date: ^2020`                    | `date` starting with `2020`                               |
| `role: ^(?!pi$)`                 | `role` NOT equal to `pi`                                  |
