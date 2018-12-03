---
title: "KLIV - Vacancies"
layout: textlay
excerpt: "Openings"
sitemap: false
permalink: /vacancies
---

# Open positions
<br />

<ol>
{% for job in site.data.jobs %}
{% if job.open %}
    <li><p style="font-size: 20px;"> {{ job.title }} </p></li>
    <ul style="line-height: 1em;">
    	{% if job.project %}<li><p style="font-size: 16px;">Project: {{ job.project }}</p></li>{% endif %}
    	{% if job.dated %}<li><p style="font-size: 16px;">Reference Date: {{ job.dated }}</p></li>{% endif %}
    	{% if job.deadline %}<li><p style="font-size: 16px;">Deadline: {{ job.deadline }}</p></li>{% endif %}
    	{% if job.reference_no %}<li><p style="font-size: 16px;">Reference No.: {{ job.reference_no }}</p></li>{% endif %}
    	{% if job.description %}<li><p style="font-size: 16px;">Description: {{ job.description }}</p></li>{% endif %}
    	{% if job.qualifications %}<li><p style="font-size: 16px;">Qualification: {{ job.qualifications }}</p></li>{% endif %}
    	{% if job.no_of_vac %}<li><p style="font-size: 16px;">No. of vacancies: {{ job.no_of_vac }}</p></li>{% endif %}
    	{% if job.application_procedure %}<li><p style="font-size: 16px;">Application Procedure: {{ job.application_procedure }}</p></li>{% endif %}
    </ul>
{% endif %}
{% endfor %}
</ol>

<br /> <br />

<center>
<figure>
<img src="{{ site.url }}{{ site.baseurl }}/images/banner_2.png" width="75%">
</figure>
</center>
