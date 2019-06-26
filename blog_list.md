---
layout: list
title: blog posts list
permalink: /blog/index.html
describe: 공유할 만한 자료들
---
<ul>
{% assign sorted = (site.blog | sort:'date') | reverse %}
{% for item in sorted%}
<li> 
<h2><a href="{{ item.url }}">{{ item.title }}</a></h2>
<p>{{ item.content | strip_html | truncatewords:20  }}</p>
<h4>{{item.date | date: "%Y-%m-%d"}}</h4>
</li>
{% endfor %}
</ul>
