# Update your template

If the template has been updated since you first created your website from it, you may want to pull in the updates.&#x20;

✨ [LATEST VERSION](https://github.com/greenelab/lab-website-template/blob/main/CITATION.cff)&#x20;

📋 [CHANGELOG](https://github.com/greenelab/lab-website-template/blob/main/CHANGELOG.md)

{% hint style="info" %}
Because this is a template and not an installable package, updating it can unfortunately be a little difficult. We can [help you](../introduction/support.md) if you have trouble.
{% endhint %}

## From pre-release

If you are coming from a pre-release version of the template (< `v1.0.0`), we **strongly recommend** just starting from scratch and not even attempting the merge instructions below. It will be quicker, easier, and less error-prone. Forget everything you know, start a new copy of the template, read through and follow the new docs, and judiciously copy and modify code from your old site into your new site. _We know this is frustrating_, but we think the upgrade is worth it.

If you can't or don't want to start from scratch, go through the merge instructions below, then go run the [setup instructions](../getting-started/set-up-your-site.md) and [custom domain instructions](../getting-started/set-up-your-url.md) if applicable.

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

The hard part is carefully picking out which changes to accept. This essentially boils down to distinguishing between [template content and user content](../basics/repo-structure.md). For template content, you want to "accept incoming changes" (pull in updates from the template). For user content, you want to "accept current changes" (keep the current content in your repo).

Sometimes updates to the template will be "breaking changes" and will affect your user content, like a component parameter being renamed. You may have also made modifications to template code, like tweaking the appearance of a component. In these cases, you'll have to judiciously decide how or if to merge in the updates.

{% hint style="warning" %}
This process is very tricky, even for the maintainers of this template. When doing this, carefully check every page and section on your site before publishing the changes.
{% endhint %}
