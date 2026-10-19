---
layout: page
permalink: /talks/
title: talks
nav: true
nav_order: 4
---

### Panels

<ul class="talks-list">
{% for t in site.data.talks.panels %}{% include talk_item.liquid t=t %}{% endfor %}
</ul>

### Industry and policy talks

<ul class="talks-list">
{% for t in site.data.talks.industry %}{% include talk_item.liquid t=t %}{% endfor %}
</ul>

### Invited seminars

<ul class="talks-list">
{% for t in site.data.talks.seminars %}{% include talk_item.liquid t=t %}{% endfor %}
</ul>

### Conference presentations

<ul class="talks-list">
{% for c in site.data.talks.conferences %}
  <li>{{ c.title }}: {{ c.venues }}</li>
{% endfor %}
</ul>
