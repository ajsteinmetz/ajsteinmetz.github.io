## About 🔭

### Notes on Introductory Electricity and Magnetism
<ul>
  {% for note in site.notes %}
    <li>
      <a href="{{ note.url | relative_url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

### Blog Posts
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>
