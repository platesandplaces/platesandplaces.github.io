---
layout: page
title: Vietnam — Desserts & Sweets
permalink: /recipes/vietnam/desserts/
nav: recipes
---

<ul class="recipe-list">
{% assign posts = site.recipes | where: 'country', 'vietnam' | where_exp: 'item', "item.tags contains 'dessert' or item.tags contains 'ice-cream' or item.tags contains 'sweet'" | sort: 'title' %}
{% for post in posts %}
  <li><a href="{{ post.url }}">{{ post.title }}</a> — <span class="tags">{{ post.tags | join: ', ' }}</span></li>
{% endfor %}
</ul>
