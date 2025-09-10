---
layout: default
title: Home
---
# Data analyst blogs 

{% for post in site.posts %}
<article>
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>

</article>
{% endfor %}
