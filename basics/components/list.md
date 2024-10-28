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
  filter="category == 'featured'"
  style="rich"
%}
```

<table><thead><tr><th width="162">Parameter</th><th>Description</th></tr></thead><tbody><tr><td><code>data</code></td><td>The <a href="../../advanced/data-and-collections.md">set of items</a> to loop through, e.g. <code>citations</code>, <code>posts</code>, <code>members</code>, etc. If your list has <code>date</code> fields, it is also sorted from newest to oldest, and grouped into sections by year.</td></tr><tr><td><code>component</code></td><td>The component to show for each item in the list. The fields in your <code>data</code> should match what this component takes as parameters (except for <code>style</code>, see below).</td></tr><tr><td><code>filter</code></td><td>Filter your <code>data</code> by arbitrary fields and values. See detailed explanation below.</td></tr><tr><td><code>style</code></td><td>A <code>style</code> parameter to automatically pass to every component in the list, so you don't have to repetitively set it on every <code>data</code> item. This is the only field that works this way, because all other fields are likely to be different for each item, but you usually want the <code>style</code> to be the same within a list.</td></tr></tbody></table>

Technically you can use [any](../../advanced/custom-components.md) structure of `data` and any `component` with the list component, but by default, the template comes with a [few placeholder data lists and matching components for common needs](../repo-structure.md#data-and-components).

## Filter

{% hint style="info" %}
**New syntax, v1.3.0+**
{% endhint %}

The **`filter`** parameter offers a flexible way to filter the items displayed by the list component. It can be any valid [Ruby expression](https://www.google.com/search?q=ruby+playground). For each item, if the expression is true, the item is shown; otherwise, it is hidden.

Your expression can get/check any field on any item in any `data` list. Simply refer to a field by its name, but in `snake_case` format (anything not a letter replaced with a `_`). You can also get a field by its unmodified name from  `item` (a hash). If the expression references something that isn't a field on the item, it will treat it as `nil` (null).

For example, if your `data` looked like this:

```yaml
# ... previous item

# current item filter is looking at
- id: abc
  Some-Field-123: "abc"

