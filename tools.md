---
title: Tools for Opencast
description: The Opencast community offers several tools, mostly open source, that work together with Opencast to increase the functionality. These tools can improve the capture, offer a export or integration into other systems, can give you a choice of different players and much more.
---
{% include marketplace_menu.html %}

# Lecturer Tracking

{% include fullsizebox.html 
title="LectureSight"
description="LectureSight is a free and open-source tracking tool that allows to steer a pan-tilt camera based on data gathered by a separate webcam. The aim of this project is to offer a more vivid video of the lecture and show more details of what is going on in the classroom. This will enable an automated recording of a lecture that uses the blackboard, i.e.

[LectureSight Homepage](https://opencast.jira.com/wiki/spaces/LECTURESIGHT/overview)"
image="/assets/img/ls-running.png"
linkurl="https://opencast.jira.com/wiki/spaces/LECTURESIGHT/overview"
align="left"
imagewidth="50%"
%}

{% include fullsizebox.html 
title="Track4K"
description="Modern cameras can capture up to 4K resultion. This offers more detail than most current displays can show. Track4K analyses the high-res video and crops videos based on the actions within the video. There is also an interactive mode for the Paella player that automatically zooms in but allows the user to change the viewing area manually.

[Track4K Homepage](http://track4k.co.za/index.html)"
image="/assets/img/track4k.jpg"
linkurl="http://track4k.co.za/index.html"
align="left"
imagewidth="50%"
backgroundcolor=site.data.colors.box
%}

---

# Recording

{% include fullsizebox.html 
title="Galicaster"
description="Galicaster, from Teltek, is currently the most popular capture software that works together with Opencast. Additional to recording devices with the Galicaster software that can be purchased from Teltek, this software under a non-commercial open-source licence that allows universities to use the software for free on their computers.

[Galicaster Homepage](https://wiki.teltek.es/display/Galicaster/Galicaster+project+Home)"
image="/assets/img/galicaster-ui.png"
linkurl="https://wiki.teltek.es/display/Galicaster/Galicaster+project+Home"
align="left"
imagewidth="50%"
%}

{% include fullsizebox.html 
title="PyCA"
description="PyCA is a fully functional Opencast capture agent written in Python. It is free software, licensed under the terms of the GNU Lesser General Public License.

PyCA can be run on almost any kind of devices: A regular PC equipped with capture cards, a server to capture network streams, small boards or embedded devices like Raspberry Pi, Beagleboard, …

[PyCA on Github](https://github.com/opencast/pyCA)"
image="/assets/img/Screenshot-from-2017-03-13-17-43-53.png"
linkurl="https://github.com/opencast/pyCA"
align="left"
imagewidth="50%"
backgroundcolor=site.data.colors.box
%}

{% include fullsizebox.html 
title="TheRec"
description="TheRec is a free and open-source recording software for Windows 7+. Currently TheRec does not offer all features that a regular capture agent provides, as it does not support scheduling and uploading from Opencast. For an automated upload it relies on MHRI. Unlike other recording tools TheRec is easy to install and to configure. It supports a wide variety of capture cards that are compatible with Microsoft DirectShow. The number of simultanous streams that can be recorded is only limited by the speed of the computer.

[TheRec Homepage](https://elan-ev.de/produkte_av_therec_english.php)"
image="/assets/img/therec.png"
linkurl="https://elan-ev.de/produkte_av_therec_english.php"
align="left"
imagewidth="50%"
%}

---

# Monitoring

{% include fullsizebox.html 
title="Galicaster Dashboard"
description="The Galicaster Dashboard is designed to monitor Capture Agents, especially Galicaster Capture Agents. The Tool gives you an overview of your recording devices, with their current status and a preview of the signals that the agent is currently recording.

[Galicaster Dashboard Homepage](https://wiki.teltek.es/display/Galicaster/Galicaster+Dashboard)"
image="/assets/img/gc-dashboard.png"
linkurl="https://wiki.teltek.es/display/Galicaster/Galicaster+Dashboard"
align="left"
imagewidth="50%"
backgroundcolor=site.data.colors.box
%}

---

# Player

{% include fullsizebox.html 
title="Paella Player"
description="The Paella Player is a free and open-source alternative player for Opencast. It is an alternative to the player included within Opencast and offers an appealing design and some unique features like virtual trimming. It is using HTML5 video with a fallback to Flash. The Paella Player can also be embedded into edX.

### Now included in Opencast 5

[Paella Player Homepage](http://paellaplayer.upv.es/)"
image="/assets/img/paellaplayer.png"
linkurl="https://wiki.teltek.es/display/Galicaster/Galicaster+Dashboard"
align="left"
backgroundcolor=site.data.colors.greenbox
imagewidth="50%"
%}

{% include fullsizebox.html 
title="Annotating Academic Video Tool"
description="Annotating Academic Video is a free and open-source annotation tool. The aim of this software is provide teacher and learners with an easy to use tool to annotate videos.

[Annotating Academic Video Tool Homepage](https://bitbucket.org/opencast-community/annotation-tool)"
image="/assets/img/annotationtool.png"
linkurl="https://bitbucket.org/opencast-community/annotation-tool"
align="left"
imagewidth="50%"
backgroundcolor=site.data.colors.box
%}

---

# Security

{% include fullsizebox.html 
title="Opencast Stream Security Plugins"
description="Opencast supports URL signing to provide additional protection of resources against unauthorised access. While the Opencast core provides both facilities to sign URLs and verify signed URLs, additional efforts are required in setups that take advantage of dedicated download and/or streaming servers. Such dedicated distribution servers need to be capable to at least verify signed URLs to offer the same level of protection for distribution artefacts they are providing access to.

Currently, there are two Opencast Stream Security plugins available:

- [Apache HTTP Stream Security Plugin](https://bitbucket.org/opencast-community/apache-httpd-stream-security-plugin)
- [Wowza Stream Security Plugin](https://bitbucket.org/opencast-community/wowza-stream-security-plugin/src)"
image="/assets/img/login-1203603_960_720.png"
linkurl="https://bitbucket.org/opencast-community/apache-httpd-stream-security-plugin"
align="left"
imagewidth="50%"
%}
