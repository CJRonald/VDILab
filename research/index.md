---
title: Research
nav:
  order: 1
  tooltip: Ongoing research projects
---

# {% include icon.html icon="fa-solid fa-microscope" %}Research

Quantitative clinical research and AI methods across four surgical domains.
Every model is trained with patient-level data splits and reported with discrimination metrics appropriate for imbalanced outcomes.

{% include section.html %}

## Burn care

<div class="project-cards">
{% assign projects = site.data.projects | where: "pillar", "burn" %}
{% for project in projects %}
  {% include project-card.html project=project %}
{% endfor %}
</div>


{% include section.html %}

## Rhinoplasty & craniofacial

<div class="project-cards">
{% assign projects = site.data.projects | where: "pillar", "face" %}
{% for project in projects %}
  {% include project-card.html project=project %}
{% endfor %}
</div>


{% include section.html %}

## Microsurgical reconstruction

<div class="project-cards">
{% assign projects = site.data.projects | where: "pillar", "micro" %}
{% for project in projects %}
  {% include project-card.html project=project %}
{% endfor %}
</div>

