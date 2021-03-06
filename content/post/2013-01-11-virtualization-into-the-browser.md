---
author: minko_gechev
categories:
- Browsers
- Development
- HTML5
- Http
- Image processing
- Internet
- Java
- JavaScript
- Linux
- OpenSource
- Programming
- RDP
- Ubuntu
- Virtualization
- VNC
date: 2013-01-11T00:00:00Z
tags:
- Development
- HTML5
- JavaScript
- OpenSource
- Programming
- Projects
- Virtual Machine
- Virtualization
- VM
title: plainvm
url: /2013/01/11/virtualization-into-the-browser/
---

<a href="http://plainvm.mgechev.com/" target="_blank">plainvm</a> can take the virtualization into different level of usage. To prove this I’ll first ask few rhetorical questions and put their answers...Which is the programming language which everyone has interpreter for? Java? Actually no! Does iOS supports Java applets for example?! No! Everyone has a browser in his smartphone. Every browser (well may be I should exclude lynx, links...) has JavaScript interpreter. And what is the common thing between all modern devices (and actually the devices most wide spread) – the browser. Another problem is that you don’t have such a great resources onto your mobile devices to run Windows/Linux/Mac even with double boot (yeah we can argue here about Debian...probably). We can use remote desktop via VNC/RDP but we have to install extra software and we will have access to a single machine not a whole cluster (well actually we can...I agree we can switch through different sessions, we can also become crazy).

For a while I’m working on an opensource project (for good or bad written in perl) called <a href="http://plainvm.mgechev.com/" title="plainvm" target="_blank">plainvm</a>. It’s main goal is to provide web interface for virtualization platforms. You can control your Virtual Machines (VMs) using your browser (stop, start, change parameters) and also log into these machines and use them! The project and all it’s components are absolutely free for non-commercial use! For the functionality I’ve mentioned I’ve used different opensource projects and brought them together with a lot of Perl and JavaScript glue. Of course event with the localStorage feature (since HTML5) we still don’t have enough memory to create a pure virtualization into the browser (only with HTML5 and JavaScript), that’s why I’ve used already proven virtualization platform for that goal. The project uses VirtualBox as core virtualization platform (of course it’ll cost you to implement just a single class for using VMware player or VMware Workstation for example). I won’t publish more details about the implementation, if you’re still curious you can visit the project’s repository at <a title="plainvm @ github" href="https://github.com/mgechev/plainvm" target="_blank">GitHub</a>, if you’re not enough curious just watch the video below and your curiosity should make you check the GitHub link.



In the next few lines I’ll make a summery of few of the most useful sides of plainvm:

*   It’s easy to use
*   It’s pure HTML5 (no plugins at all)
*   It’s lightweight
*   It uses websockets for duplex communication channel between the client and the server
*   With plainvm you can manage multiple hosts hosting different virtual machines

The project is very young, I’m planning and developing it’s features in my spare time so I cant accomplish everything I want. If you need any feature or you just like the idea and want to help, feel free to contribute. Extra implementation details can be found in the project’s wiki page (<a href="https://github.com/mgechev/plainvm/wiki" title="Wiki" target="_blank">at GitHub</a>). I tried to make the code readable enough to be as much easy to understand as possible.
