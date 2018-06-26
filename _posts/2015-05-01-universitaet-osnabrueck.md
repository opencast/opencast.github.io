---
title: Universität Osnabrück
date: 2015-05-01
description: Osnabrück was the first university to run an Opencast installation in production. They are leading the Opencast Player development. Opencast is extensively integrated into their LMS Stud.IP.
category: user
tags: [user]
logo: /assets/img/uos-logo.png
---

*Last update: August, 1st 2015*

## About the University of Osnabrück
<img src="http://www.opencast.uni-osnabrueck.de/wp-content/uploads/2015/07/uos-logo-small.gif">
Osnabrück University, founded in 1974, is a young, vibrant university in northwest Germany that is renowned for its research and teaching in the areas of Humanities, Social Sciences, Science, Law and Business Administration/Economics. The University provides ideal conditions for over 11.000 students and PhD students to learn and conduct research.
Its Center for Information Management and virtual Teaching (virtUOS) is managing the universities e-learning activities. Because of this virtUOS is engaged in several open source projects, with the LMS Stud.IP and Opencast as the larger ones among these.

The virtUOS started a homegrown lecture recording software back in 2003. In 2008 the homegrown software was dropped to contribute to Opencast. Much of the know how around the player development has been transferred to the Opencast Player. It was very appealing to contribute to a larger project that would become a more flexible and reliable base for future developments.

The University of Osnabrück was the first institution with a production system based on Opencast 1.0 back in 2010. Usually the University of Osnabrück is piloting at least some new features of upcoming Opencast releases (like the video-editor, or the new player).

Additionally the ELAN e.V. that is closely related to the virtUOS, is providing Opencast support for its member institutions and offers also commercial support and development services to other german universities.

## Local setup
<img src="http://www.opencast.org/wp-content/uploads/2015/07/schloss-uos-300x110.jpg">

The university is recording around 35 lectures per week currently. That subsumes to around 2000 hours of recordings per semester. In total there are over 4000 recordings within their Opencast system.

Current CentOS 6 server infrastructure:

- 1 x Admin VM (4 cores, 12 GB RAM)
- 4 x Worker VMs (12 cores, 8 GB RAM)
- 1 x Engage VM (1 core, 4GB RAM)
- 1 x MariaDB Database VM (4 cores, 8GB RAM)
- 1 x Wowza Streaming Server VM (2 cores, 4GB RAM)
- 25TB shared storage
- 13 rooms with capture agents in various versions (Reference CA, Galicaster, NCast, Extron)
- 8 rooms additionally equipped with Raspberry Pi backup capture agents.

The Opencast system integrates into the Stud.IP LMS, where local developers have created a very powerful plugin that does not only allow to watch the recordings within the LMS, but also allows to upload and schedule recordings, including an import of the metadata from the LMS course and session description. Additionally even the embedding of recordings in forums and other text-areas is possible.

## How has your work benefitted the Opencast community?
Since the beginning of the project the lead of the Opencast player development has been in Osnabrück. The new very modular HTML5 player in Opencast 2.0 has been developed by developers in Osnabrück. And there is currently still much afford to improve the player with a new functions and a better usability.

The QA manager for Opencast is since 2014 from Osnabrück.

The developers in Osnabrück are also interested in capture solutions. TheRec is a capture software for Windows PCs and PyCA is a software that is intended to record with a Raspberry Pi, but it has also proven that it can work on other devices too.

The Osnabrück Opencast team was among the initiators of the german-speaking Opencast community branch that is usually meeting once a year.

## Contact
Rüdiger Rolf, Project lead (rrolf@uni-osnabrueck.de, +49 541 969 6511)
Lars Kiesow, Opencast QA manager (lkiesow@uni-osnabrueck.de, +49 541 969 6533)
Christian Greweling, Opencast Administrator (cgreweling@uni-osnabrueck.de, +49 541 969 6520)
Waldemar Smirnow, TheRec Developer (wsmirnow@uni-osnabrueck.de)