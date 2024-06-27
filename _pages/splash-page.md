---
title: "Thinker's Cloud"
layout: splash
permalink: /splash-page/
date: 2016-03-23T11:48:41-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.4"
  overlay_image: "/Thinkers-splash.jpg"
  actions:
    - label: "Blog"
      url: "/year-archive/"
  caption: "Chandula Nethmal"
excerpt: "Welcome to the creative cloud of Chandula . You will find so many cool tech stuffs you may interested in. This is a Static web site created using Jekyll Static site generating tools and hosted with Github."
intro: 
  - excerpt: 'Thinkers Cloud is basically a web site based on a Blog related to Electronics, Internet of Things, Telecommunication, new technologies and many other cool stuffs related to science fields. You may find interesting projects which the author has done through his knowledge and experience in Robotics, PCB designing, Internet of Things, Embedded systems.'
feature_row:
  - image_path: "/assets/images/1_main/computer"
    alt: "placeholder image 1"
    title: "Computer Science"
    excerpt: "This blog contains some articles related to **Computer Science** projects."
  - image_path: "/assets/images/1_main/electronics"
    image_caption: "Chandula Nethmal"
    alt: "placeholder image 2"
    title: "Electronics"
    excerpt: "There are some cool **Elctronic** projects which you may interested in."
    url: "/year-archive/"
    btn_label: "Go to the Blog"
    btn_class: "btn--primary"
  - image_path: "/assets/images/1_main/robotics"
    title: "Robotics"
    excerpt: "**Robotics** projects also there at your interest."
feature_row2:
  - image_path: "/assets/images/1_main/art"
    alt: "placeholder image 2"
    title: "Entertainment"
    excerpt: 'Some **Entertainment** items for you.'
    url: "/year-archive/"
    btn_label: "Entertainment"
    btn_class: "btn--primary"
feature_row3:
  - image_path: "/assets/images/1_main/email"
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