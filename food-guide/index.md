---
layout: page
title: Food Guide
---

Explore places I recommend eating — restaurants, cafés, markets and street food.

## Browse by country
- [Japan](/food-guide/japan/)

## Latest
{% assign latest = site.eats | sort: "date" | reverse | slice: 0, 12 %}
<ul>
{% for e in latest %}
  <li><a href="{{ e.url }}">{{ e.title }}</a>{% if e.venue_type %} — <em>{{ e.venue_type }}</em>{% endif %}{% if e.city %} · {{ e.city | capitalize }}{% endif %}</li>
{% endfor %}
</ul>
