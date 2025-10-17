---
layout: page
title: Korea — Soups & Stews
---

<p>Comforting bowls from Korea — everyday soups (<em>guk</em>) and hearty stews (<em>jjigae</em>). This list updates automatically.</p>

{% assign kr_soups = site.recipes | where: "country", "korea" | where_exp: "r", "r.tags contains 'soup' or r.tags contains 'stew'" | sort: "title" %}
<ul>
{% for r in kr_soups %}
  <li><a href="{{ r.url }}">{{ r.title }}</a>{% if r.tags %} · {{ r.tags | join: ", " }}{% endif %}</li>
{% endfor %}
</ul>
