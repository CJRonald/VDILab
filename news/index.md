---
title: News
nav:
  order: 5
  tooltip: Lab news
---

# {% include icon.html icon="fa-solid fa-newspaper" %}News

Announcements, releases and funding news from VDI Lab.

{% include section.html %}

{% include search-box.html %}

{% include tags.html tags=site.tags %}

{% include search-info.html %}

{% include list.html data="posts" component="post-excerpt" %}
