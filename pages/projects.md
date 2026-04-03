---
layout: archive
title: Projects
permalink: /projects/
---

<h2>All Projects</h2>

{% assign sorted_projects = site.projects | sort: 'date' | reverse %}
{% for project in sorted_projects %}
  {% include project-card.html project=project %}
{% endfor %}