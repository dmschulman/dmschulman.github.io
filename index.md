---
layout: apollo
title: "David M. Schulman - a wonderful website"
description: "The sometimes blog containing words, works, and wonders by David M. Schulman. Come for the web development, stay for the DIY electronics and synthesizers."
---

Welcome to my homepage, things are a little drafty here at the moment. At least you'll be able to watch this site come together in some sort of pseudo real-time fashion. My website is a good place to read up and find out about various topics, pictures, code, maybe some other things who knows?

## Recent posts

<ul class="posts">
{% for post in site.posts limit:1 %}
  <li>
    <span class="date">{{ post.date | date: "%B %d, %Y" }}</span>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
    <p class="excerpt">{{ post.excerpt | strip_html | truncatewords:75 }}</p>
  </li>
{% endfor %}
</ul>
