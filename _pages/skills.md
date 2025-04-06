---
layout: page
title: Skills
permalink: /skills/
description: Certified skills and competencies
nav: true
nav_order: 5
---

<h1>Skills Overview</h1>

<div class="row row-cols-1 row-cols-md-2 g-4">
  {% assign skills = site.skills | sort: "importance" %}
  {% for skill in skills %}
    {% include skills.liquid skill=skill %}
  {% endfor %}
</div>
