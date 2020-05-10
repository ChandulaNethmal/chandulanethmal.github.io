---
title: "Thinker's Cloud"
layout: splash
permalink: /home/
date: 2020-05-7T11:48:41-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.2"
  overlay_image: "/Thinkers-splash.jpg"
  og_image: /ThinkersLogoTrans.png
  actions:
    - label: "Blog"
      url: "/year-archive/"
  caption: "Chandula Nethmal"
excerpt: "Welcome to the creative cloud of Chandula. You may find some cool tech and fun stuffs in this Static website."
intro: 
  - excerpt: 'Thinkers Cloud is basically a Static website created using Jekyll Static site generating tools and hosted with Github. Most of the Contents of the web site is based on a Blog related to Electronics, Internet of Things, Telecommunication, computer science and many other cool stuffs including awesome photos, drawings and some interesting quotes may give soemthing to your life. You may find some interesting projects related to in Robotics, PCB designing, IoT, Embedded systems and etc..'
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
    excerpt: 'Some **Entertainment** items for you to add some  colors to ur life'
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

{% include feature_row %}

{% include feature_row id="feature_row2" type="left" %}

{% include feature_row id="feature_row3" type="right" %}

{% include feature_row id="feature_row4" type="center" %}
