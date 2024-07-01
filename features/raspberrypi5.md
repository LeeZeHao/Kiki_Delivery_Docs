---
title: Raspberry Pi 5-based Drone
layout: home
parent: Features
---
# Raspberry Pi 5-based Drone

### Proposed

A Raspberry Pi 5 is used as the controller / microcomputer for the drone. It handles the drone-side WebRTC web app, and handles controlling the drone hardware via a Python script as well.  
  
The drone is planned to be a ground-based drone. By making use of the GPIO (general purpose input/output) pins on the Raspberry Pi, the drone can be expanded upon easily with different hardware to offer different features for various types of customers.  
  

### Current Progress

The hardware of the drone is controlled by a python script, which uses libraries such as GPIOD and Thread.  
  
The Python “GPIOD” library is used to interact with the GPIO pins on the Raspberry Pi, which in turn drive the hardware.  
  
Our prototype test drone is currently a small 4-wheeled drone with motors connected to each wheel. An L298n DC motor driver is used to control the 4 motors. 6 GPIO pins are connected to the motor driver, where the left and right side motor groups are each controlled by 3 pins. Of these 3 pins, 2 pins control the direction of the motors, and 1 pin outputs a pulse width modulation (PWM, used for simulating analog voltage) signal to control the speed of the motor.  
  
The Python “thread” library is used to execute the PWM control signal of the motor driver. such that it will not be interrupted by the main thread. Sleep function imported from the “time” library is used to generate the pulse width.  
  


<p align="center">
<img src="https://github.com/LeeZeHao/Kiki_Delivery_Docs/assets/46279960/37eb21e6-a3af-4b16-9814-b409a7df038b" border="10"/>  
</p>
<p align="center">
The internals of the drone.
</p>


----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
