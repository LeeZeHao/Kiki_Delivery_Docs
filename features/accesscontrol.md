---
title: Access Control System
layout: home
has_children: true
parent: Features
---
# Access Control System

### Proposed

The access control system for the control interface is used to ensure users can only access the drone with proper permissions (by opening the interface through the client app), and to identify the user which is controlling the drone.  
  
The access codes are generated automatically, and stored in the backend database (Firebase Firestore). Each time the user accesses the drone, the access code (along with extra information to identify the user) is passed to the control interface web page. At the same time, the access code is immediately changed at the backend.  
  
This results in a system that is secure, and doesn't require extra user input.  
  
The current implementation and further explanations are detailed below.  

### Current Progress

The current timeline of how the system works is split into 3 parts:  

##### Drone system startup
0. An existing access code is already stored in the Firebase Firestore cloud database.  
1. Drone (Raspberry Pi system) is booted up. Drone side web app is started. It stores WebRTC connection information along with the access code in the same Firestore document. This is done so that the connection information can be searched for using the code later.  
  
##### User connects to drone
2. User clicks the button on the app home page to connect to a drone  
3. App obtains access code from Firestore.  
4. App opens the URL for the client side control interface with arguments containing the user’s email and the access code obtained above.  
5. Client side control interface web app is opened. The access code in the Firestore database is immediately changed to a new one (old code is still stored for checking).  
6. Client side control interface checks the email against Firestore data to make sure the user exists, and checks the provided access code against Firestore (old code) for correctness.  
7. The access code is used to search for the WebRTC connection information. When it is found, a WebRTC connection can be established.  
  
##### User disconnects from drone
8. User closes out from the client control interface. (Any method is fine since the client control interface no longer has to perform any further actions.)  
9. Drone (Raspberry Pi system) is rebooted by staff.  
10. Repeat from step 0.  

In step 4, the email is passed to the client control interface. This is so that it can later track and change the user’s drone usage time left. This will be important for the “Drone usage timer system” feature described below.  
  
In step 5, the access code is immediately changed in the cloud database. This is because the code was passed as an URL argument to the control interface, thus being visible to the user. The code is therefore immediately changed so it cannot be misused. (Or else, the user could use someone else’s email and the same key, then their drone usage would be charged to the other person’s account!)  



----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
