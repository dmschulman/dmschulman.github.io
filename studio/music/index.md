---
layout: apollo
title: "Music"
description: ""
---

This page is a repository for many of the musical projects I've embarked on under various names since I began twiddling around with Ableton Live in 2008. Much of my musical output in the early days came from exploriations with a variety of synthesizers, eurorack modules, digital audio softwares, and from studying different production techniques (and much of it still does!). Most of this content lived on Soundcloud for the longest time, but in the interest of divesting myself from profit-driven platforms that have taken a turn for the worst, I'm offering it all up here, for free, under a [Creative Commons BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/) license.

If you'd like to support my music, or just hear my more cohesive musical endeavors, please visit my [Bandcamp](https://khybersound.bandcamp.com/). I also occasionally upload a DJ set to [Mixcloud](https://www.mixcloud.com/khybersound/), though I'm beginning to livestream more and more of my sets to [Twitch](https://www.twitch.tv/khybersound).

{% assign music = site.music | group_by: 'category' | sort: 'name' | reverse %}
{% for category in music %}
<h2>{{ category.name }}</h2>
<ul class="posts">
{% for item in category.items | sort: 'date' %}
<li class="music">
    <img src="{{ item.image }}" alt="{{ item.title }}" />
    <span class="name">{{ item.title }}</span>
    <audio controls src="{{ item.audio }}"> Your browser does not support the <code>audio</code> element.</audio>
    <div class="track-info">
        <span class="notes">{{ item.description }}</span>
        {% if item.tags.size > 0 %}
            <span class="tags">{{ item.tags | sort | join: ", " }}</span>
        {% endif %}
        <span class="date">{{ item.date | date: '%m/%d/%Y' }}</span>
    </div>
</li>
{% endfor %}
</ul>
{% endfor %}
