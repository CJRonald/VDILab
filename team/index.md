---
title: Team
nav:
  order: 4
  tooltip: About our team
---

# {% include icon.html icon="fa-solid fa-users" %}Team

An interdisciplinary team of surgeons and computer scientists from Chang Gung Memorial Hospital, National Yang Ming Chiao Tung University and Chang Gung University.

{% include section.html %}

{% include list.html data="members" component="portrait" filter="role == 'principal-investigator'" %}
{% include list.html data="members" component="portrait" filter="role == 'faculty' or role == 'clinical-faculty'" %}
{% include list.html data="members" component="portrait" filter="role != 'principal-investigator' and role != 'faculty' and role != 'clinical-faculty'" %}
