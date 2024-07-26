---
title: User Testing
layout: home
parent: Testing
---
# User Testing
  
Our system heavily relies on Internet connectivity for both the client app and the drone control aspects. 
  
Results of user tests conducted are as follows:

##### First User Test  
|    | **Test**                                                                        | **Result**                                                                                                                         | **Action Taken**                                           |
|----|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| 1  | Register + Login to client app                                                  | Success                                                                                                                            | -                                                          |
| 2  | Home page info display                                                          | Success, with little delay from Firestore fetch                                                                                    | -                                                          |
| 3  | Profile page info display                                                       | Success, with little delay from Firestore fetch                                                                                    | -                                                          |
| 4  | Update drone usage time after purchase                                          | Success                                                                                                                            | -                                                          |
| 5  | Client app opens control interface                                              | Success, passes correct URL parameters                                                                                             | -                                                          |
| 6  | Opening of control interface                                                    | Success                                                                                                                            | -                                                          |
| 7  | (Control interface) Access control system using email and access key parameters | Lets users connect only if both email and access key are correct. Success                                                          | -                                                          |
| 8  | Connect to drone                                                                | Connects using WebRTC to drone and turns on drone camera view after connection. Success                                            | -                                                          |
| 9  | User view drone audio and video                                                 | User can receive audio and video from drone onboard webcam clearly. The video FOV is improved greatly from last milestone. Success | -                                                          |
| 10 | Drone plays user audio                                                          | User audio can be clearly heard from the drone speaker. Success                                                                    | -                                                          |
| 11 | Control drone movement                                                          | There is little lag in both movement and camera view. The control experience is satisfactory. Considered success                   | -                                                          |
| 12 | Control drone camera rotation                                                   | Camera rotation servo motors could not worked reliably. Failed.                                                                    | Fixed servo motor ground wiring.                           |
| 13 | Control drone scissor lift                                                      | Scissor lift was not able to be lifted properly by motor.                                                                          | Redesigned central screw shaft + used oil for lubrication. |
| 14 | Timer system                                                                    | Remaining usage time by user displayed properly and updated in Firestore database. Success                                         | -                                                          |
| 15 | Disconnect from drone                                                           | If disconnected from drone while moving, drone will keep repeating last instruction received. Not ideal, considered fail           | Fixed in drone Python script software.                     |

##### Second User Test

----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
