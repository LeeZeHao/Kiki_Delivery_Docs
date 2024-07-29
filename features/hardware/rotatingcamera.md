---
title: Rotating Camera Mount
layout: home
parent: Hardware
grand_parent: Features
---
# Rotating Camera Mount

The rotating camera mount allows the user to rotate the camera across an arc. This allows the user to rotate the camera view, allowing for better situational awareness and visual capabilities than a fixed camera.  

This is achieved via two servo motors, which rotate different parts of the camera housing.  
  
<p align="center">
<img src="https://github.com/user-attachments/assets/c36c8585-dcb1-4d7e-b622-c5144273ea22" border="10"/>  
</p>
<p align="center">
3D model of the camera mount in Fusion 360.  
</p>
  
The Yaw Motor rotates the top part of the mount (along with the Pitch motor) side-to-side, providing yaw rotation for the camera view.   
The Pitch motor rotates the camera up and down, providing pitch rotation for the camera view.   
In total, this provides two degrees of freedom for the camera rotation system.   
  
Both servo motors are connected to the GPIO pins on the Raspberry Pi 5. The Python script is able to control the motors by sending signals through this connection. The servos are controlled using AngularServo class from gpiozero, via a software generated PWM (Pulse Width Modulation) signal. As this method of PWM is slightly unstable and causes some jittering, a system is implemented to cut power to the servo each time after updating the servo to the correct position.

The user can control the camera via the right joystick (lower right corner of screen) in the client side control interface.  

<p align="center">
<img src="https://github.com/user-attachments/assets/2573fc3f-3f18-43fe-aa63-a6b1a400a892" border="10"/>  
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/24aa5293-2328-4e97-b0d2-59e99e271049" border="10"/>  
</p>
<p align="center">
Current build of the camera mount.    
</p>


----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
