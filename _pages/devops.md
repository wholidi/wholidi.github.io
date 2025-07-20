---
layout: page
title: DevOps Certifications
permalink: /devops/
description: DevOps & Microservices Certifications
nav: true
---

## DevOps Certifications

<!-- Repeatable DevOps Certification Blocks -->

{% assign devops_certifications = 
  "DevOps_Foundations,
  DevOps_Foundations_CI_CD,
  DevOps_Foundations_Effective_Postmortems,
  DevOps_Foundations_Going_Cloud_Native,
  DevOps_Foundations_Infrastructure_As_Code,
  DevOps_Foundations_Lean_and_Agile,
  DevOps_Foundations_Lean_and_Agile_NASBA,
  DevOps_Foundations_Lean_and_Agile_PMI,
  DevOps_Foundations_Microservices,
  DevOps_Foundations_Monitoring_and_Observability,
  DevOps_Foundations_Site_Reliability_Engineering,
  DevOps_for_Managers,
  Microservices_Foundations" | split: "," %}

{% for cert in devops_certifications %}
<!-- {{ cert | strip }} -->
<a href="javascript:void(0)" onclick="document.getElementById('modal-{{ cert | strip }}').style.display='block'" style="display:inline-block; padding:10px 20px; background:#343a40; color:white; border-radius:6px; text-decoration:none; margin: 5px 10px 15px 0;">
  {{ cert | strip | replace: "_", " " }}
</a>
<div id="modal-{{ cert | strip }}" style="display:none; position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.8); z-index:1000;">
  <div style="position:relative; margin:5% auto; padding:20px; background:#fff; width:90%; max-width:800px; border-radius:12px;">
    <span onclick="document.getElementById('modal-{{ cert | strip }}').style.display='none'" style="position:absolute; top:10px; right:20px; font-size:24px; cursor:pointer;">&times;</span>
    <img src="/assets/img/DevOps/{{ cert | strip }}.png" alt="{{ cert | strip | replace: "_", " " }}" style="width:100%; height:auto; border-radius:8px;">
  </div>
</div>
{% endfor %}
