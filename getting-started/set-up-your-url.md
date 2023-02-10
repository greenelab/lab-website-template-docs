# Set up your URL

GitHub Pages gives you a few options for where your live site appears:

{% tabs %}
{% tab title="Custom Domain (recommended)" %}
Example URL: `your-custom-domain.com`

Purchasing a custom domain is highly recommended. It looks professional, it's easier to remember and type, and it's easy and cheap to set up (`.com`s are usually only about $10 per year).

Follow the [instructions here](https://docs.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain). In summary:

1. Purchase a domain name from a reputable service.
2. Point your domain name provider to GitHub Pages using an `A` record. This is slightly different for each provider; they should have their own instructions on how to do it.
3. Set the `custom domain` field in your repo's "[⚙️](https://emojipedia.org/gear/) Settings".
{% endtab %}

{% tab title="User/org Site" %}
Example URL: `your-lab.github.io`

...where `your-lab` is your GitHub user/organization name.

Rename your repo to `your-lab.github.io`, and that's it!
{% endtab %}

{% tab title="Project site (default)" %}
Example URL: `your-lab.github.io/your-lab-website`

...where `your-lab` is your GitHub user/organization name, and `your-lab-website` is the repo name you chose.

This is where your live site appears by default when you enable GitHub Pages.
{% endtab %}
{% endtabs %}

After making any needed changes above, wait a bit (\~30 seconds to 3 minutes) for your live site to redeploy to its new location. (You can check your repo's "[▶️](https://emojipedia.org/play-button/) Actions" for status.)
