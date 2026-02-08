---
layout: page
title: "Tools"
permalink: /tools/
---


<ul>
{% for tool in site.data.tools %}
  <li>
    <a href="{{ tool.url }}">{{ tool.name }}</a><br>
    <small>{{ tool.description }}</small>
  </li>
{% endfor %}
</ul>
