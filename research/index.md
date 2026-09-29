---
title: Research
nav:
  order: 1
  tooltip: Ongoing research projects
---

# {% include icon.html icon="fa-solid fa-microscope" %}Research

Quantitative clinical research and AI methods across four surgical domains.
Our methods standard is patient-level train/test splitting and discrimination metrics suited to imbalanced outcomes.

{% include search-box.html %}

{% include search-info.html %}

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

