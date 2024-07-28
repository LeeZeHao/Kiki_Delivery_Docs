---
title: Python Control Script
layout: home
has_children: true
parent: Features
---
# Python Control Script

The Python control script(s) are run locally on the Raspberry Pi 5. It mainly serves to retrieve control signals from the drone side WebRTC web app, and translate them into GPIO pin outputs for the drone hardware.  

### WebSocket Server

The Python script 

### 

Users in the control page can  
- Observe the drone’s camera view in middle of screen  
- Input text to be sent and displayed on the drone  
- Control the movement of drone using a virtual joystick on the bottom left side of the screen  
- Disable their own microphone or camera  
- View drone usage time left  
- Control extra functions such as camera rotation and other actuators using action buttons on the bottom right side of the screen  
- Disconnect the drone (This will also stop the consumption of drone usage time (detailed under “Drone usage timer system” section))
  
Currently, users in the control page can:  
- Establish connection to the drone  
- Observe their own camera view on top right corner  
- Observe the drone’s camera view in middle of screen  
- Input text to be sent and displayed on the drone  
- Control the movement of drone using a virtual joystick on the screen  



<p align="center">
<img src="https://github.com/LeeZeHao/Kiki_Delivery_Docs/assets/46279960/3fbd7993-ba8d-474f-8040-68dbf090e067" border="10"/>  
</p>
<p align="center">
<img src="https://github.com/LeeZeHao/Kiki_Delivery_Docs/assets/46279960/a92f2147-a370-44fb-9a36-0312cb745211" border="10"/>  
</p>
<p align="center">
Planned user control interface
</p>


----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
