---
title: Testing
layout: home
nav_order: 5
has_children: true
---

# Testing

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
