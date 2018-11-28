---
title: "KLIV - Projects"
layout: textlay
excerpt: "KLIV Group at IIT Kharagpur"
sitemap: false
permalink: /projects/
---

# Projects

<br>

### Ongoing
<br>
<ul>
{% assign count = 0 %}
{% for proj in site.data.projects %}
{% if proj.status == "ongoing" %}
    <li>
        <p style="font-size: 20px;">
        {{ proj.name }} (Sponsor: {{ proj.sponsor }})
        </p>
    </li>
{% endif %}
{% endfor %}
</ul>
<br>
### Completed
<br>
<ul>
{% assign count = 0 %}
{% for proj in site.data.projects %}
{% if proj.status == "completed" %}
    <li>
        <p style="font-size: 20px;">
        {{ proj.name }} (Sponsor: {{ proj.sponsor }})
        </p>
    </li>
{% endif %}
{% endfor %}
</ul>

<br> <br>