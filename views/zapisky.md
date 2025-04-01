---
title: Zápisky
layout: base
eleventyNavigation:
  key: Zápisky
  parent: 80fk
---
{% set navPages = collections.all | eleventyNavigation("Zápisky") %}

<ul>
{% for item in navPages %}
<li><a href="{{ item.url }}">{{ item.title }}</a></li>
{% endfor %}
</ul>