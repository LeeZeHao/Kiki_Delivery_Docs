---
title: Drone Usage Timer System
layout: home
parent: Features
---
# Drone Usage Timer System

Each user has a certain amount of drone usage time. Users may purchase more via the web app or mobile app. Once the user opens the drone control interface, the drone usage time of the user will start to decrease. Once the drone usage time reaches zero, the user’s access to the drone is cut off and they cannot rent a drone again until they purchase more.  

##### Purchase Time

Drone usage time is stored in the user profile within the Firebase Firestore database service. The user may check it via the app home page. A mock version of the purchase system, which can increase drone usage time, is included within the app prototype.  

NOTE: As it is not feasible to find and implement a payment service provider for the project at this stage, that specific part is a placeholder. However, all the other logic for purchasing and updating user drone usage time is implemented and working correctly as of Milestone 3.  

##### Tracking of Drone Usage Time  
  
Tracking of drone usage time is done by user the drone control interface.  

The drone control interface can obtain the user using the drone using the access control system (detailed in "Access Control System" feature). It can thus set the drone usage time of the current user specifically.  

The drone usage time will only start to be decreased after the user has successfully connected to a drone. After that, it will continually decrease and display the amount of drone usage time remaining for the user. However, the usage data stored in Firestore is not continually updated, but only at set intervals. This is to prevent an overload on network traffic. During testing, this interval was set to 5 minutes to avoid excess Firebase access usage, but this will be adjusted to a lower value for production.  

<p align="center">
<img src="https://github.com/user-attachments/assets/5c39a477-b422-45d0-b4a8-775073e9bf40" border="10" width="400"/>  
</p>
<p align="center">
Drone usage time is tracked while the drone is connected.
</p>


----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
