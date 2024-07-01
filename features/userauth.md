---
title: User Authentication and Profile
layout: home
parent: Client Side Application
grand_parent: Features
---
# User Authentication and Profile

### Proposed

Users are able to create an account and login to the client side application. User profile and information is stored in a cloud database.  
  

### Current Progress

User authentication is implemented via Firebase Authentication. Users can use their email to create an account. 

<p align="center">
<img src="https://github.com/LeeZeHao/Kiki_Delivery_Docs/assets/46279960/3d911dd0-ed83-4ccb-9375-97b6827cbe04" border="10"/>  
</p>
<p align="center">
Current Mobile Login and Register Screens
</p>

<p align="center">
<img src="https://github.com/LeeZeHao/Kiki_Delivery_Docs/assets/46279960/cb6e28e7-cb3d-4416-aa8c-fd1eb67050fe" border="10"/>  
</p>
<p align="center">
<img src="https://github.com/LeeZeHao/Kiki_Delivery_Docs/assets/46279960/98393732-5840-4021-8cba-5c3f85478d38" border="10"/>  
</p>
<p align="center">
Current Web Login and Register Screens  
</p>
  
An email verification system is in effect. Only users which have clicked on the verification link sent to their email will be allowed to access the app’s features. This feature is implemented via a email template in Firebase Authentication.  
  
Password resets are also implemented with Firebase Authentication. Users can apply for a password reset link to be sent to their registered email, which they can then use to reset their password.  
  
User data, including email, username, and drone usage time (discussed below), is stored via Firebase Firestore database. On first login, users are prompted to choose a username. This data is stored in this system. Any purchase or decrease in drone usage time is also saved in this way.  
  
Users can view their current account information, and change their username in the profile page.  
  
<p align="center">
<img src="https://github.com/LeeZeHao/Kiki_Delivery_Docs/assets/46279960/d76601a5-cb6a-4658-97c8-5d138cc9db5b" border="10"/>  
</p>
<p align="center">
<img src="https://github.com/LeeZeHao/Kiki_Delivery_Docs/assets/46279960/c5cde75a-e083-410d-a4ee-1b7bfd940d07" border="10"/>  
</p>
<p align="center">
Current Mobile and Web Profile Screens  
</p>

----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
