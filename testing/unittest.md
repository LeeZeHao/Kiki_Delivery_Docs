---
title: Unit Testing
layout: home
parent: Testing
---
# Unit Testing

Unit testing was done during development in order to verify the functionality of individual pieces of code. It has helped to identify issues easily and maintain bug-free code.  

As of Milestone 3, features successfully completed and tested are as follows:  
  
##### Client App (All features work on both Web and Android platforms)
1. Register with Firebase Authentication  
2. Login with Firebase Authentication  
3. Send password reset email with Firebase Authentication  
4. Send verification email with Firebase Authentication  
5. Cannot login without email verification  
6. Create and store user data using Firebase Firestore  
7. Retrieve data from Firebase Firestore for Home page  
8. Change username in Firebase Firestore from Profile page   
9. Open URL of Control page (with correct arguments taken from Firebase Firestore)  
  
##### Control page  
1. Joysticks render correctly  
2. User and drone camera view elements render correctly  
3. Can request user mic and camera permissions  
4. Can get WebRTC connection information from Firebase Firestore + log its own  
5. Can establish WebRTC connection to drone  
6. Can send control signal via WebRTC data channel to drone  
7. Can use URL arguments (email + access key) to authenticate user and verify access   
8. While open, will continuously decrease available usage time of user in Firebase Firestore  
9. If available usage time is depleted, disconnects user from drone  

##### Drone side web app  
1. Can use the mic and camera of the drone  
2. Can log WebRTC connection information to Firebase Firestore (for Control page to use)  
3. Can establish WebRTC connection to Control page  
4. Can receive control signals from WebRTC data channel  
5. Can connect to WebSocket established by (local) Python script  
6. Can reliably relay control signals to Python script

##### Drone side Python script  
1. Can establish WebSocket server for Drone side web app to connect to  
2. Can receive control signals via WebSocket  
3. Can control wheel motors via drivers through GPIO library reliably
4. Can control both camera rotation servos through GPIO library reliably
5. Can control scissor lift motor via drivers through GPIO library reliably  
6. Can use control signals to drive wheel motors (via system in point 3)   
7. Can use control signals to rotate camera in two axis (via system in point 4)  
8. Can use control signals to rotate scissor lift motor both directions (for lift raising and lowering) (via system in point 5)  



----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
