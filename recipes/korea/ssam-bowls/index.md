---
layout: page
title: Korea — Ssam Lunch Bowls
permalink: /recipes/korea/ssam-bowls/
nav: recipes
---

<p class="lead">Build‑your‑own wraps (쌈): beef + rice + leaves + a simple dip, plus packable sides. Assemble at the table.</p>

<ul class="recipe-list">
{% assign posts = site.recipes | where: 'country', 'korea' | where_exp: 'item', "item.tags contains 'ssam'" | sort: 'title' %}
{% for post in posts %}
  <li><a href="{{ post.url }}">{{ post.title }}</a> — <span class="tags">{{ post.tags | join: ', ' }}</span></li>
{% endfor %}
</ul>
