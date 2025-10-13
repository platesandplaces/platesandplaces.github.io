---
layout: page
title: Vietnam — Sides & Condiments
---

<p>Quick pickles, dips, sauces and simple sides that round out Vietnamese meals. This list updates automatically as you add more.</p>

{% assign vn = site.recipes | where: "country", "vietnam" | sort: "title" %}
<ul>
{% for r in vn %}
  <li><a href="{{ r.url }}">{{ r.title }}</a>{% if r.tags %} · {{ r.tags | join: ", " }}{% endif %}</li>
{% endfor %}
</ul>
