---
title: User Data and Profile
layout: home
parent: Client Side Application
grand_parent: Features
---
# User Data and Profile

User data, including email, username, and drone usage time, is stored via Firebase Firestore database.  
  
During first time user setup (see below), a new document is created under "user_data" collection in Firebase Firestore. This document has the user's auth ID (collected from Firebase Authentication) as it's name, and contains all the user data mentioned above in it's fields. In this way, it is easy to find a one's own user data while logged in, as the auth ID is readily available from authentication information.  
  
### First Time User Setup
  
On first login, users are prompted to choose a username. As Firestore is a read/write database, the username can still be changed later at any time.  
  
Once they confirm, a new document is created under "user_data" collection in Firebase Firestore, with the specfications listed before.

<p align="center">
<img src="https://github.com/user-attachments/assets/f047fe12-f5e6-496a-847d-feb24e7cc4cd" border="10"/>  
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/b56b5646-b5c4-43f5-a442-04a3f26e7c51" border="10" width="300"/>  
</p>
<p align="center">
First time users are asked to choose a username.
</p>  

### Profile Page
  
Users can view their current account information, and change their username in the profile page.  
  
<p align="center">
<img src="https://github.com/user-attachments/assets/0450fa45-72bc-4b2a-96dd-bf64d7fbd4cc" border="10"/>  
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/c6db78c2-cfdd-434c-8b84-80d798d00166" border="10" width="300"/>  
</p>
<p align="center">
Confirmation screens shown after user registration.
</p>  

----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
