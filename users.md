---
title: "Opencast Users"
description: "As an open-source project, it is hard to tell how many institutions are using Opencast. The software does not have to be licensed and the users do not need to register.But from registrations to the repositories we can say that hundreds of different institutions worldwide have downloaded Opencast. Here, we would like to highlight some of the institutions that use Opencast in production."
---
{% include community_menu.html %}

# Opencast success stories
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

# Opencast adopters
These are some of the institutions using Opencast. <a href="mailto:schulte@id.ethz.ch">Drop us a line</a> if you want to know more about any of these. A <a href="https://map.opencast.org/">map</a> of registered users to our repository is also available

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## Europe

-	Arnes Slovenia, Slovenia
-	Beuth Hochschule Berlin, Germany
-	ETH Zürich, Switzerland
-	FAU Erlangen-Nürnberg, Germany
-	FH Potsdam, Germany
-	Fresenius Hochschule, Germany
-	HAWK Hildesheim, Germany
-	Hochschule für Technik Stuttgart, Germany
-	Hochschule Hannover, Germany
-	Hochschule Osnabrück, Germany
-	Hochschule Wismar, Germany
-	Keele University, UK
-	KIT Karlsruhe, Germany
-	KU Leuven, Belgium
-	Leibniz Supercomputing Centre, Garching, Germany
-	Martin-Luther-Universität Halle-Wittenberg, Germany
-	RTH Köln, Germany
-	RTWH Aachen, Germany
-	Ruhr-Uni Bochum, Germany
-	Ssystems Berlin, Germany
-	SWITCH, Switzerland
-	Tierärtzliche Hochschule Hannover, Germany
-	TU Braunschweig, Germany
-	TU Clausthal, Germany
-	TU Graz, Austria
-	TU Illmenau, Germany
-	TU Wien, Austria
-	Universidad Católica de Murcia, Spain
-	Universidad de Murcia, Spain
-	Universidad Pablo de Olavide (Sevilla), Spain
- Universidad Técnica Federico Santa María, Chile
-	Universität Bremen, Germany
-	Universität Duisburg-Essen (in Vorbereitung), Germany
-	Universität Erfurt, Germany
-	Universität Für Bodenkultur Wien, Austria
-	Universität Hamburg, Germany
- Universiteit Hasselt, Belgium
-	Universität Leipzig, Germany
-	Universität Münster, Germany
-	Universität Oldenburg, Germany
-	Universität Osnabrück, Germany
-	Universitat Politecnica de Valencia, Spain
-	Universität Regensburg, Germany
-	Universität Stuttgart, Germany
-	Universität Ulm, Germany
-	Universität Vechta, Germany
-	Universität Wien, Austria
-	Universität zu Köln, Germany
-	University of Bergen, Norway
-	University of Gent, Belgium
-	University of Granada, Spain
-	University of Helsinki, Finland
-	University of Jaen, Spain
-	University of La Coruña, Spain
-	University of Lubiana, Slovenia
-	University of Manchester, UK
-	University of Sussex, UK
-	University of the Arts London, UK
-	University of Vigo, Spain

" %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## Rest of the world

- Bagley College of Engineering, USA
- University of Cape Town, South Africa
- Harvard DCE, USA
- North-West University, South Africa
- Rochester IT, USA
- Universidad Continental de Perú, Perú
- University of New Mexico, USA
- University of Ottawa, Canada
- University of the South Pacific, Fiji
- University of Toronto Dentistry, Canada


"%}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## Registered Users

<iframe src='https://map.opencast.org' width='800' height='450' frameborder='0' style='border:0' allowfullscreen></iframe>
"%}
