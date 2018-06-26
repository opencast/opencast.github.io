---
title: transLectures
date: 2015-05-01
description: The EU-funded translectures project focuses on the automated transcription and translation of lecture recordings.
category: user
tags: [user]
logo: /assets/img/translectures-logo.png
---

## Project Highlights

*Project Name*: transLectures
*Project Goals*: Develop automated transcription and translation technologies for Opencast
*Partners involved*:7 European research institutions, universities, and companies:
Univ. Politecnica de Valencia, Xerox SAS, Jozef Stefan Institute, Knowledge 4 All Foundation, RWTH Aachen, European Media Laboratory, Deluxe Media
*Project duration*: 2011-2014
URLs:
http://www.translectures.eu/project-summary/
http://videolectures.net/translectures_demo_matterhorn_integration/

## Background
With 23 official languages in 27 member states, the European Union is a prime example of multilingualism. And despite the fact that English is more and more becoming a lingua franca, this holds true for the European academic landscape. Any knowledge exchange therefore has to overcome language barriers at some stage in order for the wealth of European academia to unfold.
<img src="http://www.opencast.org/wp-content/uploads/2015/07/translectures1.png2">
Alfons Juan-Císcar, project lead
ALFONS JUAN-CÍSCAR, PROJECT LEAD

It comes as no surprise therefore that the European Commission funds projects to help overcome resulting issues and shortcomings: transLectures is one of these, dedicated to developing innovative, cost-effective tools for the automatic transcription and translation of educational videos. Its goal is to pave the way for knowledge discovery in video repositories across language barriers.

“transLectures will make educational content accessible across language barriers”, Alfons Juan-Císcar, project lead

## The Project
A research project first and foremost, transLectures focuses on automatic transcription and translation, developing tools capable of generating automatic subtitles for academic lectures or talks recorded on video. The project is based on massive adaptation, which is where existing general-purpose tools are automatically tailored to a domain in order to better handle the scientific linguistic typology. This process is guided by multimodal meta data (keywords) extracted from presentation slides that often accompany the videos. Secondly, given that current automatic systems (transLectures included) are not yet capable of producing subtitles that are sufficiently free of errors as to be considered fully usable, work is also being carried out on a system for intelligent subtitle editing. The overall aim is to make the use of these tools time- and cost-effective, and therefore sustainable over the kinds of video repositories currently emerging in academia.

As for the educational content, transLectures is exploiting two major European video repositories, VideoLectures.NET, an award-winning collection of videos recorded at various academic events set up by JSI’s Centre for Knowledge Transfer, and poliMedia, a lecture capture system designed and implemented at the Universitat Politècnica de València, UPV. The main languages being targeted in this project are English, Spanish and Slovenian; technologies are also being developed for French and German.

<img src="http://www.opencast.org/wp-content/uploads/2015/07/translectures2.png">
Nicola Cancedda, Principal Scientist and Area Manager, MLDAT Xerox Research Centre Europe
NICOLA CANCEDDA, PRINCIPAL SCIENTIST AND AREA MANAGER, MLDAT XEROX RESEARCH CENTRE EUROPE

*“Data-driven tailoring to the specific style and content of scientific lectures is what makes our solution really useful.”*, Nicola Cancedda, Principal Scientist and Area Manager, MLDAT Xerox Research Centre Europe

## Technologies I: Opencast as a processing framework
In terms of the integration of tools with the Opencast platform, the project is faced with two very different challenges. In the first instance, a communication system between the Opencast platform and the tools has to be developed and implemented to allow automatic captions to be generated for the videos. Then, the best way to implement the editing system has to be found, through which users will be able to correct any errors incurred during the transcription/translation process. The idea here is to incorporate new features typical of subtitle editors into the Opencast Engage Player.

<img src="http://www.opencast.org/wp-content/uploads/2015/07/translectures3-150x150.png">
Digital Project Manager at Knowledge 4 All Foundation Ltd.
DIGITAL PROJECT MANAGER AT KNOWLEDGE 4 ALL FOUNDATION LTD.

*“Combining the transLectures tools into the Opencast suite will prove to be a challenge well worth trying.”*, Digital Project Manager at Knowledge 4 All Foundation Ltd.

In order to allow communication between Opencast and the automatic transcription/translation system, project developers have implemented a workflow operation that will allow the necessary data to be sent from the platform to the transcription system, making use of a specially-designed web service. Figure 1 illustrates the process established for videos added to the Opencast platform using the transLectures workflow:

<img src="http://www.opencast.org/wp-content/uploads/2015/07/translectures4-300x172.png">

The screen shot shows a preliminary mock-up of the features that will be available for transcription/translation of video content:

<img src="http://www.opencast.org/wp-content/uploads/2015/07/translectures5-300x188.png">


## Technologies II: Opencast engage end
The second stage of integration involves adapting the Opencast Engage Player to be able view mono- and multilingual subtitles, as well as to allow editing by users. However, since a new Opencast Engage Player has been under development since November 2012 (http://engagedevcamp.wordpress.com/), and the current version is based on Flash (making modifications harder), alternative players for the implementation of the editing system had to be considered.

Paella Engage Player is a Opencast-compatible player developed at the UPV. It is an HTML5 based multi-stream player that allows multiple audio and video streams to be played simultaneously. Specifically designed for lecture recordings like those found on poliMedia or Opencast, it supports a number of user plug-ins.

For the project, a transLectures plug-in for Paella has been developed that makes it possible to view and edit the subtitles generated for each lecture within the player:

<img src="http://www.opencast.org/wp-content/uploads/2015/07/translectures6-300x78.png">

By doing so, transLectures has effectively paved the way for what will be the successful integration of transLectures tools with Opencast, allowing this platform to offer accurate transcriptions and translations for all videos added by its users – and for those users to contribute back to the quality of automated transcriptions and translations.

## Opencast as OSS
Open source is an important ingredient in ensuring that educational repositories adopt the transcription and translation technology being developed at transLectures – it reduces the cost barrier to entering this domain for many institutions. In addition, open source initiatives, like the Opencast project, foster collaborative efforts to further improve and refine software tools, and make them useful for anyone. This is relevant in particular in research-driven projects like transLectures, where further developments are to be expected.

<img src="http://www.opencast.org/wp-content/uploads/2015/07/translectures7.png">
Jorge Civera Saiz, project manager
JORGE CIVERA SAIZ, PROJECT MANAGER

*“At transLectures, we strongly believe that Opencast will play a key role in rapidly spreading our innovative solutions over many educational repositories in Europe and worldwide, allowing their users to overcome language barriers and reach wider audiences.“*, Jorge Civera Saiz, project manager

Contributions to the Opencast project

transLectures partner UPV will release a set of open source speech recognition tools (transLectures tools) that are fully compatible with Opencast. A module for selectively post-editing transcriptions and translations via a process of intelligent user interaction has been developed and fully integrated in the UPV’s Paella Engage Player for Opencast on May 2nd 2013 (cf. http://www.translectures.eu/tlk/).