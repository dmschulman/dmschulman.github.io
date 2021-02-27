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
{% for item in category.items | sort: 'name' %}
<li class="music">
    <img src="{{ item.image }}" alt="{{ item.title }}" />
    <span class="name">{{ item.title }}</span>
    <audio controls src="{{ item.audio }}"> Your browser does not support the <code>audio</code> element.</audio>
    <div class="track-info">
        <span class="date">{{ item.date | date: '%B %d, %Y' }}</span>
        {% if item.tags.size > 0 %}
            <span class="tags">{{ item.tags | sort | join: ", " }}</span>
        {% endif %}
    </div>
    <span class="notes">{{ item.description }}</span>
</li>
{% endfor %}
</ul>
{% endfor %}

<table class="audio-track">
    <tr>
        <td rowspan="2" class="album-art">
            <img src="http://placehold.it/120x120" alt="" /> 
        </td>
        <td>
          <span>Track Name</span>
        </td>
        <td>
          <span>Artist Name</span>
        </td>
    </tr>
    <tr>
        <td colspan="2" rowspan="1">
          <audio controls src=""> Your browser does not support the <code>audio</code> element.</audio>
        </td>
    </tr>
    <tr> 
        <td>
          <span>Tags/Genre</span>
        </td>
        <td>
          <span>
            Release Date
          </span>
      </td>
      <td>
        <span>
          Something else
        </span>
      </td>
    </tr>
    <tr>
        <td colspan="3">
          <p>Additional Notes</p>
        </td>
    </tr>
</table>
