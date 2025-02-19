---
layout: page
title: "Team"
permalink: /team/
---

## Meet the Team

<ul>
  {% for member in site.data.team %}
    <li>
      <strong>{{ member.name }}</strong> – {{ member.role }} (<a href="{{ member.github }}">GitHub</a>)
    </li>
  {% endfor %}
</ul>