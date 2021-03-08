---
layout: apollo
title: "Portfolio"
description: ""
---

{% assign work = site.work %}
<ul class="posts">
{% for item in site.work %}
<li class="content-row">
  <a href="{{ item.url }}" title="{{ item.title }}">
    <img src="{{ item.thumbnail }}" alt="{{ item.title }}" />
  </a>
  <p>
    <a href="{{ item.url }}" title="{{ item.title }}">{{ item.title }}</a>
  </p>
  <p>{{ item.description }}</p>
</li>
{% endfor %}
</ul>
