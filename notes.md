---
layout: page
title: Notes
permalink: /notes/
---

## My Collection of Notes

<ul>
  {% for note in site.notes %}
    <li>
      <a href="{{ note.url | relative_url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>
