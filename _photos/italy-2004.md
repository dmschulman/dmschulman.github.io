---
layout: photo-gallery
title: "Rome, Vatican City, Florence, and Cinque Terre"
name: "Italy 2004"
permalink: /photos/italy-2004.html
thumbnail: thumbnails/italy-trip-thumb.jpg
date: 2004-07-20
endDate: 2004-07-26
description: "In the summer of 2004, after graduating high school, I took my first trip abroad to visit the sites and sounds in and around Italy. Our adventure began on the streets of Rome, touring the Colosseum and other ancient Roman antiquities before heading to Vatican City to check out the Sistine Chapel and give the Pope John Paul II a high-five. We then rented a car (the rental agency was out of Lamborghinis unfortunately) and drove north towards Florence, then across a winding single-lane road through the mountains to get to the coastal town of Manarola in the Cinque Terre region. Finally we made a brief pit stop in a little place called Pisa before heading back towards the airport near Rome."
tags: [Italy, Rome, The Vatican, Vatican City, Florence, Cinque Terre, Manarola, Pisa, Travel, Photos]
geo: "Italy"
camera: "Canon PowerShot A40"
reel: 105
---

<ul>
     <li>{{ site.data.google-photos.feed.entry[1].id.link.href }}</li>   
</ul>

{% assign gallery = site.data.google-photos.feed.entry[n].link[2].href %}
<ul>
     <li>{{ gallery }}</li>
</ul>

<ul>
{% for gallery in site.data.google-photos.feed.entry[n].link[2].href %}
   <li>{{ gallery }}</li>
{% endfor %}    
</ul>

<ul>
     <li>{{ site.data.google-photos.feed.entry[n].id.link[2] }}</li> 
</ul>

<ul>
     <li>{{ site.data.google-photos.feed.entry[0].link[2].href }}</li>  
</ul>
