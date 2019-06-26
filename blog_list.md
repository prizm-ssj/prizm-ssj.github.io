---
layout: default
title: blog posts list
permalink: /blog/index.html
---
{% for item in site.blog %}
<h3>{{item.date | date: "%Y-%m-%d"}}</h3>
<h2><a href="{{ item.url }}">{{ item.title }}</a></h2>
<p>{{ item.content | strip_html | truncatewords:20  }}</p>
{% endfor %}
