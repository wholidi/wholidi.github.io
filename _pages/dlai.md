---
layout: page
title: DeepLearning.AI Certifications
permalink: /dlai/
description: DLAI Certified Skills in Machine Learning and Deep Learning
nav: true
---

## DeepLearning.AI Certifications

<!-- Helper function to reduce repetition -->
{% assign base_path = "/assets/img/DLAI/" %}

{% assign certs = "AI_for_Everyone, Basic_Generative_Adversarial_Networks, DLAI_Advance_Learning_Algorithms, DLAI_Auto_ML_Analyze_Datasets_and_Model_Train, DLAI_Convolutional_Neural_Network, DLAI_Deep_Learning, DLAI_Deploy_ML_Model_in_Production, DLAI_Improving_Deep_Neural_Network, DLAI_Intro_to_Machine_Learning, DLAI_Intro_to_Tensor_Flow, DLAI_MLOPs, DLAI_ML_Data_Lifecycle_in_Production, DLAI_Machine_Learning, DLAI_Machine_Learning_Modelling_Pipelines_in_Production, DLAI_Neural_Network_and_Deep__Learning, DLAI_Sequence_Time_Series_and_Prediction, DLAI_Spv_ML_Regression_Classification, DLAI_Structure_Machine_Learning_Project, DLAI_Tensor_Flow_Developer, DLAI_Unsupervised_Learning, Full_Stack_Deep_Learning_with_Python" | split: ", " %}

{% for cert in certs %}
<a href="javascript:void(0)" onclick="document.getElementById('modal-{{ cert }}').style.display='block'" style="display:inline-block; padding:10px 20px; background:#343a40; color:white; border-radius:6px; text-decoration:none; margin: 5px 10px 15px 0;">
  {{ cert | replace: "_", " " | replace: "DLAI ", "" }}
</a>

<div id="modal-{{ cert }}" style="display:none; position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.8); z-index:1000;">
  <div style="position:relative; margin:5% auto; padding:20px; background:#fff; width:90%; max-width:800px; border-radius:12px;">
    <span onclick="document.getElementById('modal-{{ cert }}').style.display='none'" style="position:absolute; top:10px; right:20px; font-size:24px; cursor:pointer;">&times;</span>
    <img src="{{ base_path }}{{ cert }}.png" alt="{{ cert | replace: "_", " " }}" style="width:100%; height:auto; border-radius:8px;">
  </div>
</div>
{% endfor %}
