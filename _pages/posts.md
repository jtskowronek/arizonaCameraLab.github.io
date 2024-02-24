---
title: "Posts"
layout: gridlay
permalink: /posts/
excerpt: "posts."
title: "Posts"
description:
nav: true
toc: true
---

<br>

<div class="content list">
{% for post in site.posts %}
<div class="list-item">
<div class="row">
<div class="col-sm-4">
<img src="{% if post.header-img %}{{ site.baseurl }}/assets/images/post/{{ post.header-img }}{% else %} {{ site.baseurl }}/assets/images/post/dummy.png {% endif %}" style="width:100%;">
</div>
<div class="col-sm-8">
<h3 class="post-title"><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h3>
<p class="list-post-title"> {{ post.date | date: "%B %-d, %Y" }}</p>
<p class="list-detail" >{{ post.content | strip_html | truncatewords:30 }}</p>
</div>
</div>
</div>
<hr>
{% endfor %}
</div>
