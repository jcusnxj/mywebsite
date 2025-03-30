---
title: Notes
layout: note
eleventyNavigation:
  key: Notes
---
{% set navPages = collections.all | eleventyNavigation("Notes") %}

<ul>
{% for item in navPages %}
<li><a href="{{ item.url }}">{{ item.title }}</a></li>
{% endfor %}
</ul>