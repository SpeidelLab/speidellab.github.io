---
title: "News"
layout: textlay
excerpt: ""
sitemap: false
permalink: /allnews.html
---

{% for article in site.data.news %}
<p>{{ article.date }} <br>
<em><a href="{{article.link}}">{{ article.headline }}</a></em>

</p>
{% endfor %}
