# Citations

Arguably the most important feature of this template is its ability to automatically generate citations from simple identifiers.&#x20;

The template is able to do this thanks to [**Manubot**](https://github.com/manubot/manubot#cite)**:**

{% embed url="https://manubot.org/" %}
Manubot is a suite of tools that (among many other things) lets you automatically generate a citation with full details from just a short identifier, like `doi`, `url`, `isbn`, `pmc`, `pmcid`, `pubmed`, `arxiv`, and [many many more](https://github.com/manubot/manubot/blob/main/manubot/cite/handlers.py#L155).
{% endembed %}

## Introduction

First let's define some consistent terminology to make things easier to explain:

* **source** - A paper, book, article, web page, film, or any other published item you want to cite.
* **metasource** - A single item that lists multiple sources, like how an author's [ORCID number](https://orcid.org/) can be used to get a list of their published works.
* **citation** - Detailed information about a source, like author(s), publisher, publish date, url, issue number, journal, etc.
* **cite process** - The automatic process the template has to run to convert your sources and metasources to citations.

{% hint style="info" %}
After running the cite process, you can **display** and **filter** **citations** on your site with the [list](../components/list.md) and [citation](../components/citation.md) components.
{% endhint %}

## How it works

1. In `/_data`, create as many source and metasource input `.yaml` files as you need, with the appropriate filename prefixes, e.g. `sources-2020.yaml`, `orcid-students.yaml`, etc.\
   _See filenames of examples below._
2. The cite process starts.
3. Each source/metasource file gets processed with the appropriate "cite plugin".
4. Metasource plugins like ORCID expand each entry the file into a list of regular sources.
5. A master list of sources is compiled, with duplicates removed (matched by `id`).
6. Manubot generates full citation details for each source.
7. A single `citations.yaml` file is generated to `/_data`.
8. The cite process finishes.
9. You **display** and **filter** **citations** on your site with the [list](../components/list.md) and [citation](../components/citation.md) components.

See examples below for filenames and behaviors of each cite plugin.

{% hint style="info" %}
**Do not edit `citations.yaml`!** This is the output of the cite process, and will get overwritten each time it is run. If you need to manually input or correct things, see below.
{% endhint %}

## Examples

### Basic id

{% code title="/_data/sources.yaml" %}
```yaml
- id: doi:10.1098/rsif.2017.0387
- id: pubmed:29424689
- id: pmc:PMC5640425
- id: arxiv:1806.05726
# ...more sources
```
{% endcode %}

| Parameter | Description                                                                                                                                                                                                                                                                |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id`      | Identifier for the source that [Manubot can understand and cite](https://github.com/manubot/manubot/blob/main/manubot/cite/handlers.py#L155). If Manubot is unable to generate a citation for this ID, the template will log an error message and exit with an error code. |

### Rich details

Optionally, you can manually pass extra "rich" details that Manubot can't determine that the template can display nicely.

{% code title="/_data/sources.yaml" %}
```yaml
- id: arxiv:1806.05726
  type: paper
  description: Lorem ipsum _dolor sit amet_.
  image: https://publisher.com/striking-image-for-your-paper.jpg
  buttons:
    - type: source
      link: https://github.com/your-lab/some-repo
    - type: website
      text: My Personal Website
      link: http://some-website.com/
  tags:
    - biology
    - big data
    - medicine
  repo: your-lab/some-repo

# ...another source
```
{% endcode %}

| Parameter     | Description                                                                                                                                           |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| `type`        | <p>The type of the source. Determines the icon to show.<br><br>See <code>/_data/types.yaml</code> for what types are built-in or to add your own.</p> |
| `description` | Brief description of the source. Supports Markdown.                                                                                                   |
| `image`       | URL to a striking image for the source. Highly recommended. Displays as a thumbnail next to the citation details.                                     |
| `buttons`     | List of [buttons](../components/button.md) to show underneath the citation details.                                                                   |
| `tags`        | List of [tags](../components/tags.md) to show underneath the citation details.                                                                        |
| `repo`        | GitHub repository to automatically fetch additional [tags](../components/tags.md) from.                                                               |

{% hint style="info" %}
Always provide a good thumbnail for your publications. Use a figure from the source, or if there are none, a journal logo or issue cover. [Here are some best practices for making a good thumbnail image](https://github.com/manubot/catalog#thumbnail-guidelines).
{% endhint %}

### Manual override

All fields you attach to a source (or metasource, see below) get passed through to the generated citation untouched. This allows you to manually input or correct details of a citation.&#x20;

{% code title="/_data/sources.yaml" %}
```yaml
# override specific citation detail
- id: pmc:PMC5640425
  publisher: Cold Spring Harbor

# manually provide all citation details
- title: Some Publication Title
  authors:
    - Steve McQueen
    - Lightning McQueen
  publisher: bioRxiv
  date: 2021-01-01
  link: biorxiv.org/1234

# attach an arbitrary field
- id: pmc:PMC5640425
  some-field: 123
```
{% endcode %}

|                            |                                                                                                                                                                                |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `title` / `authors` / etc. | Regular/basic citation information normally returned from Manubot and displayed by the [citation](../components/citation.md) component. Date should be in `YYYY-MM-DD` format. |

If you don't provide an `id`, Manubot has nothing to cite and so doesn't run. You'd only want to do this if manually providing all the citation details manually. This defeats the main benefit of the template, but sometimes necessary.

You can also attach any arbitrary field and it will be passed through. The template won't explicitly use it, but you can use it filter citations with the [list](../components/list.md) component.

### ORCID

[ORCID](https://orcid.org/) is the recommended way to retrieve a complete set of published works for an author.

{% code title="/_data/orcid.yaml" %}
```yaml
- orcid: 0000-0002-4655-3773
  some-field: 123

# ...another author
```
{% endcode %}



### PubMed



### Google Scholar

Unfortunately, Google does not provide APIs for many of its services, and that includes Scholar. Luckily there is a 3rd-party API to access it, [SerpAPI](https://serpapi.com/).

## Periodic updates

Metasources like ORCID update over time as you publish new works. As such, the template comes with a GitHub Actions scheduled/cron workflow that re-runs the cite process periodically. This will get the latest sources associated with your metasources, generate citations as normal, and open a pull request to let you review the changes before publishing them.

## Cache

If you have many sources, generating the citations for all of them can take a while. To save time, the cite process keeps a time-to-live cache for Manubot/ORCID/etc. network requests. If a cached response hasn't expired, it is used instead of making a new request. To clear this, simply delete the cache file in `_cite`. You can also customize the default expire times in the Python code in `_cite`.
