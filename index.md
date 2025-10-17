---
layout: default
title: Plates & Places
---

# Plates & Places

_A little corner for recipes & food notes — more landing content coming soon._

- 👉 <a href="/recipes/">Browse all recipes</a>
- 🇯🇵 Japan · 🇰🇷 Korea · 🇻🇳 Vietnam · 🇵🇭 Philippines · 🇪🇸 Spain · 🇫🇷 France

---

## Latest Recipe

{% assign by_date = site.recipes | where_exp: 'r', 'r.date' | sort: 'date' | reverse %}
{% if by_date.size > 0 %}
  {% assign latest = by_date.first %}
{% else %}
  {% assign latest = site.recipes | sort: 'path' | last %}
{% endif %}

{% if latest %}
<div class="card">
  <h3><a href="{{ latest.url }}">{{ latest.title }}</a></h3>
  <p>{{ latest.summary }}</p>
  <small>{{ latest.cuisine }} • {{ latest.tags | join: ', ' }}</small>
</div>
{% else %}
<p>Recipes coming soon.</p>
{% endif %}
