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

It is important to note that all of the information in each software is 'hidden' from the others unless intentionally exposed. The only sections where information is exposed or transferred are:  
1. Client app redirecting to drone control interface URL, with user email and access key obtained from Firebase Firestore as URL arguments  
2. User drone control interface connecting via WebRTC (video and audio channel + data channel) to drone side web app  
3. Python control script starting a WebSocket server to receive control signals from drone side web app  
4. Drone side web app interacting with the WebSocket server to send control signals to Python control script  

This approach brings the following benefits:  
1. Easier maintenance  
2. Modularity (as seen in "Modularization" section)  
3. Managing complexity, as large features can now be broken up into smaller sections to work on  
4. Facilitating cooperation, as different members can work on different sections without worrying about clashes  



In addition, abstraction principle is used in structuring the individual programs, in accordance with proper OOP principles.

----

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
