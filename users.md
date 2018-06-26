---
title: "Opencast Users"
description: "As an open-source project, it is hard to tell how many institutions are using Opencast. The software does not have to be licensed and the users do not need to register.But from registrations to the repositories we can say that at over 300 different institutions worldwide have downloaded Opencast. In this area we want to highlight some of the institutions that use Opencast in production."
---
{% include community_menu.html %}

# Institutions that use Opencast
Some adopters of Opencast were able to provide some feedback on how they use Opencast and what they have contributed back to the project.

{% include box-start.html backgroundcolor="#dfe6ed" %}

{% for post in site.posts %}
{% if post.categories contains "user" %}
{% include imagebox.html 
title=post.title
description=post.description
image=post.logo
linkurl=post.url
linktext="Learn More"
%}
{% endif %}
{% endfor %}

{% include box-end.html %}

---

> Opencast was the only solution that was fully automated and flexible enough to work with our existing audiovisual technology.

Stuart Phillipson, University of Manchester

---

> Opencast drastically reduces the time it takes to get educational resources online so end users can interact with content in real-time.

Rüdiger Rolf, University of Osnabrück
