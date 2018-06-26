---
title: Universität zu Köln
date: 2015-05-01
description: Opencast is a central media service at the University of Cologne that unifies the management of automatic recorded lectures, educational media and blended learning material.
category: user
tags: [user]
logo: /assets/img/uni-zu-koeln.png
---

*Last update: October, 5th 2015*

## About the University of Cologne
Universität zu Köln Logo

The university was founded in 1388 by the townspeople of Cologne. Hence, the University of Cologne is still today a city university and with nearly 50.000 students the largest university in Germany.

## Project Goals
In summer 2014 the Computing Center (RRZK) started a two years project to set up a unified infrastructure on the campus for recording scheduled lectures and make the results available for students in the learning management system ILIAS. The access to those lectures is restricted to the students of that course.
Our goal is to provide Opencast as a regular service for managing educational content and facilitating the automatic recording of lectures. Additionally we will gradually expand the number of lecture halls with the needed capture hardware. For all participants – lecturers, students and technical staff – we see a great potential to increase efficiency by offering unified video management tools to the campus.
In the summer semester 2015 we already recorded 22 courses with an average of 40 hours/week.

<img src="http://www.opencast.uni-osnabrueck.de/wp-content/uploads/2015/02/uni-zu-koeln.png">

## Local setup
We build our own RPMs with Jenkins, use Cobbler to setup the VM servers and recording units and with Ansible we deploy needed software for server and capture clients. The configuration of a new VM server node takes about 20 minutes.

CAPTURE AGENTS:
To ease the maintenance of the recording systems we homogeneously use Galicaster units (http://wiki.teltek.es/display/Galicaster/Galicaster+project+Home). In autumn 2015 version 1.4.2 is installed. On units that are also used for live streaming events we installed the licensed Pro version.
Our Galicaster unit is a Dell 7010 SFF/XE2 SFF computer equipped with an I7 processor, 16GB RAM and two 500GB HDD. For capturing we use a Datapath Vision RGB-E1S (beamer signal) and a Blackmagic Decklink Mini (camera signal). Both signals were recorded as H.264 streams in an AVI container. The audio is recorded in a separate stream.
In large lecture rooms (> 300 seats) we use Sony EVI-H100S PTZ cameras. Our mobile units are equipped with consumer camcorders.

OPENCAST SERVERS:
We operate a production system (6 nodes, version 1.6.2), a pre-production system (3 nodes, version 1.6.2) and a development system (3 nodes, version 2.0.x).
Each system has its own database (Maria DB), shared file system (NetApp) and application on the Wowza streaming server.
This is a list of our current CentOS 6 production server infrastructure:

- 1 x Admin VM (4 cores, 8 GB RAM)
- 4 x Worker VMs (4 cores, 8 GB RAM)
- 1 x Engage VM (2 core, 2 GB RAM)
- 1 x MariaDB Database VM
- 1 x Wowza Streaming Server VM (2 cores , 8 GB RAM)
- 10 TB shared NAS storage

DISTRIBUTION:
Finished recordings are distributed and available using the LMS ILIAS. Only students who are registered in a course can access and watch the videos. It is up to the teacher whether a student can see all recordings of a course, or only the last one and how long a student has access to the videos. No download is offered, only streaming using the Wowza server.

## Next Steps
- Stabilizing the recording service – currently up to 5% recording are lost
- Deploying Opencast version 2.1 for the academic year 2016
- Introducing the advanced features of the Galicaster Pro Version
- Integration of the new Opencast External API
- Integration of the new ILIAS Opencast Plugin

## Contact information
For more information please feel free to contact us:

- Ruth Lang (langr@uni-koeln.de)
- Rubén Pérez Vázquez (ruben.perez@uni-koeln.de)
