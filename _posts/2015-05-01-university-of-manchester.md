---
title: University of Manchester
date: 2015-05-01
description: The University of Manchester has brought lecture capture to a new level. With an opt-out policy for lecturers and more than 300 equipped venues by the end of 2015.
category: user
tags: [user]
logo: /assets/img/mancherster-logo.png
---

## Project Goals
During 2011/12 the University of Manchester successfully piloted lecture capture technology on a small scale in 10 locations using Podcast Producer 2. By the end of the pilot in 2012 we had concluded that lecture capture was a great benefit for students and it would be made available in many more locations. We also concluded that Podcast Producer 2 would not be suitable for a large-scale deployment. A new project was commissioned to complete the following objectives:

Deploy lecture capture technology to 100 teaching spaces.
Construct a server system capable of processing and distributing thousands of recordings.
Implement a lecture capture solution which needs the absolute minimum of user initiation in the classroom or user intervention after capture.
As with the pilot, the system would support mono-stream video only. We would Record the output of the project with the theatre microphones.
Once project delivery was underway in 2012/13 the University Senate passed a new policy governing the use of lecture capture. This included a move to an opt-out model of adoption, all lectures at the University will now be recorded by default unless teaching staff indicate a preference not to be recorded. This added a new goal for the project to implement an opt-out capable system by September 2013.

## Overview of Deployment
Preparations for a Opencast deployment began during our first semester of term 2012, which started at the end of September. The pilot system based on Podcast Producer 2 would be used to record all Semester 1 (September to December) lectures in 10 rooms while new recording equipment was selected to replace the existing Mac Minis. Opencast has its own recording platform and there are several off-the-shelf options, an early task was to select a capture agent.

After a period of testing we chose Galicaster, which is a software application capable of making Opencast formatted recordings and working with Opencast’s capture agent API. One of the major advantages of Galicaster was that it allowed us to choose a hardware platform that closely conformed to the project’s needs. Many of the spaces we planned to install equipment were incredibly small and the use of Galicaster and Mini-ITX PCs running Ubuntu allowed us to buy a pre-assembled unit which measured only 24.5cm x 19.6cm x 8.3cm (9.7’’ x 7.7’’ x 3.3’’).

During the same period of time a Opencast cluster was deployed to our virtual machine infrastructure. This included:

- 1 x admin node (to control the system and schedule recordings)
- 2 x ingest nodes (inbound file transfer)
- 1 x presentation node (to generate RSS feeds)
- 2 x http file servers (outbound file delivery)
- 4 x worker nodes (video processing)
- 1 x Monitoring VM

With this work complete we were now in a position to make the switch from Podcast Producer 2 to Opencast in the two week gap between our first and second semesters. Starting in early January all Mac Minis were replaced with new the new Galicaster/Mini-ITX system which all pointed to the new Opencast cluster. With the migration complete we now had a solid system we could begin to expand to 100 locations. A notable success of the migration was that users were completely unaffected. Because Opencast was open-source we were able to make customisations to RSS feeds, work flows and authentication. From the user perspective it appeared as though nothing had changed despite every single element of the system being replaced.

From January to May all second semester lectures were captured with Opencast / Galicaster. Approximately 65 courses made use if the system, producing around 70 to 80 hours of recordings per week, driven by a schedule entered into the Opencast system. Work now began on the scaling of the network of recording and processing devices. The total installation target was increased to 120 rooms, and the number of Opencast nodes was increased in preparation:

- 1 x admin node
- 1 x dedicated database VM
- 4 x ingest nodes
- 1 x presentation node
- 4 x http file servers
- 8 x worker nodes
- 3 x Monitoring VM

Over the summer of 2013 the total installation base increased to 60 teaching spaces and this doubled to 120 rooms during the winter. During the same summer period the opt-out policy was passed (described in more detail below). This began a three month development program of a
software system capable of reading in the University timetable. This allowed people to opt-out and the schedule of recordings in Opencast.

The production system now routinely records over 1,000 hours of recordings during a typical teaching week.

## Capture Agents
Currently all 120 locations use a Mini-ITX small form factor PC running Galicaster. The PC is built using off the shelf components and is assembled off site by mini-itx.com. Each unit has an i3 Intel processor, 60 GB SSD, Gigabyte H series motherboard and 1 x PCI-E x16 card slot used for a Blackmagic capture card. When the ‘blank’ capture agents arrive a common version of Lubuntu is installed on five units at a time, followed by Ansible to add all necessary software, dependancies and configuration.

