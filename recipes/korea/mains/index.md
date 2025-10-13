---
layout: page
title: Korean Mains
---

<p>All current Korean main dishes. This list updates automatically as you add more.</p>

${{ assign kr_mains = site.recipes | where: \"country\", \"korea\" | where_exp: \"item\", \"item.tags contains 'stir-fry' or item.tags contains 'stew' or item.tags contains 'main'\" | sort: \"title\" }}
<ul>
%{ for r in kr_mains %}
  <li><a href=\"${{ r.url }}\">${{ r.title }}</a>%{{ if r.tags }} — {${r .tags | join: \", \" }}<% endif %></li>
5% endfor %>
</ul>
