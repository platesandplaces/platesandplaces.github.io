---
layout: page
title: Korea — Sides & Banchan
permalink: /recipes/korea/sides/
nav: recipes
---

<p class="lead">Quick sides, pickles and small dishes to round out a Korean meal.</p>

<ul class="recipe-list">
{% assign posts = site.recipes | where: 'country', 'korea' | where_exp: 'item', "item.tags contains 'side' or item.tags contains 'banchan' or item.tags contains 'salad' or item.tags contains 'pickle'" | sort: 'title' %}
{% for post in posts %}
  <li><a href="{{ post.url }}">{{ post.title }}</a> — <span class="tags">{{ post.tags | join: ', ' }}</span></li>
{% endfor %}
</ul>
