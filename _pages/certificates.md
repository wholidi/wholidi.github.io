---
layout: page
title: Certificates
permalink: /certificates/
description: Certifications grouped by domain
nav: true
nav_order: 4
---

<h1>📜 Certificates</h1>

<div class="row row-cols-1 row-cols-md-3">
  {% assign certs = site.certificates | sort: "importance" %}
  {% for certificate in certs %}
    {% include certificates.liquid certificate=certificate %}
  {% endfor %}
</div>
