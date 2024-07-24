---
title: Drone Usage Timer System
layout: home
parent: Features
---
# Drone Usage Timer System

Each user has a certain amount of drone usage time. Users may purchase more via the web app or mobile app. Once the user opens the drone control interface, the drone usage time of the user will start to decrease. Once the drone usage time reaches zero, the user’s access to the drone is cut off and they cannot rent a drone again until they purchase more.

Drone usage time is stored in the user profile within the Firebase Firestore database service. The user may check it via the app home page. A mock version of the purchase system (without payment), which can increase drone usage time, is included within the app prototype.  
  
Currently, the drone usage time will be decreased by the drone control interface as long as the user has it open. It will continually decrease and display the amount of drone usage time remaining for the user. The control interface also updates the data stored in Firestore.  


----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
