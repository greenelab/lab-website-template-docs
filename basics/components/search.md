---
description: A set of components and behaviors to search a page
---

# Search

The template can dynamically hide/filter [certain components](https://github.com/greenelab/lab-website-template/blob/main/js/search.js) on the page based on a search query. A search can happen in a few different ways:

| Method               | Description                                                                                                                                                        |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Search box component | Putting a search box component on a page with `{% include search-box.html %}` lets visitors type in their own searches.                                            |
| Tags component       | Clicking on a tag in the [tags](tags.md) component automatically searches a page for items that contain that tag.                                                  |
| Permalink            | Appending `?search=some search` to a page URL automatically runs a search on that page. See [team member aliases](../team-members.md) for a good use case of this. |

To show info about what items are being filtered, e.g. _Showing 12 of 60_, you can put a search info component on a page with `{% include search-info.html %}` (only visible if something is being searched).

## Search syntax

You can search for terms, phrases, and tags:

`term1 term2 "full phrase 1" "full phrase 2" "tag: some tag" "tag: another tag"`.

Items that contain **all of the terms**, **at least one of the phrases**, and **at least one of the tags** will be considered a match. Search words will be highlighted in the results (if they're longer than 2 characters). Matching is case insensitive.

