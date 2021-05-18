---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: splash
title: A little bit about me
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/header.JPG
  #actions:
  #  - label: "Download"
  #    url: "https://github.com/mmistakes/minimal-mistakes/"
  caption: "Photo credit: [**sicheng meng**](/assets/images/header.JPG)"
excerpt: "I like STEM, and I love to tinker. Whether its a robot, a particular paper airplane, or some crazy idea I had at 2am, I want to experiment with it. Maybe I'll make something new and innovative, or something do I personally find interesting. At the very least, I'll learn a thing or two in the process. Here are some of those efforts."
intro: 
  - excerpt: '# Featured Projects'
feature_row2:
  - image_path: /assets/images/rubiks-cube-bot.JPG
    alt: "placeholder image 2"
    title: "OpenCV-based Rubik's Cube Solving Robot"
    excerpt: "I am slow at solving Rubiks Cubes and decided to make a robot that does it better using electronics I already had."
    url: "/rubiks-cube/"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row3:
  - image_path: /assets/images/keyboard.JPG
    alt: "placeholder image 3"
    title: "Reverse Engineering My Laptop's Drivers"
    excerpt: "My laptop's factory drivers sucked so I decided to try to improve on them. I wrote some new code using the Windows SDK and C++ that let me play snake on the back of my laptop."
    url: "/laptop-drivers/"
    btn_label: "Read More"
    btn_class: "btn--primary"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row id="feature_row2" type="left" %}

{% include feature_row id="feature_row3" type="left" %}