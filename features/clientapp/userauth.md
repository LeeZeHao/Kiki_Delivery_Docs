---
title: User Authentication and Profile
layout: home
parent: Client Side Application
grand_parent: Features
---
# User Authentication and Profile

Users are able to create an account and login to the client side application. Currently, user authentication is implemented via Firebase Authentication, while user data is stored using Firebase Firestore database.

User authentication is based on the simple email + password system.  

The login and register screens are shown below.  

<p align="center">
<img src="https://github.com/user-attachments/assets/f18f76f2-40c7-4202-81f4-b7f1e7776aef" border="10"/>  
</p>
<p align="center">
Desktop login screen.  
</p>  
  
<p align="center">
<img src="https://github.com/user-attachments/assets/7af897ee-5fdc-4f4f-9b4f-1fb935851bb6" border="10"  width="300"/>  
</p>
<p align="center">
Mobile login screen.  
</p>
  
<p align="center">
<img src="https://github.com/user-attachments/assets/d18649ba-cd68-405a-ad87-d83d42ac5e67" border="10"/>  
</p>
<p align="center">
Desktop new user regsiter screen.  
</p>  
  
<p align="center">
<img src="https://github.com/user-attachments/assets/46098177-8ad6-4b87-8744-4df5f440d3b3" border="10"  width="300"/>  
</p>
<p align="center">
Mobile new user regsiter screen.  
</p>
  
### Email Verification
An email verification system is in effect. Only users which have clicked on the verification link sent to their email will be allowed to access the app’s features. This feature is implemented via a customized email template in Firebase Authentication.  

<p align="center">
<img src="https://github.com/user-attachments/assets/19e668a9-ff52-42bc-991b-b60ee8555235" border="10"/>  
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/ba3a200e-7e1f-49b4-b60f-3f03416f3fe7" border="10" width="300"/>  
</p>
<p align="center">
Confirmation screens shown after user registration.
</p>  

### Password Reset
Password resets are also implemented with Firebase Authentication. Users can apply for a password reset link to be sent to their registered email, which they can then use to reset their password.  

<p align="center">
<img src="https://github.com/user-attachments/assets/0450fa45-72bc-4b2a-96dd-bf64d7fbd4cc" border="10"/>  
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/c6db78c2-cfdd-434c-8b84-80d798d00166" border="10" width="300"/>  
</p>
<p align="center">
Password reset screens.  
</p>  

----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
