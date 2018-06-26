---
title: Friedrich-Alexander-University Erlangen-Nuremberg
date: 2015-05-01
description: The Friedrich-Alexander-University Erlangen-Nuremberg is one of Germanys largest universities and has a long tradition in lecture recordings. 
category: user
tags: [user]
logo: /assets/img/fau-logo.png
---

Friedrich-Alexander-Universität Erlangen-Nürnberg (FAU) [1] is a strong research university and one of the largest universities in Germany, with more than 40,000 students, 244 degree programmes, 4,000 academic staff (including over 580 professors), 180 million euros third-party funding (as of 2014), and 500 partnerships with universities
all over the world.

The Multimedia Department at RRZE (the University IT service provider) has a long history of using professional lecture capture technology, and the first lecture capture video was published in 2002 [2]. In 2009, RRZE announced the launch of an online web video platform [3] as the official publication channel for all University video material. Today the department has one manager, four employees for capture and editing, two employees for team and management administration, one developer, and five to six student assistants every semester. The video portal hosts more than 18,000 educational resources online.
<img src="http://www.opencast.org/wp-content/uploads/2015/12/pic_1.jpg">

## Why did you decide to use Opencast?
<img src="http://www.opencast.org/wp-content/uploads/2015/12/pic_3.png">

FAU’s IT service provider, RRZE, showed great interest from the first steps of Opencast software starting with version 0.5. The need to extend the current infrastructure was clear, while the option of reducing the workload of the staff needed for capture, editing and publishing was really tempting. There were four main reasons for testing and finally choosing the Opencast software:

- Cost = Open source project, therefore no license costs.
- Scalability = Opencast offered the ability to fit to our plans.
- Community = Supported by large universities and individuals all over the world.
- Adoptability = Use of open standards (e.g. REST API)

## Use case: Creating video files to fit our needs.
We decided to keep our video portal as a publication channel and use Opencast servers for video transcoding. We achieved a level of integration in our daily department workflow by using Opencast servers to generate certain video files for the video portal, fau.tv. The standards for almost 97 percent of our recordings are:

- One audio file
- Three camera files with different resolutions, 320×180, 640×360 and 1280x720p (with an FAU logo watermark)
- One combined file for camera and computer signal (picture 1)
- Same quality and encodings, such as the files being processed by professional video editing software (FinalCut Pro)
- Intro-outro videos for all video-audio formats Picture 1

<img src="http://www.opencast.org/wp-content/uploads/2015/12/pic_4.jpg">
Picture 1
Video portal default combined layout. Post editing with Adobe Photoshop and Finalcut Pro

Using Opencast 2.0.1 we combine two video streams (camera + presentation) into one (picture 2, steps 1 and 2). Next Opencast renders the background image using a cover image (picture 2, step 3). In the final step we render Opencast metadata (title, presenters) in the bottom left box and also add our logo to the camera file. All files use the new Opencast 2.0.1 themes feature for intro-outro video. To create this kind of layout with professional editing software our team needs 30 minutes to 1 hour. With Opencast,
the total workload per person for a recording, after the capturing, dropped to 2 minutes for trimming the recording in the Opencast video editor.
Videos are published in our video portal admin area using the Opencast REST API, without the need for Opencast GUI interaction.

This winter semester 2015/2016, a clip [4] was produced exclusively by Opencast 2.0.1 and captured with Galicaster 1.4.1. The combined video file used dynamic Opencast metadata rendering.

<img src="http://www.opencast.org/wp-content/uploads/2015/12/pic_5.png">

##  Hardware-software description
Opencast Ubuntu 14.04 server nodes (October 2015)

- 1 x Opencast 2.0.1 admin node (2 cores, 4 GB RAM)
- 2 x Opencast 2.0.1 worker nodes (8 cores, 8 GB RAM)
- 1 x Opencast 2.0.1 engage node (2 cores, 4 GB RAM)
- 1 x Mysql database
- Shared NAS

+ Nagios and munin monitoring

Capture agents
5 Galicaster CA1.4.1 (with Ubuntu 12.04) and 4 NCast PR-720M

Depending on the layout of the room, we have different capture agents set up with a mix of automatic and scheduled recordings.

In the current semester we are capturing and processing 44 lectures per week. 33 percent of them use Opencast. This translates to around 24 to 28 hours per week.

## Future plans
- Deploy Opencast 2.1
- Improve processing times (current workflow for a 1h 30m lecture video, camera and computer signal takes around 6 hours to complete)
- Implement an automated capture process
- Improve video quality
- Increase the number of capture agents

## Contact information
Stefanos Georgopoulos, RRZE Multimedia and E-learning
(stefanos.georgopoulos@fau.de, +49 9131 8520190)

Michael Gräve, RRZE Multimedia and E-learning
(michael.graeve@fau.de, +49 9131 8528898, 8529953 )

## References
[1] http://fau.de
[2] http://www.video.uni-erlangen.de/clip/id/231
[3] http://www.fau.tv
[4] http://www.video.uni-erlangen.de/clip/id/5528.html
