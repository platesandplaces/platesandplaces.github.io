---
layout: page
title: Philippines — Soups & Stews
---

<p>Sour, savoury, and comforting Filipino soups and stews. This list updates automatically as you add more recipes.</p>

{% assign items = site.recipes | where: "country", "philippines" | where_exp: "r", "r.tags contains 'soup' or r.tags contains 'stew'" | sort: "title" %}
<ul>
{% for r in items %}
  <li><a href="{{ r.url }}">{{ r.title }}</a>{% if r.tags %} · {{ r.tags | join: ", " }}{% endif %}</li>
{% endfor %}
</ul>
