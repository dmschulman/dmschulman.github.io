---
layout: apollo
title: "dmschulman.com - a wonderful place"
description: "My homepage, yippie!"
---

Welcome to my homepage, things are a little drafty here at the moment. At least you'll be able to watch this site come together in some sort of pseudo real-time fashion. My website is a good place to read up and find out about various topics, pictures, code, maybe some other things who knows?

## Recent posts

<ul class="posts">
{% for post in site.posts limit:1 %}
  <li>
    <span class="date">{{ post.date | date: "%B %d, %Y" }}</span>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
  <p class="excerpt">{{ post.excerpt | strip_html | truncatewords:75 }}
    {% if post.excerpt != post.content %}
      <a class="readmore" href="{{ site.baseurl }}{{ post.url }}" title="Read more">Read more</a>
    {% endif %}
  </p>
{% endfor %}
</ul>
