---
layout: page
title: Philippines — Soups & Stews
---

<p>Comforting Filipino soups and stews. This list updates automatically as new recipes are added.</p>

{% assign ph_soups = site.recipes | where: "country", "philippines" | where_exp: "r", "r.tags contains 'soup' or r.tags contains 'stew'" | sort: "title" %}
<ul>
{% for r in ph_soups %}
  <li><a href="{{ r.url }}">{{ r.title }}</a>{% if r.tags %} · {{ r.tags | join: ", " }}{% endif %}</li>
{% endfor %}
</ul>
