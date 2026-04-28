---
layout: page
title: Publications
permalink: /publications/
description:
nav: true
nav_order: 4
---

<div class="lab-publication-list">
  {% for item in site.data.publications %}
    <article class="lab-publication-card">
      <p class="lab-publication-meta">{{ item.venue }} &middot; {{ item.year }}</p>
      <h2><a href="{{ item.link }}">{{ item.title }}</a></h2>
      <p class="lab-publication-authors">{{ item.authors }}</p>
      <p>{{ item.summary }}</p>
    </article>
  {% endfor %}
</div>
