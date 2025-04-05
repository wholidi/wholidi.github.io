---
layout: page
title: Certificates
permalink: /certificates/
description: Professional certifications
nav: true
nav_order: 4
---

<h1>📜 Certificates</h1>

<div class="row row-cols-1 row-cols-md-2">
  {% assign sorted_certs = site.data.certificates %}
  {% for cert in sorted_certs %}
    {% include certificates.liquid %}
  {% endfor %}
</div>
