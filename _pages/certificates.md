<!--
---
layout: default
title: Certificates
permalink: /certificates
---

<h1>Certificates</h1>

<ul>
  <li>ForHumanity Certified AI Auditor (2025)</li>
  <li>AWS Cloud Practitioner</li>
  <li>Practical Data Science on AWS</li>
  <li>Scrum Product Owner</li>
  <li>SAP Production Planning Certification</li>
</ul>
-->

---
layout: page
title: Certificates
permalink: /certificates/
description: Professional certifications and credentials
nav: true
nav_order: 4
display_categories: [AI & Cloud, Project Management, SAP]
horizontal: false
---

<!-- pages/certificates.md -->
<div class="projects">

{% if site.enable_project_categories and page.display_categories %}
  <!-- Categorized certificates -->
  {% for category in page.display_categories %}
    <a id="{{ category | slugify }}" href=".#{{ category | slugify }}">
      <h2 class="category">{{ category }}</h2>
    </a>

    {% assign categorized_certs = site.data.certificates | where: "category", category %}
    {% assign sorted_certs = categorized_certs | sort: "importance" %}

    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-1 row-cols-md-2">
          {% for cert in sorted_certs %}
            {% include certificates_horizontal.liquid %}
          {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="row row-cols-1 row-cols-md-3">
        {% for cert in sorted_certs %}
          {% include certificates.liquid %}
        {% endfor %}
      </div>
    {% endif %}
  {% endfor %}

{% else %}
  <!-- Non-categorized fallback -->
  {% assign sorted_certs = site.data.certificates | sort: "importance" %}

  {% if page.horizontal %}
    <div class="container">
      <div class="row row-cols-1 row-cols-md-2">
        {% for cert in sorted_certs %}
          {% include certificates_horizontal.liquid %}
        {% endfor %}
      </div>
    </div>
  {% else %}
    <div class="row row-cols-1 row-cols-md-3">
      {% for cert in sorted_certs %}
        {% include certificates.liquid %}
      {% endfor %}
    </div>
  {% endif %}
{% endif %}

</div>
