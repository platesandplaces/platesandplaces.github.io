---
layout: page
title: France — Sides
---

<p>Classic French sides to round out a meal — from gratins to simple vegetables. This list updates automatically as you add more.</p>

{% assign fr_sides = site.recipes | where: "country", "france" | where_exp: "r", "r.tags contains 'side' or r.tags contains 'gratin' or r.tags contains 'salad' or r.tags contains 'vegetable'" | sort: "title" %}
<ul>
{% for r in fr_sides %}
  <li><a href="{{ r.url }}">{{ r.title }}</a>{% if r.tags %} · {{ r.tags | join: ", " }}{% endif %}</li>
{% endfor %}
</ul>
