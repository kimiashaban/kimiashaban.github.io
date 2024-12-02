---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
author.googlescholar: true
---


You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>


{% for post in site.publications %}
  {% include archive-single.html %}
{% endfor %}

