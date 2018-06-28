---
title: News
description: Opencast related news
---

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url | remove_first:'/' }})
  _{{ post.date | date_to_long_string }}_
  {{ post.description }}
  [Read more...]({{ post.url | remove_first:'/' }})

---

{% endfor %}
