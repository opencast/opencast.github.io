---
title: Westfälische Wilhelms-Universität
date: 2018-06-08
description: With about 45.000 students the University of Münster is one of the largest universities in Germany. Organized in 15 faculties, the scientific portfolio of the university contains a wide range of professions. Initially founded on April 16, 1780 it was later demoted to an academy in the 19, century. On July 1, 1902 Emperor Wilhelm II. reenacted Münster to a university, which became known under its present name five years later.
category: user
tags: [user]
logo: /assets/img/WWUMuenster_Logo_2017_rgb.png
---

## About the university
With about 45.000 students the University of Münster is one of the largest universities in Germany. Organized in 15 faculties, the scientific portfolio of the university contains a wide range of professions. Initially founded on April 16, 1780 it was later demoted to an academy in the 19, century. On July 1, 1902 Emperor Wilhelm II. reenacted Münster to a university, which became known under its present name five years later.

## About the project and the team
The lecture recording project within the University of Münster is called eLectures. The project was initially a one room test system. In 2015 the current team was formed with the goal to make lecture recordings possible in 20 lecture halls by the end of 2017. That goal was achieved.
The team consists of five people and is split into development and service. Both sides have one PhD candidate contributing to the project with their respective fields.

## Why Opencast?
With almost a decade of positive experience of using and contributing to an open source project (Moodle), it became clear that the lecture recording solution at the University of Münster should take a similar route. Joining an open source community is following the academic spirit: Contributing to a common goal and the common knowledge while also profiting from the knowledge and effort of the others.
In the few years the project is employing Opencast, it has already proven itself with its scalability and stability. Even though the project just left its earliest steps, Opencast gives the users at the University of Münster a good and constantly improving lecture recording experience.
How we use Opencast
As of the summer term 2018 we are recording about 40 lectures per week and a bit more than 500 lectures per term. These are spread out over about 50 lecture series. Most of the lecturers are from the faculties of Law, Psychology and Business and Economics. Within the faculties of Psychology as well as Educational and Social Science there is an active user community for the Opencast Annotation Tool.

## Deployment
Lecture recordings are ingested to and processed by an Opencast cluster of currently six servers. Together they form a Docker Swarm cluster wherein the Opencast Docker containers run. This approach eases the process of scaling out additional workers. It further aids in the ability to create Opencast test clusters either locally or on test machines. Three constantly available machines are used for such a staging environment. While some recordings are publicly available, most of the distribution is done via the established Moodle platform (the so called Learnweb) of the University of Münster. The faculty of law is running a separate Ilias platform, which is also connected to Opencast.

## Recording
Currently there are 21 lecture halls equipped with the lecture recording hardware. We are using a 4K security camera from Axis and a capture agent built into a standard 19” rack. The capture agent is a custom solution with 1U height and 29cm depth, containing a current-gen Xeon E3, a Supermicro mATX board with remote management functionality, 16GB RAM and a 256GB SSD. The audio- and presentation-capturing is done by a Magewell Pro Capture HDMI capture card. The capture agents usually record the source 4K signal, an alternative digital tracking signal from the camera, the FullHD input of the presentation and an audio track from the sound installation in the lecture hall. The capture agent software used is pyCA.

## How our work benefited the Opencast community
We try to contributed back to the community wherever we can. Multiple bug and security fixes as well as features were submitted and are now part of the upstream Opencast codebase. We actively participate in mailing list discussions, web meetings and conferences, where we also presented our work on associated projects. Here we initially developed and are currently maintaining the Opencast Docker images. Driven by multiple requests from lecturers, we further financed continued work on the Opencast Annotation Tool.

## Contact information
For more information please feel free to contact us: electures@uni-muenster.de.

