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

{% for bookmark in site.data.bookmarks.bookmarks | group_by: 'cat1' | sort: 'name' %}
<h2>{{ bookmark.cat1 }}</h2>
		<ul class="bookmarks">
				<li>
					{% if bookmark.icon == '' %}
						<i aria-hidden class="fas fa-globe" title="{{ bookmark.name }}"></i>
					{% else  %}
						<img class="favicon" src="{{ bookmark.icon }}" alt="{{ bookmark.name }}" /> 
					{% endif %}
					<a href="{{ bookmark.src }}" title="{{ bookmark.name }}" target="_blank">{{ bookmark.name }}</a>
				</li>
		</ul>
{% endfor %}
</div>
</div>
