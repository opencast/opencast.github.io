---
title: University of Cape Town
date: 2019-10-01
description: The University of Cape Town (UCT) is a public research university. Founded in 1829, it is the oldest higher education institute in South Africa.  In 2018, 28 600 students were enrolled - with 17 552 undergraduate and 11 048 postgraduate students. 
category: user
tags: [user]
logo: assets/img/UCT-round-logo.png
---

## Background

The University of Cape Town (UCT) is a public research university. Founded in 1829, it is the oldest higher education institute in South Africa.  In 2018, 28 600 students were enrolled - with 17 552 undergraduate and 11 048 postgraduate students. There are over 4500 staff members consisting of academic, and professional administrative support and service staff.

The department of the Centre for Innovation in Learning and Teaching (CILT) is part of the faculty of Centre for Higher Education Development. Within CILT there are three clusters of work, including an academic staff development, course and curriculum design and learning technologies. The learning technologies team provide a number of educational services such as the learning management system (Vula) which is Sakai-based and lecture recording system which uses Opencast. The lecture recording system is closely supported by the Information and Technology Services (ICTS) for venue-related and server support.

## Why Opencast?

The team had previous experience and positive outcomes from running the current learning management system (Sakai) from open-source technology in  production for over a decade. 

Recording of lectures was occuring in an ad-hoc basis originally. In 2011, research into different lecture recording systems was investigated with Opencast being piloted the year after. There was rapid revamping of lecture venues during the [UCT Classroom Renewal project] (http://www.icts.uct.ac.za/uct_classroom_renewal_project) (2012-2017). In 2019, there are 118 recording venues across the different campuses, including the One Button Studio and other clinical teaching venues.

Opencast and Galicaster as an open-source software solution, provided advantages in both cost, scalability and robustness. There was good support and growth within the Opencast community over the years.

## Use cases

### Lecture recording
Recording of lectures is the main usage for Opencast system. Each of the teaching venues are equipped with a capture agent running Galicaster. From 2018, there are approximately 750 recordings per a week, with 3000 daily users and 7500 weekly users. There has also been a [lecture recording policy] (https://www.uct.ac.za/sites/default/files/image_tool/images/328/about/policies/Lecture_Recording_Policy_2017.pdf) introduced where by default a lecture on Upper and Middle campus are recorded (via the venue timetable), an opt-out consent model.

The main focus is on robustness, with a target of 98% reliability. Many of the venues now include an audio input into the camera stream, and if a recording fails to start, a fallback recorder captures through a PyCA server. 

### LTI integration

Opencast integrates with the learning management system, Sakai. There have been a number of customisations made, for example timetable scheduling, updating of metadata and allowing lecturers to upload their own content.

### Tracking

Blackboard legibility and quality of the camera stream has been one of the priority areas with the roll out of the lecture recording. The current PTZ camera models that are being used are the Axis 1448 and Axis 5915. Other than the Axis autotracking solution, there are a number of tracking solutions that have been adopted:
- [Lecturesight] (https://opencast.jira.com/wiki/spaces/LECTURESIGHT/overview): This would involve an overview camera (typically a Raspberry Pi) and live software tracking to adjust the PTZ camera.
- [Track4K] (https://track4k.co.za): An automated system that crops the 4K video stream to produce the effect of the lecturer being tracked.

### Captions
A more recent addition has been captions and transcripts. This is being done in a pilot phase through the Nibity API for high quality versions. It has also been trialled with the IBM Watson API, however with less accuracy.


### Other recording solutions
- [One Button Studio] (www.cilt.uct.ac.za/onebuttonstudio) has been custom setup for lecturers to pre-record short online videos. The venue records through the Galicaster capture agent, and ingests the recording to the Opencast server, which is configured via LTI to share the recording to the user through the learning management system.
- Clinical Skills: With a similar system to the One Button Studio, there are Galicaster plugins to adjust the tilt of the camera, and users also normally sign in with their institutional credentials via another Galicaster plugin.
- Screen recorder: Originally started up and used in an initial pilot phase, this screen recorder has since been enhanced by other institutions [(https://github.com/elan-ev/opencast-studio)] (https://github.com/elan-ev/opencast-studio). This is not yet put in production but will be looking at adding it in soon.

## Hardware-software description

We run a combination of virtualized and physical servers. Or worker nodes are all physical while the admin/engage, ingest, database and backup recorders are virtualized. All our servers run Ubuntu 16.04 and centralized storage is provided via NetApp. 
Our Opencast cluster is as follows: 
- 1 x admin and engage node ( 8 cores, 20GB RAM)
- 2  x ingest nodes (2 cores, 4GB RAM)
- 15 x worker nodes (396 cores in total)
- 1 x Mysql database (4 cores, 8GB RAM)
- 1 x backup recorder (pyCA) (4 cores, 4GB RAM)
- 1 x app server (2 cores, 8GB RAM)
All our capture agents run Galicaster, with Ubuntu 16.04/18.04 as the operating system. Ubuntu 18.04 will be installed going forward.

## Contact
Contact the CILT Learning Technologies team (help@vula.uct.ac.za) 


