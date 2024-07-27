---
title: Client Side Application
layout: home
parent: Features
has_children: true
---
# Client Side Application

A client (user) side application, which gives users access to all other implemented features.  
  
The application is available on Web and Android platforms.  
  
Currently, the client-side application is implemented via React Native, with web support achieved via the React Native Web plugin.  
  
Several other plugins are also in use to achieve various functionality, such as React Navigation for navigating between different screens of the app, and the Firebase plugin for Firebase functions.  

Various features under the client app are listed in seperate sections accessible via the sidebar.
  
#### Support for Both Web + Android Platforms

The application is currently confirmed to work on Web and Android platforms. Both versions of the application currently support the same features.  

Web support is achieved via the React Native Web plugin. This has allowed us to build both versions of the software using the same codebase.  

In order to improve user experience, we have also added seperate UI layouts for Web and Android since the last milestone. This is achieved by detecting the user's platform, and exporting the respective React Native component. As an example, below is the new login screen layout for Web and Android respectively.

  
<p align="center">
<img src="https://github.com/user-attachments/assets/f18f76f2-40c7-4202-81f4-b7f1e7776aef" border="10"/>  
</p>
<p align="center">
Desktop login.  
</p>  
  
<p align="center">
<img src="https://github.com/user-attachments/assets/7af897ee-5fdc-4f4f-9b4f-1fb935851bb6" border="10"  width="400"/>  
</p>
<p align="center">
Mobile login.  
</p>


----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
