---
title: Unit Testing
layout: home
parent: Testing
---
# Integration Testing
  
As in the system overview, our system consists of multiple programs. Although these programs are running separately, they have interactions that must work consistently for the system to function. Integration testing has therefore been a continual part of our development process.  
  
Interactions / Features tested are as follows:  
1. Client app redirecting user to control interface URL (with correct arguments), opening it in new tab of a browser  
2. WebRTC video and audio stream between control interface and drone can be established  
3. WebRTC data stream from control interface to drone can be established  
4. Control signals can be sent from control interface to drone via WebRTC data channel  
5. Drone side web app can receive control signals from control interface via WebRTC data channel  
6. Drone side web app can send control signals to Drone side Python script via WebSocket (local)  
7. Drone side Python script can receive control signals from Drone side web app via WebSocket


----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
