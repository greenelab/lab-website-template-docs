# Analytics

{% hint style="info" %}
Analytics scripts might not be as useful as you think, as most ad blocker extensions now prevent them from working, potentially limiting your data to only a small subset of your visitors.
{% endhint %}

There are many available analytics services, the most well-known being Google Analytics. They each work slightly differently, but they all should have a way to obtain a snippet of code that you can paste into the pages you want to track.

The snippet will generally look something like this, a minimal `<script>` with an ID unique to you:

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-XXXXXXXX-X"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'UA-XXXXXXXX-X');
</script>
```

Once you've found this code snippet, paste it into `/_includes/analytics.html` to include it on every page on your site.
