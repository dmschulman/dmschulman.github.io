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
    <figure>
      <img src="{{ item.thumbnail }}" alt="{{ item.title }}" />
      <figcaption>{{ item.title }}</figcaption>
    </figure>
  </a>
  <p>{{ item.description }}</p>
</li>
{% endfor %}
</ul>
