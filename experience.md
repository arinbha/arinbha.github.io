---
layout: page
title: Experience
permalink: /experience/
---

<div>
  {% for job in site.data.experience %}
  <section class="experience-card">
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

<!-- Education title -->
<h1 class="section-title">Education</h1>

{% for edu in site.data.education %}
<section class="experience-card">
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

