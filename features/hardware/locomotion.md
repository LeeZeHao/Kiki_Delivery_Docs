---
title: Locomotion
layout: home
parent: Hardware
---
# Locomotion

### Proposed

A set of actuators that facilitate easy implementation of ground-based movement.  
  
We have decided to opt for ground-based movement rather than aerial drones as this would significantly increase risk and project difficulty, and aerial drones cannot operate outside of line-of-sight in Singapore.


### Current Progress

Currently, the drone has a 4-wheeled chassis, where each wheel is powered by a 12V DC motor. The system is controlled by the Raspberry Pi 5 controller via two l298n motor drivers (one per each side).  
  
This system has proven to be easy to implement, and has shown good mobility during testing.   
  
<p align="center">
<img src="https://github.com/LeeZeHao/Kiki_Delivery_Docs/assets/46279960/bf524941-cab8-484b-b8ac-9a7a4ed6ec83" border="10"/>
The chassis of the drone taken apart during development. The 4 DC motors (yellow) and the motor drivers (red) are visible.
</p>


----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
