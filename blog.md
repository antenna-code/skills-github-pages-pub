---
layout: default
title: "Blog"
permalink: /blog/
---
# Blog
Welcome to my blog

<p>Number of posts: {{ site.posts | size }}</p>

{% for post in site.posts %}
  <article>
    <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
    <small>Posted on {{ post.date | date: "%B %-d, %Y" }}</small>
  </article>
{% endfor %}



