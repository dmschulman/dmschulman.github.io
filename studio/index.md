---
layout: apollo
title: "Studio"
description: "Find out more about how I produce techno and electronic music, view my synthesizer and eurorack modular collections, grab controller templates and patches for your favorite digital instruments."
---

Welcome my constantly changing, ever evolving bedroom music studio. Here you will find a wealth of resources related to synthesizers, mixers, effects, electronic music production, studio tips, and sage advice from someone who has and continues to find new ways to organize their music making equipment. Alongside information about the gear I currently use, I will be hosting in-depth pages about specific instruments (complete with patches, controller templates, manuals, and other collected bits), as well as articles and other explainers related to my production style and my take on building a home music studio.

Oh yeah, and some [music](/studio/music/index.html) too.

## Music Gear
Below are some of the synthesizers, drum machines, instruments, devices, boxes, hardware, effects, tools, technology, and other doohickies I use (or have previously used) in my studio. This collection represents my favorite music making machines, the hardware which I've found to be the most versatile, best sounding, and easiest to get along with when recording.

Rather than simply compiling a big list here, my intent is to share all of the valuable information and insights I've gathered while working with these devices. Inside each listing you'll find my personal commentary as well as a variety of archived materials such as manuals, patches, modification guides, software, pictures, videos, and much more.
{% assign gear = site.gear | group_by: 'category' | sort: 'name' | reverse %}
{% for category in gear %}
<h3>{{ category.name }}</h3>
<ul class="posts">
{% for item in category.items | sort: 'name' %}
<li class="gear">
<a href="{{ item.url }}" title="{{ item.title }}">{{ item.title }}</a>
</li>
{% endfor %}
</ul>
{% endfor %}

<p class="footnote">I find it necessary to present this archive as these materials have become harder and harder to track down online (especially for older instruments), and as time goes on, more and more of these files will likely become unavailable. I claim no ownership over the files themselves, I am merely mirroring the material for the greater good. If I'm hosting something you created and you want me to remove it, please <a href="mailto:%64%61vi%64@d%6d&#115;c%68%75%6cm&#97;n.%63%6f&#109;?subject=Studio%20page%20content%20notice">contact me</a>.</p>

## Production Posts
<ul class="posts">
{% for post in site.posts | sort: 'date' %}
{% if post.tags contains 'music production' %}
<li>
<a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
<span class="date">{{ post.date | date: "%B %d, %Y" }}</span>
<p class="excerpt">{{ post.excerpt | strip_html | truncatewords:55 }}</p>
</li>
{% endif %}
{% endfor %}
</ul>
