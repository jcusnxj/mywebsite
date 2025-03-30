---
title: Eleventy
eleventyNavigation:
  key: Eleventy
  parent: Notes
---
{% set navPages = collections.note | eleventyNavigation("Eleventy") %}

<ul>
{% for item in navPages %}
<li><a href="{{ item.url }}">{{ item.title }}</a></li>
{% endfor %}
</ul>