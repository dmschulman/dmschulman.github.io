---
layout: apollo
title: Projects
description: ""
---

<h1>{{ page.title }}</h1>

<div class="post">
  
    <ul>
{% assign groups = site.projects | group_by: "category" | sort: "name" %}
    <li>
      <a href="{{ projects.permalink }}" title="{{ projects.title }}">
        {{ projects.title }}
      </a>
    </li>
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
