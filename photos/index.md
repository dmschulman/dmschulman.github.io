---
layout: apollo
title: Photos
description: "Whether traveling abroad to far away places or simply getting lost in my own backyard, I've always managed to keep a camera at my side. View my collections of photographs here."
---

<h1>{{ page.title }}</h1>
<p>The art of photography has always fascinated, the ability to capture light is akin to freezing time iself. I received my first digital camera at the age of 16, a <a href="https://www.imaging-resource.com/PRODS/A40/A40A.HTM" title="Canon Powershot A40" target="_blank">Canon Powershot A40</a> packed to the gills with 2 megapixels. Digital photography has come a long way since then, even the camera on my mobile phone has 10x the power of that old point-and-shoot, but the thrill of capturing a perfectly composed image never leaves, no matter how fantastic or dated your technology is. The galleries below comprise much of my personal photography work, please enjoy.</p>

<div class="post">
  <ul>
{% for photos in site.photos %}
    <li>
      <img src="{{ photos.thumbnail }}" alt="{{ photos.title }}">
        {{ photos.title }}
    </li>
{% endfor %}
  </ul>
</div>
