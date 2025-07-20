---
layout: page
title: Threat Modeling
permalink: /threat/
description: Threat Modeling Certifications
nav: true
---

## Threat Modeling

<!-- Creative Problem Solving -->
<a href="javascript:void(0)" onclick="document.getElementById('modal-threat-cps').style.display='block'" style="display:inline-block; padding:10px 20px; background:#dc3545; color:white; border-radius:6px; text-decoration:none; margin: 5px 10px 15px 0;">
  Creative Problem Solving for Technologists
</a>
<div id="modal-threat-cps" style="display:none; position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.8); z-index:1000;">
  <div style="position:relative; margin:5% auto; padding:20px; background:#fff; width:90%; max-width:800px; border-radius:12px;">
    <span onclick="document.getElementById('modal-threat-cps').style.display='none'" style="position:absolute; top:10px; right:20px; font-size:24px; cursor:pointer;">&times;</span>
    <img src="/assets/img/Threat_Modeling/Creative_Problem_Solving_for_Technologists.png" alt="Creative Problem Solving for Technologists" style="width:100%; height:auto; border-radius:8px;">
  </div>
</div>

<!-- Threat Modeling Certifications -->
{% assign threat_certs = "Denial_of_Service_and_Elevation_of_Privilege,Information_Disclosure_in_Depth,Repudiation_in_Depth,Tampering_in_Depth,for_AIML_Systems,for_Security_Professionals" | split: "," %}
{% for cert in threat_certs %}
<a href="javascript:void(0)" onclick="document.getElementById('modal-threat-{{ cert }}').style.display='block'" style="display:inline-block; padding:10px 20px; background:#dc3545; color:white; border-radius:6px; text-decoration:none; margin: 5px 10px 15px 0;">
  Threat Modeling {{ cert | replace: "_", " " }}
</a>
<div id="modal-threat-{{ cert }}" style="display:none; position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.8); z-index:1000;">
  <div style="position:relative; margin:5% auto; padding:20px; background:#fff; width:90%; max-width:800px; border-radius:12px;">
    <span onclick="document.getElementById('modal-threat-{{ cert }}').style.display='none'" style="position:absolute; top:10px; right:20px; font-size:24px; cursor:pointer;">&times;</span>
    <img src="/assets/img/Threat_Modeling/Threat_Modeling_{{ cert }}.png" alt="Threat Modeling {{ cert | replace: "_", " " }}" style="width:100%; height:auto; border-radius:8px;">
  </div>
</div>
{% endfor %}
