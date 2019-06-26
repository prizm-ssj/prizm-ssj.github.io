---
layout: list
title: Works list
describe: 코드 작업은 code, 그래픽 작업은  non_code <br> 짧은 작업은 toy_project 그 이상은 long_project
permalink: /works/index.html
---
<ul>
{% assign sorted = (site.works | sort:'date') | reverse %}
{% for item in sorted%}
<li> 
<h2><a href="{{ item.url }}">{{ item.title }}</a></h2>
<h3>
{% for each in item.categories %}
<span>{{each}}</span>
{% endfor %}
</h3>
<h4>{{item.date | date: "%Y-%m-%d"}}</h4>
</li>
{% endfor %}
</ul>
