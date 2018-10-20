---
title: "KLIV - Whitepapers"
layout: gridlay
excerpt: "KLIV Group at IIT Kharagpur."
sitemap: true
permalink: /whitepapers/
---


# Blogs

<br>

Read the blogs written by the members of IIT KLIV Group. Any error/suggestion/requests are to submitted to awesomemail@mail.com

<br>

{% for post in site.posts %}

<div class="row">
<div class="clearfix">
 <div class="well">
  <h4><a href="{{ site.url }}{{ site.baseurl }}/{{ post.url }}">{{ post.title }}</a></h4>
  <img src="{{ site.url }}{{ site.baseurl }}/images/postpic/{{ post.thumbnail }}" class="img-responsive" width="20%" height="auto" style="float: left" />
  <p> {{ post.description }} </p>
  <p>Author(s): <em>{{ post.authors }}</em></p>
 </div>
</div>
</div>

{% endfor %}

<p> &nbsp; </p>
