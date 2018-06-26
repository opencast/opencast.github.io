---
title: ETH Zürich
date: 2015-05-01
description: The ETH Zürich has always been one of the driving forces of the Opencast project. A high degree on integration into their campus infrastructure is important to them.
category: user
tags: [user]
logo: /assets/img/eth-logo.png
---

## Using Opencast as a video asset management system to your CMS – introducing OAI-PMH

### Summary
ETH Zürich is using Opencast to support the local content management system (Adobe Experience Manager, a.k.a. CQ5) in video management and distribution. Metadata from Opencast is being harvested by the CMS, with CQ5 subsequently using the media package information to allocate video assets (including search functionalities) and present media using the JW Player. A variety of formats and resolutions is being used to serve video to different devices, browsers and OS, primarily as HTML5 video, with Flash as fallback; different resolutions are being called upon in different scenarios (embed, full screen, manual selection).

### Background
Plans to introduce Opencast as a lecture capture system at ETH Zürich overlapped with the launch of a new CMS late in 2013. Adobe’s CQ5 was selected as a successor to our outdated CMS; however, the appendant DAM was not implemented. Video asset management was instead delegated to Opencast in order to benefit from an existing infrastructure and expertise in video distribution.

### OAI-PMH
The main issue therefore was a connection between Opencast and CQ5 and this is where OAI-PMH came in handy: The Open Archives Initiative Protocol for Metadata Harvesting was created to consolidate metadata from different (library) repositories, thus providing the user with consistent search results across these. ETH had originally implemented OAI-PMH to Opencast in order to aggregate different video repositories as part of an unfinished project for a federated collection of academic video. Instead, OAI-PMH became the “missing link” between Opencast and CQ5, with the former being harvested by the latter for metadata describing video assets in Opencast. Within Opencast, the videos destined to be published in CQ5 have their own workflow “OAI-PMH CQ5” which results in the said harvesting interface being served. As a matter of fact, full media packages are being harvested, with distribution media (media files) being replaced by respective links to the Opencast distribution infrastructure. A handler was crafted in CQ5 to use information contained to display video as assets, including a short description and a preview image:

￼<img src="http://www.opencast.org/wp-content/uploads/2015/07/eth1-300x149.png">


### Video distribution
Once the user has pulled a video asset into his page, the embedded video is displayed using JW Player. Behind the scenes, a format schedule was established to allow for flexible video distribution: Depending on device, browser and operating system, the appropriate format is being used to display the video. As we speak, this means we have H.264 for most setups, WebM to support older versions of Firefox – and H.264 Flash for those awkward moments where HTML5 video is not supported, which affects older IE versions and Windows XP mainly.

HLS is not supported yet; for this, a manifest is needed to correctly chop and deliver the video. A workflow operation to enable this in Opencast is planned, however, for one of the next releases. Additionally, we switch between two resolutions according to video layout in CQ5: Embedded video uses the respective smaller version, with an “continuous play” switch to the larger resolution in full screen display. The standard would be

- SD: 640×480 (embed), 1024×768 (fullscreen)
- HD: 640×360 (embed), 1280×720(fullscreen)

Where applicable, users can manually switch to 1080p in fullscreen, thus getting even better video quality (example). The full matrix reads like this:

￼<img src="http://www.opencast.org/wp-content/uploads/2015/07/eth2-300x91.png">

We have a HTTP Apache server for HTML5 videos (webm with vp8 and mp4 with h.264) plus Wowza Streaming Engine 4.0 server for RTMP (mp4 with h.264) distribution. The virtual servers runs on a VMware vSphere.

### Video encoding – FFmpeg settings
In order to establish the best possible settings in FFmpeg for our content, we contracted an FFmpeg expert to elaborate these based on typical content we have (content only recordings with little fluctuation, mixed recordings video/content, video only, single stream). Against the background of our distribution infrastructure including the CMS, he thus set up a plethora of encoding workflows, the details of which you find in the wiki. One major characteristic of the process we’re using is “two pass encoding”: In this, the first pass analyses the video file and the second one encodes the video into the target resolution according to the characteristics established in the first pass. Time-consuming, yes, but for a better video quality and an agreeable user experience, we decided in favour of quality over time. Mind you, we can use “quick and dirty” workflows once we need a quick publication.

### Problems encountered – and remaining
We had a number of minor issues in the early stages when ongoing work in both systems (CQ5 and Opencast) caused interferences, OAI-PMH updates failing, publications not working in due time, some Opencast workflows resulted in too many HD options being displayed. All of these we were able to solve and with hindsight, we consider them labour pains. There is an “issue” with the continuous or seamless play when switching to and from fullscreen – it’s not that seamless. You actually get to see first frame of the video for a short moment, which was awkward at first because with most videos/players one is used to seeing “nothing”, a black screen actually. This is done by adding a black frame to the video, something we didn’t want to, so ours is a “real” first frame.

### Future scenarios for OAI-PMH
There are two additional scenarios we envisage using OAI-PMH. One is for our videos to obtain a digital object identifier (DOI). The official server to provide these at ETH also communicates using OAI-PMH and we hope to connect the two for that purpose. Also, we would like to establish an aggregated Opencast repository at some stage, with participating institutions using OAI-PMH to push metadata from their open video resources to a central video portal, which merely has to read OAI-PMH and display videos coming from institutions across the globe.


