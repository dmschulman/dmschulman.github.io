---
layout: apollo
title: Projects
---

<h1>{{ page.title }}</h1>

{% for projects in site.projects %}
  <div class="post">
    <ul>
      <li>{{ projects.title }}</li>
    </ul>
  </div>
{% endfor %}
