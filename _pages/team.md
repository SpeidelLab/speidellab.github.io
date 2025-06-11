---
title: "Speidel Lab - about"
layout: gridlay
excerpt: ""
sitemap: false
permalink: /team/
---

<h1> Members </h1>

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% assign anchor_id = member.name | slugify %}

{% if even_odd == 0 %}
<div class="row" id="{{ anchor_id }}">
{% endif %}

<div class="col-sm-11 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="13%" style="float: left" />
  <h4 class="linkable-heading">{{ member.name }} <a href="#{{ anchor_id }}" class="anchor-link" aria-label="Link to this section">🔗</a> </h4>
  {{member.role}}<br/>
  {% if member.info %}{{ member.info }}{% endif %}

  {{member.details}}<br/>
  {% if member.google %} <a href="{{ member.google.url }}" target="_blank" rel="noopener noreferrer">Google scholar</a>,
  <a href="{{ member.orcid.url }}" target="_blank" rel="noopener noreferrer">ORCID</a><br/>
  {% endif %} {% if member.email %} <i>Email: <{{ member.email }}></i><br/>
  {% endif %}
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}

  {% if member.number_educ == 6 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  <li> {{ member.education6 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


<h1> Group alumni </h1>

{% assign number_printed = 0 %}
{% for member in site.data.alumni %}
<div class="col-sm-11 clearfix">
<p>{{ member.name }}, {{member.role}}, {{member.details}}</p>
</div>

{% endfor %}

