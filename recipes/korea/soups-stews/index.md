---
layout: page
title: Korean Soups & Stews
---

<p>Hearty stews and comforting soups from Korea. This list updates automatically as you add more recipes.</p>

{% assign items = site.recipes | where: "country", "korea" | where_exp: "r", "r.tags contains 'stew' or r.tags contains 'soup'" | sort: "title" %}
<ul>
{% for r in items %}
  <li><a href="{{ r.url }}">{{ r.title }}</a>{% if r.tags %} · {{ r.tags | join: ", " }}{% endif %}</li>
{% endfor %}
</ul>
