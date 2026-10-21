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
  <span class="sep">&middot;</span>
  <a href="https://papers.ssrn.com/sol3/cf_dev/AbsByAuth.cfm?per_id=1601088" target="_blank" rel="noopener"><i class="ai ai-ssrn"></i> SSRN</a>
</p>


<h3>Research themes</h3>
<div class="themes">
  {% for t in site.data.themes %}
    <div class="theme">
      <div class="theme-name">{{ t.name }}</div>
      <div class="theme-summary">{{ t.summary }}</div>
      <ul class="theme-papers">
        {% for p in t.papers %}<li>{{ p }}</li>{% endfor %}
      </ul>
    </div>
  {% endfor %}
</div>

<div class="show-abstracts pub-timeline">

<h3>Published and accepted papers</h3>
<div class="publications">
  {% bibliography --group_by year --group_order descending --query @*[accepted=true]* %}
</div>

<h3>Working papers</h3>
<div class="publications">
  {% bibliography --group_by year --group_order descending --query @*[working=true]* %}
</div>

<h3>Work in progress</h3>
<div class="publications no-years">
  {% bibliography --group_by none --query @*[inprogress=true]* %}
</div>

</div>

