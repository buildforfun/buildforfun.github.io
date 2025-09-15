---
layout: default
title: Home
---

# My knowledge

## Psychology

{% for post in site.categories.psychology %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  </article>
{% endfor %}

## All Posts

{% for post in site.posts %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  </article>
{% endfor %}
