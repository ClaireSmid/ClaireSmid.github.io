---
layout: single
title: "Talks & Courses"
permalink: /talks-and-courses/
---

<!-- # Talks & Courses -->

Below is a list of my recent talks and courses. Each entry includes links to related materials (repositories, slides, or documents) and highlights key takeaways.

<div class="talks-and-courses-list">
  {% for item in site.data.talks_and_courses %}
  <div class="talk-or-course">
    <h3>{{ item.title }}</h3>
    <p><strong>Type:</strong> {{ item.type }}</p>
    <p>{{ item.description }}</p>
    {% if item.image %}
    <img src="{{ item.image }}" alt="{{ item.title }}" class="talk-image">
    {% endif %}
    <div class="links">
      {% if item.github_url and item.github_url != "" %}
      <br>
      <a href="{{ item.github_url }}" target="_blank" class="button">GitHub Repository</a>
      {% endif %}
      {% if item.slides_url and item.slides_url != "" %}
      <br>
      <a href="{{ item.slides_url }}" target="_blank" class="button">Slides</a>
      {% endif %}
      {% if item.doc_url and item.doc_url != "" %}
      <br>
      <a href="{{ item.doc_url }}" target="_blank" class="button">Document</a>
      {% endif %}
    </div>
  </div>
  <hr class="talk-separator">
  {% endfor %}
</div>