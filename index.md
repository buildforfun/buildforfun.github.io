---
layout: default
title: Home
---

# My knowledge

## Life
{% for post in site.categories.life %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  </article>
{% endfor %}

## Psychology
{% for post in site.categories.psychology %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  </article>
{% endfor %}

## Building Energy Modelling
{% for post in site.categories.bem %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  </article>
{% endfor %}

## Computer Science
{% for post in site.categories.comp %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  </article>
{% endfor %}


## Foundational knowledge
{% for post in site.categories.foundation %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  </article>
{% endfor %}

## TODO Pet projects

