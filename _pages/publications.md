---
layout: page
permalink: /research/
title: research
description:
nav: true
nav_order: 2
---

<!-- _pages/research.md -->
<div class="publications">
  {% bibliography --group_by none --query @*[accepted=true]* %}
</div>

