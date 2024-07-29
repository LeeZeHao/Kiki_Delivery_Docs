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

Some examples of component classes are provided below:  

##### Locomotion / Movement Control
Each update, checks state of control signal. Updates the GPIO pins' value to control the motors direction. Generates PWM signal for speed control.  

##### Scissor lift
Each update, checks state of control signal. Output corresponding pin values to lift, lower or not move the lift.  

##### Camera Rotation
Each update, checks state of control signal. Output corresponding pin values and PWM signal to rotate the two servos to the correct position.  
As the software PWM signal is unstable and causes some jitter, this contains a timed function that detects amount of time since last input, and cuts power to motors when no movement is needed.

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
