---
layout: apollo
title: "Portfolio"
description: ""
---

{% assign work = site.work | sort: 'date' | reverse %}
<ul class="posts">
{% for item in page.items | sort: 'name' %}
<li class="gear">
<a href="{{ item.url }}" title="{{ item.title }}">{{ item.title }}</a>
</li>
{% endfor %}
</ul>
