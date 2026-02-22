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
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h3>
    </li>
  {% endfor %}
</ul>
