---
title: Eleventy
layout: page
date: 2025-03-23
eleventyNavigation:
  key: Eleventy
  parent: Blog
---
{% set navPages = collections.post | eleventyNavigation("Eleventy") %}

<ul>
{% for item in navPages %}
<li><a href="{{ item.url }}">{{ item.title }}</a></li>
{% endfor %}
</ul>