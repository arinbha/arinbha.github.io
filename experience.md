---
layout: page
title: Experience
permalink: /experience/
---

<div>
  {% for job in site.data.experience %}
  <section class="experience-card" id="{{ job.company | slugify }}">
    <div class="experience-header">
      {% if job.logo %}
        <img src="{{ job.logo | relative_url }}" class="company-logo" alt="{{ job.company }} Logo">
      {% endif %}
      <div class="experience-title-group">
        <h3 class="company-name">{{ job.company }}</h3>
        <p class="job-role">{{ job.role }}</p>
        <span class="job-date">{{ job.date }}</span>
      </div>
    </div>
    <div class="experience-details">
      <ul>
        {% for bullet in job.bullets %}
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
    {% for job in site.data.experience %}
      <a href="#{{ job.company | slugify }}" class="ticker-node">
        <div class="ticker-dot"></div>
        <img src="{{ job.logo | relative_url }}" class="ticker-logo" alt="{{ job.company }}">
      </a>
    {% endfor %}
  </div>
</div>