---
layout: post
title:  "GSoC with CERN-HSF (Part-2)"
date:   2018-08-22 04:00:00 +0530
---

Hello, I’m Aman, GSoC 2018 student under CERN-HSF. Last month, [I wrote about my Project and the work I did in the first month of the GSoC coding period](https://blog.amanpratapsingh.in/2018/06/08/GSoC-with-CERN-HSF-Part-1/).
This post summarises the work I did in the last two months of the GSoC coding period and what I achieved overall in the summer.

## The second Coding Phase

In the second coding phase, I mostly worked on designing and implementing the *Jobs* tab in Jupyter tree view. This tab currently enlists the information and status of all Ganga Jobs present in the Ganga Repository. However, for the future, it is planned that for the SWAN notebook service, this Jobs tab will also list the Jobs other than Ganga such as Spark Jobs.

![The Jobs tab which lists information and status of Ganga Jobs.](https://cdn-images-1.medium.com/max/1600/1*iytdldfk_PDOl13kREzyjQ.gif)

Later in the month, I worked on the most challenging part of the project i.e. modifying the Ganga to allow sharing the Jobs between multiple Ganga sessions. Ganga is a very old project at CERN. The first commit to its codebase is dated back to 2008 and it has approx 13k commits by now. Ganga originally was not designed considering the use case of sharing of Jobs for submission in one session and monitoring in different session which was required for my project. Honestly speaking, I was initially very afraid to dive inside Ganga’s code as I was completely naive about working on core Operating System related things like file and session locking and multi-threading. However, my mentor Kuba Sir and Prof. Ulrik guided me and also arranged a Skype call with Rob Currie, who is a member of the Ganga Core team to get help from him about how it can be done. Following the instructions of Rob, I added a feature in the Ganga to share Jobs between sessions.

## The third coding phase
In the third coding phase, my main task was to integrate and test the extension in CERN’s IT infrastructure and SWAN Notebook service. My mentor Diogo Sir arranged a physical QA box machine at CERN for black-box testing. Later, I and my mentors regularly tested the extension on the QA box and we fixed many bugs and issues of the extension. We also tested the Job submission to the Condor backend other than Local backend. Also in this phase, my pull request to the Ganga with all the changes I made for the SWAN integration was also merged in the main development branch of the Ganga Project.

## Final Report
The final report of my project is [available here](https://amanpratapsingh.in/gangaextension/).

## So, that was it?  
No, not really. This is just the beginning. In the future, I plan to regularly participate in the discussions of Ganga Project Team and contribute to the Ganga and other CERN’s open source project. CERN has a plethora of open source projects and it provides a very good opportunity for contributing to the biggest particle physics organization on the planet and I would definitely exploit this opportunity in the future.

## Final Words
Finally, I would thank my mentors from CERN — **Jakub Sir** for helping me throughout the project duration in every problem that I faced, **Diogo Sir** for helping me in problems related to coding and providing valuable coding lessons and **Enric Sir** for designing initial roadmap of the project architecture.
I am also thankful to my mentor from Imperial College, London — **Prof. Ulrik Egede**, who helped and guided me in all Ganga Toolkit related problems I faced.
Other than my mentors, I am also indebted to the **Mark Smith** and **Alexander Richards** from Imperial College as they weren’t directly related to my project but still helped me whenever I faced a blocker in my project.
In the last 4 months, I attended almost 15 Skype meeting with my mentors and around 10 meeting with Ganga Core Developers team. These interactions and discussions were surely the most exciting part of my project and I got to learn a lot of things like how the developer teams work, software development and professional ethics etc.
Last but not least, I am thankful to my senior at IIT Bhubaneswar, **Krishnan R** who encouraged me to apply for GSoC, introduced me to CERN-HSF, helped me writing the project proposal and also helped me many times during the GSoC coding period as my project was quite similar to his project in GSoC 2017 at CERN-HSF.
So this was all about my experience of 4 months as a Google Summer of Code student at CERN.
If you have any query about my project or just want to say Hi, feel free to drop a mail at: **aman.pratap.singh@cern.ch**

> This post was also published on my [Medium account](https://medium.com/@amanpratapsingh/gsoc-with-cern-hsf-part-2-5483005fc018).
