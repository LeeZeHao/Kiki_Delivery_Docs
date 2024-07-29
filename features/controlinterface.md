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
<img src="https://github.com/user-attachments/assets/19b6d652-de63-42c0-ab86-3a29465d4854" border="10"/>  
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

<p align="center">
<img src="https://github.com/user-attachments/assets/7a0088a8-e8bf-4549-83ba-a835b5d6ebf6" border="10"/>  
</p>
<p align="center">
The control interface after connecting to the drone.
</p>

The functions users can access are listed below:

##### Drone Video Feed
This is achieved via WebRTC video channel. The image from the drone webcam is displayed in the center of the control interface.
##### Two-way Audio Communication
This is achieved via WebRTC audio channel. There is a speaker and a mic (integrated in the webcam) on the drone. Thus, users can directly communicate in this method.  
##### Control Drone Locomotion
Users can control the movement of the drone using a virtual joystick on the bottom left side of the screen, and two buttons on the right side of the screen (for pivot). Details about the implementation of drone controls are included below in the "Control Signals" section of the page.  
##### Control Camera Rotation
Users can control the rotation of the camera mount using a virtual joystick on the bottom right side of the screen.  
##### Control Scissor Lift
Users can control the raising and lowering of the lift using action buttons on the right side of the screen.  
##### View Remaining Drone Usage Time
Remaining drone usage time is always displayed on the left side of the screen, under the disconnect button.
##### Disconnect from the Drone
Users can click the green "Connected" button on the left side of the screen to disconnect. Remaining drone usage time will also stop being deducted.

### Control Signals

The drone control interface uses the WebRTC data channel to send control signals to the drone.  



----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
