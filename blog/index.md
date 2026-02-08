---
layout: default
title: Posts
permalink: /blog/
---
<h1>Posts</h1>

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <small>— {{ post.date | date: "%b %d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>

{% if site.posts == empty %}
<p>No posts yet.</p>
{% endif %}
