---
title: Friedrich-Alexander-University Erlangen-Nürnberg
date: 2018-09-19
description: The Friedrich-Alexander-University Erlangen-Nürnberg is one of Germanys largest universities and has a long tradition in lecture recordings.
category: user
tags: [user]
logo: assets/img/fau-logo.png
---

Friedrich-Alexander-Universität Erlangen-Nürnberg (FAU) [1] is a strong research university and one of the largest universities in Germany, with 39,780 students, 265 degree programmes, 4,000 academic staff (including over 579 professors), 199.64 million euros third-party funding, and 500 partnerships with universities
all over the world.

The Multimedia Department at RRZE (the University IT service provider) has a long history of using professional lecture capture technology, and the first lecture capture video was published in 2002 [2]. In 2009, RRZE announced the launch of an online web video platform [3] as the official publication channel for all University video material. Today the department has one manager, four employees for capture and editing, two employees for team and management administration, one developer, and five to six student assistants every semester. The video portal hosts more than 30,000 educational resources online.

![Video editing room](assets/img/2018-09-19-friedrich-alexander-university-erlangen-nuremberg/video-editting.png)

## Why did you decide to use Opencast?

FAU’s IT service provider, RRZE, showed great interest from the first steps of Opencast software starting with version 0.5. The need to extend the current infrastructure was clear, while the option of reducing the workload of the staff needed for capture, editing and publishing was really tempting. There were four main reasons for testing and finally choosing the Opencast software:

- Cost = Open source project, therefore no license costs.
- Scalability = Opencast offered the ability to fit to our plans.
- Community = Supported by large universities and individuals all over the world.
- Adoptability = Use of open standards (e.g. REST API)

## Use case: Creating video files to fit our needs.
We decided to keep our video portal as a publication channel and use Opencast servers for video transcoding. We achieved a level of integration in our daily department workflow by using Opencast servers to generate certain video files for the video portal, fau.tv. The standards for almost 97 percent of our recordings are:

- One audio file
- Three camera files with different resolutions, 640×360, 1280x720p and 1920x1080p (with an FAU logo watermark)
- Two combined files with different resolutions 1280x720p and 1920x1080p, for camera and computer signal (picture 1)
- Same quality and encodings, such as the files being processed by professional video editing software (FinalCut Pro)
- Intro-outro videos for all video-audio formats Picture 1

![Video portal default combined layout](assets/img/2018-09-19-friedrich-alexander-university-erlangen-nuremberg/default-combined-layout.png)
Picture 1
Video portal default combined layout. Post editing with Adobe Photoshop and Finalcut Pro

Using Opencast 3.5 we combine two video streams (camera + presentation) into one (picture 2, steps 1 and 2). Next Opencast renders the background image using a cover image (picture 2, step 3). In the final step we render Opencast metadata (title, presenters) in the bottom left box and also add our logo to the camera file. All files use the new Opencast 3.5 themes feature for intro-outro video. To create this kind of layout with professional editing software our team needs 30 minutes to 1 hour. With Opencast,
the total workload per person for a recording, after the capturing, dropped to 2 minutes for trimming the recording in the Opencast video editor.
Videos are published in our video portal admin area using the Opencast REST API, without the need for Opencast GUI interaction.

This summer semester 2018, a clip [4] was produced exclusively by Opencast 3.5 and captured with Galicaster 2.1. The combined video file used dynamic Opencast metadata rendering.

![Depiction of the watermarking process](assets/img/2018-09-19-friedrich-alexander-university-erlangen-nuremberg/watermark-process.png)

##  Hardware-software description
Opencast Ubuntu 16.04 server nodes (September 2018)

- 1 x Opencast 3.5 admin node (4 cores, 8 GB RAM)
- 1 x Opencast 3.5 worker node (32 cores, 64 GB RAM)
- 2 x Opencast 3.5 worker nodes (8 cores, 8 GB RAM)
- 1 x Opencast 3.5 engage node (2 cores, 4 GB RAM)
- 1 x Mysql database
- Shared NAS

+ Nagios and munin monitoring

Capture agents:
14 Galicaster CA 2.1 (with Ubuntu 16.04)

Depending on the layout of the room, we have different capture agents set up with a mix of automatic and scheduled recordings.

In the current semester we are capturing and processing ~22 lectures per week. 55 percent of them use Opencast. This translates to around 38 to 42 hours per week.

## Future plans
- Deploy Opencast 5.x
- Improve processing times (current workflow for a 1h 30m lecture video, camera and computer signal takes around 6 hours to complete)
- Implement an automated capture process
- Improve video quality
- Increase the number of capture agents

## Contact information
Stefanos Georgopoulos, RRZE Multimedia and E-learning
(stefanos.georgopoulos@fau.de, +49 9131 8520190)

Michael Gräve, RRZE Multimedia and E-learning
(michael.graeve@fau.de, +49 9131 8528898, 8529953)

## References

1. <https://fau.de>
2. <https://www.video.uni-erlangen.de/clip/id/231>
3. <https://fau.tv>
4. <https://www.video.uni-erlangen.de/clip/id/9432.html>
