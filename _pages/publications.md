---
layout: page
permalink: /research/
title: research
description:
nav: true
nav_order: 2
---

<!-- _pages/research.md -->
<h2>published & accepted papers</h2>
<div class="publications">
  {% bibliography --group_by none --query @*[accepted=true]* %}
</div>

<h2>working papers</h2>
<div class="publications">
  {% bibliography --group_by none --query @*[working=true]* %}
</div>

<h2>work in progress</h2>
<div class="publications">
  {% bibliography --group_by none --query @*[inprogress=true]* %}
</div>

