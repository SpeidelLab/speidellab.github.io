---
title: "Speidel Lab - Publications"
layout: gridlay
excerpt: ""
sitemap: false
permalink: /publications/
---


# Publications

([Google Scholar](https://scholar.google.co.jp/citations?user=ohTuYdgAAAAJ&hl), [ORCiD](https://orcid.org/0000-0002-4644-8033))

## Full List

<div class="col-8 clearfix">
#### Journal papers + preprints
<ol>
{% for publi in site.data.publist.papers %}

  <li>
  <b>{{ publi.title }}</b> <br/>
  <em>{{ publi.authors }} </em><br />
  {% if publi.link %}
  <a href="{{ publi.link.url }}" target="_blank" rel="noopener noreferrer">{{ publi.link.display }}</a><br/>
  {% endif %}
	{% if publi.preprint %}
	Preprint: <a href="{{ publi.preprint.url }}" target="_blank" rel="noopener noreferrer">{{ publi.preprint.display }}</a><br/>
  {% endif %}
	{% if publi.code %}
  Code: <a href="{{publi.code}}" target="_blank" rel="noopener noreferrer"> {{publi.code}} </a><br/>
  {% endif %}
	{% if publi.data %}
	Data: <a href="{{publi.data}}" target="_blank" rel="noopener noreferrer"> {{publi.data}} </a><br/>
	{% endif %}
  {% if publi.news %}
  Featured in:
  <ul style="overflow: hidden">
  {% for n in publi.news %} 
  <li> <a href="{{n.link}}" target="_blank" rel="noopener noreferrer"> {{n.display}} </a> </li>
  {% endfor %}
  </ul>
  {% endif %}
  <br/>
  </li>

{% endfor %}
</ol>

#### Book chapters/thesis
<ol>
{% for publi in site.data.publist.books %}

<li>
<b>{{ publi.title }}</b> <br/>
<em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a><br/>
{% if publi.preprint %}
Preprint: <a href="{{ publi.preprint.url }}" target="_blank" rel="noopener noreferrer">{{ publi.preprint.display }}</a><br/>
{% endif %}
{% if publi.description %}
<ul style="list-style-type: '&#8627;'">
<li> {{publi.description}} </li>
</ul>
{% endif %}
{% if publi.code %}
Code: <a href="{{publi.code}}" target="_blank" rel="noopener noreferrer"> {{publi.code}} </a><br/>
{% endif %}
{% if publi.data %}
Data: <a href="{{publi.data}}" target="_blank" rel="noopener noreferrer"> {{publi.data}} </a><br/>
{% endif %}
{% if publi.news %}
Featured in:
<ul style="overflow: hidden">
{% for n in publi.news %} 
<li> <a href="{{n.link}}" target="_blank" rel="noopener noreferrer"> {{n.display}} </a> </li>
{% endfor %}
</ul>
{% endif %}
<br/>
</li>

{% endfor %}
</ol>

#### Misc
<ol>
{% for publi in site.data.publist.others %}

<li>
<b>{{ publi.title }}</b> <br/>
<em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}" target="_blank" rel="noopener noreferrer">{{ publi.link.display }}</a><br/>
{% if publi.preprint %}
Preprint: <a href="{{ publi.preprint.url }}" target="_blank" rel="noopener noreferrer">{{ publi.preprint.display }}</a><br/>
{% endif %}
{% if publi.description %}
<ul style="list-style-type: '&#8627;'">
<li> {{publi.description}} </li>
</ul>
{% endif %}
{% if publi.code %}
Code: <a href="{{publi.code}}" target="_blank" rel="noopener noreferrer"> {{publi.code}} </a><br/>
{% endif %}
{% if publi.data %}
Data: <a href="{{publi.data}}" target="_blank" rel="noopener noreferrer"> {{publi.data}} </a><br/>
{% endif %}
{% if publi.news %}
Featured in:
<ul style="overflow: hidden">
{% for n in publi.news %} 
<li> <a href="{{n.link}}" target="_blank" rel="noopener noreferrer"> {{n.display}} </a> </li>
{% endfor %}
</ul>
{% endif %}
<br/>
</li>

{% endfor %}
</ol>


</div>

<script>
var coll = document.getElementsByClassName("collapsible");
var i;

for (i = 0; i < coll.length; i++) {
  coll[i].addEventListener("click", function() {
    this.classList.toggle("active");
    var content = this.nextElementSibling;
    if (content.style.maxHeight){
      content.style.maxHeight = null;
    } else {
      content.style.maxHeight = content.scrollHeight + "px";
    }
  });
}
</script>
