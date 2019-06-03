---
title: "KLIV - Alumni"
layout: gridlay
excerpt: "KLIV Group at IIT Kharagpur"
sitemap: false
permalink: /alumni/
---

## Alumni

{% assign years = "2015,2016,2017,2018,2019" | split: ',' %}
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
                <p style="font-size: 15px; text-align: justify;">
                <strong>{{ p.name }}</strong> <br /> {{ p.info }} <br /> <i>{{ p.award}}</i>
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
                <p style="font-size: 15px; text-align: justify;">
                <strong>{{ p.name }}</strong> <br /> {{ p.info }} <br /> <i>{{ p.award}}</i>
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
