---
name: "maxime grangier"
---

<h1>{{ page.name }}</h1>
<h2>{{ page.position }}</h2>

  {% assign filtered_posts = site.posts | where: 'author', page.name %}
  {% for post in filtered_posts %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}