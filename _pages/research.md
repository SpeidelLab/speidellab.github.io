---
title: "Speidel Lab - Research"
layout: textlay
excerpt: ""
sitemap: false
permalink: /research/
---

{% assign number_printed = 0 %}
{% for publi in site.data.research %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12 clearfix">
 <div class="well" style="min-height:21em">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/respic/{{ publi.image }}" class="img-responsive" width="48%" style="float: left; max-width: 100%; max-height: 100%; object-fit: contain;" />
	{% if publi.japanese %}
  <p style="text-align:right"><i><a href="{{ publi.japanese.url }}" target="_blank" rel="noopener noreferrer">{{ publi.japanese.display }}</a></i></p> 
	{% endif %}
  <p>{{ publi.description }}</p>
  <p><strong><a href="{{ publi.link.url }}" target="_blank" rel="noopener noreferrer">{{ publi.link.display }}</a></strong></p>
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

<p> &nbsp; </p>

