---
layout: page
title: "About Me"
permalink: /about/
---

## About Me

Write about your background, interests, or your journey as an embedded software engineer.

Number of posts:
<p>Number of posts: {{ site.posts | size }}</p>

{% for post in site.posts %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <small>Posted on {{ post.date | date: "%B %-d, %Y" }}</small>
    <p>{{ post.excerpt }}</p>
  </article>
{% endfor %}
