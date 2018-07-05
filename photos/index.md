---
layout: apollo
title: Photos
---

<h1>{{ page.title }}</h1>

{% for photos in site.photos %}
  <div class="post">
    <ul>
      <li>{{ photos.title }}</li>
    </ul>
  </div>
{% endfor %}
