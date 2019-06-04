---
title: "KLIV - Alumni"
layout: gridlay
excerpt: "KLIV Group at IIT Kharagpur"
sitemap: false
permalink: /alumni/
---

## Alumni

{% assign years = "2015,2016,2017" | split: ',' %}
{% for year in years reversed %}
<ul>
<li> <div style="font-size: 22px;">{{ year }}: </div> <br>
<ul>
<li> <div style="font-size: 22px;">B.Tech: </div> <br>
   <ol>
        {% for p in site.data.people %}
        {% if p.type == "alumni" and p.course == "B.Tech" %}
        {% if year contains p.year %}
            <li>
                <p style="font-size: 18px; text-align: justify;">
                <strong>{{ p.name }}</strong>{% if p.url.linkedin %} <a href="{{ p.url.linkedin }}" target="_blank"><img style="border:0px;margin:0px;" width="2%" src="{{ site.url }}{{ site.baseurl }}/images/icons/linkedin.png" /></a>{% endif %}
                {% if p.url.gscholar %} <a href="{{ p.url.gscholar }}" target="_blank"><img style="border:0px;margin:0px;" width="2%" src="{{ site.url }}{{ site.baseurl }}/images/icons/gscholar.png" /></a>{% endif %}<br /> {{ p.info }}<br /> <i>{{ p.award}}</i>
                </p>
            </li>
        {% endif %}
        {% endif %}
        {% endfor %}
   </ol>
</li>
  
<li> <div style="font-size: 22px;">M.Tech: </div> <br>
   <ol>
        {% for p in site.data.people %}
        {% if p.type == "alumni" and p.course == "M.Tech" %}
        {% if year contains p.year %}
            <li>
                <p style="font-size: 18px; text-align: justify;">
                <strong>{{ p.name }}</strong> {% if p.url.linkedin %} <a href="{{ p.url.linkedin }}" target="_blank"><img style="border:0px;margin:0px;" width="2%" src="{{ site.url }}{{ site.baseurl }}/images/icons/linkedin.png" /></a>{% endif %}
                {% if p.url.gscholar %} <a href="{{ p.url.gscholar }}" target="_blank"><img style="border:0px;margin:0px;" width="2%" src="{{ site.url }}{{ site.baseurl }}/images/icons/gscholar.png" /></a>{% endif %}<br /> {{ p.info }}<br /> <i>{{ p.award}}</i>
                </p>
            </li>
        {% endif %}
        {% endif %}
        {% endfor %}
   </ol>
</li>
</ul>

</li>
</ul>

{% endfor %}
<br />
