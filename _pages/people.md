---
layout: page
title: People
permalink: /people/
description:
nav: true
nav_order: 2
---

{% comment %}
Setting 1: detailed profile cards are preserved in `_includes/lab_people_cards.html`.
This page currently uses the simpler gallery layout.
{% endcomment %}

{% include lab_people_cards.html people=site.data.people %}
