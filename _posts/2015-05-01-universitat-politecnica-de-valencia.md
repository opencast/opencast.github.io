---
title: Universitat Politécnica de Valencia
date: 2015-05-01
description: The Universitat Politécnica de Valencia provides with the Paella Player an alternative engage player for Opencast. They are also initiated the Capture Agent Dashboard software.
category: user
tags: [user]
logo: /assets/img/upv-logo.png
---

Over a one year period ending in June 2013, the Universitat Politécnica de Valencia (UPV) implemented Opencast as a lecture recording solution for their campus. As of June 2013, UPV had installed 36 lecture halls with capture agents, and recorded the lectures of 53 teachers, resulting in 1400 lectures recorded with a peak usage of 150 hours/week.

## Project Goals
At Universitat Politécnica de Valencia (UPV), we didn’t have a really capable lecture capture solution, so we targeted Opencast in order to be able to record scheduled lectures, up to a long-term objective of 500 hours/week. We believe this is a great add-on for our local students.

The Videoapuntes project is carried out inside of a broader set of activities of the Universitat Politécnica de Valencia directed to support the production and use of technological assets by our students and teachers.

The project has been carried out by the IT department of the University, in the E-learning and Media Services units. The Media Services unit is composed by 6 people.

## About UPV
Universitat Politécnica de Valencia (UPV) is a public university of 35,000 students, located in the Eastern part of Spain, near the Mediterranean Sea. Most of our lectures are from engineering subjects.

## Scale of project
After some preliminary tests in the first semester of 2012, UPV launched a call in June 2012 to ask for teachers and facilities that wanted to have their lectures recorded as part of the project. Teachers had to agree to record all their regular lectures and facilities have to contribute to 50% of the installation cost. This call was open to all the university until December 2012.

As a result of this call we installed 36 lecture halls though the different facilities, and we recorded the lectures of 53 teachers. Through June 2013, we recorded 1400 lectures recorded, and a peak of 150 hours/week.

Lectures recorded with Opencast are published automatically in our internal Sakai CMS. The access to those lectures is restricted to the students of that course.

## Overview of the system
We use a fixed setup for all the recording lecture halls, to ease the maintenance of the system.

As the capture agent (the equipment that Opencast uses to make the actual recordings) we use Galicaster (http://wiki.teltek.es/display/Galicaster/Galicaster+project+Home). We began with the 1.2 version and we have been upgrading up to the current one (1.3.1).

The Galicaster PC is an i5 Computer with a Datapath RGB capture card and a Logitech USB Webcam 1080p. We record both the teacher and the computer video in h.264, to avoid re-encoding (as much as possible) in the Opencast core.

In our first tests we find out that one of the biggest problems was that many times the teacher failed in activating the micro. So in our setup we have installed 4 fixed microphones on the stage with a noise gate, and we record the audio from that fixed microphones.

<img src="http://www.opencast.org/wp-content/uploads/2015/07/valencia1.jpg">

<img src="http://www.opencast.org/wp-content/uploads/2015/07/valencia2.jpg">

<img src="http://www.opencast.org/wp-content/uploads/2015/07/valencia3.jpg">

<img src="http://www.opencast.org/wp-content/uploads/2015/07/valencia4-300x200.jpg">

From the server part, we have been using Opencast 1.3.1 for all this academic year. Our differences with an out-of-the-box setup are:

- LTI integration with the SAKAI CMS
- No reencoding of the H.264 MP4 file
- Downloadable content (no streaming)
- Usage of Paella Engage Player, instead of the standard engage player

About the University CMS (SAKAI) integration, the students see a new tab with the recordings, which in fact is an iframe to the Opencast engage server. The main features are:

- Display recordings within each course site
- Only students and teachers of a course can access their recordings
- There is an interval after the recording in with a teacher can withdraw that recording

The Paella Engage Player is the UPV contribution to the Opencast ecosystem. It is a HTML5 multistream video player capable of playing multiple audio & video streams synchronously and supporting a number of user plugins. It is specially designed for lecture recordings, like Opencast lectures.

By using Paella students can view both the lecture hall and the teacher’s screen, get info about the lecture (slides, OCR, series videos, footprints) and interact with the lecture (views, comments). Teachers can also soft edit the lecture to set the start and end point or make breaks in the recording.

Currently we are running the third main release of Paella. in June 2012 we released the 1.0 version and in January 2013 we released version 1.2. Current release is 2.0, and has been developed to work together with the Opencast 1.4 version.

More about Paella in its site (http://paellaengage.webs.upv.es)

<img src="http://www.opencast.org/wp-content/uploads/2015/07/valencia5-300x169.jpg">

## Why did you choose Opencast?
Universitat Politècnica de València has a long history in applying technological solutions to the learning processes. We also prefer open source solutions, as we can both tailor it to our specific needs and also be able to help the community around them. We tested this framework within the Sakai project and when we heard about the Opencast community we decided to join.

We especially like the scalabilty that Opencast provides. We are a centralized IT department and we like centralized scalable solutions, like Opencast and Sakai, and not small different installations. We like also the Java platform and the modular architecture of Opencast.

## How has your work benefitted the Opencast community?
UPV has made, and will cotinue to make several in-house developments, and all of them have been shared to the Opencast community.

- Paella Engage Player http://paellaengage.webs.upv.es/
- Dashboard for monitoring Galicaster capture agents http://github.com/polimediaupv/dashboard

## Next Steps
We are extending the videopauntes services in many ways, as we have a huge quantity of proposals from our teachers. Our next steps are:

- Getting more stability in the recording service – less than 2% recording loss
- Running the Opencast 1.4 version for the 2013-2014 academic year
- Implementation of CAS integration
- Several updates on the Paella Engage Player
- Evaluation through the Analytics Services

## Contact Information
Carlos Turró turro@cc.upv.es

## Examples/Samples
Paella Engage samples: http://paellaengage.webs.upv.es
Lecture sample: http://videoapuntes.upv.es:8080/engage/ui/watch.html?id=fdb9ab05-9344-4d63-ae11-904cac90e156
Monitoring Dashboard: https://github.com/polimediaupv/dashboard/blob/master/screenshot.png


