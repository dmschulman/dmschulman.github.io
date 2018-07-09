---
layout: apollo
title: Projects
description: ""
---

<h1>{{ page.title }}</h1>

<div class="post">
  
{% assign groups = site.projects | group_by: "category" | sort: "name" %}
  {% for group in groups %}
    <h2>{{ group.name }}</h2>
    {% for item in group.items %}
      <ul>
        <li>
          <a href="{{ item.permalink }}" title="{{ item.title }}">
            {{ item.title }}
          </a>
        </li>
      </ul>
    {% endfor %}
  {% endfor %}
{% endfor %}
  
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
