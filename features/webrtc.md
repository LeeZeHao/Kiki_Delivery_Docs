---
title: WebRTC System
layout: home
parent: Features
---
# WebRTC System

### Proposed

WebRTC is a free and open-source project which provides a simpler way to implement real-time peer-to-peer communication (video, audio and data).  

A simple explanation of how a typical WebRTC connection works is as follows:  
  
Both peers (in our case, the drone and the user control interface) create RTCPeerConnection objects, which are used to manage the connection and media exchange.  
  
Signaling mechanisms (servers or any data transfer method, in our case Firebase Firestore) help these peers exchange session control messages, such as offer and answer SDPs (Session Description Protocols), to establish the connection parameters.  
  
<p align="center">
<img src="https://github.com/LeeZeHao/Kiki_Delivery_Docs/assets/46279960/be6b9328-0349-4ef7-8f60-3ae2291d4295" border="10"/>  
</p>
<p align="center">
Basic Diagram of how WebRTC works  
(Source: https://www.linkedin.com/pulse/everything-you-need-know-webrtc-amriten-chatterjee/)  
</p>

The two peers use STUN (Session Traversal Utilities for NAT) or TURN (Traversal Using Relays around NAT) servers to handle network traversal issues, enabling a direct connection even if the users are behind NATs or firewalls.   
  
Finally, media streams and data channels can be created and transmitted directly between the peers.  


In this project, the real-time video and audio communication aspects of WebRTC are used to implement a two-way video chat between the client (user) interface and the drone, while the data transfer aspect is used to send control signals from the user to the drone.  
  
In this way, a drone system that can be remotely controlled over the Internet is set up.  

### Current Progress

The WebRTC connection is currently handled by two web apps (one as the user’s control interface, one on the robot’s end). For compatibility reasons, the web apps are coded using Javascript without any specific framework.  
  
During our work, we have realized that a connection can be established using STUN server only if both devices’ firewalls are turned off (for instance, when both devices are on the same LAN). TURN server must be used if firewall is enabled (for instance, over the internet).  
  
The currently implemented features using WebRTC are detailed under the “Client Control Interface” section.


----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
