---
title: Features
description: Opencast offers a rich set of features to support educators, learners, video-operators and administrators.
---
{% include software_menu.html %}

{% include fullsizebox.html
title="Schedule"
description="Opencast has an advanced scheduling system.  You can schedule, decide how to process each recording, and how to publish that recording on a per-event basis.  Want to schedule Tuesday and Thursday from 10 to 11, processing the media to both 720p and 1080p, then distribute to YouTube  You can do that, all in one wizard.  What about restricting access to certain users?  Opencast can do that!  Our scheduling system not only checks for conflicts, but also keeps track of detailed bibliographical data about who, and what, is in a given recording.  The scheduling system can also mark recordings as requiring additional input prior to publication.  This can anything from administrative review, to editing of the media prior to processing.

Our scheduling system...:

- Outputs open standard iCal format
- Supports manual content ingest and automated capture based on schedule
- Allows user configurable capture encoding specifications
- Has per event access control settings
- Can import iCalendar from external scheduling source
- Integrates with open source and proprietary capture hardware"
image="assets/img/large-schedule.jpg"
align="left"
imagewidth="40%"
%}

{% include fullsizebox.html
title="Process"
description="Opencast Process is a workflow-based system that provides a scalable infrastructure for encoding and enriching video with metadata, preview images, brands, captioning and text analysis to make the media more discoverable and accessible.

- Customizable workflow for processing throughout the distribution life cycle
- Default encoding engine based on FFmpeg; other engines can be integrated
- Advanced media analysis, including video OCR that extracts time-synched metadata from slides
- Powerful search capabilities for static, dynamic, and user-generated metadata
- Administrative dashboard for monitoring and management of media life cycle"
image="assets/img/large-process.jpg"
align="right"
backgroundcolor=site.data.colors.box
imagewidth="40%"
%}

{% include fullsizebox.html
title="Distribute"
description="With Opencast Distribute enables you to publish recordings for on-demand viewing or download. Learning tools interoperability (LTI) and RSS/Atom feeds are available for integration with other systems, and publishing to iTunes U and YouTube can be automated.

- Integration with many platforms, including Learning Management Systems via LTI
- Publish as downloadable and/or streamed content
- Local search index using solr available
- Distribution via RSS/Atom to learning management systems
- Automated publishing to iTunes U and YouTube
- Custom workflows to enable distribution and archiving to local or distribution servers"
image="assets/img/large-distribute.jpg"
align="left"
imagewidth="40%"
%}

{% include fullsizebox.html
title="Playback"
description="The Opencast player can be used as a standalone application, or embedded inside other applications like blogs, wikis or content management systems. Opencast Playback enables slide segmentation and in-video text search. All player functionality is fully accessible, supporting assistive technology across multiple platforms.

- Split-screen player for viewing video and slide content simultaneously
- Unlimited number of simultaneous video streams
- Zoom in any video window
- Automatic slide index
- Heat maps indicate sections of content most often watched
- Multiple quality adaptive Streaming support with HTTP Live Streaming (HLS) or MPEG-DASH
- Subtitles
- Support for multiple audio tracks
- REST APIs make it easy to extend to or integrate 
- Easy customization and localization of the player interface
- Customizable permissions settings
- User directory integration (LDAP, CAS etc.)

"image="assets/img/large-playback.jpg"
align="right"
backgroundcolor=site.data.colors.box
imagewidth="40%"
%}

{% include fullsizebox.html
title="Live Streaming"
description="Opencast has robust, and extraordinarily reliable, support for live streaming of your lectures, provided that your capture agents support it.  Live streams can be scheduled in advance, or on the fly.  Active live streams can be extended or shortened as needed.  For example, Harvard DCE live streams hundreds of hours of lectures each month from their 23 Opencast equipped classrooms with essentially no downtime. "
image="assets/img/large-playback.jpg"
align="left"
backgroundcolor=site.data.colors.box
imagewidth="40%"
%}

{% include fullsizebox.html
title="Manage"
description="Opencast Manage provides a dashboard for administrators to configure the system, make bulk edits to content and metadata, track the status and performance of content and configure distribution of video content.

- Metadata entry and editing for related recordings
- Distribution to supported channels (i.e. iTunes, YouTube, RSS, Opencast Playback)
- Manual media upload (e.g. user-generated or production video)
- Bulk editing; media trimming and recording search/filtering
- Monitoring dashboard; status, performance statistics and technical details"
image="assets/img/large-manage.jpg"
align="right"
imagewidth="40%"
%}

{% include fullsizebox.html
title="xAPI/Learning Analytics"
description="In many cases Opencast is used in teaching and learning scenarios. In such environments understanding how the students are interacting with the videos is becoming more and more critical.

- Opencast supports xAPI, the de facto standard in student interactions capture for next generation digital learning systems.
- Thanks to xAPI an Opencast platform can be integrated in a Learning Analytics solution based on Learning Record Store (LRS)
- Using xAPI, detailed data about how students interact with your Opencast videos can be collected in a standardized format. When a student raises volume, skips a video fragment or watches it again can be captured and analyzed.
- Opencast also supports common web analytics like visitor profiles, heatmaps, session recording.  These can be generated adding [Matomo](https://matomo.org/) to your Opencast deployment"
image="assets/img/large-manage.jpg"
align="left"
imagewidth="40%"
%}

{% include fullsizebox.html
title="Cloud"
description="Opencast can be run entirely in a public cloud, with the only on campus equipment being the capture devices in each classroom.

There are many potential benefits to running Opencast in the cloud including:

- Exceptional uptime:  cloud providers are really good at managing all the machines, networking, cooling, redundant backup power, and 24 hour system administrator staffing and support that you would otherwise need to do yourself.
- Flexibility: running in the cloud allows you to scale your cluster up and down as needed.  How much new video will you generate on weekdays during a semester?  On weekends between semesters?  The cloud enables you to run, and only pay for, exactly as many computer resources as you need at any given time.
- Cloud capabilities: public clouds provide services that would be difficult or impossible to implement yourself.  For example, Amazon S3 provides effectively unlimited available storage with a 99.999999999% guarantee that your data will be safe.  Similarly, delivering your Opencast content via a Content Delivery Network enables you to stream video to your users from data centers around the globe.

Opencast includes sophisticated automation tools for running in AWS, Amazon’s cloud.  That tooling provides capabilities including:

- Automatic horizontal scaling of worker nodes: it automatically spins up more worker nodes when there is a lot of processing to be done, and scales back down when the work is complete.

- Automated deployment and management of your cluster: with a single command you can automatically create a new cluster from scratch, rollout a new version of Opencast, or turn off your cluster. "
image="assets/img/large-manage.jpg"
align="right"
imagewidth="40%"
%}

{% include software.html %}
