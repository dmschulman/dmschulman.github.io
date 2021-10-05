---
layout: work
title: "USciences Bicentennial"
description: "Being the first college of pharmacy in the nation, University of the Sciences (established in 1821) has a lot to be proud of in its 200 years of educating leaders in science and healthcare. To celebrate this milestone, a series of events, lectures, fundraising campaigns, class reunions, and other festivities were planned for the 2020-2021 academic year. To help promote and communicate the Bicentennial and build excitement around the event it was determined a microsite would need to be built within our existing CMS allowing the university to promote the event and its storied past to the public."
image: "https://dmschulman.com/about/work/usciences-bicentennial.jpg"
link: https://www.usciences.edu/200
date: 2020-12-15
category: "University of the Sciences" 
tags: 
  - OUCampus
  - XSL
  - HTML
  - CSS
  - XML
  - JS
---

## Challenges

The story of University of the Sciences is a complex one with multiple facets to present, highly dependent on images and visual materials pulled from the university archives. Presenting this material within our normal site templates was not an option, but creating a separate web presence was beyond the scope and timeline of what we needed to accomplish. A unique solution had to be designed and coded within our existing content management system, and one that would work well and load quickly for our majority mobile audience. After content was finalized it was decided that building a microsite would be the only way to achieve the inspirational tone and forward-thinking design the project required.

It was necessary that the design of the microsite incorporate some flexibility as the campaign would evolve throughout the 2021 and 2022 academic years and new content would need to be included, no matter the format. The microsite would additionally need to deliver an image-heavy presentation though be nimble enough to load quickly on a mobile phone. A balance between immersive visual design and clever coding would need to be established in order to deliver on spec and within the confines of our CMS. Finally, the essence of the microsite would need to visually communicate, not only the university's past, but its growth, development, and exciting future ahead.

## Solutions

We went through many iterations of the two most prominent pages on the microsite: the main landing page and the historic timeline. We eventually landed on concepts that allow for easy reflowing of new distinct content (using horizontal container and repeatable regions that could be easily customized) and the inclusion of just enough visual flare that it would support the tone without overwhelming visitors or the web browser.

Though we intended to make the microsite as slim as possible, it was necessary to implement a few Javascript libraries that could render the dynamic presentations the initial design called for. Special care was taken to layer these functions within the preexisting framework of the website (which includes its own unique JS). Examples of this can be found in the Alumni Profiles section of the landing page, utilizing the Flexslider library, as well as the Then & Now section, where jQuery TwentyTwenty was used to present the old vs new image overlay, which was then wrapped inside a Flexslider region.

Graphic assets, such as banners and background images, were saved down separately for desktop and mobile presentations, helping us save valuable bandwidth without compromising on image quality. Techniques such as lazy loading were also utilized to provide the best user experience, natively, across platforms, and without the use of additional Javascript. Where we could, we took advantage of SVG icons and transparent PNG files to give the illusion of a contiguous image or asset (but saving on file size and bandwidth on the backend).

These savings were especially important for the timeline presentation, a chronological list of important events and moments during the university's 200 year history, each illustrated with a set of images and a marker to delineate when it occurred. An XSL transformation was utilized to capture the information for each item and render it into a designed component on the timeline. This allowed for easy data entry and management for the content itself while foolproofing the way the element would appear within the context of the greater timeline's design.

The timeline serves as both a snapshot of the university's past as well as UScience's maturation into a university and the bright future that lies ahead for the institution. The introductory banner graphic helps present the "spark" that ignited the presence of the university (a theme throughout our Bicentennial campaign marketing) and a background gradient is used to convey the passage of time: the original Philadelphia College of Pharmacy, represented by their blue varsity color, transitioning over the centuries to become the maroon-hued University of the Sciences we know today.

<ul class="pictures">
  <li>
    <a href="https://dmschulman.com/about/work/usciences-bicentennial-profiles.jpg" title="Alumni profiles widget" target="_blank">
      <img src="https://dmschulman.com/about/work/usciences-bicentennial-profiles.jpg" alt="Alumni profiles widget from the USciences Bicentennial website">
    </a>
  </li>
  <li>
    <a href="https://dmschulman.com/about/work/usciences-bicentennial-timeline-1.jpg" title="Bicentennial Timeline beginning" target="_blank">
      <img src="https://dmschulman.com/about/work/usciences-bicentennial-timeline-1.jpg" alt="The introduction to the USciences Bicentennial Timeline which beings in the year 1821">
    </a>
  </li>
  <li>
    <a href="https://dmschulman.com/about/work/usciences-bicentennial-reunion.jpg" title="Alumni Reunion banner" target="_blank">
      <img src="https://dmschulman.com/about/work/usciences-bicentennial-reunion.jpg" alt="A banner promoting USciences Alumni Reunion weekend and activities">
    </a>
  </li>
  <li>
    <a href="https://dmschulman.com/about/work/usciences-bicentennial-timeline-2.jpg" title="Bicentennial Timeline past" target="_blank">
      <img src="https://dmschulman.com/about/work/usciences-bicentennial-timeline-2.jpg" alt="A section of the Bicentennial Timeline describing the creation of the Philadelphia College of Pharmacy in 1822">
    </a>
  </li>
  <li>
    <a href="https://dmschulman.com/about/work/usciences-bicentennial-then-now.jpg" title="Then and Now widget" target="_blank">
      <img src="https://dmschulman.com/about/work/usciences-bicentennial-then-now.jpg" alt="A feature juxtoposing old photos of campus with recent images of the same place">
    </a>
  </li>
  <li>
    <a href="https://dmschulman.com/about/work/usciences-bicentennial-timeline-3.jpg" title="Bicentennial Timeline modern era" target="_blank">
      <img src="https://dmschulman.com/about/work/usciences-bicentennial-timeline-3.jpg" alt="A section of the Bicentennial Timeline describing the McNeil Sciences and Technology Center building, constructed in 2006">
    </a>
  </li>
</ul>
