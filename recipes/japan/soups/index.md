---
layout: page
title: Japan — Soups, Broths & Miso
permalink: /recipes/japan/soups/
nav: recipes
---

<ul class="recipe-list">
{% assign posts = site.recipes | where: 'country', 'japan' | where_exp: 'item', "item.tags contains 'soup' or item.tags contains 'miso' or item.tags contains 'dashi' or item.tags contains 'broth' or item.tags contains 'stock'" | sort: 'title' %}
{% for post in posts %}
  <li><a href="{{ post.url }}">{{ post.title }}</a> — <span class="tags">{{ post.tags | join: ', ' }}</span></li>
{% endfor %}
</ul>
