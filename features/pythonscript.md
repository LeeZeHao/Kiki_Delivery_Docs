---
title: Python Control Script
layout: home
parent: Features
---
# Python Control Script

The Python control script is run locally on the Raspberry Pi 5. It mainly serves to retrieve control signals from the drone side WebRTC web app, and translate them into GPIO pin outputs for the drone hardware.  

It uses libraries such as GPIOD and Thread, to direct signals sent from GPIO pins on the Raspberry Pi, which in turn control the electronic hardware.  

### Main.py

This script contains component classes responsible for various funcitons of the drone. When it is run, every instance of each component class is instantiated, and a while loop is used to update every component continuously.  

### WebSocket Server

The Python script starts and maintains a WebSocket server which is hosted locally (at port 8765). This is used by the drone side web app which receives control signals via WebRTC and passes them on to the Python control script via this server. The Python script listens to that local port to receive the control signals.

Tornado library is used to host this server.

----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
