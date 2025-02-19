---
layout: default
title: "Blog"
permalink: /blog/
---
# Blog

Welcome to my blog. Here are my latest posts:

{% for post in site.posts %}
<article>
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <small>Posted on {{ post.date | date: "%B %-d, %Y" }}</small>
  <p>{{ post.excerpt }}</p>
</article>
{% endfor %}

Number of posts!:
<p>Number of posts: {{ site.posts | size }}</p>