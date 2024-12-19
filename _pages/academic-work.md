---
layout: single
title: "Academic Work"
permalink: /academic-work/
---

<!-- # Academic Work -->

Explore my academic publications below. Each entry includes an image, a short description of the work, and the full citation.

<div class="publication-list">
  {% for publication in site.data.publications %}
  <div class="publication">
    <br>
    <img src="{{ publication.image }}" alt="{{ publication.title }}" class="publication-image">
    <div class="publication-info">
      <h3>{{ publication.title }}</h3>
      <p>{{ publication.description | markdownify }}</p>
      <p class="citation"><strong>Citation:</strong> {{ publication.citation | markdownify }}</p>
      <a href="{{ publication.url }}" target="_blank" class="publication-link">Full Paper</a>
      {% if publication.github_url and publication.github_url != "" %}
      <br>
      <a href="{{ publication.github_url }}" target="_blank" class="button">GitHub Repository</a>
      {% endif %}
      <br>
    </div>
  </div>
  <hr class="publication-separator">
  {% endfor %}
</div>
