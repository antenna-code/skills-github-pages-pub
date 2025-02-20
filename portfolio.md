---
layout: page
title: "Portfolio"
permalink: /portfolio/
---

## Portfolio Projects

<ul>
  {% for project in site.data.projects %}
    <li>
      <strong>{{ project.name }}</strong>: {{ project.description }}
      (<a href="{{ project.url }}">Learn more</a>)
    </li>
  {% endfor %}
</ul>