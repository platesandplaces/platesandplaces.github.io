---
layout: page
title: Vietnam — Mains
---

<p>Main dishes from Vietnam — stir-fries, braises and grilled favourites. This list updates automatically as you add more.</p>

{% assign vn_mains = site.recipes | where: "country", "vietnam" | where_exp: "r", "r.tags contains 'main'" | sort: "title" %}
<ul>
{% for r in vn_mains %}
  <li><a href="{{ r.url }}">{{ r.title }}</a>{% if r.tags %} · {{ r.tags | join: ", " }}{% endif %}</li>
{% endfor %}
</ul>
