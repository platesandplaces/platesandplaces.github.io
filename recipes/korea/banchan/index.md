---
layout: page
title: Korean Banchan
---

<p>Small plates, snacks, and sides to round out a Korean meal. This list updates automatically as you add more.</p>

{% assign items = site.recipes | where: "country", "korea" | where_exp: "r", "r.tags contains 'banchan' or r.tags contains 'side' or r.tags contains 'snack'" | sort: "title" %}
<ul>
{% for r in items %}
  <li><a href="{{ r.url }}">{{ r.title }}</a>{% if r.tags %} · {{ r.tags | join: ", " }}{% endif %}</li>
{% endfor %}
</ul>
