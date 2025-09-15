---
layout: default
title: Home
---
# My knowledge

{% for post in site.posts %}
<article>
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>

## Psychology
{% for post in site.categories.psychology %}

</article>
{% endfor %}
