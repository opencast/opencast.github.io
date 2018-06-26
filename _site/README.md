Opencast is a flexible and customizable video capture and distribution system for modern institutions. Opencast is built by a growing community of developers in collaboration with leading universities and organizations worldwide.

{% include software.html %}


# Introduction 

{% include videoplayer.html id="57a2b005-fe70-4566-a234-aa864faf1e29" %}

---

# News

{% for post in site.posts limit:5 %}
## [{{ post.title }}]({{ post.url }})
  _{{ post.date | date_to_long_string }}_ 
  {{ post.description }}
  [Read more...]({{ post.url }})
  
---

{% endfor %}

# Features

{% include fullsizebox.html 
title="Schedule"
description="Schedule events to automatically record based on a pre-defined timetable and, capture both video of the presenter and the  PC screen."
image="/assets/img/schedule.png"
linkurl="/software"
align="left"
backgroundcolor=site.data.colors.box
%}

{% include fullsizebox.html 
title="Edit"
description="Bulk edit and trim video recordings. The editor provides graphical visualization of elements such as audio can significantly reduce editing time."
image="/assets/img/edit.png"
linkurl="/software"
align="right"
%}

{% include fullsizebox.html 
title="Process"
description="A scalable infrastructure to encode video, generate metadata and preview images, create captioning and bulk edit to support video processing at scale."
image="/assets/img/events.png"
linkurl="/software"
align="left"
backgroundcolor=site.data.colors.box
%}

{% include fullsizebox.html 
title="Distribute"
description="Publish recordings for download or on-demand viewing via YouTube, RSS, Atom-feeds or with OAI-PMH."
image="/assets/img/distribute.png"
linkurl="/software"
align="right"
%}

{% include fullsizebox.html 
title="Playback"
description="The media player is a standalone application or embedded on blogs, wikis or a content management system."
image="/assets/img/playback.png"
linkurl="/software"
align="left"
backgroundcolor=site.data.colors.box
%}

{% include fullsizebox.html 
title="Manage"
description="A robust dashboard to manage, configure and track the status and performance of video content and distribution channels."
image="/assets/img/manage.png"
linkurl="/software"
align="right"
%}

---

# Trusted by a Collection of Innovative Organizations
[<img class="center-image" src="/assets/img/opencast-homepage-logos-rev2.png">](/users)

