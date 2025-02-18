---
layout: default
title: "Welcome to my blog"
---

<h1>Welcome to my blog</h1>

{% for post in site.posts %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt }}</p>
  </article>
{% endfor %}
