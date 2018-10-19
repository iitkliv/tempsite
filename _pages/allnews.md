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
<p>
    [{{ article.date }}]
    <br>
    {{ article.headline }}
</p>
<hr style="height:1px; border:none; background-color:#aaaaaa;" />
{% endfor %}
