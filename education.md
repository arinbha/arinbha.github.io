---
layout: page
title: Education
permalink: /education/
---
<div>
{% for edu in site.data.education %}
<section class="experience-card" id="{{ edu.school | slugify }}">
  <div class="experience-header">
        {% if edu.logo %}
        <img src="{{ edu.logo | relative_url }}" class="company-logo" alt="{{ edu.school }} Logo">
      {% endif %}
    <div class="experience-title-group">
      <h3 class="company-name">{{ edu.school }}</h3>
      <p class="job-role">{{ edu.degree }}</p>
      <span class="job-date">{{ edu.date }}</span>
    </div>
  </div>

  <div class="experience-details">
    <ul>
      {% for bullet in edu.bullets %}
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
    {% for edu in site.data.education %}
      <a href="#{{ edu.school | slugify }}" class="ticker-node">
        <div class="ticker-dot"></div>
        <img src="{{ edu.logo | relative_url }}" class="ticker-logo" alt="{{ edu.school }}">
      </a>
    {% endfor %}
  </div>
</div>
