---
title: "News"
layout: textlay
sitemap: false
permalink: /allnews.html
---

## News

{% for article in site.data.news %}
<p style="text-align:justify">{{ article.date }} <br> {{ article.headline | markdownify}}</p>
<br>
{% endfor %}
