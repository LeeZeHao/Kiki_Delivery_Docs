---
title: Authentication and Authorization
layout: home
parent: Software Engineering Practices
---
# Authentication and Authorization

In our project, there is a system that tracks the user’s drone usage time. Therefore, there has to be a user account system.  
  
Our authentication system is mainly handled by Firebase Authentication. Currently, users are able to sign up using their email address, and the system supports email verification (users cannot use the app until they verify their email) and password resets (users will receive a password confirmation email).  
  
Each user also has a (changeable) username and a record of how much drone usage time they have left. This extra information is kept in a user profile stored in Firebase Firestore database. This database can also be accessed by the client control interface, so that the drone usage time remaining of each user can be decreased.  
  


----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
