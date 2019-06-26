---
layout: default
title: work projects list
permalink: /works/index.html
---
<ul class="list">
{% assign sorted = (site.works | sort:'date') | reverse %}
{% for item in sorted%}
<li>
<h3>
{% for each in item.categories %}
<span>{{each}}</span>
{% endfor %}
</h3>
<h2><a href="{{ item.url }}">{{ item.title }}</a></h2>  
<h4>{{item.date | date: "%Y-%m-%d"}}</h4>
</li>
{% endfor %}
</ul>
