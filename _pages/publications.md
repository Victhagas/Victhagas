---
title: "Neural Pathways Lab - Publications"
layout: gridlay
sitemap: false
permalink: /publications/
---

<div style="margin-top: 45px;">

### Publications
</div>

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix" style="text-align: justify;">
 <div class="well" style="margin-top:16px">
  <pubtit>{{ publi.title }}</projtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ proj.image }}" class="img-responsive" width="33%" style="float: left;" />
  <p>{{ proj.description }}</p>
  <p><em>{{ proj.authors }}</em></p>
  <p><strong><a href="{{ proj.link.url }}">{{ proj.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ proj.news1 }}</strong></p>
  <p> {{ proj.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

### Full List of publications

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
