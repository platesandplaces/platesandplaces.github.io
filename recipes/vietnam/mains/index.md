---
layout: page
title: Vietnam — Mains
---

<p>Everyday Vietnamese mains — stir-fries, braises, noodle and rice dishes. This list updates automatically as you add more.</p>

{% assign vn_mains = site.recipes | where: "country", "vietnam" | where_exp: "r", "r.tags contains 'main' or r.tags contains 'stir-fry' or r.tags contains 'braise' or r.tags contains 'curry' or r.tags contains 'grill' or r.tags contains 'noodles' or r.tags contains 'rice'" | sort: "title" %}
<ul>
{% for r in vn_mains %}
  <li><a href="{{ r.url }}">{{ r.title }}</a>{% if r.tags %} · {{ r.tags | join: ", " }}{% endif %}</li>
{% endfor %}
</ul>
