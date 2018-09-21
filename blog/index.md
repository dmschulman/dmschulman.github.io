---
layout: apollo
title: "Blog"
description: "'blog' /bläɡ/ noun, a regularly updated website or web page, typically one run by an individual or small group, that is written in an informal or conversational style."
---

<h1>{{ page.title }}</h1>
<ul class="posts">
  {% for post in site.posts %}
    <li>
	<span class="date">{{ post.date | date: "%B %d, %Y" }}</span>
	<a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
    </li>
    <p>{{ post.excerpt | strip_html | truncatewords:75 }}
      {% if post.excerpt != post.content %}
        <a class="readmore" href="{{ site.baseurl }}{{ post.url }}" title="Read more">Read more</a>
	    {% endif %}</p>
  {% endfor %}
</ul>
