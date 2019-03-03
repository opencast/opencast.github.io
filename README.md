---
redirect_from: "/matterhorn"
---

Opencast is a flexible, scalable and reliable video capture, distribution, and management system for academic institutions. Opencast is built by a growing community of developers in collaboration with leading universities and organizations worldwide.

{% include software.html %}

---

# Introduction

{% include videoplayer.html id="57a2b005-fe70-4566-a234-aa864faf1e29" %}

---

# News

{% for post in site.posts limit:5 %}
## [{{ post.title }}]({{ post.url | remove_first:'/' }})
  _{{ post.date | date_to_long_string }}_
  {{ post.description }}
  [Read more...]({{ post.url | remove_first:'/' }})

---

{% endfor %}

[News Archive...](news)


---

# Features

{% include fullsizebox.html
title="Schedule"
description="Schedule events to automatically record based on a pre-defined timetable and capture both video(s) of the presenter and the  computer signal."
image="assets/img/schedule.png"
linkurl="software"
align="left"
backgroundcolor=site.data.colors.box
%}

{% include fullsizebox.html
title="Edit"
description="Bulk edit and trim video recordings. The UI provides graphical visualization of standard edits and can therefore significantly reduce editing time."
image="assets/img/edit.png"
linkurl="software"
align="right"
%}

{% include fullsizebox.html
title="Process"
description="A scalable infrastructure to encode video, generate metadata and preview images, create captioning and bulk edit to support video processing at scale."
image="assets/img/events.png"
linkurl="software"
align="left"
backgroundcolor=site.data.colors.box
%}

{% include fullsizebox.html
title="Distribute"
description="Publish recordings for download or on-demand viewing via YouTube, RSS, Atom-feeds or with OAI-PMH."
image="assets/img/distribute.png"
linkurl="software"
align="right"
%}

{% include fullsizebox.html
title="Playback"
description="The media player is a standalone application or embedded on blogs, wikis or a content management system."
image="assets/img/playback.png"
linkurl="software"
align="left"
backgroundcolor=site.data.colors.box
%}

{% include fullsizebox.html
title="Manage"
description="A robust dashboard to manage, configure and track the status and performance of video content and distribution channels."
image="assets/img/manage.png"
linkurl="software"
align="right"
%}

---

<i class="fas fa-at" style="float: right; margin-left: 2rem; margin-top: 2rem; display: inline-block; font-size: 5rem; color: {{ site.data.colors.header-blue }}"></i>

# Get Involved

Opencast has an active, helpful and engaging community. [Here you can find information on how to get in contact with us](communication).

---

# Trusted by a Collection of Innovative Organizations including these 6 Institutions
[<img class="center-image" src="assets/img/opencast-homepage-logos-rev2.png">](users)

