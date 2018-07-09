---
layout: apollo
title: Projects
description: ""
---

<h1>{{ page.title }}</h1>

<div class="post">
  <ul>
  {% for projects in site.projects %}
    <li>
      <a href="{{ projects.permalink }}" title="{{ projects.title }}">
        {{ projects.title }}
      </a>
      <span>{{ projects.category }}</span>
    </li>
  {% endfor %}
  </ul>
</div>
