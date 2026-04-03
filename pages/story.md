---
layout: archive
title: My Story
permalink: /story/
---

<h2>My Story Chapters</h2>

{% assign sorted_story = site.story | sort: 'sequence' %}
{% for chapter in sorted_story %}
  {% include story-card.html chapter=chapter %}
{% endfor %}