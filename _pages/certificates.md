---
layout: page
title: Certificates
permalink: /certificates/
description: Professional certifications by category
nav: true
nav_order: 4
---

<h1>📜 Certificates by Domain</h1>

<div class="row row-cols-1 row-cols-md-3">
  {% assign sorted_certs = site.data.certificates | sort: "importance" %}
  {% for cert in sorted_certs %}
    {% include certificates.liquid %}
  {% endfor %}
</div>
