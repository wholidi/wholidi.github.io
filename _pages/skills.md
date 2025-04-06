---
layout: page
title: For Humanity Certified Auditor
permalink: /skills/
description: Certified skills and competencies
nav: true
nav_order: 5
---

<!-- <h1> Skills Overview</h1> -->
<!--
<div class="row row-cols-1 row-cols-md-2 g-4">
  {% assign skills = site.skills | sort: "importance" %}
  {% for skill in skills %}
    {% include skills.liquid skill=skill %}
  {% endfor %}
</div>
-->

<!-- View Certificates Button -->
<a href="/AI_Audit/" style="display:inline-block; padding:10px 20px; background:#007bff; color:white; border-radius:5px; text-decoration:none; margin-bottom:30px;">
   AI Audit
</a>


{% assign grouped_skills = site.skills | group_by: 'category' %}

{% for category in grouped_skills %}
  <h2>{{ category.name }}</h2>
  <div class="row row-cols-1 row-cols-md-2 g-4">
    {% for skill in category.items %}
      {% include skill-card.html skill=skill %}
    {% endfor %}
  </div>
{% endfor %}
