---
title: Python Control Script
layout: home
parent: Features
---
# Python Control Script

The Python control script is run locally on the Raspberry Pi 5. It mainly serves to retrieve control signals from the drone side WebRTC web app, and translate them into GPIO pin outputs for the drone hardware.  

It uses libraries such as GPIOD and Thread. It uses these libraries to direct signals sent from GPIO pins on the Raspberry Pi, which in turn control the electronic hardware.  

The Python “Thread” library is used to execute the PWM control signal of the motor driver (software PWM), such that it will not be interrupted by the main thread. Sleep function imported from the “time” library is used to generate the pulse width.   


### WebSocket Server

The Python script starts and maintains a WebSocket server to be used locally. This is used by the drone side web app. After receiving control signals via WebRTC, it passes on the signals to the Python control script via this server.

### Hardware

Each component of the drone (Locomotion motors, scissor lift, camera rotation servos, etc) is seperated into its own class.  

----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
