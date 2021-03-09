---
layout: apollo
title: "Portfolio"
description: ""
---

{% assign work = site.work %}
<ul class="posts">
{% for item in site.work %}
<li class="row">
  <a href="{{ item.url }}" title="{{ item.title }}">
    <figure>
      <img src="{{ item.thumbnail }}" alt="{{ item.title }}" />
      <figcaption>{{ item.title }}</figcaption>
    </figure>
  </a>
  <div class="post-meta">
    {% if item.tags.size > 0 %}
      <span class="tags">
        <i aria-hidden class="fas fa-tags" title="Tags"></i> {{ item.tags | sort | join: ", " }}
      </span>
    {% endif %}
    {% if item.category.size > 0 %}
      <span class="category">{{ item.category }}</span>
    {% endif %}
  </div>
  <p>{{ item.description }}</p>
</li>
{% endfor %}
</ul>
