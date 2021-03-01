---
layout: apollo
title: "Music"
description: ""
---

Here you'll find a repository of some of the musical projects I've embarked on under various names since I began twiddling around with Ableton Live in 2010. Much of my musical output in the early days came from exploriations with various synthesizers, eurorack modules, digital audio softwares, and studying different production techniques (and much of it still does!). Most of this content lived in Soundclound for the longest time, but in the interest of divesting myself from profit-driven platforms that have taken a turn for the worst, I'm instead offering it all up here, for free, under a [Creative Commons BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/) license.

To hear my more cohesive musical endeavors, please visit my [Bandcamp](https://khybersound.bandcamp.com/).

{% assign music = site.music | group_by: 'category' | sort: 'name' | reverse %}
{% for category in music %}
<h2>{{ category.name }}</h2>
<ul class="posts">
{% for item in category.items | sort: 'date' %}
<li class="music">
    <img src="{{ item.image }}" alt="{{ item.title }}" />
    <span class="name">{{ item.title }}</span>
    <audio controls src="{{ item.audio }}"> Your browser does not support the <code>audio</code> element.</audio>
    <span class="notes">{{ item.description }}</span>
    <div class="track-info">
        {% if item.tags.size > 0 %}
            <span class="tags">{{ item.tags | sort | join: ", " }}</span>
        {% endif %}
        <span class="date">{{ item.date | date: '%m/%d/%Y' }}</span>
    </div>
</li>
{% endfor %}
</ul>
{% endfor %}
