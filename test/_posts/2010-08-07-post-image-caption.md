---
title: "Post: Image (Caption)"
categories:
  - Post Formats
tags:
  - image
  - Post Formats
---

{% capture fig_img %}
![Foo]({{ https://www.instagram.com/p/B3PaetDhHtX/?utm_source=ig_web_copy_link | relative_url }})
{% endcapture %}

<figure>
  {{ fig_img | markdownify | remove: "<p>" | remove: "</p>" }}
  <figcaption>Red & blue, what a combination of the wonderful nature!A random click from Yahangala mountain.</figcaption>
</figure>