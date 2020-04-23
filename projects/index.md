---
layout: apollo
title: Projects
description: ""
---

A repository for all of my various projects. Most of the items here will be related to DIY electronics, guitar pedals, and synthesizer projects but who knows, maybe some other interesting content will show up here?

<!-- <div class="post">
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
</div> -->

{% assign project = site.project | group_by: 'category' | sort: 'name' | reverse %}
{% for category in project %}
<h3>{{ category.name }}</h3>
<ul class="posts">
{% for item in category.items | sort: 'name' %}
<li class="gear">
<a href="{{ item.url }}" title="{{ item.title }}">{{ item.title }}</a>
</li>
{% endfor %}
</ul>
{% endfor %}
