---
layout: page
permalink: /talks/
title: talks
nav: true
nav_order: 4
---

### Invited seminars

{% assign seminar_years = site.data.talks.seminars | group_by: 'year' | sort: 'name' | reverse %}
{% for y in seminar_years %}
<h5 class="talks-year">{{ y.name }}</h5>
<ul class="talks-list">
{% for t in y.items %}<li>{{ t.event }}{% if t.location %}, {{ t.location }}{% endif %}</li>{% endfor %}
</ul>
{% endfor %}

### Conference presentations

{% assign conf_years = site.data.talks.conferences | group_by: 'year' | sort: 'name' | reverse %}
{% for y in conf_years %}
<h5 class="talks-year">{{ y.name }}</h5>
<ul class="talks-list">
{% for t in y.items %}<li>{{ t.event }}{% if t.location %} ({{ t.location }}){% endif %}: {{ t.paper }}{% if t.note %} ({{ t.note }}){% endif %}</li>{% endfor %}
</ul>
{% endfor %}

### Panels and industry talks

<ul class="talks-list">
{% for t in site.data.talks.panels %}{% include talk_item.liquid t=t %}{% endfor %}
{% for t in site.data.talks.industry %}{% include talk_item.liquid t=t %}{% endfor %}
</ul>
