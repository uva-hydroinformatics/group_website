---
title: "Hydroinformatics Group - Publications"
layout: gridlay
excerpt: "Hydroinformatics Group -- Publications"
sitemap: false
permalink: /publications/
---


# Selected Publications

 For citation data and an up to date list of all publications, please see Jon Goodall's [Google Scholar Profile](https://scholar.google.com/citations?sortby=pubdate&user=M9aKXDwAAAAJ). If final papers are published in a journal without open access, the preprint manuscript (the version of the manuscript before final edits and typesetting were completed) is provided in accordance with the copyright license from the journal.

<!--
## Highlights

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong>  
{% if publi.linkpdf %}
  ~  
{% endif %}
<strong><a href="{{ publi.linkpdf.pdf }}">{{ publi.linkpdf.display }}

  </a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
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


## Full List -->

{% for publi in site.data.publist %}
  <hr>
  <h5>{{publi.title}}</h5>
  <em>{{ publi.authors }}</em><br />
  <b>{{ publi.description }}</b>, {{publi.date}}<br />
  <a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
  {% if publi.linkpdf.pdf %} ~  <a href="{{ publi.linkpdf.pdf }}">{{ publi.linkpdf.display }}</a> {% endif %}
  {{ publi.news2 }}
{% endfor %}
