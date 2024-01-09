---
title: "Hydroinformatics Group - Team"
layout: gridlay
excerpt: "Hydroinformatics Group -- Team"
sitemap: false
permalink: /team/
---

### Current Team
{% assign number_printed = 0 %}
{% for member in site.data.team %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br />email: {{ member.email }}{% if member.website %} <br /> {{ member.website }} {% endif %}</i>

  {% if member.number_educ == 1 %}
  <p>{{ member.education1 }} </p>
  {% endif %}

  {% if member.number_educ == 2 %}
  <p> {{ member.education1 }} <br />
  {{ member.education2 }} </p>
  {% endif %}

  {% if member.number_educ == 3 %}
  <p> {{ member.education1 }} <br />
  {{ member.education2 }} <br />
  {{ member.education3 }} </p>
  {% endif %}

  {% if member.number_educ == 4 %}
  <p> {{ member.education1 }} </li>
  {{ member.education2 }} <br />
  {{ member.education3 }} <br />
  {{ member.education4 }} </p>
  {% endif %}

  <p>{{ member.statement }} </p>
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

### Alumni
{% assign number_printed = 0 %}
{% for member in site.data.alumni %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>

  {% if member.number_educ == 1 %}
  <p>{{ member.education1 }}</p>
  {% endif %}

  {% if member.number_educ == 2 %}
  <p>{{ member.education1 }} <br />
  {{ member.education2 }} </p>
  {% endif %}

  {% if member.number_educ == 3 %}
  <p>{{ member.education1 }} <br />
  {{ member.education2 }} <br />
  {{ member.education3 }} </p>
  {% endif %}

  {% if member.number_educ == 4 %}
  <p>{{ member.education1 }} <br />
  {{ member.education2 }} <br />
  {{ member.education3 }} <br />
  {{ member.education4 }} </p>
  {% endif %}

  <p>{{ member.statement }} </p>
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
