---
title: Tech Stack
layout: home
nav_order: 2
---

# Scope
Kiki’s Delivery is a publicly available (ground-based) drone rental service, which allows users to pay money in order to rent drones for a certain amount of time.  The client side app supports both Web and Android.  
  
Users can sign up for the service using their email address. The login system supports email verification processes and password resets.  
  
After logging in, users will reach the home page. Users can see their profile information, and the amount of drone usage time they have left.  
  
Drone usage time is the amount of time a user may rent a drone. It continually decreases while a user is renting a drone. Users may purchase more drone usage time from the home page.  
  
After that, users may request to rent a drone. The user can then proceed to the controller app (on Web this is opened in a separate browser page, on Android it is embedded within the app) and enter the code.  The user may now access the drone.  
  
During this access, the user will be able to control the robot, and have two-way visual and audio communication via the robot (similar to a video call). Drone usage time is decreased during this period. If the user’s drone usage time runs out, they will first receive a warning, then their access will be cut off. The user may also stop their access before then.  


<p align="center">
<img src="https://github.com/LeeZeHao/Kiki_Delivery_Docs/assets/46279960/8095dcb4-dc11-45aa-81d6-e06b1176d6fc" border="10"/>  
Basic system overview
</p>



----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
