---
title: Code and Data
nav:
  order: 2
  tooltip: Public demos and tools
---

# {% include icon.html icon="fa-solid fa-code" %}Code and Data

{% include alert.html type="warning" content="All demos are **research prototypes**, not clinical tools. They must not be used for diagnosis or treatment decisions." %}

{% include section.html %}

## Public demos

{% capture col1 %}
{% include card.html image="images/tiles/burn-segmentation.svg" link="https://huggingface.co/spaces/CJRonald/burn-segmentation-demo" title="Burn segmentation demo" subtitle="Hugging Face Space" description="Upload a burn photograph and see the wound outlined by a deep-supervision UNet++. Images are processed in memory and not stored." tags="burn, segmentation" %}
{% endcapture %}
{% capture col2 %}
{% include card.html image="images/tiles/flap.svg" link="https://huggingface.co/spaces/CJRonald/flap-prediction-demo" title="Flap circulation demo" subtitle="Hugging Face Space" description="A ResNet18 region-of-interest model that classifies free-flap circulation from a flap photograph." tags="microsurgery, perfusion" %}
{% endcapture %}
{% include cols.html col1=col1 col2=col2 %}

{% include section.html %}

## Annotation tools

We build in-house, browser-only annotation tools (landmarks, tissue masks) for our reliability studies.
Photographs are processed on the annotator's device and never uploaded.
These tools are shared with study raters directly rather than listed here.

## Data

Clinical data used in our studies are governed by Chang Gung Medical Foundation IRB approvals and Taiwan's Personal Data Protection Act, and cannot be shared publicly.
