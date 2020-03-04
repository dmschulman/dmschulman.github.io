---
layout: apollo
title: "Blog"
description: "'blog' /bläɡ/ noun, a regularly updated website or web page, typically one run by an individual or small group, that is written in an informal or conversational style."
---

<ul class="posts">
  {% for post in site.posts %}
    <li>
	<a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
	<span class="date">{{ post.date | date: "%B %d, %Y" }}</span>
	<p class="excerpt">{{ post.excerpt | strip_html | truncatewords:75 }}</p>
    </li>
  {% endfor %}
</ul>
