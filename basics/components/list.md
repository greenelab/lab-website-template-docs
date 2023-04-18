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

| Parameter   | Description                                                                                                                                                                                                                                                                                                 |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `data`      | The [set of items](../../advanced/data-and-collections.md) to loop through, e.g. `citations`, `posts`, `members`, etc. If your list has `date` fields, it is also sorted from newest to oldest, and grouped into sections by year.                                                                          |
| `component` | The component to show for each item in the list. The fields in your `data` should match what this component takes as parameters (except for `style`, see below).                                                                                                                                            |
| `filters`   | Filter your `data` by arbitrary fields and values. See detailed explanation below.                                                                                                                                                                                                                          |
| `style`     | A `style` parameter to pass through to every component in the list, so you don't have to repetitively set it on every `data` item. This is the only field that works this way, because all other fields are likely to be different for each item, but you'll likely always want the same `style` parameter. |

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
