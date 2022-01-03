---
layout: single
title:  "Mapping a drone's location in 3D space using OpenCV"
date:   2021-05-19 12:14:04 -0400
categories: projects
author_profile: true
share: false
tags: example
toc: true
---

## Summary
Designed for my computer science class, I created a self-contained system powered by Raspberry Pi that can map the position of a drone in 3D space with higher precision than GPS, increasing reliability and accuracy when taking off and landing.

![landing pad](/assets/images/landing-pad.jpg) 

Video presentation outlining the entire project:
<iframe width="560" height="315" src="https://www.youtube.com/embed/uL7iPueBP54" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Background
For my grade 12 computer science class, I was to design a product with real-world usage. I wanted to explore OpenCV, and I had prior experience with drones. I decided to combine the two.
The idea is that for a drone to be fully autonomous, it must be able to take off and land with more precision than can be offered by GPS. This is fine when flying, but if a drone needs to land into a mount or dock to recharge, my project would come into use.

## The Design
Retro-reflective tape is mounted to the bottom of the drone in a specific pattern allowing it to be reconized by the landing pad's camera.
This design allows (almost) all of the hardware to be mounted in the ground station, reducing additional weight of the drone. 
The Raspberry Pi would pick up on the specific pattern, and then use trigonometry to determin the altitude as well as the x and y axis offsets of the drone from the center of the landing pad.
This would be accurate to centimeters or milimeters, rather than the meters that is (civilian) GPS precision.
Lastly, it would display all this data into augmented reality goggles in an overlay, allowing a pilot to control the drone.

Here is a rough wiring outline of the entire project:
![wiring](/assets/images/drone-mapper-wiring.png)

## Next Steps
The original design allowed for PID loop-based feedback of the drone based on the position calculated by the landing pad. This would autonomously land the drone itself.
However, the control system that forward the signal and mixed it into manual pilot input introduced too much latency, and it was unsafe to continue with the current setup.
It was possible to reduce latency by eliminating the pilot input altogether, but this would be too unsafe to test.
As I only had a few weeks to make this for my class, I ran out of time to continue with alternate methods, but I would like to revisit this in the future, possibly eventually flying a drone fully autonomously from take-off to landing.

