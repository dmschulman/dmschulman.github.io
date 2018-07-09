---
layout: apollo
title: Projects
description: ""
---

<h1>{{ page.title }}</h1>

<div class="post">
  <ul>
    {% for projects in site.categories %}
    {% if projects.url %}
        <li><a href="{{ projects.url }}">{{ projects.title }}</a></li>
    {% endif %}
  {% endfor %}
  </ul>
  
  <!-- <ul>
{% for projects in site.projects %}
    <li>
      <a href="{{ projects.permalink }}" title="{{ projects.title }}">
        {{ projects.title }}
      </a>
    </li>
{% endfor %}
  </ul> -->
</div>
