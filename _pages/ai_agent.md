---
layout: page
title: AI Agent
permalink: /ai_agent/
description: AI Agent Certifications
nav: true
---

## AI Agent

<!-- AI Agent Certifications -->
{% assign agent_certs = "Lang_Chain_Apps,Lang_Chain_Chat,Lang_Chain_Function_Tools,Multi_Agent_Badge" | split: "," %}
{% for cert in agent_certs %}
<a href="javascript:void(0)" onclick="document.getElementById('modal-agent-{{ cert }}').style.display='block'" style="display:inline-block; padding:10px 20px; background:#343a40; color:white; border-radius:6px; text-decoration:none; margin: 5px 10px 15px 0;">
  {{ cert | replace: "_", " " }}
</a>
<div id="modal-agent-{{ cert }}" style="display:none; position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.8); z-index:1000;">
  <div style="position:relative; margin:5% auto; padding:20px; background:#fff; width:90%; max-width:800px; border-radius:12px;">
    <span onclick="document.getElementById('modal-agent-{{ cert }}').style.display='none'" style="position:absolute; top:10px; right:20px; font-size:24px; cursor:pointer;">&times;</span>
    <img src="/assets/img/AI_Agent/{{ cert }}.png" alt="{{ cert | replace: "_", " " }}" style="width:100%; height:auto; border-radius:8px;">
  </div>
</div>
{% endfor %}
