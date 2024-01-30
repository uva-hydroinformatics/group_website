---
title: "Hydroinformatics Group - Publications"
layout: gridlay
excerpt: "Hydroinformatics Group -- Publications"
sitemap: false
permalink: /publications/
---


# Publications

 For a complete list of publications, please see [Jon Goodall's Google Scholar Profile](https://scholar.google.com/citations?sortby=pubdate&user=M9aKXDwAAAAJ). Preprints are available for papers not published as open access, in accordance with the copyright license from the journal.

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
  <pubtit><strong>{{ publi.title }}</strong></pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
{% if publi.linkpdf %}
  ~  
{% endif %}
<a href="{{ publi.linkpdf.pdf }}">{{ publi.linkpdf.display }}

  </a></p>
  <p class="text-danger">{{ publi.news1 }}</p>
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
  <h5><b>{{publi.title}}</b></h5>
  <em>{{ publi.authors }}</em><br />
  {{ publi.description }}, {{publi.date}}<br />
  <a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
  {% if publi.linkpdf.pdf %} ~  <a href="{{ publi.linkpdf.pdf }}">{{ publi.linkpdf.display }}</a> {% endif %}
  {{ publi.news2 }}
{% endfor %}
