---
title: Testing
layout: home
nav_order: 5
---

# Testing

## Unit Testing

Unit testing was done during development in order to verify the functionality of individual pieces of code. It has helped to identify issues easily and maintain bug-free code.  

As of Milestone 2, features successfully completed and tested are as follows:  
  
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
8 .While open, will continuously decrease available usage time of user in Firebase Firestore  

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
4. Can use control signals to drive wheel motors (via system in point 3)  

## Integration Testing
  
As in the system overview, our system consists of multiple programs. Although these programs are running separately, they have interactions that must work consistently for the system to function. Integration testing has therefore been a continual part of our development process.  
  
Interactions / Features tested are as follows:  
1. Client app redirecting user to control interface URL (with correct arguments), opening it in new tab of a browser  
2. WebRTC video and audio stream between control interface and drone can be established  
3. WebRTC data stream from control interface to drone can be established  
4. Control signals can be sent from control interface to drone via WebRTC data channel  
5. Drone side web app can receive control signals from control interface via WebRTC data channel  
6. Drone side web app can send control signals to Drone side Python script via WebSocket (local)  
7. Drone side Python script can receive control signals from Drone side web app via WebSocket
  
## System Testing
  
System testing was done to ensure our system functions correctly as a whole. In particular, we focused on the user flow, making sure that the user doesn’t encounter errors during use of our project.  
  
Interactions / Features tested are as follows:  
1. User can register  
2. User can receive verification email (and must verify email before being allowed to log in)  
3. User can log in and log out  
4. User can reset password  
5. User can view information on the Home screen  
6. User can view information and change username in Profile screen  
7. User can “buy” drone usage time (no payment system implemented yet, but data is saved to cloud properly)  
8. User can use button on Home screen to rent a drone (bring them to the control page)  
9. User can see their own webcam view on control page  
10. User can connect to drone on control page  
11. User can see drone’s webcam view and hear audio from drone on control page  
12. User can use bottom left joystick to control drone  
13. User can control the drone reliably (without significant lag, input delay etc)  









----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
