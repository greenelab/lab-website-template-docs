# Update your template

If the template [has been updated](https://github.com/greenelab/lab-website-template/commits/main) since you first created your website from it, you may want to pull in the updates.&#x20;

{% hint style="info" %}
Because this is a template, and not a cleanly-separated installable package, updating it can unfortunately be a little difficult. We can [help you](../introduction/support.md) if you have trouble.
{% endhint %}

## Begin a merge

First, begin a merge of the latest template repo into your website repo. The method to do this depends on [whether you generated or forked from the template](../getting-started/set-up-your-site.md):

{% tabs %}
{% tab title="Generated" %}
Based on [this post](https://stackoverflow.com/questions/56577184/github-pull-changes-from-a-template-repository):

```bash
git remote add template https://github.com/greenelab/lab-website-template
git fetch --all
git merge template/main --allow-unrelated-histories
```
{% endtab %}

{% tab title="Forked" %}
Based on [this article](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork):

```bash
git fetch upstream
git merge upstream/main
```
{% endtab %}
{% endtabs %}

## Resolve merge conflicts

After you've started a merge, you'll mostly likely have to resolve some merge conflicts.&#x20;

If you **generated** your website, you'll have to resolve all of the conflicts manually. This is because generating from a template starts a completely new, unrelated Git repo with no shared commit history, so Git has a difficult time automating the process.

If you **forked** your website, the process should be a little bit easier, but you'll still probably have to manually resolve some conflicts.

We'll assume you already know how to [perform a merge conflict resolution in your Git interface of choice](https://code.visualstudio.com/docs/sourcecontrol/overview#\_merge-conflicts).&#x20;

The hard part is carefully picking out which changes to accept. This essentially boils down to distinguishing between **template code** ("under-the-hood") and **content code** (for your specific website). For template code, you want to "accept incoming changes" (pull in updates from the template). For content code, you want to "accept current changes" (keep the current content in your repo).

**In general**, here's how the files and folders in the template fall into these two categories. We've tried to keep these two separated in the [repo structure](repo-structure.md) as possible (within the limitations of Jekyll). Note that if you've made modifications to template code (e.g. tweaking the appearance of a component), you'll have to judiciously decide where and how to merge in the updates.

| Template code                                                                                                             | Content code                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Folders that start with `_` ...except for :point\_right:                                                                  | <p><code>/_data</code> </p><p><code>/_members</code> </p><p><code>/_posts</code></p><p><code>/_styles/theme.scss</code></p> |
| Folders that start with `.`                                                                                               |                                                                                                                             |
| <p><code>CITATION.cff</code></p><p><code>LICENSE.md</code></p><p><code>Gemfile</code></p><p><code>Gemfile.lock</code></p> | <p><code>/blog</code><br><code>/images</code><br><code>/team</code><br>etc.<br><code>index.md</code></p>                    |

{% hint style="warning" %}
This process is very tricky, even for the maintainers of this template. When doing this, carefully check every page and section on your site before publishing the changes.
{% endhint %}
