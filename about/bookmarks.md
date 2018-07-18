---
layout: apollo
title: "Bookmarks"
description: "A list of bookmarks"
permalink: /about/bookmarks.html
---

<h1>{{ page.title }}</h1>
<div class="content">
	<p>This page contains a lengthy list of web bookmarks I’ve collected over the years. These links have been painstakingly catalogued here for posterity’s sake, I will do my best to maintain these lists but I make no guarantees that any of the items here are immune from <a href="https://en.wikipedia.org/wiki/Link_rot" title="link rot" target="_blank">link rot</a>. Some of these sites you will know, but many, I anticipate, you will not. I hope you’ll have as much fun and enjoyment exploring these sites as I did when I first stumbled on them.</p>

<div class="post">

{{ site.data.bookmarks.bookmarks | group_by: 'cat1' }}

{% assign items_grouped = site.data.bookmarks.items | group_by: 'cat1' | sort: 'name' %}
{% for group in items_grouped %}
  {% assign items = item.items | sort: 'cat1' %}
  {% for item in items  %}
    {{ item.name }}
  {% endfor %}
{% endfor %}


{% for category in site.data.bookmarks | group_by: 'cat1' %}
{% assign category = name %}
{{ category }}
{% endfor %}

{% for category in site.data.bookmarks | group_by: 'cat1' %}
  category: <h2>{{ category.name }}</h2>
  {% for bookmark in category %}
    bookmark: <p>{{ bookmark.name }}</p>
  {% endfor %}
{% endfor %}

</div>
