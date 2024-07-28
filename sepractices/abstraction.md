---
title: Abstraction
layout: home
parent: Software Engineering Practices
---
# Abstraction

Abstraction is the practice of hiding unnecessary information and displaying only necessary information to the users interacting with a specific component. This is an essential practice on Object Oriented Programming. Due to the needs of managing a multi-software project, we have applied this to the project as a whole as well.

This is a hybrid hardware/software project with significant complexity. Due to both necessity of the technologies being used (for instance, it is easiest to drive hardware with Raspberry Pi using Python scripts), and In order to ensure easy collaboration, the software section of the project consists of multiple sections, including:  
- Client app (Written using React Native + Expo framework)  
- Client drone control interface (Written using basic HTML + JS)  
- Drone end web app (Written using basic HTML + JS)  
- Drone hardware Python control script (Written using Python)  

<p align="center">
<img src="https://github.com/LeeZeHao/Kiki_Delivery_Docs/assets/46279960/502c45e0-ce7e-45ae-8e37-b70388dacec5" border="10"/>  
</p>
<p align="center">
Software system overview
</p>

These different programs operate separately and only communicate between each other when needed. For instance, the client app links to a URL where the drone control interface is hosted, and the drone end WebRTC control app communicates with the Python script using WebSocket.  
  
This ensures that:  
1. The different programs can be easily split up to be developed and maintained by different people.  
2. The scope of each separate program is manageable and less complex, speeding up development.  
3. It is much easier to pinpoint any errors that occur.
  
Aside from that, there are also examples of modularization within each of the separate programs. For instance, each screen in React Native is largely self contained.


----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
