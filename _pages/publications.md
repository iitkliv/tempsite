---
title: "KLIV - Publications"
layout: gridlay
excerpt: "KLIV Group at IIT Kharagpur."
sitemap: false
permalink: /publications/
---


# Publications

<br>

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  {% if publi.image %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="50%" style="float: left" />
  {% else %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/default.png" class="img-responsive" width="60%" style="float: left" />
  {% endif %}
  <p style="font-size: 13px; text-align: justify;">{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
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

## Full list of publications
(You may also visit the [Google Scholar](https://scholar.google.com/citations?user=x-0vLSsAAAAJ&hl=en) page)

{% assign years = "2014,2015,2016,2017,2018,2019" | split: ',' %}
{% for year in years reversed %}
<ul>
  <li> <div style="font-size: 22px;">{{ year }}: </div> <br>
    <ol>
        {% for pub in site.data.publist %}
        {% if year contains pub.year %}
            <li>
                <p style="font-size: 17px; text-align: justify;">
                {{ pub.authors }}, "{{ pub.title }}", <a href="{{ pub.link.url }}" target="_blank"><i>{{ pub.link.display }}</i></a> {% if pub.pp %}{{ pub.pp }}{% endif %}
                </p>
            </li>
        {% endif %}
        {% endfor %}
    </ol>
  </li>
</ul>
{% endfor %}

<p> &nbsp; </p>