# ... another item
```

You could make references in your `filter` like this:

```ruby
# snake cased field name
Some_Field
# original field name
item['Some-Field-123']
# field perhaps present on other items, but not present on this item
optional_field # treated as `nil` (null)
```

### Examples

<table><thead><tr><th width="349">Filter expression</th><th>Show item if...</th><th>Example scenario</th></tr></thead><tbody><tr><td><code>repo</code></td><td>has some <code>repo</code> field</td><td><em>"Show my tools that have a repo link"</em></td></tr><tr><td><code>!id</code></td><td>has no <code>id</code> field</td><td><em>"Show my</em> <a href="../citations.md#manual-override"><em>manual citations</em></a><em>"</em></td></tr><tr><td><code>type == 'package' and category != 'featured'</code></td><td><code>type</code> is <code>package</code> and <code>category</code> is not <code>featured</code></td><td><em>"Show my secondary packages"</em> </td></tr><tr><td><code>role =~ /student/i</code></td><td><code>role</code> contains <code>student</code>, case-insensitive</td><td><em>"Show my students, of any level"</em></td></tr><tr><td><code>role =~ /^Senior/</code></td><td><code>role</code> starts with <code>senior</code>, case-sensitive</td><td><em>"Show my senior level members"</em></td></tr><tr><td><code>date.between?('2020', '2023')</code></td><td><code>date</code> is between <code>2020</code> and <code>2023</code> </td><td><em>"Show my papers published during COVID"</em></td></tr><tr><td><code>publisher.end_with?('Biology')</code></td><td><code>publisher</code> ends with <code>Biology</code></td><td><em>"Show my papers in major biology journals"</em></td></tr><tr><td><code>alumni ? name === 'Steve McQueen' : true</code></td><td>not <code>alumni</code> , or <code>alumni</code> where <code>name</code> is <code>Steve McQueen</code></td><td><em>"Hide my past members, unless they're super cool"</em></td></tr></tbody></table>

{% hint style="info" %}
References:

[/Regex/](https://en.wikipedia.org/wiki/Regular\_expression)

[Ruby string functions](https://ruby-doc.org/3.2.2/String.html#class-String-label-Methods+for+Querying)
{% endhint %}

Experiment with more advanced expressions:

{% embed url="https://try.ruby-lang.org/playground/#code=data+%3D+%5B%0A++%7B%22name%22+%3D%3E+%22Jane+Smith%22%2C+%22date%22+%3D%3E+%222015-01-01%22%7D%2C%0A++%7B%22name%22+%3D%3E+%22John+Smith%22%2C+%22date%22+%3D%3E+%222019-02-01%22%7D%2C%0A++%7B%22name%22+%3D%3E+%22Ada+Lovelace%22%2C+%22date%22+%3D%3E+%222020-03-01%22%2C+%22alumni%22%3D%3E+true%7D%2C%0A++%7B%22name%22+%3D%3E+%22Alan+Turing%22%2C+%22date%22+%3D%3E+%222024-04-01%22%2C+%22alumni%22%3D%3E+true%7D%2C%0A++%7B%22name%22+%3D%3E+%22Margaret+Hamilton%22%2C+%22date%22+%3D%3E+%222018-05-01%22%2C+%22alumni%22%3D%3E+true%7D%2C%0A%5D%0A%0Afilter+%3D+%22alumni+%3F+!name.start_with%3F('A')+%3A+true%22%0A%0A%0A%23%23%23%23%23%23%23%23%23%23%23%0A%0A%0Adef+empty_binding%0A++binding%0Aend%0A%0A%23+make+arbitrary+string+into+valid+ruby+variable+name%0Adef+safe_var_name(name)%0A++return+name.to_s.gsub(%2F%5B%5Ea-z%5D%2B%2Fi%2C+%22_%22).gsub(%2F%5E_%7C_%24%2F%2C+%22%22)%0Aend%0A%0A%23+filter+a+list+of+hashes%0Adef+data_filter(data%2C+filter)%0A++if+not+filter.is_a%3F(String)%0A++++return+data%0A++end%0A%0A++%23+filter+data%0A++return+data.clone.select%7B%0A++++%7Citem%7C%0A++++%23+start+with+empty+context+of+local+variables%0A++++b+%3D+empty_binding%0A++++%23+add+item+as+local+variable%0A++++b.local_variable_set(%22item%22%2C+item)%0A++++%23+also+set+each+item+field+as+local+variable+when+evaluating+filter%0A++++item.each+do+%7Cvar%2C+val%7C%0A++++++b.local_variable_set(safe_var_name(var)%2C+val)%0A++++end%0A++++%23+whether+to+keep+item%0A++++keep+%3D+true%0A++++while+true%0A++++++begin%0A++++++++%23+evaluate+expression+as+true%2Ffalse%0A++++++++keep+%3D+!!eval(filter%2C+b)%0A++++++++break%0A++++++++%23+if+a+var+in+expression+isn't+a+field+on+item%0A++++++rescue+NameError+%3D%3E+e%0A++++++++%23+define+it+and+re-evaluate%0A++++++++b.local_variable_set(safe_var_name(e.name)%2C+nil)%0A++++++end%0A++++end%0A++++%23+keep%2Fdiscard+item%0A++++keep%0A++%7D%0Aend%0A%0Afiltered+%3D+data_filter(data%2C+filter)%0A%0Afiltered.each+do+%7Citem%7C%0A++puts+item%0Aend&engine=cruby-3.2.0" %}

## Filters

{% hint style="danger" %}
**Old syntax, < v1.3.0**
{% endhint %}

The **`filters`** parameter is a comma separated list of field/value filters, like `field: value, field: value, field: value`. An item is considered a match only if **all of the filters match**.&#x20;

The `field` is the particular field/key of the data item to check. The `value` is the value to compare against. `value` can be:

* A plain string for a **partial** match.
* Blank to match unspecified fields.
* [Ruby-flavored regex](https://docs.ruby-lang.org/en/master/Regexp.html) string for more complex matching.

### Examples

| Filter string                    | Show items that have...                                       |
| -------------------------------- | ------------------------------------------------------------- |
| `role: programmer, alumni: true` | `role` containing `programmer` AND `alumni` containing `true` |
| `affiliation: ^CU$`              | `affiliation` EXACTLY equal to `CU`                           |
| `category:`                      | no specified `category`                                       |
| `description: .+`                | some specified/defined `description`                          |
| `date: ^2020`                    | `date` starting with `2020`                                   |
| `role: ^(?!pi$)`                 | `role` NOT equal to `pi`                                      |
