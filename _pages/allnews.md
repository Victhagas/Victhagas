---
title: "News"
layout: textlay
excerpt: "Neural Pathways Lab at the University of Sheffield."
sitemap: false
permalink: /allnews.html
---

## News

{% for article in site.data.news %}
**{{ article.date }}** <br> {{ article.headline | markdownify}} <br> {{ article.link | markdownify}}>
{% endfor %}
