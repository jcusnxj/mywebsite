---
title: blog
layout: base
eleventyNavigation:
  key: Blog
---
<section class="blog-feed">

{% set navPages = collections.post | reverse %}

{% for item in navPages %}
<article class="blog-post">
<div class="post-title"><a href="{{ item.url }}">{{ item.data.title }}</a></div>
<p class="post-date">{{ item.data.date | dateObject("LLL d, yyyy") }}</p>
<p class="post-excerpt">{{ item.page.excerpt }}</p>
</article>
{% endfor %}

</section>   



