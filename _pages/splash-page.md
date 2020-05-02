---
title: "Thinker's Cloud"
layout: splash
permalink: /splash-page/
date: 2016-03-23T11:48:41-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: "https://source.unsplash.com/1600x400/?tech"
  actions:
    - label: "Blog"
      url: "/year-archive/"
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
excerpt: "Welcome to the creative cloud of Chandula. you will find so many cool tech stuffs you may interested in. This is a Static web site created using Jekyll Static site generating tools and hosted with Github."
intro: 
  - excerpt: 'Thinkers Cloud is basically a web site based on a Blog related to Electronics, Internet of Things, Telecommunication, new technologies and many other cool stuffs related to science fields. You may find interesting projects which the author has done through his knowledge and experience in Robotics, PCB designing, Internet of Things, Embedded systems. Centered with `type="center"`'
feature_row:
  - image_path: "https://source.unsplash.com/800x800/?computer"
    alt: "placeholder image 1"
    title: "Computer Science"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
  - image_path: "https://source.unsplash.com/800x800/?electronic_circuit"
    image_caption: "Image courtesy of [Unsplash](https://unsplash.com/)"
    alt: "placeholder image 2"
    title: "Electronics"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
    url: "#test-link"
    btn_label: "Go to the Blog"
    btn_class: "btn--primary"
  - image_path: "https://source.unsplash.com/800x800/?robotics"
    title: "Robotics"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
feature_row2:
  - image_path: "https://source.unsplash.com/400x400/?entertainment"
    alt: "placeholder image 2"
    title: "Entertainment"
    excerpt: 'Some **Entertainment** items for you. Left aligned with `type="left"`'
    url: "#test-link"
    btn_label: "Entertainment"
    btn_class: "btn--primary"
feature_row3:
  - image_path: "https://source.unsplash.com/400x400/?contact_details"
    alt: "placeholder image 2"
    title: "Contact Us"
    excerpt: 'This is some sample content that goes here with **Markdown** formatting. Right aligned with `type="right"`'
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row4:
  - image_path: "https://source.unsplash.com/400x400/?about_me"
    alt: "placeholder image 2"
    title: "About Me"
    excerpt: 'Find out details on what is the **Thinkers Cloud** and some details about the author. Centered with `type="center"`'
    url: "#test-link"
    btn_label: "About"
    btn_class: "btn--primary"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}

{% include feature_row id="feature_row2" type="left" %}

{% include feature_row id="feature_row3" type="right" %}

{% include feature_row id="feature_row4" type="center" %}