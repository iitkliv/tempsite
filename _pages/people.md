---
title: "KLIV - People"
layout: gridlay
excerpt: "KLIV Group at IIT Kharagpur"
sitemap: false
permalink: /people/
---

# People

 **We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**

## Principal Investigator
{% for member in site.data.people %}
{% if member.type == "head" %}

<div class="row">
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br>email: <{{ member.email }}></i>
  <ul style="overflow: hidden">

  {% for line in member.description %}
  <li> {{ line }} </li>
  {% endfor %}
  <a href="{{ member.url.gscholar }}" target="_blank"><img  width="7%" src="{{ site.url }}{{ site.baseurl }}/images/icons/gscholar.png" /></a>
  <a href="{{ member.url.linkedin }}" target="_blank"><img  width="7%" src="{{ site.url }}{{ site.baseurl }}/images/icons/linkedin.png" /></a>
  <a href="{{ member.url.github }}" target="_blank"><img width="8%" src="{{ site.url }}{{ site.baseurl }}/images/icons/github.png" /></a>
  <a href="{{ member.url.researchgate }}" target="_blank"><img width="8%" src="{{ site.url }}{{ site.baseurl }}/images/icons/rg.png" /></a>
  </ul>
</div>
</div>

{% endif %}
{% endfor %}

## Members
{% assign number_printed = 0 %}
{% for member in site.data.people %}
{% if member.type == "member" %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br>email: <{{ member.email }}></i>
  <ul style="overflow: hidden">

  {% for line in member.description %}
  <li> {{ line }} </li>
  {% endfor %}
  {% if member.url.gscholar %}<a href="{{ member.url.gscholar }}" target="_blank"><img width="7%" src="{{ site.url }}{{ site.baseurl }}/images/icons/gscholar.png" /></a>{% endif %}
  {% if member.url.linkedin %} <a href="{{ member.url.linkedin }}" target="_blank"><img width="7%" src="{{ site.url }}{{ site.baseurl }}/images/icons/linkedin.png" /></a>{% endif %}
  {% if member.url.github %} <a href="{{ member.url.github }}" target="_blank"><img width="8%" src="{{ site.url }}{{ site.baseurl }}/images/icons/github.png" /></a>{% endif %}
  {% if member.url.researchgate %} <a href="{{ member.url.researchgate }}" target="_blank"><img width="8%" src="{{ site.url }}{{ site.baseurl }}/images/icons/rg.png" /></a>{% endif %}
  </ul>
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




## Student Members
{% assign number_printed = 0 %}
{% for member in site.data.people %}
{% if member.type == "undergrad" %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br>email: <{{ member.email }}><br>{% if member.url %} URL: <a href="{{ member.url }}" target="_blank">LinkedIn</a> {% endif %}</i>
  <ul style="overflow: hidden">

  {% for line in member.description %}
  <li> {{ line }} </li>
  {% endfor %}
 
  {% if member.Linkedin %} <a href="{{ member.Linkedin }}" target="_blank"><img width="7%" src="{{ site.url }}{{ site.baseurl }}/images/icons/linkedin.png" /></a>{% endif %}
  </ul>
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

## Administrative Support

{% assign number_printed = 0 %}
{% for member in site.data.people %}
{% if member.type == "support" %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br>email: <{{ member.email }}><br>{% if member.url %} URL: <a href="{{ member.url }}" target="_blank">LinkedIn</a> {% endif %}</i>
  <ul style="overflow: hidden">

  {% for line in member.description %}
  <li> {{ line }} </li>
  {% endfor %}

  </ul>
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

## Alumni

<div style="font-size:20px;"> → <a href="{{ site.url }}{{ site.baseurl }}/alumni/" target="_blank">list of all our alumni</a>.

<br> <br>
