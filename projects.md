---
layout: page
title: Projects
permalink: /projects/
---

<div>
  {% for project in site.data.projects %}
  <section class="experience-card" id="{{ project.name | slugify }}">
    <div class="experience-header">
      {% if project.logo %}
        <img src="{{ project.logo | relative_url }}" class="company-logo" alt="{{ project.name }} Logo">
      {% endif %}
      <div class="experience-title-group">
        <h3 class="company-name">{{ project.name }}</h3>
      </div>
    </div>
    <div class="experience-details">
      <ul>
        {% for bullet in project.bullets %}
          <li>{{ bullet }}</li>
        {% endfor %}
      </ul>
    </div>
  </section>
  {% endfor %}
</div>

<div class="ticker-nav-container" id="ticker-container">
  <div class="ticker-line"></div>
  <div class="ticker-content">
    {% for project in site.data.projects %}
      <a href="#{{ project.name | slugify }}" class="ticker-node">
        <div class="ticker-dot"></div>
        <img src="{{ project.logo | relative_url }}" class="ticker-logo" alt="{{ project.name }}">
      </a>
    {% endfor %}
  </div>
</div>
