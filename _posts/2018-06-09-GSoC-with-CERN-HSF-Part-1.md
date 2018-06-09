---
layout: post
title:  "GSoC with CERN-HSF (Part-1)"
date:   2018-06-09 04:00:00 +0530
---

![](https://cdn-images-1.medium.com/max/800/1*tO8m8T4r33ITpdrRaGLfQA.jpeg)

I have been selected in Google Summer of Code 2018 under CERN-HSF umbrella organisation. My project is co-mentored by HEP Software Foundation and Imperial College, London.


This was the first time I applied for GSoC. It was my dream from the freshman year and I started preparing for it from a long time ago. I started writing code for fun, published it on Github, contributed to multiple open source projects. The first major milestone in my open source journey was in December last year when my first PR got merged in Jupyter Lab and I got an invitation to become part of JupyterLab organisation on Github. Later when GSoC announced selected organisation, I started searching for organisations. One of my college senior was GSoC 2017 student and he suggested me to apply for CERN-HSF. I applied for project Large-scale computing backend for Jupyter notebooks - HTCondor batch job submission and monitoring using the Ganga toolkit. On April 23, the results for GSoC 2018 came and my project proposal got accepted.

![](https://cdn-images-1.medium.com/max/800/1*RNr-rgG0iUbqoqFRjmahbQ.png)

## Project Synopsis
Jupyter Notebook is an interactive computing environment that creates notebooks which contains computer code as well as rich text elements like equations, figures, plots, widgets and theory. These notebooks are easily understandable and can be executed to perform interactive data analysis, scientific computing and code prototyping.
In experiments like LHC(Large Hadron Collider), a very large amount of data (in order of petabytes) is generated. This huge amount of data is then processed using a collection of powerful computers at multiple computing sites by distributing the data in small chunks and processing them individually at remote distributed computing network and then finally collecting the result. These multiple sites are interconnected by a grid. These type of Grids can be accessed by a toolkit called Ganga.
Ganga is an open source iPython based interface tool to the computing grid which leverage the power of distributed computing grid and provide scientists an interface supported by a powerful backend where they can submit their computation intensive programs to Ganga as a batch job. After submitting the job, Ganga processes the program somewhere on the grid, it keeps track of status of the job and after completion of job it gives back output to the user. It can also provide job statistics and job errors, if any.
HTCondor is a workload management system created by University of Wisconsin-Madison. It is based on High-Throughput Computing which effectively utilizes the computing power of idle computers on a network or on a computing grid and offload computing intensive tasks on the idle machines available on a network or computing grid. It provides various features such as job queueing, job prioritization, resource monitoring and management etc. HTCondor provides intelligent resource management by match-making resources available on different machines and resources required by program.
This project aims to create a plugin for Jupyter Notebook and also integrate it to SWAN Notebook service which is a cloud data analysis service developed and powered by CERN. This plugin will easily submit and monitor batch computation jobs to HTCondor using Ganga toolkit. The plugin will display status of ongoing job, progress bar, job statistics and errors in Notebook itself and will also allow termination of ongoing jobs. The plugin shall provide user-friendly Notebook interface to easily perform computation intensive task on Notebook by integrating cell based structure of Notebook to submit jobs and peeking the progress and statistics of the job executed from a cell.

**tl;dr : My project involves creating a Jupyter extension for submitting and monitoring large-computation jobs from Jupyter based notebooks using Ganga Toolkit interface to HT Condor backend.**

## Community Bonding Period
The first phase for selected students was community bonding period which started on April 24th. In this period students familiarise with organisation's community, understand code base, contact their mentors and decide their communication modes, meeting time etc. Fortunately, I have 5 mentors  for my project (most of the projects have only 1–2 mentors). We decided to have a Skype meeting for project status reporting and other guidelines on each Friday for the project duration.

## First Coding Phase
The first coding phase started on May 14th. In this phase, I started creating Jupyter Extension for writing job details inside notebook. For this, I registered a Ganga Cell Magic in IPython kernel and then this magic compiles written job and submits it to Ganga. After submitting the job, kernel extension sends a job info message to frontend using Jupyter's comm API. The frontend parses the received job info and displays a widget below Ganga Magic Cell. This widget contains all the job info like Appliation, backend, subjobs, splitters etc. After sending the job info, the kernel creates a new thread and send job status to frontend each second until the job finishes. The frontend widget consist buttons for killing job and resubmitting failed jobs.


![](https://cdn-images-1.medium.com/max/800/1*-Iv2XOcShgcm7MoAWLP6Ew.gif)

## The Road ahead
In the subsequent weeks, I'll design a paradigm to integrate the notebook's namespace with Ganga job submission session and output of job. The next goals for my project are:
- Creating a Ganga Jobs tab in Jupyter tree view to monitor Ganga Job Repository.
- Updating extension to facilitate job application script writing inside same notebook.
- Testing extension on real large-computation batch jobs using Condor backend.
- Testing plugin on CERN's batch infrastructure.
- Integrating the extension to SWAN (CERN's on demand notebook service).

So this is all for my first GSoC blog. In my next blog, I'll update the second coding phase(Jun 15-July 8) progress. If you have any query related to my project and just want to say Hi, feel free to ping me. Thank You for reading, have a pleasant day ahead.

This post was also published on [Medium](https://medium.com/@amanpratapsingh/gsoc-blog-1-7939b0f80456)