---
layout: page
title: All Recipes
permalink: /recipes/
nav: recipes
---

<p class="lead">Browse everything in one place. Grouped by cuisine.</p>

{% assign countries = site.recipes | map: 'country' | uniq | sort %}
{% for c in countries %}
### {{ c | capitalize }}
<ul class="recipe-list">
  {% assign items = site.recipes | where: 'country', c | sort: 'title' %}
  {% for r in items %}
    <li><a href="{{ r.url }}">{{ r.title }}</a> — <span class="tags">{{ r.tags | join: ', ' }}</span></li>
  {% endfor %}
</ul>
{% endfor %}
