---
title: "News"
layout: textlay
excerpt: "Neural Pathways Lab at the University of Sheffield."
sitemap: false
permalink: /allnews.html
---

## News

{% for article in site.data.news %}
<p>**{{ article.date }}** <br> {{ article.headline | markdownify}}</p>
{% endfor %}
