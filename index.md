---
layout: home
title: "Welcome"
permalink: /
---
# Welcome to My Website
This is the landing page of my site.

{% for post in site.posts %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <small>Posted on {{ post.date | date: "%B %-d, %Y" }}</small>
    <p>{{ post.excerpt }}</p>
  </article>
{% endfor %}