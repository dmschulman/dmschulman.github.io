---
layout: apollo
title: "Portfolio"
description: ""
---

{% assign work = site.work %}
<ul class="posts">
{% for item in site.work %}
<li>
<a href="{{ item.url }}" title="{{ item.title }}">{{ item.title }}</a>
</li>
{% endfor %}
</ul>
