---
# Comment - this is frontmatter
layout : home
---

Welcome to the new LXD blog.

{% for post in site.posts %}
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p>{{ post.excerpt }}</p>
{% endfor %}
