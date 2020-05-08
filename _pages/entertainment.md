---
title: "Entertainment Items"
layout: splash
permalink: /entertainment/
date: 2020-05-07T11:48:41-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.1"
  overlay_image: "https://source.unsplash.com/1000x200/?entertainment"
  actions:
    - label: "Blog"
      url: "/year-archive/"
  caption: "Chandula Nethmal"
excerpt: "Welcome to the creative cloud of Chandula . You will find so many cool tech stuffs you may interested in. This is a Static web site created using Jekyll Static site generating tools and hosted with Github."
intro: 
  - excerpt: 'Thinkers Cloud is basically a web site based on a Blog related to Electronics, Internet of Things, Telecommunication, new technologies and many other cool stuffs related to science fields. You may find interesting projects which the author has done through his knowledge and experience in Robotics, PCB designing, Internet of Things, Embedded systems.'
feature_row:
   - image_path: "https://source.unsplash.com/800x800/?vector_graphics"
    image_caption: "Chandula Nethmal"
    alt: "placeholder image 2"
    title: "Photos"
    excerpt: "There are some cool **Photos** projects taken by me may interested in."
    url: "/graphics/"
    btn_label: "Go to Photos"
    btn_class: "btn--primary"
  feature_row2:
  - image_path: "https://source.unsplash.com/400x400/?drawings"
    alt: "placeholder image 2"
    title: "Go to Drawings & Graphic Designs"
    excerpt: 'Some **Computer Graphic Designs and Pencil Sketches** for you.'
    url: "/drawings/"
    btn_label: "Drawings"
    btn_class: "btn--primary"
feature_row3:
  - image_path: "https://source.unsplash.com/400x400/?quotes"
    alt: "placeholder image 2"
    title: "Go to Quotes"
    excerpt: 'Some interesting Quotes from Movies and other Erudites'
    url: "/quotes/"
    btn_label: "Quotes"
    btn_class: "btn--primary"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}

{% include feature_row id="feature_row2" type="left" %}

{% include feature_row id="feature_row3" type="right" %}


