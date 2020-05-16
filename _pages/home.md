---
title: "Thinker's Cloud"
layout: splash
permalink: /home/
date: 2020-05-7T11:48:41-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.1"
  overlay_image: "/Thinkers-splash.jpg"
  og_image: "/Thinkers-splash3.jpg"
  actions:
    - label: "Blog"
      url: "/year-archive/"
  caption: "Chandula Nethmal"
excerpt: "**Welcome to the Creative Cloud of Chandula!** *You may find some CooL Tech and Fun stuffs in this Static Website.*"
intro: 
  - excerpt: '**Thinker`s Cloud is basically a Static website created using Jekyll Static site generating tools and hosted with Github. Most of the Contents of the web site are based on a Blog related to Electronics, Internet of Things, Telecommunication, Computer Science and many other cool informative stuffs including awesome photos, drawings and some  quotes may add some colors to your life. Also, you may find some interesting projects related to in Robotics, PCB designing, IoT, Embedded systems and etc..**'

site_map:
  - image_path: /assets/images/sitemap.png
    alt: "placeholder image 2"
    title: "Little Guide to Site-Map"
    excerpt: 'The blog contains mostly tech related articles and you can get access to them in the order of timeline via the **Blog** page. These articles are also categorized under most suitable topics considering the content and you can easily go to a particular category of interest via **Categories** page. There is another advantage in this blog which is the **Tags** feature. You can easily find a similar set of articles categorized using common tags via tags you find in the end of each article. Other than above features, there is a keyword search feature in the header of the site, in order to find an article using whatever the keyword in your mind.

*Finally, have a kind request from you to give us a feedback. Whatever on your mind about articles, please don`t hesitate to hit an emoji and type a comment.* '

feature_row:
  - image_path: "https://source.unsplash.com/800x800/?computer"
    alt: "placeholder image 1"
    title: "Computer Science"
    excerpt: "This blog contains some articles related to **Computer Science** projects."
  - image_path: "https://source.unsplash.com/800x800/?electronic_circuit"
    image_caption: "Chandula Nethmal"
    alt: "placeholder image 2"
    title: "Electronics"
    excerpt: "There are some cool **Elctronic** projects you may interested in."
    url: "/year-archive/"
    btn_label: "Go to the Blog"
    btn_class: "btn--primary"
  - image_path: "https://source.unsplash.com/800x800/?robotics"
    title: "Robotics"
    excerpt: "**Robotics** projects also there at your interest."
feature_row2:
  - image_path: "https://source.unsplash.com/400x400/?entertainment"
    alt: "placeholder image 2"
    title: "Entertainment"
    excerpt: 'Some **Entertainment** items for you to add some  colors to ur life. *Entertainment is about taking people away from the regular order of things when there is some chaos and pain and stress.*'
    url: "/entertainment/"
    btn_label: "Go to Entertainment Items"
    btn_class: "btn--primary"
feature_row3:
  - image_path: "https://source.unsplash.com/400x400/?email"
    alt: "placeholder image 2"
    title: "Contact Us"
    excerpt: 'If you have anything to share with us or need to know something related to the content, do not hesitate to contact us!'
    url: "/about/"
    btn_label: "Contact Details"
    btn_class: "btn--primary"
feature_row4:
  - image_path: /site-image.jpg
    alt: "placeholder image 2"
    title: "About Me"
    excerpt: 'Find out details on what is the **Thinkers Cloud** and some details about the author.'
    url: "/about/"
    btn_label: "About"
    btn_class: "btn--primary"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row id="site_map" type="left" %}

{% include feature_row %}

{% include feature_row id="feature_row2" type="left" %}

{% include feature_row id="feature_row3" type="right" %}

{% include feature_row id="feature_row4" type="center" %}
