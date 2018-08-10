---
layout: apollo
title: Studio
description: "Find out more about how I produce techno and electronic music, view my synthesizer and eurorack modular collections, grab controller templates and patches for your favorite digital instruments."
---

# {{ page.title }}
Welcome my constantly changing, ever evolving bedroom music studio. Here you will find a wealth of resources related to synthesizers, mixers, effects, electronic music production, studio tips, and sage advice from someone who has and continues to find new ways to organize their music making equipment. Alongside information about the gear I currently use, I will be hosting in-depth pages about specific instruments (complete with patches, controller templates, manuals, and other collected bits), as well as other articles and columns related to my production style and my take on building my personal studio.

Oh yeah, and some music too.

## Music Gear
{% assign gear = site.gear | group_by: 'category' | sort: 'name' %}
{% for category in gear %}
  <h3>{{ category.name }}</h3>
  {% for item in category.items %}
    <ul class="posts">
      <li><a href="{{ item.url }}" title="{{ item.title }}">{{ item.title }}</a></li>
    </ul>
   {% endfor %}
{% endfor %}

## Production Posts
{% for post in site.posts | sort: 'date' %}
{% if post.tags contains 'music production' %}
  <ul class="posts">
    <li><a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></li>
  </ul>
{% endif %}
{% endfor %}
