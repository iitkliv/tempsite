---
title: "News"
layout: textlay
excerpt: "KLIV at IIT Kharagpur"
sitemap: false
permalink: /allnews.html
---

# News
<hr style="height:1px; border:none; background-color:#aaaaaa;" />
{% for article in site.data.news %}
<center><p>
    [{{ article.date }}]
    <br>
    {{ article.headline }}
    {% if article.thumbnail %}
    <center>
    	<img src="{{ site.url }}{{ site.baseurl }}/images/news/{{ article.thumbnail }}" class="img-responsive" />
	</center>
    {% endif %}
</p></center>
<hr style="height:1px; border:none; background-color:#aaaaaa;" />
{% endfor %}
