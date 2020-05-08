---
title: "Some Random Quotes"
permalink: /quotes/
header:
  og_image: /assets/images/unsplash-image-2.jpg
excerpt: "This is Chandula Nethmal's Official web site."
layouts_gallery:
  - url: /assets/images/mm-layout-splash.png
    image_path: /assets/images/mm-layout-splash.png
    alt: "splash layout example"
  - url: /assets/images/mm-layout-single-meta.png
    image_path: /assets/images/mm-layout-single-meta.png
    alt: "single layout with comments and related posts"
  - url: /assets/images/mm-layout-archive.png
    image_path: /assets/images/mm-layout-archive.png
    alt: "archive layout example"
last_modified_at: 2020-05-08T14:07:54-04:00
toc: true
---


{% capture fig_img %}
![Foo]({{ '/assets/images/quotes/1.jpg' | relative_url }})
{% endcapture %}

<figure>
  {{ fig_img | markdownify | remove: "<p>" | remove: "</p>" }}
  <figcaption>____.</figcaption>
</figure>

{% capture fig_img %}
![Foo]({{ '/assets/images/quotes/2.jpeg' | relative_url }})
{% endcapture %}

<figure>
  {{ fig_img | markdownify | remove: "<p>" | remove: "</p>" }}
  <figcaption>______.</figcaption>
</figure>



---




