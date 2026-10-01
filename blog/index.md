---
layout: default
title: Posts
description: >-
  Research notes and explanations about metallobiochemistry, enzyme design, computational analysis, and research software.
permalink: /blog/
---

# Posts

<hr>

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>{{ post.date | date: "%b %d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>

{% if site.posts == empty %}
<p>No posts yet.</p>
{% endif %}
