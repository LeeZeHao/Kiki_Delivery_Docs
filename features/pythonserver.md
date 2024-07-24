---
title: Python Server
layout: home
parent: Features
---
# Python Server

A Raspberry Pi 5 is used as the controller / microcomputer for the drone. A python script on the Raspberry Pi 5 can be used to control the drone’s hardware via GPIO.  
  
However, the script handling the WebRTC connection (and receiving data from the user control interface) is written in JavaScript and run as a web app. Therefore, we use a Python server to transmit the control data from the JavaScript program to Python. A detailed explanation is as follows: \
  
On the Python control script of the Raspberry Pi, a “pySocket” class opens a Python server at port 8000 and listens for a connection.  The drone WebRTC Js-based web app will send a handshake request, and the Python server will handle the handshake. Once the connection is established between webpage and the Python server, data will be sent to Python via websocket.  
    
Within the Python script, data is interpreted and handled over another class “droneControl”, which is responsible for handling the drone hardware, including locomotion and other actuators.  
  
Currently, unsuccessfully sent data will result in a “payload length mismatch error”. To handle this, a string “0” will be sent to the web app as a request to resend the previous data (which is cached in a Socket class written in JavaScript).   


----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
