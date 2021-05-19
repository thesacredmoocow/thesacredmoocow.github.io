---
layout: single
title:  "Reverse Engineering my Laptop's Drivers"
date:   2021-05-18 13:14:04 -0400
categories: projects
author_profile: true
share: true
tags: software c++ python
toc: true
permalink: /laptop-drivers/
---
## Summary
I hated the stock software for my laptop and wanted to improve them. I improved on an open-source app and added 2 major features: controlling the power usage of the dedicated graphics card through scripts,
as well as reverse engineering and mimicking the communications protocol for the LED panel on the back, and then playing snake on it.

![keyboard](/assets/images/keyboard.jpg)

## Backstory
I bought a new laptop for university august of last year, and quickly realized that as good as the hardware was, the software **sucked**.

Fortunately, the community support for this laptop was great, including many open-source third-party tools which I could use to modify it as needed.

One tool in particular stood out to me. It was called G14Control. It was a simple python program which combined various CLI apps into a simple tray app. With a single click of a button, 
I could adjust the maximum power usage of my CPU set the screen's refresh rate lower to save battery. However, I had noticed that this app had not been maintained in months, and took it upon myself to improve on it.


## Result
With the help of various other software developers, I was able to add two major features which I considered essential to the usage of my computer.

First of all, after detecting a change in power source, it could automatically enable or disable the dedicated graphics card, instantly boosting the battery life of my laptop to upwards of 8 hours.

The other major feature was a matrix of LEDs on the back of the lid. Using the stock firmware, it could load low-resolution videos or display things such as notifications or the time. 

After some digging, it turned out that this secondary screen was controlled as a USB device. Reading through packets captured with Wireshark as well as some source code for a linux app, I was able to determine the protocol that the device used.
From there, I created a new driver using the Windows SDK, and loaded it into the device. I mimick'd the packets and I had free reign over the LEDs, and could control them however I wanted!

I designed some raindrop/firework patterns which looked similar to a screensaver, and added it to my continuation of the G14Control app. Most importantly, however, I could now **play snake on my computer's lid**.

<iframe width="560" height="315" src="https://www.youtube.com/embed/bMbww_unV3w" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

[Source Code](https://github.com/thesacredmoocow/g14control-r2)

