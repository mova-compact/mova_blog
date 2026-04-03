---
layout: home
title: Home
---

<div class="intro-block">
  <h1>Welcome to My Publishing Hub</h1>
  <p>I am [Your Name], working on AI, agent systems, workflow architecture, and digital products. This site serves as my knowledge hub and public showcase.</p>
</div>

<div class="navigation-block">
  <h2>Explore</h2>
  <ul>
    <li><a href="/articles/">Articles & Publications</a></li>
    <li><a href="/story/">My Story</a></li>
    <li><a href="/projects/">Projects</a></li>
    <li><a href="/about/">About</a></li>
  </ul>
</div>

<div class="mova-block">
  <h2>MOVA Ecosystem</h2>
  <p>The starting point of my work in [describe MOVA briefly].</p>
  <a href="/projects/mova/">Learn more about MOVA</a>
</div>

<div class="story-block">
  <h2>My Journey</h2>
  {% assign featured_story = site.story | where: "featured", true | first %}
  {% if featured_story %}
    <article class="story-card">
      <h3><a href="{{ featured_story.url }}">{{ featured_story.title }}</a></h3>
      <p>{{ featured_story.summary }}</p>
    </article>
  {% endif %}
  <a href="/story/">Read my story</a>
</div>

<div class="projects-block">
  <h2>Featured Projects</h2>
  {% assign featured_projects = site.projects | where: "featured", true | limit: 3 %}
  {% for project in featured_projects %}
    <article class="project-card">
      <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
      <p>{{ project.summary }}</p>
    </article>
  {% endfor %}
  <a href="/projects/">View all projects</a>
</div>

<div class="recent-posts">
  <h2>Recent Publications</h2>
  {% assign recent_posts = site.posts | limit: 5 %}
  {% for post in recent_posts %}
    <article class="post-card">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt }}</p>
      <time>{{ post.date | date: "%B %d, %Y" }}</time>
    </article>
  {% endfor %}
  <a href="/articles/">View all articles</a>
</div>