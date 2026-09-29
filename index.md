---
# old single-page site URLs
redirect_from:
  - /index-en.html
---

# Visual-Driven Intelligence for Surgery

**VDI Lab** is a clinical AI group at the Chang Gung Memorial Hospital Burn Center, Linkou, founded in 2025 with AI teams from National Yang Ming Chiao Tung University and Chang Gung University.
We build quantitative measurement methods and AI models — image analysis, natural language processing and multimodal learning — that surgeons can use at the bedside.

Rooted in burn care, our work extends across rhinoplasty, craniofacial and microsurgical reconstruction.

{% include section.html %}

## Research pillars

{% capture text %}
Automated assessment of burn area and depth, inhalation-injury risk prediction, and outcome research on the Chang Gung Research Database.

{% include button.html link="research" text="Burn projects" icon="fa-solid fa-arrow-right" flip=true style="bare" %}
{% endcapture %}
{% include feature.html image="images/tiles/pillar-burn.svg" link="research" title="Burn care" text=text %}

{% capture text %}
Landmark-based morphometrics for rhinoplasty, and CBCT / 3D models for orthognathic planning and bad-split risk.

{% include button.html link="research" text="Face projects" icon="fa-solid fa-arrow-right" flip=true style="bare" %}
{% endcapture %}
{% include feature.html image="images/tiles/pillar-face.svg" link="research" title="Rhinoplasty & craniofacial" flip=true text=text %}

{% capture text %}
Perfusion imaging and deep learning for monitoring free-flap circulation.

{% include button.html link="research" text="Microsurgery projects" icon="fa-solid fa-arrow-right" flip=true style="bare" %}
{% endcapture %}
{% include feature.html image="images/tiles/pillar-micro.svg" link="research" title="Microsurgical reconstruction" text=text %}

{% include section.html %}

## Highlights

<div class="project-cards">
{% assign projects = site.data.projects  %}
{% for project in projects %}
  {% include project-card.html project=project %}
{% endfor %}
</div>

{% include button.html link="code-and-data" text="Try our public demos" icon="fa-solid fa-arrow-right" flip=true %}
