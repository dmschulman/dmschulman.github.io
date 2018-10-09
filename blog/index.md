---
layout: apollo
title: "Blog"
description: "'blog' /bläɡ/ noun, a regularly updated website or web page, typically one run by an individual or small group, that is written in an informal or conversational style."
---

<ul class="posts">
  {% for post in site.posts %}
    <li>
	<h2><a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></h2>
	<span class="date">{{ post.date | date: "%B %d, %Y" }}</span>
    </li>
    <p class="excerpt">{{ post.excerpt | strip_html | truncatewords:75 }}
      {% if post.excerpt != post.content %}
        <a class="readmore" href="{{ site.baseurl }}{{ post.url }}" title="Read more">Read more</a>
      {% endif %}
    </p>
  {% endfor %}
</ul>
