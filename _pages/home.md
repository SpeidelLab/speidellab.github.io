---
title: "Speidel Lab"
layout: homelay
excerpt: ""
sitemap: false
permalink: /
carousels:
    - images: 
      - image: /images/homepic/IMG_8179.jpeg
      - image: /images/homepic/IMG_0971.jpeg
      - image: /images/homepic/DSC09860.JPG
---

<!--<div class="col-12 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}/images/homepic/PC081532.png" class="img-responsive" width="60%" style="float: center" />
</div>-->

<div class="col-xs-12" style="height:15px;"></div>

<div class="col-12 clearfix">
Welcome to the Mathematical Genomics Research Unit at <a href="https://www.riken.jp/en/" target="_blank" rel="noopener noreferrer">RIKEN</a>, Japan's national scientific research institute.<br/> 
We are part of the <a href="https://ithems.riken.jp/en" target="_blank" rel="noopener noreferrer">Center for Interdisciplinary Theoretical and Mathematical Sciences (iTHEMS)</a> and RIKEN <a href="https://www.riken.jp/en/careers/programs/riken_ecl/" target="_blank" rel="noopener noreferrer">Early Careers Leader Program</a>. 

Please get in touch if you're interested in joining us in Tokyo. See here for <a href="https://www.riken.jp/en/careers/programs/index.html" target="_blank" rel="noopener noreferrer">RIKEN-funded fellowships</a> and <a href="https://www.jsps.go.jp/english/e-fellow/" target="_blank" rel="noopener noreferrer">JSPS-funded fellowships</a> at PhD and postdoc level, in addition to positions funded directly by us.<br/>

数理遺伝学理研ECL研究ユニットの研究にご興味のある方は、どうぞお気軽にご連絡ください。

博士課程やポスドクへの応募を希望される方は、英語の履歴書をメールでお送りください。
当研究室の募集に加え、理化学研究所の<a href="https://www.riken.jp/careers/programs/spdr/index.html" target="_blank" rel="noopener noreferrer">「基礎科学特別研究員制度」</a>、<a href = "https://www.riken.jp/careers/programs/jra/jra2025/index.html" target="_blank" rel="noopener noreferrer">「JRA制度」</a>や、<a href="https://www.jsps.go.jp/j-pd/pd_sin.html" target="_blank" rel="noopener noreferrer">日本学術振興会（JSPS）</a>のフェローシップ制度もご確認ください。

<h3> Research interests </h3>
We are interested in developing powerful statistical tools that utilise the rapidly growing numbers of genomes of modern and ancient humans (or of other species) to reconstruct our shared genetic past. 

Our genomes can, for instance, inform us about past migrations, introgression with Neanderthals and other extinct hominids, and adaptation to environmental or lifestyle changes throughout human history. In particular, we are interested in understanding how evolutionary forces have shaped our genetic differences and how these may impact our health.

<b>Keywords</b>: Population Genetics, Evolutionary Biology, Ancestral Recombination Graphs, ancient DNA, population history, human origins, natural selection, mutation rate evolution, bacterial evolution, canid evolution, speciation, introgression

<h3> Software documentation </h3>

<div class="col-8 clearfix">
<div class="row">
{% for publi in site.data.highlights %}
<div class="col-md-4 mb-4">
<h5 style="font-weight: bold;">{{ publi.title }}</h5>
<a href="{{ publi.paperurl }}" target="_blank" rel="noopener noreferrer">
<img src="{{ site.url }}{{ site.baseurl }}/images/paperpic/{{ publi.image }}"
style="width: 100%; height: 300px; object-fit: contain; margin-bottom: 10px;"
alt="{{ publi.title }}" />
</a>
<p><a href="{{ publi.link.url }}" target="_blank" rel="noopener noreferrer">{{ publi.link.display }}</a></p>
{% if publi.resource %}
<p>Resources: <a href="{{ publi.resource.url }}" target="_blank" rel="noopener noreferrer">{{ publi.resource.display }}</a></p>
{% endif %}


</div>
{% endfor %}
</div>
</div>

<h3>News・お知らせ</h3>

<dl class="dl-horizontal">
{% for article in site.data.news limit:5 %}
<dt>{{ article.date }}</dt>
<dd> <a href="{{article.link}}" target="_blank" rel="noopener noreferrer">{{ article.headline }}</a> 
</dd>
{% endfor %}
</dl>
<h4><a href="{{ site.url }}{{ site.baseurl }}/allnews.html">... see all News</a></h4>

