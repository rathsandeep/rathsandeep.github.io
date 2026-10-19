---
layout: page
permalink: /research/
title: research
description:
nav: true
nav_order: 2
---

<!-- _pages/research.md -->
<p class="research-profiles">
  <a href="https://scholar.google.com/citations?user={{ site.scholar_userid }}" target="_blank" rel="noopener"><i class="ai ai-google-scholar"></i> Google Scholar</a>
  <span class="sep">&middot;</span>
  <a href="https://orcid.org/{{ site.orcid_id }}" target="_blank" rel="noopener"><i class="ai ai-orcid"></i> ORCID</a>
</p>


<div class="show-abstracts">

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

</div>