There is a great deal of variety in the audio/video environment of our lecture theatres. The mini-ITX + Galicaster combination has allowed us to over come two key problems in this area. The first is that the hardware platform is physically small enough to install inside existing lecterns and desks. The second is that with the use of a Kramer VP-435 video scaler and our capture agent, we now have a single hardware platform that is compatible with all the AV inputs across 120 spaces.

## Monitoring
Currently we use three forms of monitoring to maintain quality an increase operational awareness.

Nagios monitoring allows us to know the state and load of all our Opencast servers and capture agents. Generally this is used for sys-admin type troubleshooting, such as spotting when a storage device is nearing capacity or measuring the uptime of a unit. The example
below shows the load on a capture agent increasing as it performs recordings. Gaps in the data represent the capture agent shutting down at night.

<img src="http://www.opencast.org/wp-content/uploads/2015/07/manchester1-300x217.png">

New Relic monitoring allows us to see a great deal of application orientated data from the Opencast cluster. This includes information about the JMV and its activity, but also highly detailed information about the SQL database, its responsiveness, load and query specific data. Most recently we used this to identify a resource intensive query which was removed, reducing the total database load by approximately 90%.



The Capture Agent Monitor is the final monitoring tool we use. Originally developed by Universitat Politécnica de Valencia, it is a web based tool that allows you to monitor the input and activity of all capture agents simultaneously. Each box represents a lecture theatre and what the projector is currently displaying. There is an audio levels meter, web based VNC and information about its current schedule of jobs. The monitor also allows a technician to remotely monitor audio quality and make adjustments.

<img src="http://www.opencast.uni-osnabrueck.de/wp-content/uploads/2015/07/manchester3.png">

## Opt-out Policy
In late June a lecture capture policy sponsored by Prof. Richard Reece, the Associate Vice President for Teaching, Learning and Students, was approved by the University Senate. One of the key aspects of the policy was to move the University from the previous opt-in model
(academics volunteering to be recorded) to an opt-out model (lectures will be recorded unless an academic specifies that they should not). This was a major change for the project and required the creation of a Opencast module which could synchronise a recording schedule with the timetable, while at the same time allowing academics to express a preference for not being recorded.

The development work for what would become the Participation Management Module (PM) was contracted out to a commercial company that offers professional services for Opencast, Entwine GmbH. Within two months Entwine had produced a functional module with timetable integration, user and management UIs and a set of rest end points. An example of the UI for users is below.

<img src="http://www.opencast.org/wp-content/uploads/2015/07/manchester4-300x173.png">

We launched with opt-out in September and the results were immediate and dramatic. With opt-in we were expecting somewhere between 10-20% of all lectures to be recorded, with opt-out this figure rocketed to 70%. The effectiveness of this change can be seen in our first round of feedback from students, 97% of the responses about the lecture capture service were either praising its use or asking for it to be extended to more courses.

## Why Did You Choose Opencast?
The University of Manchester did not have a preference when it came to the use of open-source or commercial system when it came to lecture capture. We did find that Opencast had certain features that made it ideal for our situation:

- Cost – Opencast proved to be incredibly cost effective, with no licensing or support fees Opencast was easy to test with no financial commitment and long term operating costs were very low.
- Scalability – The modular system design of Opencast meant that we were free not to use elements that did not suit our deployment scenario. This also meant that we could run many instances of high demand services in parallel, such as workers and ingest nodes.
- Customisation – The compressed timescale of the project required new functionality to be delivered in a very short space of time. It also required the project to be flexible, delivering change and adapting to the needs of the University rapidly. The open nature of Opencast allowed us to deliver change swiftly, with direct access to the code base we were free to develop new extensions, functions and fixes with the minimum of time.

## How has your work benefitted the Opencast community?
We now have two committers within the Opencast Community who have worked on over 100 bugs and patches for various Opencast releases, donating time to assist with QA efforts. During 2014 we intent to publish our participation management system, once it is fully complete and
documented. During 2014/15 we plan to focus on increasing Opencast performance for scaling and service decentralisation, which will benefit other users and allow Opencast to support even larger installations.

## Contact information
For more information please feel free to contact us:

Stuart Phillipson, Project manager and operations.
James Perrin, Developer
Tobias Schiebeck, Developer
Andy Wilson, Developer