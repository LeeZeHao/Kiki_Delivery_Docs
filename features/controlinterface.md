---
title: Client Control Interface
layout: home
has_children: true
parent: Features
---
# Client Control Interface

The control page is the user interface for connecting to the robot and controlling it.  

### Automatic Authentication / Access Control
  
When the user is redirected from the client app, it passes the user email and an access key (obtained from Firestore) to the control interface via URL arguments.  

Once it is opened, users will see this screen.

<p align="center">
<img src="https://github.com/user-attachments/assets/c0567c48-b978-433a-891f-3733b2b6869c" border="10"/>  
</p>
<p align="center">
The control interface on startup.
</p>

At this stage, the control interface is not yet connected to the drone. The user cannot control the drone, and the user's drone usage time will not decrease. Users must use the "Connect to Drone" button (green) to start a connection.
  
When the user tries to connect to a drone, authentication of the user is done by using a Firestore query (to the "user_data" collection) to search registered users by the provided email to verify that the user exists + get the user id of the user. The provided access key is also checked against the key in Firestore (under "access_code" collection). The access key changes each time it is queried, so the user cannot enter it into the URL themselves. If this step fails, the user cannot connect to a drone.   
  
This system ensures the control interface can only be opened from the client app and not through other methods (for instance, the user typing the URL into a browser themselves). This system is such that users can be identified easily, and that they cannot exploit possible loopholes (for example, opening the control interface while passing others' email as an argument).  
   
A more detailed, step-by-step explanation of this system is provided in the [Access Control System](https://leezehao.github.io/Kiki_Delivery_Docs/features/accesscontrol.html) feature page.  
  
### Main Control Interface

After connecting to the drone, users will begin receiving audio and video feed from the drone. The user's audio feed will also be sent to the drone.  

The functions users can perform are listed below:

##### Two-way Audio Communication


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
