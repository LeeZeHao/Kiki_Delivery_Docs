---
title: Unit Testing
layout: home
parent: Testing
---
# Unit Testing

Unit testing was done during development in order to verify the functionality of individual pieces of code. It has helped to identify issues easily and maintain bug-free code.  

As of Milestone 3, features successfully completed and tested are as follows:  
  
### Client App (All features work on both Web and Android platforms)
1. Display different layout for Web and Android platforms
2. Register with Firebase Authentication  
3. Login with Firebase Authentication  
4. Send password reset email with Firebase Authentication  
5. Send verification email with Firebase Authentication  
6. Cannot login without email verification  
7. Create and store user data using Firebase Firestore  
8. Retrieve data from Firebase Firestore for Home page  
9. Change username in Firebase Firestore from Profile page   
10. Open URL of Control page (with correct arguments taken from Firebase Firestore)  
##### Bugs found and fixed:
1. After logout, able to go back to home page directly using back button without logging in again - Erase react-navigation navigation history after logout
2. Can set empty username at first time user setup - Put username restrictions in place
3. User can start using drone with zero drone usage time - Put lower limit on remaining drone usage time before allowing opening of drone control page
4. Interface styling for mobile looks stretched on desktop - Implement detection of platforms and switch layouts accordingly
  
### Control page  
1. Joysticks render correctly  
2. User and drone camera view elements render correctly  
3. Can request user mic and camera permissions  
4. Can get WebRTC connection information from Firebase Firestore + log its own  
5. Can establish WebRTC connection to drone  
6. Can send control signal via WebRTC data channel to drone  
7. Can use URL arguments (email + access key) to authenticate user and verify access
8. While open, will continuously update available usage time of user in the UI  
9. While open, will decrease available usage time of user in Firebase Firestore at set intervals   
10. If available usage time is depleted, disconnects user from drone  
##### Bugs found and fixed:
1. User can hear their own audio (audio feedback) - Fixed by muting the local audio stream  
2. Scissor lift controls are reversed - Fixed by reversing them back to normal  
3. User can change email address in URL to login as other people - Fixed by implementing current access key system  
4. User is not disconnected even after available usage time is over - Added check for 0 usage time and auto disconnect   

### Drone side web app  
1. Can use the mic and camera of the drone  
2. Can log WebRTC connection information to Firebase Firestore (for Control page to use)  
3. Can establish WebRTC connection to Control page  
4. Can receive control signals from WebRTC data channel  
5. Can connect to WebSocket established by (local) Python script  
6. Can reliably relay control signals to Python script
##### Bugs found and fixed:
1. Transmission of control signals to Python script unreliable, many missed signals - Decreased individual signal size
2. If user unexpectedly disconnects, will get 'stuck' on last control signal - Implement default control signal which instructs drone to stop  

### Drone side Python script  
1. Can establish WebSocket server for Drone side web app to connect to  
2. Can receive control signals via WebSocket  
3. Can control wheel motors via drivers through GPIO library reliably
4. Can control both camera rotation servos (pitch and yaw) through GPIO library reliably
5. Can control scissor lift motor via drivers through GPIO library reliably  
6. Can use control signals to drive wheel motors (via system in point 3)   
7. Can use control signals to rotate camera in two axis (via system in point 4)  
8. Can use control signals to rotate scissor lift motor both directions (for lift raising and lowering) (via system in point 5)  
##### Bugs found and fixed:
1. Software-based PWM signal provided is unstable, causing camera rotation servo to be jittery even when stopped - Fixed by cutting power to servos when stopped  

### Hardware 
1. Power supply to Raspberry Pi 5 is reliable
2. Wheel motors and drivers work
3. Both camera rotation servos (pitch and yaw) work
4. Scissor lift motor via drivers work
5. Testing battery charge time from empty, averages to 7.6 hours. Approximately matches with advertised charging time of 8 hours.
6. Testing battery life from full under normal usage, averages to 2.4 hours.  
##### Bugs found and fixed:
1. Right side wheel motors not getting power - Fixed by using two motor drivers (one per side), instead of only one  
2. Camera rotation servo is jittery even when stopped - Fixed by cutting power when stopped via software  
3. Scissor lift screw shaft breaks often - Fixed by using stronger design and lubrication  



----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
