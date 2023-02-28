# Set up your site

There are two ways to start your copy of the template from [GitHub](https://github.com/greenelab/lab-website-template): **generating** or **forking**. They each have pros and cons:

|        | Generate (recommended)                                                                                                   | Fork                                                                                                                                                                                                                                                                                                                                |
| ------ | ------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|        | <img src="../.gitbook/assets/106949308-c4877180-66fa-11eb-9300-9468cb8a6aaa.png" alt="" data-size="line">                | <img src="../.gitbook/assets/106949309-c4877180-66fa-11eb-86fd-d0a2741e49d0 (1).png" alt="" data-size="line">                                                                                                                                                                                                                       |
| _Pros_ | <ul><li>Clean commit and Actions history; a "fresh start".</li><li>Can have multiple per user/organization.</li></ul>    | <ul><li>A bit easier to <a href="../advanced/update-your-template.md">update your version of the template</a>.</li></ul>                                                                                                                                                                                                            |
| _Cons_ | <ul><li>A bit harder to <a href="../advanced/update-your-template.md">update your version of the template</a>.</li></ul> | <ul><li>You get <a href="https://github.com/greenelab/lab-website-template/commits/main">the development history of the template</a> in your repo's commit and Actions history.</li><li>Can only have one per user/organization.</li><li><a href="https://github.com/orgs/community/discussions/11729">Accidental PRs</a></li></ul> |

Once you decide which approach to take, follow the appropriate setup steps below. We've tried to automate this setup for you as much as possible, within the limitations of GitHub!

{% tabs %}
{% tab title="Generate" %}
1. [Generate a new repo from this template under your account](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template) with the <img src="https://user-images.githubusercontent.com/8326331/106949308-c4877180-66fa-11eb-9300-9468cb8a6aaa.png" alt="Use this template" data-size="line"> button.
   1. Name your repo something like `your-lab-website` to avoid confusion with the template itself.
   2. Set the repo to "Public" visibility.
   3. Uncheck "Include all branches".
2. In your repo's "▶️ Actions", find the "first time setup" workflow and [run it manually](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow). Wait for it to complete (\~30 seconds).
3. In your repo's "⚙️ Settings", [set GitHub Pages to build/publish from](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) the `gh-pages` branch. Wait for the first build of your site to complete (\~3 minutes, multiple Actions workflows will run).
4. In your repo's "⚙️ Settings", [allow GitHub Actions to create pull requests](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/managing-github-actions-settings-for-a-repository#preventing-github-actions-from-creating-or-approving-pull-requests).
5. Your repo should be initialized and your site should be live! Check your readme for the link.
{% endtab %}

{% tab title="Fork" %}
1. [Fork this repo under your account](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo) with the <img src="https://user-images.githubusercontent.com/8326331/106949309-c4877180-66fa-11eb-86fd-d0a2741e49d0.png" alt="Fork" data-size="line"> button.
   1. Name your repo something like `your-lab-website` to avoid confusion with the template itself.
   2. Check "Copy the `main` branch only".
2. In your repo's "▶️ Actions", acknowledge the warning and enable Actions workflows.
3. In your repo's "▶️ Actions", find the "first time setup" workflow and [run it manually](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow). Wait for it to complete (\~30 seconds).
4. In your repo's "⚙️ Settings", [set GitHub Pages to build/publish from](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) the `gh-pages` branch. Wait for the first build of your site to complete (\~3 minutes, multiple Actions workflows will run).
5. In your repo's "⚙️ Settings", [allow GitHub Actions to create pull requests](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/managing-github-actions-settings-for-a-repository#preventing-github-actions-from-creating-or-approving-pull-requests).
6. Your repo should be initialized and your site should be live! Check your readme for the link.
{% endtab %}
{% endtabs %}

{% hint style="info" %}
A lot of the automation in this template relies on GitHub Actions, which sometimes (very rarely) [goes down](https://www.githubstatus.com/). Be aware of this in case a process in the template ever fails.
{% endhint %}

{% hint style="info" %}
GitHub frequently changes and rearranges its web interface, so you may notice slight discrepancies in the instructions above. We've tried to write the instructions more abstractly, linking to GitHub's official documentation for more details.
{% endhint %}
